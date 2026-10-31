# Newspapers.com trial kit — Decipher clue-column hunt (2026-10-31)

Purpose: recover the **monthly clue columns (1987–1991)** that Decipher, Inc. released
to the hotline *and* "to the media and to retailers", which progressively eliminated
author names. Finding even two or three collapses the 33-author pool to a handful per
message (`docs/decipher-iii.md`). This is the only known mechanism that can change the
Decipher outcome; everything else is edition-bound book screening.

**Read this whole page before paying for anything.** The kit is ordered so that the
cheap falsification test runs first and can stop the spend.

---

## 0. Before you pay: two checks that can make the purchase unnecessary

1. **Library route first — but verify the package, it is a different product.**
   *Newspapers.com Library Edition* is distributed by **ProQuest**, not by
   Newspapers.com: 4,000+ titles, licensed to libraries in **packages** (World
   Collection, multi-state, or state-level e.g. "Texas Edition"). Two consequences:
   - Coverage depends on which package *your* library bought. Confirm it includes
     Virginia, Texas, Oregon, Tennessee and Wisconsin before relying on it (§1 lists
     the five papers we need).
   - You log in through the **library's database portal**, not a Newspapers.com
     account, so the search interface and clipping tools differ from the consumer site.
   - Whether Library Edition includes **Publisher Extra** titles is unconfirmed — and
     the one concrete lead we hold (§0.2) *is* a Publisher Extra page. The free route
     may not reach it.
   Still zero cost, so check your library's A–Z database list first; just don't assume
   it substitutes for a consumer trial. (`docs/sources.md` lists it as the cheapest path.)
2. **Tier check.** The one concrete live lead — `newspapers.com/newspage/640735315`
   (Fort Worth Star-Telegram, Sun 1988-04-24, p. 523) — is a **Publisher Extra** page,
   the paid add-on tier. Open that exact URL while logged in on a trial and confirm it
   renders *before* committing to anything beyond the trial. A basic-tier subscription
   may not unlock the single page we already know is a hit.

## 1. The calibration test (run FIRST, ~30–45 min) — the stop/go gate

