# Direct Final Poster Generation

Purpose: generate a complete, campaign-ready e-commerce poster as one commercial composition instead of generating an empty mood background or isolated hero image first and assembling the sales poster afterward.

Use this as the default production protocol for explicit static `成品海报 / 电商促销海报 / 商品促销海报 / final poster` outputs and for any other output contract explicitly classified as a finished poster. Use staged anchor/background workflows only when the client explicitly requests staged direction approval or when a documented technical limitation makes direct integrated production impossible.

## Output-route boundary

Direct Final Poster Generation applies to BOTH main-visual/hero requests and final/promotional poster requests. Without an explicit quantity, produce TWO individually complete finished posters:
- Hero A / Product Hero: complete product-focused poster with legible headline, brand and applicable confirmed copy.
- Hero B / active Usage Hero: complete usage-focused poster with real actor/product interaction, legible headline, brand and applicable confirmed copy.

Use a shared Campaign Visual System but distinct camera, composition, scene function and evidence. An explicit quantity overrides two; never infer quantity from 4:5 or other aspect ratios.

## Required sequence

**PRODUCT ANALYSIS → CATEGORY VISUAL STRATEGY → REFERENCE EXTRACTION → TWO COMPLETE POSTER COMPOSITION PLANS → PRODUCT–SCENE–TEXT INTEGRATED GENERATION → VERIFY EXACT COPY → CONDITIONAL MINIMAL TEXT REPAIR → INDIVIDUAL + PAIR QA**

Do not output an empty background, pure mood image, isolated visual draft, or separate hero layer as the default intermediate client deliverable.

## Final-poster contract

Every poster must resolve in one frame:
- product subject,
- background/environment,
- core-copy zone,
- selling-point information zone,
- brand zone,
- campaign/price/date/CTA zone when applicable,
- commercial composition,
- complete visual hierarchy.

The generated visual base must already behave like an **integrated ecommerce poster** with **product embedded in environment**, **scene-aware product placement**, **commercial composition**, **poster-ready layout**, **copy-safe negative space**, **hero product dominance**, **retail advertising**, **campaign-ready key visual**, and **premium ecommerce finish**.

**Default to one-pass finished typography inside the scene**: headline, supplied offer/price/date, selling points and brand are designed and rendered jointly with product/environment/usage wherever the active tool can do so. Plan exact wording, zones, contrast fields, scale, color, hierarchy and product relationship before generation. Verify the rendered text. Only when exact wording fails may a deterministic repair replace the affected glyphs in the existing planned zone; do not routinely generate a text-free plate and overlay all copy later.

## Unified composition lock

Before each poster is generated, lock all of the following as one composition:

```yaml
product_position:
product_scale:
camera_angle:
horizon:
contact_surface:
light_direction:
shadow_direction:
environment_color:
product_reflection:
copy_zone:
headline_zone:
price_zone:
brand_zone:
```

Also resolve lens/focal-length feeling, depth-of-field behavior, foreground/midground/background, natural occlusion, intended product–environment interaction, and exact commercial hierarchy.

No field may be planned as an independent layer that contradicts the others. Product, environment, lighting, camera, contact surface, copy zones, and commercial hierarchy must form one scene.

## Typography spatial preflight

Before generation, compile the Typography Prominence Contract from `composition-and-typography.md` and bind it to the unified composition. Resolve:

- headline contrast field,
- price/primary-offer field,
- brand field,
- controlled negative space,
- local background complexity behind each important role,
- headline scale/weight/line structure,
- headline–product relationship,
- thumbnail reading order.

Record:

