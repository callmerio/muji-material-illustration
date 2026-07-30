# Prompt Patterns

Read `references/visual-style.md` first. Replace bracketed fields and keep prompts direct, concrete, and faithful to the user's data.

## Base Prompt Shell

```text
Use case: stylized-concept
Asset type: [wide horizontal 1.9:1 / 16:9 / 1:1] Japanese minimalist kraft-paper lifestyle instruction-card illustration for [final use]
Primary request: [plain-language description of one concept and one visual metaphor].
Chinese labels: Add [3-5] short Simplified Chinese labels as clean printed labels: "[label 1]", "[label 2]", "[label 3]", "[label 4]". Place each beside the matching object or line; keep labels horizontal, clear, readable, and away from edges.
Background: clean warm natural kraft paper close to light beige, oatmeal, and pale khaki, with extremely subtle paper fibers, fine grain, and restrained uneven tone; no stains, folds, tears, or heavy vintage distressing.
Printing: dark brown-red or muted brick-red single-color print effect, with at most a small amount of charcoal; low saturation, soft natural contrast.
Drawing: fine, even, clear two-dimensional hand-drawn linework with slight human warmth; accurate recognizable objects, moderately simplified details, front-facing flat composition.
Layout: simple orderly grid, generous natural whitespace, thin rules, short dashed lines, small heading boxes, numbered steps, simple arrows, and consistent small icons.
Typography: upright clean Chinese print type with a Japanese lifestyle magazine or product-insert feeling; restrained title, legible spaced body text, no calligraphy or proprietary brand type.
Constraints: no extra words beyond the specified labels, no English labels, no brand names, no MUJI logo or wordmark, no copied packaging or store signage, no photorealism, no 3D rendering, no real depth of field, no perspective lens effect, no thick shadows, no cartoon exaggeration, no children's picture-book style, no neon, no metallic color, no complex gradient, no crop.
```

## Cycle Diagram

Use for loops, feedback, repeated work, and recurring behavior.

```text
Primary request: [Concept] shown as a simple flat instruction diagram. Arrange [object A], [object B], [object C], and [object D] around a thin circular arrow path with numbered steps. Keep the modules evenly spaced and leave generous kraft-paper whitespace.
Chinese labels: Add four short Simplified Chinese labels: "[start label]", "[work label]", "[check label]", "[return label]".
```

Example labels: `用户提示`, `AI 执行`, `结果检查`, `下一轮`.

## Pipeline Diagram

Use for ordered work, transformation, routing, review, and lifecycle.

```text
Primary request: [Concept] shown as a left-to-right flat printed pipeline. A clear input icon enters on the left, passes through [step 1], [step 2], and [step 3] modules connected by thin arrows, then exits as a completed result on the right. Use consistent line icons and wide spacing.
Chinese labels: Add four short Simplified Chinese labels: "[input]", "[step 1]", "[step 2]", "[output]".
```

Example labels: `事件进入`, `工作流分流`, `子代理处理`, `复查收口`.

## Goal And Evaluator Diagram

Use for goals, success criteria, judging, and retry loops.

```text
Primary request: Goal-based instruction diagram. A clear target or finish condition sits on the left, an AI builder works through numbered flat task modules in the middle, and a neutral evaluator box checks whether the target is met on the right. Add a thin return arrow from the evaluator back to the builder for failed attempts.
Chinese labels: Add four short Simplified Chinese labels: "明确目标", "AI 尝试", "评估器", "未过重试".
```

## Time Check Diagram

Use for scheduled checks, polling, recurring summaries, and monitoring.

```text
Primary request: Time-based flat instruction diagram. A simple clock and calendar icon on the left trigger a small AI inspector in the center to periodically check an external system on the right, represented by clean line icons and status marks. Add a thin return line that waits for the next scheduled check.
Chinese labels: Add four short Simplified Chinese labels: "时间触发", "AI 巡检", "外部系统", "等下次".
```

## Hub-And-Spoke Diagram

Use for orchestration, classification, and parallel work.

```text
Primary request: [Concept] shown as a central printed routing box. Incoming items arrive from the left, the central box splits them into a few sparse balanced branches, each branch has a small unbranded line icon, and the branches merge into a reviewed output on the right. Use dark brown-red lines and at most a little charcoal.
Chinese labels: Add four short Simplified Chinese labels: "[input]", "[hub]", "[branch work]", "[review/output]".
```

## Before/After Diagram

Use for transformation, migration, upgrade, cleanup, and contrast.

```text
Primary request: [Concept] shown as a clean before-and-after instruction card. The left side shows [old state] with a few unresolved line icons, the center shows [intervention/process] as a numbered step, and the right side shows [new state] as ordered and complete. Keep both panels flat, legible, and evenly spaced.
Chinese labels: Add three short Simplified Chinese labels: "[before]", "[process]", "[after]".
```

## Label Repair Prompt

If the image is visually good but labels are wrong, regenerate. Do not patch text with HTML unless the user asks for external overlay text.

```text
Regenerate the same flat kraft-paper instruction-card illustration with the same composition, but make the Chinese labels exactly: "[label 1]", "[label 2]", "[label 3]", "[label 4]". Use dark brown-red printed labels, clean upright Chinese print type, generous whitespace, and no other text, brand marks, packaging, logo, 3D effect, shadow, or perspective.
```
