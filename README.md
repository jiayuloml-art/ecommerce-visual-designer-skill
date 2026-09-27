# ecommerce-visual-designer — V1 Draft

This package is the first Codex-compatible draft derived from the V0.6 framework.

## Test philosophy
Use fresh-context black-box tests to separate skill quality from long-chat context leakage.

### Black-box mode
Give the agent only:
- this Skill package,
- one test brief,
- test assets when present.

Do not provide the expected-behavior file to the agent.

### Debug / regression mode
Enable DEVELOPMENT / DEBUG MODE and inspect routing, state, QA, and fallback behavior after a black-box failure.

## Recommended first test
`tests/T01-coffee-detail/brief.md`

Run once in a fresh context, then compare against `expected-behaviors.md`.

## Pass philosophy
A visually attractive result does not automatically pass. Truth, platform readiness, client communication, routing, and artifact status matter.
