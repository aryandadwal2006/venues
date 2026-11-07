# AI Research Venue Tracker

This repository is the canonical home for the AI research venue tracker used to plan research submissions for competitive PhD applications.

## Files

- `AI_Research_Venue_Tracker_2027_2028.xlsx` — primary workbook, designed to open in Excel and import into Google Sheets.
- This README documents the maintenance and notification rules.

## Workbook structure

1. **Dashboard** — summary counts and near-term deadline view.
2. **Deadline Tracker** — conference cycles and their abstract, extended abstract, full paper, supplementary material, rebuttal/author response, decision, camera-ready and conference milestones.
3. **Venue Directory** — canonical venue names, abbreviations, venue type, research area and official website/CFP.
4. **Journal Tracker** — rolling journal submission routes, author guidelines and source links.
5. **Read Me** — usage, field definitions and maintenance notes.

## Update policy

- Use official conference, society, publisher and journal pages as primary sources.
- Track the 2027 and 2028 cycles, and add subsequent cycles when official calls are published.
- Do not infer dates from prior years or third-party deadline aggregators.
- If an official deadline is not announced, leave its date blank and mark its status as **TBA**.
- Distinguish abstract registration, extended abstract, full paper, supplement, author response/rebuttal, camera-ready and other track-specific deadlines. Do not collapse staged submission processes into one date.
- Record the exact source URL, the date checked, deadline timezone, and whether the date is confirmed or tentative.
- For journals, record whether submissions are rolling and link to the official submission guidelines; do not invent fixed deadlines.
- Preserve user-editable fields such as project, priority and paper status when refreshing the workbook.
- Keep a concise change log describing new calls, changed deadlines and corrected entries.

## Reminder policy

Send a ChatGPT notification **two calendar days before each active submission milestone** with a confirmed date. This includes abstract registration, extended abstract, full paper, supplement, rebuttal/author response, camera-ready and special-track submission deadlines. Do not send reminders for conference dates, decision notifications or journal rolling submissions unless a fixed, officially announced deadline applies. Send each reminder only once per milestone. Use the deadline's stated timezone when available; if no timezone is stated, say so in the reminder rather than silently assuming one.

## Weekly maintenance

On the weekly update run:
1. Read the current workbook from this repository before making changes.
2. Recheck every tracked venue's official CFP/date/author-instructions pages and search for newly announced 2027–2028 calls.
3. Update the workbook without deleting user-managed project, priority or submission-status fields.
4. Add an entry to the change log and update the last-checked date.
5. Commit the refreshed workbook to the `main` branch with a descriptive commit message.
6. If GitHub write access is unavailable, do not claim the repository was updated; provide the refreshed workbook separately and report the blocker.

Daily deadline checks should use the current repository workbook and issue one-time notifications for milestones exactly two calendar days away. Suppress repeat alerts for the same venue, cycle, milestone and deadline date.

## Data quality

- Full venue names should be used alongside abbreviations.
- Distinguish conferences from journals and workshop tracks from main tracks.
- Prefer the official call for papers or official submission page over general event pages.
- Store dates in ISO `YYYY-MM-DD` form and identify the timezone separately.
- Never represent an unannounced or unverified date as confirmed.

## Repository

https://github.com/aryandadwal2006/venues
