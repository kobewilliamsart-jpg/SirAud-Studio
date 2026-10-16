# SirAud-Studio v1.2 (open source, offline PWA)

Text-to-speech studio with a Voice lab (voice matching) and an audio editor. No API key. Works offline after setup.

## Deploy (important)
Upload the WHOLE folder, not only index.html:
- Netlify: drag and drop the entire `siraud-studio-pwa` folder onto your site's Deploys page (or `netlify deploy --dir=. --prod`).
- Any static host (GitHub Pages, etc.): upload all files and folders, keeping the structure.
Required next to index.html: `vendor/` (speech engine), `fonts/`, `icons/`, `manifest.json`, `sw.js`.
(If `vendor/` is missing, the app tries to load the engine from jsDelivr, which needs internet and is slower to set up.)

## First use (needs internet once)
1. Open the app, read and accept the legal conditions (shown at every install, update and reinstall).
2. Open **Voices & resources** (box icon) and press **Save engine for offline use**.
3. Download a voice for your language (about 60 MB each). Voices are stored on your device.

## Install as an app
Chrome/Edge/Android: use the Install button (or the browser menu). iPhone: Share, then Add to Home Screen.

## Voice lab
Record or upload 10 to 30 s of clear speech, install a few voices, then press Extract and match.

See LICENSES.md for third-party licenses.
