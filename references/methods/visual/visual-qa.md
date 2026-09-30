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

### V9 Strategy–Visual Alignment
Confirm the dominant visual resource and first focal point support the approved communication job and hero selling point.

### V10 Campaign Contact-sheet Review
For multi-image/multi-slot work, compare side-by-side for:
- unnecessary repetition,
- continuity,
- campaign locks,
- meaningful variation,
- duplicate jobs,
- drift.

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
