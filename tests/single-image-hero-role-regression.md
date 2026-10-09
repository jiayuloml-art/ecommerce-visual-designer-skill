# Single-Image Hero Role — Regression Acceptance Cases

Use `SKILL.md`, `references/methods/single-image-hero-role-confirmation.md`, `references/methods/output-system.md`, and `references/methods/production/mandatory-input-confirmation.md`. Run fresh projects or explicitly sourced existing project facts.

**These are expected behaviors; this file is NOT evidence of an executed live Codex or image-generation test.**

| ID | User message (other required platform/product facts are already confirmed unless noted) | Expected gate / interaction | Forbidden |
|---|---|---|---|
| H01 | “只要一张” | `SINGLE_EXPLICIT`, role unknown, `BLOCKED_AWAITING_USER`; ask “Hero A（产品展示型）还是 Hero B（真实使用场景型）？”; wait | Immediately generate Hero A/B |
| H02 | “只做一张 4:5 成品海报” | Same role-choice question, wait | Derive Hero A from 4:5, poster or generic defaults |
| H03 | “只做一张产品展示版” | Lock `PRODUCT_HERO`, `USER_EXPLICIT`, role PASS; generate exactly one after other gates PASS | Redundant A/B question |
| H04 | “只做一张真实使用场景版” | Lock `USAGE_HERO`, `USER_EXPLICIT`, role PASS; generate exactly one, with active category-valid use | Default Product Hero / passive lifestyle scene |
| H05 | “只做一张，你帮我选” | Recommend one role with concrete reason, enter `RECOMMENDED_AWAITING_CONFIRMATION`, explicitly ask approval and wait | Recommendation treated as approval |
| H06 | “设计商品主视觉” (no image count) | Existing `DUAL_DEFAULT` complete Product Hero + active Usage Hero; do not ask A/B selection | Single-image default or role question |
| H07 | “只做一张新品促销海报，4:5，用于京东” | Ask A/B selection; knowing platform is not knowing role | Product Hero inferred from platform |
| H08 | “一张 Hero B” with all required facts | Generate exactly one actual Usage Hero; don't ask role again | Duplicate role prompt or dual-output override |
| H09 | “只做一张 4:5 海报” with role unknown AND price/date/platform unknown | Ask role + necessary commercial/platform questions efficiently; no provider/image call until BOTH independent gates PASS | Proceeding after only platform or only role confirmation |
| H10 | “只做一张” → agent recommends A → user replies “可以，做A” | Persist USER_CONFIRMED_AFTER_QUESTION and selected PRODUCT_HERO, gate PASS; continue without re-asking role | Repeating A/B question or still blocking on already confirmed role |
| H11 | “只做一张，给我展示产品造型和材质” | Clearly PRODUCT_HERO even without the literal term; gate PASS, no redundant question | Treating all one-image briefs as ambiguous despite clear semantics |
| H12 | “一张广告，用人物展示真实佩戴使用” | Clearly USAGE_HERO; real contact/action required, gate PASS | Treating mention of a person as generic decoration or defaulting A |
| H13 | User previously chose A for a DIFFERENT campaign, new project says “只要一张” | Ask again; cross-project prior role is not active project approval | Importing an unrelated old selection |
| H14 | User changes confirmed A to B before render | Record updated client selection, invalidate role-dependent plan, rebuild B; still one output | Keeping Product Hero structure or quietly rendering A |

## Test evidence template
For every live Codex run record: `scenario_id`, `count_detected`, `role_detected_from_user`, `role_gate_status_before_render`, `question_or_recommendation`, `actual_user_confirmation`, `provider_called_before_approval`, `required_input_gate_status`, `output_count`, `actual_hero_role`, `final_gate_result`.

Fail if an image provider was called before role confirmation (where required), if the role was auto-chosen, if an unnecessary question was asked for an explicit role, if the output count diverged, or if a default dual contract becomes single.

Static policy consistency checks can be reported independently, but **never** represent static inspection as having executed this table against Codex.
