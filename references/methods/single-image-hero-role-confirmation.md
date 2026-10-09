# Single-Image Hero Role Confirmation Gate

## Scope and precedence
For any **finished static main-visual, hero, or promotional-poster request that explicitly asks for exactly ONE image**, the requested image count is confirmed (`SINGLE_EXPLICIT`), but **its Hero role is NOT implicitly confirmed**. A final image must be either:

- `PRODUCT_HERO` / **Hero A** — product-first presentation of verified form/material/design and product desire, or
- `USAGE_HERO` / **Hero B** — genuine active use of the product by a person, hand, pet or other category-valid actor, emphasizing practical or emotional use experience.

The distinction is a **client-owned consequential output choice**, not a designer-owned camera or styling choice. It requires confirmation when the brief does not already clearly settle it.

**This gate overrides any legacy "one unspecified hero defaults to Product Hero" or "choose the more plausible role" rule.** It operates alongside the mandatory missing-input/No Placeholders gate; both must PASS independently before any final single-image generation. Do not silently relabel an ambiguous single image as product-focused.

## Classification and client interaction

1. **No explicit image count** — keep existing two-complete-poster default: `DUAL_DEFAULT` with Hero A + active Hero B; do not ask about picking just one.
2. **Explicitly one image + clearly specified product presentation** — set `SINGLE_EXPLICIT`, `selected_hero_role: PRODUCT_HERO`, `role_confirmation_source: USER_EXPLICIT`; no repeated role question. Examples: "只做一张 Hero A", "只要一张产品展示版", "一张主要拍产品本体的海报".
3. **Explicitly one image + clearly specified active-use presentation** — set `SINGLE_EXPLICIT`, `selected_hero_role: USAGE_HERO`, `role_confirmation_source: USER_EXPLICIT`; no repeated role question. Examples: "只做一张 Hero B", "一张真实佩戴使用场景海报", "一张人在运动中使用手表的广告". Show genuine active use, not a lifestyle subject merely nearby.
4. **Explicitly one image + NO role specified** — set `selected_hero_role: null`, `single_image_hero_role_gate: BLOCKED_AWAITING_USER`, ask and WAIT: **"这张你要的是 Hero A（产品展示型），还是 Hero B（真实使用场景型）？"** Only after an affirmative user answer is the gate PASS.
5. **Explicitly one image + "你帮我选" / asks for recommendation** — propose a reasoned recommendation and request an explicit decision: e.g. "建议 Hero A，更能突出产品外观与材质。确认这张按 Hero A 做吗？" Mark `RECOMMENDED_AWAITING_CONFIRMATION` (still blocks production). A recommendation is NOT approval. User confirmation then locks the recommended role.
6. **Role ambiguous or contradictory** — ask one role-choice question; do not assume. After clarification, persist the chosen role. When the user later changes role, invalidate dependent production plans and replan before generation.

**Aspect ratio 4:5, platform, "成品海报", "主视觉", "新品促销", "一张", or "one final poster" are NOT Hero role specifications.** They must not be used as grounds to pick A or B. A product reference photo alone does not confirm the role. Existing project decisions can be reused only when explicitly confirmed for the active task under source-scope rules.

## Gate/state contract

```yaml
single_image_hero_role_confirmation:
  applies: false # true only when the client requested exactly one final image
  explicit_image_count: null # 1 for SINGLE_EXPLICIT
  selected_hero_role: null # PRODUCT_HERO | USAGE_HERO | null
  role_confirmation_source: null # USER_EXPLICIT | USER_CONFIRMED_AFTER_QUESTION | null
  recommendation: null # non-binding until confirmed
  status: NOT_APPLICABLE # NOT_APPLICABLE | NOT_CHECKED | BLOCKED_AWAITING_USER | RECOMMENDED_AWAITING_CONFIRMATION | PASS
  pending_question: null
  confirmed_in_current_project: false
```

**Production readiness and final-delivery hard gates:**
- If `SINGLE_EXPLICIT`, demand `single_image_hero_role_confirmation.status == PASS` AND selected role in `PRODUCT_HERO | USAGE_HERO` AND confirmed source.
- `BLOCKED_AWAITING_USER`, `RECOMMENDED_AWAITING_CONFIRMATION` and `NOT_CHECKED` all forbid **image generation, finished deliverable, "已完成" / approval-ready status, or silent fallback**.
- Never generate two when exactly one was requested. Never generate one under the default dual contract unless the user explicitly changes the count.
- The separate mandatory input gate checks platform and missing commercial/product facts. If both gates have missing decisions, ask clearly and efficiently; avoid repeat questions; proceed autonomously with ordinary design after confirmation.
- Keep Product Hero Impact / active Usage Authenticity and all product truth, typography, integration and final-delivery QA applicable to the confirmed role.

## Regression scenarios (behavioral expectations, not executed render tests)

| Scenario | Expected behavior |
|---|---|
| "只要一张" | ASK A or B; wait; no final image call |
| "只做一张 4:5 成品海报" | ASK A or B; ratio does not decide role |
| "一张产品展示版" | PRODUCT_HERO; do not ask role again |
| "只要一张真实使用场景版" | USAGE_HERO; do not ask role again |
| "只做一张，你帮我选" | RECOMMEND one role, ASK confirmation and wait |
| "设计商品主视觉" with no quantity | DUAL_DEFAULT A+B, no role-choice question |
| Explicit one + role answer but missing platform | Role PASS, mandatory-input gate still BLOCKED; ask platform |
| Explicit one + both role and all required facts known | Exactly one image, selected role, no redundant question |

To establish production behavior PASS, inspect actual Codex conversations and image-provider call order; static documentation checks alone are insufficient.
