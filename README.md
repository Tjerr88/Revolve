# Revolve PWA

An installable, offline-ready version of Revolve for GitHub Pages.

## Publish with GitHub Pages

1. Create a new GitHub repository, for example `revolve`.
2. Upload **the contents of this folder** to the repository root.
3. Open **Settings → Pages** in GitHub.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then click **Save**.
6. GitHub will provide the public HTTPS address for the app.

## Install

- Open the GitHub Pages address in Chrome, Edge, or Safari.
- Use the always-visible **Install app** button in Revolve.
- If direct browser installation is unavailable, the same button shows device-specific instructions.
- On iPhone and iPad, installation is managed through **Share → Add to Home Screen**.

A service worker requires HTTPS or localhost. It cannot run when `index.html` is opened directly as a local file.

## Data

Sessions, loads, reps, rotations, and settings are stored locally in the browser. Nothing is sent to GitHub. Use **Settings → Export data** to create a backup.

## Files

- `index.html` — the complete Revolve app
- `manifest.webmanifest` — installation settings and app icons
- `service-worker.js` — offline cache
- `background-revolve.webp`, `header-revolve.webp`, and `logo-revolve.webp` — brand imagery
- `icon-*.png` — app icons

All files are intentionally placed in this single flat directory. Upload them together to the repository root.
