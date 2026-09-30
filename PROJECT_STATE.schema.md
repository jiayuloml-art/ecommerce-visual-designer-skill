# PROJECT_STATE Schema

Use this structure to persist project truth and decisions independently from chat history.

```yaml
project:
  id: null
  name: null
  current_stage: null
  task_operation: null # CREATE | EXTEND | REVISE | ADAPT | DIRECTION_ONLY
  mode: CLIENT

facts:
  product: {}
  product_condition: null
  audience: []
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

outputs:
  proposed: []
  confirmed: []
  completed: []
  pending: []
  slots: []

visual_system:
  visual_thesis: null
  perceptual_target: []
  locks: {}
  allowed_variations: {}
  distinctive_device: null
  approved_references: []
  negative_direction: []

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
    path_or_ref: null

pending:
  decisions: []
  inputs: []
  approvals: []
  conflicts: []

history:
  - timestamp: null
    change: null
    previous: null
    current: null
    reason: null
```

## Persistence rules
- Store confirmed facts, explicit derived benefits/hypotheses, prohibited inferences, client-approved decisions, and unresolved conflicts; do not store hidden reasoning.
- Keep missing information distinct from conflicting information.
- A new client decision supersedes an old decision explicitly; do not silently overwrite.
- Runtime/host capabilities are session properties and should not be persisted as durable project truth.
- If an approved artifact changes, set `integrity: CHANGED` until it passes affected-scope QA and required approval again.
- Keep only meaningful history entries: approved changes, rejected routes, resolved conflicts, platform changes, major visual-system changes, and final artifact versions.
