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
