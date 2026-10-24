# Visual system and rendering

## Retained reference

Inspect `../assets/style-reference.png`. This is the user's selected 1536 × 1024 PNG, retained unchanged from the attachment supplied when the skill was created. It demonstrates the desired rendering quality and map/commentary layout. Its depicted park geometry is illustrative, and its route arrows and photography timing are not standards to reproduce.

Preserve these visual traits:

- Delicate ink contours, soft watercolor, warm ivory paper, natural foliage greens and blue water; subtle texture without photorealistic sharpening.
- Predominantly overhead cartography with lightly dimensional trees or furnishings. Geographic structure remains legible beneath illustration.
- Deep green serif venue title, restrained italic feature labels, comfortable body text. Orange numbered circles with ivory outlines and fine dashed orange route arrows.
- In photographer mode, roughly two-thirds map and one-third matching numbered commentary cards on the right. Each card has a short bold scene title and concise lens/lighting prose. Prefer shorter notes or more sheets over tiny text.
- In client mode, expand the map and use only a compact numbered spot key where needed. No empty photographer cards or technical notes in the margins.
- Small legend, floor/zone subtitle, optional verified north arrow, and discreet “Illustrated map · Not to scale” footer. Include map-data attribution where the source requires it; do not automatically attribute indoor plans to OpenStreetMap.

Match style across a multi-image set. Do not carry over J.C. Saddington Park, its pond, willow trees, room names, five-stop count, clock times, or lighting assumptions to unrelated locations.

## Prompt assembly

Use the built-in image tool. Before an edit, inspect any local edit target that has not yet been viewed. Pass every required source by local image path when available; clearly distinguish the role of each input. For PDF plans, use the PDF workflow to inspect and render the relevant pages as reference images.

Compose each prompt from the actual researched stop list:

```text
Asset: finished illustrated photoshoot map PNG.
Audience: [photographer OR client].
Image roles: [bundled style reference; verified layout reference; optional edit target].
Location and sheet: [venue, outdoor zone or exact floor name, sheet index].
Geography: [source-backed outline, landmarks/rooms, entrances, connections, orientation].
Composition: [map extent, landscape framing, notes column OR client spot key].
Visual style: preserve the bundled reference's watercolor/ink rendering and detail level.
Stops: [stable numbers, short names, exact positions anchored to features].
Route: [ordered walkable connections, transfers, off-map continuations].
Text verbatim: [approved title, labels, numbered notes or client key, legend, footer].
Constraints: preserve verified geometry; no invented connections; no text overlap.
Audience exclusions: [explicitly list technical content to omit for client mode].
```

Request generous landscape resolution, normally at least 1536 × 1024 and preferably larger for five commentary cards. Use the tool's supported controls; do not promise an exact size it does not expose. Verify actual output dimensions. Dense notes should be shortened meaningfully or split across images, not omitted without explanation. Client prompts should contain client copy only rather than passing photographer paragraphs and hoping they disappear.

## Zooms and edits

For a user-requested detail map, preserve the original image's rendering, orientation, and relative geography. A 2× linear zoom shows approximately half the source width and half the source height; a 5× zoom shows one-fifth. Center on the requested feature and state approximate source bounds in the image prompt where useful. A sidebar changes the available map panel, so distinguish map zoom from total-canvas size.

Use the full original as the geography/style target when the user asks to zoom the original; do not repeatedly zoom a previously regenerated close-up. Keep feature identity and relative positions; do not add photorealistic detail or reshape the location. Retypeset labels at readable sizes instead of enlarging lettering with the map.

Stops outside the cropped extent get clearly named edge arrows or a separate overview/detail sheet. Do not pull distant features into the crop. If a shoreline or room is outside the detail, label the continuation honestly. Keep route numbers and note correspondence unchanged across sheets.

## Inspect before saving

Visually inspect every generated map against the source geography and stop list:

1. Venue, floor/zone, crop center, and orientation are correct; no invented walls, water crossings, or access routes.
2. Every intended stop appears once on its relevant map or as an explicit off-map continuation. Pin numbers match the notes and arrows progress in shooting order.
3. Photographer mode includes useful lens and lighting guidance at each stop; client mode has no photographer instructions anywhere in the image.
4. Labels and commentary are legible, correctly spelled, complete, and uncropped; markers avoid covering the very feature they identify.
5. Exact times/directions and access claims match evidence or are clearly marked as estimates. A compass is not decorative evidence of north.
6. The illustration matches the reference style; map scale/detail is not sacrificed to commentary. Related maps look like a coherent set.

Use a focused image edit for observed defects, recheck affected geography/text, then save and open the selected PNG at its final destination. Do not describe a visual check as proof of surveying accuracy. Keep source URLs and important assumptions in the delivery message rather than cluttering the map with long citations.
