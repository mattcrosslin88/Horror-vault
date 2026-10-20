# Horror Vault — Streaming availability update

## What's new
- Adds a **Where to watch** section to movie cards, using TMDB's watch-provider endpoint for the United States.
- Shows provider logos grouped by subscription, free, ad-supported, rental, and purchase options when those listings are available.
- Provider logos link to the TMDB/JustWatch availability page. Listings are cached locally for 12 hours and refreshed when online.
- Keeps the existing TMDB search, movie details, chronological sorting, custom posters, local reviews, JSON backup/restore, and Reviews & Diary fix.

## Before publishing
1. Keep your latest JSON backup safe.
2. Open `index.html` and find `TMDB_ACCESS_TOKEN`. If the placeholder is still there, replace it with your existing TMDB Read Access Token before uploading. **Do not commit a token to a public repository unless you accept that it is publicly visible.**
3. Upload the extracted package contents to the root of your existing GitHub Pages repository, replacing the matching files and keeping the `icons/` folder. Commit to `main`.
4. Keep the same website address and do not clear browser site data.

## Notes
- Streaming listings depend on TMDB/JustWatch data and may be incomplete or change by location and date. This build defaults to the United States.
- Existing movies need a TMDB ID to look up providers. Movies added through **Search & Add Movie** get a TMDB ID automatically. Older manual entries show a **Find this movie** button. Use it to select the exact TMDB title/year and attach streaming availability without losing your existing review, personal rating, watched status, or date.
- TMDB's watch-provider data requires attribution to JustWatch.
- Movie data and custom posters remain in browser-local storage; continue to export JSON backups regularly.


## Streaming list display
The Where to watch section is now collapsed by default on each movie card. Tap the dropdown to reveal provider icons grouped by subscription, free, ad-supported, rental, and purchase options. It shows a compact provider count and preserves its open/closed state while availability refreshes.
