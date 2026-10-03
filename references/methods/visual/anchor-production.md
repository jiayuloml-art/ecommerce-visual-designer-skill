# Anchor Production

Purpose: produce a representative hero/KV/anchor from an approved Visual Direction and Composition Contract while preserving product truth and visual quality.

This module owns production order. It does not invent the direction and it does not self-approve the final visual.

Required sequence:

**READY → PRODUCT VIEW → SCENE/CAMERA → PRODUCT INTEGRATION → SEMANTIC EFFECT → TYPOGRAPHY → CANDIDATE**

A later stage must not bypass a failed prerequisite.

## A0 — READY
Confirm:
- Visual Direction completed,
- Composition Contract completed,
- product truth locks,
- usable product evidence/assets,
- platform/surface state or explicit concept-only status,
- production route,
- recovery route,
- active runtime/provider capability.

Do not start an expensive image call merely because a mood is known.

## A1 — PRODUCT VIEW

### Product identity lock
Protect verified identity:
- silhouette/form,
- proportions,
- color/material,
- logo/labels,
- controls/components,
- quantity/variant,
- supported structural features.

### View flexibility
**Product identity locked does not mean camera view locked.**

Assign the usable view state from evidence:

- `VIEW_LOCKED` — only one trustworthy view / insufficient geometry evidence; scene must adapt to that view.
- `VIEW_SELECTABLE` — multiple trustworthy official/source views exist; choose the view that best serves the composition.
- `VIEW_RECONSTRUCTABLE` — sufficient multi-view/video/360/3D/reference evidence exists and the production route can create a new camera view while preserving identity; rendered result requires strict T2 comparison.
- `VIEW_PROHIBITED` — the intended view would expose unsupported geometry/structure; do not fabricate it.

Prefer a better verified view when the supplied view is incompatible with the intended scene. Do not keep a poor camera match merely to preserve source pixels.

## A2 — SCENE / CAMERA

Build or select the scene for the chosen product view.

Resolve as applicable:
- horizon/camera height,
- perspective strength,
- product placement plane,
- environmental scale cues,
- product scale relative to nearby objects,
- source/environment light direction,
- light softness/color temperature,
- copy/effect space,
- foreground/midground/background roles.

A beautiful room is not enough. It must be camera-compatible with the product.

### Scene checkpoint
Without final product/copy, verify:
- plausible placement plane,
- compatible perspective,
- believable environmental scale,
- compatible light system,
- sufficient composition space,
- semantic relevance to the Visual Thesis.

If FAIL, rebuild/reselect the scene.

## A3 — PRODUCT INTEGRATION

Composite/edit/reconstruct according to the view state and chosen route.

Check and repair as applicable:
- scale,
- perspective,
- grounding/contact,
- cast/contact shadow,
- ambient color/light influence,
- edge quality,
- occlusion/depth,
- reflection/material response,
- identity locks.

### Integration checkpoint — no final typography
Inspect product + scene without final copy.

The product must look physically present in the same photographic world.

If it reads as a sticker, cutout, floating layer, isolated card, oversized/miniature object, or mismatched light source, integration FAILS.

A fallback that preserves exact pixels but fails integration remains an internal recovery draft.

## A4 — SEMANTIC EFFECT

If the Visual Direction uses an effect, add it only after product/scene geometry is stable.

The effect must:
- communicate a real idea or verified mechanism at the appropriate abstraction level,
- support attention/composition,
- visually belong to the scene or graphic system,
- avoid implying unsupported product performance.

Examples include airflow, particles, material transformation, light behavior, motion traces, or graphic systems.

Decorative overlays that do not strengthen meaning or composition should be removed.

## A5 — TYPOGRAPHY

Apply the approved Composition Contract.

Use the copy roles:
- IDENTITY,
- HOOK,
- SUPPORT,
- PROOF.

Keep strategy labels internal.
Render exact commercial/product text deterministically by default.

Check:
- first/second read,
- readable scale,
- purposeful line breaks,
- contrast,
- product/copy relationship,
- balance/tension,
- whether the type participates in the composition.

Do not add copy merely to fill empty space.

## A6 — CANDIDATE

Export an internal candidate and preserve passed upstream layers.

Do not call it completed, approved, or ready for client review yet.

Send the candidate to `visual-critic.md` and separately run applicable hard/integrity QA.

Only a candidate that passes both visual criticism and applicable hard gates may become CLIENT PREVIEW.

## Runtime / failure behavior
Use the active runtime adapter for provider wait budgets.

General rules:
- one active expensive call per production objective,
- classify stalled calls according to runtime rules,
- no repeated "still waiting" narration,
- no identical retry loops,
- preserve passed stage artifacts when rerouting,
- fallback does not waive visual quality.

## Repair map
- generic direction / weak idea → Visual Direction
- passive or template composition → Composition & Typography
- unsupported/new product geometry → A1 / Product Truth
- scene perspective/scale mismatch → A2
- cutout/shadow/light mismatch → A3
- meaningless effect → Visual Direction or A4
- text hierarchy/readability → Composition & Typography / A5
- stalled provider → runtime/failure recovery

## Expansion rule
Do not expand a failed or unapproved anchor into the campaign.
