# Visual Production Plan

Use one structured plan per output instance or independently produced slot. This is the production compilation layer between design decisions and tool/provider requests.

## Shared vs local
Campaign-level strategy, product truth, and campaign visual system are shared.
Production decisions are output/slot-specific.

```yaml
slot_identity:
  slot_id:
  output_id:
  anchor: false

output_identity:
  output:
  platform:
  surface:
  medium:
  primary_job:
  viewer_question:

output_role:
message:
  main:
  supporting:

truth_constraints:
  fact_ids: []
  preserve: []
  allowed_derivations: []
  prohibited_inferences: []

visual_lock:
  fixed_rules: []
  allowed_changes: []

reference_map:
  # asset/reference id, role, what to take, preserve, influence, coverage limits

composition:
  primary_focal_subject:
  product_scale_target:
  product_bbox:
  copy_safe_zone:
  visual_path: []
  supporting_elements: []
  forbidden_competition: []
  angle:
  spatial_relationship:
  sequence_or_timing:

scene_layers:
  atmosphere:
  semantic_context:
  attention_guidance:

content_layers:
  - product
  - scene
  - person
  - graphic
  - text
  - logo
  - cta
  - proof

copy:
  exact_strings: []
  fact_mappings: []
  rendering_owner: null # DETERMINISTIC_LAYOUT | MODEL_RENDERED_AND_VERIFIED | NO_TEXT

layer_ownership: {}

precision_requirements:
  product_fidelity:
  text_fidelity:
  layout_precision:
  brand_precision:
  creative_freedom:

campaign_locks: []
variable_zone: []

technical_spec: {}

tool_plan:
  production_route: null # GENERATE | EDIT | COMPOSITE | LAYOUT | VIDEO | HYBRID
  runtime_requirement: null
  provider_requirement: null
  parameters: {}

checks:
  truth_supported: NOT_CHECKED
  hierarchy_clear: NOT_CHECKED
  visual_lock_consistent: NOT_CHECKED
  technical_supported: NOT_CHECKED

unresolved_conflicts: []
status: NOT_COMPILED # NOT_COMPILED | BLOCKED | READY
```

## Three-layer scene stack
When a scene/background is used:
1. **Atmosphere** — color, material, light, mood.
2. **Semantic Context** — space, props, or context that explains relevance.
3. **Attention Guidance** — light, contrast, depth, framing, or motion that returns attention to the product/message.

Remove elements that do not serve communication, context, attention, brand, or necessary production function.

## Visual resource allocation
The plan must make clear:
- what is the first focal subject,
- where/how large the product is intended to appear,
- where copy can safely live,
- the intended visual path,
- which supporting elements are justified,
- what must not compete with the primary focal subject.

Do not hard-code universal product occupancy percentages.

## Product identity anchors
When product fidelity matters, explicitly lock what cannot change:
shape/silhouette, proportions, color, material, logo/label, controls/components, quantity/variant, scale cues, current condition.

## Truth checkpoints
Use three truth checkpoints when product fidelity or commercial claims matter:

- **T0 — Pre-lock:** before compilation, lock supported facts, preserve rules, allowed derivations, prohibited inferences, and unresolved conflicts.
- **T1 — Compile guard:** before execution, verify that prompts/instructions/tool parameters do not introduce unsupported geometry, claims, quantities, variants, text, or other prohibited inferences.
- **T2 — Rendered-result check:** after execution, compare the actual rendered artifact against the source product/evidence and the compiled truth constraints.

T1 must fail closed: if a required truth-sensitive field is unresolved, mark the dependent slot `BLOCKED` rather than silently compiling a guess.

## Compilation rule
A production plan is not a provider API request. Compile it into provider/runtime-specific instructions only after the design plan is resolved.
