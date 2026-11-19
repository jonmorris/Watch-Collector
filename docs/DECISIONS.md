# Decisions

The reasoning behind Watch Collector's decisions, one `##` section each. `DECISION-LOG.md` indexes these sections; this file holds the why.

Add a section here before logging any decision whose reasoning isn't written down somewhere else.

## Adopt running records

**Date:** 2026-11-19 · **Status:** Adopted

The project has no code yet. Its only decisions so far were made in a planning conversation, and nothing in the repo records them. Two repo-only records start now, so that decisions and the project's story build up while the work happens instead of being pieced together afterwards:

- `DECISION-LOG.md` is a dated, one-row-per-decision index that points into this file and the other docs.
- `CASE-STUDY.md` is a modular portfolio write-up drawn from that log.

New log entries are separate files in `docs/decision-log/` and get folded into the table on main. Rows that parallel branches append to the same table conflict every time, and separate files never do.

The repo has no language toolchain or test runner yet, so for now the checks and the fold are a documented convention, not a script. See *Tooling* in `DECISION-LOG.md`.

## Open questions (not yet decided)

These came up in the initial planning conversation (2026-10-14) and are still unanswered. They are not decisions. Each gets its own section above, and a log entry, once it is settled.

1. **Catalog data source.** The options are a curated seed catalog with manual entry, a licensed data provider, or community contributions. Scraping marketplaces raises terms-of-service problems.
2. **Image rights.** Brand press photos are copyrighted. One option is linked or attributed images in the catalog and the owner's own photos in the collection.
3. **Audience.** A single user, or multi-user accounts, possibly with shareable collections.
4. **Market pricing.** Values entered by hand, or automatic tracking (which runs into question 1 again).
5. **Primary device.** Desktop, phone, or both equally.
