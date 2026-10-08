# Independent Visual Critic

Purpose: judge the visible artifact independently from the producer's explanation.

The Critic evaluates **result, not intention**.

**INTENTION ≠ RESULT**

A producer saying "the shadow was checked", "the circles represent airflow", or "the reference was used" does not make those things visually successful.

## Independence rule

For the first criticism pass, use only:
- the rendered artifact,
- the concise communication goal / Brief,
- necessary product/source reference for identity comparison,
- intended viewing condition.

Do not read the producer's rationale, prompt, production note, self-QA report, or claimed design decisions before the first-pass visual judgment. This reduces confirmation bias.

After first-pass judgment, benchmark/reference trace may be inspected only to evaluate transfer and repair.

## Verdicts
Use only:
- **PASS** — visually suitable to become a client-preview candidate, subject to hard/integrity QA.
- **REVISE** — direction is viable; specific craft/production changes can repair it without rethinking the core visual proposition.
- **REJECT** — first-impression, direction, composition, or product-scene relationship is fundamentally weak/generic; return upstream.

Do not use an averaged aesthetic score.

## Mandatory Visual Core gates

Judge every applicable item explicitly:

### A. PRODUCT PRESENCE
Is the product sufficiently prominent, identifiable, and visually weighted for the communication job?

### B. COMMERCIAL READABILITY
Does the artifact behave like a real e-commerce sales visual with clear benefit/message hierarchy rather than environment concept art?

### C. REFERENCE ADOPTION
Do the rendered composition, scale, camera, light, material, typography, depth, and/or action visibly correspond to the approved Reference Adoption Mapping?

### D. PRODUCT–ENVIRONMENT INTEGRATION
Do perspective, contact, shadow, light, environmental influence, occlusion, scale, color temperature, depth of field, edge behavior, and material response form one believable world?

### E. CATEGORY FIT
Does the result express this category/subcategory's use, purchase, sensory, and trust logic rather than a generic AI style?

### F. VISUAL DISTINCTIVENESS
Are major stylistic decisions product/brand/reference-specific and justified, rather than repeated gradient/floating/glow/pedestal/futuristic defaults?

### G. USAGE AUTHENTICITY
For Usage Hero or use-dependent work, is the product actively used through credible contact/action rather than merely held, posed beside, or placed in a lifestyle scene?

### H. COPY READINESS
Are text-safe, headline, logo, supporting/CTA, negative-space, and product-silhouette zones intentionally resolved?

### I. THUMBNAIL IMPACT
At intended small/mobile size, do product + core benefit remain the immediate read?

### J. PRODUCT TRUTH
Are geometry, material, color, identity, state, quantity, and visible claims preserved?

### K. TYPOGRAPHY PROMINENCE
Does the primary headline function as a commercial visual element, form a deliberate relationship with the product, retain presence at 25% scale, and make the offer legible at the priority required by the brief?

### L. TYPOGRAPHY CONTRAST
Do headline, price/offer, and core selling points visibly separate from their actual local backgrounds through color, size, weight, local whitespace, background simplification, and a planned contrast field rather than post-hoc rescue panels?

Use `PASS / FAIL / NOT_APPLICABLE`. An applicable NOT_CHECKED is not PASS.

## Blocking visual failures

Use **REVISE** or **REJECT** regardless of general attractiveness when any applicable condition is visibly true:
- pasted-on product or unrelated lighting system,
- missing/fake contact, floating without reason, incorrect hand/body/pet interaction,
- incompatible perspective, scale, shadow, reflection, occlusion, color temperature, depth of field, edge, or material response,
- product/background hierarchy reversed or product too small at thumbnail size,
- lifestyle scene without active usage when usage is the job,
- model/architecture/props overpower the product-use relationship,
- Reference Adoption Mapping has no visible counterpart,
- category logic collapses into generic AI luxury, cyberpunk, glow, particles, fog, decorative gradient, or futuristic UI,
- copy was forced into an unreserved area or competes with product/action,
- primary headline is visually weak, reads as body copy, or disappears at thumbnail scale,
- core offer is unreadable or materially weaker than ordinary supporting copy,
- typography depends on zooming, opaque rescue cards, or leftover-space placement,
- product truth drift.

