# Evidence record — steveapps.co

One JSON object per line in [`ledger.jsonl`](ledger.jsonl). The ledger is empty. The block below is the field shape, not an observation.

```json
{
  "id": "",
  "site": "steveapps.co",
  "provider": "",
  "tool_or_endpoint": "",
  "upstream": "",
  "timestamp": "",
  "market": {
    "country": "",
    "language": "",
    "location": "",
    "device": ""
  },
  "subject": {
    "kind": "",
    "value": ""
  },
  "evidence_class": "",
  "params": {},
  "cost_usd_est": null,
  "cost_usd_billed": null,
  "result_ref": "",
  "summary": "",
  "cached_from": null,
  "reviewed_by": null
}
```

| Required | Field |
|---|---|
| Site id | `site` |
| Provider | `provider` |
| Endpoint or tool | `tool_or_endpoint` (upstream API, when there is one, in `upstream`) |
| Timestamp | `timestamp` (UTC, ISO-8601) |
| Country, language, location, device | `market.country`, `market.language`, `market.location`, `market.device` |
| The query | `subject`. For a keyword, `subject.kind` is `keyword` and `subject.value` is the query |
| Measured, estimated, inferred, or manual | `evidence_class` |
| Parameters | `params` |
| Evidence reference | `result_ref`, a path under `data/raw/<provider>/<date>/` or another durable file |

## Class rules

- **measured** — observed first-party or observed live (Search Console, a live SERP check, a curl result, an AI answer that was read).
- **estimated** — a provider model (volume, difficulty, traffic, backlink counts).
- **inferred** — reasoning over measured or estimated rows. The summary names the source ids.
- **manual** — a human statement or decision.

A failed lookup is `evidence_class` left as an unknown result in `summary`, not a rank of "not ranking" and not a volume of zero. Partial provider results stay, and `summary` says they are partial.

`cost_usd_billed` stays null until a billed-cost read has actually been done. This schema does not claim that read works.

Only `og-seo-evidence` appends ledger lines.
