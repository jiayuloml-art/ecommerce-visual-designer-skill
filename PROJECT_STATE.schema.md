# PROJECT_STATE Schema

Use this structure to persist project truth and decisions independently from chat history.

```yaml
project:
  id: null
  name: null
  current_stage: null
  task_operation: null # CREATE | EXTEND | REVISE | ADAPT | DIRECTION_ONLY
  mode: CLIENT
  workspace_rel: null # relative to the current runtime/workspace root; no machine-specific absolute path
  source_scope: [] # active-project files and explicitly allowed external references
  continuity: NEW # NEW | EXTEND | REVISE | ADAPT
  baseline_project: null # explicit only; never inferred from same product/brand
  inherited_truth_sources: [] # named base-truth sources only unless broader inheritance is explicitly approved

facts:
  product: {}
  product_condition: null
  audience: []
  evidence_authorizations: [] # unresolved/verified/user-described/concept-authorized/concept-prohibited truth-sensitive depiction decisions; include whether HG2 is required before fallback
  commercial_context: {}
  verified_claims: []
  derived_benefits: []
  hypotheses: []
  prohibited_inferences: []
  prohibited_or_unverified_claims: []

decisions:
  positioning: null
  platform: null
  surface: null
  strategy: null
  approved_direction: null
  generation_mode: DIRECT_FINAL_POSTER # DIRECT_FINAL_POSTER | EXPLICIT_STAGED_ANCHOR | OTHER
  category_visual_intelligence:
    category: null
    subcategory: null
    purchase_motivation: null
    usage_context: null
    sensory_attributes: []
    visual_grammar: []
    rejected_cliches: []
  style_justifications: []

outputs:
  proposed: []
  confirmed: []
  completed: []
  pending: []
  slots: []
  hero_output_mode: DUAL_DEFAULT # DUAL_DEFAULT | SINGLE_EXPLICIT | COUNT_EXPLICIT; hero and finished-poster requests share default
  recommended_deliverables_count: 2 # explicit count overrides
  product_hero_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
  usage_hero_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
  typography_contrast_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
  typography_prominence_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
  thumbnail_typography_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
  anchor_package:
    mode: null # SINGLE | DUAL_HERO | COUNT_EXPLICIT; DUAL_HERO default for hero and finished-poster requests without a specified count
    hero_a_product: null
    hero_b_usage: null
    pair_approval: NOT_CHECKED

visual_system:
  visual_thesis: null
  perceptual_target: []
  locks: {}
  allowed_variations: {}
  distinctive_device: null
  approved_references: []
  reference_adoption:
    records: [] # SOURCE / observations / ADOPT / ADAPT / DO_NOT_COPY / IGNORE
    output_traceability: []
    qa_status: NOT_CHECKED
  negative_direction: []
  diversity_guard:
    recent_devices: []
    unsupported_repetitions: []
  dual_hero_relationship:
    shared_locks: []
    required_differences: []
    pair_qa_status: NOT_CHECKED

technical_specs:
  platform: null
  surface: null
  category: null
  verified: {}
  design_defaults: {}
  runtime_checks_required: []
  last_verified: null

assets:
  available: []
  approved: []
  missing: []
  rejected: []

artifacts:
  - id: null
    output_id: null
    slot_id: null
    version: v1
    status: S0_CONCEPT
    integrity: CLEAN
    baseline: false
    qa_status: null
    qa_checks: {}
    visual_core_checks:
      product_presence: NOT_CHECKED
      commercial_readability: NOT_CHECKED
      reference_adoption: NOT_CHECKED
      product_environment_integration: NOT_CHECKED
      product_scene_relationship: NOT_CHECKED
      product_hero_impact: NOT_CHECKED # applicable to Product Hero
      category_fit: NOT_CHECKED
      visual_distinctiveness: NOT_CHECKED
      usage_authenticity: NOT_CHECKED
      copy_readiness: NOT_CHECKED
      thumbnail_impact: NOT_CHECKED
      typography_prominence: NOT_CHECKED
      product_truth: NOT_CHECKED
    integration_checks:
      perspective: NOT_CHECKED
      contact: NOT_CHECKED
      shadow: NOT_CHECKED
      light: NOT_CHECKED
      environmental_influence: NOT_CHECKED
      occlusion: NOT_CHECKED
      scale: NOT_CHECKED
      color_temperature: NOT_CHECKED
      depth_of_field: NOT_CHECKED
      edge_integration: NOT_CHECKED
      material_response: NOT_CHECKED
    final_poster_completeness:
      product_subject: NOT_CHECKED
      environment: NOT_CHECKED
      core_copy_zone: NOT_CHECKED
      selling_point_zone: NOT_CHECKED
      brand_zone: NOT_CHECKED
      campaign_zone: NOT_CHECKED
      commercial_hierarchy: NOT_CHECKED
    unified_composition:
      product_position: null
      product_scale: null
      camera_angle: null
      horizon: null
      contact_surface: null
      light_direction: null
      shadow_direction: null
      environment_color: null
      product_reflection: null
      copy_zone: null
      headline_zone: null
      price_zone: null
      brand_zone: null
    product_background_relationship:
      scene_role: null
      scene_specificity_thesis: null
      functional_relevance: null
      visual_correspondence: null
      spatial_relationship: null
      composition_guidance: null
      brand_emotional_fit: null
      background_swap_test: null
      role_specific_difference: null
    product_hero_impact:
      core_product_focal_advantage: null
      visual_impact_mechanism: null
      product_silhouette_read: null
      camera_angle_and_lens_logic: null
      product_frame_dominance_and_crop: null
      material_and_highlight_plan: null
      scene_to_product_contrast_plan: null
      product_typography_counterweight: null
      protected_identity_and_legibility_zones: []
      selected_direction_rationale: null
    product_hero_impact_score:
      product_focal_dominance: null
      camera_silhouette_expressiveness: null
      material_lighting_quality: null
      compositional_energy: null
      commercial_impact_brand_fit: null
      total: null
      status: NOT_CHECKED # each >=7/10 and total >=40/50
    product_scene_relationship_score:
      scene_relevance: null
      visual_correspondence: null
      spatial_integration: null
      commercial_hierarchy: null
      brand_consistency: null
      total: null
      status: NOT_CHECKED # all >=7, total >=40/50
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
    typography_prominence_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
    typography_contrast_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
    thumbnail_typography_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
    typography_contrast_contract:
      headline_text_color: null
      headline_size_strategy: null
      headline_weight_strategy: null
      headline_background_relation: null
      price_contrast_strategy: null
      selling_point_contrast_strategy: null
      local_background_complexity: null
      contrast_field_method: null
      fallback_enhancement: null
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
    integrated_visual_generation_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
    text_accuracy_verified_status: NOT_CHECKED # NOT_CHECKED | PASS | REVISE | FAIL
    text_repair_reason: null # only on failed integrated exact-copy rendering
    qa_invalidated_by_client_feedback: false
    path_or_ref: null

pending:
  decisions: []
  inputs: []
  approvals: []
  conflicts: []
  evidence_authorizations: [] # unresolved authorization decisions that block/downgrade approved evidence routes

history:
  - timestamp: null
    change: null
    previous: null
    current: null
    reason: null
```

