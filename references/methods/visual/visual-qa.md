# Visual QA and Revision

Use explicit QA states:
- **PASS**
- **FAIL**
- **NOT_CHECKED**
- **NOT_APPLICABLE**

An applicable NOT_CHECKED item is not PASS.

## Hard gates
Hard-gate failures cannot be averaged away by aesthetic scores.

### Q0 Fact / Product Truth QA
Check product/SKU/condition, prices, claims, numbers, logo/brand facts, accessories, variant, labels, geometry, and prohibited inferences.

For rendered product visuals, perform the T2 source comparison: compare the actual artifact against the supplied/verified source product and the slot truth constraints, not only against the prompt.

### Q1 Technical QA
Canvas, aspect ratio, resolution, duration, file size, format, font load, missing assets, overflow, safe zone, collisions, export integrity.

### Q2 Regression QA
When an approved baseline exists, check for unexpected changes:
- product geometry/color,
- campaign locks,
- layout areas not intended to change,
- disappearing approved elements,
- copy drift.

Do not rely on pure pixel diff for generative imagery; compare structural/semantic invariants as well.

### Q3 Platform / Compliance QA
Check platform-valid action path, output/surface fit, current technical spec, claims/compliance, and viewing-condition performance.

## Visual Excellence QA
Run after applicable hard gates pass.

Within the soft optimization layer, prioritize:
1. **Visual Excellence**
2. Communication Effectiveness
3. Platform Fit
4. Production Efficiency

This order never overrides Product Truth, Compliance, or critical Technical Accuracy.

### V1 Full-size Craft
Check product fidelity, material/light coherence, edges, reflections, typography, contact/grounding, and visible artifacts.

### V2 Thumbnail / First Impression
At reduced viewing size:
- is the primary product/message still clear?
- is the product or intended focal subject dominant?
- does hierarchy survive detail loss?

### V3 Product Specificity
Ask: if the product were swapped for another item in the same category, would the design work almost unchanged?
If yes, strengthen product-specific form, use, evidence, context, or visual proposition.

### V4 Brand Specificity
Ask: if the logo/brand name were swapped, would the visual remain essentially identical?
If yes, strengthen evidenced brand structure, voice, distinctive device, or campaign logic rather than adding arbitrary decoration.

### V5 Grounding / Contact
Check contact surface, shadow, light direction, occlusion, scale, and product integration.

### V6 Element Justification
Every non-required element should serve at least one:
- communication,
- semantic context,
- attention guidance,
- brand/campaign identity.

Remove unjustified competition.

### V7 Composition Rhythm
Check balance, tension, spacing, repetition/variation, crop, scale, and negative space.

### V8 Information Hierarchy
Check first, second, and supporting reads. Exact copy should remain legible at the intended viewing condition.

### V8a Hero Typography
For hero/KV work, explicitly verify:
- headline legibility at reduced viewing size,
- clear headline/supporting-copy hierarchy,
- purposeful line breaks and spacing,
- sufficient contrast over the image,
- product/copy spatial relationship,
- absence of unnecessary translucent cards/pills or template-like text containers,
- restraint: supporting facts do not overwhelm the first impression.

If the title, model name, or proof text becomes hard to read at the intended thumbnail/mobile scale, this check is **FAIL** even when the exact strings are technically correct.

### V9 Strategy–Visual Alignment
Confirm the dominant visual resource and first focal point support the approved communication job and hero selling point.

### V9a Benchmark-to-Artifact Transfer
When visual benchmarking informed the direction, verify that the final artifact actually expresses the selected reusable mechanisms (for example composition, hierarchy, light/material treatment, typography role, scene semantics, or brand device). A research summary that leaves no visible trace in the artifact does not satisfy this check.

### V10 Campaign Contact-sheet Review
For multi-image/multi-slot work, compare side-by-side for:
- unnecessary repetition,
- continuity,
- campaign locks,
- meaningful variation,
- duplicate jobs,
- drift.

### V11 Anchor Acceptance Gate
For representative hero/KV anchors, the authoritative gate order and reject/revision behavior are defined in `anchor-production-protocol.md`. This section supplies QA criteria; it does not permit skipping an earlier protocol stage.

Before presenting a representative anchor as a direction for client approval, all applicable hero/KV checks must pass or be explicitly marked unresolved:
- product truth,
- grounding/contact,
- first-impression hierarchy,
- hero typography,
- product/brand specificity,
- strategy–visual alignment,
- benchmark-to-artifact transfer when benchmarking was used.

A technically correct artifact with obvious template composition, weak typography, poor grounding, or unreadable text must remain an internal/recovery draft rather than an approval-ready anchor.

## Production Efficiency Review
Keep this separate from Visual Excellence and hard gates. When materially relevant, record:
- total elapsed time to a usable artifact,
- stalls/timeouts,
- retries and route changes,
- avoidable tool calls or rework caused by unresolved upstream decisions,
- whether the final artifact quality justified the production cost/time.

A visually strong result may still have an efficiency problem; an efficient result may still fail Visual Excellence.

## Failure evidence and repair
Every FAIL should identify:
- visible failure/evidence,
- responsible layer,
- executable repair action.

## Revision loop / QA Return Map
**Detect → classify → responsible layer → nearest responsible node → minimum-variable fix → re-QA affected scope**

Typical return points:
- fact/claim error → Product Truth / input resolution,
- scene/priority error → Art Direction,
- product/layout error → Production Plan / composition,
- campaign inconsistency → Campaign Visual System,
- text error → deterministic text/layout,
- provider/capability error → routing,
- export/spec error → technical/export layer.

Once structure is correct, stop adding random elements. Improve only the highest-impact remaining craft issues.
