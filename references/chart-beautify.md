# Chart Beautify

Use this reference when the user provides a chart screenshot, table, benchmark result, or metric list and wants a flat Japanese minimalist kraft-paper instruction-card chart.

## Principle

Let the image model handle printed linework, hierarchy, labels, and restrained paper texture. Do not let it infer the data.

When the input is a screenshot, extract the chart's semantic structure only. Do not inherit the screenshot's visual style.

Keep:

- Chart type.
- Title.
- Data values.
- Category order.
- X-axis and Y-axis labels.
- Axis range, tick labels, and units.
- Error bars or confidence ranges.

Discard:

- Source colors.
- Source typography.
- Source bar shape, line style, spacing, shadows, and background.
- Source screenshot crop and export artifacts.

After extraction, redraw the chart as a flat printed graphic on clean warm kraft paper. Use dark brown-red or muted brick-red as the main ink and at most a small amount of charcoal.

Do not assume the source layout is worth preserving. If the source chart is plain, cramped, ugly, or the user only provides raw data, compose a new instruction-card data graphic from scratch.

Before prompting, extract or define:

- Chart title.
- Chart type: bar, line, scatter, ranking, matrix, etc.
- Axis range and tick labels.
- Category order.
- Exact values and value labels.
- Error bars or confidence ranges if present.
- Any rule such as "lower is better" or "higher is better".

If the exact data cannot be read from a screenshot, say so and either ask for the data or mark uncertain values as approximate.

## Composition Strategy

Choose one of two chart composition modes.

### Faithful Chart Redraw

Use this only when the original chart layout is already good and the user mainly wants polish.

- Keep the same chart type and approximate chart footprint.
- Preserve the original reading order and emphasis.
- Redraw the chart with flat printed axes, fine linework, simple filled marks, and a clean hierarchy.
- Do not inherit source colors, typography, shadows, or background.

### Data-First Instruction-Card Composition

Use this by default when:

- The source chart layout is weak, generic, or too screenshot-like.
- The user only provides data.
- The chart topic benefits from a few explanatory line icons or numbered notes.
- The final image should feel like a useful printed data card rather than a report screenshot.

In this mode:

- Let the chart occupy roughly 50-70% of the image.
- Use a sparse flat line-icon panel or one small numbered note around the chart, only when it improves comprehension.
- Keep the title in a restrained heading box or simple printed header.
- Keep data marks readable and exact. Any supporting module must stay subordinate to the chart.
- Use whitespace and alignment to create hierarchy; never use perspective or decorative depth to fill the page.

Prompt pattern:

```text
Design a new flat printed composition from the extracted data: a compact [chart type] should occupy about [50-70%] of the image on clean warm kraft paper, with dark brown-red printed axes and marks, a restrained heading box, and at most one small unbranded line-icon note for [topic]. The image should feel like a useful life-instruction data card, not a dashboard screenshot or decorative poster.
```

Examples:

- Coding benchmark: a flat terminal or checklist line icon beside a compact chart.
- Travel spend chart: a route line and small luggage-tag icon beside a compact chart.
- Fitness progress chart: a calendar and timer line icon beside a compact chart.
- Finance chart: a ledger and small warning flag line icon beside a compact chart.

## Reference Lookup For Entity Icons

When chart categories contain concrete entities, add small semantic line icons only if they help the viewer scan the data.

Look up reference images when:

- The entity is a brand, model family, product, app, dataset, city, material, object, animal, food, or other visual concept.
- The model may not know the current silhouette, icon geometry, or visual convention.
- Multiple categories come from different vendors or domains and would benefit from distinguishable abstract cues.

Do not look up references when:

- All categories share the same visual identity and icons would add noise.
- The user asks for a purely abstract chart.
- The data is sensitive and visual branding could imply endorsement.

Reference workflow:

1. Search for 1-3 reference images per icon family, preferably official or widely recognized sources.
2. Extract only the stable visual cue: silhouette, symbol type, geometry, motif, or icon metaphor.
3. Prompt the image model to create a simple unbranded two-dimensional line icon based on that cue.
4. Keep all icons in the same dark brown-red print system, with at most a small amount of charcoal and no filled 3D volume.
5. Do not paste flat logos into the final chart. Convert stable visual cues into abstract unbranded icons instead.

Prompt pattern:

```text
Reference-informed icons: include a small two-dimensional line icon beside each relevant category, printed in dark brown-red on warm kraft paper. [Entity group A] uses a simplified [visual cue]. [Entity group B] uses a simplified [visual cue]. These are abstract category cues, not pasted logos or copied brand marks.
```

