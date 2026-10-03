# Independent Visual Critic

Purpose: judge the visible artifact independently from the producer's explanation.

The Critic evaluates **result, not intention**.

**INTENTION ≠ RESULT**

A producer saying "the shadow was checked", "the circles represent airflow", or "the reference was used" does not make those things visually successful.

## Independence rule

For the first criticism pass, use only:
- the rendered artifact,
- the concise communication goal / Brief,
- necessary product/source reference for identity comparison,
- intended viewing condition.

Do not read the producer's rationale, prompt, production note, self-QA report, or claimed design decisions before the first-pass visual judgment. This reduces confirmation bias.

After first-pass judgment, benchmark/reference trace may be inspected only to evaluate transfer and repair.

## Verdicts
Use only:
- **PASS** — visually suitable to become a client-preview candidate, subject to hard/integrity QA.
- **REVISE** — direction is viable; specific craft/production changes can repair it without rethinking the core visual proposition.
- **REJECT** — first-impression, direction, composition, or product-scene relationship is fundamentally weak/generic; return upstream.

Do not use an averaged aesthetic score.

## C0 — Two-second test

At intended thumbnail/mobile viewing size, answer from the visible result:
- What is noticed first?
- Is that the intended focal subject?
- Can the viewer tell what kind of product / offer this is?
- Is the communication direction roughly understandable?
- Does the artifact feel designed, or assembled from separate assets?

If the first impression is fundamentally wrong, use **REJECT** without rationalizing it through process notes.

## C1 — Composition
Inspect:
- focal hierarchy,
- balance/tension,
- negative space,
- crop/framing,
- depth/overlap,
- relationship among product, type, scene, and effect,
- whether the layout is a generic left-text/right-product or other default template without justification.

## C2 — Product / scene realism
Inspect:
- relative scale,
- perspective/camera compatibility,
- contact/weight,
- shadow direction/softness,
- environment light/color influence,
- edge quality,
- occlusion/depth,
- material response,
- product identity fidelity.

The product must look like it belongs to the same visual world as the scene.

## C3 — Typography
Inspect:
- identity legibility,
- headline impact,
- reading order,
- line breaks,
- rhythm/spacing,
- contrast,
- type/product relationship,
- whether typography is an active composition element.

Reject metadata-like strategy keywords, tiny accidental product identifiers, or text blocks that merely occupy empty space.

## C4 — Semantic effect
If effects exist:
- what do they communicate from the image alone?
- do they reinforce the product/benefit/context?
- do they guide attention?
- are they visually integrated?
- do they imply unsupported facts?

If an effect is only decoration, revise or remove it.

## C5 — Specificity
Ask:
- if the product were swapped for a competitor, would the design remain almost unchanged?
- if the logo were swapped, would the design remain almost unchanged?

If yes, product/brand specificity is insufficient.

## C6 — Strategy alignment
Confirm the visible result supports the approved communication job and first impression without relying on explanatory text outside the artifact.

## C7 — Benchmark transfer
Only after C0–C6, inspect the Reference Basis when benchmarking informed the direction.

Verify:
**Reference mechanism → visible artifact behavior**

A research summary with no visible transfer does not count.

## C8 — Element justification
Every non-required element should serve at least one:
- communication,
- semantic context,
- attention,
- product/brand identity,
- necessary production function.

Remove unjustified competition.

## Verdict + return map

Every non-PASS verdict must state:
- visible failure,
- responsible module/stage,
- exact repair target,
- what should remain preserved.

Typical routing:
- weak/generic visual thesis → Visual Direction → REJECT
- template/passive composition → Composition & Typography → REJECT or REVISE
- camera/scale/light mismatch → Anchor Production A2/A3 → REVISE
- typography hierarchy → Composition & Typography / A5 → REVISE
- decorative effect → Visual Direction / A4 → REVISE or REJECT
- product identity drift → Product Truth / A1 → REVISE
- benchmark not transferred → Visual Direction → REJECT

## Client-preview gate
The producer may not present an anchor as completed/approval-ready unless:
1. Visual Critic verdict is PASS, and
2. all applicable hard/integrity QA gates are PASS.

A concept status such as S0 does not waive basic visual quality.
