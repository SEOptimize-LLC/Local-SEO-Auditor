# Local SEO Auditor

Comprehensive Local SEO audit skills for Claude Code. Runs a sequential 16-phase audit workflow that scores findings across three ranking channels: Local Map Pack, Local Organic, and AI Search Visibility.

Based on the **2025 Whitespark Survey & 2026 Local Search Ranking Factors**.

## Installation

### Claude Code Plugin (Recommended)

```bash
claude plugin add SEOptimize-LLC/Local-SEO-Auditor
```

### Clone and Copy

```bash
git clone https://github.com/SEOptimize-LLC/Local-SEO-Auditor.git
cp -r Local-SEO-Auditor/skills/ ~/.claude/skills/
```

### Git Submodule

```bash
git submodule add https://github.com/SEOptimize-LLC/Local-SEO-Auditor.git .claude/local-seo-auditor
```

## Usage

### Full Audit

```
/local-seo-audit
```

Runs all 16 phases sequentially. The discovery phase establishes scope and requests necessary data exports.

### Individual Skills

Each phase can be invoked independently:

| Command | Phase | Description |
|---------|-------|-------------|
| `/local-seo-audit` | Orchestrator | Full sequential audit |
| `/discovery-intake` | 1 | Client & site discovery, scope selection |
| `/gbp-audit` | 2 | Google Business Profile audit (flagship) |
| `/review-audit` | 3 | Review signals audit (flagship) |
| `/local-citation-audit` | 4 | NAP & citation consistency |
| `/local-keyword-research` | 5 | Local keyword analysis |
| `/map-pack-analysis` | 6 | Local pack & SERP analysis |
| `/local-on-page-audit` | 7 | On-page optimization for local |
| `/local-landing-pages` | 8 | Location & service page audit |
| `/technical-seo-local` | 9 | Technical issues affecting local SEO |
| `/local-schema-markup` | 10 | Structured data for local |
| `/local-link-audit` | 11 | Local backlink analysis |
| `/local-content-strategy` | 12 | Local content & topical authority |
| `/local-competitor-analysis` | 13 | Competitor deep-dive |
| `/ai-search-visibility` | 14 | AI search visibility audit |
| `/site-architecture-local` | 15 | URL structure & hierarchy |
| `/local-seo-reporting` | 16 | Final report & KPIs |

## Three-Channel Scoring

Every finding is scored against all three ranking channels:

| Channel | Click Share | Top Ranking Factors |
|---------|-------------|---------------------|
| Local Map Pack | 44% | GBP (32%), Reviews (20%), On-Page (15%) |
| Local Organic | 30% | On-Page (33%), Links (24%), Reviews (15%) |
| AI Search | Emerging | On-Page (24%), Social (18%), Reviews (16%), Citations (13%) |

## Data Sources

### Automatic (DataForSEO MCP)
The skills automatically pull live data via 16+ DataForSEO MCP endpoints for SERP results, keyword volumes, backlink profiles, on-page analysis, business listings, and more.

### User-Provided Exports

| Phase | Source | Export |
|-------|--------|--------|
| 1 (Discovery) | GSC | Keyword + Page Performance (last 16 months) |
| 1 (Discovery) | Semrush | Domain Overview + Organic Positions |
| 5 (Keywords) | Semrush | Keyword Gap + Keyword Magic Tool |
| 9 (Technical) | Screaming Frog | Full crawl export (100+ URL sites only) |
| 11 (Links) | Semrush | Backlink Audit |

## Audit Scope Options

Set during the discovery phase:

- **Focused** — GBP listing + specific service page(s)
- **Subfolder** — GBP listing + URLs under a specific path
- **Full Site** — GBP listing + entire website (local lens)

For large sites (100+ URLs), the skill requests a Screaming Frog crawl export instead of live-crawling.

## Output

The audit produces a comprehensive markdown report including:
- Overall Local SEO Score (composite of three channels)
- Channel-specific scores (Map Pack, Organic, AI Search)
- Detailed findings by phase with prioritized recommendations
- 30/60/90-day action plan
- 12-month maintenance framework
- KPI tracking framework with baselines and targets

## License

MIT
