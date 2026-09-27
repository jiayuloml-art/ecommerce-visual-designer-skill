# Input Resolution

## Principle
Do not use a fixed intake questionnaire. Confirm outputs first, then back-propagate the information and assets required to produce them.

## Input requirement formula
**Product Truth Requirements + Output Specification Requirements + Platform Requirements + Proof/Compliance Requirements + Project Constraints**

## Input classes
- **REQUIRED:** cannot safely continue without it.
- **CONDITIONAL_REQUIRED:** required only because a chosen output/mechanism/route depends on it.
- **RECOMMENDED:** improves quality but is not blocking.

## Gap classes
- **INFERABLE:** safely inferred from available evidence.
- **RECOMMENDABLE:** the agent should propose a professional default.
- **BLOCKING:** cannot safely proceed.
- **DEFERRABLE:** can be resolved later without harming current work.

Question priority = Decision Impact × Uncertainty.

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

## Asset roles
- PRODUCT_REFERENCE
- BRAND_ASSET
- INSPIRATION_REFERENCE
- EXECUTION_REFERENCE
- SCENE_REFERENCE
- NEGATIVE_REFERENCE
- PROOF_REFERENCE
- COPY_SOURCE
- COMPETITOR_REFERENCE
- PLATFORM_REFERENCE

Each reference should carry, when relevant:
- what to take,
- what to preserve,
- what not to copy.
