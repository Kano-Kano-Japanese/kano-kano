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