These items are **known to exist** (cited in Baldwin & Sherman 1990 p. 283, or held as
scans in Karen's Drive archive). They are the ground truth for whether this archive can
find Decipher content at all. Holdings verified on newspapers.com 2026-10-31:

| # | Paper | newspapers.com | Coverage | Date | What |
|---|---|---|---|---|---|
| 1 | Virginian-Pilot (Norfolk VA) | id **30397** | 1899–2026, 686,051 pp | 1985-04-17 p.D6 | "Puzzle players decipher cryptogram" (Bryant) |
| 2 | Statesman Journal (Salem OR) | id **3746** | 1869–2026, 1,536,608 pp | 1986-03-25 pp.1–2 | "Decipher II game pays off in cold cash" (Forstrom) — 2-1 Novak |
| 3 | The Leaf-Chronicle (Clarksville TN) | id **3763** | 1884–2026, 1,158,079 pp | 1986-09-27 | AP wire, 2-2 Chirpich |
| 4 | Milwaukee Sentinel / Milwaukee Journal Sentinel | ids **41738** / **43101** | 43101: 1844–2026, 479,581 pp | c. 1986-11 | "She cracks code to win $25,000" (Collins) — 2-3 Brown |
| 5 | Fort Worth Star-Telegram | id **3455** | 1902–2026, ~9.08M pp | 1988-04-24 p.523 | the §0.2 tier check — also a real Decipher ad |
| 6 | Boston Globe | not verified | likely Publisher Extra | 1985-04-04 pp.1, 15 | Decipher I winners (Dolnick) |

**Dropped from this gate:** the two *The Tech* (MIT) items — Kaliski 1983-09-27 and
Kilian 1985-04-05. A college paper, it is not a newspapers.com title; its own archive
(`tech.mit.edu/archives`) is login-gated per `docs/sources.md`. Keep it as a separate
free lead (ask MIT libraries), not as calibration.

**Run each item two ways**, because they test different things:
- **(a) Full-text search**, scoped to the paper + year, using a distinctive title
  phrase. OCR mangles "Decipher": also try `Decip*`, `Decipher puzzle`, and the winner
  surnames Novak / Chirpich / Brown / Forstrom.
- **(b) Date-browse** to the known issue and flip to the known page. Publisher
  subdomains expose per-date article listings — e.g.
  `statesmanjournal.newspapers.com/paper/statesman-journal/3746/articles/1985-05-30/`.
  This is deterministic and does not depend on OCR quality.

**Decision rule** — the distinction matters, because hunting clue columns requires
full-text search (we don't know their dates or papers):
- **(a) finds ≥ 4** → the OCR index is good. Run the full query list (§3).
- **(a) finds 2–3** → partial. Run only §3 group A (paper-scoped), where the archive
  demonstrably holds the paper.
- **(a) finds ≤ 1 but (b) confirms the pages exist** → the pages are there and the
  *search* cannot see them. Clue columns would be invisible to queries too. **Do not
  renew.** Fallback only: date-browse the Virginian-Pilot through 1987–1991 looking for
  a recurring Decipher column — slow, but the single paper most likely to have carried it.
- **(b) also fails** → the paper/date is misattributed in the bibliography, or not
  digitised. Record which, and stop.

Note the Virginian-Pilot (item 1) is Holland's hometown paper — the single most likely
home of a recurring monthly column, which is why it anchors group A.

**Prior, revised down 2026-10-31:** a general web search across ~15 query variants
("monthly clue column", author names eliminated, `627-GOLD`, Youth Beat, etc.) surfaced
**no trace of any Decipher newspaper clue column** anywhere — only this repo, Wikipedia,
Reddit, Puzzling SE and the Cryptologia paper. That is weak evidence against the column
having run widely (a recurring syndicated column usually leaves a genealogy-board
footprint), though archive OCR text is not web-crawled, so the test still stands. Treat
§1's calibration gate as the real decider, not the web.

## 2. Triage rules (pre-commit to these; hit counts will lie to you)

- **Only editorial/article pages count.** Publisher Extra pages are paid advertising
  inserts. Every Decipher clipping recovered so far (five 1987–1991 clippings in
  Karen's Drive; three Toledo Blade mail-order ads in the 2026-10-30 free-archive
  sweep) is exactly that class. An ad is a **non-result**.
- Record per hit: paper, date, page number, the search snippet, and whether it is
  editorial or Publisher Extra.
- **Clip, don't read, in-trial.** Download the page/clip image and move on. Reading
  happens afterwards (see §5). Trial hours are for searching and capturing.
- Expect OCR mangling: `Decipher` → `Decipber`, `Deciphr`, `Decipher,`; `Holland` →
  `Hollend`. Run the two highest-value queries with a wildcard/truncated form too.

## 3. Query list (1985–1992), in priority order

**Group A — paper-scoped, highest prior (Virginian-Pilot 30397 first):**
1. paper=Virginian-Pilot, 1987–1991: `Decipher`
2. paper=Virginian-Pilot, 1987–1991: `Holland` AND `puzzle`
3. paper=Virginian-Pilot, 1987–1991: `627-GOLD` / `627-4653`
4. paper=Virginian-Pilot, 1985: `Decipher` (calibration item 1 should surface here)

**Group B — site-wide, mechanism words:**
5. `"clue of the month"` 1987–1991
6. `"monthly clue"` AND `puzzle` 1987–1991
7. `Decipher` AND `hotline` 1985–1992
8. `Decipher` AND `eliminated` 1987–1991 (the clue columns *eliminated author names* —
   this phrasing is the column's signature if it ran as editorial)
9. `Decipher III` 1987–1992
10. `627-GOLD` ; `627-4653` ; `654-3939` (site-wide, all years)

**Group C — site-wide, product words:**
11. `Decipher` AND `jigsaw` AND `prize` 1985–1992
12. `"solid gold"` AND `Decipher` 1987–1990
13. `Youth Beat` AND `Decipher` (the 1988 tie-in contest seen in Toledo Blade ads)
14. `Decipher` AND `bestseller` AND `author` 1987–1991

**Group D — author-name elimination sweep (only if Group B hits):**
15. For each of the 33 printed author names: `<surname>` AND `Decipher` 1987–1991.
    Run only the Group B/C survivors' neighbours first (Heller, Clavell, Vonnegut,
    Asimov, Pasternak, Poe) — a column naming who is *out* is the jackpot.

**Group E — Money Hunt secondary (same trial, double duty), 1986–1989:**
16. `"Money Hunt"` AND `puzzle` AND `million`
17. `Poser` AND `puzzle`
18. `"Empire State"` AND `treasure` AND `puzzle` 1986–1988

## 4. What a win looks like

Any editorial page that prints (a) an author name stated as eliminated or still live
for a given message, or (b) a clue beyond the five already in hand, or (c) the
hotline's monthly text. One such page changes the search space; three likely end it.
Capture the clip at full page resolution and note the column name and byline.

## 5. Handoff to the agent (after the trial, or during, via downloaded clips)

Drop clip images into `private/karen-puzzles/newspaper-clips-<date>/`. I will:
- transcribe each at vision resolution and diff every claim against
  `docs/decipher-ii.md`, `docs/decipher-iii.md` and `results/RUN_LOG.md`;
- extract any author-elimination statements into a new `docs/clue-columns.md` with
  paper/date/page provenance;
- re-run `solver/sweep.py` restricted to the surviving author pool if the pool shrinks.
I cannot log in or search the site for you; the search index is the only thing that
can "look through" newspapers.com, and it needs a human at the keyboard.

## 6. Budget

Calibration §1: 30–45 min. Full Groups A–C: 2–4 h. Group D only on a Group B hit.
Everything fits inside a 7-day trial with room to spare. **Do not buy months.**
