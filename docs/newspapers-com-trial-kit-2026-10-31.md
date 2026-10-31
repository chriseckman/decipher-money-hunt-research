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

1. **Library route first.** Many public libraries include *Newspapers.com Library
   Edition* with a card, often a broader product than the consumer tier. Same queries,
   zero cost. Check your library's Databases/A–Z list for "Newspapers.com" before
   buying. (`docs/sources.md` lists this as the cheapest path.)
2. **Tier check.** The one concrete live lead — `newspapers.com/newspage/640735315`
   (Fort Worth Star-Telegram, Sun 1988-04-24, p. 523) — is a **Publisher Extra** page,
   the paid add-on tier. Open that exact URL while logged in on a trial and confirm it
   renders *before* committing to anything beyond the trial. A basic-tier subscription
   may not unlock the single page we already know is a hit.

## 1. The calibration test (run FIRST, ~30–45 min) — the stop/go gate

These eight items are **known to exist** (cited in Baldwin & Sherman 1990 p. 283, or
held as scans in Karen's Drive archive). They are the ground truth for whether this
archive's coverage and OCR can find Decipher content at all.

| # | Paper | Date | Page | What |
|---|---|---|---|---|
| 1 | Virginian-Pilot | 1985-04-17 | D6 | "Puzzle players decipher cryptogram" (Bryant) |
| 2 | Boston Globe | 1985-04-04 | 1 | Decipher I winners (Dolnick) |
| 3 | Boston Globe | 1985-04-04 | 15 | continuation |
| 4 | The Tech (MIT) | 1983-09-27 | — | Kaliski |
| 5 | The Tech (MIT) | 1985-04-05 | — | Kilian |
| 6 | Statesman Journal (Salem OR) | 1986-03-25 | 1–2 | "Decipher II game pays off in cold cash" (Forstrom) — 2-1 Novak |
| 7 | Milwaukee Sentinel | c. 1986-11 | — | "She cracks code to win $25,000" (Collins) — 2-3 Brown |
| 8 | The Leaf-Chronicle (Clarksville TN) | 1986-09-27 | — | AP wire, 2-2 Chirpich |

Search each by paper + date + a distinctive phrase from the title (OCR will mangle
"Decipher"; also try `Decip*`, `Decipher puzzle`, and the winner surnames Novak /
Chirpich / Brown).

**Decision rule:**
- **< 2 of 8 found** → the archive's coverage/OCR cannot see this niche. **Stop. Do not
  renew.** The clue columns would be invisible here too.
- **2–3 found** → partial. Proceed only with the paper-scoped queries (§3 group A),
  which target papers the archive demonstrably holds.
- **≥ 4 found** → index is good. Run the full query list (§3).

Note the Virginian-Pilot is newspapers.com paper **30397** and is Holland's hometown
paper — the single most likely home of a recurring monthly column. Item 1 doubles as
the coverage check for it.

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
