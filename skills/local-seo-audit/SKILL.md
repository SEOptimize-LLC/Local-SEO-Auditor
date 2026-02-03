---
name: local-seo-audit
description: Master orchestrator for comprehensive local SEO audit across 16 phases
version: 1.0.0
tags: [local-seo, audit, orchestrator, gbp, map-pack]
related: [discovery-intake, gbp-audit, review-audit, local-citation-audit, local-keyword-research, map-pack-analysis, local-on-page-audit, local-landing-pages, technical-seo-local, local-schema-markup, local-link-audit, local-content-strategy, local-competitor-analysis, ai-search-visibility, site-architecture-local, local-seo-reporting]
---

# Local SEO Audit — Master Orchestrator

## When to Use This Skill

Use `/local-seo-audit` when you need to run a comprehensive local SEO audit for a business. This skill orchestrates all 16 audit phases in sequence, collecting findings and compiling a final report with three-channel scoring.

You can also start at any specific phase if a partial audit is needed. The user can invoke individual phase skills directly (e.g., `/gbp-audit`, `/review-audit`).

## Three-Channel Scoring Model

All findings are scored against their impact on three distinct ranking channels (2025 Whitespark Survey & 2026 Local Search Ranking Factors):

| Channel | Click Share | Top Factors |
|---------|-------------|-------------|
| **Local Map Pack** | 44% | GBP (32%), Reviews (20%), On-Page (15%), Behavioral (9%), Links (8%), Citations (6%) |
| **Local Organic** | 30% | On-Page (33%), Links (24%), Reviews (15%), Behavioral (10%), Citations (10%), GBP (7%) |
| **AI Search** | Emerging | On-Page (24%), Social (18%), Reviews (16%), Citations (13%), Links (13%), GBP (12%) |

## Audit Workflow

Execute these phases in order. After each phase, compile findings before moving to the next.

### Phase 1: Discovery Intake (`/discovery-intake`)
Establish business context, audit scope, and data availability. Request upfront data exports from user.

**Gate:** Do not proceed until you have at minimum: business name, URL, GBP listing, target service area, and audit scope selection.

### Phase 2: GBP Audit (`/gbp-audit`) — FLAGSHIP
Audit the Google Business Profile listing. This is the single most impactful area for Local Map Pack (32% weight).

**Critical check:** Business Hours "Openness" signal — Google removes closed businesses from immediate-need queries entirely. This is a filter, not just a ranking signal.

### Phase 3: Review Audit (`/review-audit`) — FLAGSHIP
Audit review signals across all platforms. Reviews = 20% of Local Map Pack (doubled from prior estimates). This is the primary actionable ranking lever.

### Phase 4: Citation Audit (`/local-citation-audit`)
Audit NAP consistency and citation presence. Use bifurcated strategy: 50-75 quality citations for Map Pack, 100+ for AI Search.

### Phase 5: Keyword Research (`/local-keyword-research`)
Build local keyword map with service + location modifiers, near-me queries, and seasonal trends.

### Phase 6: Map Pack Analysis (`/map-pack-analysis`)
Analyze current map pack rankings, triggers, proximity factors, and competitive positioning.

### Phase 7: On-Page Audit (`/local-on-page-audit`)
Audit on-page elements through a local lens. On-Page = 15% Map Pack / 33% Organic / 24% AI Search.

### Phase 8: Landing Pages (`/local-landing-pages`)
Assess service pages and location pages for uniqueness, local signals, and content quality.

### Phase 9: Technical SEO (`/technical-seo-local`)
Audit technical issues that impact local SEO: crawlability, indexation, mobile, speed, redirects.

### Phase 10: Schema Markup (`/local-schema-markup`)
Validate structured data: LocalBusiness, Service, FAQ, Breadcrumb, AggregateRating, OpeningHours.

### Phase 11: Link Audit (`/local-link-audit`)
Assess backlink profile with channel-specific strategy. Links = 8% Map Pack / 24% Organic / 13% AI.

### Phase 12: Content Strategy (`/local-content-strategy`)
Evaluate local topical authority and build 90-day content calendar.

### Phase 13: Competitor Analysis (`/local-competitor-analysis`)
Deep-dive on top 3-5 local competitors across all ranking factors.

### Phase 14: AI Search Visibility (`/ai-search-visibility`)
Audit the emerging AI search channel: citations for AI, social signals, content citability.

### Phase 15: Site Architecture (`/site-architecture-local`)
Evaluate URL structure, internal linking, and silo architecture for local hierarchy.

### Phase 16: Reporting (`/local-seo-reporting`)
Compile all findings into the master audit report using the template in `templates/audit-report-template.md`.

## After Completing All Phases

1. Generate the final audit report using the template
2. Calculate three-channel scores using the weight tables above
3. Identify quick wins (high impact + low effort)
4. Build the 30/60/90-day action plan using `templates/90-day-action-plan-template.md`
5. Set KPI baselines and targets

## Handling Partial Audits

If the user only wants specific phases:
- Accept any combination of phases
- Still provide three-channel scoring for the phases completed
- Note which phases were skipped and what data may be missing
- Still generate a prioritized action plan from available findings

## Data Availability

If the user cannot provide certain exports (GSC, Semrush, Screaming Frog):
- Proceed with available data
- Use DFS MCP tools to fill gaps where possible
- Note data gaps in the report and how they limit findings
- Never block the audit because of missing data — work with what you have
