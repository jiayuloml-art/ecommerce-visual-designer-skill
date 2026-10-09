# Visual Production Plan

Use one structured plan per output instance or independently produced slot. This is the production compilation layer between design decisions and tool/provider requests.

## Shared vs local
Campaign-level strategy, product truth, and campaign visual system are shared.
Production decisions are output/slot-specific.

For BOTH finished-poster and hero/main-visual requests without an explicit count, use `generation_mode: DIRECT_FINAL_POSTER`, `hero_output_mode: DUAL_DEFAULT` and compile TWO independently complete final-poster plans: Hero A / Product Hero and Hero B / active Usage Hero. An explicit count overrides two. Use `anchor-production.md` only when staged approval is requested or documented as necessary.

```yaml
slot_identity:
  slot_id:
  output_id:
  anchor: false
  generation_mode: DIRECT_FINAL_POSTER # DIRECT_FINAL_POSTER | HERO_VISUAL | EXPLICIT_STAGED_ANCHOR | OTHER
  hero_role: null # PRODUCT_HERO | USAGE_HERO | null; each role is an independently complete final poster
  paired_anchor_id: null
  anchor_protocol_stage: null # AP0_READY | AP1_DESIGN_LOCK | AP2_SCENE_FIT | AP3_PRODUCT_INTEGRATION | AP4_TYPOGRAPHY | AP5_FINAL_QA | AP6_CLIENT_PREVIEW

hero_outputs:
  hero_output_mode: DUAL_DEFAULT # DUAL_DEFAULT | SINGLE_EXPLICIT | COUNT_EXPLICIT
  recommended_deliverables_count: 2 # explicit user count overrides
  hero_a:
    role: product_hero
    output_id: null
    communication_job: PRODUCT_DESIRE
    status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
  hero_b:
    role: usage_hero
    output_id: null
    communication_job: USAGE_DESIRE_EXPERIENCE
    active_usage_actor: null # person | hand | pet | relevant_object
    active_usage_action: null
    contact_occlusion_force_evidence: []
    status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
  shared_campaign_visual_system: []
  required_pair_differences:
    - composition
    - camera
    - scene_function
    - evidence_route
  pair_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL

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

category_intelligence:
  category:
  subcategory:
  purchase_motivation:
  usage_context:
  sensory_attributes: []
  brand_positioning:
  visual_grammar: []
  rejected_cliches: []
  style_justifications: []

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
  - reference_id:
    source:
    role:
    visible_observations: []
    adopt: []
    adapt: []
    do_not_copy: []
    ignore: []
    output_trace: {}
    verification_cues: []

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
  product_position:
  product_scale_target:
  product_bbox:
  camera_angle:
  horizon:
  contact_surface:
  light_direction:
  shadow_direction:
  environment_color:
  product_reflection:
  copy_safe_zone:
  headline_zone:
  price_zone:
  brand_zone:
  logo_zone:
  cta_support_zone:
  product_silhouette_zone:
  negative_space_behavior:
  visual_path: []
  supporting_elements: []
  forbidden_competition: []
  angle:
  spatial_relationship:
  product_scene_relationship:
  interaction_action:
  reference_influences: []
  sequence_or_timing:

typography_prominence_contract:
  primary_message:
  headline_role:
  headline_scale:
  headline_weight:
  headline_lines:
  headline_alignment:
  headline_contrast_strategy:
  headline_product_relationship:
  price_role:
  price_priority:
  price_scale:
  price_contrast_strategy:
  supporting_copy_scale:
  supporting_copy_density:
  brand_scale:
  brand_position:
  copy_density: null # LOW | MEDIUM | HIGH
  local_background_complexity:
  text_contrast_field:
  thumbnail_reading_order: []

typography_contrast_contract:
  headline_text_color:
  headline_size_strategy:
  headline_weight_strategy:
  headline_background_relation:
  price_contrast_strategy:
  selling_point_contrast_strategy:
  local_background_complexity:
  contrast_field_method:
  fallback_enhancement:
  execution_status:
    zones_locked: NOT_CHECKED
    background_assessed: NOT_CHECKED
    text_color_selected: NOT_CHECKED
    size_weight_locked: NOT_CHECKED
    contrast_field_built: NOT_CHECKED
    fallback_checked: NOT_CHECKED
    scale_tests_complete: NOT_CHECKED

scene_layers:
  atmosphere:
  semantic_context:
  human_or_object_interaction:
  attention_guidance:

product_background_relationship:
  scene_role:
  scene_specificity_thesis:
  functional_relevance:
  visual_correspondence:
  spatial_relationship:
  composition_guidance:
  brand_emotional_fit:
  background_swap_test:
  role_specific_difference:

product_scene_integration:
  camera_height:
  horizon:
  vanishing_direction:
  lens_perspective_feeling:
  perspective_scale:
  dimensional_plausibility:
  interaction_contact:
  contact:
  shadow:
  key_fill_rim_light:
  shadow_direction_softness:
  ambient_light_color:
  environmental_reflection:
  color_temperature:
  material_response:
  edge_quality:
  depth_occlusion:
  depth_of_field:
  preserve_product_identity: true

direct_final_poster:
  complete_product_subject: NOT_CHECKED
  environment_resolved: NOT_CHECKED
  core_copy_zone_resolved: NOT_CHECKED
  selling_point_zone_resolved: NOT_CHECKED
  brand_zone_resolved: NOT_CHECKED
  campaign_zone_resolved: NOT_CHECKED
  commercial_hierarchy_resolved: NOT_CHECKED
  one_scene_system: NOT_CHECKED
  one_lighting_system: NOT_CHECKED
  one_camera_system: NOT_CHECKED
  one_pass_product_scene_typography: NOT_CHECKED # PASS requires joint poster generation, or documented runtime limitation with minimal exact-text correction
  text_accuracy_verified: NOT_CHECKED
  provider_prompt_negatives: []

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
  rendering_owner: MODEL_RENDERED_AND_VERIFIED # MODEL_RENDERED_AND_VERIFIED default | MINIMAL_DETERMINISTIC_REPAIR on verified failure | NO_TEXT only if explicitly requested
  text_accuracy_checks: []
  localized_repairs: []

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
  reference_adoption: NOT_CHECKED
  product_scene_integration: NOT_CHECKED
  commercial_hierarchy: NOT_CHECKED
  usage_authenticity: NOT_CHECKED
  copy_readiness: NOT_CHECKED
  thumbnail_impact: NOT_CHECKED
  direct_final_poster_complete: NOT_CHECKED
  product_background_fusion: NOT_CHECKED
  product_hero_impact: NOT_CHECKED # only for product-focused final posters
  product_scene_relationship: NOT_CHECKED
  typography_prominence: NOT_CHECKED
  typography_contrast: NOT_CHECKED
  thumbnail_typography: NOT_CHECKED
  hero_output: NOT_CHECKED
  integrated_visual_generation: NOT_CHECKED
  text_accuracy_verified: NOT_CHECKED

product_background_fusion_score:
  perspective: null
  lighting: null
  shadow: null
  reflection: null
  scale: null
  occlusion: null
  material_response: null
  color_temperature: null
  contact_realism: null
  overall_scene_coherence: null
  total: null
  status: NOT_CHECKED

product_hero_impact:
  core_product_focal_advantage: null
  visual_impact_mechanism: null
  product_silhouette_read: null
  camera_angle_and_lens_logic: null
  product_frame_dominance_and_crop: null
  foreground_midground_background_depth: null
  material_and_highlight_plan: null
  scene_to_product_contrast_plan: null
  product_typography_counterweight: null
  hero_specific_background_relationship: null
  protected_identity_and_legibility_zones: []
  overstyling_risks_to_avoid: []
  selected_direction_rationale: null

product_hero_impact_score:
  product_focal_dominance: null
  camera_silhouette_expressiveness: null
  material_lighting_quality: null
  compositional_energy: null
  commercial_impact_brand_fit: null
  total: null
  status: NOT_CHECKED # each ≥7 and total ≥40/50

product_scene_relationship_score:
  scene_relevance: null
  visual_correspondence: null
  spatial_integration: null
  commercial_hierarchy: null
  brand_consistency: null
  total: null
  status: NOT_CHECKED # each >=7 and total >=40/50

typography_prominence_score:
  headline_visibility: null
  headline_scale: null
  headline_contrast: null
  reading_hierarchy: null
  product_type_relationship: null
  offer_visibility: null
  mobile_thumbnail_readability: null
  overall_commercial_typography: null
  total: null
  status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL

unresolved_conflicts: []
status: NOT_COMPILED # NOT_COMPILED | BLOCKED | READY
```

