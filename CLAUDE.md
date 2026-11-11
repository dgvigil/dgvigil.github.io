# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Personal blog for Dave Vigil, served at dgvigil.github.io via GitHub Pages. Jekyll site based on the "Jekyll Now" theme (barryclark). No CI workflow; GitHub Pages builds on push to `main`. Dependabot bumps gems via PRs.

## Commands

Ruby 3.3.3 (`.ruby-version`). Uses the `github-pages` gem, so plugin/version set is pinned to what GitHub Pages supports.

```sh
bundle install
bundle exec jekyll serve          # dev server at http://localhost:4000, rebuilds on change (restart after _config.yml edits)
bundle exec jekyll build          # output to _site/ (gitignored)
```

No test suite or linter. Verify by building and viewing the page.

## Architecture

- `_config.yml`: site metadata, footer social links, `permalink: /:title/`, kramdown (GFM) + rouge highlighting, plugin list (jekyll-feed, sitemap, redirect-from, mentions, jemoji, github-metadata). `google_analytics` only renders when `jekyll.environment == 'production'`. Edits here need a server restart.
- Layouts: `default.html` (shell, includes `meta.html`, analytics, footer) -> `page.html` / `post.html`. `index.html` lists all posts with excerpts.
- `style.scss` (root, has front matter) imports partials from `_sass/` (`_variables`, `_reset`, `_highlights`, `_svg-icons`). Compiled to `/style.css`.
- Posts in `_posts/YYYY-MM-DD-title.md`. Some posts embed large pre-rendered HTML (charts/notebooks) from `_includes/` via `{% include ... %}` (e.g. `NLP_and_Baseball_HOF.html`, `Houston_Astros_fans.html`, `man_on_second.html`, `keyboad-layout.html` [sic]). Match existing filenames exactly.
- `images/` holds post assets (including PDFs and a .MOV); reference as `/images/...`.
- `CNAME` and `README.md` are in the `exclude` list; add new non-site files there too.
