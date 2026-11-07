# AI Research Venue Tracker

Canonical tracker for research-publication planning across AI, computer science, mathematical foundations, systems, robotics, computational biology and AI for science.

## Repository files

- `AI_Research_Venue_Tracker_Expanded_2027_2028.xlsx` — primary workbook. The **Venue Directory** sheet is the authoritative full catalogue.
- `tracker-config.json` — venue scopes, required conference list, deadline schema and automation rules.
- `reminder-log.csv` — one-time notification ledger, keyed by venue, cycle, milestone and deadline.
- `VENUE_SELECTION.md` — explanation of which venues are core, specialist or conditional targets.

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

## Deadline and travel-grant fields

For conference rows, track abstract/registration, extended abstract, full paper, supplementary material, author response/rebuttal, decision notification, camera-ready, conference dates, location and timezone.

Two travel-grant columns are mandatory:
- **Travel grant available? (Yes / No / TBA)** — use Yes or No only when an official source verifies the status. TBA means not checked or not announced; it does not mean No.
- **Travel grant deadline** — the official application deadline for student travel support. If multiple programmes exist, record the main student travel-support deadline and describe other options in Notes.

The reminder monitor should alert two calendar days before every confirmed submission milestone and every confirmed travel-grant application deadline. It must suppress duplicate notifications for the same deadline key.

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

## Repository

https://github.com/aryandadwal2006/venues
