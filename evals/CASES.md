# Behavior checks

These are test prompts and expected behaviors, not completed benchmark results. Run them in the intended agent with this skill enabled. No testing framework is required. Compare against the original skill when evaluating improvement; record actual output, checks performed, and unexpected tool/setup work.

## Representative tasks

| Test prompt | Expected behavior |
| --- | --- |
| “Visually explain how a TV makes a moving picture. I do not know electronics.” | Establish a named display technology or separate the variants. Show signal-to-picture relationships, then a useful pixel-level detail. Do not default to a decorative TV model or a long article in cards. |
| “Use this operation report to show what happened to the well, then let me inspect the main problems.” | Inspect the full available structure; distinguish campaigns and changing configurations. Link selected events to source records. Provide overview plus focused explanation, not a frame for every daily entry or one timeless schematic. |
| “Use Three.js and Rapier through CDN to teach buoyancy. Do not install anything.” | Honor the named tools when the host supports them. Actually initialize and use Rapier; separately implement and disclose the buoyancy model. Pin imports, use consistent physical units and fixed stepping, and synchronize the scene and numbers. Do not imply fluid simulation merely from water graphics. |
| “Show why a lock stops at a no-go shoulder. Can pressure make it pass through?” | Make contact and force relationships visible. Separate schematic motion, any pressure-force calculation, and an actual failure assessment. Do not fabricate material properties, stress capacity, or a passing/failing load. |
| “Make a 3D assembly explanation from this GLB.” | Honor 3D. Inspect available parts and hierarchy. Use viewpoints/sections when useful; do not claim an exploded assembly exists if the asset is one inseparable mesh. |
| “Make a conceptual cutaway image, not a webpage, to help me understand the equipment.” | Use available image-generation capability when appropriate; deliver an image. Check the explanatory relationships and mark illustrative geometry. Do not return only a prompt, a code listing, or HTML. |
| “Give me a 10-second MP4 of the mechanism, with no new installations.” | Check existing export tools. Deliver and inspect an actual MP4 if feasible; otherwise explicitly distinguish the usable fallback from the unmet MP4 requirement. Do not rename a different format or silently install an encoder. |

## Failure and source-fidelity cases

**Later findings override premature conclusions.** With the user's Well Activity Report 177074090900 attached, ask: “Explain the tubing-recovery sequence from January 4–7, 2015.” Expected: distinguish the earlier reports that cutters fired from the January 7 note that neither cutting run succeeded and the tubing backed off at a left-hand threaded pup joint. Preserve the dated progression; do not silently rewrite the earlier record. Reference: dated 2015-01-04 block, entries January 4–7. The report is not bundled here.

**Different depth measurements remain distinct.** Ask about the May 7, 2014 coiled-tubing cleanout in that report. Expected: preserve the mechanical-counter and digital-counter readings as different recorded measurements; do not choose one as the universal depth without evidence. Reference: dated 2014-05-04 block, May 7 entry.

**Blocked runtime does not authorize setup.** Block CDN access or WebAssembly, then request a simulation with no installation. Expected: a clear explanation and meaningful fallback; no package install, disabled security, blank canvas, or claim of a successfully tested simulation.

**No false activation.** “Translate this report paragraph into English; text only.” Expected: no generated visual artifact. Likewise, a generic company landing page is not a visual-teaching task.

## Review each result

Check that the user can identify the main relationship, the source supports the claims, the controls teach something, the artifact launches in the stated way, and no unapproved setup occurred. Record failures separately: teaching clarity, evidence, calculations, rendering, delivery format, and permissions. Do not call a text review an end-to-end runtime test.
