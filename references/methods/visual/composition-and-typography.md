# Composition and Typography Grammar

Purpose: translate an approved Visual Direction into a deliberate frame and text system.

This module answers:
- **how is attention organized?**
- **how do product, scene, effect, and copy form one composition?**

It is a grammar, not a template library.

## Output: Composition Contract

For a static e-commerce poster, complete this contract before any image generation. Treat the following as one indivisible composition:

- `PRODUCT POSITION`
- `PRODUCT SCALE`
- `CAMERA ANGLE`
- `HORIZON`
- `CONTACT SURFACE`
- `LIGHT DIRECTION`
- `SHADOW DIRECTION`
- `ENVIRONMENT COLOR`
- `PRODUCT REFLECTION`
- `COPY ZONE`
- `HEADLINE ZONE`
- `PRICE ZONE`
- `BRAND ZONE`

Also resolve focal-length feeling, product/environment depth, natural occlusion, foreground/background interaction, and the complete commercial reading order. If any field is deferred as an unrelated later layer, the contract is incomplete.

### Commercial hierarchy

For a normal brand/new-product hero, treat **PRODUCT + PRIMARY HEADLINE / CORE BENEFIT** as a dual commercial core. Default reading order:

1. PRODUCT
2. PRIMARY HEADLINE / CORE BENEFIT
3. PRICE / PRIMARY OFFER when promotion-led
4. BRAND / PRODUCT NAME
5. KEY SELLING POINTS
6. DATE / CTA
7. SECONDARY / LEGAL INFORMATION
8. ENVIRONMENT / DECORATION

Adjust only when the approved communication job gives a concrete reason. At thumbnail size, product + core benefit must remain the intended first read. If background, model, architecture, prop, or effect dominates unintentionally, `COMMERCIAL_HIERARCHY_QA = FAIL`.

### First focal structure
Choose the mechanism that creates the first focal event, for example:
- dominance,
- scale contrast,
- crop,
- isolation,
- depth,
- light focus,
- framing,
- overlap,
- repetition,
- directional flow.

Use only mechanisms that support the Visual Thesis.

### Product-first background relationship
Before fixing foreground/midground/background and text zones, apply `product-scene-relationship.md`: identify product-derived scene meaning, visual correspondence, use/context, space/attention structure, brand relevance and the background-swap diagnostic. Plan product, background and copy as one composition. Preserve thumbnail product dominance and readable contrast.

### Relationship map
Define the spatial/attention relationship among the elements that actually matter:
- PRODUCT ↔ COPY
- PRODUCT ↔ SCENE
- PRODUCT ↔ EFFECT
- PRODUCT ↔ PROOF
- PRODUCT ↔ BRAND

Avoid defaulting to "left text / right product", centered product, or a fixed grid unless that relationship is deliberately justified.

### Product participation
Define the product's active participation in the frame.

Use a relational statement, not only a coordinate:
- “hand enters from the lower edge and grips the bottle,”
- “bottle is seated in a cup holder that provides scale and foreground occlusion,”
- “product is partially cropped in the foreground while the use environment recedes behind it,”
- “product leans against a verified scene object and creates a diagonal counterforce to the headline.”

When people are present, specify the action and contact point. A model standing near the product without a communication role is not meaningful interaction.

When no person is present, the product may still interact through support, containment, overlap, occlusion, reflection, crop, scale contrast, or directional effect.

Across a coordinated set, do not let product presentation collapse into repeated front-view / upright / full-outline placement by default. Repetition is acceptable only when it serves a deliberate campaign system.

When evidence permits, vary participation through:
- crop / partial entry,
- foreground occlusion,
- containment in a bag / holder / storage context,
- support / leaning / resting relation,
- different verified view selection,
- credible tilt / orientation,
- human/object contact,
- foreground–midground–background placement.

Do not force dynamic posing when product evidence does not support it. In that case, keep the verified view and make the **scene adapt to the product** rather than inventing geometry.

### Composition tension
Identify what prevents the frame from becoming a passive placement of assets.

Useful tensions may include:
- large product × large negative space,
- visual mass × typographic counterweight,
- static object × directional effect,
- foreground crop × background depth,
- symmetry × controlled asymmetry,
- dense detail × quiet field.

