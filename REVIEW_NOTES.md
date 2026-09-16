# Kano×Kano reviewed build — 2026-09-14

## Fixed
- Fixed the free-trial booking submit path: removed an undefined `ref` reference that could stop `confirmBooking()` before the API request.
- Corrected the booking completion notice so it matches the current Supabase-backed behavior.
- Corrected an extra closing `section` tag in the booking page.
- Added privacy-policy consent to the booking confirmation step.
- Added a multilingual privacy policy (`privacy.html`) and linked it from public/member pages.
- Aligned Daily Conversation copy across Japanese, English, Thai, Korean, and Chinese with the current fixed 30/50-minute monthly subscription model.
- Corrected stale Thai beginner/intermediate plan notes.
- Prevented normal public pages from sending users to Stripe **test** Checkout/Customer Portal URLs. Test Stripe flows are only exposed when `?stripe_test=1` is explicitly added for development checks.
- Updated the payment-status notice to direct public users to the free trial while live payment setup is unfinished.
- Updated the Act on Specified Commercial Transactions page wording for the not-yet-live Stripe checkout.
- Added basic SEO/social metadata to the official landing page.
- Fixed the brand home link so it points to `index.html` rather than `#`.

## Verification performed
- JavaScript syntax check: all inline scripts in all HTML files pass `node --check`.
- HTML ID check: no duplicate IDs found.
- Local file-reference check: no missing local assets/pages found.
- Booking submit smoke test with a stubbed API: booking reaches the completion screen and displays the returned booking reference.
- Language-switch smoke test on the official site: Japanese, English, Thai, Korean, and Chinese pricing summaries switch without runtime errors in the offline preview.

## Still requires production credentials / backend verification
- Replace Stripe test products/payment links/customer portal with live-mode equivalents before accepting real payments.
- Verify Supabase Edge Function CORS, Auth Site URL/redirects, and RLS/Edge Function authorization against the final production domain.
- Complete verified production email sender setup.
- Complete the final Google Calendar / Google Meet production integration if automated meeting creation is required.

## v37 mobile/content refinements
- Repositioned the HEART / LEARN / CONNECT hero artwork to the right of the mobile headline and prevented it from covering the intro copy; the CONNECT card stays inside the viewport.
- Rewrote the “3 reasons” intro as a concise Kano×Kano strengths message.
- Kept the representative name on one line on narrow phones and revised the profile goal statement around understanding others, expressing oneself, and building relationships.
- Made the JLPT 6-month / 1-year track names the primary labels in the N5 and N4 detail choices.
- Changed the lesson-flow layout to a clear vertical 1 → 2 → 3 → 4 sequence.
- Verified 320 / 360 / 390 / 430 / 498 px mobile widths without page-level horizontal overflow.

### v66 multilingual verification
- Verified translation-key parity for ja/en/th/ko/zh on `index.html` and `booking.html`.
- Verified inline JavaScript syntax and duplicate IDs for `index.html`, `booking.html`, and `privacy.html`.
- Fixed language persistence from landing page → booking page and booking/privacy navigation.

## v75 pre-launch language audit
- Verified index/booking translation key parity across ja/en/th/ko/zh.
- Checked 320px, 390px and desktop widths for horizontal text overflow on index and all four booking steps.
- Added full five-language support and language persistence to `tokusho.html`.
- Updated Japanese timezone note to reflect that local-time conversion is already implemented.


## v80
- Added Supabase Calendar/Meet sync queue + dispatcher architecture.
- Admin Meet URL is read-only/automatic; confirming a booking triggers generation after Google Apps Script bridge is connected.
- Monthly-plan no-rollover/expiry policy clarified in site, student portal, and legal page in 5 languages.
- Stripe sandbox monthly Payment Links require explicit agreement to credit expiry policy.
- Added Google Apps Script bridge source and one-time setup guide.

## v81
- Hardened Google Calendar bridge against duplicate event creation.
- Added Apps Script LockService serialization and booking-ID extendedProperties lookup.
- Repeated/concurrent upsert calls now reuse the same Calendar event and Meet link.

