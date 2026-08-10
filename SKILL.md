---
name: mixed-media-deconstruction-poster
description: Analyze an uploaded or local image and preserve its most story-rich photographic details while translating adjacent in-place fragments into watercolor, graphite, simple line drawing, crayon, ink, or paper texture. Keep the source's natural colors, coordinate system, scale, viewpoint, silhouettes, and structural relationships; reserve at least 20% of the total canvas as clean visible whitespace and require 2–4 clearly visible in-place torn-paper seams that follow real contours such as trees, roofs, shorelines, roads, garments, or figures. Use for 原位艺术化, 位置锁定拼贴, 同画面撕裂融合, 照片与手绘融合, 图片局部水彩素描蜡笔化, spatially registered mixed-media posters, or clean source-preserving zine treatments without yellow vintage grading or stacked photo-and-illustration layouts.
---

# Mixed-Media Deconstruction Poster

Transform one source image within a single locked coordinate system. Replace selected regions with different physical art media in place. Do not extract, enlarge, duplicate, orbit, or rearrange parts.

Preserve the source photograph's natural color identity. The default result is clean, contemporary, and light—not yellowed, sepia, antique, distressed, or uniformly retro.

## Load the references

- Read `references/deconstruction-framework.md` for every request.
- Read `references/medium-library.md` before assigning media.
- Read `references/composition-recipes.md` before choosing an in-place transition pattern.
- Read `references/prompt-compiler.md` before generating or returning a prompt.
- Read `references/quality-gate.md` before delivery.

## Route the request

- **Analyze + Generate — default:** inspect the source, build a registered zone map, generate an in-place mixed-media poster, and inspect the raster.
- **Analyze only:** return the registered zone map, priority map, medium assignment, whitespace plan, and limitations.
- **Prompt only:** inspect the source and return the same plan plus a production-ready prompt.
- **Batch variants:** keep the identical source geometry and vary only medium allocation, transition boundaries, paper tone, or retained-photo coverage.

When the user supplies an image and asks to make a poster, use Analyze + Generate. Do not ask about choices that can be derived from the image.

## Non-negotiable spatial contract

- Preserve the source camera viewpoint, crop logic, perspective, horizon, vanishing directions, subject pose, object count, relative scale, overlap order, and adjacency.
- Keep every transformed part over the same source region. A roof remains over the roof, a face remains over the face, and a road remains over the road.
- Keep long structural lines continuous across media boundaries: rooflines, streets, rails, wires, limbs, tools, edges, and sight lines must meet at the same coordinates.
- Keep the most story-rich real photographic fragment in place. Prefer a region containing human presence, lived traces, a decisive architectural detail, an interaction, weather, light, or another source-specific narrative clue—not merely the largest or sharpest area.
- Make torn boundaries travel along or respond to source contours such as tree crowns, branches, rooflines, eaves, shorelines, ridges, roads, garment edges, or figure silhouettes. Avoid arbitrary horizontal or vertical cuts through important forms.
- Include 2–4 clearly visible in-place torn-paper seams in every generated image. They are mandatory, not optional, and soft fades or pigment blooms cannot substitute for them.
- Make each seam visibly physical: show an irregular white fibrous edge, a slight lifted paper lip, perceptible paper thickness, and a very shallow natural shadow. Keep these cues restrained but readable when the image is viewed at 25% scale.
- Put a different medium on each side of every seam, such as photo → graphite, photo → watercolor, watercolor → line drawing, or another declared pair from the zone map.
- Permit an in-place paper-layer overlap only when both sides remain registered to the same source coordinates. Never move, rotate, independently scale, detach, or float a paper fragment.
- Never create detached detail studies, exploded views, orbiting fragments, extra panels, duplicated parts, or enlarged close-ups unless the user explicitly asks to break position lock.
- Never divide the composition into an upper photograph and lower illustration, a left/right before-and-after split, stacked bands, equal panels, or a photo block pasted beside a drawing. All media must coexist as interlocking fragments inside one continuous scene.
- Permit only uniform whole-image scaling when adding peripheral paper margins or changing output size. Never scale, rotate, or translate one part independently.
- Create whitespace by fading or omitting low-priority source detail at its original location, or by adding paper around the intact image field. Do not move important content into the cleared area.
- Reserve at least 20% of the total canvas as visible whitespace. Count bare neutral paper and only extremely faint, incomplete graphite or watercolor residue; do not count densely rendered illustration, photographic texture, or decorative paper effects as whitespace. Never erase required identity or structure merely to reach the minimum.

Treat these rules as higher priority than stylistic variety.

## Source-image contract

Inspect every supplied image with `view_image`. Record dimensions, ratio, important subjects, spatial axes, structural lines, distinctive markers, visible text or branding, and uncertain regions.

Assign each image one role:

- **Edit target:** preserve its composition and transform selected regions in place.
- **Style reference:** learn only medium boundaries, paper treatment, palette, and omission behavior.
- **Supporting source:** use only when the user explicitly identifies a source region or texture.

Default the image to **edit target** when the user asks to transform “this image.” Treat additional examples as style references unless told otherwise. Do not reproduce reference watermarks, platform marks, captions, brands, or exact sample-specific tears.

