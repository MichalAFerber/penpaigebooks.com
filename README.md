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

## Deploying

Cloudflare Pages builds from `main` via the Git integration, publishing `public/`
— one deploy path, no Actions deploy step (§4). Pull requests are gated by the
`ci` workflow, which checks every HTML file parses.

## License

MIT — see [`LICENSE`](./LICENSE).
