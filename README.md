# Horror Vault — Android PWA

This package is a separate updated copy based on the existing Horror Vault HTML file.

## Added
- **Chronological movie lists:** all movie grids sort by release year, oldest to newest; unknown years appear at the end, with titles alphabetized within the same year.
- **No Wikipedia lookups:** the app no longer automatically fetches film descriptions or poster images from Wikipedia.
- **Google Search shortcuts:** each movie card includes Google film-info and Google Images searches with the title and release year. Review results yourself, then add synopsis/notes through Edit or save a poster image to your phone and use Change poster.
- **Change poster** on each movie card. Pick an image saved on your phone.
- Posters are resized and stored in IndexedDB on the device, so they can display offline after the app has loaded and cached its shell.
- Backup exports movie data and custom posters.
- Restore imports new backups and older JSON backups that contain only movie data.
- PWA manifest, icons, and service worker for installation and app-shell caching.

## Publish
1. Keep your downloaded JSON backup safe.
2. Extract this ZIP.
3. Upload the contents of this folder to the root of the existing GitHub repository, replacing `index.html` and adding/replacing `manifest.webmanifest`, `service-worker.js`, and `icons/`. Keep the same repository and website URL.
4. Commit to `main`; wait for GitHub Pages to deploy.
5. Open the same GitHub Pages URL in Chrome, refresh, and choose Install app or Add to Home screen.

## Data safety
This update does not automatically copy data between different origins or browsers. Updating the existing GitHub Pages site at the same origin should preserve its local browser storage, but keep your JSON backup. Restore replaces the current movie list, so back up before restoring. Poster images are stored in IndexedDB and included in new JSON backups. Clearing browser/site storage or uninstalling can still remove local data.


Google Search note: a static GitHub Pages app cannot reliably scrape Google's results as a data API. This version opens targeted Google Search/Google Images results instead of automatically importing unverified descriptions or images. Google results require internet access; manually saved movie notes and custom posters remain local and work offline after caching.
