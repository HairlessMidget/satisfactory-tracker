# Satisfactory Collectibles Tracker

Personal map app for tracking power slugs, mercer spheres, somersloops, and hard drives in Satisfactory. Click markers to mark them complete. Progress saves automatically in the browser.

## Files

- `satisfactory.html` — the app (self-contained, includes all node data)
- `satisfactory_map_bg.png` — map background image
- `manifest.json` — PWA manifest (for "Add to Home Screen")
- `sw.js` — service worker (offline support)
- `icon-192.png`, `icon-512.png` — app icons

All five must live in the same folder.

## Running it locally (desktop, no installation)

You can't just double-click `satisfactory.html` because browsers block service workers and some features on `file://`. The simplest fix is a one-line local server:

```
cd "C:\Users\arabo\OneDrive\Desktop\New folder (6)"
python -m http.server 8000
```

Then open http://localhost:8000/satisfactory.html in any browser.

## Hosting it (for tablet + friends)

Free option: **GitHub Pages**.

1. Make a free account at github.com if you don't have one
2. Create a new public repo (e.g. `satisfactory-tracker`)
3. Upload all 5 files via the web UI (no git needed)
4. Repo Settings → Pages → set Source to "main" branch, root folder, Save
5. Wait ~1 minute. You'll get a URL like:
   `https://YOURNAME.github.io/satisfactory-tracker/satisfactory.html`
6. Open that URL on your tablet, share with friends

## Installing on your Android tablet

1. Open the URL from above in Chrome
2. Three-dot menu → "Add to Home screen" or "Install app"
3. Confirm — you'll get an icon on your home screen
4. Launch from the icon: full-screen, no browser chrome, works offline after first load

## Sharing progress between devices

Progress is stored per-browser-per-device. To move it:

- **Export progress** button → saves a JSON file
- Send the file (Discord/email/Drive/etc.) to the other device
- **Import progress** button → loads it

Each device is independent. There's no automatic sync.

## Tips

- Toggle layers on/off in the sidebar to declutter
- "Hide completed" hides markers you've already grabbed
- Hover/tap markers for type, item name (for hard drives), and altitude
- "Reset all progress" wipes everything (with confirmation)
