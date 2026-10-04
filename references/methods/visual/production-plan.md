# Visual Production Plan

Use one structured plan per output instance or independently produced slot. This is the production compilation layer between design decisions and tool/provider requests.

## Shared vs local
Campaign-level strategy, product truth, and campaign visual system are shared.
Production decisions are output/slot-specific.

When `anchor: true`, the slot must follow `anchor-production.md`. The production plan records the current protocol stage but does not replace the protocol's mandatory transition gates.

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

visual_evidence:
  required_visible_evidence:
  evidence_route:
  scene_or_action:
  required_assets: []
  truth_boundary: []
  evidence_authorization_state:
  dimensional_basis:
  benchmark_question:
  fallback_evidence_route:

truth_constraints:
  fact_ids: []
  preserve: []
  allowed_derivations: []
  prohibited_inferences: []

product_representation:
  mode: null # SOURCE_PIXEL_LOCKED | IDENTITY_PRESERVING_RECONSTRUCTION | AUTHORIZED_CONCEPT_STATE
  source_identity_assets: []
  identity_anchors: []
  allowed_pose_view_state_changes: []
  authorization_required_for: []
  provisional_state_label: null

visual_lock:
  fixed_rules: []
  allowed_changes: []

reference_map:
  # reference id, visible observations, extracted mechanism, transfer target, do-not-copy boundary, coverage limits

preproduction_readiness:
  platform_surface_resolved: NOT_CHECKED
  truth_resolved: NOT_CHECKED
  benchmark_translated: NOT_CHECKED
  visual_evidence_resolved: NOT_CHECKED
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
  product_scene_relationship:
  interaction_action:
  reference_influences: []
  sequence_or_timing:

scene_layers:
  atmosphere:
  semantic_context:
  human_or_object_interaction:
  attention_guidance:

product_scene_integration:
  perspective_scale:
  dimensional_plausibility:
  interaction_contact:
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

For benchmarked hero/KV work, `reference_influences` should name the concrete decisions inherited from the Reference Transfer Map. Empty or generic entries such as “premium”, “clean”, or “more dynamic” do not satisfy benchmark translation.

For scene-based work, `product_scene_relationship` should state how the product participates in the scene. If the field can only be described as “product placed left/right/center”, revisit Visual Direction / Composition.

For selling-point / demonstration slots, resolve `visual_evidence.required_visible_evidence` before layout. If the intended message requires use, fit, scale, interaction, or detail proof, copy plus a decorative arrow/shape does not satisfy this field by itself.

If the strongest evidence route cannot be produced truthfully with available assets, invoke the Evidence Authorization Ladder. Prefer client-supplied visual evidence, then specific factual description, then explicit concept authorization; if concept depiction is prohibited, choose a truthful fallback evidence route or mark the dependent slot BLOCKED / request the minimum input. Do not decorate around missing evidence.

For fit / containment / compatibility / wearable / insertion visuals, record the dimensional basis:
- verified dimensions,
- credible visible scale cue,
- user-confirmed approximate relation,
- or contextual-only illustration.

Do not present contextual-only illustration as dimensional proof.

## Pre-Production Readiness Gate
Before a slot becomes `READY`, resolve every production-critical field that materially affects the intended result. A slot may still proceed as `S0 CONCEPT` with explicit gaps, but it must not silently enter production-ready execution.

For hero/KV work, readiness normally includes:
- output/surface/platform state when it changes composition or export behavior,
- product-truth locks,
- benchmark-to-visual mechanism translation when benchmarking is required,
- required visible evidence / evidence route for the slot,
- art direction and first focal event,
- required product/brand assets,
- supporting scene/prop/usage assets needed by the concept,
- primary production route,
- recovery route for critical tool/provider failure.

Do not call an expensive generation/edit route merely because a general mood has been chosen.

## Product identity anchors
When product fidelity matters, explicitly lock what cannot change:
shape/silhouette, proportions, color, material, logo/label, controls/components, quantity/variant, scale cues, current condition.

Do not confuse identity preservation with source-image preservation.

Choose a `product_representation.mode` deliberately:
- use `SOURCE_PIXEL_LOCKED` when exact source pixels are actually required,
- use `IDENTITY_PRESERVING_RECONSTRUCTION` when better integration, pose, view, crop, or verified use-state depiction materially improves the communication job,
- use `AUTHORIZED_CONCEPT_STATE` only after the Evidence Authorization Human Gate when exact alternate/open/hidden geometry is not fully evidenced.

A reconstruction must still pass T2 against the identity anchors. It may improve scene integration; it may not silently redesign the product.

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