```yaml
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

Execute in fixed order: lock headline/price/selling-point zones → judge local complexity and tone → choose text color → set headline size/weight → create the contrast field → add only a lightweight enhancement if still necessary → inspect at 100%, 50%, 25%, and run the 2-Second Read Test.

The provider brief must cause the scene itself to reserve low-complexity, contrast-capable copy regions. Do not wait for the image to finish and then search for empty pixels. If a field cannot support the intended type without opaque rescue cards, revise scene composition/light/detail before commercial-info composite.

When the local background is a middle tone, do not accept weak light-gray or thin dark-gray typography. Move the local field decisively lighter or darker, simplify it, and choose an opposing text tone/weight. The title, promotional price, and core selling points must remain visually distinct from the background at thumbnail scale.

## Product–scene integration plan

Prioritize:
- physically grounded product,
- realistic contact shadow,
- matched perspective,
- matched camera angle,
- matched focal length,
- environmental lighting continuity,
- color temperature consistency,
- ambient light spill,
- surface reflection,
- material response,
- natural occlusion,
- depth integration,
- foreground–background interaction,
- realistic product grounding,
- non-collage look,
- non-cutout look,
- non-pasted product,
- single-scene coherence.

Enforce:
1. The product must not read as a later overlay.
2. Product and environment must share one lighting system.
3. The product must have credible weight-bearing contact and contact shadow.
4. Product material must receive environmental reflection, bounce light, and color temperature.
5. Product perspective and lens feeling must match the scene.
6. Product scale must be plausible for the environment and nearby cues.
7. A held, worn, or operated product must show credible occlusion, grip/pressure, deformation, support, and force relationships.
8. Product edges must not show extraction halos or cutout contours.
9. Product and background must not read as separately rendered images.
10. The complete frame must read as one commercial photograph or high-quality commercial composite.

When exact source pixels cannot satisfy camera, lighting, contact, occlusion, or material-response requirements, prefer an identity-preserving edit/reconstruction route when product evidence supports it. Do not preserve source pixels at the cost of obvious pasted-on integration. Product truth remains non-negotiable.

## Prompt/production vocabulary

Use the following concepts when relevant; translate them into concrete camera, light, surface, material, layout, and interaction instructions rather than dumping keywords without structure:

`integrated ecommerce poster`, `product embedded in environment`, `scene-aware product placement`, `physically grounded product`, `realistic contact shadow`, `matched perspective`, `matched camera angle`, `matched focal length`, `environmental lighting continuity`, `color temperature consistency`, `ambient light spill`, `surface reflection`, `material response`, `natural occlusion`, `depth integration`, `foreground-background interaction`, `realistic product grounding`, `commercial composition`, `poster-ready layout`, `copy-safe negative space`, `hero product dominance`, `high visual hierarchy`, `retail advertising`, `campaign-ready key visual`, `premium ecommerce finish`, `strong commercial typography`, `poster-scale type`, `high local text contrast`, `headline-product counterbalance`, `clear offer hierarchy`, `mobile-readable headline`, `thumbnail-readable commercial message`, `non-collage look`, `non-cutout look`, `non-pasted product`, `single-scene coherence`.

Translate typography vocabulary into concrete scale, position, weight, negative space, light, local background complexity, and product relationship. Do not dump keywords into prompts.

## Hard negative constraints

Include applicable negatives in every provider prompt or production brief:

- avoid pasted-on product
- avoid floating product
- avoid disconnected background
- avoid mismatched lighting
- avoid mismatched shadows
- avoid wrong perspective
- avoid fake reflections
- avoid cutout edges
- avoid collage appearance
- avoid separate product/background rendering
- avoid generic decorative scenery
- avoid background overpowering product
- avoid cinematic scene with weak ecommerce readability
- avoid empty mood image without selling information
- avoid tiny or weak headline
- avoid low-contrast or washed-out typography
- avoid thin type on complex background
- avoid equal-size information hierarchy
- avoid metadata-like or micro typography
- avoid headline in leftover space
- avoid product-only visual dominance
- avoid shrinking type to fit
- avoid disconnected typography
- avoid generic UI-card typography or unnecessary translucent text panels
- avoid white type on high-key highlights
- avoid dark type sinking into dark or middle-tone fields
- avoid headline/background colors with weak separation
- avoid fine/light headline weight
- avoid headline and supporting copy at nearly equal scale
- avoid price styled like date, CTA, or metadata
- avoid complex detail behind headline, price, or core selling points
- avoid technically present but commercially invisible copy
- avoid cheap text boxes, PPT-style slabs, social-media stickers, or large scene-obscuring panels

## Human interaction

When people are present, plan contact before generation:
- hand path and finger occlusion,
- grip or support point,
- pressure/deformation,
- body/product overlap order,
- gaze/action relevance,
- product scale relative to anatomy,
- cast/contact shadow and reflected light across both person and product.

A person standing near a product is not usage evidence. A hand touching the outline without wrapping, pressure, or correct depth is not credible contact.

## Typography and commercial information

Render the full scene, product, usage action, headline, brand and any verified promotion copy **together** whenever supported. Then:
1. verify every exact required string, punctuation, number, brand mark and claim against source data; do not invent prices or promotional dates;
2. if image-generated glyphs fail, use the smallest localized deterministic text correction in its planned contrast field, keeping camera, scene, type scale and spatial relation fixed;
3. preserve the preplanned zones and reading order, including the product + headline dual core;
4. verify that text does not obscure product interaction or integration evidence;
5. verify full-view, 50%, and 25% readability and run the 2-Second Read Test;
6. do not use opaque cards, fog, glow, or cropping to hide failed product–scene integration or an unresolved contrast field.

Typography Contrast fails closed when the headline is not obvious at first glance, requires zooming, is too light/small relative to supporting copy, is swallowed by texture/highlight/shadow, or when price/core selling points lack commercial presence. Repair the planned contrast field or typographic hierarchy; do not rationalize the result as subtle or premium.

## Product–Background Fusion Score

Score each field from 1–10 on the rendered poster:

| Field | Question |
|---|---|
| Perspective | Do product geometry, horizon, vanishing direction, and lens feeling match the scene? |
| Lighting | Do key/fill/rim direction, exposure, softness, and ambient spill form one system? |
| Shadow | Are contact and cast shadows directionally and physically credible? |
| Reflection | Does the product receive plausible environmental reflections/bounce without fake gloss? |
| Scale | Is product size believable relative to the environment and use context? |
| Occlusion | Are foreground overlap, hand/body contact, and depth order natural where applicable? |
| Material response | Do fabric, metal, plastic, glass, skin, etc. respond correctly to the environment? |
| Color temperature | Do product and environment share a coherent temperature while retaining identity? |
| Contact realism | Does the product show weight, support, grip, pressure, or containment rather than floating? |
| Overall scene coherence | Does the frame read as one photograph/commercial composite rather than assembled layers? |

Hard gate:
- any field below **7/10** → FAIL; regenerate or repair the responsible integration layer;
- total below **80/100** → FAIL; regenerate or structurally revise;
- only a score with every field ≥7 and total ≥80 may proceed to delivery, subject to Product Truth, Technical, Compliance, Copy, and Visual Critic gates.

Record the ten field scores and total in project/artifact state. Do not replace visible inspection with a self-reported prompt claim.

## Final standard

The first impression must be:

**real commercial photography / high-quality commercial compositing completed as an e-commerce advertisement**

not:

**product PNG placed on an attractive AI background**

Require:

**ONE SCENE · ONE LIGHTING SYSTEM · ONE CAMERA SYSTEM · ONE PRODUCT–TYPOGRAPHY COMPOSITION · TWO COMPLETE FINAL POSTERS BY DEFAULT**