## Three-layer scene stack
When a scene/background is used:
1. **Atmosphere** — color, material, light, mood.
2. **Semantic Context** — space, props, or context that explains relevance.
3. **Attention Guidance** — light, contrast, depth, framing, or motion that returns attention to the product/message.

Remove elements that do not serve communication, context, attention, brand, or necessary production function.

## Main-visual default Dual-Hero production cards

Use when the client asks only for `主视觉 / 商品主视觉 / hero visual / campaign hero / 核心视觉` and does not explicitly say one image. Set `hero_output_mode: DUAL_DEFAULT` and compile two separate integrated hero plans linked by `paired_anchor_id`. Do not wait for a second instruction and do not treat Hero A as an intermediate for Hero B.

If the client explicitly requests one image, set `hero_output_mode: SINGLE_EXPLICIT` and create exactly one complete poster in the requested role (or product-focused by default). Other explicit counts use `COUNT_EXPLICIT` and compile that many complete plans. For `成品海报 / 电商促销海报 / final poster`, apply the SAME dual-hero default as main visuals. Every member is a final poster, not a background or auxiliary scene.

### Hero A — Product Hero

Use the Product Hero Impact Protocol (`product-hero-impact.md`). Internally compare 2–3 product-specific visual strategies and compile the strongest one. The result must foreground a real signature form/material/benefit through at least two supported camera, scale, light, depth, background contrast or typographic mechanisms; avoid universal extreme effects.

