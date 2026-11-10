# SARSWATI PUJA SAMITI – BAGHAKOL Official Website

A free static website + existing Supabase-backed web portal.

## Free stack
- GitHub Pages: free static hosting (no paid server required).
- Existing Supabase project: reuse the current project and publishable key.
- QR Code: generated in the browser from the deployed website URL.
- APK distribution: add a reviewed APK under `downloads/app.apk`, or use a GitHub Release asset.

No new paid backend is required. Static hosting serves the site; Supabase remains the data/auth backend for `portal.html`.

## Important APK security gate
The APK supplied for this project contains Groq, Gemini and OpenAI API keys in its embedded `assets/public/config.js`. Do NOT publish that APK. Revoke/rotate those provider keys, remove them from client-side code, route AI requests through secured Supabase Edge Functions, rebuild and test a clean APK first.

The download button is deliberately disabled in `js/site.js`:
`const APP_DOWNLOAD_ENABLED = false;`
After placing the security-reviewed APK at `downloads/app.apk`, change it to `true`.

The QR code currently points to this website's `#download` section. After deployment, it automatically reflects the live website URL and can be saved as a PNG from the page.

## Deploy free with GitHub Pages
1. Create a GitHub account if needed.
2. Create a public repository, e.g. `sarswati-puja-samiti`.
3. Upload all files/folders in this project to the repository root (not the ZIP itself).
4. Open repository Settings → Pages.
5. Under Build and deployment, choose Deploy from a branch.
6. Select `main` and `/ (root)`, then Save.
7. GitHub will provide a free URL such as `https://USERNAME.github.io/sarswati-puja-samiti/`.
8. Open the URL. The QR is generated using that actual live URL.

GitHub Pages is static hosting; it does not run a private server. The web portal connects to the existing Supabase backend. Never put a Supabase service_role key or AI provider secret in this repository.

## Upload the APK
Recommended: create a GitHub Release and upload the reviewed APK as a release asset. Or place it in `downloads/app.apk` before publishing. If you use a Release URL, update `APP_DOWNLOAD_URL` in `js/site.js` to that exact asset URL.

## Web portal
`portal.html` is the existing app's browser interface copied from the project source. It uses `portal-config.js` and the same Supabase project. Its real access depends on deployed tables, RPCs, Edge Functions and RLS policies. The live backend was not independently verified during website packaging.

## Files
- `index.html`: public website and app download page
- `portal.html`: existing Supabase-connected web portal
- `portal-config.js`: Supabase URL + publishable key only
- `assets/`: original Samiti logo
- `css/site.css`, `js/site.js`: website design and QR generator
- `downloads/`: place the security-reviewed APK here

## No paid services
You can use the default GitHub Pages URL for free. A custom domain is optional and generally costs money. Supabase free-plan limits and current plan terms apply; this website does not create a second Supabase project.
