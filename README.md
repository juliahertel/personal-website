# julia-hertel.de

Static site, no build step. Open `index.html` (English) or `de/index.html` (German) in a browser to preview.

## Files
- `index.html`, `de/index.html`: the English and German home pages. Keep them in sync when you change content.
- `impressum.html`, `de/impressum.html`: legal notice and privacy notice (your own text; check it when something changes, e.g. hosting, contact data or job title).
- `404.html`, `favicon.svg`, `CNAME` (the custom domain for GitHub Pages).
- `assets/style.css`: all styling (dark theme, colours at the top of the file).
- `assets/fonts/`: Inter (SIL Open Font License, free to use and share), Latin subset, with the licence file.
- `assets/img/`: photos and figures. `assets/img/web/` holds the web-sized project images and publication thumbnails.
- `Julia-Hertel-CV.pdf`, `Julia-Hertel-Lebenslauf.pdf`: web versions of the CVs (without address and phone). They are created by `..\CV\build.bat`.

Papers are not hosted here. The "Get Paper" buttons link to the publishers' pages; a button without a link is shown as "Coming soon".

## Editing
- The pages are generated from one source script, so the easiest way to change text is to ask for the change. Edited by hand, change both language versions.
- Project entries: copy an `<article class="ev proj">` block. Role, partners and papers are inside `<details>`.
- Publications: copy a `<li class="pub">` block. The thumbnail is a 360 px square, shown at 112 px.
- Project image strips: each strip fills the text width at a height of 150 px. Prepare images at the aspect ratio that makes the widths add up, so nothing is stretched or cropped much.
- Hero keywords: the `<ul class="kw">` list in the hero section.

## Publishing (GitHub Pages)
1. Create a public repository on GitHub and upload everything in this folder, including the `CNAME` file.
2. Settings > Pages: source = "Deploy from a branch", branch `main`, folder `/ (root)`. Custom domain = `julia-hertel.de`.
3. At IONOS remove old A/AAAA records for the domain, then set four `A` records for `@` (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) and a `CNAME` for `www` pointing to `<your-github-username>.github.io`.
4. When the DNS check is green, tick "Enforce HTTPS".
5. After going live, check both language versions, the Impressum link, the paper links and the CV downloads.
