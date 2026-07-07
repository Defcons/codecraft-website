# CODE-MAP — codecraft-website

Single-page marketing site for **Codecraft AS** (codecraft.cc / codecrafts.cc).
Static: hand-written `index.html` + `styles.css` + `script.js`, served by nginx in a
container. Deploy = push to `master` → GitHub Actions → server (see `.github/`, `deploy/`).

_Last verified: 2026-07-07_

## Positioning
AI-first: the site leads with AI-engineering as the core offering, with 8 years of
industrial/subsea automation delivery as the credibility foundation (not the headline).
Keep that balance when editing copy — AI is the method, automation is the proof.

## Layout
- `index.html` — all content. Sections in order (each `<section id=…>`):
  `hero → about → founder → ai → services → projects → websites → contact → footer`.
  (AI & Innovation sits *above* Services/Track Record by design.) Section backgrounds
  alternate secondary/primary down the page — preserve alternation if you reorder.
- Services grid: cards 01–03 are AI services, 04–09 industrial automation.
- `styles.css` — design tokens in `:root` (dark theme; `--accent` blue, `--accent-secondary`
  cyan). Styles grouped by section with matching header comments. Mobile breakpoints at 1024/768/480.
- `script.js` — one IIFE. Key fns: `setLanguage` (EN/NO via `data-en`/`data-no` on every
  translatable node, persisted to `localStorage['cc-lang']`), `initModal`, `initScrollAnimations`
  (IntersectionObserver adds `.visible` to `.fade-in`), navbar/hamburger/contact-form handlers.
  Contact email is base64-assembled at runtime (kept out of source).

## Bilingual invariant
Every user-visible string carries BOTH `data-en` and `data-no`; `setLanguage` swaps
`textContent` on toggle. When adding content, always add both or it won't translate.

## Project modal (AI & Innovation + Websites)
- Any card with class `ai-card--modal` is clickable (mouse + Enter/Space) → opens `#projectModal`.
- `initModal` reads the clicked card's `data-*`: `data-shot`/`data-shot2` (images → main +
  thumbnail switcher), `data-link`/`data-link-label` (+ `data-link2…`) → gradient link buttons,
  `data-private="1"` → shows the "repository kept closed" note, and mirrors the card's `.ai-badge`
  (Live/Private/In dev) into the modal. Title/description are pulled from the card's `h3`/`p`.
- No screenshot for a card → modal hides its media block (CloudDrive, Vehicle Telemetry,
  Smart Home currently have none).

## Images
- `images/projects/` — card/modal screenshots, JPEG q82 (~1 MB total). Source-of-truth originals
  live in sibling repos (epoglogs → `../epoglogs-architecture/screenshots`, frostwake →
  `../../codecrafts-sites/frostwake/assets`, nobs → `../../gym-tracker/assets`,
  dreadmark → `../../dreadmark`, client demos → headless-captured from `../../client-sites/*`,
  homelab → captured from `../homelab-architecture`). Re-optimize with `sharp` (present in
  `../../gym-tracker/node_modules`).
- Bump `?v=N` on changed assets; `styles.css`/`script.js` are versioned in `index.html` head/foot.

## Gotchas
- Headless-Chrome `--screenshot` captures only the top viewport (no scroll); isolate a section
  by hiding siblings via injected CSS to screenshot it. `.fade-in` starts at opacity 0 — force
  `opacity:1` when capturing or cards render blank.