- v82: Removed the orange box-shadow/glow outside the fixed free-trial CTA; pill shape and internal sheen remain unchanged.


## v83
- Hero catchcopy changed from 「ことばで、人と人を近づける。」 to 「ことばで、人と人をつなげる。」; equivalent localized hero copy updated.
- Mobile three-reasons detail illustrations enlarged; HEART, LEARN/CONNECT cards and orange labels use larger type while keeping long labels single-line and inside the illustration.


## v84 mobile reason-detail polish
- Expanded reason-detail illustration is moved to the top of the phone viewport.
- Orange route labels are substantially larger while remaining single-line.
- Detail overlay uses nearly the full dynamic viewport height; explanation text is no longer clipped and can scroll only when truly necessary.


## v85 pricing update
- Beginner 50-min monthly plans: ¥12,000 / ¥23,200 / ¥33,600 for 4 / 8 / 12 lessons.
- Intermediate 50-min monthly plans: same pricing.
- Local-currency approximate conversion source amounts updated.
- Daily conversation and JLPT pricing unchanged.
- Stripe sandbox: created new recurring Prices and Payment Links for the six beginner/intermediate plans; website test links now point to the new sandbox links. Old sandbox payment links deactivated.
- Supabase stripe_plan_mappings updated to the six new sandbox Price IDs and new JPY amounts.
- Production Stripe remains untouched/not enabled.


## v86 pricing update
- Updated daily conversation monthly pricing across all 5 languages.
- 30 min: 4/month ¥7,200; 8/month ¥13,600; 12/month ¥19,200.
- 50 min: 4/month ¥10,400; 8/month ¥20,000; 12/month ¥28,800.
- Updated JPY source values used for approximate currency display.
- JLPT pricing remains unchanged in v86 pending final decision.


## v87 JLPT pricing update
- Updated JLPT N5 51-lesson package from ¥100,000 to ¥160,000.
- Updated JLPT N4 51-lesson package from ¥100,000 to ¥170,000.
- Updated all five site languages and local-currency reference amounts.
- Updated sandbox Stripe test Payment Links to the new v87 one-time Prices and retired the previous ¥100,000 JLPT links.
- Updated the legal price range in `tokusho.html` to ¥7,200–¥170,000.
- Updated Supabase `stripe_plan_mappings` for `jlpt_n5_package` and `jlpt_n4_package` to the new Stripe Price IDs and prices.


## v88 pricing consistency fix
- Replaced all six daily-conversation sandbox Stripe Prices with the new monthly prices: 30 min ¥7,200 / ¥13,600 / ¥19,200; 50 min ¥10,400 / ¥20,000 / ¥28,800.
- Replaced the six sandbox Payment Links in `index.html` and retired the previous daily-conversation Payment Links.
- Updated Supabase `stripe_plan_mappings` for all six daily-conversation plans to the new Price IDs and amounts.
- Retired the previous daily-conversation sandbox Stripe Price objects.
- No Stripe live-mode objects were changed.
- Updated the admin manual-entry default from the retired ¥16,000 example to ¥23,200, matching the current 50-minute monthly 8-lesson standard plan.


## v89
- Added a new pre-course section explaining Kano×Kano continuous learning support beyond lesson time.
- Added animated learning cycle: 1-to-1 lesson → feedback/focus → between-lesson learning → questions → next lesson.
- Added responsive mobile timeline and five-language localization.

## v97
- Enlarged the collapsed continuity-cycle nodes so all five Japanese titles remain on one line on mobile, including 「わからないことを質問」.
- Changed the Kano×Kano flow comparison pill to the same soft orange palette used by the 「だから〜」 conclusion card.

## v101
- Changed the continuity-cycle trail so every moving arrow erases the opposite blue trail by the same travelled fraction; the effect now uses line length rather than a delayed opacity fade.
- Removed forced empty space above course detail links; detail prompts now sit immediately under each course description.
- Removed JLPT package prices from the closed course cards and moved the 51-lesson package, price, one-to-one format, ongoing support, and 6-month/1-year choice into the opened detail panel.
- Added ongoing-support wording to Beginner, Intermediate, JLPT N5, and JLPT N4 plan metadata in all five languages.
