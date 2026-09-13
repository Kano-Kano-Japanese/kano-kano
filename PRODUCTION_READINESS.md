# Kano×Kano production-readiness checklist

## Hosting / domain
- Deploy `kano-kano` on Vercel.
- Verify the actual `*.vercel.app` URL.
- Update Supabase CORS if Vercel assigns a different hostname.
- Remove the temporary Netlify origin after cutover.
- Consider a paid custom domain later if needed.

## Stripe
- Current links are sandbox/test mode only.
- Before launch, complete Stripe account/KYC and payout settings.
- Recreate products, prices, Payment Links, webhook endpoint, and Customer Portal in live mode.
- Run a real live-mode low-value verification only when ready.

## Supabase
- Verify Vercel origin for public-booking-api, student-api, teacher-api, admin-api.
- Verify Auth Site URL / Redirect URLs for the final Vercel hostname.
- Current security-advisor warning about leaked-password protection may require a paid Supabase plan.

## Email / calendar
- Replace Resend onboarding sender with a verified Kano×Kano sending domain before production.
- Google Meet / Calendar automation still needs final production integration.

## Legal / operations
- Keep subscription cancellation policy separate from lesson-booking cancellation policy.
- Final legal review is recommended before accepting production payments internationally.
- Confirm support/contact details and privacy policy.
