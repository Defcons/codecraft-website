# agentas-website — Knowledge Base  (RETIRED)

_The distilled truth about a **retired** repo. The code index is
[`CodeMap.md`](CodeMap.md); the history is [`ResearchJournal.md`](ResearchJournal.md)._

_The triad: **CodeMap = the machine · KnowledgeBase = the model ·
ResearchJournal = the history.**_

_Last verified: 2026-08-03 @ c53eee0 (master) — retirement confirmed against
CodeMap + the live successor `../agentas-sites/apex/` (present)._

## Status: RETIRED (2026-07-30)
- **[FACT]** This repo is **no longer the live source.** Its site was **folded
  into `agentas-sites/apex/`** on 2026-07-30; that `apex/` dir now serves the
  apex company domain on its container. This repo/container is kept for history
  only. The sibling `C:\Dev\agentas\agentas-sites` (with `apex/`) is confirmed
  present as the successor.
- **[FACT]** It is **frozen pre-rebrand**: its own `index.html` still reads
  **"Codecraft AS — Software & Automation Engineering"** (confirmed). The company
  later rebranded **Codecraft → Agentas**, and that live rebrand happened in
  agentas-sites, not here — which is why the working folder is named
  `agentas-website` while the content + `CodeMap.md` still self-identify as
  `codecraft-website`.

## What it was
- **[FACT]** Single-page **marketing site for Codecraft AS**
  (codecraft.cc / codecrafts.cc). Static hand-written `index.html` + `styles.css`
  + `script.js`, served by nginx in a container; deploy was push-`master` →
  GitHub Actions → server.
- **[FACT]** **Positioning:** AI-first — it led with AI-engineering as the core
  offering, backed by ~8 years of industrial/subsea automation delivery as the
  credibility foundation (AI the method, automation the proof).
- **[FACT]** It shared the pattern the surviving sites still use: bilingual EN/NO
  `data-en`/`data-no` `textContent` swap (`localStorage['cc-lang']`), `initModal`
  project modals, IntersectionObserver scroll reveals, and a base64-assembled
  contact email. Full mechanics remain in [`CodeMap.md`](CodeMap.md).

## Where it lives now
- **[FACT]** Live successor: **`agentas-sites/apex/`** (see that repo's own triad
  docs). The `*.codecrafts.cc` subdomain sites are the separate `codecrafts-sites`
  container. Do NOT resurrect this repo as a live source.
