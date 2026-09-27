# Platform Technical Specifications

Technical specs are volatile. Treat this file as a structured cache, not timeless truth. Re-verify current official rules before `S2 PLATFORM_READY` when the rule is stale, incomplete, category-dependent, or account-dependent.

## Resolution schema
```yaml
platform:
surface:
output_type:
category:
account_feature_state:

hard_requirements:
  ratio:
  resolution:
  duration:
  file_size:
  format:
  count:

official_recommendations: {}
design_defaults: {}
content_constraints: {}
category_or_feature_overrides: {}
runtime_checks: []
source_metadata:
  source:
  last_verified:
  confidence: VERIFIED | PARTIALLY_VERIFIED | RUNTIME_REQUIRED | USER_CONFIRM_REQUIRED | DESIGN_DEFAULT
```

## Override order
General platform rule → surface rule → output-type rule → category/account override → latest verified rule.

## Known verified examples from current research
### Douyin e-commerce — product main video
- Duration: 5–60s
- Official recommendation: preferably ≤30s
- Format: MP4
- File size: ≤100MB
- Ratios supported: 1:1 / 3:4 / 9:16
- Resolution: ≥720p
- Re-verify before final production.

### JD — product main video
- Duration: 6–90s
- File size: ≤200MB
- Resolution: ≥720p
- Common supported ratios include 1:1 and 3:4
- Re-verify before final production.

### JD — detail video
- Duration: 5–180s
- File size: ≤500MB
- Resolution: ≥720p
- Re-verify before final production.

### Xiaohongshu — image note share interface
- Up to 18 images via documented share interface.
- Older SDK crop guidance includes supported ratio/crop constraints; do not present 3:4 as the only official required ratio.
- Use 3:4 only as a `DESIGN_DEFAULT` when appropriate.

### Taobao / Tmall
- Category-specific publishing rules exist; do not hardcode one universal detail-page width from community lore.
- Final upload width / slicing / file-size requirements may require runtime merchant-backend verification.

### Xianyu / Dewu
- Publicly accessible fixed numeric limits are incomplete in current research; use runtime verification before platform-ready delivery.

## Rule
Hard requirement, official recommendation, and internal design default must never be conflated.
