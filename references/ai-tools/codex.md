# Codex Runtime Adapter

This file contains non-empty, host-specific execution behavior for the current Codex workflow. Re-check if the host/runtime exposes materially different behavior in a future version.

## Scope
Use this adapter only when the active host is Codex. Core design logic remains in the shared Skill references.

## Project workspace
Resolve Core paths such as `projects/<project-id>/...` against the active Codex workspace. Keep Skill installation/configuration files separate from active-project inputs, working files, state, and outputs.

## Native image generation / edit behavior
Treat native image generation/edit as a potentially asynchronous or long-running provider call.

For a single direct-final poster or other expensive image objective:
- allow only one active generation/edit attempt for the same production objective at a time;
- do not narrate repeated "still waiting" progress messages;
- if no usable artifact or meaningful progress signal appears within the **soft wait budget of 6 minutes**, perform one status check and classify the call as suspected `STALLED`;
- if the same call still has no usable result by the **hard wait budget of 10 minutes total**, stop polling/waiting for that objective, record it as `STALLED`, and move to the planned alternate route;
- do not allow a background shell/process wait, status check, or image-inspection step to keep the same objective open past the hard budget without an explicit new recovery decision;
- retry the same expensive call at most once, and only when there is a concrete transient-failure reason;
- never restart identical generation/edit calls in a loop.

These are internal runtime defaults for production efficiency, not platform requirements. If the runtime exposes a reliable provider-specific timeout/progress contract, prefer that verified contract.

## Direct-final poster routing
When the user supplies a verified product asset, default to an integrated final-poster route:

1. analyze and lock product identity/truth;
2. resolve category strategy and reference mapping;
3. lock product position/scale, camera/horizon/lens feeling, contact surface, light/shadow direction, environment color/reflection, and copy/headline/price/brand zones as one composition;
4. use native generation/edit or an identity-preserving reconstruction/composite route that produces one coherent product–scene system;
5. place exact copy/logo/price/date/CTA deterministically inside the preplanned zones;
6. run Product–Background Fusion Score, Visual Critic, and hard artifact QA before delivery.

Do not default to generating a text-free empty background and later placing a flat product cutout on it. A verified product layer may be used only when the full route can produce matched camera/perspective, credible contact and shadows, environmental light spill/reflection, material response, natural occlusion, depth integration, and clean edges. Otherwise use a supported identity-preserving edit/reconstruction route or redesign the composition.

## Deterministic fallback
A local script/HTML/SVG/compositing fallback may preserve exact product pixels and copy, but it is not automatically visually acceptable.

If the fallback cannot produce plausible product-scene integration or art-directed typography:
- keep it as a working/recovery draft,
- do not ask the client to approve it as a final poster,
- either revise the composition locally or prepare a manual/provider handoff that preserves the approved art direction.

## Evidence to record in development state
When a production call stalls or reroutes, record when available:
- start time,
- active production time,
- wall-clock elapsed time when materially different,
- time to first usable artifact,
- soft/hard budget reached,
- stall duration,
- retry count,
- route change,
- final artifact status.

Do not expose this log in CLIENT MODE unless it changes the client's decision.
