# dougcrocco.com

Static site — no build step. Put these files at the repo root.

## Files
- index.html — the site (home, works, exhibits, news, info)
- works-data.js — catalogue: works, series, 24 exhibitions, news, CV
- support.js — runtime the page loads
- staring-at-the-sun-review.html — rebuilt LA Times review
- images/ — images stored locally with the site

## Artwork images — one switch
Artwork paths are stored repo-relative (artwork/uploads/YYYY/MM/file.jpg) and are
prefixed at load time by one line at the top of works-data.js:

    window.IMG_BASE = window.IMG_BASE || 'https://allart.la/';

Today they load from allart.la. To host them here instead:
1. Copy the whole artwork/uploads/ tree from the WordPress host to the repo root,
   so the path becomes artwork/uploads/2019/05/... — include 2005/09, 2014/10,
   2018/09 and 2024/05 (those hold the eleven files currently 404ing).
2. Change that line to:

    window.IMG_BASE = window.IMG_BASE || '';

Nothing else changes.

## Deploy
GitHub Pages: Settings → Pages → main / (root).
