# Layout and Typography

## Exact commercial text
Prefer deterministic production for:
- brand names and logos,
- product model names,
- price and promotions,
- parameters,
- CTA,
- certification / legal copy,
- QR codes,
- precise product labels.

Image models may generate atmosphere, lettering concepts, or text-free layouts, but uncontrolled text generation is not a reliable source of final commercial copy when exactness matters.

## Text rendering ownership
Assign one mode for each text-critical output/slot:

- **DETERMINISTIC_LAYOUT** — exact copy is placed by a deterministic layout/composition system.
- **MODEL_RENDERED_AND_VERIFIED** — model rendering is acceptable only when the final rendered text is explicitly verified.
- **NO_TEXT** — the visual intentionally contains no in-image text.

Default exact commercial text to DETERMINISTIC_LAYOUT.

## Layout-first use cases
- promotional banners,
- price/offer modules,
- infographics,
- parameter cards,
- comparison tables,
- detail-page information modules,
- platform-safe CTA components.

## Layout QA
Check:
- exact copy,
- canvas size,
- overflow,
- text overflow,
- missing fonts/assets,
- safe-zone violations,
- collisions,
- alignment,
- thumbnail/readability at actual viewing scale.


## Hero typography craft
Deterministic text placement guarantees accuracy, not design quality. For hero/KV work, resolve typography as a visual system rather than a text dump.

Check:
- headline dominance and readable scale at the intended viewing condition,
- purposeful line breaks and phrase grouping,
- contrast against the underlying image,
- hierarchy among headline, product/model, proof, and secondary messages,
- spacing/rhythm between text groups,
- alignment or counterbalance with the product focal subject,
- whether pills/cards/labels are necessary or merely default UI-like decoration,
- whether the text block creates a distinct visual relationship with the product instead of occupying leftover empty space.

Avoid:
- stacking all confirmed facts into the hero,
- multiple low-contrast translucent text boxes over a detailed scene,
- tiny model names or proof copy that disappear at thumbnail scale,
- default centered/left-column templates with no art-direction role,
- using deterministic layout as a reason to skip typography craft.

For a hero anchor, the copy should usually be reduced to the minimum message set needed for the first impression; additional proof belongs in supporting slots unless the approved strategy requires otherwise.
