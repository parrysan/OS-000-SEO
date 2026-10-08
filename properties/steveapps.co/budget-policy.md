# Budget policy — steveapps.co

Captain decision D-5, approved 2026-10-08. Source: design section 7.4. These are the ceilings. They are not an approval to spend.

A paid call or a DataForSEO call (including a free account endpoint) also needs the captain's approval, and it waits until Steve commits to the Open SEO idea. The figures below apply after that unlock.

| Rule | Value |
|---|---|
| Max per agent run before a fresh approval | **$0.25** |
| Fresh approval (Phil, in chat) | any run estimated above $0.25; any new schedule or tracker; any new provider or engine; any competitor expansion beyond the limits below |
| Monthly alert | **$3** |
| Hard stop | **$10**, then report and stop |
| Balance | keep the DataForSEO balance small. That balance is the real hard cap, because OpenSEO has no account-level monthly limit. Top up only on Phil's instruction |
| Rank tracking | weekly, mobile only, depth 40, at most 40 keywords. Daily only inside a launch window of at most 2 weeks, with approval |
| AI prompts | at most 25 prompts. Perplexity monthly. Claude off |
| Competitor expansion | at most 5 domains per question; at most 20 SERP keywords per run |
| Keyword discovery | at most 3 seeds × 50 rows per run; at most 150 new terms before a human prunes |

## Caching (check the ledger before every paid call)

Same `(provider, endpoint, params, location, language, device)` inside the TTL is a hit. Label it `cached from <date>`.

| Kind | TTL |
|---|---|
| Keyword metrics | 30 days |
| SERP and rank | 7 days |
| Competitor lookups | 30 days |
| Backlinks | 60 days |
| AI answers | one per prompt per engine per run |

## Call rules

- Every `run_rank_tracker` passes `maxCostCredits` equal to the approved ceiling. A rejected run is not retried.
- Credential names may be recorded. Credential values never are. No token belongs in this folder.
- Month-to-date spend is summed from the ledger. Reconciling it against the provider balance is itself a DataForSEO call and stays behind the same approval gate.
- OpenSEO is not installed (D-6 is not approved). This file does not authorize installing it.
