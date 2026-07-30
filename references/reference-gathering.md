# Reference Gathering

Use references to improve conceptual and visual accuracy. References can be information, not only images.

## When To Gather References

Gather references when:

- The topic is niche, new, technical, historical, biological, chemical, physical, regional, or culturally specific.
- The image needs a recognizable object, species, apparatus, logo cue, model family, map, artifact, costume, or building.
- The model may not know the concept well enough to draw it accurately.
- The user provides only a name but expects a concrete visual.

Do not gather references when:

- The concept is generic and references would not change the image.
- The user asks for a fast rough concept and accuracy is not important.
- The requested image is intentionally abstract.

## What To Gather

Use the web or local source material to collect:

- Short factual description: what it is, what parts matter, what process happens.
- Stable visual cues: silhouette, shape, color convention, icon geometry, material, environment.
- Relationships: cause/effect, hierarchy, sequence, comparison, map position, organism/part relation.
- Constraints: what must not be confused with a similar concept.

For brands and model families:

- Prefer official brand pages, docs, or widely recognized references.
- Extract geometry or motif only. Do not paste flat logos into the generated image.
- Use high-level visual cues, then convert the result into an abstract, unified two-dimensional line icon. Do not reproduce a branded product, logo, packaging, or proprietary type treatment.

For science:

- Prefer educational/reference sources, diagrams, textbooks, official institutions, or standard descriptions.
- Extract mechanism and part names before prompting.
- Avoid decorative objects that distort the science.

For humanities:

- Prefer reliable summaries, museum pages, historical references, primary source context, or encyclopedic references.
- Extract setting, era, social relation, artifact, clothing/tool cues, and symbolic motifs.
- Use symbolic scenes when exact depiction would imply unsupported certainty.

## Prompting With References

Do not dump references into the image prompt. Convert them into concise guidance:

```text
Reference-informed visual cues: [entity] should use [stable cue], [object] should include [important part], [scene] should suggest [era/context]. Translate these cues into the same warm kraft-paper, dark brown-red printed linework, sparse charcoal detail, and Japanese lifestyle instruction-card system. Keep the drawing flat, front-facing, and unbranded; do not include brand names, logos, copied packaging, store signage, or proprietary typography.
```

## Record Keeping

In `PROMPTS.md`, record:

- References searched or consulted.
- Extracted visual/factual cues.
- Final prompt.
- Any uncertainty that remains.
