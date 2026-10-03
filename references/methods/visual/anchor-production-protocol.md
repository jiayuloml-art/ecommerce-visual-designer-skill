# Anchor Production Protocol

Use this protocol for any representative hero/KV/anchor visual whose approval will propagate a visual language to later outputs.

This protocol is the **authoritative execution order** for anchor production. Supporting references such as `art-direction.md`, `production-plan.md`, `production-routing.md`, `layout-and-typography.md`, `visual-qa.md`, and runtime/provider adapters supply methods and checks, but they do not change the stage order below.

The purpose is to prevent the common failure mode:

**vague direction → render too early → patch product into scene → add text → declare success**

The required order is:

**READY → DESIGN LOCK → SCENE FIT → PRODUCT INTEGRATION → TYPOGRAPHY → FINAL QA → CLIENT PREVIEW**

A later stage must not begin while its preceding gate is FAIL or NOT_CHECKED.

---

## AP0 — READY

Before any expensive generation/edit call, confirm the minimum production-critical context.

Required when materially relevant:
- output role and intended viewing condition,
- platform/surface state or explicit concept-only status,
- product truth / identity locks,
- usable product asset(s),
- brand asset/state,
- benchmark synthesis when benchmarking is required,
- selected primary production route,
- selected recovery route.

If a missing item materially changes the anchor, ask the minimum upstream question.
If the gap is deferrable, mark the artifact `S0 CONCEPT` and continue only where the missing item does not affect the current stage.

**Gate AP0:** production may begin only when the anchor can be designed without inventing product/commercial truth.

---

## AP1 — DESIGN LOCK

Resolve the anchor as a design before rendering it.

Create a compact internal **Anchor Design Contract**:

### 1. First focal event
What should be noticed first at thumbnail/mobile viewing size?

### 2. Product relationship
How does the product relate to:
- scene,
- copy,
- evidence,
- brand,
- negative space?

### 3. Distinctive visual mechanism
Identify at least one deliberate mechanism that makes the anchor more than a generic category template, for example:
- spatial framing,
- scale/crop tension,
- product-context interaction,
- light/material behavior,
- graphic device,
- typographic counterweight,
- another product/brand-specific relationship.

### 4. Camera / scene fit
From the verified product source, infer only what is visibly supported:
- product view angle,
- vertical/perspective behavior,
- approximate camera height/horizon behavior,
- source light direction/softness,
- intended placement plane and environmental scale cues.

Design the scene **for the product view that actually exists**. Do not generate a beautiful room first and then search for a place to paste the product.

### 5. Typography role
Resolve:
- headline role,
- brand/product identification role,
- optional proof/support role,
- text-image spatial relationship,
- what will be omitted from the hero and deferred to supporting slots.

Exact wording may still use placeholders when commercial facts are unresolved.

### 6. Reference translation
If benchmarking was used, identify which concrete visual mechanisms are being transferred and which parts must not be copied.

**Gate AP1:** if the direction can be described only with mood adjectives (for example “warm”, “premium”, “young”, “clean”) and not with executable relationships, do not render yet.

---

## AP2 — SCENE FIT

Create/source the scene **without product and without final text** when a scene-based hero is required.

The scene must be planned around the AP1 camera/placement requirements:
- plausible product placement plane,
- compatible perspective,
- usable scale cues,
- compatible light direction and softness,
- intentional negative space for the planned copy relationship,
- semantic context that supports the communication job,
- no props that will compete with the product.

Do not treat an attractive background as sufficient.

### Scene Fit Check
Before inserting the product, verify:
- the target placement is geometrically plausible,
- environmental scale will not make the product look miniature/oversized,
- light can be reconciled with the real product asset,
- the intended focal hierarchy still has room to work,
- the scene supports the design thesis rather than merely matching a mood.

If FAIL: revise/regenerate the scene. Do not continue to product compositing.

**Gate AP2:** scene fit PASS.

---

## AP3 — PRODUCT INTEGRATION

Insert the verified product asset while preserving identity.

Required integration work as applicable:
- scale and perspective alignment,
- grounding/contact,
- cast/contact shadow,
- ambient light and color influence,
- edge treatment,
- depth and occlusion,
- reflection/material response when supported,
- protection of product silhouette, proportions, color, logo/label, controls/components, and quantity/variant.

