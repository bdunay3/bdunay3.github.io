# bdunay3.github.io

The home page for my apps, served by GitHub Pages at <https://bdunay3.github.io/>.

It's plain HTML and CSS with no build step. Every page shares `assets/css/site.css`.

## Layout

```
index.html                          Home page, lists every app
assets/css/site.css                 Shared styles (light and dark)
apps/<app-name>/index.html          An app's page
apps/<app-name>/privacy/index.html  That app's privacy policy
```

Links between pages are relative (for example `../../assets/css/site.css`), so the pages also work
when opened straight from disk.

## Adding an app

1. Copy `apps/tcg-collector/` to `apps/<new-app>/` and rewrite both pages for the new app.
2. Add a list item for it under **Apps** in `index.html`, and a link in each page's `<nav>`.
3. Preview locally with `python3 -m http.server` and open <http://localhost:8000/>.

`.nojekyll` tells GitHub Pages to serve the files as they are, without running Jekyll.
