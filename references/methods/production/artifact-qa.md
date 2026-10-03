# Artifact Integrity QA

Purpose: verify non-aesthetic hard gates independently from visual criticism.

This module checks truth, technical integrity, regression, and platform/compliance state. It does not decide whether a design is visually excellent.

Use states:
- **PASS**
- **FAIL**
- **NOT_CHECKED**
- **NOT_APPLICABLE**

Applicable NOT_CHECKED items are not PASS.

## Q0 — Product Truth / Fact QA
Check:
- product/SKU/variant/condition,
- geometry and identity locks,
- logo/labels,
- quantities/accessories,
- prices/offers,
- claims/parameters,
- certifications/legal facts,
- prohibited inferences.

For rendered product visuals, perform T2 comparison against supplied/verified product evidence.

## Q1 — Technical QA
Check as applicable:
- canvas/aspect ratio/resolution,
- format/file size,
- font/assets loaded,
- overflow/collision,
- safe zones,
- export integrity,
- duration/frame/audio/subtitle constraints for temporal outputs.

## Q2 — Regression QA
When an approved baseline exists, check unintended changes to:
- product identity,
- campaign locks,
- unaffected layout/content,
- exact copy,
- approved assets.

For generative imagery compare structural/semantic invariants, not only pixels.

## Q3 — Platform / Compliance QA
Check:
- platform/surface/output fit,
- latest verified technical rule state,
- claims/compliance,
- commercial text requirements,
- intended viewing condition.

If account-dependent or current platform rules are unresolved, do not claim platform-ready status.

## Blocking rule
Hard-gate failures cannot be averaged away by visual quality.

A visually strong artifact with an applicable hard-gate FAIL cannot become S2/S3 or be described as platform/final ready.

## Relationship to Visual Critic
A client-preview anchor requires:
- Visual Critic PASS, and
- all applicable hard/integrity gates PASS.

Keep visual criticism in `references/methods/visual/visual-critic.md`; do not move aesthetic judgments into this file.
