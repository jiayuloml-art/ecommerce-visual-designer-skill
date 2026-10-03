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
When a hero requires both lifestyle atmosphere and strict product fidelity, prefer a staged route when appropriate:
1. create/source the scene or background without inventing the product,
2. preserve the verified product layer,
3. composite and integrate it into the scene,
4. apply deterministic typography/brand layers,
5. verify the rendered artifact against product source and art direction.

This staged pattern is **not** sufficient by itself when the communication job depends on a real interaction/contact relationship.

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

Do **not** default to “background-only generation + flat front-view product overlay” when the concept depends on real interaction. That route may be acceptable for atmosphere-only scenes, but it cannot substitute for missing use evidence.

If the required interaction cannot be produced truthfully with current evidence/capabilities, use the fallback evidence route from `visual-evidence-strategy.md` or block/request the minimum input.

If a required scene asset is missing, the production plan should identify and create/source it intentionally rather than defaulting to an empty template.

## Anchor-first production
For any representative hero/KV/anchor that will establish the visual language for later outputs, follow `anchor-production.md`.

That protocol is authoritative for stage order and client-preview eligibility:
**READY → DESIGN LOCK → SCENE FIT → PRODUCT INTEGRATION → TYPOGRAPHY → FINAL QA → CLIENT PREVIEW**.

Do not bypass failed gates, do not show an internal failed candidate as an approval-ready concept, and do not propagate a failed anchor across the set.

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
A fast generative concept may be used to validate direction before final production. Label it `S0 CONCEPT`; do not treat its text, pricing, product details, or platform specs as final.
