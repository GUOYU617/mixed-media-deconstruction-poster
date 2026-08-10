# Position-Locked Transition Patterns

The source composition remains fixed. Choose only how media replace or fade source regions. Preserve the source ratio by default; when no usable ratio exists, use vertical 3:5.

## Interlocking registered torn reveal — default

Keep one or two story-rich irregular photographic regions in their original coordinates. Translate adjacent source regions into graphite, watercolor, line work, or crayon without moving them. Use 2–4 mandatory interlocking torn-paper seams whose paths are derived from visible source structures such as tree crowns, branches, rooflines, eaves, shorelines, ridges, roads, garments, or figure silhouettes. Give every seam different media on its two sides. Show irregular white paper fibers, a slight lifted lip, perceptible paper thickness, and a very shallow natural shadow. Continue every road, rail, roofline, limb, or contour across the tear.

Use when identity or factual detail benefits from a photographic anchor.

## Continuous line scaffold

Reduce much of the source to graphite or ink construction lines at the original coordinates, then retain selected photo or color-media zones in place. Long source lines form the scaffold and must remain uninterrupted.

Use for streets, architecture, vehicles, tools, and strong perspective.

## Selective material substitution

Keep the entire original geometry visible while replacing neighboring material zones in place: for example sky as watercolor, structure as graphite, openings as line art, and ground as crayon. Boundaries follow source parts rather than arbitrary panels.

Use for buildings, products, garments, armor, plants, and layered objects.

## Peripheral paper fade

Keep the main subject and required context registered near their original positions. Gradually reduce low-priority peripheral or background regions into faint lines, dry-brush residue, and blank paper. Do not pull the subject toward the new whitespace.

Use when the source is cluttered or the user wants more breathing room.

## Single photo window

Retain one dominant, irregular photo window at its original location and render the remaining source field as sparse aligned drawing or wash. Avoid additional photo fragments or separate detail cards.

Use for documentary scenes, people, artwork, or culturally sensitive subjects.

## Layer-locked wash

Keep all source contours and positions, but vary media through translucent masks aligned to visible structural layers. Let the same outline pass through watercolor, graphite, and crayon without duplication.

Use when hard torn edges would damage identity or continuous form.

Even with this pattern, place the 2–4 mandatory torn seams along safer surrounding contours. Soft layer transitions may protect faces, hands, text, or fine structure, but they do not replace the visible seams.

## Mandatory seam rule

- Include exactly 2–4 clearly visible in-place torn-paper seams in every generated result.
- Route them along named source contours; never use an arbitrary full-width or full-height divider.
- Put different declared media on the two sides of each seam.
- Show white fibrous rupture, a slight lifted paper lip, visible paper thickness, and a very shallow shadow.
- Permit registered paper-layer overlap, but forbid moved, rotated, independently scaled, detached, floating, or sticker-like fragments.
- At 25% viewing scale, at least two seams must still read immediately as torn paper rather than watercolor feathering or a soft mask.

## Whitespace rules

- Reserve at least 20% of the total canvas as visible whitespace in every default result.
- Count bare neutral paper and only extremely faint, incomplete graphite lines or watercolor residue toward this minimum. Do not count dense drawing, full watercolor coverage, photographic texture, torn-edge decoration, stains, or paper color alone.
- Create whitespace at the source perimeter, in C-priority regions, or through faint incomplete rendering.
- Permit uniform whole-image reduction to create an outer paper margin; keep internal coordinates unchanged.
- Preserve important subject coverage even when the reference aesthetic is sparse.
- Do not fill cleared areas with relocated objects, close-ups, labels, or decorative fragments.
- Prefer generous calm paper fields over evenly filling every source region. Preserve enough aligned evidence to recognize the original scene, then let low-priority texture stop early.
- Use neutral, source-matched pale paper; whitespace must not tint the entire image yellow.
- Estimate whitespace as a share of the whole canvas before generation and verify it again on the raster. If the estimate is below 20%, enlarge peripheral paper fields or simplify additional C-priority detail without moving or erasing required A/B regions.

## Forbidden default layouts

Do not use exploded specimens, orbiting parts, field-note constellations, separate detail studies, foldout panels, material islands, four-quadrant samples, independently enlarged crops, upper-photo/lower-illustration stacks, left/right before-and-after splits, equal bands, or a rectangular photo pasted beside a drawing unless the user explicitly requests repositioning.

## Pattern record

```text
<transition pattern> / <photo-retained region> / <B regions and media> /
<C regions> / <continuation lines> / <paper margin or internal fade>
```
