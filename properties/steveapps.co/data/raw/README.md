# Raw payloads

Layout: `data/raw/<provider>/<date>/<file>`.

No payloads are stored. A file appears here only after an approved `og-seo-evidence` run writes it, and `result_ref` on the ledger line points at it.

Retention, once files exist: 13 months, then the ledger line stays and the payload may be deleted. Search Console exports are dated and never overwritten; they live under `data/gsc/`, not here.
