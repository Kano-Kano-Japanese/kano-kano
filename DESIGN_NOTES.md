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


## v51
- Repositioned reason-detail orange labels into two fixed, equally spaced routes between the dashed and solid ellipses.
- Lower-left route: 資格 → 経験 → 説明力. Upper-right route: フィードバック → 復習 → コミュニケーション力.
- Preserved cumulative 01 → 02 → 03 positions and kept labels clear of わかる / 伝わる.

## v52 mobile reason illustration polish
- CONNECT / 「伝わる」 now uses the same gentle floating animation as LEARN / 「わかる」.
- Orange labels are spread over the full lower-left and upper-right routes with even spacing while avoiding both LEARN and CONNECT.
- REASON 01 now includes 「資格」 + 「経験」; later panels keep cumulative positions and add the remaining labels.


## v53
- Rebalanced the reason-detail orange labels across the full left and right arcs.
- Left route: 資格 → 経験 → 説明力; right route: フィードバック → 復習 → コミュニケーション力.
- CONNECT / 伝わる now uses the exact same rvFloat animation and phase as LEARN / わかる.


## v54
- 「わかる」「伝わる」の浮遊を margin ベースから transform ベースへ変更。特に bottom で絶対配置されている「伝わる」でも、10px の上下移動が確実に見えるようにした。


## v55
- Shortened and completed the Japanese “全員 国家資格” detail copy; removed 「指導経験や」.
- Learning-flow lines now run circle-edge to circle-edge instead of through node centers.
- On mobile, the next learning node remains fully hidden until the incoming line reaches its edge, then appears at the same threshold.
- Removed the passive learning guide line so no line continues beyond the final 「つながる」 goal.

## v57 (2026-09-15)
- Hero copy order changed to 「相手を理解し、気持ちを伝え」.
- Hero LEARN / CONNECT cards now slowly orbit the HEART mark on a shared path.
- 「伝わる」 learning feature chip changed to the orange accent treatment.
- Founder profile adds long-term exposure to Japanese culture: anime, over 10 years of kendo (3rd dan), and a calligraphy rank.
- AI-era profile sentence revised to 「知識が一瞬で手に入り、簡単に翻訳できる時代」.
- Japanese course heading shortened to 「コース・料金案内」.
- On mobile, 30-minute and 50-minute Daily Conversation consultation buttons stay side-by-side for 4/8/12 monthly plans.

## v58
- Hero orbit corrected so LEARN/CONNECT revolve around the actual HEART center on mobile without crossing the heart tile.
- Beginner title updated to 「初級日本語コース（ゼロ～N5目安）」.
- Replaced the orange monthly-price summary on the three main course cards with lesson-duration information: 50-minute 1-to-1 for beginner/intermediate; 30- or 50-minute 1-to-1 choice for conversation.

## v60
- Mobile hero orbit moved inward so LEARN/CONNECT cards never clip at the right viewport edge.
- Long コミュニケーション力 chip shifted inward while keeping the reason-illustration route.
- EXPRESS feature pill keeps orange treatment with a blue leading dot.
- Course duration summaries use the orange accent.


- v63: Repositioned the long 「コミュニケーション力」 pill so it clears HEART, CONNECT, and the right edge on mobile.


## v65 — Hero free-trial button sheen
- Extended the hero CTA sheen travel so the highlight exits completely past the right edge instead of stopping mid-button.
- The visible sweep now runs continuously across the full button before fading out and waiting for the next cycle.
