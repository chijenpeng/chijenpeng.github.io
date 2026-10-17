# chijenpeng.github.io

Personal website, hosted on GitHub Pages. The layout is a small custom Jekyll theme styled after an audio plug-in UI (no JavaScript) (originally forked from the [Academic Pages](https://github.com/academicpages/academicpages.github.io) template, MIT, see `LICENSE`; none of its layouts remain).

## Where things are

- `_layouts/default.html` — the single page skeleton: head, header, `<main>`. There is no footer.
- `_includes/` — `head.html` (meta, fonts, CSS, favicons), `header.html` (site title and nav), `seo.html` (title, description, canonical, Open Graph), `base_path`.
- `_sass/site.scss` — all of the CSS. `assets/css/main.scss` only imports it.
- `_data/navigation.yml` — the top nav. Each item has `title` and `url`, and optionally `new_tab` and `separator` (draws the rule before the item).
- `_pages/` — `about.md` (home, `/`), `music.md`, `plugins.md`, `404.md`, and `cv.md` (redirects `/cv/` and `/resume` to the PDF). Pages hold raw HTML wrapped in `{::nomarkdown}`.
- `files/cv.pdf` — the CV. The nav's CV link opens it directly. To update, copy the new PDF over it (source lives in the separate `resume` repo).
- `images/` — `profile.jpg`, `plugins/` screenshots, favicons (`favicon.svg` is the source for the PNGs), `manifest.json`.
- `_config.yml` — site name, description and author details.
- `resume.tex` (old resume source) is gitignored and never published.

## Deploy

Push to `main`. GitHub Pages builds the site automatically; it appears at https://chijenpeng.github.io within a minute or two.

## Preview locally (optional)

Needs Ruby 3.x (e.g. `brew install ruby`).

```sh
bundle install
bundle exec jekyll serve -l -H localhost
```

Then open http://localhost:4000. The site uses only the GitHub Pages plugins `jekyll-feed`, `jekyll-sitemap` and `jekyll-redirect-from`.
