# Output System

## Output discovery
The client should not have to specify every deliverable. Recommend a package from strategy, platform, communication jobs, campaign scale, evidence needs, and viewer questions.

## Output Contract Gate

Visual production requires a **Confirmed Output Set**.

The minimum contract for each output is:
- output type,
- platform/surface state,
- primary communication job,
- scope,
- viewer question,
- priority.

### Explicit client output
If the client already specified a sufficiently precise deliverable, use it as the contract starting point and resolve only material gaps.

### Ambiguous output
If the brief contains product facts, campaign copy, price, CTA, or assets but does **not** make the deliverable clear, do not silently convert the brief into a hero/KV/poster/main image/detail page.

Instead:
1. diagnose the likely communication need,
2. recommend one primary output package or route,
3. give a short reason,
4. ask the client to approve or adjust it.

This is a recommendation, not a questionnaire.

### Platform/surface
If platform/surface materially changes the output package, benchmark set, information density, composition, or technical production, resolve it before production.

If the platform is unknown, the agent may recommend a likely route, but a platform-neutral concept may only be produced after the client explicitly approves that concept-only scope.

### Fail-closed rule
**No Confirmed Output Set → no visual production.**

Preparing strategy, benchmark research, or a proposed output package is allowed before confirmation. Rendering/assembling the client-facing artifact is not.

Each proposed output should include:
- Output type
- Platform / surface
- Primary communication job
- Viewer question
- Priority: Core / Supporting / Optional
- Short reason

After approval, create a Confirmed Output Set.

## Output levels
- **Output Family:** medium family such as Static, Sequence, Long-form, Temporal/Video.
- **Output Instance:** a specific asset with a specific job.
- **Slot:** one independently planned visual unit within an output instance or coordinated image set.
- **Output Package:** a set of coordinated instances.

## Image/slot role planning
For each meaningful slot, map:

**Viewer Question → Primary Communication Job → Required Visible Evidence → Evidence Route → First Visual Focal Point → In-image Text / Source**

For selling-point or use-context slots, load `references/methods/visual/visual-evidence-strategy.md` before composition.

A slot may use supporting mechanisms, but it should not exist only to increase image count. Copy or decorative graphics do not count as sufficient visual evidence when the viewer question requires demonstration, context, fit, scale, or use.

## No Redundant Output Rule
Every additional output/slot must add at least one of:
- a distinct communication job,
- new evidence,
- a new viewer question,
- a new scenario/use context,
- new decision support.

If it does not, merge or remove it.

## Package / bundle semantic routing
Resolve mentions of 套餐, 组合, 内容组合 and 套餐方案 by context before output defaults. **In an e-commerce visual-design request, prefer `VISUAL_CONTENT_SET` as the working interpretation** (multiple differentiated image roles), unless explicit source facts identify a product sales bundle, SKU quantity, gift, discount or purchase entitlement. Classify as VISUAL_CONTENT_SET, SALES_BUNDLE_FACT, BOTH (separate contracts), or AMBIGUOUS (ask one decision-changing question only if this changes output scope). Words alone do not authorize a sales bundle or commercial offer. Resolve conflicts between a visual set and an explicit one-image request before production. Preserve product-first joint product–scene design and legitimate per-image viewpoint variation in either visual route.

## Visual Content Set contract
When a confirmed visual-content set is requested for direct production, produce at least two actual inspectable visuals with distinct primary Communication Jobs unless the user explicitly settles a conflicting count. For each, retain its viewer question, role, factual scope, actual file/ref and QA status in the delivery manifest. Planning alone, one image or duplicate roles never satisfies the contract.

## Direct detail-page contract
An explicit direct detail-page request requires one actual first-screen image and a complete inspectable group of ordered module visuals. The first screen communicates product identity and core value; include a price **only when confirmed and required/applicable**, never as a fabricated or compulsory field. Product and scene should be purposefully co-designed in each scene-based unit, with module-specific supported camera/interaction variation. Separate product/core-value introduction from module-by-module explanation or proof. Map every confirmed requested selling point to at least one module; record each module's role, source evidence, actual image/crop, dimensions, crop bounds and status, plus omitted items and checks. Show prices only when verified and applicable. A single undifferentiated stitched image or a text-only plan does not satisfy completion. Detail pages do not inherit the dual-Hero poster default.

