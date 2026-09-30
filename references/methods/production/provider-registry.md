# Provider Registry

Provider capabilities change quickly. Re-check current access, pricing, and API status when execution depends on them.

This registry describes **production providers/tools**, not the AI host/runtime in which the Skill is running. Host/runtime behavior belongs in `references/ai-tools/runtime-adapters.md`.

## Provider profile schema
- Provider
- Capability
- Access mode: Native / API / MCP / Browser / Manual
- Supports: generate / edit / reference / composite / typography / vector / video / upscale / etc.
- Strengths
- Weaknesses
- Best for
- Avoid for
- Fidelity characteristics
- Control level
- Cost model
- Authentication
- Automation status
- External asset upload implications
- Current availability
- Last checked

## Candidate roles
### General image generation
Host-native/OpenAI Image, Adobe Firefly, FLUX, Stability.

### Product-preserving image edit
Host-native image edit, Adobe Firefly, Stability, Ideogram, FLUX.

### Graphic / typography / vector
Ideogram, Recraft.

### Video
Runway, Luma, Veo/Vertex AI, Sora/API depending current access.

### Deterministic layout
Figma, HTML/CSS/SVG or equivalent local renderer.

### Utility / post-production
Upscale, background removal, reframe, vectorize, localization; choose based on currently connected capability.

## Rule
Do not bind the Skill architecture to one provider. Maintain provider metadata separately from design logic and separately from host/runtime adaptation.
