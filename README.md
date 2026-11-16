# AI Research Venue Tracker

Canonical tracker for research-publication planning across AI, computer science, mathematical foundations, systems, robotics, computational biology and AI for science.

## Repository files

- `AI_Research_Venue_Tracker_AI_Only_Final.xlsx` — canonical workbook. The **Venue Directory** sheet is the authoritative full catalogue.
- `tracker-config.json` — venue scopes, required conference list, deadline schema and automation rules.
- `reminder-log.csv` — one-time notification ledger, keyed by venue, cycle, milestone and deadline.
- `VENUE_SELECTION.md` — explanation of which venues are core, specialist or conditional targets, including ITCS, IPDPS and FM.

## Source-list distinction

The user-provided acceptance-rate list is from **csconferences.org**. It is not the same thing as CSRankings. CSRankings is a separate metrics-based department ranking that counts papers from its own curated set of top conferences. This tracker includes the complete conference set supplied from csconferences.org as mandatory coverage, while separately retaining specialist venues and journals for research areas that the list does not cover.

Primary references:
- https://csconferences.org/
- https://csrankings.org/
- https://csrankings.org/faq.html

## Workbook structure

1. **Dashboard** — counts and tracker scope.
2. **Deadline Tracker** — 2027/2028 conference cycles, submission milestones, travel-grant availability and travel-grant deadlines.
3. **Venue Directory** — full names, abbreviations, research areas, source-list membership and retention decisions.
4. **Journal Tracker** — rolling journal targets and scope guidance.
5. **Read Me** — field definitions and maintenance instructions.
6. **AI-Only** — curated 38-venue AI research view, with 12 configured groups and aliases.

## Deadline and travel-grant fields

For conference rows, track abstract/registration, extended abstract, full paper, supplementary material, author response/rebuttal, decision notification, camera-ready, fixed special-track deadlines, conference dates, location, timezone, deadline status and official venue/CFP links.

Two travel-grant columns are mandatory:
- **Travel grant available? (Yes / No / TBA)** — use Yes or No only when an official source verifies the status. TBA means not checked or not announced; it does not mean No.
- **Travel grant deadline** — the official application deadline for student travel support. If multiple programmes exist, record the main student travel-support deadline and describe other options in Notes.

The reminder monitor should alert two calendar days before every confirmed submission milestone, camera-ready deadline and confirmed travel-grant application deadline. It suppresses duplicates by venue + cycle + milestone + exact deadline date.

## Weekly maintenance

- Read the workbook and `tracker-config.json` from this repository before updating.
- Verify official CFP, important dates, author instructions and student travel-support pages.
- Update newly announced 2027/2028 calls and any subsequent cycle announced by the venue.
- Never infer dates from prior years, search snippets or third-party trackers. Use TBA until an official page confirms a date.
- Record official source URLs, last-checked date and deadline timezone.
- Preserve manually editable priority, paper status and project fields.
- Commit the refreshed workbook and reminder log to `main`. If a GitHub write fails, do not claim the repository changed; attach the refreshed workbook separately and report the blocker.

## Admissions interpretation

The workbook is a research-planning catalogue, not an admissions ranking. A publication is valuable when the contribution is strong and directly relevant to the venue's research community. Venue prestige, selectivity, authorship position and PhD value cannot be reduced to one universal ordering. A specialized top venue can be more relevant than a broad AI venue for the right paper, but it is not automatically more valuable for every applicant.

## Inventory and source distinction

The Venue Directory contains 169 canonical entries: 96 conference venues and 73 journal targets. The 66 user-supplied csconferences.org conference venues remain mandatory coverage; this list is not CSRankings. The separate AI-Only sheet has 38 canonical identities across 12 groups. SIGGRAPH Asia is retained in AI-Only but is outside the 96-venue comprehensive conference array.

## Repository

https://github.com/aryandadwal2006/venues


## AI-only worksheet

The workbook contains a separate **AI-Only** sheet. It includes only the 38 canonical venues from the user's explicit AI venue groups, after deduplicating cross-listed aliases such as PAMI/TPAMI. Its category memberships and requested subtrack notes are defined in tracker-config.json. Do not append unrelated CS venues to this tab.

The AI-Only tab retains submission milestones, cycle, paper status, priority, official CFP/source link and both travel-support fields. It also tracks extended abstracts separately from full-paper deadlines.

Monitor **Datasets & Benchmarks** and **Findings** only when the official CFP/submission portal confirms the track for that venue and year. A requested track label is not evidence that every listed venue offers it.

Workbook primary file: `AI_Research_Venue_Tracker_AI_Only_Final.xlsx`. GitHub main is canonical; no Google Sheet or Google Drive copy is maintained.


## Sorting and archived cycles

Both `Deadline Tracker` and `AI-Only` are sorted by the earliest future **actionable submission/response/travel-grant deadline**. The active dates appear first in ascending order. Undated 2027/2028 watch cycles follow, then rolling journals, then expired submission cycles in a muted grey archive at the bottom. For an expired cycle, retain its historical dates and ensure the next annual cycle (even if its CFP is still TBA) is present above the archive. Decision notifications, conference dates and camera-ready dates remain recorded but do not keep a closed submission cycle in the active submission queue. Camera-ready dates may still generate their own two-day reminders.
The Days to next active deadline field is positive for future actionable submission/response/travel-grant milestones and negative from the most recent past actionable milestone for archived rows; TBA and rolling rows remain blank. Fixed special-track submission deadlines are included.


## Audit status

The 2026-11-16 refresh is documented in AUDIT_LOG.md. It verified the official pages listed there but did not complete a page-by-page audit of all 96 conference CFP/travel-support sources and all 73 journal author pages. Unchecked rows retain prior last-checked dates or TBA; this refresh is explicitly partial.