### Integration Check — NO TYPOGRAPHY YET
Review the product+scene image without final copy.

Ask:
- Does the product look physically present in this environment?
- Does its scale agree with nearby objects/floor/wall cues?
- Does its lighting belong to the same scene?
- Is the contact/weight believable?
- Does it still match the verified source product?
- Is the product clearly the intended focal subject?

If the result looks like a cutout, sticker, floating object, isolated card, or unrelated layer, this gate is FAIL.

A deterministic fallback that preserves exact pixels but fails physical integration remains an **INTERNAL RECOVERY DRAFT**.

If FAIL: repair the responsible integration variable or change scene/route. Do not proceed to typography.

**Gate AP3:** product truth PASS + product-scene integration PASS.

---

## AP4 — TYPOGRAPHY

Only after AP3 passes, design the text layer.

For a hero/KV, typography is a second design pass, not a metadata dump.

Resolve:
- product/brand identification sufficient for the viewing context,
- headline hierarchy and purposeful line breaks,
- contrast and legibility,
- relation between type block and product focal subject,
- supporting copy only when it materially strengthens first-impression communication,
- deterministic rendering for exact commercial/product strings.

Avoid default UI-like pills/cards, tiny model names, scattered fact boxes, and text placed merely in leftover empty space unless the art direction specifically justifies them.

### Typography Check
Inspect both full size and intended thumbnail/mobile scale:
- Can the viewer identify what the product is?
- Is the first/second read intentional?
- Does the type participate in the composition?
- Is important text readable without zooming?
- Does the text strengthen rather than dilute the product focal point?

If FAIL: revise typography/layout only; preserve the passed product-scene composite.

**Gate AP4:** hero typography + information hierarchy PASS.

---

## AP5 — FINAL ANCHOR QA

Run the complete anchor acceptance gate before client preview.

Required applicable checks:
1. Product Truth / fidelity
2. Technical integrity
3. Platform/compliance state
4. Thumbnail / first impression
5. Grounding / product-scene integration
6. Composition rhythm
7. Hero typography / readability
8. Product specificity
9. Brand specificity
10. Strategy–visual alignment
11. Benchmark-to-artifact transfer when benchmarking was used
12. Element justification
13. Production-efficiency evidence when execution stalled/retried/rerouted

### Reject rule
If any anchor-critical visual check is FAIL:
- keep the artifact internal,
- identify the responsible stage,
- return to the nearest stage that can fix it,
- make the minimum-variable repair,
- re-run downstream gates.

Do **not** show a visibly failed artifact merely because it is labeled `S0 CONCEPT`.
`S0 CONCEPT` relaxes final platform completeness; it does not waive basic visual quality.

Do not describe a failed candidate as “completed”, “ready for direction approval”, or equivalent.

**Gate AP5:** all applicable anchor-critical checks PASS.

---

## AP6 — CLIENT PREVIEW

Only after AP5 passes:
- export the anchor artifact,
- state its actual artifact status (`S0` / `S1` / `S2` / `S3`),
- provide a concise client-facing design rationale,
- disclose only material unresolved platform/commercial constraints,
- request direction approval when appropriate.

A client preview is an approval candidate, not an internal diagnostic draft.

---

## Runtime / failure behavior

Use the active runtime adapter for wait budgets and provider-specific behavior.

General rules:
- only one active expensive generation/edit attempt for the same anchor objective at a time,
- do not narrate repeated waiting states,
- classify long-running calls as STALLED according to the runtime adapter,
- do not loop identical calls,
- fallback does not skip AP2–AP5 gates,
- a visually weaker fallback must not be promoted to client preview merely because the primary provider failed.

---

## Repair map

- scene perspective / scale mismatch → AP2
- product cutout / shadow / lighting mismatch → AP3
- product truth drift → AP3 or source asset
- headline / hierarchy / readability → AP4
- generic/template feeling → AP1, then rebuild downstream stages as needed
- benchmark not visible in artifact → AP1
- platform/export issue only → technical/export layer; preserve passed visual stages
- stalled provider/tool → runtime/failure recovery; preserve passed stage artifacts

---

## Expansion rule

Do not expand an anchor into a multi-image set until the client has approved an AP5-passed anchor or explicitly asks to continue despite a known limitation.

A failed anchor must never become the visual template for the rest of the campaign.
