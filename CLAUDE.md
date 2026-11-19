# CLAUDE.md

Watch Collector is a planned website for researching watch purchases and tracking a watch collection, with a strong visual focus. It is a research tool and a digital collection, not a marketplace. No code exists yet.

## Running records

`docs/DECISION-LOG.md` and `docs/CASE-STUDY.md` are repo-only indexes over the other docs (the reasoning lives in `docs/DECISIONS.md`). They are never built or shipped.

- When a change makes a decision, or is worth telling, add a decision-log entry file and/or amend a case-study module **in the same commit**.
- A decision-log entry is always a **new file** in `docs/decision-log/` (`YYYY-MM-DD-short-name.md`, one table row). Never edit the table. Folding happens on main in its own commit.
- Write the why in `docs/DECISIONS.md` (or another doc) first; the entry's Ref points to it.
- In the case study, never invent `[[placeholders]]` (role, tools, metrics, reflections); the owner fills them in.
