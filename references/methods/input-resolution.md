# Input Resolution

## Principle
Do not use a fixed intake questionnaire. Confirm outputs first, then back-propagate the information and assets required to produce them.

## Input requirement formula
**Product Truth Requirements + Output Specification Requirements + Platform Requirements + Proof/Compliance Requirements + Project Constraints**

## Input classes
- **REQUIRED:** cannot safely continue with the dependent branch without it.
- **CONDITIONAL_REQUIRED:** required only because a chosen output/mechanism/route depends on it.
- **RECOMMENDED:** improves quality but is not blocking.

## Gap classes
- **INFERABLE:** safely inferred from available evidence.
- **RECOMMENDABLE:** the agent should propose a professional default.
- **BLOCKING:** the dependent branch cannot safely proceed.
- **DEFERRABLE:** can be resolved later without harming current work.

Question priority = Decision Impact × Uncertainty.

## Evidence priority
Use the strongest available evidence:
1. user-verified fact or explicit client decision,
2. official specification / manual / brand source,
3. supplied project document,
4. unambiguous visible information in supplied assets,
5. category/domain knowledge only as a **HYPOTHESIS** until verified.

Do not upgrade lower-confidence evidence into verified truth.

## Project source scope
Before resolving inputs, establish which files belong to the active project.

### Same product does not imply same project
Reusing the same product, brand, SKU, or source image does **not** authorize reuse of a prior campaign/project state.

Treat `EXTEND / REVISE / ADAPT` as continuity operations only when the client explicitly indicates continuity or explicitly selects an existing project / approved artifact as the baseline.

A new platform, new campaign, new output-family test, or fresh brief using the same product should default to a **new project boundary** unless continuity is explicit.

Default source scope:
- the current brief and files supplied or explicitly selected for this project,
- the active project's own state and project-local inputs,
- Skill/reference files needed to execute the method,
- external references explicitly selected or authorized for this project.

For **CREATE**, do not search or inherit:
- sibling project folders,
- prior `PROJECT_STATE`,
- prior campaign visual systems,
- prior prompts / generation plans,
- prior generated scenes / outputs,
- prior platform/surface decisions,
- prior QA conclusions,

unless the client explicitly selects a specific item as a reference or baseline.

### Selective inheritance
A new project may selectively reuse **base truth sources** from an earlier project, such as:
- original user-supplied product photography,
- verified logo / brand asset,
- verified product dimensions/specifications,
- official manuals or source documents.

Selective inheritance must name the specific source item. Do not import the earlier project directory as a whole.

Generated campaign imagery, composed outputs, derived copy, visual direction, platform strategy, prompts, and project state are **not** base truth sources by default.

For **EXTEND / REVISE / ADAPT**, reuse only the explicitly selected existing project's state and artifacts. A nearby file is not evidence merely because it exists in the same parent directory.

If a file's project ownership is ambiguous, treat it as out of scope until its role is established. This prevents cross-project contamination from being mistaken for product truth.

## Truth states
- **CONFIRMED FACT** — directly verified.
- **DERIVED BENEFIT** — reasonable benefit derived from confirmed facts; keep the derivation traceable.
- **HYPOTHESIS** — plausible but not verified; never present it as product fact.

For truth-sensitive production, record:
- what must be preserved,
- what derivations are allowed,
- what inferences are prohibited.

## Scoped blocking
A missing or conflicting input blocks only the outputs, slots, claims, or production decisions that depend on it unless the unresolved item invalidates the whole direction.

Example:
- unresolved price → block exact promotional price layer,
- product image + verified geometry available → composition/background work may continue,
- unknown certification → block certification claim, not unrelated visual production.

## Upstream resolution first
When one upstream answer can resolve several downstream unknowns, resolve the upstream item first. Do not ask the client separately for downstream choices the agent can determine afterward.

### Minimum-sufficient upstream question
Ask only the nearest unresolved variable that materially changes downstream work.

### Minimum questions are not zero questions
The goal is to reduce client burden, not to remove consequential client decisions.

If a missing variable changes **what will be produced**, **where it will be used**, or **the scope the client is approving**, it cannot be silently replaced by a professional design default.

