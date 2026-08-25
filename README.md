# U.S. Citizenship Test — Study Web App

A standalone web page — no build tools, no server code, no login required.
Everything (progress, XP, custom questions, your preferred answers, your
"need more practice" list) is saved right on your device using the browser's
local storage.

## What's new in this version

- ❌ Voice mode removed
- 💾 No login — progress auto-saves to your device
- ✏️ **Add your own custom questions** (Manage → My Questions)
- 📝 **Edit any official answer** to a phrasing that's easier for you to
  remember (Manage → Edit Answers) — used in both Writing mode and Learn mode
- 🚩 **Need More Practice list** — any question you get wrong is automatically
  flagged; get it right once to clear it, or manage it by hand
  (Manage → Practice List). A dedicated card appears on the home screen
  whenever you have flagged questions.

## How to run it right now

You don't need to install anything. Just open `index.html` in a browser:

- **On a computer:** double-click `index.html`, or drag it into Chrome/Edge/Safari.
- **Quick local server (optional, avoids some browser file:// restrictions):**
  ```
  cd webapp
  python3 -m http.server 8000
  ```
  then visit `http://localhost:8000` on the same device.

Internet is required the first time you load the page (it pulls React from a
CDN) — after that, the service worker caches everything for offline use.

## How to install it as an app (PWA)

Once it's hosted somewhere reachable (see below), open the page in:

- **Android (Chrome):** tap the ⋮ menu → "Add to Home screen" / "Install app".
- **iPhone/iPad (Safari):** tap the Share icon → "Add to Home Screen".
- **Windows/Mac (Chrome or Edge):** click the install icon (⊕) in the address bar,
  or menu → "Install [app name]".

It will then behave like a native app — its own icon, full-screen, works offline.

## How to host it for free (so you can install it from any device)

Any static file host works. Two easy options:

**Option A — Netlify Drop (no account needed)**
1. Go to https://app.netlify.com/drop
2. Drag the whole `webapp` folder onto the page
3. You get a live URL instantly — open it on your phone to install

**Option B — GitHub Pages**
1. Create a new GitHub repo
2. Upload all files in `webapp/` to the repo root
3. Settings → Pages → deploy from the `main` branch
4. Your app will be live at `https://<username>.github.io/<repo>/`

## Files in this package

- `index.html` — the app shell (loads React/Babel from CDN, mounts the app)
- `app.jsx` — all app logic and UI (readable JSX, no build step required)
- `manifest.json` — PWA metadata (name, icons, colors)
- `sw.js` — service worker for offline caching
- `icon-192.png`, `icon-512.png` — app icons (from your brand kit)

## Notes for future changes

- All quiz data (the 100 official questions, lesson groupings, keyword lists,
  and Learn-mode tips) lives near the top of `app.jsx`.
- To change colors, search for the hex codes used throughout `app.jsx`
  (e.g. `#58CC02` green, `#FF9F00` amber, `#CE82FF` purple, `#FF4B4B` red).
- Since this is plain JSX read by Babel in the browser, you can edit
  `app.jsx` directly in any text editor and refresh the page to see changes —
  no npm install, no build step.
