IA08 | Deployment Readiness, Release Evidence and Rollback
Walkthrough
1. Deployment Configuration & Smoke Tests
Stack: Next.js App Router deployed on Vercel / Render connected to Supabase PostgreSQL.
Environment Variables: NEXT_PUBLIC_SUPABASE_URL, NEXT_PUBLIC_SUPABASE_ANON_KEY.
Smoke Tests: Menu fetching, delivery calculation, POS auth, kitchen queue update, admin dashboard
metrics, and error handling.
2. Rollback Walkthrough
In case of a breaking database migration causing API failures, immediate rollback is triggered on Vercel/
Render to previous stable tag (`v1.0-release`), followed by hotfix patching and re-verification.
