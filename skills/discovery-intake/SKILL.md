---
name: discovery-intake
description: Client & site discovery phase — establishes audit scope and gathers initial data
version: 1.0.0
tags: [local-seo, discovery, intake, scope]
related: [local-seo-audit, gbp-audit, review-audit]
---

# Phase 1: Discovery Intake

## When to Use This Skill

Use `/discovery-intake` at the start of any local SEO audit. This phase establishes the business context, defines audit scope, checks data availability, and requests upfront data exports from the user.

**Do not proceed to other phases until this discovery brief is complete.**

## Discovery Questions

Ask the user the following questions. Adapt based on what information is already available.

### 1. Business Information

```
REQUIRED:
- Business name (exact legal name as it appears on GBP)
- Business URL (primary website)
- GBP listing URL (or search for it)
- Business type: SAB (service area business), Storefront, Hybrid, Multi-location
- Physical address (if storefront/hybrid)
- Phone number
- Primary service category (what does the business do?)

HELPFUL:
- How long has the business been operating?
- When was the GBP listing created/last updated?
- Any recent changes to the business (name, address, phone, services)?
- Any previous SEO work done? If so, what and when?
- Any known Google penalties or manual actions?
```

### 2. Service & Location Details

```
REQUIRED:
- Primary services offered (list all)
- Primary service area (city, metro area, radius)
- Target locations/neighborhoods (specific areas they want to rank in)

HELPFUL:
- Secondary services
- Seasonal service patterns (e.g., HVAC more calls in summer/winter)
- Are there services they want to grow vs. maintain?
- Multiple locations? If so, list all addresses
```

### 3. Competitive Landscape

```
REQUIRED:
- Top 3-5 known local competitors (business names and/or URLs)

HELPFUL:
- Who do they lose business to most often?
- Any competitor they consider the "leader" in their area?
- Are there new competitors emerging?
```

### 4. Audit Scope Selection

Present these options to the user:

```
SCOPE OPTIONS:

A) FOCUSED AUDIT
   - Audit the GBP listing
   - Audit specific service page(s) or URL(s) you provide
   - Technical checks only where they directly impact those pages
   - Best for: Single service focus, quick assessment

B) SUBFOLDER AUDIT
   - Audit the GBP listing
   - Audit all URLs under a specific path (e.g., /services/, /locations/)
   - Technical checks scoped to that subfolder
   - Best for: Service-area businesses with organized URL structure

C) FULL SITE AUDIT
   - Audit the GBP listing
   - Audit the entire website through a local SEO lens
   - Full technical audit
   - Best for: Comprehensive assessment, new clients, major strategy shifts

NOTE FOR LARGE SITES (100+ URLs):
If the site has 100+ URLs and you select Subfolder or Full Site,
you'll need to provide a Screaming Frog crawl export (CSV).
The skill will process the export rather than crawling live.
```

### 5. Data Availability Check

Ask which tools/data the user has access to:

```
TOOLS AVAILABLE?
☐ Google Search Console (GSC) — access to the property?
☐ Semrush — active account?
☐ Screaming Frog — installed and licensed?
☐ DataForSEO API — via MCP tools (auto-available)
☐ Google Analytics (GA4) — access to the property?
☐ GBP Dashboard — owner/manager access?
```

### 6. Upfront Data Requests

Based on available tools, request these exports immediately so they're ready for later phases:

**From GSC (if available):**
- Performance > Search Results > Export (last 16 months, all queries) → CSV
- Performance > Search Results > Pages tab > Export → CSV

**From Semrush (if available):**
- Domain Overview for [target domain] > Export → CSV
- Organic Research > Positions > Export (filter by target country) → CSV

**From Screaming Frog (only if Full Site/Subfolder scope AND 100+ URLs):**
- Run crawl of [target URL or subfolder]
- File > Export > Internal > All (HTML only) → CSV
- Reports > Crawl Overview > Export → CSV

**From GBP Dashboard (if available):**
- Insights data (impressions, searches, actions — last 6 months)
- Review list export (if possible)
- Current photos list

## Output: Discovery Brief

After gathering all answers, compile a discovery brief in this format:

```markdown
## Discovery Brief

### Business Profile
- **Name:** [Legal business name]
- **URL:** [Primary website URL]
- **GBP:** [GBP listing URL]
- **Type:** [SAB / Storefront / Hybrid / Multi-location]
- **Address:** [Physical address or "Service Area Only"]
- **Phone:** [Primary phone]
- **Primary Category:** [Main GBP category]
- **Primary Services:** [List]
- **Service Area:** [City/metro + specific neighborhoods]

### Audit Configuration
- **Scope:** [Focused / Subfolder / Full Site]
- **Target URLs:** [Specific URLs or subfolder path]
- **Estimated URL Count:** [Approximate number of pages in scope]

### Competitors
1. [Competitor 1 — Name + URL]
2. [Competitor 2 — Name + URL]
3. [Competitor 3 — Name + URL]
4. [Competitor 4 — Name + URL (if applicable)]
5. [Competitor 5 — Name + URL (if applicable)]

### Data Available
- GSC: [Yes/No — exports requested/received]
- Semrush: [Yes/No — exports requested/received]
- Screaming Frog: [Yes/No — crawl requested/received]
- GA4: [Yes/No]
- GBP Dashboard: [Yes/No]
- DataForSEO MCP: [Available — auto]

### Data Gaps
[List any tools/exports not available and how this limits the audit]

### Notes
[Any additional context: recent changes, known issues, specific concerns]
```

## Proceeding to Phase 2

Once the discovery brief is complete, proceed to Phase 2: GBP Audit (`/gbp-audit`). Pass the discovery brief context to all subsequent phases.
