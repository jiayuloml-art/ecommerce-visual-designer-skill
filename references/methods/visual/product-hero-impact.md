# Product Hero Visual Impact Protocol

## Purpose
Give **Hero A / Product Hero** stronger first-glance product presence and premium photographic energy while preserving product truth, physical grounding, product–scene relevance, typography contrast, brand identity and platform fit.

**Impact is not equal to brightness, oversized glow, chaotic motion or an arbitrarily huge product.** It comes from a specific product feature being made unmistakably desirable through camera, scale, silhouette, material, light and compositional tension. Applies when a single requested poster is explicitly product-focused, too. This protocol does **not** automatically impose the same dramatic art direction on Usage Hero.

## Product-first impact strategy (compile before rendering)
Start from real product assets, verified visible geometry and the primary purchase motivation. Choose the **one product-specific focal advantage** that must survive a 2-second glance: e.g. signature silhouette, craftsmanship, interface, form transition, material, precision or recognizable design detail.

Do not assume a camera angle can reveal unseen geometry. Identity-preserving pose/view reconstruction is allowed only within source evidence and Product Truth constraints. Never redesign the SKU or exaggerate an unverified property to make the image more dramatic.

Compile:
```yaml
product_hero_impact:
  core_product_focal_advantage: null
  visual_impact_mechanism: null # HEROIC_SCALE | SCULPTURAL_CAMERA | MATERIAL_MACRO | CONTROLLED_CHIAROSCURO | DEPTH_TENSION | BRAND_COLOR_CONTRAST | other justified route
  product_silhouette_read: null
  camera_angle_and_lens_logic: null
  product_frame_dominance_and_crop: null
  foreground_midground_background_depth: null
  material_and_highlight_plan: null
  scene_to_product_contrast_plan: null
  product_typography_counterweight: null
  hero_specific_background_relationship: null
  protected_identity_and_legibility_zones: []
  overstyling_risks_to_avoid: []
  thumbnail_and_two_second_target: null
  selected_direction_rationale: null
```

## Six product-hero impact levers
Use **at least two mutually reinforcing levers**, selected by category, product geometry and communication goal. Do not activate all six by default.

1. **Heroic scale and silhouette:** grant the product a clearly dominant visual mass without a rigid percentage. Consider deliberate near-camera prominence, proportionate negative space, decisive silhouette separation and selective editorial crop. Never obscure distinguishing functional parts, distort dimensions or cut essential product evidence.
2. **Camera and perspective:** choose an evidence-supported three-quarter, slightly lower, near/far perspective, elevated, or precise macro view to reveal unique form. Avoid lazy frontal catalog framing by default, but do not impose extreme wide-angle distortion or invent hidden/unverified surfaces. An intentional orthographic studio image can be equally powerful.
3. **Material-led cinematic light:** design key, fill, rim and reflection to reveal real curvature, texture, tactile detail, edge precision and construction. Metal, glass, fabric, plastic and ceramic require different specular/roughness behavior. Strong light contrast is permissible; fake glow, oversaturation, plastic-looking glossy surfaces and crushed details are not.
4. **Compositional energy:** use directional line, diagonal tension, asymmetrical balance, foreground/background depth, framing, product-to-copy counterweight, and restrained motion cues where truthful. The image should feel art-directed rather than a product centered on an arbitrary podium.
5. **Product–background resonance:** let environment structure, gradient, material planes and brand palette emphasize the signature product feature. Preserve physical shadows/contact and the separate Product–Scene Relationship Check. Background must reinforce product impact, not be the visual star.
6. **Detail and proof hierarchy:** spotlight one meaningful, verified distinctive design detail without cluttering with callouts, tiny split-frame closeups, fake cutaways or unsupported technical claims. When an inset is genuinely required, treat it as a deliberate part of the complete advertisement.

