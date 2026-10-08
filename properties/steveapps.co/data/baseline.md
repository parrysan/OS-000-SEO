# Baseline — steveapps.co

Template from the measurement plan (design section 6). Five measures, kept separate. No combined score.

**No measurement was taken for this file.** The WordPress site is not public and has no Search Console property, so there is no search baseline to record. A prior design mentions scores for the live SPA; those figures are not copied here, because this task did not re-measure them.

| # | Measure | Source (when it exists) | Class | Cadence | Status |
|---|---|---|---|---|---|
| 1 | Technical eligibility | `curl` / browser on staging; OpenSEO audit and Lighthouse only after cutover; `og-seo-health-check` | measured | each release, and monthly | not measured |
| 2 | Search performance | Search Console `get_search_console_performance` | measured | weekly pull, monthly report | not measured. No property (D-3 not approved) |
| 3 | Observed rank | OpenSEO rank tracker, UK, mobile default | measured (sampled) | weekly | not measured. Tracking waits on G0 and a public URL |
| 4 | Qualified traffic and conversions | Fluent Forms entries and Search Console clicks. GA4 is off (D-8) | measured | monthly | not measured |
| 5 | AI mentions, citations, referrals | OpenSEO AI Visibility on the fixed prompt set, plus manual spot checks | measured (sampled) | monthly | not measured. `prompts.txt` is empty |

## What a later baseline row must include

Date, measure number, source, evidence class, market (country, language, location, device), and a ledger id from `data/evidence/ledger.jsonl`. A number without a ledger id does not enter this file.

## Comparison rules (for later)

Same device and country. Full weeks. Trailing 28 days against the previous 28. Seasonality is unknown on a new site. If several changes ship in one window, list them as confounders. Do not treat a before/after pair as a cause.
