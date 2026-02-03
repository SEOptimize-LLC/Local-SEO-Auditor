# Data Requirements — Pre-Audit Checklist

Prepare these reports before starting an audit. Drop them into the client's project folder and provide the folder path when invoking `/local-seo-audit`.

## Folder Structure

```
client-name/
├── data/
│   ├── semrush/
│   │   ├── domain-overview.csv
│   │   ├── organic-positions.csv
│   │   ├── keyword-gap.csv          (Phase 5)
│   │   ├── keyword-magic.csv        (Phase 5)
│   │   └── backlink-audit.csv       (Phase 11)
│   ├── gsc/
│   │   ├── keyword-performance.csv
│   │   └── page-performance.csv
│   ├── screaming-frog/              (only for 100+ URL sites)
│   │   ├── internal-html.csv
│   │   └── crawl-overview.csv
│   └── gbp/
│       └── insights-export.csv      (if available)
└── reports/                          (audit output goes here)
```

## Reports by Phase

### Phase 1 — Upfront (have ready before starting)

| Report | Source | How to Export |
|--------|--------|--------------|
| Keyword Performance | GSC | Performance > Search Results > Date range: last 16 months > Export (CSV) |
| Page Performance | GSC | Performance > Search Results > Pages tab > Export (CSV) |
| Domain Overview | Semrush | Enter domain in Domain Overview > Export (CSV) |
| Organic Positions | Semrush | Organic Research > Positions > Filter by country > Export (CSV) |

### Phase 5 — Keyword Research

| Report | Source | How to Export |
|--------|--------|--------------|
| Keyword Gap | Semrush | Keyword Gap > Enter your domain + 3 competitor domains > Export (CSV) |
| Keyword Magic Tool | Semrush | Enter seed keywords (your services + target locations) > Export (CSV) |

### Phase 9 — Technical SEO (only for sites with 100+ URLs)

| Report | Source | How to Export |
|--------|--------|--------------|
| Internal HTML Crawl | Screaming Frog | Run full crawl > File > Export > Internal > All (HTML) > Save as CSV |
| Crawl Overview | Screaming Frog | Reports > Crawl Overview > Export (CSV) |

### Phase 11 — Link Audit

| Report | Source | How to Export |
|--------|--------|--------------|
| Backlink Audit | Semrush | Backlink Audit > Export (CSV) — OR — Backlink Analytics > Backlinks > Export (CSV) |

### Optional — GBP Insights

| Report | Source | How to Export |
|--------|--------|--------------|
| GBP Insights | GBP Dashboard | Performance section > Export data (if available) |

## What If You Don't Have a Tool?

| Missing Tool | Impact | Mitigation |
|-------------|--------|------------|
| GSC | Loses actual click/impression data for existing keywords | DFS MCP provides estimated search volumes and SERP rankings |
| Semrush | Loses competitor keyword gap and backlink audit detail | DFS MCP covers keyword research, backlink analysis, and competitor data |
| Screaming Frog | Loses full crawl data for large sites | DFS MCP `on_page_instant_pages` analyzes individual pages; limit scope to key pages |
| GBP Dashboard | Loses actual GBP performance metrics | Audit still assesses GBP completeness; metrics come from post-audit tracking |

The audit never blocks on missing data. It works with what's available and notes gaps in the report.

## Future: MCP Integrations

When GSC and GA4 MCP servers are configured, these manual exports will no longer be needed — the auditor will pull data directly via API.
