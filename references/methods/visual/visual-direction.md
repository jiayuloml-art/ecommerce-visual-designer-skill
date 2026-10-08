# Visual Direction

Purpose: convert strategy and benchmark evidence into a product-specific visual proposition before composition or rendering.

This module answers: **why should this visual look this way?**

It does not render assets, choose providers, or perform final QA.

## Inputs
Use only what is relevant:
- communication job / viewer question,
- product truth and available product evidence,
- brand evidence,
- platform/surface state,
- selected selling point(s),
- required visible evidence / evidence route when the viewer question depends on demonstration or context,
- benchmark synthesis and references when required,
- approved campaign locks for revisions/extensions.

When category materially changes use, sensory response, trust, material treatment, or purchase imagination, also load the Category Visual Intelligence result from `references/context/categories/category-playbooks.md`.

## Output: Visual Direction Card

### Communication job
What must the visual accomplish for the viewer?

### First impression
What should be understood or felt within the first viewing moment?

### Visual thesis
State one product-specific design proposition that explains the visual relationship, not only the mood.

Weak:
> warm, young, premium, lifestyle

Stronger:
> Turn airflow into the spatial link between purifier, room, and headline so “small-space clean air” is visible as a relationship rather than stated as a label.

Mood words may support the thesis; they cannot replace it.

### Product role
Define how the product participates in the visual:
- dominant object,
- object in context,
- object + effect,
- object + evidence,
- object + copy,
- another deliberate relationship.

Do not encode aesthetic judgment as a universal product-area percentage.

For hero work, product prominence is non-negotiable even when the chosen mechanism uses a person, architecture, or an expressive environment. The Product Hero must make the product the first visual subject; the Usage Hero must make the product-use relationship—not the model or room—the first meaningful read.

### Product–scene relationship
When a scene is used, define **how the product physically or visually participates in it**.

Prefer a relationship expressed as an action or spatial interaction, for example:
- held / gripped / picked up,
- inserted into a verified holder or storage context,
- supported by or resting against a scene object,
- partially occluded by a foreground object,
- cropped into the frame to create proximity,
- nested in a workspace / travel / use context,
- connected to a semantic effect or directional graphic system.

Do not reduce this to coordinates such as “product on the right”.

**Product Identity Lock ≠ Source Pixel Lock ≠ Product Pose Lock.**

A supplied product image is a source of product truth; it is **not automatically a requirement to reuse those exact pixels, that exact camera, or that exact pose**.

Resolve the product representation mode for the output:

- `SOURCE_PIXEL_LOCKED` — exact supplied pixels / approved render must be preserved; use when the client, legal/compliance, retouching requirement, or product-fidelity risk demands it.
- `IDENTITY_PRESERVING_RECONSTRUCTION` — the supplied image is a visual identity reference. The product may be re-rendered / reconstructed into a better camera, pose, crop, contact relation, or verified functional state when product identity can remain stable.
- `AUTHORIZED_CONCEPT_STATE` — the client explicitly authorizes an alternate/open/hidden state whose exact geometry is not fully evidenced. It may be used as a clearly provisional/conceptual depiction, not as factual mechanism proof.

Preserve verified identity anchors: overall product family/form, proportions that are known, color/material, branding, controls/components that are visible/confirmed, quantity/variant, and verified functional relationships.

Prefer reference-grounded reconstruction over a visibly pasted cutout when exact source pixels prevent credible scene integration and the chosen representation mode allows reconstruction.

For functional states such as opening, folding, extending, inserting, wearing, or operating:
- if the state and geometry are evidenced, reconstruct it faithfully;
- if the function is confirmed but exact hidden geometry is not, use the Evidence Authorization Ladder before showing a reconstructed state;
- if concept authorization is granted, keep the depiction plausible and avoid presenting the invented hidden geometry as technical proof.

Any physical interaction must remain plausible for the product and must not imply an unsupported function, accessory, performance claim, or exact hidden geometry.

### Distinctive visual mechanism
Resolve at least one mechanism that makes the direction more than a category template, such as:
- spatial framing,
- scale/crop tension,
- depth/occlusion,
- product-context interaction,
- material/light behavior,
- semantic visual effect,
- typographic counterweight,
- brand-specific graphic behavior.

If the same mechanism would work unchanged after swapping in any competitor product and logo, strengthen specificity.

### Scene logic
Define what the environment must communicate and which contextual elements are necessary. Avoid decorating the scene with props that do not support meaning, scale, attention, or brand.

For daily-use functional physical products, default toward a **credible use context** rather than an abstract design stage when the communication goal benefits from purchase imagination, relevance, or use understanding.

Prefer, in order when appropriate:
1. real use action / physical interaction,
2. credible use-context environment,
3. use-adjacent context with clear scale/use cues,
4. abstract symbolic stage only when it better serves the approved communication job.

A person is optional; believable product ownership/use context is the requirement.

If an abstract pedestal/geometric scene is chosen instead, state the functional reason. Pure polish, “premium feeling”, or empty visual spectacle is insufficient.

