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

### 2. Skill packaging / invocation
How is the Skill discovered or invoked in this host?
When relevant, record:
- required Skill file/folder naming,
- frontmatter/manifest requirements,
- installation or registration location,
- reload/refresh requirements,
- invocation name or trigger semantics.

Do not copy host-specific packaging rules into the Core Skill unless they are truly portable.

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

### 4A. Workspace root / project-path mapping
The Core Skill uses **relative, host-neutral project paths**. The runtime adapter must resolve those paths against the actual workspace available in the current host.

Default logical project root:
`projects/<project-id>/`

The exact physical location may differ by host or user-selected workspace. Do not hard-code a particular product directory, operating-system drive, home directory, or Skill installation path into Core rules.

Keep these boundaries distinct where the host permits:
- Skill/configuration files,
- active-project files,
- sibling/archived projects,
- temporary runtime storage.

A new project should not inherit sibling-project files merely because the runtime can technically read them. Runtime capability defines what **can** be accessed; project source scope defines what **may be treated as current evidence**.

### 5. Script/code execution
Can local scripts run?
What languages/runtimes are available?
What filesystem/output restrictions apply?

### 6. External API access
Can the host call external APIs directly or only through connectors?
How are credentials/permissions handled?
Never assume API keys exist.

### 7. Tool / API binding
When the host must bind the Core Skill to a native tool, connector, MCP action, script, or API, describe the interface boundary explicitly:
- invocation/tool name,
- input schema and required fields,
- output/result schema,
- file/image/reference semantics,
- authentication and permission boundary,
- synchronous / asynchronous / pending behavior,
- timeout and retry behavior,
- idempotency / duplicate-execution risk,
- error states and fallback mapping.

The Core Skill should express the production/research requirement; the runtime adapter translates that requirement into host-specific calls. Do not hard-code host API syntax into design-method references.

### 8. Human Gates / authorization
How should spend, login, external upload, or consequential actions be surfaced and approved?

### 9. Artifact handling
What output types can be generated, saved, rendered, downloaded, or handed off?

### 10. State / persistence
Which project state survives turns/sessions?
Do not confuse runtime state with durable project truth.

### 11. Fallback
If a required capability is missing:
1. use an equivalent native/connected capability,
2. choose an alternate production route,
3. create a provider-ready manual handoff,
4. ask only when client-exclusive input is actually blocking.

### 12. Known limitations
Record only verified host-specific limitations that materially affect execution.

## Capability honesty
Do not infer capability from the host/product name. Inspect the actual tools/permissions available in the current session.

Runtime capability resolution is cross-cutting. Perform it before any tool-dependent research, file operation, production, external action, or verification step—not only during image production.

## Progressive disclosure
Load host-specific details only when they affect the current task.

## Host-specific files
Do not pre-create empty files for every AI product. Create a dedicated host file only when it contains real, stable differences from this common contract.

Potential hosts may include ChatGPT, Codex, Claude, Copilot, Cursor, Gemini, DeepSeek, Doubao, Kimi, Qwen, or others; this list is not a capability claim.


## Codex host adapter
When the active host is Codex, load `references/ai-tools/codex.md` for host-specific image-generation wait budgets, staged product-hero routing, and deterministic fallback behavior.
