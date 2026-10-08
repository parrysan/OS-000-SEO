# Experiment log — steveapps.co

One line per release in [`changes.jsonl`](changes.jsonl). The file is empty. No release has been logged by this task.

## Line shape

```json
{
  "date": "",
  "release_id": "",
  "urls": [],
  "templates": [],
  "fields": [],
  "hypothesis": "",
  "expected_signal": "",
  "measure": "",
  "comparison_window": "",
  "rollback": ""
}
```

`measure` is one of the five names in `baseline.md` (technical eligibility, search performance, observed rank, qualified traffic and conversions, AI mentions). It is never a combined score.

`expected_signal` names what would count as the hypothesis failing, and which ledger ids would show it.

Weekly dashboard notes and monthly reports cite `release_id`. They do not invent a result the log does not contain.