### Semantic effect
Any particles, airflow, light trails, gradients, waves, diagrams, overlays, or graphic devices must have a communication role.

Prefer effects that serve more than one function:
- meaning,
- composition,
- attention guidance,
- brand/product specificity.

**Effect must communicate, not decorate.**

### Emotional tone
Record the intended emotional quality only after the visual mechanism is clear.

### Negative direction
Define:
- category clichés to avoid,
- AI slop to avoid,
- client-declared dislikes,
- visual approaches contradicted by product/brand evidence.

Include these defaults when relevant:
- pasted-on product,
- inconsistent lighting or shadows,
- floating without a semantic reason,
- fake contact / incorrect hand or body interaction,
- wrong scale or camera mismatch,
- background / model / props stronger than product,
- generic AI luxury styling,
- excessive glow, particles, fog, neon, futuristic UI, or decorative gradients,
- lifestyle scene without active use,
- reference researched but not visibly adopted,
- product too small at thumbnail size,
- fake materials or excessive depth of field that hides the product.

## Category Visual Intelligence

Derive the direction through this chain:

**CATEGORY → SUBCATEGORY → PURCHASE MOTIVATION → USAGE CONTEXT → SENSORY ATTRIBUTE → BRAND POSITIONING → VISUAL GRAMMAR**

Category supplies a prior, not a finished style. Resolve how category-specific viewer questions, use behavior, material response, trust expectations, and sensory cues change the product view, action, scene, light, camera, and evidence. Then override generic priors with verified brand rules, platform behavior, product truth, selling point, price tier, audience, and selected references.

Do not use fixed equations such as technology = blue gradient, sustainability = green, beauty = pink, premium = black/gold, sport = red/black, or baby = pink/blue.

## Visual Diversity Guard and Style Justification

Before locking the direction, check whether the current or recent work is defaulting without evidence to:
- purple-blue gradient,
- floating product,
- glowing ring,
- pedestal,
- fog / neon / particles,
- abstract wave,
- centered object,
- split layout,
- giant sans-serif headline,
- generic futuristic studio.

For each major visual choice, record a concise Style Justification:

```yaml
decision:
supported_by: # product attribute / brand / selling point / category intelligence / platform / reference
why_it_serves_this_product:
rejected_default_or_cliche:
```

If the answer is only “it looks premium”, the decision is unsupported. Remove or replace it.

## Dual-Hero Visual Direction

When Dual-Hero applies, resolve one shared campaign thesis plus two non-redundant expressions.

### Hero A — Product Hero
- communication job: PRODUCT DESIRE,
- first impression: product identity + primary benefit,
- define product scale, camera/view, composition, background role, lighting, copy zone, and reference mapping,
- environment and effects remain subordinate to product form/material/benefit.

### Hero B — Usage Hero
- communication job: USAGE DESIRE / EXPERIENCE,
- first impression: product actively used in a category-valid relationship,
- define user/pet/object, exact usage action, contact/occlusion, camera, environment, lighting, copy zone, and reference mapping,
- the user or environment may supply emotion and scale but may not overpower the product-use relationship.

The pair must share color/material/type/brand logic while differing in camera, composition backbone, scene function, and evidence route. A background swap is not a second hero.

## Reference Transfer Map

When benchmarking was used, retain an internal trace for selected references:

**Reference → Visible observation → Mechanism extracted → Current design use → Do-not-copy boundary**

“Current design use” must name the decision actually affected, such as:
- product placement / crop / angle,
- product–scene interaction,
- scene cue or human action,
- typography scale / line break / spatial relation,
- color / light / material treatment,
- graphic / semantic effect,
- depth / overlap / negative-space behavior.

A reference that produces only a mood adjective or post-hoc explanation is not considered transferred.

The benchmark is not complete for visual direction if it yields only URLs, style adjectives, or generic language that would remain true for almost any layout.

### Client-facing reference basis
When benchmarking was required, CLIENT MODE **must** show a concise 2–4 reference summary with the direction/delivery:
- reference/source,
- mechanism learned,
- where that mechanism appears in the current design.

Do not dump the full research log or copy a reference layout.

## Completion gate

Visual Direction is resolved only when all are true:
- the first impression is explicit,
- the visual thesis describes an executable relationship,
- product role is clear,
- product–scene relationship is explicit when a scene is used,
- required visible evidence is compatible with the chosen scene / interaction when the viewer question depends on evidence,
- at least one distinctive visual mechanism is defined,
- scene/effect logic is purposeful where applicable,
- benchmark evidence has been translated into named current-design decisions when benchmarking was required,
- negative direction is known.
- Category Visual Intelligence has been applied when material, and no fixed category-style shortcut is used.
- major visual decisions have Style Justification and pass the Visual Diversity Guard.
- when Dual-Hero applies, both hero expressions and their meaningful differences are explicit.

If these are not resolved, do not move to composition or rendering.

## Persistence
Persist approved direction outputs into the Campaign Visual System. Do not persist hidden reasoning or speculative intermediate chains.
