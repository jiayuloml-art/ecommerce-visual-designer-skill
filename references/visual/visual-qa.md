# Visual QA and Revision

## QA order
### Q0 Fact / Truth QA
Check product/SKU/condition, prices, claims, numbers, logo/brand facts, accessories, variant, labels.
Blocking truth failure = artifact FAIL regardless of aesthetic score.

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

### Q3 Semantic Visual / Communication QA
Rubric examples:
- Product fidelity: PASS/WARN/FAIL
- Visual hierarchy: 1–5
- Communication-job completion: 1–5
- Campaign consistency: 1–5
- Platform fit: 1–5
- Artificial artifacts / visual slop: list
- Critical failures: list
- Revision target: one highest-impact target

### Q4 Platform / Compliance QA
Check platform-valid action path, output/surface fit, current technical spec, claims/compliance, viewing-condition performance.

### Q5 Human approval
Use only when required by project importance, major creative decision, or final approval contract.

## Revision loop
Detect → classify → rank severity → fix highest-impact failure → re-QA.

### Structural revision
Use when product truth, core hierarchy, art direction, or communication job cannot be satisfied by local edits.

### Polish pass
Once structure is correct, stop adding random elements. Improve spacing, alignment, edge quality, material, lighting, typography, balance, and local artifacts.
