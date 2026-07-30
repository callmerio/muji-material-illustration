# QA Checklist

Run this before delivering final images.

## Universal

- The image answers the user's actual content need, not merely the production method.
- The composition improves weak source screenshots into a clear, readable visual.
- The whole subject fits; no important text, label, icon, object, or axis is cropped.
- Text is readable at the intended display size.
- The image uses clean warm kraft paper with only subtle fiber/grain variation; no stains, folds, tears, or overdone vintage distressing.
- The image does not contain MUJI or another brand name, logo, watermark, copied packaging, store signage, or proprietary typography.
- The style is consistent with the Japanese minimalist kraft-paper lifestyle instruction-card system.
- The dominant print is dark brown-red or muted brick red, with at most a small amount of charcoal and no unrelated vivid color.
- Graphics are fine, even, clear two-dimensional hand-drawn linework with a front-facing flat composition.
- There is no photorealism, 3D rendering, real depth of field, perspective lens effect, thick shadow, exaggerated cartoon style, or children's picture-book treatment.
- Negative constraints in the prompt protect the main risk: wrong data, clutter, wrong tone, unsupported facts, or cropped labels.

## Labels And Explainers

- Labels are short, upright, legible, and attached to the correct objects or lines.
- The viewer can understand the main relationship without reading a paragraph.
- Thin rules, short dashed lines, small heading boxes, numbers, arrows, and icons are consistent across modules.
- The image does not contain a dense in-image legend.
- If labels are wrong or garbled, regenerate rather than patching with unrelated overlay text unless the user wants external layout text.

## Charts

- Chart type matches the data.
- Axis range and tick labels are correct.
- Category order is correct.
- Every value label is exact.
- Data marks visually match the numbers.
- Error bars or uncertainty ranges appear when requested.
- Chart axes, bars, lines, dots, and icons are flat printed graphics with no perspective or depth distortion.
- Scene elements do not block chart reading.
- If a chart is attractive but numerically wrong, reject it.

## Reference-Informed Images

- Reference cues are accurate enough for the intended audience.
- Brand/model/entity icons are abstracted into unbranded two-dimensional line icons without copied logos, packaging, product silhouettes, or proprietary type.
- Historical, cultural, scientific, or biological details do not imply unsupported certainty.

## Education And Science

- Labels point to the correct part or process.
- Mechanism, scale, direction, or sequence is not misleading.
- Cute scene elements do not distract from the concept.
- Uncertain details are noted in `PROMPTS.md`.
