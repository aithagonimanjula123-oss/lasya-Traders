# Lasya Traders — Cloudflare Pages frontend

Premium styling and authenticated same-origin API functions are prepared on the upgrade/cloudflare-premium branch.

## Deploy checklist
1. Create a Cloudflare Pages project called lasya-traders connected to this repository and select this branch for preview.
2. Create D1 database last-traders-production, replace the placeholder UUID in wrangler.toml, and apply migrations/0001_initial.sql.
3. Set Pages secrets AUTH_SECRET, OWNER_EMAIL, OWNER_PASSWORD, STAFF_EMAIL, and STAFF_PASSWORD.
4. Test the preview before merging to the production branch.

See the backend repository's CLOUDFLARE-DEPLOY.md for complete setup and security notes. Real product data is intentionally not seeded yet.