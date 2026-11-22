# CapsheetWebsite

Static one-page site for Capsheet (closeout audits for California subcontractors). No build step; the only script is the Calendly embed.

- `index.html` — the page
- `styles.css` — base styles and palette (light and dark, responsive)
- `modern.css` — the visual layer (shadows, dark pricing band, entrance). Remove its `<link>` to fall back to the flat look.
- `assets/` — Capsheet mark, wordmark, lockup and favicons

## Deploy

Any static host works. Fastest options:

- **GitHub Pages:** repo Settings → Pages → Deploy from branch → `main` / root. Add a `CNAME` file containing your domain, then point the domain's DNS at GitHub Pages (A records `185.199.108–111.153`, or a CNAME to `<user>.github.io`).
- **Netlify / Vercel / Cloudflare Pages:** connect the repo, no build command, output directory `/`.

`CNAME` holds the custom domain. Only one GitHub repo can claim a domain, so it must not match the old closeout-website repo.

## Editing

Numbers in the sample ledger come from `closeout-cash/04_mock_report/job_ledger_apex.csv`. If the mock report changes, update the table by hand; it's five rows.

No prices on the page (removed Nov 16). The fee section says only: flat fee set by revenue, quoted on the first call, 10× refund, optional monthly tracking. The price list lives in the project context doc, not here.