Examples:
- headline + price + CTA does not establish that the client wants a poster/KV;
- product images do not establish that the client wants a main image rather than a detail page or campaign set;
- an open platform does not automatically authorize a generic 4:5 deliverable when platform choice changes the useful output.

When the output is ambiguous, recommend the most suitable route and request approval. Ask downstream craft questions only when they remain genuinely decision-changing after that approval.

Example:
- if the client has already requested a **detail page** but the platform is unknown, ask for the **target platform**;
- after the platform is known, infer or recommend the platform's ordinary detail-page surface/default presentation when safe;
- do **not** immediately ask separate questions about mobile/desktop, aspect ratio, page container, or similar downstream details unless they remain materially ambiguous after the platform is resolved.

A missing platform may block platform-specific benchmarking, platform-fit claims, and final technical production, while generic strategy/page-structure work may continue.

## Missing vs conflict
- **MISSING:** no supported value exists.
- **CONFLICT:** two or more credible sources disagree.

Do not silently pick a value from a conflict. Record it in project state and resolve only when the dependent branch requires it.

## Product truth examples
May include:
- exact model/SKU/variant,
- geometry and proportions,
- color/material,
- labels/logo,
- included accessories,
- current condition for second-hand goods,
- verified features/claims,
- dimensions/power/capacity only when supplied or verified.

Unknown product truth must never be converted into a verified-looking fact.

## Unseen geometry rule
Not observed does not equal verified. Do not invent product backs, interiors, opened states, hidden mechanisms, accessories, ports, controls, or structural details that are not supported by evidence.

## Evidence Authorization Ladder

When a confirmed communication job materially benefits from an unseen / opened / internal / alternate-state product view, do not stop at a generic prohibition and do not silently fabricate the missing structure.

Resolve the truth boundary in this order:

1. **Check supplied / project evidence first.**
   Look for relevant photos, video, CAD, renders, manuals, diagrams, 360/multi-view assets, prior approved visuals, or other project-scoped evidence.
2. **Ask for missing factual support only when needed.**
   If no usable visual evidence exists, ask whether the client can provide:
   - a relevant image/video/render,
   - or a concise written description / dimensions / structural explanation that constrains the requested state.
3. **Use user-confirmed descriptive evidence carefully.**
   A specific client-supplied structural description may become a confirmed fact for the described attributes, but generated pixels remain generated evidence and still require T2 review.
4. **If factual evidence remains unavailable, ask whether a clearly labeled conceptual visualization is acceptable.**
   Client authorization may permit a speculative concept illustration for communication/exploration, but it does **not** convert invented geometry into verified Product Truth. Mark the dependent output as concept/provisional and avoid wording that implies the internal structure is factual.
5. **If conceptual invention is not allowed, change the evidence route.**
   Use another truthful route such as external hand/contact action, use context, result/proof, verified exterior detail, scale relation, or adjusted copy.

### Authorization states
Use when helpful:
- `EVIDENCE_VERIFIED` — supported by project/official evidence.
- `EVIDENCE_USER_DESCRIBED` — specific client-provided factual description constrains the depiction.
- `CONCEPT_AUTHORIZED` — client explicitly permits speculative concept visualization; not Product Truth.
- `CONCEPT_PROHIBITED` — client does not permit speculative depiction; select another evidence route.
- `EVIDENCE_UNRESOLVED` — required truth-sensitive depiction is still blocked.

Ask at the nearest consequential point. Do not make this a routine intake question for outputs that do not need unseen structure.

## Asset roles
- PRODUCT_REFERENCE
- BRAND_ASSET
- INSPIRATION_REFERENCE
- EXECUTION_REFERENCE
- SCENE_REFERENCE
- COMPOSITION_REFERENCE
- MOTION_REFERENCE
- NEGATIVE_REFERENCE
- PROOF_REFERENCE
- COPY_SOURCE
- COMPETITOR_REFERENCE
- PLATFORM_REFERENCE

Each reference should carry, when relevant:
- what to take,
- what to preserve,
- what not to copy,
- coverage limits.
