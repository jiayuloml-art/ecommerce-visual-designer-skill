# Failure and Recovery

## Core rule
Never silently guess. Never silently downgrade fidelity.

## Execution outcome states
Treat a tool/provider execution as one of:
- **SUCCESS** — a usable result was returned and can be verified.
- **FAILED** — an explicit error or unusable result was returned.
- **STALLED** — the call remains pending with no meaningful progress beyond the route/runtime's reasonable wait budget.

A STALLED call is a failure-recovery condition. Do not keep waiting indefinitely or repeatedly tell the client that the same call is still running.

## Recovery order
1. RECOVER in the current route.
2. ALTERNATE ROUTE with equivalent capability.
3. MANUAL HANDOFF with a provider-ready production pack.
4. FOCUSED CLARIFICATION only for client-exclusive blocking information.

## Bounded retry / stall recovery
For a FAILED or STALLED production call:
1. inspect whether the failure is transient and whether any useful partial artifact exists,
2. retry the same route at most once when there is a concrete reason the retry may succeed,
3. otherwise move to an equivalent alternate route,
4. if the alternate route materially reduces visual quality or fidelity, downgrade artifact status and state that limitation,
5. use manual handoff or focused clarification only when automatic recovery cannot responsibly continue.

Once the runtime's hard wait budget is reached:
- stop polling / waiting on that objective,
- mark the attempt `STALLED`,
- preserve any usable partial artifacts,
- continue only through the planned recovery route,
- do not later report active production time as though the stalled wait never occurred.

Do not restart the same expensive operation in a loop. Runtime-specific adapters/providers may define a reasonable wait budget; Core does not hard-code one universal minute threshold.

## Missing product information
- If non-blocking: omit or use explicit placeholder.
- If needed only later: defer.
- If blocking: ask one focused question.
- Never invent dimensions, performance, certifications, warranty, claims, price, or SKU facts.

## Conflicting information
- Keep the conflict explicit.
- Do not silently choose one source.
- Block only the dependent branch.
- Resolve at the nearest upstream source of truth when needed.

## Missing / stale platform spec
1. Check local verified reference.
2. Check current official source.
3. Check current merchant/admin UI if account-dependent.
4. Ask user for current UI screenshot if necessary.
5. If unresolved, remain `S1 PRODUCTION_DRAFT`; do not claim platform-ready.

## Provider unavailable
- Re-resolve current runtime capabilities.
- Try an equivalent available capability.
- If quality/fidelity changes materially, tell the client and request a choice only if needed.
- If no automatic route exists, create a provider-ready handoff package.

## External cost / asset upload
Trigger HG3 before unapproved external spend, credits, login, or third-party asset upload.

## Production-efficiency evidence
When execution is materially slow, stalled, retried, or rerouted, record compact operational evidence in development state when available:
- active production time when available,
- wall-clock elapsed time when materially different,
- elapsed time to first usable artifact,
- stalled/failed tool calls and stall duration,
- retry count,
- route changes,
- whether the final quality justified the added execution cost/time.

This is diagnostic evidence, not client-facing narration by default.

## Artifact failure
Classify:
- truth/fidelity failure,
- technical failure,
- regression,
- strategy/direction failure,
- structural visual failure,
- local polish failure,
- runtime/provider failure.

## QA Return Map
For each failure:
1. identify the responsible layer,
2. return to the nearest node that can actually correct it,
3. change the minimum number of variables,
4. preserve unaffected verified assets,
5. re-QA the affected scope.

Examples:
- fact/claim → Product Truth / input resolution,
- product form → product-preserving production route,
- hierarchy → production plan/composition,
- campaign drift → campaign visual system,
- exact copy → deterministic text/layout,
- export/spec → technical/export,
- provider unavailable → capability/provider routing.

Fix highest-impact failure first. Structural revision is justified only when local repair cannot satisfy the target.
