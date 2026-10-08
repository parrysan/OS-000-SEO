# SEO Context — steveapps.co

> **This file is the single source of positioning truth for all SEO work on this property.**
> A copy (or symlink) of it lives in the site's own repo as `.agents/product-marketing.md`
> so the ecosystem skills (`seo-audit`, `ai-seo`, `programmatic-seo`) pick it up automatically.
> Update here first; sync to the site repo.
>
> **Dormant.** Filled from the approved 2026-10-08 design. This task did not re-probe the site and recorded no measurement. Paid research and rank tracking wait until Steve commits to the Open SEO idea.

## Identity

- **Website URL**: https://steveapps.co (public host is still the existing site; the WordPress build is not public)
- **Business name**: Steve Apps
- **One-line positioning**: Business psychologist and leadership communication coach
- **Business model**: services
- **CMS / framework**: WordPress block theme `steveapps`, ACF Pro. As recorded in the 2026-10-08 design (not re-checked here): WordPress 6.9, PHP 8.3, ACF Pro 6.8.10, custom post types `service`, `testimonial`, `client`, `credential`
- **Rendering**: WordPress (server-rendered theme). The design records the live host as a React SPA and the WordPress build as staging-only. This task did not fetch either
- **SEO plugin**: none, by design. The theme and one mu-plugin own titles, meta, canonicals, sitemap, robots, JSON-LD, and redirects. Do not add Yoast, Rank Math, or The SEO Framework without a new decision
- **Visibility**: staging-only, tailnet-only, not yet public. Production host is undecided

## Audience & geography

- **Target audience**: leaders who hire a business psychologist for communication coaching (executive communication, executive presence, speaker coaching, leadership communication)
- **Primary geography / languages**: English. Markets named in the design: United Kingdom and United States. No hreflang work now
- **Local SEO relevant?**: no. Steve is not a local business. Do not run local or Google Business work

## Local SEO block (only if relevant — see docs/playbooks/local-seo-gbp-playbook.md)

Not relevant. Left blank on purpose.

## Search intent map

Head terms the design assigns to service or home pages (a plan, not a measured volume table): executive communication coaching, executive presence coaching, speaker coaching, leadership communication, communicating change.

- **Money queries** (convert): the head terms above, one primary target per URL, once a keyword map exists
- **Consideration queries** (compare/evaluate): unknown. No research run
- **Awareness queries** (learn): article drafts exist on staging; publishing waits on rights (not asked; D-7 is not approved)
- **AI prompt set** (25–100 fixed prompts used to measure share-of-answer): `data/prompts.txt` is a placeholder. The fixed set is not written

## Competitors

| Competitor | URL | Why they win today |
|---|---|---|
| — | — | No competitor list. Research is dormant |

## Goals & constraints

- **Primary goal**: be ready to measure demand and, after a public WordPress cutover, search performance. The design's own caveat: the lever is cutover and Steve's publishing decisions, not tooling
- **KPI baseline**: none for the WordPress site. It is not public and has no Search Console property. See `data/baseline.md`
- **Known problems**: evidenced defects are listed in `plans/backlog.md` as design findings. This folder does not repeat them as new observations
- **Out of scope / do-not-touch**: OpenSEO install (D-6), Search Console DNS change (D-3), any message to Steve (D-7), any paid or DataForSEO call, GA4 (D-8 is no), programmatic pages, mass FAQs, backlink outreach, local SEO, a second metadata plugin

## Access

- **Google Search Console**: not connected. No property for the WordPress site. When a property exists, access is via `gog`. D-3 (DNS verification) is not approved
- **Analytics**: none. D-8 keeps GA4 off. Conversions, later, would be Fluent Forms entries plus Search Console clicks
- **Deploy path**: WordPress staging, branch-per-task. Production host undecided. This SEO repo does not deploy the site