## Workflow

1. **Read the source geometry and color.** Identify the whole image field, primary subject, horizon or main axis, vanishing lines, silhouettes, overlaps, joints, repeated rhythms, quiet regions, dominant natural hues, neutral balance, and light direction.
2. **Build a registered zone map.** Divide the existing image into 3–7 source-anchored regions. Record each region's approximate source location and boundary; do not make a list of movable objects. Follow `references/deconstruction-framework.md`.
3. **Assign priority and story value.** Mark each region `A — preserve`, `B — translate`, or `C — fade/omit`, then select one or two A regions as the story anchor. Keep identity-bearing and geometry-bearing regions at A or B; retain real photographic evidence where it carries the scene's narrative.
4. **Declare coordinate invariants.** State which positions, intersections, contours, counts, and continuation lines must remain unchanged.
5. **Assign media in place.** Give each A or B region one primary treatment from `references/medium-library.md`. Use at least three distinguishable media when the image supports them, but never force a medium by relocating content.
6. **Choose one registered transition pattern and budget whitespace.** Default to an interlocking registered torn reveal plus peripheral paper fade. Plan 2–4 mandatory seams, name both media on every seam, trace each path from an existing contour, and identify enough perimeter and C-priority regions to produce at least 20% visible whitespace without sacrificing required structure.
7. **Compile the prompt.** Follow `references/prompt-compiler.md`. State the 2–4 mandatory seam paths and their physical paper cues, state a source-specific whitespace target of `20% or more`, name the regions that create it, and repeat the spatial lock before the region mapping and in the avoid list.
8. **Generate through `$legacy-imagegen`.** Use its edit workflow with the actual local edit-target path. Save outside the skill directory without overwriting existing output.
9. **Inspect the raster.** Compare source and result using `references/quality-gate.md`. Any important part that moved, duplicated, changed scale independently, or broke a continuation line is a central failure. Make at most one targeted regeneration.
10. **Return the artifact and record.** Show the result, saved path, registered zone-to-medium map, retained-photo share, whitespace plan, final prompt, and any limitation.

## Design discipline

- Build one continuous scene from interlocking, position-registered fragments. Never use stacked photo-plus-illustration bands or side-by-side comparison blocks.
- Let irregular torn-paper edges follow visible natural or built contours. Continue underlying geometry through every tear; do not use arbitrary rectangular windows unless the source itself contains that shape.
- Make 2–4 torn-paper seams unmistakable through irregular white fibers, a slight lifted lip, visible paper thickness, and a very shallow shadow. Do not replace them with only watercolor feathering, dry fades, or blurred masks.
- Keep each seam between two different declared media while preserving one continuous source-registered scene. In-place paper overlap is allowed; displaced, rotated, floating, or sticker-like fragments are not.
- Preserve one or two photographic regions that contain the strongest story evidence, identity, or factual detail; transform adjacent regions without shifting them.
- Allow unimportant sky, floor, distant clutter, shadow, or repeated texture to dissolve into clean neutral paper, faint graphite, or incomplete line work.
- Keep blank paper mostly at the perimeter or inside low-priority regions. Do not erase a required face, hand, product feature, architectural opening, or structural intersection.
- Use the photograph's own natural palette as the color source. Keep whites and neutrals neutral, preserve believable greens, blues, stone, skin, wood, and local material colors, and permit only small saturation/value adjustments needed for medium translation.
- Prefer off-white, ivory-neutral, soft gray-white, or source-matched pale paper. Avoid cream-yellow wash, sepia, tobacco brown, orange cast, heavy faded-film grading, faux aging, stains, burn marks, and excessive distressing.
- Make whitespace materially generous and visually calm; the final poster should feel clean, contemporary, and editorially refined. Keep text optional and short.
- Treat 20% whitespace as a floor, not a target ceiling. Use more when the source supports it, but preserve enough aligned evidence to recognize the scene and its story.
- Do not imitate a living artist or copy reference captions, signatures, watermarks, brands, or exact transition shapes.

## Output format

````markdown
**成品海报**

![Position-locked mixed-media poster](absolute-image-path)

**原位结构与媒介映射**

| 原图区域 | 优先级 | 原位处理 | 必须保持 |
| --- | --- | --- | --- |
| ... | A/B/C | ... | ... |

**制作记录**

- Mode: [Analyze + Generate / Analyze only / Prompt only / Batch]
- Source role: [edit target / style reference / supporting source]
- Spatial preservation: locked
- Transition pattern: [recipe]
- Retained-photo share: [estimate]
- Whitespace plan: [periphery and C regions]
- Estimated whitespace share: [must be at least 20%]
- Limitation: [omit when none]

**最终 Prompt**

```text
[prompt used or ready for generation]
```
````

## Example requests

- “用 `$mixed-media-deconstruction-poster` 把这张街景原位转成照片、水彩、素描和蜡笔融合海报，建筑、道路和人物位置完全不动，天空与地面可以淡出留白。”
- “保留产品照片的轮廓和所有接口位置，只在原区域分别改成水彩、线稿和蜡笔，不要做爆炸图或局部放大。”
- “只分析这张图，给我 A/B/C 区域、原位媒介映射和留白方案，不生成图片。”
