# Provider Routing

## Separation of concerns
- **Production Router:** what method is needed? Generate / Edit / Composite / Layout / Video / Hybrid.
- **Capability Resolver:** what capabilities are currently available?
- **Provider Router:** which eligible provider/tool should execute the method?

## Selection factors
- Capability match
- Product fidelity
- Text fidelity
- Reference control
- Motion / temporal control
- Format support
- Automation
- Cost
- Latency
- Commercial/privacy constraints
- Current availability

Do not expose an arbitrary numeric score to the client.

## Execution modes
### E0 NATIVE EXECUTION
Current agent/runtime can execute directly.

### E1 CONNECTED EXECUTION
Use configured API / MCP / connector.

### E2 EXTERNAL CONFIRMED EXECUTION
External spend, credits, login, or third-party asset upload requires HG3 unless already authorized.

### E3 MANUAL HANDOFF
If automation is unavailable, export a provider-ready production pack.

## Provider-ready production pack
Include:
- target provider / production goal,
- output specification,
- product truth / identity lock,
- references and roles,
- visual thesis / campaign locks,
- negative direction,
- composition / shot plan,
- executable prompt/instructions,
- parameters / ratio / resolution / duration,
- typography and post-production plan,
- QA checklist.

## Least unnecessary dependency
Do not call an external provider merely because it exists. Prefer the simplest available route that satisfies the required quality, fidelity, and precision.
