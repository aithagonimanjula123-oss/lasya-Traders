# Lasya Traders Shop Chandur

Static storefront for **Lasya Traders Shop Chandur**. The existing design and demo portal remain in `index.html`.

## Netlify deployment

This repository is a plain HTML/CSS/JavaScript site and does not need a build command.

1. In Netlify, choose **Add new site → Import an existing project**.
2. Connect GitHub and select `aithagonimanjula123-oss/lasya-Traders`, branch `main`.
3. Use an empty build command and publish directory `.` (the repository root).
4. After the first deploy succeeds, open **Site configuration → General → Site details → Change site name** and enter `lasyatradersshopchandur`, if that name is available.
5. Verify `https://lasyatradersshopchandur.netlify.app/` before removing or renaming any old site.

The backend CORS allowlist includes `https://lasyatradersshopchandur.netlify.app`. A Netlify site name/domain still has to be assigned in the Netlify dashboard.

## Backend and database

- Backend repository: [lasya-Traders-backend](https://github.com/aithagonimanjula123-oss/lasya-Traders-backend)
- Backend URL: `https://lasya-traders-backend-2.onrender.com`
- Health endpoint: `https://lasya-traders-backend-2.onrender.com/api/health`
- Supabase project URL: `https://ftzomdrpgpdnfrqguwdj.supabase.co`

Configure these on the Render backend service (never put server secrets in frontend files):

- `SUPABASE_URL`
- `SUPABASE_SERVICE_ROLE_KEY` (server-side only; preferred for the backend)
- `SESSION_SECRET` (a long, random secret)

If you configure `SUPABASE_ANON_KEY` instead, follow Supabase RLS policies carefully. Before production use, review and enable suitable Row Level Security policies for `products`, `orders`, and `revenue_snapshots`; do not expose a service-role key in the browser.

## Deployment checks

- Confirm the Netlify deploy is successful and the requested site URL loads over HTTPS.
- Confirm the backend health endpoint reports a connected database.
- Confirm products and orders behave as expected using test data.
- Review Supabase security advisories before handling real customer orders.

**Note:** The database project and core tables already exist. This README does not seed or modify product records, orders, demo login behavior, or existing data.
