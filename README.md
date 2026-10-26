# Poke Stick Studio — v0.1.2

A buildless, responsive static studio website for GitHub Pages. HTML5, CSS3, original SVG studio favicon and existing Popposite branding. No JavaScript, dependencies, tracking, remote fonts, cookies, or build step.

## Files

- `index.html`: studio homepage and contact.
- `games/popposite.html`: game overview and real Unity Editor screenshot gallery.
- `privacy/popposite.html`: public, pre-release privacy policy.
- `assets/style.css`, `assets/favicon.svg`: shared original presentation.
- `assets/screenshots/`: JPEG web copies of pre-release Unity Editor captures, with full-size image links.
- `.nojekyll`: bypass Jekyll processing.
- `PokeStickStudio-v0.1.0-report.md`: implementation, verification, and developer review list.

## GitHub Pages deployment

The files in this directory belong at the root of the existing `MariusDirda/PokeStickStudio` repository. Do not place the directory itself inside another `PokeStickStudio` directory.

1. Open the repository **Settings → Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Choose **main** and **/ (root)**, then **Save**.
4. Wait for the **pages build and deployment** workflow to complete.
5. Open `https://mariusdirda.github.io/PokeStickStudio/` in a signed-out browser.
6. Verify `https://mariusdirda.github.io/PokeStickStudio/privacy/popposite.html` loads without authentication before using that URL in Google Play Console.

All local navigation/assets use relative paths and support `/PokeStickStudio/`. Canonical and Open Graph URLs target the expected Pages URL. Update these metadata URLs if the host or domain changes.

The GitHub connector can write repository files but has no Pages-settings mutation tool. Publishing the repository does not by itself enable Pages. The settings steps above may need to be completed by the repository owner.

## Local preview

No server is needed for basic navigation: open `index.html`. To test the production base path, serve the parent of the repository directory on localhost and open `/PokeStickStudio/`. For example, from the parent directory with Python installed:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Then open `http://127.0.0.1:8000/PokeStickStudio/`. The repository folder must be named `PokeStickStudio` for that exact path.

## Branding

`assets/branding/` contains resized web copies of the existing Popposite logo and Android launcher artwork. These are used on the studio homepage and game page. No new artwork was generated. The studio favicon remains distinct from the game branding.

## Before the game launches

Review every explicitly marked item in the privacy policy and the versioned report. In particular, confirm the release advertising configuration, target age audience, legal operator details, distribution regions, and support email retention period. The reviewed Unity configuration disables production ad requests and Firebase Analytics. Re-review after changing SDK settings or enabling production ads. No Unity source, identifiers, configuration, player saves, or credentials belong in this repository.

The gallery contains real Unity Editor UI captures from isolated presentation fixtures, not physical Android captures or claims about particular campaign outcomes. See the v0.1.1 report for provenance. Refresh these with new release captures when the UI changes. Keep the Google Play button disabled until a real public store listing exists, then use its verified URL. Preserve reduced-motion support and keyboard navigation when editing.
