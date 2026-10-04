# Anchor Production

Purpose: produce a representative hero/KV/anchor from an approved Visual Direction and Composition Contract while preserving product truth and visual quality.

This module owns production order. It does not invent the direction and it does not self-approve the final visual.

Required sequence:

**READY → PRODUCT VIEW → SCENE/CAMERA → PRODUCT INTEGRATION → SEMANTIC EFFECT → TYPOGRAPHY → CANDIDATE**

A later stage must not bypass a failed prerequisite.

## A0 — READY
Confirm:
- Visual Evidence Strategy resolved when the viewer question depends on use / fit / scale / interaction / detail / proof,
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

### Product representation mode
**Product identity locked does not mean source pixels or camera view are locked.**

Resolve both the representation mode and usable view state.

Representation mode:
- `SOURCE_PIXEL_LOCKED` — exact supplied/approved pixels must remain the product layer.
- `IDENTITY_PRESERVING_RECONSTRUCTION` — supplied assets define identity, but the product may be re-rendered/reconstructed into a better camera, pose, crop, contact relation, or verified functional state.
- `AUTHORIZED_CONCEPT_STATE` — client-authorized conceptual alternate/open/hidden state; provisional only, never technical proof.

View state:
- `VIEW_LOCKED` — only one trustworthy view / insufficient geometry evidence; if representation mode is source-pixel locked, the scene must adapt to that view.
- `VIEW_SELECTABLE` — multiple trustworthy official/source views exist; choose the view that best serves the composition.
- `VIEW_RECONSTRUCTABLE` — enough identity/geometry evidence exists to create a new camera view while preserving product identity; rendered result requires strict T2 comparison.
- `VIEW_PROHIBITED` — the intended view/state would expose unsupported geometry and has not received concept authorization.

Do not default to `SOURCE_PIXEL_LOCKED` merely because a PNG exists. If exact cutout reuse creates a stiff, pasted, or camera-incompatible result, prefer identity-preserving reconstruction when truth evidence and authorization allow it.

For an opened/operating state:
- verified visual/structural evidence → reconstruct faithfully,
- confirmed function but unresolved hidden geometry → trigger Evidence Authorization / HG2,
- explicit concept authorization → allow a plausible provisional state with the truth boundary recorded,
- no authorization → choose another truthful evidence route.

Prefer a better verified/reconstructable view when the supplied view is incompatible with the intended scene. Do not keep a poor camera match merely to preserve source pixels.

### Pose / interaction flexibility
**Product identity locked does not mean product pose or scene relationship must remain static.**

When evidence and the production route support it, the product may be:
- tilted or rotated within verified geometry,
- held or picked up,
- inserted into a verified holder / storage / use context,
- partially cropped or occluded,
- supported by or resting against another object,
- positioned to participate in foreground / midground depth,
- connected to a semantic effect or directional visual system.

Do not invent contact geometry, hidden surfaces, accessories, states, or functions that are not supported. If the desired interaction exceeds available evidence, keep the trustworthy product view and redesign the scene around it.

## A2 — SCENE / CAMERA

Build or select the scene for the chosen product view.

Resolve as applicable:
- intended product–scene relationship / action,
- human or object contact when used,
- horizon/camera height,
- perspective strength,
- product placement plane,
- environmental scale cues,
- product scale relative to nearby objects,
- dimensional basis when fit / containment / compatibility is part of the communication job,
- source/environment light direction,
- light softness/color temperature,
- copy/effect space,
- foreground/midground/background roles.

A beautiful room is not enough. It must be camera-compatible with the product.

### Scene checkpoint
Without final product/copy, verify:
- the intended product–scene relationship is geometrically plausible,
- the receiver/container/contact zone is actually located where the product can interact with it,
- human/object interaction has a credible contact path when used,
- plausible placement plane,
- compatible perspective,
- believable environmental scale,
- dimensionally plausible product/context relation when fit / compatibility is being implied,
- the intended containment / insertion depth can be achieved without faking the geometry through arbitrary masks or offsets,
- compatible light system,
- sufficient composition space,
- semantic relevance to the Visual Thesis.

If any intended interaction requires the product to be moved into a region or angle the scene does not support, Scene Fit FAILS. Rebuild/reselect the scene before integration.

## A3 — PRODUCT INTEGRATION

Composite/edit/reconstruct according to the view state and chosen route.

Check and repair as applicable:
- scale,
- dimensional plausibility / fit relation when relevant,
- human/object contact geometry,
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

If it reads as a sticker, cutout, floating layer, isolated card, oversized/miniature object, mismatched light source, or if the product is visibly not inside/on/against the object it is supposed to interact with, integration FAILS.

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
- scene perspective / scale / receiver-position mismatch → A2 / reselect scene
- repeated failure to create containment/contact through local offsets/masks → A2 / structural revision
- cutout/shadow/light mismatch with otherwise-valid geometry → A3
- meaningless effect → Visual Direction or A4
- text hierarchy/readability → Composition & Typography / A5
- stalled provider → runtime/failure recovery

## Expansion rule
Anchor-first is fail-closed.

When an anchor establishes the visual language for a multi-output package:
1. produce only the anchor,
2. run Visual Critic + applicable hard QA,
3. present the passing anchor for the required client approval,
4. record that approval,
5. only then render/export supporting outputs.

Planning supporting outputs, benchmark questions, evidence routes, or production needs before anchor approval is allowed. Rendering/exporting supporting outputs is not.

Do not expand a failed, unapproved, or NOT_CHECKED anchor into the campaign.
