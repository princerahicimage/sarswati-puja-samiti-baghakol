# Sarswati Puja Samiti – Baghakol Official Website

## Contents
- `index.html` — redesigned official public website
- `css/style.css`, `js/site.js` — responsive styling and navigation
- `assets/samiti-logo.png` — original logo extracted from the supplied app package
- `assets/gallery/` — photos supplied by the Samiti
- `portal.html`, `portal-config.js` — existing web portal and its browser-safe Supabase publishable configuration
- `site.webmanifest` — installable website metadata

## Publish free using GitHub Pages
1. Open your existing repository `princerahicimage/sarswati-puja-samiti-bag hakol` (use the exact repository name shown in GitHub).
2. Upload the contents of this folder to the repository root. Do not upload the parent folder itself.
3. Replace the existing `index.html`, `portal.html`, `portal-config.js`, and `README.md` if GitHub asks.
4. Commit to branch `main`.
5. In Settings → Pages, choose Deploy from a branch → `main` → `/(root)` → Save.
6. Wait for the Pages deployment to finish, then hard-refresh the website (Ctrl+F5).

## APK security warning — do not publish the currently supplied APK
The supplied APK contains Groq, Gemini and OpenAI API credentials embedded in `assets/public/config.js`. Anyone downloading the APK can extract these credentials and use them. Revoke/rotate those keys immediately, remove provider secrets from client-side app code, move AI calls behind a secured backend (e.g. Supabase Edge Functions with authentication and rate limits), rebuild and test a clean APK.
The supplied APK is included at `downloads/sarswati-puja-samiti.apk`, and the download button plus APK QR code are enabled as requested. **Security warning:** this APK contains provider API credentials embedded in client-side assets. Publishing it publicly lets anyone extract and misuse those keys. Revoke/rotate them immediately and replace this APK with a clean, secured build as soon as possible.

## Contact details
Official email and Google Maps link are already included. The official phone/WhatsApp number was not supplied, so the website shows a clear pending-confirmation label instead of inventing a number.

## Gallery
The large temple image is explicitly labelled a design visualization/reference, not a photograph of a completed structure.
