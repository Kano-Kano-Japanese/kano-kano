# Kano×Kano v15 design notes

- Added English **HEART** to the main 心 visual, with “LANGUAGE CONNECTS HEARTS”.
- Reasons cards gently float; tapping triggers a crack-like split animation before details emerge.
- Founder photo is embedded directly into `index.html` as WebP so it cannot go missing when only the HTML is moved.
- Founder section now blends the photo into the copy with a continuous gradient rather than separating image/text into columns.
- Monthly course cards are aligned horizontally on desktop; mobile uses horizontal swipe cards.
- Readability improved by switching all supporting copy/headings to a modern sans-serif stack. The hero slogan retains the editorial serif treatment.
- Kendo/calligraphy references were removed from non-Japanese translations and the founder philosophy was aligned across languages.


## v16
- Representative photo is shown uncropped/contained on the left and blended into the profile copy with a continuous gradient.
- Beginner/intermediate/conversation expanded monthly 4/8/12 plans span the course row and remain side-by-side; mobile uses horizontal swipe.


## v17
- Replaced the three reason cards with floating blue circular orbs.
- Tapping an orb lifts/enlarges it and opens the existing detailed explanation below.
- Orb labels are concise and localized.


## v18 interaction
- The three reasons remain floating blue orbs.
- Tapping an orb now expands that same blue orb to roughly 108vmax, intentionally clipping at screen edges and filling almost the whole viewport.
- The selected reason title and existing detailed explanation appear inside the enlarged orb.
- Close with the × button, Escape, or the small uncovered backdrop corners.

## v20 motion polish
- Reason orb close animation now returns in ~0.56s with a cross-fade into the original floating orb.
- Removed the temporary empty-blue-circle pause after closing.
- Floating free-trial CTA is hidden while the cinematic orb overlay is active to avoid visual overlap.


## v22 interaction fix
- Reason-orb zoom now uses a captured viewport rectangle (FLIP-style) from the exact clicked floating orb.
- The same frozen rectangle is reused on close, preventing the second/third orb from launching or returning from a shifted position.
- Scrollbar width is compensated while the overlay is open, eliminating horizontal layout jumps.


## v23
Reason orb zoom now uses per-click Web Animations geometry instead of persistent CSS coordinates. Each orb launches from its own current position and returns to the same frozen source position without a direction snap.

## v24 reason-orb interaction
- The 3 blue reason orbs may float outside the visual stage boundary.
- Expansion uses a pixel-perfect clone of the orb clicked in that exact frame.
- The same clone expands and contracts, avoiding the previous launch/return hand-off jump.
- Expanded content uses a wider two-column layout on desktop to reduce empty blue space.

## v25 animation fix
- Reason orbs are paused before measurement so the return target cannot drift.
- Zoom/unzoom uses compositor-only `transform` animation rather than animating left/top/width/height.
- The source orb stays paused for the entire round trip and resumes only after a pixel-matched handoff.
- Scrollbar compensation prevents horizontal layout movement while the full-screen orb is open.


## v27
- Hero connection artwork stays fully inside the hero canvas (no right/bottom overflow).
- Restored full original saturation/opacity; no faded treatment.
- HEART sits above 心, matching LEARN/CONNECT label hierarchy.