Aesthetic appeal cannot average away these failures.

## Hero Output Check

First classify the output contract:
- explicit hero/main-visual request with no explicit single-image instruction → require two outputs;
- explicit single hero → require only the requested one;
- explicit finished/final poster → do not require the hero pair unless separately requested.

For `hero_output_mode: DUAL_DEFAULT`, verify:
- Hero A / Product Hero is present and makes product form, material, structure, core benefit, and commercial display the dominant job;
- Hero B / Usage Hero is present and shows active, category-valid use by a person, hand, pet, or relevant object;
- Hero B includes credible contact, occlusion, fit/pressure/grip/support/force behavior as applicable;
- both heroes share the Campaign Visual System in color, brand character, typography logic, and reference logic;
- composition, camera, scene function, and evidence route are meaningfully different;
- the pair is not one image with a replaced background.

Missing Hero B, passive lifestyle adjacency, or a background-only variation is a blocking `FAIL`. Judge both outputs independently; one PASS cannot compensate for the other.

## 2-Second Read Test (C0)

At intended thumbnail/mobile viewing size, answer from the visible result:
- What is noticed first?
- Is that the intended focal subject?
- Can the viewer tell what kind of product / offer this is?
- Is the communication direction roughly understandable?
- Does the artifact feel designed, or assembled from separate assets?

If the first impression is fundamentally wrong, use **REJECT** without rationalizing it through process notes.

## C1 — Composition
Inspect:
- focal hierarchy,
- balance/tension,
- negative space,
- crop/framing,
- depth/overlap,
- relationship among product, type, scene, and effect,
- whether the layout is a generic left-text/right-product or other default template without justification.

## C2 — Product / scene realism
Inspect:
- relative scale,
- dimensional plausibility when fit / containment / compatibility is part of the claim,
- perspective/camera compatibility,
- whether the receiver/container is actually under/around/against the product where the claim requires it,
- credible containment / insertion depth,
- contact/weight,
- shadow direction/softness,
- environment light/color influence,
- edge quality,
- occlusion/depth,
- material response,
- product identity fidelity.

The product must look like it belongs to the same visual world as the scene.

Run the Product–Scene Integration QA fields explicitly: perspective, contact, shadow, light, environmental reflection/influence, occlusion, scale, color temperature, depth of field, edge integration, and material response. Any obvious applicable failure blocks PASS.

### Product–Background Fusion Score

For every scene-based e-commerce poster, assign 1–10 to:

1. Perspective
2. Lighting
3. Shadow
4. Reflection
5. Scale
6. Occlusion
7. Material response
8. Color temperature
9. Contact realism
10. Overall scene coherence

Scoring is a hard gate, not an averaged aesthetic preference:
- any field below **7** → `FAIL` and `REVISE`/`REJECT`;
- total below **80/100** → `FAIL` and regenerate or structurally repair;
- delivery requires every field ≥7 and total ≥80, plus all other applicable gates.

Judge the visible artifact, not prompt wording or producer claims. Record all ten values and the total.

If the claim requires containment or insertion, a nearby container elsewhere in the frame does not count. The visible geometry must show the product actually entering / resting in / being held by the intended receiver.

## C3 — Typography
Inspect:
- identity legibility,
- headline impact,
- reading order,
- line breaks,
- rhythm/spacing,
- contrast,
- type/product relationship,
- whether typography is an active composition element,
- price / offer / date / CTA spacing and grouping,
- whether labels collide with large numerals or other commercial text,
- whether type color remains legible against the actual local background,
- whether repeated roles across a set use coherent scale and spacing.

Reject metadata-like strategy keywords, tiny accidental product identifiers, low-contrast commercial text, accidental overlaps, or text blocks that merely occupy empty space.

### Typography Contrast Check

Check PRIMARY HEADLINE, PRICE/OFFER, BRAND, SELLING POINT, CTA, and DATE separately for foreground/background luminance separation, local complexity, weight, visual size, spacing, overlap, edge collision, product collision, scene interference, and reading priority.