## Hero vs final-poster routing

Classify explicit output language before applying package recommendations:

- `主视觉 / 商品主视觉 / hero visual / campaign hero / 核心视觉 / 成品海报 / 电商促销海报 / 商品促销海报 / final poster` without an explicitly specified quantity → **recommend and deliver 2 complete final posters**: Hero A / product-focused full poster + Hero B / active-usage full poster.
- Any explicit count overrides two: one means exactly one complete poster (requested hero role, otherwise product-focused); other explicit counts determine the actual number delivered. Do not treat aspect ratio `4:5` as quantity.
- Both output families use Direct Final Poster Generation with the same complete-poster standard and individual QA. Do not recommend a single platform-neutral 4:5 poster as the default.

The default two-hero package is not redundant: Product Hero answers product desire/form/material/core-benefit questions, while Usage Hero answers use/fit/interaction/experience questions. Hero B must show active, category-valid use rather than lifestyle adjacency.

## Default direct-final poster output

When the client requests a finished promotional/final poster without an explicit quantity, recommend TWO individually complete integrated posters: Product Hero and active Usage Hero. The user may explicitly override the quantity. Do not convert a user-specified format into an assumed single image.

Every poster contract must include:
- product subject and identity locks,
- background/environment and contact surface,
- core-copy/headline zone,
- selling-point information zone,
- brand zone,
- campaign/price/date/CTA zone when applicable,
- commercial hierarchy and intended thumbnail read,
- one camera, perspective, lighting, shadow, reflection, and material-response system,
- Product–Background Fusion Score gate.

Default hierarchy:

**PRODUCT → PRIMARY BENEFIT / HEADLINE → BRAND / SERIES → SELLING POINTS / OFFER → ENVIRONMENT / DECORATION**

Do not add an empty-background deliverable, pure mood frame, isolated product hero, or layout-only intermediate to the client package unless the client explicitly asks for that staged artifact. Prefer generating each full poster with product + scene + finished typography and offer copy in a single coordinated image-generation pass. If exact glyphs cannot be verified, locally repair only failed text instead of reverting to a default background-first multi-layer workflow.

When a multi-poster set is justified, each image must add a distinct communication job/evidence route while remaining a complete poster. Do not generate one hero first merely to establish a background style and then treat the remaining posters as downstream layout variants.

For the default or explicitly requested Dual-Hero full-poster package, each member must have final ad typography, product/scene integration, brand and applicable supplied commercial information, and pass independently; the pair must not become background swaps. Share color, brand character, typography logic, and reference logic, but require meaningful differences in composition, camera, scene function, and evidence route.

## Runtime Output Specification
Compose from:
**Common Output Core + Medium Grammar + Primary Job + Supporting Mechanisms + Platform Adapter + Product/Strategy Context + Campaign Visual System**.

### O1 Identity
Output type, medium, platform, surface, format, priority.

### O2 Communication Job
Primary job, optional secondary job, desired user action, proposed destination, platform-valid destination.

### O3 Content
Main message, supporting message, product facts, features, benefits, proof, scenario, price, promotion, CTA, disclaimer.

### O4 Information / Temporal Structure
Hierarchy, reading/reveal order, grouping, density, rhythm, timing.

### O5 Visual Expression
Product presentation, composition, photography/rendering, typography role, graphic language, color, lighting, material, motion.

### O6 Production Dependency
Facts, assets, references, proof, people/scenes, commerce information, dynamic fields, platform-specific data.

### O7 Constraints
Product truth, brand, platform, compliance, copyright/IP, AI modification, budget, timeline.

### O8 Campaign Relationship
Shared visual system, shared product truth, shared message logic, continuity, allowed variation.

### O9 QA Criteria
Communication, product, visual, brand, platform, campaign, compliance.

## Dynamic commerce components
Price, promotion, gift, coupon, time window, CTA, and other volatile commercial data should be separable when possible so they can be replaced without regenerating the entire visual.
