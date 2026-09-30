# Runtime Adapters

This layer adapts the same core Skill to different AI hosts/runtimes without rewriting design logic.

## Core separation
- **Core Skill:** what the design process should decide and verify.
- **Host Runtime Adapter:** what the current AI environment can actually execute and how state/tools/approvals are represented.
- **Production Provider Adapter:** which downstream provider/tool performs image, video, layout, editing, or other production.

**Host Runtime ≠ Production Provider.**

## Runtime Adapter Contract
For the active host/session, resolve only what is relevant:

### 1. Host identity
What AI host/runtime is executing the Skill?

### 2. Invocation
How is the Skill discovered or invoked in this host?

### 3. Native capabilities
Does the current runtime support:
- image generation/editing,
- code execution,
- shell/local scripts,
- browser/web research,
- files/artifact creation,
- connectors/plugins/MCP,
- structured UI/approval surfaces?

### 4. File access
What files can be read/written?
What path/reference model applies?
What persistence exists?

### 5. Script/code execution
Can local scripts run?
What languages/runtimes are available?
What filesystem/output restrictions apply?

### 6. External API access
Can the host call external APIs directly or only through connectors?
How are credentials/permissions handled?
Never assume API keys exist.

### 7. Human Gates / authorization
How should spend, login, external upload, or consequential actions be surfaced and approved?

### 8. Artifact handling
What output types can be generated, saved, rendered, downloaded, or handed off?

### 9. State / persistence
Which project state survives turns/sessions?
Do not confuse runtime state with durable project truth.

### 10. Fallback
If a required capability is missing:
1. use an equivalent native/connected capability,
2. choose an alternate production route,
3. create a provider-ready manual handoff,
4. ask only when client-exclusive input is actually blocking.

### 11. Known limitations
Record only verified host-specific limitations that materially affect execution.

## Capability honesty
Do not infer capability from the host/product name. Inspect the actual tools/permissions available in the current session.

## Progressive disclosure
Load host-specific details only when they affect the current task.

## Host-specific files
Do not pre-create empty files for every AI product. Create a dedicated host file only when it contains real, stable differences from this common contract.

Potential hosts may include ChatGPT, Codex, Claude, Copilot, Cursor, Gemini, DeepSeek, Doubao, Kimi, Qwen, or others; this list is not a capability claim.
