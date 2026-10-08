# steveapps.co — dormant property record

One engagement, one folder, copied from [`templates/property/`](../../templates/property/README.md) and extended with the evidence ledger from the SEO/AEO domain law ([`docs/seo-domain-design.md`](../../docs/seo-domain-design.md)).

**Status: dormant.** Docs and skill text only. No measurement was taken for this record. No paid call, no DataForSEO call, no OpenSEO install, nothing sent to Steve.

`properties/` stays gitignored. These scaffold files are force-tracked because captain decision D-1 approved the record. Future crawl exports, Search Console dumps, raw payloads, and client reports stay untracked (see `.gitignore` in this folder).

## Layout

```
properties/steveapps.co/
├── context.md                 # identity (template contract)
├── decisions.md               # append-only: D-1, D-2, D-4, D-5, D-8, D-9 and the ones not approved
├── budget-policy.md           # §7.4 numbers
├── data/
│   ├── prompts.txt            # empty on purpose (M3 gated)
│   ├── baseline.md            # five measures, none filled
│   ├── experiment-log.md      # changes.jsonl field template
│   ├── changes.jsonl          # empty
│   ├── evidence/
│   │   ├── SCHEMA.md          # one JSON object per observation
│   │   └── ledger.jsonl       # empty
│   ├── raw/README.md          # data/raw/<provider>/<date>/ — no payloads
│   ├── gsc/README.md
│   ├── crawls/README.md
│   └── analytics/README.md
├── plans/backlog.md           # §4 items with status
├── audits/README.md
└── reports/README.md
```

Skills (global library, not this repo): `og-seo-evidence`, `og-seo-research`, `og-seo-cycle`. Front door remains `og-seo-health-check`.
