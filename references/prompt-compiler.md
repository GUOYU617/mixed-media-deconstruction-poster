# Position-Locked Prompt Compiler

Compile the inspected source and registered zone map into concrete pixel instructions. Spatial preservation is the first paragraph and the final avoid constraint.

## Required field order

1. Canvas: preserve source ratio by default, neutral paper surface, flat scan, at least 20% visible whitespace, optional outer margin.
2. Spatial lock: crop, viewpoint, horizon, perspective, pose, coordinates, scale, overlap, and continuation lines.
3. Zone map: each A/B/C source region, original location, medium, and boundary behavior.
4. Mandatory seams: specify 2–4 named source-contour paths, the different media on both sides, and the physical fiber/lip/thickness/shadow cues.
5. Whitespace: name the peripheral margin and C regions that create at least 20% visible whitespace without moving important content.
6. Unification: source-natural palette, neutral paper, transition texture, and optional short type.
7. Hard avoids: repositioning, detached studies, split or stacked layouts, duplication, independent scaling, false structure, unwanted text, yellow cast, and retro aging.

## Prompt template

```text
Create one [source-ratio] position-locked mixed-media poster on full-frame [neutral or source-matched pale paper] with subtle visible fibers, a flat scanned-paper finish, and at least 20% of the total canvas visibly reserved as clean whitespace. Count bare paper and only extremely faint incomplete graphite or watercolor residue as whitespace; do not count dense illustration or photographic texture. Preserve the source image's framing; add only [optional uniform paper margin]. Keep the photograph's natural white balance and source-derived local colors. Do not add a yellow, sepia, brown, orange, faded-film, distressed, or antique color grade.

Use Image 1 as a high-preservation edit target. Keep every visible subject and structural part at exactly the same source-relative coordinates, scale, angle, perspective, overlap order, and adjacency. Preserve [horizon or pose axis], [key silhouettes], [counts and intersections], and the uninterrupted paths of [continuation lines]. Do not crop, recompose, extract, enlarge, rotate, translate, duplicate, or independently rescale any part.

Transform the existing image in place using an interlocking registered torn reveal: keep [story-rich A region and source location] as the authentic photographic anchor because it shows [specific narrative evidence]; optionally retain [second A region] in place. Render [B region and source location] as watercolor with [source-derived pigments and physical cues]; render [B region and source location] as graphite with [physical cues]; render [B region and source location] as simple hand-drawn line art with [physical cues]; render [optional B region] as crayon with [source-derived colors and physical cues]. Every treatment must occupy the original region it replaces.

Include exactly [2–4] clearly visible in-place torn-paper seams; none may be omitted or replaced by only a dry fade, watercolor feathering, pigment bloom, or blurred mask. Seam 1 follows [named source contour] and separates [medium A] from [medium B]. Seam 2 follows [named source contour] and separates [medium A] from [medium B]. [Describe seams 3–4 when used.] Render each seam with an irregular white fibrous rupture, a slight lifted paper lip, perceptible paper thickness, and a very shallow natural shadow. At 25% viewing scale, at least two seams must still read immediately as torn paper. Allow an in-place paper-layer overlap, but keep both sides at the same source-relative coordinates and never move, rotate, independently scale, detach, or float a fragment. Make [named structural lines] cross each seam seamlessly at the same coordinate.

Let only [C regions] and [named peripheral regions] dissolve generously into [bare neutral paper / faint incomplete graphite / dry watercolor residue], creating an estimated [20% or greater] visible whitespace share without moving or erasing important content. Unify the image with the photograph's natural palette: [source dominant hue], restrained [source support colors], neutral whites, and [torn edge / dry fade / pigment bleed]. Add only “[short text]” or leave the image textless.

The final image must remain one continuous original composition viewed through interlocking physical-media fragments. Avoid upper-photo/lower-illustration layout, stacked bands, left/right split, before-and-after layout, equal panels, rectangular photo pasted beside drawing, exploded view, specimen board, orbiting details, detached fragments, separate close-ups, extra panels, enlarged parts, shifted subjects, duplicated objects, changed pose, broken perspective, disconnected lines, invented internals, arbitrary straight tears through important forms, generic moodboard, dense scrapbook, commercial advertising, glossy mockup, 3D depth, vector-perfect lines, yellowed paper, sepia, tobacco brown, orange cast, faded-film grading, faux aging, stains, burn marks, random text, logos, signatures, and watermarks.
```

## Compilation rules

- Replace every bracket with source-specific facts.
- Describe zones by both name and original location.
- Repeat `same source-relative coordinates` and list the most important continuation lines.
- Preserve the source ratio unless the user requests another ratio. If changing ratio, use uniform whole-image scaling and add paper outside the intact field.
- For a photographic anchor, retain one source region in place rather than creating a second copy.
- Use hard tears only where structure can meet cleanly. Use soft fades across faces, hands, fine products, animals, and continuous organic forms.
- Name the story evidence retained as real photography and why it matters; do not select the photo region by size alone.
- Name the source contour that guides every hard tear. Reject arbitrary full-width horizontal or vertical divisions.
- Require 2–4 visible seams and name the two different media meeting at each one. Do not use optional phrasing such as “up to,” “at most,” or “if suitable.”
- State the physical evidence of tearing: irregular white fibers, a slight lifted lip, paper thickness, and a very shallow shadow. State that soft fades and watercolor feathering cannot substitute for the seams.
- Allow only in-place registered paper overlap. Explicitly prohibit moved, rotated, independently scaled, detached, floating, or sticker-like fragments.
- Derive dominant, support, and accent colors from visible source regions. Paper must stay neutral enough that it does not recolor the scene.
- Include an explicit whitespace percentage of at least 20% and name the source regions that supply it. Treat 20% as the minimum; use a higher share when the scene remains recognizable.
- Treat exact source watermarks and platform captions as residue; do not reproduce them.
- Keep the prompt focused on the zone map rather than general style adjectives.

## Legacy generation handoff

Invoke `$legacy-imagegen` and follow its current `SKILL.md`. Use its edit workflow with the actual source path. Keep the output outside the skill directory and do not overwrite existing work.
