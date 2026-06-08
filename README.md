# Migraine Journal

Personal migraine and sleep log PWA for one person. Optimized for fast iPhone logging during migraine symptoms.

Live app URL after GitHub Pages is enabled:

https://afaitz19.github.io/migrainesleeplogs/

## iPhone setup

1. Open the live app URL in Safari.
2. Tap Share.
3. Tap Add to Home Screen.
4. Use the Home Screen icon like an app.

Do not open the local `file://` HTML file on iPhone. iPhone Safari/PWA works much better from the GitHub Pages web URL.

## Backup

The app stores daily data in localStorage for fast offline use. Use Export to Files to save `migraine_data_YYYY-MM-DD.json` to iCloud Drive, then Import from Files on another device when needed.

There is no server, no login, and no fake automatic iCloud sync.

## GitHub Pages

This repository includes a static `index.html`, `.nojekyll`, and a GitHub Actions Pages workflow. If the live URL does not work yet, open repository Settings, then Pages, and set the source to GitHub Actions.

Deployment trigger: 2026-06-09.