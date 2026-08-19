BikePro ERP — Production Deploy

Files:
- index.html: complete ERP
- manifest.webmanifest: PWA manifest
- sw.js: offline/PWA service worker
- icon-192.png / icon-512.png: PWA icons
- BikePro_Supabase_Production.sql: Supabase table + RLS setup

Deploy:
1. Run BikePro_Supabase_Production.sql once in Supabase SQL Editor.
2. Upload all files except the SQL file to the root of your GitHub Pages repository.
3. Keep index.html at the repository root.
4. Open the site and hard-refresh once.
5. Use Create account or Sign in for Cloud.

Notes:
- The browser-side Supabase publishable key is safe to expose; database access is protected by RLS.
- Each authenticated user gets an isolated bikepro_data row.
- LocalStorage remains available as offline fallback.
- PWA install requires HTTPS (GitHub Pages provides HTTPS).
