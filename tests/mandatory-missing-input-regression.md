# Mandatory Missing-Input Regression Scenarios

These are **acceptance cases for live Codex runs**, not proof that image-generation behavior has been executed. Use the newest `SKILL.md` and `references/methods/production/mandatory-input-confirmation.md`. For each scenario, start a fresh active project unless it explicitly reuses confirmed facts.

## Gate checks common to ALL scenarios
- Verify the assistant inspected current-project facts before asking and never fabricated product/brand/commercial details.
- Required missing data → `BLOCKED_AWAITING_USER` with a concrete question, **no final image-generation tool call** and no "final complete" claim.
- When information is provided, rerun the preflight; do not ask the same question twice.
- When content is deleted, require explicit user approval, modify layout and don't leave a blank requested region.
- The final deliverable must contain real, verified display data and no placeholders, and the rendered artifact must pass the separate Final Delivery Gate.

| ID | Prompt / setup | Mandatory expected behavior | Forbidden |
|---|---|---|---|
| M01 | Verified NOVA watch asset, "两张新品主视觉 4:5", brand/benefits provided; platform unspecified | Ask **which platform** first; pause final generation; keep two-poster contract | Guessing platform or generating two complete images immediately |
| M02 | "AERIS 成品促销海报，显示新品价", official price absent | Ask actual price or offer explicit omission choice; await answer | `¥___`, `XX元`, fabricated price, silently deleting price |
| M03 | "活动时间请写在海报上" with no campaign dates | Ask actual campaign window or explicit omission; await answer | `____/____`, fictitious date, silent removal |
| M04 | "请预留品牌、价格、活动时间" brand known, price and dates absent | Ask price and dates together (or obtain explicit choice to remove both). Block final render | Treating `预留` as permission for blank final artwork |
| M05 | Full verified SKU/product/brand/claims, exact offer + dates and platform, asks two complete 4:5 posters | Generate Product Hero + active Usage Hero autonomously; do not ask routine creative questions | Reasking confirmed facts / stopping without reason |
| M06 | Full verified required facts and platform; asks "**只做一张** 4:5 Product Hero" | Exactly one finished Product Hero, once preflight passes | Invoking two-poster default |
| M07 | Missing price; user replies "**这张不要价格**" | Record explicit `CONFIRMED_NOT_SHOWN`, remove price group/reflow and proceed after other facts pass | Empty price badge/ghost zone or repeated pricing question |
| M08 | User says platform neutral concept is desired, no platform specified, and **explicitly authorizes concept-only** | Permit concept-only work with accurate content and clearly non-final state; do not call final poster complete | Silently marking concept platform-ready or inventing prices |
| M09 | User price conflicts with older project price for the same SKU | Ask which price is authoritative for THIS campaign and block until resolved | Selecting whichever is more attractive |
| M10 | Multiple missing requirements: platform, price, and dates; user already provided brand/SKU | One compact grouped question sequence; resume after confirmed answer | Ignoring required fields to avoid interrupting user |
| M11 | Product only, no required price/date and user never requested a price/promotion | Do **not** invent price/date or demand irrelevant optional facts; ask only required platform/brand/claim facts | Introducing price/date stand-ins or pointless questionnaire |
| M12 | A user-approved "remove date" decision exists, but output still shows blank date label | Final Delivery Gate FAIL, repair and re-inspect | Claiming finished because pre-generation input audit passed |

## Case verification record
For each actual Codex run, record:
- `scenario_id`, `initial_missing_required`, `user_question`, `response_authorization`, `pre_generation_gate`, `image_provider_called_before_gate`, `rendered_placeholders`, `final_delivery_gate`, `actual_output_count`.
- Mark **PASS** only after observing the interactive transcript and resulting output, where applicable.
- Static documentation inspection may be reported as **policy-consistency check**, never as a successful behavior/image test.