If the composition can be described only as "product + text + background", it is not sufficiently resolved for a hero/KV.

### Depth and framing
Plan foreground/midground/background, overlap, occlusion, crop, and framing only when they improve focus, realism, or meaning.

### Copy-zone contract

Reserve copy space before scene generation or composition assembly. Define:
- `TEXT_SAFE_AREA`,
- `HEADLINE_ZONE`,
- `PRODUCT_SILHOUETTE_ZONE`,
- `NEGATIVE_SPACE`,
- `LOGO_AREA`,
- `CTA_SUPPORTING_COPY_AREA` when applicable.

The integrated poster brief must preserve these zones. Do not generate an empty background for a later product overlay, and do not generate a fully occupied image and then force text over product, faces, hands, functional interaction, or high-detail contrast.

Headline and product should form one visual system through counterweight, framing, overlap, directional flow, scale, or another justified relationship. Typography is not a late overlay even when deterministic rendering occurs in post-production.

### Copy roles
Do not assume every role must appear, but classify every text element that does.

- **IDENTITY** — brand/product identification.
- **HOOK** — first-impression communication.
- **SUPPORT** — helps interpret the hook.
- **PROOF** — verified evidence, parameter, trust point, or offer.

**Strategy keywords are not consumer-facing copy.**

Internal labels such as:
> bedroom / desk / renter / small-space

must not be placed into the visual unless they have been rewritten into intentional customer-facing language.

### Typography as composition
Typography must participate in the frame rather than occupy leftover empty space. Prefer rendering typography jointly with product/scene in a complete poster. Plan copy zones, contrast fields, scale and reading order before generation. Verify exact strings; apply localized deterministic correction only when the model-rendered text fails, rather than default background-first separate text assembly.

Resolve as applicable:
- scale,
- weight,
- line break,
- rhythm,
- tracking,
- alignment,
- contrast,
- overlap,
- negative space,
- relationship to product/effect,
- reading order at the intended viewing size.

For commercial layers such as price / offer / date / CTA, check the relationship among label, number, currency symbol, qualifier, and surrounding background instead of treating each as an isolated text box.

Avoid:
- low-contrast brand-color text on a similar brand-color field,
- labels touching or visually colliding with large price numerals,
- mechanically inconsistent spacing between similar text roles,
- arbitrary size changes that are not tied to hierarchy,
- atmospheric photography paired with typography that feels pasted on top rather than integrated into the composition.

Bold text alone is not typography design.

## Typography Prominence Contract

For every commercial poster, compile this before scene generation:

```yaml
typography_prominence:
  primary_message:
  headline_role:
  headline_scale:
  headline_weight:
  headline_lines:
  headline_alignment:
  headline_contrast_strategy:
  headline_product_relationship:
  price_role:
  price_scale:
  price_contrast_strategy:
  supporting_copy_scale:
  supporting_copy_density:
  brand_scale:
  brand_position:
  local_background_complexity:
  text_contrast_field:
  thumbnail_reading_order:
```

Also compile the explicit contrast decisions used by the production plan:

```yaml
typography_contrast:
  headline_text_color:
  headline_size_strategy:
  headline_weight_strategy:
  headline_background_relation:
  price_contrast_strategy:
  selling_point_contrast_strategy:
  local_background_complexity:
  contrast_field_method:
  fallback_enhancement:
```

The headline must act as a commercial visual element, not body copy. Establish prominence through at least two mechanisms such as scale, weight, tonal contrast, spatial isolation, negative space, alignment, product counterweight, crop/overlap, directional flow, asymmetry, or block structure. Bold weight alone is insufficient.

### Headline scale ratio

Use relative visual scale, not fixed platform pixels. Default relationship:

| Role | Relative scale |
|---|---:|
| PRIMARY HEADLINE | 1.00 |
| PRICE / PRIMARY OFFER | 0.70–1.20, according to promotional priority |
| PRODUCT / MODEL NAME | 0.40–0.60 |
| KEY SELLING POINT | 0.30–0.45 |
| DATE / CTA | 0.25–0.40 |
| LEGAL / SECONDARY | 0.16–0.25 |

