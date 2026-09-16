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