Confirm that the planned contrast field is visible in the scene: low-complexity local detail, controlled negative space, purposeful tonal separation, restrained highlights/shadows, and no collision with faces, active hands, product contact, or critical product structure. A post-hoc card is not evidence that the field was planned.

Direct fail when any applicable condition is visible:
- headline color and local background are too close,
- headline exists but is not obvious at first glance,
- headline requires enlargement/zoom to read clearly,
- headline weight is too light,
- headline size differs too little from supporting information,
- white text sits on a high-key highlight and appears washed out,
- dark text sinks into a dark or middle-tone field,
- complex background detail swallows the headline,
- type covers a face, hand contact, or product-critical structure,
- headline functions like body copy or a corner label,
- promotional price/offer is no more prominent than date, CTA, or ordinary supporting copy,
- product is prominent but copy fails to become the second visual center,
- copy is technically present but lacks commercial visual presence,
- primary hierarchy disappears at 25% view,
- core communication requires zooming.

Do not accept low contrast as “quiet,” “minimal,” or “premium.” Repair color/background relation, size, weight, local scene complexity, or the contrast field. Use restrained shadow, soft backing, or localized gradient only after structural contrast is correct; reject cheap text boxes, PPT-style slabs, sticker treatments, or large image-obscuring panels.

### Thumbnail Readability Check

Inspect the rendered artifact at 100%, 50%, and 25%. At 25%, the viewer must still perceive product category, primary message/core benefit, and—when promotion-led—the importance of the price/offer. Supporting details need not remain fully readable, but the primary headline may not disappear, become a thin gray trace, or lose its second-center relationship with the product.

### 2-Second Read Test

Record the first, second, and third read. Target: `PRODUCT → PRIMARY MESSAGE → OFFER / BENEFIT`, allowing product and headline to operate as a balanced dual core. Fail when the sequence is background-first, product-only with no message, or headline-only with delayed product recognition.

### Typography Prominence Score

Score each field 1–10 from the visible artifact:

1. Headline visibility
2. Headline scale
3. Headline contrast
4. Reading hierarchy
5. Product–type relationship
6. Offer visibility
7. Mobile / thumbnail readability
8. Overall commercial typography

Hard gate:
- any field below **7/10** → `FAIL`;
- total below **64/80** → `FAIL`;
- primary headline visually disappears, core offer is unreadable, headline functions like body copy, type overlaps important product evidence, hierarchy cannot be identified, contrast depends on zooming, or copy is technically present but commercially invisible → direct `FAIL`.

Record all eight values, total, and status. Product–Background Fusion, Product Truth, Commercial Hierarchy, Reference Adoption, and Final Artifact QA remain independent gates and cannot average away a typography failure.

## C4 — Semantic effect
If effects exist:
- what do they communicate from the image alone?
- do they reinforce the product/benefit/context?
- do they guide attention?
- are they visually integrated?
- do they imply unsupported facts?

If an effect is only decoration, revise or remove it.

## C5 — Specificity / repetition
Ask:
- if the product were swapped for a competitor, would the design remain almost unchanged?
- if the logo were swapped, would the design remain almost unchanged?
- across a coordinated set, is the product repeatedly shown as the same front-view / upright / full-outline cutout without a deliberate communication reason?
- do page-to-page differences come mainly from background swaps rather than meaningful product participation?

If yes, product/brand specificity or product participation is insufficient.

Also compare against Category Visual Intelligence and Style Justification. If the same gradient, floating product, glow ring, pedestal, fog, neon, centered object, split layout, giant headline, or futuristic studio could be used unchanged for an unrelated category, require evidence for the choice or revise it.

## C6 — Viewer Question / Visual Evidence
For each supporting or selling-point output, ask:
- what viewer question is this slot supposed to answer?
- what visible evidence in the artifact answers it?
- if the headline/caption were hidden, would the image still provide material evidence for the claim, use context, fit, scale, or action?
- is the evidence route appropriate to the communication job?

Text may clarify evidence, but it must not be the only reason the selling point is understandable when the slot depends on demonstration, use, context, fit, scale, or interaction.

