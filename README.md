# Horror Vault — Review Diary Fix

This update fixes the Reviews & Diary section so it displays only movies where you have written a non-empty personal review. Marking a watchlist movie as Watched, adding a rating, or importing a plot synopsis will not by itself create a diary entry. The diary shows the user's own review text only.

## Publish to your existing GitHub Pages app
1. Keep a current JSON backup of your collection.
2. Extract this ZIP.
3. Upload the contents of this folder to the root of your existing `Horror-vault` repository, replacing matching files and preserving the `icons/` folder.
4. Commit to `main`; leave GitHub Pages publishing from `main` and `/(root)`.
5. Open the existing site at `https://mattcrosslin88.github.io/Horror-vault/` while online and refresh it so the updated service worker can install.

Keep the same site address and do not clear browser storage. Movie records, reviews, and custom poster data are stored separately from these static app files. Keep your JSON backup as a precaution.

## Privacy note
If you use a TMDB access token embedded in `index.html`, it is visible to anyone who can read the source of a public GitHub repository. Do not upload a real token to a public repository unless you accept that exposure.