Must explicitly resolve:
- `communication_job`: PRODUCT DESIRE,
- `product_scale`,
- `camera`,
- `composition`,
- `background`,
- `lighting`,
- `copy_zone`,
- `reference_mapping`.

The plan must make the product the primary visual mass and keep the background supportive.

### Hero B — Usage Hero

Must explicitly resolve:
- `communication_job`: USAGE DESIRE / EXPERIENCE,
- `user` or other actor,
- `usage_action`,
- `interaction` and contact points,
- `camera`,
- `environment`,
- `lighting`,
- `copy_zone`,
- `reference_mapping`.

The action must be active and category-valid. Record required occlusion, pressure, containment, grip, body fit, fur/hair overlap, food/liquid behavior, or other interaction evidence when applicable.

Pair-level compilation must confirm shared Campaign Visual System locks and meaningful differences in composition, camera, evidence route, and scene function.

Hero B must show active use, not lifestyle adjacency. Examples include an eye mask visibly worn with credible fit/occlusion, TWS earbuds worn in-ear, or a pet drinking from a fountain with believable muzzle/water/contact behavior. A person, hand, or pet merely appearing near the product does not satisfy the plan.

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

Every ADOPT item in `reference_map` must appear in `output_trace` and constrain a production field. References without a production trace are removed or marked non-influential; they cannot be cited as adopted.

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

For direct-final poster work, every unified composition field and the Typography Prominence Contract must be resolved before rendering. The headline–product relationship and text contrast field cannot be blank. For referenced work, `reference_adoption` must be resolved before rendering. For scene-based work, the applicable integration fields must be resolved rather than left as generic “match lighting” instructions.

For typography-bearing poster work, `typography_contrast_contract` must be complete in this order: headline/price/selling-point zones → local background complexity/tone → text color → headline size/weight → contrast field → lightweight fallback enhancement if needed → 100%/50%/25% and 2-Second Read Test. Midtone fields that do not separate decisively from either light or dark text must be intentionally shifted/simplified before rendering.

For `DUAL_DEFAULT`, readiness requires a fully resolved Product Hero Impact strategy for Hero A (signature product focus, ≥2 justified impact levers, identity protection and typography fit) and two distinct COMPLETE FINAL POSTER cards, matching campaign visual system, confirmed commercial text, active-usage evidence for Hero B, preplanned title/price contrast fields, joint-generation plan, and explicit differences in camera/composition/scene-function/evidence. Missing Hero B, missing final copy, or a background-only variation is `BLOCKED`, not a smaller package.

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
