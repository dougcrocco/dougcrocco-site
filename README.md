# dougcrocco.com

Static site. No build step — serve this folder as-is.

## Files
- index.html — the site (home, works, exhibits, news, info)
- works-data.js — catalogue: 70 works, 7 series, 24 exhibitions, 24 press notes, CV
- support.js — runtime the page loads
- staring-at-the-sun-review.html — rebuilt LA Times review, linked from that exhibit
- images/ — four locally stored images (two venue photos, two press screenshots)

## Artwork images
All other images load from https://allart.la/artwork/uploads/... mirroring the old
WordPress paths. Keep that host serving them, or copy the uploads tree in and swap
the base URL in works-data.js.

## Deploy
Contents go at the repo root. GitHub Pages: Settings → Pages → main / (root).
