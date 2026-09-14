Kano×Kano v30
- Rebuilt blue reason-orb zoom as an isolated transform-only layer.
- Blue circle remains visible behind detail text for the whole expanded state.
- Founder/profile and all later sections stay behind the expanded circle.
- Exact source-position freeze and eased post-handoff settle remove the old return snap.


## v32
Reason orbs now use a single exact-position fixed clone. The clone first paints over the tapped orb, then visibly interpolates left/top/width/height for 1.7 s. Details fade in only after expansion; closing reverses the exact geometry back to the frozen source before handoff.