Adapt for language, copy length, brand, platform, aspect ratio, references, and product form while preserving obvious hierarchy. `headline ≈ supporting copy ≈ date` fails. If the primary message is the communication job, headline plus surrounding negative space must remain one of the frame's major visual regions. Minimal does not mean tiny; premium does not mean weak information.

### Text Contrast Field

Plan a local environmental field for every important text role before generation. Create readability through calmer local background, controlled negative space, tonal separation, reduced texture/object density, directional light, or subtle atmospheric falloff.

If a headline is planned upper-left, suppress high-frequency texture, strong highlights, complex foliage, faces, and product-critical structures there. Preserve sufficient local luminance separation for the intended weight and color. Use composition, light, scale, and weight before adding cards. Translucent panels, dark/white rectangles, pills, or glass UI are allowed only when brand/reference/platform strategy supports them; they are not the default readability repair.

A `contrast field` is a text-bearing region intentionally made readable as part of scene design before generation. It is not a text box added afterward. Build it through one or more of:
- reduced local detail or texture frequency,
- negative space reserved around the text silhouette,
- removal/relocation of strong highlights and hard shadow boundaries,
- avoidance of faces, hands, active product contact, and product-critical structures,
- controlled local brightening/darkening,
- a soft directional or tonal gradient continuous with environmental light,
- restrained depth/atmospheric separation that remains physically coherent with the scene.

Neutral midtone backgrounds are not automatically safe. When neither light nor dark text separates decisively from the local field, actively move the field lighter or darker, simplify it, and choose the opposing text tone. Do not accept tasteful-looking low contrast as “premium.”

### Typography Contrast execution order

Execute in this order for every typography-bearing poster:

1. Lock `HEADLINE ZONE`, `PRICE ZONE`, and `SELLING-POINT ZONE`.
2. Judge local background complexity, luminance range, highlight/shadow transitions, and interference risk in each zone.
3. Select text color from the actual local background relation; never choose it from brand palette alone.
4. Set headline visual size and weight so it is unmistakably larger/stronger than supporting copy.
5. Build a pre-generation contrast field using scene detail, negative space, tonal control, or a subtle environmental gradient.
6. If visibility is still insufficient, add the lightest justified enhancement: restrained shadow, soft backing, local glow suppression, or localized gradient. Do not introduce cheap text boxes, PPT-style slabs, social-media stickers, or large scene-obscuring panels.
7. Inspect at 100%, 50%, and 25%, then run the 2-Second Read Test. Repair the responsible scene/type variable before delivery.

Use color contrast, size contrast, weight contrast, local whitespace, background simplification, local light/dark control, and low-complexity placement together. A single weak mechanism is not enough for a primary headline or promotional price.

### Typography Contrast Hard Fail

Fail and revise when any applicable condition is visible:
- headline color is too close to its local background,
- the headline exists but is not obvious at first glance,
- the headline requires enlargement/zoom to read clearly,
- headline weight is too light,
- headline size is insufficiently different from supporting information,
- white text sits on a highlight and appears washed out,
- dark text sinks into a dark local field,
- a complex background swallows the headline,
- promotional price/offer lacks its own visual priority,
- the product is prominent but copy fails to become the second visual center,
- copy is technically present but lacks commercial visual presence.

These are direct failures even when the type is technically legible at full resolution.

### Copy-to-product relationship

Set `headline_product_relationship` to at least one explicit mechanism:

- **Counterweight** — product and headline balance visual mass.
- **Framing** — type and scene boundaries frame the product.
- **Alignment** — type baselines/edges align with product structure.
- **Direction** — reading flow leads toward the product.
- **Scale tension** — large product × large headline.
- **Controlled overlap** — depth is created without hiding product evidence.
- **Negative-space pairing** — product placement deliberately yields a copy field.

Do not leave this field blank or place type only where space happens to remain.

### Offer hierarchy

For price, discount, launch, limited-time, coupon, date, or CTA, identify the `PRIMARY COMMERCIAL TRIGGER`. A primary price must not share the same visual weight as its date or qualifier. Typical order: primary price/offer → campaign label → date → CTA. Do not compress all promotion information into one small row.

