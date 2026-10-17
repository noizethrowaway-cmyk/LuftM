# LuftM PWA

Static, dependency-free web app: `index.html`, `manifest.webmanifest`, `sw.js`, `icons/`. No build step.

## Deploy on GitHub Pages
1. Create a repository (e.g. `luftm`) and upload **the contents of this folder** to the repo root (so `index.html` is at the top level).
2. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder `/ (root)`. Save.
3. After a minute the site is live at `https://<your-username>.github.io/luftm/` (HTTPS, required for install and location).
4. Open it on your phone: Chrome/Edge menu → **Install app / Add to Home screen**; Safari (iOS) Share → **Add to Home Screen**.

All paths are relative, so it works under a repo subpath. To update, commit changes and bump `C='luftm-v1'` in `sw.js`.

## Other free hosts
Cloudflare Pages (unlimited bandwidth, easiest drag-and-drop upload), Netlify (drag-and-drop folder), Vercel. All serve HTTPS; no config needed.

## Differences from the Android app
- No background reminders: web apps can't schedule notifications without a push server, so this version is open-the-app advice only.
- Location is the browser's approximate one-shot lookup (permission asked only when you tap the button).
- Settings and the last forecast are kept in the browser's localStorage on your device.
- Times use the phone's time zone.
- Weather data by Open-Meteo.com; review https://open-meteo.com/en/license (free tier is non-commercial).
