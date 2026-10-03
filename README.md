# ecommerce-visual-designer

A portable AI Skill for e-commerce visual design.

## Version status

- **V1.1** is the current integrated baseline.
- It includes the completed four-peer capability integration and repository restructuring.
- External black-box validation remains intentionally outside this repository.
- Test-driven fixes discovered from V1.1 will be collected into **V1.2** rather than continuously mutating the V1.1 baseline.
- The original V1 baseline commit is `953d35840649bdfe067b80f79da836c7a72cb3ca`.

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

Recommended evaluation of the frozen V1.1 baseline:
- full-flow,
- boundary behavior,
- revision/local repair,
- capability failure,
- visual quality,
- cross-runtime behavior,
- holdout regression.

A visually attractive result is not automatically a pass. Product truth, compliance, technical readiness, client communication, routing, QA state, and artifact status remain non-negotiable hard constraints.

## Project workspace isolation

V1.2 evaluation introduces a portable project-isolation rule. The Skill installation path is not the default destination for project artifacts. Each new project is assigned a dedicated logical workspace relative to the active runtime/workspace root:

```text
projects/<project-id>/
├── input/
├── state/
├── working/
└── output/
```

The physical parent directory is runtime/user dependent. Core rules must not assume `.codex`, a Windows drive, a home directory, or any other host-specific absolute path. Sibling projects are outside the active evidence scope unless explicitly selected.

## Version iteration policy

Use **V1.1** as the fixed black-box test baseline. Record test findings externally. Consolidate validated fixes in `release/v1.2` so different testers do not unknowingly evaluate different V1.1 states. The V1.2 pull request serves as the integration and evaluation log; test evidence belongs in PR discussion rather than inside the runtime Skill.


## V1.2 Visual Core

Representative e-commerce visual production is organized as:

```text
Visual Benchmarking
        ↓
Visual Direction
        ↓
Composition & Typography
        ↓
Anchor Production
        ↓
Independent Visual Critic
        ↓
Client Preview / revision loop
```

Hard artifact QA (truth, technical, regression, platform/compliance) remains separate from visual criticism.
