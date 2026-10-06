# photocraft-pages

Deploys the web (wasm) build of [PhotoCraft](https://github.com/storytold/photocraft) to GitHub Pages.

The workflow `.github/workflows/deploy.yml`:

1. Finds the newest published release of `storytold/photocraft` that ships a `photocraft-web-*.zip` (or the tag you pass when running it by hand).
2. Downloads the zip, checks it against `SHA256SUMS.txt`, and unpacks it.
3. Publishes it to GitHub Pages, with a `version.txt` holding the deployed tag.

It runs every 6 hours and only deploys when a new release is out. You can also run it by hand from the Actions tab ("Run workflow"), optionally with a specific tag or `force`.

## Setup (once)

Settings → Pages → Build and deployment → Source: **GitHub Actions**.
