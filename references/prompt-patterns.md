# Prompt Patterns

Read `references/visual-style.md` first. Replace bracketed fields and keep prompts direct, concrete, and faithful to the user's data.

## Base Prompt Shell

```text
Use case: stylized-concept
Asset type: [wide horizontal 1.9:1 / 16:9 / 1:1] labeled material illustration for [final use]
Primary request: [plain-language description of one concept and one visual metaphor].
Chinese labels: Add [3-5] short Simplified Chinese labels as clean printed callouts: "[label 1]", "[label 2]", "[label 3]", "[label 4]". Place each near the matching object; keep labels horizontal, large, high-contrast, readable, and away from edges.
Style/medium: MUJI-inspired quiet Japanese utilitarian editorial illustration; warm paper/off-white, matte cardboard/wood/ceramic materials, thin charcoal linework, soft diffuse daylight, restrained natural palette, one muted [accent name] accent ([hex]).
Composition/framing: [ratio] composition, generous whitespace, full subject visible, centered vertical balance, safe margins on all sides, designed for [known image well if any].
Tone: calm, useful, tactile, human-made, low visual noise.
Constraints: no extra words beyond the specified Chinese labels, no English labels, no numbers unless requested, no brand names, no MUJI logo or wordmark, no copied packaging or store signage, no proprietary typography, no fake brand marks, no watermark, no app chrome, no decorative blobs, no neon, no dramatic gradient, no crop.
```

## Cycle Diagram

Use for loops, feedback, repeated work, and recurring behavior.

```text
Primary request: [Concept] shown as a simple cycle. Arrange [object A], [object B], [object C], and [object D] around a sparse circular arrow path so the viewer sees how work repeats until it returns to the start. Use matte paper or small physical tokens rather than a glossy dashboard.
Chinese labels: Add four short Simplified Chinese labels: "[start label]", "[work label]", "[check label]", "[return label]".
```

Example labels: `用户提示`, `AI 执行`, `结果检查`, `下一轮`.

## Pipeline Diagram

Use for ordered work, transformation, routing, review, and lifecycle.

```text
Primary request: [Concept] shown as a left-to-right pipeline. A clear input card enters on the left, passes through [step 1 object], [step 2 object], and [step 3 object], then exits as a completed result on the right. Keep the scene sparse and tactile.
Chinese labels: Add four short Simplified Chinese labels: "[input]", "[step 1]", "[step 2]", "[output]".
```

Example labels: `事件进入`, `工作流分流`, `子代理处理`, `复查收口`.

## Goal And Evaluator Diagram

Use for goals, success criteria, judging, and retry loops.

```text
Primary request: Goal-based agent loop illustration. A clear target or finish condition sits on the left, an AI builder iterates through small paper task blocks in the middle, and a neutral evaluator gate checks whether the target is met on the right. Add a subtle return arrow from the evaluator back to the builder for failed attempts.
Chinese labels: Add four short Simplified Chinese labels: "明确目标", "AI 尝试", "评估器", "未过重试".
```

## Time Check Diagram

Use for scheduled checks, polling, recurring summaries, and monitoring.

```text
Primary request: Time-based agent loop illustration. A plain clock and calendar on the left trigger a small AI inspector in the center to periodically check an external system on the right, represented by quiet paper cards and status marks. Add a return line that waits for the next scheduled check.
Chinese labels: Add four short Simplified Chinese labels: "时间触发", "AI 巡检", "外部系统", "等下次".
```

## Hub-And-Spoke Diagram

Use for orchestration, classification, and parallel work.

```text
Primary request: [Concept] shown as a central routing hub. Incoming items arrive from the left, the neutral hub splits them into several sparse branches, each branch has a small task object, and the branches merge into a reviewed output on the right. Use one muted accent only for the route lines.
Chinese labels: Add four short Simplified Chinese labels: "[input]", "[hub]", "[branch work]", "[review/output]".
```

## Before/After Diagram

Use for transformation, migration, upgrade, cleanup, and contrast.

```text
Primary request: [Concept] shown as a before-and-after transformation. The left side shows [old state] as unorganized paper or objects, the center shows [intervention/process], and the right side shows [new state] as ordered and complete. Keep the contrast legible without exaggerated mess or glossy effects.
Chinese labels: Add three short Simplified Chinese labels: "[before]", "[process]", "[after]".
```

## Label Repair Prompt

If the image is visually good but labels are wrong, regenerate. Do not patch text with HTML unless the user asks for external overlay text.

```text
Regenerate the same illustration with the same composition and MUJI-inspired material system, but make the Chinese labels exactly: "[label 1]", "[label 2]", "[label 3]", "[label 4]". Use large printed callouts on quiet unbranded paper plates, horizontal text, high contrast, and place them away from all edges. No other text, brand marks, packaging, or logo.
```
