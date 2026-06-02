# gumdemo

Coming-soon page for **gumdemo** — the [vote 182](https://vote.kmikeym.com/k5m/questions/182) "do something dumb" mandate: $350 of gum, bought in one day in LA, demoed and reviewed solo and with guests.

Live domain: [gumdemo.com](https://gumdemo.com) (Mike-owned).

## What's here

- `index.html` — self-contained static teaser page (inline CSS, Google Fonts via CDN, no build step).
- `assets/coming-soon.png` — **drop your generated coming-soon art here.** Until it exists, the page shows a styled dashed placeholder so it never looks broken.

## Aesthetic

"Bubblegum retail." Warm-cream paper, floating gumballs, a fat **Bagel Fat One** wordmark, **DM Mono** body (receipt/inventory feel — ties to the $350-of-receipts bit), and a price-sticker "COMING SOON" badge. Respects `prefers-reduced-motion`.

## Preview locally

```sh
cd /Users/kmikeym/Projects/gumdemo
python3 -m http.server 8080   # then open http://localhost:8080
```

## Deploy

Static — drops onto Cloudflare Pages (same pattern as `kmikeym/k5m-bot-site`). Point the `gumdemo.com` Pages project at this repo's root; no build command, output dir `/`.

## Lane note

The bit, concept, and gumdemo.com architecture are **Thalberg's** production lane (see `K5M/Charlie/ch-gumdemo.md`). This teaser was scaffolded by Charlie on Mike's direct request as a fast first thing on the domain. Hand off to Thalberg for the real site.
