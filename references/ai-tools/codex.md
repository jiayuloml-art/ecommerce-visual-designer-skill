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

## Codex single-image Hero role stop-before-render
Run `references/methods/single-image-hero-role-confirmation.md` BEFORE any image tool/provider/script for `SINGLE_EXPLICIT`. Count = one does NOT mean product-focused default. If the brief explicitly says Hero A / product showcase, lock A; if it explicitly says Hero B / real active use, lock B; no redundant question. If role is unspecified (even with `4:5` / `成品海报`), ASK “你要 Hero A（产品展示型）还是 Hero B（真实使用场景型）？” and wait. If asked to pick, recommend but wait for an affirmative confirmation. Persist `selected_hero_role` and `single_image_hero_role_confirmation: PASS`. This gate is independent of platform/price/product-fact confirmation and cannot be bypassed by an image-generation provider, local script or autonomous creative decisions.

## Mandatory Codex stop-before-render behavior
Apply `references/methods/production/mandatory-input-confirmation.md` as an explicit preflight **before any image provider call or final poster script**. Inspect existing context and confirmed facts, then ask for each missing required final-content field (group related questions). Missing platform ALWAYS requires a question unless the user explicitly authorized a separate platform-neutral concept-only scope. Missing user-requested price/date (even when only 'reserved zones' were requested) must STOP formal generation until real values or affirmative omission permission arrive. Never create `¥___`, `____/____`, `XX元` placeholders, silently delete required text, or claim the unfinished/blocked image final. The few-questions preference does not supersede this hard gate. Resume only after facts/approval are recorded and preflight PASS, then run separate rendered-artifact final delivery QA.

## Direct-final poster routing
Both unspecified `主视觉` and `成品海报 / 电商促销海报` requests default to TWO complete posters (Product Hero + active Usage Hero); explicit image count overrides. For explicitly ONE poster with no role, STOP and confirm A/B; never pick Product Hero by default. Ratio 4:5 is not a count. Both outputs include commercial typography and undergo individual plus pair QA.
When the user supplies a verified product asset, default to an integrated final-poster route:

1. analyze and lock product identity/truth; **block finished generation if mandatory confirmed-input audit is not PASS**;
2. resolve category strategy and reference mapping;
3. lock product position/scale, camera/horizon/lens feeling, contact surface, light/shadow direction, environment color/reflection, and copy/headline/price/brand zones as one composition;
4. use native generation/edit or an identity-preserving reconstruction/composite route that produces one coherent product–scene system;
5. generate product, scene and commercial typography together whenever supported; verify exact copy and perform only localized deterministic correction where generated text fails;
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
