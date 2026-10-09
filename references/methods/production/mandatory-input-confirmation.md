# Mandatory Missing-Input Confirmation & No Placeholders

## Authority / precedence
**This is a fail-closed production and delivery policy for any final/finished commercial output.** It takes precedence over generic "ask only if convenient", autonomous execution, scoped blocking, deferral, prompt completion, concept fallback, and legacy placeholder advice.

A missing required input means **STOP final image generation, ask, wait for a user answer or authoritative verification, update the confirmed output contract, then resume**. "Few questions" never means "zero questions when required information is missing". Do not repeatedly ask for existing verified answers. Do not silently reinterpret a finished-poster request as a draft to bypass the stop.

## Independent Single-Image Hero Role Decision
In addition to this factual-input audit, if the user explicitly requests ONE finished image, apply `../single-image-hero-role-confirmation.md`. Role selection (Hero A vs Hero B) belongs to the client when not already evident in their brief. Even all verified platform/product/price/date facts do not authorize generating a one-poster result whose Hero role is unknown. Block until a clear explicit user choice or confirmation of a recommended role. `4:5` or `成品海报` do not settle that choice. This role gate and the missing-input gate must BOTH PASS before single-image generation.

## No Placeholders Policy
Never put unresolved stand-ins in a purported final artwork: no `¥___`, `XX元`, `待填写`, `____/____`, blank offer/date/price zones presented as finished copy, `TBD`, `Coming soon` used to mask unknown event dates, synthetic sample numbers, invented specifications/benefits, or incomplete logos/brand names.

Never quietly omit, replace, weaken or generalize any **user-requested** price, promotional period, model, claim, brand element or other required content. The phrase "预留价格/活动时间区域" is **not** consent to blank values: ask for the real content OR explicitly ask whether to remove that element from the final design; only a user's affirmative opt-out authorizes removal and layout recomposition.

Exact wording can be professionally written from **confirmed** product facts and an approved communication goal; its factual claims cannot be invented.

## Mandatory Missing-Input Confirmation Gate — BEFORE any finished image generation
Inspect the active brief, user-approved decisions, product/source images, current project files, and trustworthy official sources first. Record for EACH necessary final-output input its status, evidence and user authorization:

- **Platform / intended destination** and up-to-date applicable constraints. If missing, ASK which platform. "4:5" is a ratio, not a platform. A user can explicitly authorize a platform-neutral concept-only scope, but the agent must not choose it silently or label it platform-ready.
- **Product identity and truth:** brand, product name/model/SKU/variant where needed, authentic product assets, appearance, actual function, confirmed feature/benefit/claim and proof where required.
- **Required commercial text:** all requested display fields (price, prior price, discount, coupon, gift, CTA, campaign window, launch date, legal/certification claim, etc.). Verify an exact authoritative source for this **same campaign** when available; otherwise ask. An unrelated market price or plausible date is not authorization.
- **Other decision-changing facts:** licensing or missing product-state evidence, audience/market where it impacts the approved poster, requirements that affect legal correctness or platform readiness.

Input states:
- `VERIFIED`: user supplied or an authoritative applicable source verified, with evidence.
- `CONFIRMED_NOT_SHOWN`: user explicitly approved removing an otherwise requested field, with corresponding layout replan.
- `OPTIONAL_NOT_REQUESTED`: not required in the user's stated finished output; do not invent it or force a new question.
- `MISSING_REQUIRED`: required/requested, unresolved; **blocks finished generation**.
- `CONFLICTING`: mutually inconsistent required facts; ask user and **block**.
- `NEEDS_SOURCE_EVIDENCE`: exact product claims/geometry/permissions unsupported; obtain evidence/approval or redesign after explicit authorization.

**Pre-generation PASS** for the input audit requires known output count and scope, platform or an explicitly authorized non-platform concept boundary, and ZERO `MISSING_REQUIRED`/`CONFLICTING`/`NEEDS_SOURCE_EVIDENCE` fields that affect the finished output. Persist checks and approvals. A "reserved" blank price/date still counts as `MISSING_REQUIRED`.

## Question efficiency
Before asking, review existing project-confirmed data; never ask twice. Group only related necessary factual unknowns, preferably in one concise turn (normally 1–3 concrete questions, flexible if more independent blocking facts). Ask platform first when it determines downstream specs. Ask directly for the values, or offer explicit removal as a user decision when appropriate. Do not ask about routine designer-owned camera, backdrop, lighting or type decisions. **After answers, rerun the gate and proceed autonomously.** Do not treat an unanswered question as a default acceptance.

## Stage and status behavior
- `BLOCKED_AWAITING_USER`: formal generation is stopped. Existing verified strategy work may continue internally, without creating an approval-ready or nominally completed poster.
- `AUTHORIZED_CONCEPT_ONLY`: user explicitly requested a separate exploratory output, after understanding that it is not a final/platform-ready poster. Even concepts may not manufacture facts, copy stand-ins or counterfeit the finished deliverable.
- `READY_FOR_FINAL_GENERATION`: all required inputs confirmed or explicitly removed by user; all upstream gates PASS.
- `FINAL_DELIVERY_PASS`: final-generation gate PASS **and** finished artifact contains correct complete real-world wording (no placeholders), all required elements, valid technical/platform checks and all applicable product/visual QA.

No "completed final poster", `S2/S3`, final commercial export, client-ready approval or "platform ready" when the relevant gate is BLOCKED/NOT_CHECKED/FAIL. A beautiful image does not bypass this.

## Two mandatory checkpoints
1. **Before any final image generation**: check input audit/approval statuses and `missing_input_confirmation_gate`; if not PASS, ask and wait. If `SINGLE_EXPLICIT`, separately require `single_image_hero_role_confirmation: PASS` before any provider/image-render call. If both role and factual information are missing, ask efficiently and wait for BOTH.
2. **Before final delivery**: inspect actually rendered text/copy/fields, user-required elements, layout after removal approvals, QA and technical specifications. Detect visual placeholders, pseudo-values, invented price/time/claims, omitted requirements. Fail closed and repair/reconfirm rather than calling it done.

Readiness and delivery are **independent**: a preflight PASS does not automatically mean rendered exact text or commercial QA PASS.

## Regression acceptance matrix (rule level; no claim of actual model rendering)
| Scenario | Expected action |
|---|---|
| NOVA hero, brand/product/copy supplied, platform missing | ASK platform; do not generate a final poster yet |
| AERIS, required price not supplied | ASK exact price or explicit permission to remove pricing; no placeholder |
| AERIS, required campaign time absent | ASK exact dates/window or explicit permission to remove; no fake date |
| User says "预留价格、活动时间区域" but supplies no values | ASK both missing values or offer explicit removal, STOP; cannot render blank zones |
| User specifies one 4:5 poster, all facts verified and platform confirmed | GENERATE exactly one; no dual default, no repeated question |
| User explicitly says "不要价格和日期" for this artwork, with platform confirmed | Mark `CONFIRMED_NOT_SHOWN`; redesign clean layout; no ghost price/date fields |
| Verified campaign facts conflict with user supplied amount | ASK to resolve discrepancy before use |
| User explicitly approves platform-neutral concept-only | May produce an accurately labeled concept if other required concept facts are resolved; not a final ready poster |
| All required inputs verified + appropriate user decisions | Advance immediately without unrelated design-choice questions |

If the live Codex behavior differs from this matrix, report a failed scenario and update the actual controller/adapter, not just a rationale in prose.
