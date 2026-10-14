# Artifact Integrity QA

Purpose: verify non-aesthetic hard gates independently from visual criticism.

This module checks truth, technical integrity, regression, and platform/compliance state. It does not decide whether a design is visually excellent.

Use states:
- **PASS**
- **FAIL**
- **NOT_CHECKED**
- **NOT_APPLICABLE**

Applicable NOT_CHECKED items are not PASS.

## Q0 — Product Truth / Fact QA
Check:
- product/SKU/variant/condition,
- geometry and identity locks,
- logo/labels,
- quantities/accessories,
- prices/offers,
- claims/parameters,
- certifications/legal facts,
- prohibited inferences.

For rendered product visuals, perform T2 comparison against supplied/verified product evidence. **Compare identity anchors and depicted claims, not arbitrary source-pixel or camera similarity**; an approved, evidence-supported perspective, crop, pose or lighting change is not a failure. Fail only unsupported physical changes or unverified newly exposed geometry. Truth and benchmark-source verification must not replace the existing Visual Excellence/Impact/Integration checks.

## Q0b — Final commercial-content and delivery gate
For each finished commercial poster, before rendering require `outputs.final_artwork_input_audit.status: PASS` and verified target platform; requested/required copy fields must be exact and supported or explicitly approved not to appear with layout reflow. After rendering, inspect actual visible text, price, date, model, claim and CTA against canonical/source wording. Reject blank fields, placeholders (`¥___`, `____/____`, `待填`, etc.), unsupported claims and unauthorized omissions. Set the artifact `final_delivery_gate: PASS` only after rendered copy matches and all applicable hard gates pass. Concept-only work must be clearly labeled and must not claim final delivery.

## Q1 — Technical QA
Check as applicable:
- canvas/aspect ratio/resolution,
- format/file size,
- font/assets loaded,
- overflow/collision,
- safe zones,
- text/graphic edge clearance,
- legibility of secondary text at intended viewing size,
- hierarchy spacing and unintended crowding,
- export integrity,
- duration/frame/audio/subtitle constraints for temporal outputs.
- required package completeness: for unspecified-count hero OR finished-poster requests, BOTH complete Product Hero and active Usage Hero posters exist, are identified, and retain separate QA states; explicit count overrides,
- complete integrated commercial text remains readable and verified in reserved contrast fields without colliding with required product or usage evidence; minimal deterministic repair only if rendered exact copy fails.

For coordinated visual sets, also check:
- numbering does not overpower the selling point,
- spacing rhythm is coherent across the series,
- repeated alignment is intentional rather than mechanically identical,
- text does not collide with product, arrows, rings, or other graphics,
- recurring line / arrow / dot / radius / label / icon treatments follow one coherent graphic token system,
- commercial text groups (price / offer label / date / CTA) remain legible and internally spaced at intended viewing size.

For every static e-commerce poster, also check:
- the delivered artifact is a complete poster, not an empty background, isolated product visual, or mood draft,
- product, environment, headline/core-copy zone, selling-point zone, brand zone, campaign/price/date/CTA zone as applicable, and commercial hierarchy are all resolved,
- typography and product/scene are planned and preferably generated together; exact copy is verified and corrected locally only if necessary rather than using default staged text overlay,
- the Product–Background Fusion Score report contains ten numeric fields and a total,
- every fusion field is at least 7/10 and the total is at least 80/100.

## Q2 — Regression QA
When an approved baseline exists, check unintended changes to:
- product identity,
- campaign locks,
- unaffected layout/content,
- exact copy,
- approved assets.

For generative imagery compare structural/semantic invariants, not only pixels.

## Q3 — Platform / Compliance QA
Check:
- platform/surface/output fit,
- latest verified technical rule state,
- claims/compliance,
- commercial text requirements,
- intended viewing condition.

If account-dependent or current platform rules are unresolved, do not claim platform-ready status.

## Client-facing delivery verification
At actual first visual delivery, check the four client-facing sections (design rationale, delivered outputs, factual boundaries, delivery status) in the active case language, each tied to actual rendered artifacts. When references were used, inspect the verifiable source URLs and record their concrete transferable visual mechanisms and actual adoption; absent or unverified research must never be invented. For local revisions, check the four incremental revision-note fields and affected-scope version/regression state. Reject unverified 'completed' claims, text-only output masquerading as produced visuals, or English boilerplate in a Chinese-case response (and vice versa). This verification **does not reduce product–scene creation, viewpoint diversity or existing visual quality gates**.

## Specialized visual-set and detail-page integrity checks
**Q0 — Geographic representation:** Verify every newly added flag, map, national border, regional emblem or comparable symbol has confirmed current-case necessity, accurate meaning and authorization. Authentic source-packaging marks may remain if faithful, but do not authorize additional decoration.

**Q1 — Package completeness:** A VISUAL_CONTENT_SET must have actual inspectable images (normally at least two), distinct primary Communication Jobs, and per-image file/ref, factual scope and QA status. Confirm product-first co-designed scene/camera in each applicable image and useful variations in angle/composition or scene role, while preserving product identity and campaign locks. A DETAIL_PAGE must have an actual first screen and each required module or inspectable crop, with complete requested-point coverage, order, module count, export dimensions, crop boundaries and missing-items check. A plan or partial render never passes.

**Q2 — Local revision:** Compare affected portions with the approved baseline, confirm unrelated product truth, scene, typography, campaign locks and assets remain intact; report actual updated file, version, integrity and affected-scope QA.

**Applicability:** These specialized checks are mandatory only for their respective contracts. The existing two-Hero and commercial-poster hard gates remain unchanged for Hero/final-poster contracts; do not force them onto detail modules. Applicable NOT_CHECKED cannot become PASS.

## Blocking rule
Hard-gate failures cannot be averaged away by visual quality.

A visually strong artifact with an applicable hard-gate FAIL cannot become S2/S3 or be described as platform/final ready.

A scene-based poster with any Product–Background Fusion Score field below 7 or total below 80 cannot be delivered, regardless of attractiveness or copy accuracy.

## Relationship to Visual Critic
A client-preview anchor requires:
- Visual Critic PASS, and
- all applicable hard/integrity gates PASS.

For Dual-Hero, this requirement applies to both hero artifacts and the pair-level gate. Do not mark the package complete when only one hero passes.

Keep visual criticism in `references/methods/visual/visual-critic.md`; do not move aesthetic judgments into this file.
