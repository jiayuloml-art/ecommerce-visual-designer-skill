# ecommerce-visual-designer

A portable AI Skill for e-commerce visual design.

## Version status

- **V1.2** is the current unreleased Visual Quality Upgrade.
- **V1.1** remains the fixed integrated baseline for historical black-box comparison.
- V1.2 preserves the seven-state controller, Product Truth, Human Gates, platform verification, production/provider routing, project isolation, CLIENT MODE, artifact states, and deterministic commercial typography.
- External black-box validation remains intentionally outside this repository.
- The original V1 baseline commit is `953d35840649bdfe067b80f79da836c7a72cb3ca`.
- V1.2 routes explicit finished posters through **Direct Final Poster Generation**: one scene, one camera, one lighting system, one commercial composition, followed by deterministic exact-copy completion, a fail-closed Product–Background Fusion Score, and fail-closed Typography Contrast/Prominence checks.
- Explicit `主视觉 / 商品主视觉 / hero visual / campaign hero / 核心视觉` requests default to two coordinated outputs when the client does not explicitly ask for one: Hero A / Product Hero plus Hero B / active Usage Hero.

## What V1.1 changes

V1.1 keeps the seven-state controller and strengthens four areas:

1. **Strategy intelligence** — selling-point discovery and evidence-backed visual benchmarking.
2. **Production discipline** — non-redundant output planning, direct integrated poster generation, asset preservation, and local revision.
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

Representative final-poster production is organized as:

```text
Visual Benchmarking
        ↓
Visual Direction
        ↓
Full Poster Composition Plan
        ↓
Product–Scene Integration Plan
        ↓
Direct Final Poster Generation
        ↓
Integrated Text Verification / Minimal Repair if Needed
        ↓
Typography Prominence + Thumbnail QA
        ↓
Independent Visual Critic
        ↓
Client Preview / revision loop
```

Both main-visual and finished-poster requests default to this dual complete-poster branch:

```text
Shared Campaign Visual System
        ↓
Full Product Poster ── Full Active-Usage Poster
        ↓                         ↓
Independent QA              Independent QA
        └──────── Pair Consistency + Diversity Gate ────────┘
```

Both complete posters share color, brand character, type and reference logic, but differ in composition, camera and communication job. Both use Direct Final Poster Generation; explicit counts override the two-poster default.

Hard artifact QA (truth, technical, regression, platform/compliance) remains separate from visual criticism.

### Single-Image Hero A/B Confirmation Gate
If the client explicitly requests exactly one final image, the Skill no longer defaults to Product Hero. If its communication role is not clear, it MUST ask “Hero A（产品展示型）还是 Hero B（真实使用场景型）？” before generation. Explicit product showcase or active-use language settles the role without a redundant question; “你帮我选” allows a recommendation but requires the client's approval. Ratio 4:5, platform and general poster wording do not determine Hero role. The gate is separate from missing platform/price/claim confirmation and has a blocking `BLOCKED_AWAITING_USER` state. No quantity specified retains default TWO complete Product Hero + Usage Hero outputs. See `references/methods/single-image-hero-role-confirmation.md` and `tests/single-image-hero-role-regression.md`.

### No Placeholders & Mandatory Confirmation Gates
Final commercial image generation now requires a **Mandatory Missing-Input Confirmation Gate**: check the actual product/brand facts, verified requested claims, campaign price/discount/date/CTA and target platform. **No placeholders** (including blank price/date reserved areas), invented values, silent omission, or unapproved neutral-platform fallback. Ask for required missing fields and wait; the user can explicitly authorize removing a requested field and reflowing the design. Designer-owned visual choices remain autonomous; explicit output image count overrides the default two posters. A separate **Fail-Closed Final Delivery Gate** inspects rendered artwork for accurate required content and platform/quality checks before claiming completion. See `references/methods/production/mandatory-input-confirmation.md` and `tests/mandatory-missing-input-regression.md`.

### Product Hero Visual Impact Upgrade
Product Hero now has a dedicated `references/methods/visual/product-hero-impact.md` art-direction and QA protocol. Choose at least two product-specific visual levers—dominant recognizable silhouette, evidence-supported expressive camera, material-led cinematographic light, purposeful depth/compositional tension, product–scene contrast, or detailed focal proof—without fabricating product features or forcing neon/floating podiums. Judge the rendered Product Hero independently on focal dominance, camera/silhouette, material/light, composition energy and commercial/brand impact (each ≥7/10, total ≥40/50). This strengthens the product-focused poster without altering the Usage Hero active-use obligation, dual-complete-poster default or integrated typography.

### Product–Background Relationship Upgrade
New `references/methods/visual/product-scene-relationship.md` requires a product-first scene rationale, function/context relevance, visual material/form correspondence, spatial support, commercial focus and brand specificity. Independent five-part Relationship Score: all fields ≥7/10, total ≥40/50; this supplements (never replaces) ten-part physical Fusion Score. Background-swap tests reject generic scenery but allow justified minimal studios. Default two complete integrated posters and copy/usage rules remain unchanged.

### Visual Quality Upgrade

V1.2 adds nine connected mechanisms:

1. **Direct Final Poster Generation** — every static e-commerce output is planned and generated as a complete poster rather than an empty background plus product overlay.
2. **Product–Background Fusion Score** — ten 1–10 integration fields fail closed below 7 each or 80/100 total.
3. **Reference Adoption Protocol** — SEARCH → SELECT → DECOMPOSE → ADOPT → PRODUCE → COMPARE → REVISE. Every important reference records SOURCE / ADOPT / ADAPT / DO NOT COPY / IGNORE and a Reference → Output trace.
4. **Product–Environment Integration Protocol** — scene-based output fails closed on perspective, contact, shadow, light, environmental influence, occlusion, scale, color temperature, depth of field, edge integration, or material response.
5. **Category Visual Intelligence** — visual grammar is derived from category, subcategory, purchase motivation, use context, sensory attribute, brand positioning, platform, and benchmark evidence; category-to-color templates are prohibited.
6. **Commercial and diversity guards** — product + core benefit must survive thumbnail viewing, copy zones are reserved before generation, and unsupported AI-default styling requires revision.
7. **Typography Prominence Protocol** — headline, offer, brand, and selling points are planned as commercial visual structure before generation; scene-aware Text Contrast Fields, headline/product relationships, 100%/50%/25% checks, a 2-Second Read Test, and an eight-field 64/80 hard gate prevent technically present but commercially invisible copy.
8. **Default Dual Complete-Poster Router** — main-visual AND finished-poster requests without a count produce Product Hero + active Usage Hero as TWO independently complete advertising posters.
9. **Typography Contrast Hard Gate** — headline, price, and selling-point zones are designed before generation; local complexity/tone determines text color, size, weight, and contrast field; 100%/50%/25% plus 2-Second checks reject midtone washout, thin type, weak price hierarchy, and commercially invisible copy.

The upgraded system is intended to be:

**REFERENCE-INFORMED · PRODUCT-CENTERED · SCENE-INTEGRATED · TYPOGRAPHICALLY STRONG · CATEGORY-SPECIFIC · COMMERCIALLY READABLE · THUMBNAIL-LEGIBLE · VISUALLY DISTINCTIVE**

It is not a request for more decorative or more elaborate imagery.
