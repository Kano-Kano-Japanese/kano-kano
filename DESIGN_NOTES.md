Kano×Kano v30
- Rebuilt blue reason-orb zoom as an isolated transform-only layer.
- Blue circle remains visible behind detail text for the whole expanded state.
- Founder/profile and all later sections stay behind the expanded circle.
- Exact source-position freeze and eased post-handoff settle remove the old return snap.


## v32
Reason orbs now use a single exact-position fixed clone. The clone first paints over the tapped orb, then visibly interpolates left/top/width/height for 1.7 s. Details fade in only after expansion; closing reverses the exact geometry back to the frozen source before handoff.

## v47 mobile illustration polish
- Mobile HEART caption 「ことばは心をつなぐ」 enlarged while keeping the compact vertical spacing.
- Reason-detail orange labels now accumulate consistently from 01 → 02 → 03: existing labels retain identical positions.
- 「説明力」 moved directly below 「経験」.
- All orange labels enlarged to a common size; 「資格」「復習」「フィードバック」 are easier to read on phones.
- 03 「経験」「コミュニケーション力」 reuse the 02 positions to avoid LEARN/CONNECT overlap.
- CONNECT/「伝わる」 receives a fully opaque foreground cover so orbit lines cannot show through.


## v48 mobile refinements
- Reason illustration labels remain cumulative from 01 to 02 to 03, with qualification moved below LEARN, experience/explanation stacked below, communication moved slightly down while remaining above CONNECT, and review/feedback placed between LEARN and communication.
- CONNECT card now has an explicit opaque foreground cover so orbit lines cannot appear inside it.
- Learning-section heading is left-aligned on mobile; the small indicator dots on the first two blue nodes are orange.
- The mobile learning path has no guide line beyond the final CONNECT/つながる node; つながる is the terminal goal.

## v49 mobile reason-detail polish
- Made the CONNECT / 「伝わる」 card fully opaque with an erase halo so neither the solid nor dashed orbit can appear inside or under its rounded edge.
- Repositioned all orange labels on a shared middle ellipse between the solid and dashed orbits.
- Within each reason illustration, orange labels are distributed at equal angular intervals (01: 1 point, 02: 4 × 90°, 03: 6 × 60°).
