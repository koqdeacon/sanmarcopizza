# sanmarcopizza — public website (www.pizzasanmarco.org)

Plain static HTML on GitHub Pages: push to `main` and it is live in about a
minute. No build step, no framework. Domain via `CNAME`
(`www.pizzasanmarco.org`; DNS in Cloudflare).

## Pages
- `index.html` — landing page + walkthrough with screenshots from `shots/`
- `anleitung.html` — full guide, customer and owner tabs (`#owner` deep link)
- `privacy.html`, `terms.html`, `support.html` — linked from the App Store
  listing; keep them working
- `reset.html`, `email-changed.html`, `index_email_confirmed.html`,
  `stripe-connect.html` — redirect/landing pages used by the apps and
  Supabase/Stripe flows; don't rename or remove
- `style.css` — shared styles; `shots/README.md` — screenshot spec

## Conventions
- Bilingual DE/EN: translated elements carry `data-de` / `data-en` (HTML
  entity-escaped, set via `innerHTML`); guide articles have
  `[data-body="de"]` / `[data-body="en"]` blocks. Add both languages for
  every new text.
- Keep the guide's table of contents and article numbering in sync.
- **No Wine Tasting, alcohol or "18+" wording for now** — removed 2026-10 to
  match the App Store metadata after a Guideline 1.1 rejection.
- This is a hobby project: keep legal pages plain and honest, not formal.
- Verify after pushing: `curl -s https://www.pizzasanmarco.org/<page>`.
