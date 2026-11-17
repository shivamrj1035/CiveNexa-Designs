# CiveNexa Designs

Personal design-sharing site for Civenexa product designs and clickable prototypes, published with GitHub Pages.

Live site (after Pages is enabled): https://shivamrj1035.github.io/CiveNexa-Designs/

## What is here

| Path | Purpose |
| --- | --- |
| `index.html` | Gallery. Reads `designs.json`, groups designs by module, no build step. |
| `designs.json` | Registry of every design shown on the gallery. |
| `designs/<design-id>/` | One folder per design (self-contained HTML plus any images/PDFs). |
| `designs/_template/` | Starter page with Civenexa brand tokens. |
| `.nojekyll` | Tells GitHub Pages to serve files as they are. |

## Current designs

- `designs/provider-onboarding/`: service provider onboarding prototype (tap through, or open with `?walkthrough` to watch it run automatically; add `&persona=2` for the individual-plumber scenario) and the flow map.

## Add a new design

1. Copy `designs/_template/` to `designs/<module>-<name>/` (for example `designs/customer-booking/`).
2. Build the page. Keep it self-contained (inline CSS and JS) so it also works as a single file shared over email or WhatsApp.
3. Add an entry to `designs.json`: `id`, `title`, `module` (used for the filter chips, for example "Service Provider", "Customer", "Admin"), `domain`, `kind`, `status`, `updated`, `description`, optional `thumb`, and `links`.
4. Commit and push. Pages updates within a minute or two.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Publish with GitHub Pages (one time)

1. Push this folder to `main` of `shivamrj1035/CiveNexa-Designs`.
2. On GitHub: Settings → Pages → Build and deployment → Source: "Deploy from a branch" → Branch: `main`, folder `/ (root)` → Save.
3. Wait about a minute, then open the live site URL above.

Note: GitHub Pages on a free account needs the repository to be public. Anyone with the link can open the designs.
