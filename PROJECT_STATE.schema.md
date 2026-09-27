# PROJECT_STATE Schema

Use this structure to persist project truth and decisions independently from chat history.

```yaml
project:
  id: null
  name: null
  current_stage: null
  mode: CLIENT

facts:
  product: {}
  product_condition: null
  audience: []
  commercial_context: {}
  verified_claims: []
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

visual_system:
  visual_thesis: null
  perceptual_target: []
  locks: {}
  allowed_variations: {}
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
    version: v1
    status: S0_CONCEPT
    integrity: CLEAN
    baseline: false
    qa_status: null
    path_or_ref: null

pending:
  decisions: []
  inputs: []
  approvals: []

history:
  - timestamp: null
    change: null
    previous: null
    current: null
    reason: null
```

## Persistence rules
- Store confirmed facts and client-approved decisions, not hidden reasoning.
- A new client decision supersedes an old decision explicitly; do not silently overwrite.
- If an approved artifact changes, set `integrity: CHANGED` until it passes QA and required approval again.
- Keep only meaningful history entries: approved changes, rejected routes, platform changes, major visual-system changes, and final artifact versions.
