# ecommerce-visual-designer

A portable AI Skill for e-commerce visual design.

## Version status

- `main` remains the stable V1 baseline until V1.1 is approved.
- `release/v1.1` is the integration branch for the V1.1 architecture and behavior upgrade.
- The V1 baseline commit is `953d35840649bdfe067b80f79da836c7a72cb3ca`.

## What V1.1 changes

V1.1 keeps the seven-state controller and strengthens four areas:

1. **Strategy intelligence** — selling-point discovery and evidence-backed visual benchmarking.
2. **Production discipline** — non-redundant output planning, anchor-first expansion, asset preservation, and local revision.
3. **Production compilation** — structured per-output/slot plans with truth constraints, scene layers, visual resource allocation, text ownership, routing, and QA states.
4. **Runtime portability** — host/runtime adaptation is separated from production-provider selection.

## Repository structure

```text
SKILL.md
PROJECT_STATE.schema.md
CHANGELOG.md
references/
├── context/
│   ├── platforms/
│   └── categories/
├── methods/
│   ├── strategy/
│   ├── mediums/
│   ├── visual/
│   └── production/
└── ai-tools/
```

The upper-level structure separates:
- **context** — external task conditions,
- **methods** — design and production methods,
- **ai-tools** — host/runtime adaptation.

The detailed design taxonomy remains inside those layers rather than being flattened into one directory.

## Repository governance

Before adding a new runtime file, confirm all four:

1. **Stable responsibility** — the file owns a durable concept rather than one incidental idea.
2. **Clear caller** — a controller/reference can identify when it should be loaded.
3. **Loading condition** — there is a concrete reason to load it on demand.
4. **Non-overlap** — its responsibility is not already owned by an existing file.

Prefer strengthening an existing high-cohesion reference over creating a new file. Do not create empty host/provider/category files merely for symmetry.

## Client behavior

The Skill defaults to **CLIENT MODE**: client-facing responses stay concise and decision-oriented. Internal taxonomies, state labels, routing logic, and debug diagnostics remain hidden unless development/debugging is explicitly requested.

## Testing

Black-box evaluation files and expected-behavior rubrics remain outside the runtime Skill so the tested agent cannot read answers in advance.

Recommended evaluation after V1.1 integration:
- full-flow,
- boundary behavior,
- revision/local repair,
- capability failure,
- visual quality,
- cross-runtime behavior,
- holdout regression.

A visually attractive result is not automatically a pass. Product truth, compliance, technical readiness, client communication, routing, QA state, and artifact status remain non-negotiable hard constraints.
