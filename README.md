# El Warda — optimized static build (GitHub Pages)

Structure
- `index.html`   inline critical CSS + markup (≈50 KB raw / ≈14 KB gzip), static age gate
- `js/app.js`    all page scripts, loaded with `defer` (≈24 KB gzip)
- `assets/`      WebP images (logo, 11 flavor fronts, 4 size cut-outs, side texture) — loaded on demand
- root files     favicon.ico, apple-touch-icon.png, icon-192/512.png, og-image.png, robots.txt, sitemap.xml, .nojekyll

Deploy on GitHub Pages (repo `m-eid-ss/Elwarda`)
1. Delete the old `index.html` in the repo.
2. Upload everything in this folder (keep the folder names `js/` and `assets/`) to the repo root.
3. Settings → Pages → Branch `main` / root. Wait ~1 minute, then hard-refresh.
All paths are relative, so the site works under `/Elwarda/`.

Local test:  `python3 -m http.server 8000`  →  http://localhost:8000
Self-check panel: open the page with `#debug` at the end of the URL.

Not done in code (see report): self-hosting Google Fonts (needs the .woff2 files), cache headers (GitHub Pages fixes them to 10 min).
