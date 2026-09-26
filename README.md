# MAJÉ — Mahjong Scorer (PWA)

This is the publish-ready mobile web package for MAJÉ.

## Included

- `index.html` — production entry point containing the existing MAJÉ app
- `manifest.json` — installable PWA metadata
- `sw.js` — app-shell/service-worker caching
- `icons/icon-180.png` — Apple touch icon
- `icons/icon-192.png` — Android/PWA icon
- `icons/icon-512.png` — large PWA icon
- `vercel.json` — Vercel configuration
- `README.md` — deployment guide

## Preserved from the original app

- Existing UI/design and app logic
- Embedded MAJÉ logo
- `localStorage` game/history behavior
- Save Image functionality
- Share functionality
- Existing bilingual EN/ID language switcher

## Deploy to Vercel

### Easiest method: GitHub → Vercel

1. Create a new GitHub repository, for example `maje-mahjong-web`.
2. Upload all files in this folder, keeping the `icons` folder structure.
3. In Vercel, choose **Add New → Project**.
4. Import the GitHub repository.
5. Framework Preset: **Other** (or leave the detected/default option if Vercel detects it as static).
6. Build Command: leave empty.
7. Output Directory: leave empty.
8. Click **Deploy**.
9. Vercel will give you a free `*.vercel.app` URL.

Every time you update `index.html` or another project file and push the changes to GitHub, Vercel can automatically redeploy the updated version.

## Local test

Because service workers require a secure origin (HTTPS) or localhost, don't test the PWA by double-clicking `index.html` as a `file://` URL.

You can use any simple local HTTP server, then open the localhost URL in your browser.

## Updating the app

The main app is still in `index.html`. You can edit that file and push the changes to GitHub. Vercel will redeploy from the connected repository.

## Notes

The original app uses Tailwind via `https://cdn.tailwindcss.com`. The service worker includes that CDN resource in the app shell cache so it can remain available after it has been cached once. The app's embedded MAJÉ logo does not depend on an external image file.
