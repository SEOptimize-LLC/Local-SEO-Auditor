# Local SEO Auditor - Claude Code Instructions

## Project Overview

This is a comprehensive Local SEO Audit skill suite for Claude Code. It provides a sequential 16-phase audit workflow that scores findings across three distinct ranking channels based on the 2025 Whitespark Survey & 2026 Local Search Ranking Factors.

## Three-Channel Scoring Model

Every audit finding MUST be evaluated against its impact on all three channels:

| Channel | Click Share | Weight Distribution |
|---------|-------------|---------------------|
| **Local Map Pack** | 44% | GBP 32%, Reviews 20%, On-Page 15%, Behavioral 9%, Links 8%, Citations 6%, Personalization 6%, Social 4% |
| **Local Organic** | 30% | On-Page 33%, Links 24%, Reviews 15%, Behavioral 10%, Citations 10%, GBP 7% |
| **AI Search** | Emerging | On-Page 24%, Social 18%, Reviews 16%, Citations 13%, Links 13%, GBP 12%, Behavioral 4% |

## Knowledge Base

The file `Knowledge Base/local_seo_audit_2026.md` contains the authoritative reference data:
- 2025 Whitespark survey ranking factor weights
- Business Hours "Openness" critical filter documentation
- GBP compliance requirements (August 2025)
- Review generation frameworks and targets
- Citation bifurcated strategy (Map Pack vs AI)
- 90-day recovery timeline
- Schema markup templates
- On-page optimization templates

Always reference this file for ranking factor weights and audit benchmarks.

## Default Tool Stack

### Auto-fetched (DFS MCP)
The following DataForSEO MCP tools are available and should be used as the primary data source:
- `mcp__dfs-mcp__serp_organic_live_advanced` — SERP results
- `mcp__dfs-mcp__kw_data_google_ads_search_volume` — Keyword volumes
- `mcp__dfs-mcp__dataforseo_labs_google_keyword_suggestions` — Keyword suggestions
- `mcp__dfs-mcp__dataforseo_labs_google_keyword_ideas` — Keyword ideas
- `mcp__dfs-mcp__dataforseo_labs_search_intent` — Search intent classification
- `mcp__dfs-mcp__on_page_instant_pages` — On-page analysis
- `mcp__dfs-mcp__on_page_lighthouse` — Lighthouse scores
- `mcp__dfs-mcp__backlinks_summary` — Backlink overview
- `mcp__dfs-mcp__backlinks_backlinks` — Backlink list
- `mcp__dfs-mcp__backlinks_competitors` — Backlink competitors
- `mcp__dfs-mcp__backlinks_domain_intersection` — Domain intersection
- `mcp__dfs-mcp__dataforseo_labs_google_competitors_domain` — Competitor domains
- `mcp__dfs-mcp__dataforseo_labs_google_ranked_keywords` — Ranked keywords
- `mcp__dfs-mcp__dataforseo_labs_google_domain_intersection` — Domain keyword overlap
- `mcp__dfs-mcp__business_data_business_listings_search` — Business listings
- `mcp__dfs-mcp__content_analysis_search` — Content analysis
- `mcp__dfs-mcp__kw_data_dfs_trends_explore` — Keyword trends

**CRITICAL — API Cost Optimization:**
Most DFS API endpoints support up to **2,000 requests per single API call** via batch/array payloads. You MUST always batch requests to minimize API costs:
- **ALWAYS** read the DFS MCP tool documentation before making calls (use `mcp__dfs-mcp__tools_documentation` or `mcp__n8n-mcp__tools_documentation` to check parameters)
- **ALWAYS** batch multiple keywords, URLs, or domains into a single API call instead of making individual calls
- Example: To get search volume for 50 keywords, send ALL 50 in one `kw_data_google_ads_search_volume` call — NOT 50 separate calls
- Example: To check SERP results for 20 keywords, send ALL 20 in one `serp_organic_live_advanced` call
- This reduces API costs by up to 2,000x
- If unsure whether an endpoint supports batching, check the documentation FIRST

### User-Provided Data

See `templates/data-requirements.md` for the full list of reports, how to export them, and recommended folder structure.

The user will provide a project folder path at the start of each audit containing data exports in a `data/` subfolder. Reports are organized by source:
- `data/semrush/` — Domain Overview, Organic Positions, Keyword Gap, Keyword Magic, Backlink Audit
- `data/gsc/` — Keyword Performance (last 16 months), Page Performance
- `data/screaming-frog/` — Full crawl export (only for sites with 100+ URLs)
- `data/gbp/` — GBP Insights export (if available)

When reading user-provided CSVs, always check the file exists before processing. If a report is missing, note the gap and proceed with available data + DFS MCP tools.

## Audit Workflow

The master orchestrator (`/local-seo-audit`) runs phases sequentially:
1. Discovery Intake → 2. GBP Audit → 3. Review Audit → 4. Citation Audit →
5. Keyword Research → 6. Map Pack Analysis → 7. On-Page Audit →
8. Landing Pages → 9. Technical SEO → 10. Schema Markup →
11. Link Audit → 12. Content Strategy → 13. Competitor Analysis →
14. AI Search Visibility → 15. Site Architecture → 16. Reporting

Each phase skill can also be invoked independently via its slash command.

## Scoring Guidelines

- Score each area on a 0-100 scale
- Use the channel weights above to compute weighted channel scores
- Priority levels: Critical (blocks ranking), High (significant impact), Medium (moderate impact), Low (minor optimization)
- Quick wins: Items that are high-impact AND low-effort

## Output Standards

- All reports in markdown format
- Use the templates in `templates/` for consistent formatting
- Include actionable recommendations with specific steps
- Reference the 30/60/90-day timeline from the knowledge base
- Always include KPI tracking framework with baseline and target metrics