## Persistence rules
- Keep one `PROJECT_STATE` per active project workspace. Do not reuse another project's state as implicit context for a new project.
- Store portable relative paths where possible; host/runtime-specific absolute paths may be used transiently for execution but should not become durable project truth.
- Cross-project references must be explicit in `source_scope`; sibling project folders are not implicitly readable evidence.
- Same product/brand/SKU does not imply continuity. New platform/campaign/output-family tests default to `continuity: NEW` unless the client explicitly selects an existing project/baseline.
- For `continuity: NEW`, inherit only specifically named base-truth sources; prior campaign state, prompts, generated scenes, visual direction, outputs, platform decisions, and QA are excluded by default.
- Store confirmed facts, explicit derived benefits/hypotheses, prohibited inferences, client-approved decisions, and unresolved conflicts; do not store hidden reasoning.
- Persist direct-final poster mode, unified composition fields, poster-completeness checks, and the ten-field Product–Background Fusion Score for every scene-based poster.
- Persist Typography Contrast status, Typography Prominence status, the eight-field prominence score, and 100%/50%/25% thumbnail typography status for every commercial poster. Applicable NOT_CHECKED, REVISE, or FAIL states are not deliverable PASS.
- Persist `hero_output_mode`, `recommended_deliverables_count`, `product_hero_status`, and `usage_hero_status`. Both main-visual AND finished-poster requests without a stated quantity use `DUAL_DEFAULT`: two individually complete posters with two PASS statuses and pair approval. Explicit one uses `SINGLE_EXPLICIT`; other explicit counts use `COUNT_EXPLICIT`. Record unified image+text rendering status, exact-copy verification and any needed localized repair reason.
- Persist separate hero readiness/QA and pair approval whenever the default or explicitly requested coordinated pair applies. For every Product Hero, persist its impact contract, chosen product-specific visual levers and five-field rendered Product Hero Impact Score (each ≥7/10, total ≥40/50), independently of product truth, scene relationship, fusion, and typography.
- Persist Reference Adoption Records and output traceability when references are used; a URL list without ADOPT/ADAPT/DO_NOT_COPY/IGNORE and mapped output fields is incomplete.
- Persist Category Visual Intelligence and Style Justification only as concise decisions/constraints, not hidden reasoning.
- Keep missing information distinct from conflicting information.
- A new client decision supersedes an old decision explicitly; do not silently overwrite.
- Runtime/host capabilities are session properties and should not be persisted as durable project truth.
- If an approved artifact changes, set `integrity: CHANGED` until it passes affected-scope QA and required approval again.
- If concrete client feedback contradicts a prior visual PASS, mark that artifact's affected QA scope invalidated and require re-QA after repair.
- Keep only meaningful history entries: approved changes, rejected routes, resolved conflicts, platform changes, major visual-system changes, and final artifact versions.
