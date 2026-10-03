# Visual Production Plan

Use one structured plan per output instance or independently produced slot. This is the production compilation layer between design decisions and tool/provider requests.

## Shared vs local
Campaign-level strategy, product truth, and campaign visual system are shared.
Production decisions are output/slot-specific.

When `anchor: true`, the slot must follow `anchor-production-protocol.md`. The production plan records the current protocol stage but does not replace the protocol's mandatory transition gates.

```yaml
slot_identity:
  slot_id:
  output_id:
  anchor: false
  anchor_protocol_stage: null # AP0_READY | AP1_DESIGN_LOCK | AP2_SCENE_FIT | AP3_PRODUCT_INTEGRATION | AP4_TYPOGRAPHY | AP5_FINAL_QA | AP6_CLIENT_PREVIEW

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

preproduction_readiness:
  platform_surface_resolved: NOT_CHECKED
  truth_resolved: NOT_CHECKED
  benchmark_translated: NOT_CHECKED
  asset_plan_resolved: NOT_CHECKED
  art_direction_resolved: NOT_CHECKED
  production_route_resolved: NOT_CHECKED
  recovery_route_resolved: NOT_CHECKED

supporting_asset_plan:
  existing_assets: []
  assets_to_generate_or_source: []
  semantic_purpose: []
  truth_or_ip_limits: []

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

product_scene_integration:
  perspective_scale:
  contact:
  shadow:
  ambient_light_color:
  edge_quality:
  depth_occlusion:
  preserve_product_identity: true

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

## Pre-Production Readiness Gate
Before a slot becomes `READY`, resolve every production-critical field that materially affects the intended result. A slot may still proceed as `S0 CONCEPT` with explicit gaps, but it must not silently enter production-ready execution.

For hero/KV work, readiness normally includes:
- output/surface/platform state when it changes composition or export behavior,
- product-truth locks,
- benchmark-to-visual mechanism translation when benchmarking is required,
- art direction and first focal event,
- required product/brand assets,
- supporting scene/prop/usage assets needed by the concept,
- primary production route,
- recovery route for critical tool/provider failure.

Do not call an expensive generation/edit route merely because a general mood has been chosen.

## Product identity anchors
When product fidelity matters, explicitly lock what cannot change:
shape/silhouette, proportions, color, material, logo/label, controls/components, quantity/variant, scale cues, current condition.

## Fidelity-preserving integration
Preserving the source product does not mean leaving it visually isolated from the scene. When a verified product layer is composited into a new environment, integrate it non-destructively through perspective/scale alignment, contact shadow, ambient light/color matching, edge treatment, depth, and occlusion as appropriate.

Do not hide an integration failure inside a generic white card, rounded rectangle, or isolated cutout unless that separation is an intentional part of the approved art direction.

## Truth checkpoints
Use three truth checkpoints when product fidelity or commercial claims matter:

- **T0 — Pre-lock:** before compilation, lock supported facts, preserve rules, allowed derivations, prohibited inferences, and unresolved conflicts.
- **T1 — Compile guard:** before execution, verify that prompts/instructions/tool parameters do not introduce unsupported geometry, claims, quantities, variants, text, or other prohibited inferences.
- **T2 — Rendered-result check:** after execution, compare the actual rendered artifact against the source product/evidence and the compiled truth constraints.

T1 must fail closed: if a required truth-sensitive field is unresolved, mark the dependent slot `BLOCKED` rather than silently compiling a guess.

## Compilation rule
A production plan is not a provider API request. Compile it into provider/runtime-specific instructions only after the design plan is resolved.
