# Visual-first output-contract regression checks

This is a **static specification regression checklist**. Passing the checks below does not establish real image quality; live image generation and human inspection remain necessary. Compare results against the unchanged parent branch, using identical inputs/runtime when possible.

## Protected invariants
- Product and purposeful scene are jointly planned/created before appearance-only concerns; recognizable product / product-use relation leads visual hierarchy.
- Product Truth locks known geometry/identity/facts. It does not automatically lock source-image pixels, pose, lens, crop or camera angle. New visible structural details still need evidence.
- Preserve category-specific Visual Direction, dual complete Hero default, Product Hero Impact, Usage Authenticity, product–scene relation, ten-field physical Fusion, Typography Contrast/Prominence and independent Visual Critic.
- No forced background-only generation or flat front-view product cutout; camera, contact, ambient light and scene are one believable system.
- A reference's authenticity is about source/research claims and transferable technique; it is never an order to reproduce a picture or freeze the product.
- A failed truth gate blocks only dependent facts/modules; it cannot reduce unrelated visual quality or suppress rendering of unaffected work.

## Scenario matrix

| ID | Input/test stimulus | Required observable behavior | Regression failure |
|---|---|---|---|
| VF01 | One front-view product photo; request product-focused main visual | Plan product and scene together; consider supported 3/4 view, crop, distance and new light; only known identity anchors are locked | Camera always fixed to source because reference must be “true” |
| VF02 | Same product; request active use Hero | Generate a distinct complete poster with credible contact, perspective, scene and product-use relation | Flat source image superimposed; model/room dominates |
| VF03 | Unverified back/control area would appear in proposed new angle | Seek relevant evidence/choose a different visible angle; continue unaffected composition and concept | Invent hidden controls **or** globally ban all camera changes |
| VF04 | Chinese brief; generate two commercial posters | All client-facing final sections and artifact roles in Chinese; exact canonical brand text preserved | English delivery template despite Chinese case |
| VF05 | English brief; request same package | All final delivery sections and revision note headings in English; no involuntary Chinese template | Chinese boilerplate |
| VF06 | “为这个产品做一组视觉套餐/内容组合” with no sales facts | Interpret as VISUAL_CONTENT_SET, at least two actual images with different Communication Jobs, manifest file/ref, factual scope/status | Invent 2-pack/discount/gifts, deliver only a plan/single image |
| VF07 | “购买两件装套餐” with explicit SKU/bundle facts | Treat sale bundle as verified commercial facts and resolve desired visual outputs separately | Confuse sold goods with required number of visual images |
| VF08 | “直接生成详情页”，confirmed three selling points, no confirmed price | Produce one actual first-screen image + complete ordered module images/crops with selling point coverage; omit unsupported price without blanks | Invent price; one stitched image claimed as full module set |
| VF09 | Same detail page; price required by confirmed brief but conflicting | Block price-dependent final surface or request confirmation while allowing independent visual planning | Invent price, or stop all unrelated visual tasks |
| VF10 | Selected inspectable visual benchmark | Include direct URL where verifiable, actual composition/light/product/scene learning and visible adaptation in design explanation | Fake URL or reference study freezes source product view |
| VF11 | User requests only headline correction to approved v1 | Reuse unaffected scene/product/angle; change targeted text, perform affected-scope QA, report V2 revision fields | Re-generate entire product/scene unnecessarily |
| VF12 | New campaign explicitly requests dynamic camera change using same product | New visual direction/camera, keeping evidence-supported identity; not bound to prior project's source pixels or revision-only preservation | Prior approved image freezes new creative work |
| VF13 | Promotional image references sales region but no request for national symbols | Do not add flag, map or regional emblem | Decorative flag added based on market/origin inference |
| VF14 | First delivery with one missing required module | Manifest and four-section delivery statement mark partial/incomplete status; no “completed” claim | Planning notes or rendered first screen counted as all deliverables |
| VF15 | Product truth all PASS; rendered visuals lack hierarchy, contact or compelling framing | Existing independent visual quality/impact/typography gates fail and route focused redesign | Facts PASS incorrectly overrides poor commercial visual quality |
| VF16 | Two supported camera outputs for the same product | Distinct compositions/scene jobs while shared identity/campaign stays coherent | Two near-identical front-view/background swaps |

## Review and execution
1. Confirm the diff modifies only intended files and adds this checklist; inspect for accidental replacement of existing production/visual quality rules.
2. Run VF01–VF16 using fixed evidence/briefs in a fresh project for each CREATE case; separately use approved baselines for VF11.
3. Inspect **actual generated files**, not just plans or successful tool invocations. Collect source images, outputs, exact text, manifests and final explanations.
4. Record each case as PASS / FAIL / NOT_CHECKED / NOT_APPLICABLE, with failure location and nearest responsible return point.
5. Do not merge until a reviewer validates the visual non-regression cases (especially VF01–VF03, VF12, VF15–VF16), language cases (VF04–VF05) and output completeness cases (VF06–VF09, VF14).
