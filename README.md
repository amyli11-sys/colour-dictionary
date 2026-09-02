# Wada colours — home screen app

A standalone, installable web app for browsing Sanzo Wada's 348 colour
combinations by shade. Works offline once installed.

## Files

- `index.html` — the app (all 159 colours and combinations are embedded, no network needed)
- `manifest.json` — tells the phone how to install it (name, icon, colours)
- `sw.js` — service worker, caches the app so it works offline
- `icon-192.png` / `icon-512.png` — home screen icons

## 1. Host it (GitHub Pages, free)

1. Create a new GitHub repository (public is fine, e.g. `wada-colours`)
2. Upload all five files in this folder to the repository root
3. Go to the repo's **Settings → Pages**
4. Under "Build and deployment", set **Source: Deploy from a branch**,
   branch: `main`, folder: `/ (root)` — save
5. Wait a minute, then your app is live at:
   `https://<your-username>.github.io/wada-colours/`

(Netlify or Vercel also work if you prefer — just drag the folder into
their dashboard; no build step is needed since this is plain HTML/JS.)

## 2. Add to your home screen

**iOS (Safari):**
1. Open the hosted URL in Safari
2. Tap the Share icon → **Add to Home Screen**
3. Tap **Add** — you'll get an app icon that opens full-screen

**Android (Chrome):**
1. Open the hosted URL in Chrome
2. Tap the ⋮ menu → **Add to Home screen** (or you may see an automatic install prompt)
3. Tap **Add**

## Notes

- All colour data is baked into `index.html`, so once installed the app
  needs no internet connection to work.
- If you ever want to update the app, just re-upload a changed
  `index.html` to the repo — the service worker will pick up the new
  version next time it's opened with a connection.
- Data source: Sanzo Wada's *A Dictionary of Colour Combinations*
  (first edition), digitised by Dain M. Blodorn Kim and refined by
  Matt DesLauriers, MIT licensed.
