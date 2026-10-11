# Horror Vault — Android-installable PWA

This package wraps the existing Horror Vault app as a Progressive Web App (PWA).

## Included
- `index.html` — the existing interactive Horror Vault app
- `manifest.webmanifest` — install name, theme, and app icons
- `service-worker.js` — caches the app shell for offline launching
- `icons/` — Android/app icons

## Important data notes
- Your movie collection, watched statuses, categories, reviews, and notes remain in browser local storage on this device/browser.
- The app shell is cached for offline launching. Wikipedia summary/poster lookups require an internet connection; externally hosted artwork may not always appear offline.
- Use Horror Vault's JSON Backup control regularly. Clearing Chrome site data or uninstalling/resetting browser data can erase local storage.
- Installing this PWA on a different device does not automatically transfer the movie list. Import/migration is not currently automatic; use the app's JSON backup as your safety copy.

## Publish securely with GitHub Pages (free)
1. On a computer, sign in to GitHub and create a **new public repository** named `horror-vault` (a public repo is required for free GitHub Pages on the standard free plan).
2. Upload the contents of this folder to the repository root. The root should contain `index.html`, `manifest.webmanifest`, `service-worker.js`, and the `icons` folder. Do not upload only the ZIP.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.
5. Wait for GitHub Pages to finish publishing. Your URL will look like `https://YOUR-USERNAME.github.io/horror-vault/`. Use the exact URL GitHub shows.
6. Open that HTTPS URL in Chrome on your Android phone and wait for the app to load once while online.
7. In Chrome, tap **⋮ → Install app** (or **Add to Home screen**, depending on the version) and confirm.
8. Open Horror Vault from the new home-screen icon. Visit it online once after future app updates so the cached app shell can refresh.

## Before relying on it
- Open the published URL and verify the library loads.
- Export a JSON backup from the app.
- Try airplane mode after the first online load to confirm the shell launches. Online poster/synopsis lookup will not work in airplane mode.
