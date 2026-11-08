# Aava website

Landing page for **Aava** — Every craft. One current.

- Live: https://aava.dev *(DNS pending)*
- GitHub Pages preview: https://martintondel02.github.io/aava-site/
- Main product repo: https://github.com/martintondel02/aava-cut
- Brand guide: https://github.com/martintondel02/aava-cut/blob/main/docs/BRAND.md

## Structure

```text
index.html        landing page
styles.css        brand styling, responsive layout
script.js         navigation, reveal, year
assets/           mark, lockup, app screenshot, fonts, OG image
```

## Local preview

```bash
python3 -m http.server 8080
# http://127.0.0.1:8080
```

## Deploy

The site is plain static HTML/CSS/JS. GitHub Pages serves the `main` branch at `/`.

```bash
git add .
git commit -m "feat: add Aava suite landing page"
git push
```

## Custom domain — aava.dev

When DNS is ready:

1. Add these records at the DNS provider:

| Type | Name | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `martintondel02.github.io` |

2. Add `aava.dev` under **Repo → Settings → Pages → Custom domain**.
3. Enable **Enforce HTTPS**.
4. Add a `CNAME` file containing `aava.dev` (GitHub can create it for you).

Until DNS is live, keep using the GitHub Pages preview URL. Do not add the CNAME file before DNS is ready or the preview will redirect to an unresolved domain.

## Updating downloads

Package cards link to the latest GitHub release:

`https://github.com/martintondel02/aava-cut/releases/latest`

The release page carries the current RPM, DEB, AppImage and `SHA256SUMS`.