Example:

```text
GPT/OpenAI categories use a simplified knot-like line icon. Claude categories use a simplified radial starburst line icon. Gemini category uses a simplified four-point sparkle line icon. These are abstract category cues, not pasted logos or copied brand marks.
```

## Prompt Requirements

For chart generation, include a `Required chart accuracy` block in the prompt. List every value explicitly.

Example:

```text
Required chart accuracy: y-axis tick labels must be exactly 1.0, 1.5, 2.0, 2.5, 3.0. Bar heights must match the values relative to this axis. Category labels must be exactly: "Sonnet 4.6", "Mythos Preview", "Opus 4.8", "Sonnet 5". Value labels must be exactly: "2.89", "1.95", "2.10", "2.53".
```

Also include:

- `Do not add extra categories.`
- `Do not swap bar order.`
- `Do not invent extra tick labels.`
- `All text must be crisp, readable, and spelled exactly as specified.`

## Visual Treatment

Use the same visual language as the main instruction-card system:

- Clean warm kraft paper with only subtle fiber and grain variation.
- Dark brown-red or muted brick-red axes, rules, marks, and labels.
- At most a small amount of charcoal for secondary structure.
- Flat bars, lines, dots, grids, and simple line icons; no perspective, 3D rendering, or heavy shadow.
- Generous margins and orderly spacing; keep the chart recognizable as a chart, not a decorative poster.

Good chart enhancements:

- Fine printed gridlines and clear axis labels.
- Flat bars with restrained ink-density variation.
- Small line icons that clarify categories without becoming logos.
- Exact value labels above marks.
- One minimal numbered callout for a highlighted point.

Avoid:

- Overly cinematic backgrounds.
- Perspective that distorts the axis.
- Decorative objects that obscure bars, labels, or error bars.
- Extra explanatory text inside the plot area.
- Glossy, metallic, neon, gradient, or 3D effects.
- Preserving a weak screenshot layout just because a screenshot was provided.

## QA Checklist

After generation, inspect the image and verify:

- Axis range and tick labels are correct.
- Category order is correct.
- Every value label is exact.
- Bar heights or data marks visually match the numbers.
- Error bars are present when requested and roughly match the specified ranges.
- Text has no spelling mistakes.
- The paper, ink, linework, and layout match the instruction-card system.
- No source watermark, fake logo, brand name, or copied packaging was added.

If any number, category, or tick label is wrong, regenerate. Do not accept an attractive chart with wrong data.

## Example Prompt: Benchmark Bar Chart

```text
Use case: infographic-diagram
Asset type: 16:9 flat printed benchmark chart on a Japanese minimalist kraft-paper instruction card
Primary request: Create a clear benchmark bar chart titled "Misaligned behavior". The chart must show four model scores on a y-axis from 1.0 to 3.0. Lower score is better. Preserve these exact data values and print the value above each bar: Sonnet 4.6 = 2.89, Mythos Preview = 1.95, Opus 4.8 = 2.10, Sonnet 5 = 2.53. Use flat vertical bars, fine dark brown-red linework, restrained filled ink, and generous paper margins.
Required chart accuracy: y-axis tick labels must be exactly 1.0, 1.5, 2.0, 2.5, 3.0. Bar heights must match the values relative to this axis. Category labels must be exactly: "Sonnet 4.6", "Mythos Preview", "Opus 4.8", "Sonnet 5". Value labels must be exactly: "2.89", "1.95", "2.10", "2.53".
Background: clean warm natural kraft paper close to light beige, oatmeal, and pale khaki, with extremely subtle paper fibers and fine grain; no stains, folds, tears, or heavy vintage distressing.
Printing: dark brown-red or muted brick-red single-color print effect, with at most a small amount of charcoal; low saturation, soft natural contrast.
Drawing: fine, even, clear two-dimensional hand-drawn linework, front-facing flat composition, no photorealism, no 3D rendering, no perspective lens effect, no heavy shadow.
Composition/framing: wide 16:9 chart, generous margins, no cropped labels, restrained title box at top, axis label on the left, clean printed gridlines.
Text constraints: all text must be crisp, readable, and spelled exactly as specified. Do not add extra words beyond the title, axis label, tick labels, category labels, and value labels.
Avoid: wrong numbers, wrong tick labels, extra categories, swapped bar order, distorted coordinate system, watermark, logo, brand name, copied packaging, proprietary typography, decorative blobs, neon, metallic color, complex gradient, or children's picture-book styling.
```
