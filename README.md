# talks

Public talks from [Værksted AI](https://maskin.io). Each deck is a single self-contained HTML file. Hosted at [talks.maskin.io](https://talks.maskin.io) via Cloudflare Pages — merging a PR to `main` deploys it live within a few minutes.

## Publishing a new deck

Three steps:

1. Drop the built HTML at `/talks/{slug}/index.html`. Slug format: `YYYY-MM-{format}-{topic}` — e.g. `2026-11-meetup-cph`.
2. Add a `<li class="talk">` entry to `/index.html` linking to the new slug (top of the list, newest first).
3. Open a PR against `main`. Cloudflare Pages will build a preview URL on the PR — verify the deck renders end-to-end there (all slides, keyboard nav, `n`-key notes overlay). Merge → live at `talks.maskin.io/{slug}/`.

That's it. No build step, no framework. Static files served from the repo root.

## Layout

```
/                          — landing page listing all published talks
/talks/{slug}/index.html   — one directory per deck
/README.md                 — this file
```

## Hosting

- **Cloudflare Pages** project connected to this repo. Build command: none. Output dir: `/`.
- Custom domain: `talks.maskin.io` (CNAME on the maskin.io DNS zone).
- Preview URLs auto-generated on every PR.

## Not in scope

- View analytics per deck (may add CF Web Analytics later).
- Auth / access control — all published talks are public. Gated decks would live elsewhere.
