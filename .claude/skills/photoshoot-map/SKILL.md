---
name: photoshoot-map
description: "Create illustrated photoshoot maps for a supplied location, with numbered shooting spots, routes, and lens and lighting notes. Use for outdoor shoot planning, indoor or multi-floor venue maps, and client-facing versions that show shooting spots without photographer instructions."
metadata:
  version: "0.1.0"
---

# Photoshoot Map

Create finished PNG maps in the visual style of [assets/style-reference.png](assets/style-reference.png). A location alone is enough to start. Research the place, choose useful shooting spots, and render the maps; do not stop at a written itinerary or image prompt.

## Inputs and defaults

- Required: an identifiable location or a supplied site/floor plan. Resolve the location from context and research; ask only if plausible alternatives remain.
- Optional: indoor/outdoor scope, shoot type, date and local time, duration, group size, mobility needs, available lenses/lights, crop or zoom, output destination, and audience.
- Default audience: photographer. Every proposed spot gets lens/framing and lighting guidance tailored to that scene. Default to a small portrait session when the subject is unspecified, stating the assumption briefly rather than requiring an intake questionnaire.
- Default coverage: outdoor locations use outdoor maps. An indoor request uses interior maps. A named multi-floor attraction such as Casa Loma calls for separate maps of its relevant, verified, publicly accessible floors; include grounds only when requested or useful for the proposed shoot. Read [references/indoor.md](references/indoor.md) for indoor or mixed coverage.
- Default deliverable: landscape PNG, one map for a compact location. Split into floor, zone, or overview/detail maps when scale, route, or note readability warrants it. Do not force every venue into five stops or one image.
- If date/time is missing, describe useful light conditions or relative timing such as “before sunset.” Do not reuse the reference's September clock times, sunset direction, or equipment settings.

## Establish the geography and shoot conditions

Inspect the bundled style image with the image viewer before the first render. It is a visual reference, not evidence of the new location's geography, amenities, or shooting conditions.

Use current authoritative venue maps, visitor floor plans, park/city pages, and recent site imagery to establish entrances, walkable connections, landmarks, rooms, floors, and usable shooting areas. Prefer official sources; use OpenStreetMap or other mapping sources for outdoor geometry when useful. Keep source links and distinguish verified layout from photographic recommendations. Inspect map images rather than relying only on search snippets. Preserve required source attribution.

Check venue photography/access rules when they affect the proposed shoot, especially indoor flash, tripods, commercial sessions, and restricted rooms. Do not infer that visitor access permits a booked photoshoot. Record a concrete unresolved constraint briefly rather than inventing permission or adding a generic warning page. Do not book, contact a venue, or submit a permit without authorization.

For a supplied date/time, verify local timezone and sun position before printing exact sunset times or directional lighting claims. Treat weather, seasonal foliage, and interior lights as uncertain unless supported. Distinguish a plausible window-light setup from a verified window orientation. Do not invent room layouts, water crossings, doors, stairs, or access connections to make a route fit.

## Plan the shooting spots

Choose a varied, practical sequence based on backgrounds, usable light, group movement, and the requested session length. Usually three to six stops fit a compact map; use fewer or additional sheets when appropriate. Honor supplied shoot locations and commentary, correcting evident mismatches rather than silently relocating the features.

Maintain one working stop list before rendering. For each stop record:

- A stable number, short name, map/floor, and a location anchored to a verified feature.
- Intended portrait/framing and why that background works.
- Lens or focal-length range, expressed as full-frame equivalent unless the user's camera is known; adapt to available gear and working distance.
- Lighting direction/quality, where subjects face or stand, and a feasible modifier or available-light alternative when relevant.
- Timing only when useful and supported; any material access uncertainty.

Photographer notes should be concise and practical, usually two to four short sentences per spot. Avoid a generic lens list repeated at every stop. For example, wider environmental portraits need careful distance and edge placement; a tight interior may not support an 85mm portrait. Recommend apertures for the actual subject depth rather than copying f/2.8 onto every group. Treat exposure compensation as a starting experiment, not a universally correct setting. Never recommend prohibited lighting gear; offer an allowed alternative.

Keep numbering consistent across map pins, commentary, route, and every sheet in the set. Continue numbering across floors in shooting order and label transfers by actual stair/lift names where known. Route lines follow walkable ground or corridors, with arrows pointing in shooting order. Do not draw straight connections through water, walls, planted beds, or restricted rooms.

## Audience modes

**Photographer (default):** illustrated map plus a side column of matching numbered notes. Include scene-specific lens/framing and lighting at every stop; add timing or posing only when helpful. Use the supplied image's map-and-commentary balance.

**Client-facing:** show only intended shooting spots and the minimal map context needed to locate them: numbers, short location names, recognizable landmarks, a simple route or floor transfer, and a short nontechnical description of the planned photo if useful. Remove the photography notes column or replace it with a compact spot key. Exclude focal lengths, lens names, apertures, ISO, shutter speed, exposure compensation, metering, flash/reflector placement, lighting theory, and directing/posing instructions from both the image and accompanying client deliverable. Keep any necessary planning clarification separate and brief. Do not produce an unrequested photographer version.

If both versions are requested, derive them from the same stop list and geometry; preserve spot numbers and floor names. More than one floor/zone can still be needed in either audience mode.

## Render and deliver

Read [references/rendering.md](references/rendering.md) for the visual system, prompt structure, zoom handling, and visual checks. Use the available built-in image generation tool and the imagegen skill for raster generation and edits. Attach the bundled image as a **style reference** and any site/floor plans as **geography references**, identifying their roles explicitly. For edits, identify the existing map as the edit target. The skill is portable: resolve assets relative to this SKILL.md, not the original attachment path.

Generate one image per planned map and inspect each before delivery. Repair observed rendering problems with focused image edits. If image generation is unavailable, explain the limitation and retain a concrete shoot plan and render specification; do not claim a PNG was created or silently replace it with a schematic. Follow the imagegen workflow for any fallback.

Copy the final generated PNGs into the user's requested destination, otherwise `output/photoshoot-maps/<location-slug>/` under the active workspace. Use descriptive names such as `<location>-outdoor-photographer.png`, `<location>-ground-floor-client.png`, or `<location>-pond-2x-photographer.png`. Preserve existing files by versioning new outputs unless replacement was requested. Verify the saved PNG opens and has the intended dimensions.

Deliver clickable links to all final PNGs, with floor/zone and audience identified. Include concise source links and material assumptions in the accompanying response; keep the maps visually uncluttered. Do not claim the package is installed globally merely because this project-local skill exists.
