# Decisions — steveapps.co

Append-only. Captain approval date: 2026-10-08. Source: the OpenSEO + DataForSEO design, section 9. This file records the decision. It does not carry it out beyond the dormant scaffold.

## Approved

### D-1 — Create this property and the three skills

**Decision:** yes. **Date:** 2026-10-08.

Create `properties/steveapps.co/` and write `og-seo-evidence`, `og-seo-research`, and `og-seo-cycle` in the global skill library. This folder is that property record. The skills are text. They stay dormant.

### D-2 — Staging fixes for the free technical defects

**Decision:** yes. **Date:** 2026-10-08.

Apply B1, B2, B3 (code only), B5, and B8a on staging (branch, backup, merge). Copy for B3 and B4 comes back to Phil before it is applied. Status of the staging work is in `plans/backlog.md`. This SEO task does not edit WordPress.

### D-4 — Category archives at launch

**Decision:** `noindex,follow` (backlog B6). **Date:** 2026-10-08.

Service pages stay the indexed destinations. Revisit only with Search Console data, which does not exist yet.

### D-5 — Budget policy

**Decision:** yes. **Date:** 2026-10-08.

The numbers live in `budget-policy.md`: $0.25 per run before a fresh approval, $3 monthly alert, $10 hard stop, and a small DataForSEO balance as the real cap. Approving the policy does not approve a spend. No paid call is in scope.

### D-8 — GA4

**Decision:** no. **Date:** 2026-10-08.

Search Console plus form entries. GA4 stays off unless the captain opens a new decision.

### D-9 — AI engines in the tracked set

**Decision:** yes. **Date:** 2026-10-08.

ChatGPT, Gemini, and Google AI Overviews weekly; Perplexity monthly; Claude off. The prompt set is not written. No visibility run is approved.

## Not approved

### D-3 — Search Console property via a DNS change

**Decision:** not approved. **Out of scope.**

Option A would add a DNS TXT record at Cloudflare for the live site. Option B would wait until cutover. Neither is approved.

**Condition to reopen:** the captain approves a specific option (live DNS now, or verification at cutover). Until then, do not change DNS and do not create the property.

### D-6 — Install OpenSEO

**Decision:** not approved. **Out of scope.**

**Condition to reopen:** the captain approves an install. The design suggested a no-spend spike, or an install after Steve commits (G0). This task does not install anything and does not register an MCP server.

### D-7 — Anything sent to Steve

**Decision:** not approved. **Out of scope.**

Covers the rights question (article copyright) and the person-versus-brand question (schema). 

**Condition to reopen:** the captain approves the wording. Nothing is sent until then.

### Paid calls and DataForSEO spend

**Decision:** not approved. **Out of scope.**

**Condition to reopen:** Steve commits to the Open SEO idea (gate G0), the run fits `budget-policy.md`, and the captain approves the spend. Until all three are true, no keyword research, no rank tracking, no AI visibility check, and no DataForSEO call (including a free balance lookup).