Examples:
- “one-hand operation” shown only by an arrow and label → insufficient,
- “portable” shown only by motion graphics and copy → insufficient when no use/scale evidence exists,
- “cup-holder fit” shown only as an abstract circle → insufficient if the slot claims in-context compatibility.

If required visible evidence is absent, use **REVISE** or **REJECT** and return to Visual Evidence Strategy / Production Plan rather than polishing typography around the gap.

## C7 — Strategy / platform alignment
Confirm the visible result supports the approved communication job and first impression without relying on explanatory text outside the artifact.

Also compare the artifact against the already-approved platform/content strategy. If production reintroduces elements that the strategy intentionally deferred, removed, or softened — for example moving price / CTA back onto a content-first cover after deciding to place commerce information later in the sequence — treat that as strategy drift and revise unless there is a documented reason.

## C8 — Benchmark transfer
Only after C0–C6, inspect the Reference Basis when benchmarking informed the direction.

Verify:
**Reference mechanism → visible artifact behavior**

A research summary with no visible transfer does not count.

For every important reference, inspect SOURCE / ADOPT / ADAPT / DO NOT COPY / IGNORE and its output trace. `REFERENCE_ADOPTION_QA = FAIL` when a promised ADOPT parameter is missing, contradicted, or visible only in the rationale. Check concrete mapped fields rather than overall resemblance; the goal is visual-language transfer, not copying.

## C9 — Element justification
Every non-required element should serve at least one:
- communication,
- semantic context,
- attention,
- product/brand identity,
- necessary production function.

Remove unjustified competition.

## Dual-Hero pair gate

When `hero_output_mode: DUAL_DEFAULT` or an explicit two-hero request applies, assess each hero independently and then the pair:
- Hero A achieves Product Desire with product-first commercial hierarchy,
- Hero B achieves Usage Desire / Experience through active category-valid use,
- campaign color/material/type/brand/reference logic is coherent,
- composition, camera, scene function, and evidence route are meaningfully different,
- the pair is not a background swap,
- both survive thumbnail review.

One PASS cannot compensate for the other hero's FAIL / REVISE / NOT_CHECKED.

## Verdict + return map

Every non-PASS verdict must state:
- visible failure,
- responsible module/stage,
- exact repair target,
- what should remain preserved.

Typical routing:
- weak/generic visual thesis → Visual Direction → REJECT
- template/passive composition → Composition & Typography → REJECT or REVISE
- receiver-position / camera / scale / containment mismatch → Direct Final Poster Composition / Integration Plan → REVISE or REJECT
- light/edge/local integration mismatch with valid geometry → Product–Scene Integration repair → REVISE
- typography hierarchy → Composition & Typography / Commercial Info Composite → REVISE
- decorative effect → Visual Direction / A4 → REVISE or REJECT
- product identity drift → Product Truth / A1 → REVISE
- missing/weak visible evidence for viewer question → Visual Evidence Strategy / Production Plan → REVISE or REJECT
- static product repetition across the set → Composition & Typography / Production Plan → REVISE
- platform strategy drift → Strategy / Production Plan → REVISE
- benchmark not transferred → Visual Direction → REJECT

## Client-preview gate
The producer may not present an anchor as completed/approval-ready unless:
1. Visual Critic verdict is PASS, and
2. all applicable hard/integrity QA gates are PASS.

For referenced or scene-based anchors, PASS also requires applicable Reference Adoption QA, Product–Scene Integration QA, Commercial Hierarchy QA, Usage Authenticity QA, Copy Readiness QA, and Thumbnail Impact QA. For Dual-Hero, both individual verdicts and the pair gate must PASS.

A concept status such as S0 does not waive basic visual quality.

### Client contradiction rule
If the client points out a concrete visible failure that contradicts a prior PASS — for example missing containment, obvious scale mismatch, pasted-on integration, text collision, or scene relationship failure — the prior PASS is invalidated for that scope.

Do not defend the previous verdict or continue downstream as if it still passed. Mark the affected artifact/QA state for revision and return to the responsible stage.

If the same client-visible failure remains after one bounded local repair, invoke the Recovery Viability Gate and reassess whether the defect is structural.
