# Backlog — steveapps.co

Staged from the 2026-10-08 design, section 4. Status is the state of that item as of this record. Findings below are the design's evidence, not a new audit. This task did not re-check the staging URLs.

WordPress edits happen in the site repo, branch-per-task, backup first. This folder stores the list.

Priority P0 (before any public exposure) to P3. Confidence H/M/L. Effort S (under 2 h), M (half day), L (day or more).

## 4A. Technical and metadata

| ID | Status | Problem (as recorded in the design) | Pri | Conf | Eff | Approval |
|---|---|---|---|---|---|---|
| B1 | in progress, staging | Advertised Markdown alternate URLs redirect to HTML. `.md` links and the homepage alternate href. `Vary: Accept` missing. Owner: `mu-plugins/steve-agent-ready/markdown.php` | P1 | H | S | Agent, non-destructive branch |
| B2 | in progress, staging | Two `rel=canonical` tags on pages and services (theme and core). Archives echo the request URI. Owner: `themes/steveapps/inc/seo.php` | P1 | H | S | Agent |
| B3-code | in progress, staging | Meta description falls through to the site tagline on non-article pages. Code change: fallback `meta_description`, then service `short_description`, then post `tldr_summary`, then tagline. Owner: `inc/seo.php` | P1 | H | S | Agent for the code |
| B3-copy | not started | Real per-page descriptions in the ACF "Page SEO" field for 4 services, About, Clients, Insights. Steve's voice stays. Unique, under about 160 characters | P1 | H | M | Phil approves copy |
| B4 | not started | Titles carry no search term. Set `meta_title` on home and the 4 services, about 60 characters, service term in plain language, brand kept | P1 | M | S | Phil approves wording |
| B5 | in progress, staging | No H1 on `/about/` and none on category archives. Owner: Bio block and the category archive template | P1 | H | S | Agent |
| B6 | in progress, staging | Category archives duplicate the service pages. Decision D-4: `noindex,follow` at launch. Sitemap omits them. Service pages stay in the sitemap | P2 | M | S | Approved (D-4). Depends on B5 |
| B7 | not started | Sitemap returns 404 on staging while search is discouraged. Pre-cutover test on a scratch copy with `blog_public=1`. Go-live step is separate | P0 at cutover | M | S | Part of cutover approval. Depends on production host |
| B8a | in progress, staging | `Person.url` is `/about` without a trailing slash and 301s. Use `home_url('/about/')`. Owner: schema output | P2 | M | S | Agent |
| B8b | not started | Article `Person` name is the site name "Steve Apps". Confirm person versus brand with Steve | P2 | M | S | D-7 not approved. Nothing is sent |
| B8c | not started | `ProfessionalService` is on the home page only. A `Service` node on each service page is optional, and only if it matches visible text | P2 | M | S | Agent, if it adds information |
| B8d | not started | Default social image is a large portrait PNG. Needs a purpose-made 1200×630 share image | P2 | M | M | Phil |

Acceptance tests stay the ones in the design (curl for B1, one canonical on 10 URLs for B2, unique descriptions for B3, title length and term for B4, one H1 per indexable template for B5, `noindex,follow` for B6, sitemap 200 at cutover for B7, validators for B8). They have not been run by this task.

## 4B. Content, IA, and AEO

| ID | Status | Item | Pri | Depends on |
|---|---|---|---|---|
| C1 | gated | 16 of 17 article PDFs end with a Persona Partnership copyright line, per the design. Articles stay private drafts. The rights question is not sent | P0 | D-7, then Steve's written answer, recorded here as `manual` evidence |
| C2 | gated | Most article keywords have no verified metric. One batched lookup after Steve commits. Estimate in the design was under $0.15. No lookup is run from this record | P1 | G0 (Steve commits) and a spend approval inside `budget-policy.md` |
| C3 | gated | One primary target per URL (`keyword-map.md`, not created). Head terms stay on service or home pages | P1 | C2 |
| C4 | gated | Service pages need a page-level review against a SERP read. Briefs only. No generated pages | P2 | C2 and a public site |
| C5 | gated | Communicating Change has one article (The Brain). A new-topic brief waits on Steve's real stories | P3 | C1 |
| C6 | gated | Article dates in schema must match what the page visibly states. Steve decides original year versus publish date | P2 | Steve, via a captain-approved question (D-7) |

## 4C. Measurement

| ID | Status | Item | Pri | Depends on |
|---|---|---|---|---|
| M1 | done (scaffold only) | This folder: context, prompts placeholder, ledger schema, `changes.jsonl`. No rows | P1 | — |
| M2 | gated | Search Console property and Google Cloud OAuth client for OpenSEO | P1 | D-3, which is not approved, and a cutover plan |
| M3 | gated | 25 hand-written AI prompts, reviewed by Phil. `data/prompts.txt` is empty | P2 | G0 |
| M4 | gated | Replace simulated dashboard rows with measured rows, one row at a time, each with an evidence class | P2 | M2 and a first real datum |

## Gates (not backlog items)

- **G0** — Steve commits to the Open SEO idea. Until then, no paid research or tracking.
- **G1** — Rights answer from Steve. Blocked on D-7.
- **G2** — Public host decided and cutover done. Host decision is still deferred.
- **G3** — Search Console property verified. Blocked on D-3.
