# Artifact Integrity QA

Purpose: verify non-aesthetic hard gates independently from visual criticism.

This module checks truth, technical integrity, regression, and platform/compliance state. It does not decide whether a design is visually excellent.

Use states:
- **PASS**
- **FAIL**
- **NOT_CHECKED**
- **NOT_APPLICABLE**

Applicable NOT_CHECKED items are not PASS.

## Q-1 — Mandatory Pre-Generation Confirmation (blocking)
Before ANY final commercial poster generation, inspect `mandatory-input-confirmation.md`. All requested/required facts and the target platform must be verified/confirmed; a missing price or date *including a requested reserved zone* is blocking unless the user explicitly approves removal. NO placeholders, guessed promotion facts or unapproved deletion. If input audit is NOT_CHECKED/BLOCKED/FAIL, halt generation and ask the user. This check cannot be waived by excellent composition or autonomous execution.

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

For rendered product visuals, perform T2 comparison against supplied/verified product evidence.

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

If target platform is absent or an account-dependent rule cannot be resolved for final production, ask for the missing information BEFORE final image generation. Do not choose a generic platform or silently proceed with a finished export.

## Q4 — Fail-Closed Final Delivery Gate (blocking)
Inspect the rendered artifact itself and verify: (1) pre-generation audit PASS, (2) every required user field is present with **actual confirmed content** or explicitly removed with user approval, (3) zero price/date/brand/parameter stand-ins, blanks or invented facts, (4) real text accurately matches verified sources, (5) platform and technical rules satisfied and relevant visual/artifact QA PASS. A blank region labeled price/date does NOT satisfy content completeness. Failure / NOT_CHECKED blocks 'final', S2/S3, client approval-ready and platform-ready claims. Request data or re-render/reflow, then inspect again.

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
