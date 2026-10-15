# Visual Evidence Strategy

Purpose: decide **what the viewer must be able to see** before choosing scene, composition, or production route.

This module bridges:

**Viewer Question / Selling Point → Required Visible Evidence → Scene / Action / Detail / Proof → Production Need**

It prevents a selling point from being reduced to copy plus a decorative graphic device.

## When to use

Use for:
- hero/KV work where purchase desire depends on imagining use,
- supporting selling-point visuals,
- feature/demo slots,
- scenario or compatibility claims,
- any output where the viewer question cannot be answered by product presence alone.

Do not add a new questionnaire for the client. Resolve this internally from the approved output, Product Truth, category/use context, and available evidence.

## Evidence-first rule

Before composition, answer:

1. **Viewer Question** — what does the viewer need to understand or believe?
2. **Required Visible Evidence** — what should be visible for that answer to feel credible?
3. **Evidence Route** — what kind of visual evidence best answers it?
4. **Truth Boundary** — what can be shown without inventing geometry, behavior, performance, or context?
5. **Production Need** — what assets / interaction / edit / composite capability are required?

Copy may explain evidence; it should not substitute for missing evidence when the communication job depends on demonstration, context, fit, scale, or use.

## Evidence routes

These are a routing vocabulary, not a mandatory taxonomy. Use only what materially helps.

- **USE / ACTION** — a person or body part performs the relevant action.
- **CONTEXT FIT** — the product is shown credibly inside the real use environment or compatibility context.
- **DETAIL / MECHANISM** — a verified detail, control, opening, interface, material, or mechanism is shown closely enough to explain the point.
- **SCALE / RELATION** — nearby objects, body contact, or environment establish size, portability, fit, or spatial relationship.
- **PROOF / DATA** — verified test result, parameter, certification, comparison, or evidence is the primary support.
- **MATERIAL / SENSORY CUE** — verified material, finish, texture, temperature, food, liquid, or other sensory evidence is shown through appropriate photography/rendering.
- **SYMBOLIC / GRAPHIC** — a graphic abstraction communicates meaning. Use only when abstraction is appropriate to the job or when truth constraints make direct demonstration impossible.

Prefer evidence that directly answers the viewer question with the least semantic distance.

## Dual-Hero evidence split

When Dual-Hero applies:

- **Hero A — Product Hero:** visible evidence must make product identity, form/material, and the selected primary benefit legible. Product presence and benefit evidence take priority over lifestyle atmosphere.
- **Hero B — Usage Hero:** visible evidence must show active use and the resulting experience through a real contact/action relationship. A nearby person, hand, pet, room, or prop is not usage evidence by itself.

Resolve separate Slot Evidence Cards for both heroes. Reusing the Product Hero card for Usage Hero fails readiness.

### Active usage authenticity

Specify:
- actor: person / hand / body / pet / food or drink / environment / compatible object,
- action verb: wearing, gripping, inserting, applying, drinking, eating, pouring, charging, operating, feeding, playing, cleaning, organizing, etc.,
- contact points,
- expected occlusion / pressure / deformation / containment when applicable,
- functional result visible in the scene,
- truth boundary and required source evidence.

Reject passive substitutes such as “model holds product”, “pet sits beside product”, or “product appears in a home” when no functional action is visible.

## Daily-use functional product default

For ordinary physical products whose value is understood through use — such as drinkware, home appliances, kitchen tools, storage, commuting goods, wearables, and similar utility products — prefer:

**real use action / credible use context**
over
**abstract pedestal / geometric stage / decorative lifestyle background**

for hero and key selling-point visuals, unless a verified brand/campaign direction gives a stronger reason to abstract.

A person is not mandatory. A credible use-context scene may work through:
- hand / body contact,
- product inside a holder, workspace, bag, kitchen, bathroom, vehicle, or other real context,
- nearby objects that establish use and scale,
- realistic support / containment / occlusion,
- visible traces of actual use.

The scene should help the viewer imagine owning or using the product.

If an abstract stage is chosen for a daily-use functional product, record why it serves the communication job better than a credible use context. “Looks premium” is not sufficient by itself.

## Selling-point examples

### One-hand operation
Weak evidence:
- product cutout + arrow + “one-hand” copy.

Stronger evidence:
- verified hand/contact action,
- verified lid/control detail,
- or a truthful partial action that demonstrates the operation without inventing unseen geometry.

### Lightweight / portable
Weak evidence:
- motion line + “lightweight” copy.

Stronger evidence:
- carry / pick-up / bag / commute relationship,
- body-scale or object-scale cue,
- verified weight/proof when available.

### Cup-holder compatibility
Weak evidence:
- abstract circle standing in for a cup holder,
- context composite whose product/container scale is visually plausible but dimensionally unsupported while presented as fit proof.

Stronger evidence:
- credible vehicle cup-holder context,
- visible fit / scale relationship,
- verified product/container dimensions when available,
- or a clearly framed scenario illustration when dimensional proof is unavailable.

For fit / compatibility / containment claims, distinguish **contextual plausibility** from **dimensional proof**. If exact dimensions are unavailable, do not let a composite imply precision it does not have.

## Slot Evidence Card

For each meaningful slot, resolve:

```yaml
viewer_question:
communication_job:
selling_point_or_message:
required_visible_evidence:
evidence_route:
scene_or_action:
product_scene_relationship:
required_assets:
truth_boundary:
evidence_authorization_state:
benchmark_question:
production_implication:
fallback_evidence_route:
usage_actor:
usage_action:
contact_points: []
required_occlusion:
functional_result:
```

Do not force every field when irrelevant, but `required_visible_evidence` and `production_implication` must be explicit for supporting selling-point outputs.

## Missing evidence behavior

If the strongest evidence route requires unsupported geometry, hidden states, opened states, internal structure, or unavailable product interaction:

1. invoke the **Evidence Authorization Ladder** in `references/methods/input-resolution.md`,
2. first check for supplied visual/technical evidence,
3. if missing and decision-changing, ask for a relevant image/video/render or concise factual description,
4. if factual evidence remains unavailable, ask whether a clearly labeled conceptual visualization is acceptable,
5. if conceptual invention is not allowed, choose another truthful evidence route,
6. otherwise downgrade or remove the unsupported slot rather than decorating around the gap.

Client authorization to create a concept does not convert speculative structure into verified Product Truth.

## Handoff

Pass to:
- Visual Benchmarking: the unresolved evidence / interaction question to research,
- Visual Direction: the intended product/use relationship,
- Production Plan: required evidence, assets, and production implications,
- Production Routing: whether interaction-aware edit/composite/generation is required,
- Visual Critic: the viewer question and evidence expectation.

The module does not choose a final layout or provider.