## Direction exploration — internal, not extra client deliverables
Internally compare **two or three distinct impact directions** suitable for this actual product, such as:
- Sculptural product camera + dramatic but physically credible edge light.
- Material macro/three-quarter emphasis + controlled refined backdrop.
- Bold brand-color contrast + deep editorial framing.

Select **one strongest direction** based on Product Truth, distinctiveness, commercial hierarchy, brand, background relation and text readability. Do not show three rough options to the client unless explicitly asked. Do not make the direction mechanically the same for every category.

## Category-specific strategy examples (illustrative, not templates)
- **Sports watch:** emphasize verified watch case, display, strap material and precision of form with an intentional three-quarter camera and light shaping; do not invent a new face/interface or rotate to an unsupported view.
- **Modular sofa:** express the real modular silhouette, cushion volume, textile texture and spacious physical mass with convincing architectural perspective and daylight/shadow; do not shrink furniture into a tiny floating 'product render'.
- **Aroma humidifier:** use the actual silhouette, material translucency and honest light/surface interaction, emphasizing the tactile/object relationship; do not add unverified vapor intensity, rainbow light or magical effects.

## Constraints and negative prompts
Reject:
- generic product-front shot with timid visual mass, excessive dead space and no focal feature;
- obligatory centered podium, floating product, neon particles, sci-fi beams, fake splash/fire or fake speed trails;
- extremely wide lens distortion, broken product silhouette, fabricated ports/displays/materials, false transparent cutaways;
- cluttered props/models that steal the focus or become the first read;
- strong color cast that changes verified product color, over-sharpened plastic reflections, crushed blacks and unreadable real features;
- dramatic typography that overwhelms or collides with the product, low-contrast text, or unplanned copy placement.

A subtle/minimal product hero can PASS if its silhouette, material, framing and contrast create **clear editorial impact**. 'More visual impact' must not automatically mean 'more complicated.'

## Independent Product Hero Impact Check
Judge the **rendered Product Hero**, not the prompt or producer narrative. Score 1–10:
1. **Product Focal Dominance:** instant and recognizable primary product read at intended viewing size.
2. **Camera / Silhouette Expressiveness:** angle, perspective and crop highlight verified distinctive form.
3. **Material / Lighting Quality:** real material feels tactile and premium, highlights and shadows serve shape.
4. **Compositional Energy:** deliberate tension, depth, balance and background guidance make the ad memorable without noise.
5. **Commercial Impact / Brand Fit:** desire/benefit/message registers within 2 seconds while exact product, copy and identity remain trustworthy.

**Hard gate for Product Hero:** every field >=7/10 AND total >=40/50. Any FAIL or NOT_CHECKED blocks Product Hero delivery. This is independent of Product Truth, Product–Background Fusion, Product–Scene Relationship, Typography Prominence/Contrast, technical and platform checks; no aesthetic score can compensate for a hard truth/compliance failure.

Repair should target the weak lever: product too small -> visual mass/crop/layout; weak silhouette -> evidence-supported camera; flat light -> shape/material-specific lighting; noisy composition -> background/props/depth; low benefit clarity -> focal advantage and copy relationship. Re-render or local edit and re-inspect actual output.

## Regression scenarios
1. 'NOVA 运动手表，设计商品主视觉' (no count) -> retain TWO complete posters; Product Hero passes visual impact with verified case/material emphasis; Usage Hero still demonstrates genuine worn use.
2. 'MORA 模块化沙发，设计成品海报' -> Product Hero emphasizes physical volume, fabric and spatial presence; Usage Hero remains active and credible.
3. 'AERIS 香氛加湿器，只做一张 4:5 产品型成品海报' -> exactly ONE complete Product Hero with stronger silhouette/light/scene fit, no invented functionality.
4. Minimal studio setting -> allow bold product silhouette and nuanced editorial light without forced spectacle.

Perform rule-level checks for routing, fields and gates; **do not report real image quality as tested** until live model outputs have been generated and assessed.
