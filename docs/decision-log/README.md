# Pending decision-log entries

Each file here is one decision waiting to be folded into the table in [`../DECISION-LOG.md`](../DECISION-LOG.md). Files are named `YYYY-MM-DD-short-name.md` and contain exactly one table row. The rules and the fold command are in that file.

To print the pending entries, from the repo root:

```sh
cat $(ls docs/decision-log/2*.md | sort)
```