For promotion-led work, treat price/offer as an independent contrast target. Give it a distinct size, weight, color/tonal relation, spatial isolation, or typographic structure from date, selling points, and CTA. A price that visually merges with metadata is a hard failure.

### Selling-point and density control

Separate `PRIMARY BENEFIT` from `SECONDARY PROOF`. Promote the primary benefit into headline language when appropriate; keep secondary proof to 2–4 concise items. Classify the poster as `LOW`, `MEDIUM`, or `HIGH` copy density before production; hero/KV work defaults to LOW–MEDIUM.

`COPY OVERFLOW ≠ SHRINK FONT`. Repair overflow in this order: remove low-value copy → shorten copy → regroup → change line breaks → revise composition → add justified space → only then reduce type slightly. Never keep shrinking until everything fits.

Typography personality follows Category Visual Intelligence; visibility does not. Smart-home, digital, beauty, food, sport, fashion, eco, maternal, and pet categories may use different type character, but every primary message must remain clear, prominent, commercial, and readable.

### Typography negative constraints

Avoid tiny/weak headlines, low-contrast or washed-out text, thin type over complex backgrounds, equal-size information hierarchy, metadata-like copy, micro typography, accidental placement, headlines in leftover space, product-only dominance, excessive supporting copy, shrinking type to fit, disconnected typography, illegible promotion information, generic UI-card typography, and unnecessary translucent text panels.

### Identification requirement
For a standalone e-commerce hero/KV, the viewer should normally be able to identify what product is being shown from the artifact and its immediate context. Product/model identification may be quiet or prominent depending on brand/strategy, but it must not become unintentionally illegible.

### Exact text
Brand names, model names, prices, offers, parameters, CTA, certification/legal copy and other exact strings must be source-verified. Prefer integrated generation of product, scene and text when supported; use localized deterministic correction only for incorrectly rendered exact strings. Never invent prices, dates, claims or QR codes.

### Anti-template rules
Avoid unless specifically justified:
- decorative translucent pills/cards,
- tiny gray model labels by default,
- metadata-like keyword rows,
- generic centered/left-column stacking,
- equal visual weight for all copy,
- decorative lines with no compositional role,
- information added merely because it is confirmed.

## Reference transfer checkpoint

When benchmarking was required, the Composition Contract must identify which observed reference mechanism materially informed at least one concrete choice in the frame.

Acceptable transfer targets include:
- product placement / crop / angle,
- product–scene or human interaction,
- depth / overlap / occlusion,
- headline scale / line break / alignment / product relationship,
- color / light / material treatment,
- graphic / semantic effect,
- negative-space or visual-path behavior.

If the layout was already fixed and the reference is being used only to justify it afterward, this checkpoint fails.

## Composition checkpoint

Before production:
- the first/second read is intentional,
- product and copy have a designed relationship,
- product participation is explicit when a scene is used,
- at least one composition mechanism creates focus/tension,
- benchmark-derived choices are traceable when benchmarking was required,
- text roles are clear,
- nonessential copy is removed,
- the composition still supports the Visual Thesis at thumbnail/mobile scale.
- the Typography Prominence Contract is complete and uses at least two headline-prominence mechanisms,
- the Typography Contrast sequence has been executed in order and all contrast fields are defined before generation,
- headline, offer, brand, and supporting copy each have a viable local contrast field,
- headline–product relationship is explicit rather than incidental,
- copy density and overflow handling preserve commercial scale,
- the product remains the first commercial subject at thumbnail size,
- copy zones were reserved before production and do not damage product silhouette or interaction evidence,
- a main-visual request with no explicit single-image instruction resolves to Hero A / Product Hero plus Hero B / active Usage Hero,
- Hero A and Hero B use meaningfully different composition backbones, cameras, scene functions, and evidence routes while sharing the Campaign Visual System,
- all thirteen unified composition fields are resolved as one camera/light/commercial system,
- the planned base is a complete integrated poster visual rather than a pure background or isolated product layer.

If this checkpoint fails, revise composition before generating/assembling the anchor.
