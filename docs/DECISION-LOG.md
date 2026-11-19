# Decision log

A dated index of Watch Collector's decisions, one row per decision. **It is an index, not a second source of truth.** Each row's *Ref* names the file and section that hold the reasoning. Right now that file is [`DECISIONS.md`](DECISIONS.md), which holds the why behind each decision plus the open questions. Other docs (requirements, conventions, a deferred list) become valid Refs once they exist.

This is a repo-only doc. It is never built or shipped.

## How to keep this file

- **Add a file, not a row.** A new decision goes in [`docs/decision-log/`](decision-log/) as its own file named `YYYY-MM-DD-short-name.md` (lowercase, hyphenated), containing exactly one table row. Never edit the table on a branch: rows that parallel branches append to the same last line always conflict, and separate files never do.
- **Fold on main.** Folding appends the waiting entries to the end of the table in filename order (date, then name) and deletes their files. Do it on main, in a commit of its own, whenever the folder gets long. The command is under *Tooling*.
- **One row per decision, not per commit.** A reversed decision gets a new row of kind Reversed. The old row stays.
- **Say the decision, not the change.** Write "Collection photos are owner-uploaded only", not "edit upload.ts".
- **Kind** is one of the list below. This list is the only place it is defined.
- **Ref** names the file and section that hold the why (`DECISIONS.md → Adopt running records`). If the why isn't written anywhere, write it there first.

### Kinds

| Kind | Use for |
|---|---|
| Product | What the site does and for whom: modes, features, scope |
| Design | How it looks and feels: visual direction, layout, interaction |
| Data | Where catalog data and images come from, the metadata schema, licensing and rights |
| Engineering | Stack, architecture, infrastructure, tooling |
| Process | How the project is run: workflow, records, conventions |
| Deferred | Something consciously not done now (say what would bring it back) |
| Reversed | Undoes an earlier row (name that row's date and decision) |

### Entry format

One line, a leading and trailing `|`, exactly four cells, and the Date must match the filename's date:

```
| 2026-11-19 | Process | Decisions logged as one file per entry, folded into this table on main | DECISIONS.md → Adopt running records |
```

### Tooling

The repo has no language toolchain or test runner yet, so there is no validation script and no CI check. When one is added (for example `package.json`), add a `decision-log` script to it, with unit tests. The script validates entry files against the rules above (filename `^\d{4}-\d{2}-\d{2}-[a-z0-9]+(-[a-z0-9]+)*\.md$`, Date cell matching the filename date, Kind from the list, non-empty Decision and Ref) and folds them with `--fold`. Hook those tests into the test command so CI fails on a malformed entry.

Until then, from the repo root:

```sh
# Print pending entries, in fold order
cat $(ls docs/decision-log/2*.md | sort)

# Fold (on main, in its own commit): append to the table, then delete the files
cat $(ls docs/decision-log/2*.md | sort) >> docs/DECISION-LOG.md && git rm -q docs/decision-log/2*.md
```

The fold works because the table is the last thing in this file. Keep it that way.

## Log

| Date | Kind | Decision | Ref |
|---|---|---|---|
