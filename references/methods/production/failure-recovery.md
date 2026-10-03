# Failure and Recovery

## Core rule
Never silently guess. Never silently downgrade fidelity.

## Recovery order
1. RECOVER in the current route.
2. ALTERNATE ROUTE with equivalent capability.
3. MANUAL HANDOFF with a provider-ready production pack.
4. FOCUSED CLARIFICATION only for client-exclusive blocking information.

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
