# Feed the Owl — installable PWA

A standalone home-screen app. Saves progress on your phone (localStorage), works offline. No backend, no accounts, no cost.

## Files
- `index.html` — the whole app
- `manifest.webmanifest` — makes it installable (name, icon, standalone)
- `sw.js` — service worker, caches the app so it opens offline
- `icons/` — app icons

## Put it online (GitHub Pages)
A PWA must be served over **https** for install + offline to work. GitHub Pages does this for free.

1. Create a repo, e.g. `feed-the-owl` (public).
2. Upload all these files, keeping the `icons/` folder.
3. Repo **Settings → Pages → Source: Deploy from a branch → main → / (root) → Save**.
4. Wait ~1 min. Your app is at `https://<your-username>.github.io/feed-the-owl/`.

## Install on your phone
- **iPhone (Safari):** open the URL → Share → **Add to Home Screen**.
- **Android (Chrome):** open the URL → tap the **📲 Install app** button, or menu → **Add to Home Screen / Install app**.

It then opens fullscreen like a native app, with its own icon.

## Notes
- All data lives on the device it was installed on. Uninstalling / clearing site data wipes progress.
- To update the app later: change the files, and bump the version in `sw.js` (`feed-the-owl-v1` → `v2`) so phones fetch the new version.
