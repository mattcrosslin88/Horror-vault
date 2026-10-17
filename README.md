# Horror Vault — TMDB Search Integration

This package adds a **Search & Add Movie** workflow to the existing Horror Vault PWA. It keeps chronological sorting, custom posters, local collection storage, JSON backup/restore, and offline shell support.

## Search workflow
1. Open Horror Vault and tap **Search & Add Movie**.
2. Before publishing, open `index.html` and find `const TMDB_ACCESS_TOKEN = 'PASTE_YOUR_TMDB_READ_ACCESS_TOKEN_HERE';`. Replace the placeholder text inside the quotes with your TMDB API Read Access Token. Do not include extra quotes. After publishing, search works automatically with no token prompt.
3. Search for a title, compare poster/year/overview, and select the exact film.
4. Tap **Use this movie** to prefill the existing Add Movie form. Review it and save.

TMDB provides the audience rating and vote count shown here. It does not provide a critics score; the app leaves that as an optional field for a verified separate source. This product uses the TMDB API but is not endorsed or certified by TMDB.

## Publish to the existing GitHub Pages site
1. Keep your current JSON backup safe.
2. Upload the contents of this folder into the root of the existing `Horror-vault` repository, replacing the matching app files. The root must contain `index.html`, `manifest.webmanifest`, `service-worker.js`, and `icons/`.
3. In GitHub Pages, keep `main` and `/(root)` selected.
4. Commit changes and wait for the Pages deployment to finish.
5. Open the same URL: `https://mattcrosslin88.github.io/Horror-vault/`.

## Token privacy
- This convenience version embeds the token directly in `index.html`. If your GitHub repository is public, anyone can view and copy it. Hiding the field in the app does not hide the token from the source code.
- Only use this if you accept that exposure risk. If the token is exposed or misused, revoke/rotate it in TMDB.
- The token is not included in JSON movie backups.

## Data safety
- Existing movie records are kept in browser local storage under `horrorVaultData`; updates at the same origin should preserve them.
- Custom posters remain in IndexedDB and are not erased by this code update.
- Importing a backup replaces current movie records, so only restore when needed.
- Do not clear browser site data or change the website origin. Keep making JSON backups.
- TMDB posters are cached locally when the browser permits image download; if not, the poster can still display online and a custom poster can be added manually.
- Automatic Wikipedia lookups have been removed.
