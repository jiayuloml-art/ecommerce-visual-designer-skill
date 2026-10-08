# Production Routing

## Production routes
### R1 GENERATIVE
Use for conceptual/lifestyle imagery, backgrounds, illustration, creative exploration where product truth will not be fabricated.

### R2 EDIT
Use when existing product/person identity must be preserved while changing background, context, or local visual properties.

### R3 COMPOSITE
Use when exact product/brand assets should be combined with generated scenes, lighting, shadows, or graphics. A composite is incomplete until the product is plausibly integrated through scale/perspective, contact, shadow, ambient light/color, edge quality, depth, and occlusion where relevant.

### R4 LAYOUT
Use when exact typography, prices, parameters, CTA, icon systems, or structured information dominate.

### R5 VIDEO
Use for temporal output; resolve duration, shot plan, motion, camera, transition, subtitle, audio, and CTA timing.

### R6 HYBRID
Use when generative imagery and deterministic commercial layers must coexist.

## Routing principle
- High precision → deterministic / reference-grounded route.
- High creative freedom → generative route.
- Mixed requirements → hybrid route.
- Unknown product truth must never be generated as verified fact.
- Use the simplest route that satisfies quality, fidelity, and precision; escalate only when needed.

### Scene + exact-product pattern
For static e-commerce posters, default to a direct integrated route:
1. plan the full poster composition, including product, environment, camera, contact surface, light/shadow/reflection, foreground/background interaction, and all copy/commercial zones,
2. use an edit, identity-preserving reconstruction, compositing, or hybrid method that can make the product and scene one photographic system,
3. generate/render the integrated poster visual rather than an empty background,
4. composite exact typography, price, date, CTA, legal, and volatile commerce information into the pre-reserved zones,
5. run Product Truth, Product–Background Fusion Score, Visual Critic, and technical/compliance QA.

Do not default to `empty AI background → flat product PNG overlay`. A separate verified product layer is permitted only when the route includes real perspective/scale alignment, contact/weight, matched shadows, environmental light spill, reflection/material response, natural occlusion, depth, and edge integration. If these cannot be achieved, use an interaction-capable edit/reconstruction route or redesign the scene.

Deterministic typography remains encouraged; deterministic type completion does not make the visual a staged background workflow because its zones and hierarchy are resolved before generation.

### Interaction-aware routing
If the Visual Evidence Strategy requires any of the following:
- hand ↔ product,
- body ↔ wearable/product,
- product ↔ cup holder / bag / storage / appliance / furniture,
- foreground object ↔ product,
- use-state contact / containment / insertion,
- meaningful overlap / occlusion that proves context,

route production through a method that can preserve the required contact geometry and depth.

Prefer, as appropriate:
- **EDIT** when an existing product/person/context image can be modified while preserving identity,
- **COMPOSITE** when separate verified layers can be combined with masks, foreground/background occlusion, contact/shadow, and perspective control,
- **HYBRID** when generated context plus deterministic exact-product/text layers must coexist,
- **GENERATIVE / reconstruction** only when product evidence is sufficient for the required view/state and strict truth verification remains possible.

Do **not** use “background-only generation + flat front-view product overlay” as the final-poster route. A background-only asset may exist only as an internal recovery component, and it still requires a subsequent integration process that produces one camera/light/contact/material system before typography and delivery.

If the required interaction cannot be produced truthfully with current evidence/capabilities, use the fallback evidence route from `visual-evidence-strategy.md` or block/request the minimum input.

If a required scene asset is missing, the production plan should identify and create/source it intentionally rather than defaulting to an empty template.

### Usage Hero route test

Before selecting the provider/method, verify that the route can produce:
- the active action, not passive holding/posing,
- required contact and pressure,
- correct occlusion order,
- camera-compatible product and actor geometry,
- category-valid scale and material response,
- T2 identity verification after generation/edit/composite.

If not, the route is ineligible even if it can make an attractive lifestyle image.

## Direct final poster production
For static e-commerce posters/KVs, follow `direct-final-poster-generation.md`:

**PRODUCT ANALYSIS → CATEGORY VISUAL STRATEGY → REFERENCE EXTRACTION → FULL POSTER COMPOSITION PLAN → PRODUCT–SCENE INTEGRATION PLAN → DIRECT FINAL POSTER GENERATION → TYPOGRAPHY / COMMERCIAL INFO COMPOSITE → FINAL QA**.

Use `anchor-production.md` only for explicitly requested staged approval. Do not show an empty mood image, background plate, or isolated product layer as though it were the final campaign direction.

## Asset preservation
A verified layer is preserved by default when the requested change does not depend on it.

Examples:
- copy/price change → text/layout layer,
- background change → background/edit layer,
- local prop defect → local edit,
- product-fidelity defect → product-preserving route,
- structural hierarchy failure → composition revision,
- direction failure → art-direction revision.

## Locality rule
Prefer:
**local defect → local repair**
before:
**structural defect → structural revision**
before:
**direction defect → re-art-direction**

But local repair is allowed only after the **Recovery Viability Gate** in `failure-recovery.md`.

If the intended relationship depends on a different camera, product-placement plane, container geometry, product scale class, major occlusion path, or product view/pose, classify the defect as STRUCTURAL and return upstream immediately.

Do not keep a scene merely because some useful pixels already exist. Preserving a structurally incompatible scene is false economy.

Do not regenerate unrelated verified layers.

## Fallback quality rule
An alternate route is a recovery path, not permission to collapse visual quality. A fallback artifact must still satisfy the intended communication job and applicable Visual Excellence QA. If the fallback preserves truth but materially degrades the approved visual concept, label it as a recovery draft/prototype and do not present it as equivalent final output.

Generic white-card isolation, untouched cutout-on-template composition, or placeholder decoration is not a default product-preservation solution unless intentionally supported by the art direction.

## Slot-level routing
Different slots in one campaign may use different routes. The campaign visual system can remain shared while hero, detail, proof, price, and video units use different production methods.

## Project-local artifact routing
All generated task artifacts should be written inside the active project workspace by default.

Portable relative layout:
```text
projects/<project-id>/
├── input/
├── state/
├── working/
└── output/
```

This is a logical layout, not an absolute filesystem requirement. The runtime may map it to another host-specific location, but the boundaries must remain equivalent.

Rules:
- do not write normal project outputs into the Skill installation/configuration directory,
- do not reuse another project's `state/`, `working/`, or `output/` as implicit context,
- temporary scripts/intermediates created for a project belong in that project's `working/` area unless the runtime requires another temporary location,
- final exports belong in the active project's `output/`,
- if the user explicitly chooses another destination, preserve project/source attribution so future sessions do not treat unrelated files as current-project evidence.

## Visual concept prototype
A fast generative concept may be used only when the client explicitly requests exploration or when a documented blocker prevents direct final production. Label it `S0 CONCEPT`; do not present it as the default deliverable or as final text, pricing, product detail, or platform-ready output.
