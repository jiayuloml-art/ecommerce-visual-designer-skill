# ecommerce-visual-designer

A Codex-compatible AI Skill for e-commerce visual design.

This V1 draft turns an incomplete client brief into a structured workflow for:
- diagnosis and strategy,
- output-package recommendation,
- platform and technical-spec resolution,
- art direction and campaign visual systems,
- production/tool routing,
- visual QA and delivery.

## Structure

- `SKILL.md` — main controller and operating rules
- `PROJECT_STATE.schema.md` — persistent project-state schema
- `references/` — progressively loaded design, platform, production, provider, and QA references

## Client behavior

The Skill defaults to **CLIENT MODE**: client-facing responses stay concise and decision-oriented. Internal taxonomies, state labels, routing logic, and debug diagnostics remain hidden unless development/debugging is explicitly requested.

## Testing

Black-box evaluation files are intentionally kept **outside this repository** so the tested agent cannot read expected behaviors in advance.

Recommended evaluation pattern:

1. Install/use this Skill in a fresh Codex context.
2. Provide only the test brief and any test assets.
3. Run the task without exposing the expected-behavior rubric.
4. Compare the result against the external evaluation rubric afterward.
5. Use DEVELOPMENT / DEBUG MODE only when diagnosing a failed test.

## Status

**V1 Draft** — ready for fresh-context black-box testing and iterative patching.

A visually attractive result is not automatically a pass. Product truth, client communication, routing, platform readiness, QA, and artifact status all matter.
