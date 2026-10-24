# Manual Example Scenarios

Use these scenarios when changing skill behavior. They are validation prompts and expected checks, not claims that sessions have been run.

| Scenario | Example request | Inspect in the output |
| --- | --- | --- |
| Outdoor default | Create a photoshoot map for J.C. Saddington Park for a family portrait session. | Research-backed positions and walkable route; lens/framing and lighting at every stop; no unsupported clock times |
| Indoor multiple floors | Create maps for the relevant publicly accessible floors of Casa Loma. | Current floor names and plans, separate relevant sheets, stable numbering, real transfers, venue photography constraints |
| Client only | Use this supplied venue plan to create a client-facing map of these three shooting spots. | Supplied positions retained; no lens, exposure, modifier, posing, or lighting instructions in image or accompanying client copy |
| Both audiences | Create photographer and client versions of the same route. | Identical spot IDs and geography; notes appropriate to each audience |
| Detail edit | Make a 2× map detail around the pond in this existing map. | Original target used; approximately half-width/half-height map extent; honest continuations for excluded spots |
| Missing geometry | Map these verified rooms when their connections are unknown. | Clearly identified schematic with independent spot groups or a request for the essential plan; no invented doors |
| No image tool | Create a PNG when the host has no image-generation capability. | Limitation stated; concrete plan retained; no claim that a PNG exists |

Record the host/tool version, input prompt and source plans, output files, observed defects, and repairs. Reopen each final PNG. Packaging CI cannot verify these behaviors.

The repository's style example is separate from these scenarios and does not count as a completed run.
