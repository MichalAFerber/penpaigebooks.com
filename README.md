# penpaigebooks.com

The author links page for **Penelope Paige**, live at
<https://penpaigebooks.com>.

## What's here

Everything served is in `public/`:

- `index.html` — the links page.
- `404.html` — the not-found page.
- `pen_signature_tx.svg`, `bg.png` — the signature mark and background.
- `favicon.svg`, `favicon.ico`, `favicon-16.png`, `favicon-32.png`,
  `apple-touch-icon.png` — the icon set.
- `robots.txt`, `sitemap-index.xml`, `sitemap.xml` — the crawler files. The
  sitemap is hand-written: a new page needs its own `<url>` entry with a
  `lastmod`, and CI fails until it has one. Each indexable page also needs one
  `<link rel="canonical">` naming that same URL; a `noindex` page must carry none.
- `ads.txt`, `llms.txt`, `.well-known/security.txt` — the DEV-STANDARDS §11
  plumbing files. `security.txt` carries an `Expires:` date to renew before it
  passes.
- `_headers` — noindexes the `pages.dev` hosts, which serve the same pages.

## Deploying

`.github/workflows/deploy.yml` publishes `public/` to the Cloudflare Pages project
`penpaigebooks` (`wrangler pages deploy`) on every push to `main`, so a merge is a
production deploy. Pull requests are gated by the
`ci` workflow, which checks every HTML file parses, the sitemap lists every
indexable page, and each such page names its sitemap URL as its canonical.

## Deviations

- §1—Social meta MUST set `twitter:creator` = `@michalaferber`—Penelope Paige is a client's pen name, and the tag would publicly tie it to Michal's handle; the card names `@penpaigebooks` as `twitter:site` instead—2026-11-21—permanent

## License

MIT — see [`LICENSE`](./LICENSE).
