# gumdemo

Coming-soon page for **gumdemo** — the [vote 182](https://vote.kmikeym.com/k5m/questions/182) "do something dumb" mandate: $350 of gum, bought in one day in LA, demoed and reviewed solo and with guests.

**Live:** [gumdemo.pages.dev](https://gumdemo.pages.dev) (Cloudflare Pages). Custom domain `gumdemo.com` (Mike-owned, DNS at Hover) not yet attached.

## What's here

- `public/` — the deploy root (only these files ship).
  - `public/index.html` — self-contained static teaser page (inline CSS, Google Fonts via CDN, no build step).
  - `public/assets/coming-soon.jpg` — the hero art. Replace it to update the image; the page falls back to a styled dashed placeholder if it's ever missing.
- `README.md`, `.gitignore` — repo-only, never deployed (that's why `public/` is the deploy root).

## Aesthetic

extragum.com-inspired: deep signature green, soft "fresh" light orbs, a white **italic Hanken Grotesk** wordmark, the hero framed in a white product card, mint/watermelon accents, and a "Frequently Chewed Questions" accordion. Respects `prefers-reduced-motion`.

## Preview locally

```sh
cd /Users/kmikeym/Projects/gumdemo/public
python3 -m http.server 8080   # then open http://localhost:8080
```

## Deploy

Cloudflare Pages, **direct upload** (project `gumdemo`, account: KmikeyM / Quarterly Systems):

```sh
cd /Users/kmikeym/Projects/gumdemo
wrangler pages deploy public --project-name gumdemo --branch main
```

To attach `gumdemo.com` later: move the domain onto Cloudflare (swap nameservers at Hover), then add it as a custom domain on the `gumdemo` Pages project. Or switch the project to GitHub git-integration (like `k5m-bot-site`) for auto-deploy on push.

## Lane note

The bit, concept, and gumdemo.com architecture are **Thalberg's** production lane (see `K5M/Charlie/ch-gumdemo.md`). This teaser was scaffolded by Charlie on Mike's direct request as a fast first thing on the domain. Hand off to Thalberg for the real site.
