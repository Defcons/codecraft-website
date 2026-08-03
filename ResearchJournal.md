# agentas-website — Research Journal  (RETIRED)

_Append-only chronological history of a **retired** repo. The distilled truth is
in [`KnowledgeBase.md`](KnowledgeBase.md); the code index in
[`CodeMap.md`](CodeMap.md)._

_The triad: **CodeMap = the machine · KnowledgeBase = the model ·
ResearchJournal = the history.**_

_Last verified: 2026-08-03 @ c53eee0 (master) — reconstructed from `git log`
(48 commits)._

## Arc (2026-03-30 → retired 2026-07-30)

### 2026-03-30 — Born as Codecraft AS
Initial "Codecraft AS website" + a GitHub Actions auto-deploy workflow; early
theme-lightening and cache/deploy-pipeline verification churn.

### 2026-04 → 06 — Content build-out
AI-first repositioning; lighter navy/slate theme; a Founder section + concrete AI
project cards; real client imagery (Symra subsea, Nye SUS, E1 Oslo, Ivar Aasen,
Turfpal, Powerpal); "repositories are private, available on request";
contact-email obfuscation (assembled at runtime); a Frostwake hobby card
(reworded to drop the hobby framing); CI hardening (Tailscale deploy to a private
LXC, `set -euo pipefail`).

### 2026-07-08 — web.codecrafts.cc rebrand + cross-links
Real automation imagery, portfolio + dreadmark links, the web.codecrafts.cc
rebrand; portfolio link fixed to martindavidsen.cc; showcased the 6 live
web.codecrafts.cc templates on the Websites grid.

### 2026-07-12 — Last content commit
Dropped orphaned client-demo images; recorded the NPM 502 gotcha in CODE-MAP (a
502 on codecrafts.cc while the other subdomains stay 200 = the proxy's Websockets
toggle, not the container).

### 2026-07-30 — RETIRED
Site folded into **`agentas-sites/apex/`**; this repo/container ceased to be the
live source. (Recorded in CodeMap; no further content commits.)

### 2026-08-03 — Triad standardization (post-retirement bookkeeping)
CODE-MAP.md → CodeMap.md + repo flagged retired; this KB + Journal seeded to
complete the triad for the archive.

## For the next session
Do not develop here. The living site is `agentas-sites/apex/` — make changes
there. This repo is a historical snapshot of the Codecraft-branded predecessor.
