# Newspapers.com sweep #1 — 2026-10-31 (trial day 1)

Consumer trial with Publisher Extra. Method and raw data live in
`private/karen-puzzles/newspaper-clips-2026-10-31/` (calibration log, hits log,
per-year sweep JSON). This note records only findings safe for the public repo.

## Calibration gate result (kit §1)

Six known-to-exist items tested; **4 confirmed in-archive, both misses are
coverage gaps, not search blindness**:

| Item | Result |
|---|---|
| Virginian-Pilot 1985-04-17 p.D6 | NOT COVERED — paper holds nothing 1964–2025 (browse and search agree) |
| Statesman Journal 1986-03-25 | FOUND by full-text search (5 pages hit) |
| Leaf-Chronicle 1986-09-27 | FOUND by full-text search (p.10) |
| Milwaukee c.1986-11 | NOT COVERED — archive has no 1986 |
| Fort Worth 1988-04-24 p.523 | CONFIRMED by browse (Decipher III Gold Edition ad visible) |
| Boston Globe 1985-04-04 | FOUND by search — exactly 1 match, Page 15, matching the citation |

Consequence: kit Group A (Virginian-Pilot 1987–91) is impossible on this archive —
the paper does not hold those years. Site-wide queries (Groups B/C) remain viable.

## Editorial find #1: Decipher I elimination mechanism, in print

**Detroit Free Press, Sunday 1984-03-25, page 71 (3G), column "Deciphering clues"**
(next to John Dunphy's consumer-watch column; clipping images in private folder).

Verified facts from the article:

- Warren Holland promised **$10,000** to the first person to solve Decipher I.
- Key = a popular novel by one of **21 authors** disclosed by Holland.
- Owners got an extension to **March 1, 1985**.
- "Beginning in May he will delete the names of **two authors each month** from
  the list until the key author is known."
- **$1,000 a month** added to the pot.
- On **May 1 (1984)** players could start calling the Decipher hotline
  **1-800-623-CLUE** for authors dropped from the list "or other clues that may
  be released."

This is the elimination mechanism that the Decipher III monthly clue columns
(1987–91) continued. The 1984 hotline number and the "two authors per month"
cadence are new facts for `docs/decipher-ii.md` provenance work.

## Clue-column hunt status (Decipher III, 1987–1991)

- Per-year match counts for kit queries B5–B10, C12, E16 and six targeted
  elimination-phrase variants are in the private sweep JSON. Counts are high
  (hundreds/year) because page-level matching couples Decipher ads with
  unrelated copy using the same words.
- All low-count phrase hits opened so far were false positives (Kryptos feature,
  crime wire, news-index page, business page). Logged in the private hits log.
- No recurring single-paper signature of a clue column yet. Next best moves:
  papers/dates of Karen's five known 1987–91 clippings (then paper-scope around
  those dates), and the unopened 1987–88 relevance-ranked hits (Patriot Ledger,
  San Antonio Express-News, The Blade, El Paso Herald-Post).

## Money Hunt (secondary)

Query `"Money Hunt" puzzle million` per year: 24 (1986), 9 (1987), 5 (1988),
8 (1989) — discriminating but unopened; first hits include Chicago Tribune
1986-11-28 p.128 and Los Angeles Herald Examiner 1988-04-28 p.12.

## Search mechanics reference (for future sessions)

- `?query=` / `?keyword=` + `&ymd=` (accepts YYYY / YYYY-MM / YYYY-MM-DD); no
  multi-year range parameter exists.
- Paper scope: `&publication-ids=<paper id>`.
- Result pages link to `/image/<id>/?match=N&terms=...` which opens the viewer
  pre-highlighted; find-bar prev/next jumps between matches.
- Browse-tab year list is ground truth for holdings; archive pages' "YYYY–2026"
  marketing span overstates (Virginian-Pilot claims 1899–2026, holds ≤1963+2026).
- Long exact phrases fail on OCR noise; single distinctive words + per-year
  filters work. Multi-word queries behave as phrases plus optional extra terms.

## Trial day 2 update (2026-11-01)

- Karen's five known 1987–91 clippings reviewed (three are ads; two are
  editorial gift-guide items: Courier-Post 1988-12-06 and Palm Beach Post
  1990-12-20). The Palm Beach item confirms the elimination-mechanism chain:
  "the three puzzles can be solved in sequence from **monthly clues available on
  the Decipher III Hotline**… call Decipher Inc. at **(800) 654-3939**."
  1988-era ads give a second number, 1-800-366-4747 (Youth Beat mail-order
  campaign).
- Paper IDs established: Courier-Post 3767, Palm Beach Post 4012,
  Patriot Ledger 43247, The Blade 43279. Per-year paper-scoped `Decipher`
  counts and dated hit lists captured privately.
- All opened candidate pages were false positives (ordinary-usage "decipher" in
  news copy: POW/MIA story, moon-rocks feature, genetic-code feature, tax story)
  except one: The Blade 1988-04-24 p.127, which is a Youth Beat mail-order ad
  identical to the known Arizona Daily Star 1988-04-16 ad. A cluster of
  "Decipher hotline" 1988 hits across San Antonio / Toledo / El Paso /
  Fort Worth / Tucson on 1988-04-22..28 is now explained as that single
  national Sunday ad campaign, not syndicated editorial.
- Working hypothesis after two trial days: Decipher III monthly clues were
  delivered by hotline, not by a recurring newspaper column; newspapers carried
  launch coverage, gift guides, and ads. Remaining untested angles: hotline
  numbers as literal OCR queries, the Money Hunt low-count hits, and editorial
  in the two clipping papers outside the clipping dates.
