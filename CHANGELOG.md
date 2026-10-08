# Changelog

## [1.2.0] — Unreleased

### Added
- Fail-closed Output Contract Gate: ambiguous briefs receive a recommended output package and client approval before visual production; minimum questioning no longer permits silent output selection.
- Project workspace isolation: each distinct project uses an explicit active project scope instead of inheriting unrelated files from a shared parent directory.
- Portable relative project layout (`projects/<project-id>/input|state|working|output`) with runtime-specific path mapping.
- Explicit cross-project source-scope rules: sibling projects and prior artifacts are not current evidence unless deliberately selected.
- Pre-Production Readiness Gate before expensive or fidelity-sensitive production.
- Hero/KV craft framework and template-resistance check.
- Benchmark-to-visual mechanism deconstruction and completion gate.
- Fidelity-preserving product/scene integration pass.
- STALLED execution state, bounded retry, and production-efficiency evidence.
- Client-facing visual delivery rationale.
- Codex-specific runtime adapter with bounded image-generation wait budgets and staged exact-product hero routing.
- Hero typography craft and approval-ready anchor acceptance gate.
- Mandatory Anchor Production Protocol: READY → DESIGN LOCK → SCENE FIT → PRODUCT INTEGRATION → TYPOGRAPHY → FINAL QA → CLIENT PREVIEW, with fail-closed stage transitions and no client preview for failed candidates.
- Creative-proposition gate: a visual thesis must add an insight, tension, or device beyond the brief; restating or rewording client-supplied themes, campaign names, promo lines, or fact lines no longer qualifies as a concept.
- Named differentiation commitment: benchmark synthesis must end with at least one committed departure from category convention, handed off to Visual Direction and presented to the client as the distinctiveness rationale at direction approval.
- Ownable device requirement: new campaigns created without a client-supplied concept must name a repeatable distinctive device/motif across outputs or record an explicit, justified “quiet system” decision; mood, palette, and seasonal atmosphere are support layers, not mechanisms.
- Direction-level swap test: creative specificity is checked on the Visual Direction Card before composition, not only on finished artifacts; paraphrased concepts and category-typical mood-only systems are treated as insufficient specificity.

### Changed
- Project-state schema moved under `references/methods/` so runtime state guidance is routed with other task methods.
- Category scene validity now checks whether the product has a credible use/context relationship instead of accepting literal campaign-copy scenery.
- Visual Core reorganized into four explicit design responsibilities: Visual Direction, Composition & Typography, Anchor Production, and Independent Visual Critic.
- Product fidelity now separates Product Identity Lock from View Flexibility (VIEW_LOCKED / VIEW_SELECTABLE / VIEW_RECONSTRUCTABLE / VIEW_PROHIBITED).
- Scene production is camera-matched to the selected verified product view instead of generating a generic attractive background first.
- Visual effects require semantic/compositional purpose; decorative effects alone are insufficient.
- Final visual criticism is separated from producer self-QA; visible result is judged before rationale/self-QA to reduce confirmation bias.
- Hard artifact QA (truth/technical/regression/platform) is separated from aesthetic criticism.
- Visual Benchmarking now prioritizes target-platform/category evidence, qualifies samples by accessibility and visible market signals, keeps Market/Platform and Visual Excellence references distinct, and requires auditable benchmark deliverables before synthesis.
- Platform/input resolution now asks the minimum sufficient upstream question: when an output type is already known, resolve the target platform first and infer ordinary downstream surface defaults unless a remaining ambiguity materially changes execution.
- Input resolution now distinguishes filesystem accessibility from project evidence scope.
- Runtime adapters resolve host-neutral relative project paths rather than embedding one host's absolute/configuration path.
- Production routing keeps project state, intermediates, and outputs inside the active project workspace by default.
- Fallback routes must preserve a minimum visual-quality baseline; truth-preserving but visually degraded fallbacks remain recovery drafts rather than equivalent finals.
- Visual QA now checks whether benchmark principles visibly transfer into the artifact and tracks production efficiency separately from visual quality.

## [1.1.0] — 2026-10-03

V1.1 is the integrated baseline for external black-box testing. Test-driven corrections will be accumulated for V1.2.

### Added
- Task-operation routing: CREATE / EXTEND / REVISE / ADAPT / DIRECTION_ONLY.
- Scoped blocking and upstream-resolution rules.
- Selling-point discovery with evidence typing and visual-potential selection.
- Dual-track visual benchmarking: market/platform effectiveness + visual excellence.
- Viewer-question and no-redundant-output planning.
- Per-output/per-slot structured production compilation.
- Visual resource allocation and three-layer scene planning.
- Anchor-first expansion for multi-output work.
- Visual Excellence QA and QA Return Map.
- Host/runtime adapter contract separated from production-provider routing, including Skill packaging/invocation and tool/API binding semantics.
- Explicit tracking of prohibited inferences, unresolved conflicts, and QA states.

### Changed
- Product Truth now distinguishes confirmed facts, derived benefits, hypotheses, preserved invariants, and prohibited inferences.
- Client communication now formalizes professional autonomy.
- Art direction now includes visual priority, impact levers, and hero relation.
- Campaign Visual System now distinguishes fixed rules and allowed changes.
- Production routing now favors asset preservation and minimum-variable repair.
- Exact commercial text now has explicit rendering ownership.
- Repository references are organized under Context (including AI runtime conditions) and Methods.
- Runtime capability resolution is cross-cutting rather than limited to production.
- Repository growth follows stable-responsibility / caller / loading-condition / non-overlap governance.
- After hard gates pass, Visual Excellence is the primary optimization target.
- Product Truth now uses pre-lock, compile-guard, and rendered-result checkpoints where fidelity/claims matter.

### Preserved
- Seven-state Controller.
- D1–D6 diagnosis architecture.
- Communication Jobs J1–J8.
- Strategy-derived output package.
- Human Gates.
- Artifact status S0–S3 and CLEAN/CHANGED integrity.
- Execution modes E0–E3.
- Provider registry/routing as a provider-agnostic layer.

### Not adopted
- A second scene-type taxonomy overlapping Communication Jobs.
- Fixed visual-driver taxonomy as a mandatory runtime classification.
- Fixed product-size percentages or fixed editorial ratios.
- A universal 100-point QA score or aesthetic threshold that can override hard failures.
- Fixed full marketing bundles.
- Provider architecture limited to specific vendors.
- One deterministic composition technology as the only route.
- Empty host-specific runtime files without real behavior differences.
