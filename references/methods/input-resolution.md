# Input Resolution

## Principle
Do not use a fixed intake questionnaire. Confirm outputs first, then back-propagate the information and assets required to produce them.

## Input requirement formula
**Product Truth Requirements + Output Specification Requirements + Platform Requirements + Proof/Compliance Requirements + Project Constraints**

## Input classes
- **REQUIRED:** cannot safely continue with the dependent branch without it.
- **CONDITIONAL_REQUIRED:** required only because a chosen output/mechanism/route depends on it.
- **RECOMMENDED:** improves quality but is not blocking.

## Gap classes
- **INFERABLE:** safely inferred from available evidence.
- **RECOMMENDABLE:** the agent should propose a professional default.
- **BLOCKING:** the dependent branch cannot safely proceed.
- **DEFERRABLE:** can be resolved later without harming current work.

Question priority = Decision Impact × Uncertainty.

## Evidence priority
Use the strongest available evidence:
1. user-verified fact or explicit client decision,
2. official specification / manual / brand source,
3. supplied project document,
4. unambiguous visible information in supplied assets,
5. category/domain knowledge only as a **HYPOTHESIS** until verified.

Do not upgrade lower-confidence evidence into verified truth.

## Truth states
- **CONFIRMED FACT** — directly verified.
- **DERIVED BENEFIT** — reasonable benefit derived from confirmed facts; keep the derivation traceable.
- **HYPOTHESIS** — plausible but not verified; never present it as product fact.

For truth-sensitive production, record:
- what must be preserved,
- what derivations are allowed,
- what inferences are prohibited.

## Scoped blocking
A missing or conflicting input blocks only the outputs, slots, claims, or production decisions that depend on it unless the unresolved item invalidates the whole direction.

Example:
- unresolved price → block exact promotional price layer,
- product image + verified geometry available → composition/background work may continue,
- unknown certification → block certification claim, not unrelated visual production.

## Upstream resolution first
When one upstream answer can resolve several downstream unknowns, resolve the upstream item first. Do not ask the client separately for downstream choices the agent can determine afterward.

## Missing vs conflict
- **MISSING:** no supported value exists.
- **CONFLICT:** two or more credible sources disagree.

Do not silently pick a value from a conflict. Record it in project state and resolve only when the dependent branch requires it.

## Product truth examples
May include:
- exact model/SKU/variant,
- geometry and proportions,
- color/material,
- labels/logo,
- included accessories,
- current condition for second-hand goods,
- verified features/claims,
- dimensions/power/capacity only when supplied or verified.

Unknown product truth must never be converted into a verified-looking fact.

## Unseen geometry rule
Not observed does not equal verified. Do not invent product backs, interiors, opened states, hidden mechanisms, accessories, ports, controls, or structural details that are not supported by evidence.

## Asset roles
- PRODUCT_REFERENCE
- BRAND_ASSET
- INSPIRATION_REFERENCE
- EXECUTION_REFERENCE
- SCENE_REFERENCE
- COMPOSITION_REFERENCE
- MOTION_REFERENCE
- NEGATIVE_REFERENCE
- PROOF_REFERENCE
- COPY_SOURCE
- COMPETITOR_REFERENCE
- PLATFORM_REFERENCE

Each reference should carry, when relevant:
- what to take,
- what to preserve,
- what not to copy,
- coverage limits.
