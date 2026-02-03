---
name: local-seo-reporting
description: Master audit report compilation, three-channel scoring, priority classification, action plan generation, and KPI tracking framework
version: 1.0.0
tags: [local-seo, reporting, kpi, scoring, action-plan, audit-report]
related: [discovery-intake, gbp-audit, review-audit, local-citation-audit, local-on-page-audit, local-schema-markup, map-pack-analysis, technical-seo-local, local-keyword-research, local-content-strategy, local-link-audit, local-landing-pages, local-competitor-analysis, ai-search-visibility, site-architecture-local]
---

# Phase 16: Local SEO Reporting & KPIs

> **This is the FINAL phase of the Local SEO Auditor suite.** It compiles findings from all 15 preceding phases into a unified audit report with three-channel scoring, prioritized action items, and a measurable action plan. The report transforms raw audit data into a clear strategic roadmap that clients and implementation teams can execute against.

---

## When to Use This Skill

- **As the final step of the full Local SEO Audit**: Run this as Phase 16, after all individual audits are complete. This phase does not generate new audit data --- it synthesizes, scores, and prioritizes findings from Phases 1-15.
- **As a periodic reporting tool**: Run quarterly to re-score and track progress against baseline metrics established in the initial audit.
- **Trigger scenarios**:
  - Full audit is complete and needs to be compiled into a deliverable report
  - Quarterly progress review against baseline scores
  - Client presentation preparation
  - Annual strategy reset with updated benchmarks

---

## Prerequisites

Before compiling the final report, the following phases should be complete (or marked as not applicable):

| Phase | Skill | Status Required |
|-------|-------|----------------|
| 1 | `/discovery-intake` | Complete (required) |
| 2 | `/gbp-audit` | Complete (required for Map Pack score) |
| 3 | `/review-audit` | Complete (required for all channel scores) |
| 4 | `/local-citation-audit` | Complete (required for all channel scores) |
| 5 | `/local-on-page-audit` | Complete (required for Organic + AI scores) |
| 6 | `/local-schema-markup` | Complete (recommended) |
| 7 | `/map-pack-analysis` | Complete (recommended) |
| 8 | `/technical-seo-local` | Complete (recommended) |
| 9 | `/local-keyword-research` | Complete (recommended) |
| 10 | `/local-content-strategy` | Complete (recommended) |
| 11 | `/local-link-audit` | Complete (required for Organic score) |
| 12 | `/local-landing-pages` | Complete (recommended) |
| 13 | `/local-competitor-analysis` | Complete (recommended) |
| 14 | `/ai-search-visibility` | Complete (required for AI score) |
| 15 | `/site-architecture-local` | Complete (recommended) |

**Minimum Viable Report**: Phases 1-5 and 11 provide enough data for the core three-channel scores. Phases 6-10 and 12-15 enrich the report with deeper analysis and more precise recommendations.

---

## Three-Channel Score Calculation Methodology

The three-channel scoring model reflects how local search traffic is distributed across discovery channels, weighted by the 2025 Whitespark Local Search Ranking Factors Survey.

### Channel Click Share Weights

| Channel | Click Share | Description |
|---------|------------|-------------|
| **Local Map Pack** | **44%** | Google Maps pack (3-pack), Maps results, and local pack features |
| **Local Organic** | **30%** | Traditional organic results below the Map Pack for local-intent queries |
| **AI Search** | **26%** | ChatGPT, Gemini, Perplexity, AI Overviews (emerging, growing rapidly) |

---

### Map Pack Score Calculation

The Map Pack Score is a weighted sum of individual signal scores, where each signal weight comes from the 2025 Whitespark data for Map Pack ranking factors.

```
MAP PACK SCORE = (GBP Score * 0.32)
              + (Review Score * 0.20)
              + (On-Page Score * 0.15)
              + (Behavioral Score * 0.09)
              + (Link Score * 0.08)
              + (Citation Score * 0.06)
```

**Input Scores** (each normalized to 0-100 scale):

| Signal | Source Phase | How to Normalize |
|--------|------------|------------------|
| GBP Score | Phase 2: `/gbp-audit` | Direct score: GBP Health Score out of 100 |
| Review Score | Phase 3: `/review-audit` | Direct score: Review Health Score out of 100 |
| On-Page Score | Phase 5: `/local-on-page-audit` | Direct score: On-Page Score out of 100 |
| Behavioral Score | Phase 7: `/map-pack-analysis` | Estimated from CTR data, GBP Insights engagement metrics. If no data available, use 50 as neutral default. |
| Link Score | Phase 11: `/local-link-audit` | Direct score: Link Profile Score out of 100 |
| Citation Score | Phase 4: `/local-citation-audit` | Direct score: Citation Score out of 100 |

**Calculation Example**:
```
GBP Score: 75/100
Review Score: 60/100
On-Page Score: 70/100
Behavioral Score: 50/100 (default)
Link Score: 45/100
Citation Score: 80/100

Map Pack Score = (75 * 0.32) + (60 * 0.20) + (70 * 0.15)
              + (50 * 0.09) + (45 * 0.08) + (80 * 0.06)
             = 24.0 + 12.0 + 10.5 + 4.5 + 3.6 + 4.8
             = 59.4/100
```

---

### Organic Score Calculation

```
ORGANIC SCORE = (On-Page Score * 0.33)
             + (Link Score * 0.24)
             + (Review Score * 0.15)
             + (Citation Score * 0.10)
             + (Behavioral Score * 0.10)
             + (GBP Score * 0.07)
```

**Input Scores**: Same source phases as Map Pack, same normalization.

---

### AI Search Score Calculation

```
AI SCORE = (On-Page Score * 0.24)
        + (Social Score * 0.18)
        + (Review Score * 0.16)
        + (Citation Score * 0.13)
        + (Link Score * 0.13)
        + (GBP Score * 0.12)
        + (Behavioral Score * 0.04)
```

**Additional Input**:

| Signal | Source Phase | How to Normalize |
|--------|------------|------------------|
| Social Score | Phase 14: `/ai-search-visibility` | From social signals assessment (Section 14.4), normalized to 0-100 |

**Note**: If the AI Search Visibility audit (Phase 14) was completed, use the AI Visibility Score directly. If not, calculate from the formula above using available component scores, substituting 30 as a conservative default for Social Score.

---

### Overall Local SEO Score

```
OVERALL SCORE = (Map Pack Score * 0.44)
             + (Organic Score * 0.30)
             + (AI Score * 0.26)
```

This produces a single 0-100 score representing the business's overall local search visibility potential across all discovery channels.

---

### Score Calculation Template

```
==============================================================================
THREE-CHANNEL LOCAL SEO SCORE
==============================================================================

INPUT SCORES (0-100 scale):
  GBP Score:          ___/100  (from /gbp-audit)
  Review Score:       ___/100  (from /review-audit)
  On-Page Score:      ___/100  (from /local-on-page-audit)
  Link Score:         ___/100  (from /local-link-audit)
  Citation Score:     ___/100  (from /local-citation-audit)
  Behavioral Score:   ___/100  (from /map-pack-analysis or default 50)
  Social Score:       ___/100  (from /ai-search-visibility or default 30)

CHANNEL SCORES:
--------------------------------------------------------------
  MAP PACK SCORE:     ___/100
    = (GBP * 0.32) + (Review * 0.20) + (OnPage * 0.15)
    + (Behavioral * 0.09) + (Link * 0.08) + (Citation * 0.06)

  ORGANIC SCORE:      ___/100
    = (OnPage * 0.33) + (Link * 0.24) + (Review * 0.15)
    + (Citation * 0.10) + (Behavioral * 0.10) + (GBP * 0.07)

  AI SEARCH SCORE:    ___/100
    = (OnPage * 0.24) + (Social * 0.18) + (Review * 0.16)
    + (Citation * 0.13) + (Link * 0.13) + (GBP * 0.12)
    + (Behavioral * 0.04)

--------------------------------------------------------------
  OVERALL LOCAL SEO SCORE:  ___/100
    = (MapPack * 0.44) + (Organic * 0.30) + (AI * 0.26)

INTERPRETATION:
  85-100: Dominant --- strong visibility across all channels
  70-84:  Competitive --- well-positioned with room to improve
  50-69:  Average --- visible but significant gaps vs competitors
  30-49:  Below Average --- major investment needed
  0-29:   Critical --- foundational issues across multiple signals
==============================================================================
```

---

## Priority Classification System

Every finding from all phases must be classified into one of four priority levels. Priority determines the order of implementation in the action plan.

### Critical Priority

**Definition**: Issues that block ranking entirely, risk listing suspension, or cause immediate trust damage.

**Examples**:
- `noindex` tag on money pages (service or location pages)
- GBP suspension or suspension risk (name keyword stuffing)
- Business name does not match legal name in GBP
- GBP listing unverified
- Website is HTTP-only (no SSL)
- Robots.txt blocking critical pages from crawling
- Manual action or Google penalty detected
- NAP completely inconsistent across major platforms

**Action Timeline**: Immediately --- within 24-48 hours.

### High Priority

**Definition**: Issues with significant ranking impact that should be addressed in the first 30 days.

**Examples**:
- Low review count (below competitive threshold)
- Inaccurate or missing business hours in GBP
- Missing LocalBusiness schema markup
- Primary GBP category is wrong or too broad
- No location-specific landing pages for target cities
- Thin content on service pages (under 300 words)
- Missing title tags or H1 headers on local pages
- Mobile usability issues
- Slow page speed (LCP > 4 seconds)

**Action Timeline**: Within 30 days.

### Medium Priority

**Definition**: Issues with moderate ranking impact --- optimization opportunities rather than blockers.

**Examples**:
- Suboptimal title tags (present but not keyword-optimized)
- Missing secondary GBP categories
- Incomplete GBP attributes
- Missing image alt text with local keywords
- Blog content not linked to service pages
- Missing breadcrumb navigation
- Incomplete meta descriptions
- Photos older than 6 months on GBP

**Action Timeline**: Within 60 days.

### Low Priority

**Definition**: Minor optimizations that provide incremental improvement.

**Examples**:
- Photo captions and EXIF data optimization
- GBP attribute completeness (non-critical attributes)
- Additional Q&A seeding on GBP
- Social media profile optimization
- Internal linking refinements
- Content freshness updates on existing pages

**Action Timeline**: Within 90 days or as part of ongoing maintenance.

---

## Quick Wins Identification

Quick wins are items that combine HIGH IMPACT with LOW EFFORT. These should be executed first to generate early momentum and demonstrate value.

**Quick Win Criteria**:
- Can be completed in under 2 hours of work
- Does not require development resources or content creation
- Has measurable impact on at least one channel score
- Does not depend on completing other tasks first

**Common Quick Wins by Category**:

| Quick Win | Time | Impact | Channel |
|-----------|------|--------|---------|
| Fix GBP business name compliance | 15 min | Critical | Map Pack |
| Update GBP hours to match reality | 15 min | High | Map Pack |
| Add missing GBP secondary categories | 20 min | Medium | Map Pack |
| Set GBP holiday/special hours | 15 min | Medium | Map Pack |
| Complete GBP attributes | 30 min | Medium | Map Pack |
| Write optimized GBP description | 30 min | Medium | Map Pack |
| Add title tags to untagged local pages | 1 hour | High | Organic |
| Add H1 headers to pages missing them | 30 min | High | Organic |
| Fix broken internal links | 1 hour | Medium | Organic |
| Respond to unanswered Google reviews | 30 min | Medium | Map Pack |
| Claim missing social media profiles | 1 hour | Medium | AI Search |
| Add self-referencing canonical tags | 30 min | Medium | Organic |

---

## 30/60/90-Day Action Plan

The action plan organizes all findings into a phased implementation timeline. Reference the template at `templates/90-day-action-plan-template.md` for the full deliverable format.

### Days 1-30: Foundation & Critical Fixes

**Objectives**: Resolve all Critical and High priority items. Establish baseline metrics. Implement quick wins.

```
WEEK 1-2: CRITICAL FIXES
  [ ] Resolve any GBP compliance issues (name, verification)
  [ ] Fix any technical blockers (noindex, robots.txt, SSL)
  [ ] Correct GBP hours, category, and address
  [ ] Respond to all unanswered reviews
  [ ] Fix NAP inconsistencies on top 10 directories

WEEK 2-3: HIGH PRIORITY
  [ ] Implement LocalBusiness schema markup
  [ ] Optimize title tags and H1s on all local pages
  [ ] Add/update GBP photos (15+ minimum)
  [ ] Submit citation corrections to major platforms
  [ ] Begin review generation campaign

WEEK 3-4: QUICK WINS + MONITORING
  [ ] Complete all identified quick wins
  [ ] Set up rank tracking for target keywords
  [ ] Set up GBP Insights monitoring
  [ ] Establish review monitoring process
  [ ] Set up Google Search Console monitoring
```

### Days 31-60: Optimization & Content

**Objectives**: Address all Medium priority items. Begin content creation. Build initial links.

```
WEEK 5-6: ON-PAGE OPTIMIZATION
  [ ] Optimize all service page content (depth, keywords, structure)
  [ ] Create missing location landing pages
  [ ] Implement breadcrumb navigation
  [ ] Fix internal linking gaps and orphan pages
  [ ] Optimize images (alt text, compression, local keywords)

WEEK 7-8: CONTENT & LINKS
  [ ] Publish 2-4 locally relevant blog posts
  [ ] Begin local link building outreach
  [ ] Submit to remaining citation directories
  [ ] Start GBP posting schedule (2-3/week)
  [ ] Seed GBP Q&A with 5-10 questions
```

### Days 61-90: Growth & AI Visibility

**Objectives**: Address Low priority items. Focus on emerging channels. Establish maintenance cadence.

```
WEEK 9-10: AI & SOCIAL
  [ ] Optimize social media profiles for AI visibility
  [ ] Create 2-3 citable content pieces (local guides, FAQ pages)
  [ ] Pursue "Best of [City]" listicle placements
  [ ] Complete schema markup with all AI-relevant properties
  [ ] Run AI visibility baseline test (ChatGPT, Gemini, Perplexity)

WEEK 11-12: REFINEMENT & REPORTING
  [ ] Complete all Low priority items
  [ ] Re-run three-channel scoring to measure progress
  [ ] Generate first progress report
  [ ] Establish 12-month maintenance calendar
  [ ] Present results and ongoing strategy to client
```

---

## 12-Month Maintenance Framework

After the initial 90-day sprint, ongoing maintenance preserves and builds on gains.

### Monthly Tasks

| Task | Time | Responsible |
|------|------|-------------|
| Publish 2-4 blog posts with local relevance | 4-8 hrs | Content team |
| Post to GBP 2-3x/week | 2 hrs | Social/marketing |
| Monitor and respond to all new reviews within 48 hrs | 1-2 hrs | Client/team |
| Check GBP Insights for anomalies | 30 min | SEO team |
| Review rank tracking data for target keywords | 30 min | SEO team |
| Upload 3-5 new photos to GBP | 30 min | Client/team |
| Check for new citation inconsistencies | 30 min | SEO team |
| Monitor AI visibility for 3-5 key queries | 30 min | SEO team |

### Quarterly Tasks

| Task | Time | Responsible |
|------|------|-------------|
| Re-run three-channel scoring | 2-4 hrs | SEO team |
| Full GBP audit refresh | 2 hrs | SEO team |
| Review and update hours (seasonal adjustments) | 30 min | Client |
| Competitive landscape check (new competitors?) | 1-2 hrs | SEO team |
| Content gap analysis refresh | 1-2 hrs | SEO team |
| Link building outreach batch | 4-8 hrs | SEO team |
| Citation audit refresh | 1-2 hrs | SEO team |
| AI visibility re-test (full query set) | 1-2 hrs | SEO team |
| Client progress report generation | 2-4 hrs | SEO team |

---

## KPI Tracking Framework

### Baseline and Target Metrics

Establish baselines from the initial audit and set 90-day and 6-month targets.

```
==============================================================================
KPI TRACKING FRAMEWORK
==============================================================================

Metric                    | Baseline | 90-Day Target | 6-Month Target
--------------------------|----------|---------------|----------------
Overall Local SEO Score   |  ___/100 |   ___/100     |   ___/100
Map Pack Score            |  ___/100 |   ___/100     |   ___/100
Organic Score             |  ___/100 |   ___/100     |   ___/100
AI Search Score           |  ___/100 |   ___/100     |   ___/100
                          |          |               |
GBP Impressions/month     |  ___     |   ___         |   ___
GBP Actions/month         |  ___     |   ___         |   ___
GBP Calls/month           |  ___     |   ___         |   ___
GBP Direction Requests/mo |  ___     |   ___         |   ___
                          |          |               |
Google Review Count       |  ___     |   ___         |   ___
Google Average Rating     |  ___     |   ___         |   ___
Review Velocity/month     |  ___     |   ___         |   ___
                          |          |               |
Organic Traffic (local)   |  ___     |   ___         |   ___
Top 3 Keywords (count)    |  ___     |   ___         |   ___
Top 10 Keywords (count)   |  ___     |   ___         |   ___
                          |          |               |
Total Citations           |  ___     |   ___         |   ___
Citation Consistency %    |  ___%    |   ___%        |   ___%
                          |          |               |
AI Mention Rate           |  ___%    |   ___%        |   ___%
==============================================================================
```

---

## Expected Results by Milestone

Setting realistic expectations is critical for client retention and satisfaction.

### Week 2-3: Quick Win Results
- GBP profile completeness score jumps (often +15-25 points)
- GBP Insights may show early impression increases
- Review response rate reaches 100%
- Technical blockers resolved (noindex, SSL, robots.txt)
- **Client should see**: Cleaner GBP profile, faster website, initial review responses

### Week 4-6: Early Ranking Movement
- Local pack positions begin to shift (especially for less competitive keywords)
- GBP impressions trend upward (10-20% increase typical)
- New citations begin appearing in search
- First batch of new reviews arrives
- **Client should see**: Movement in rank tracking reports, growing review count

### Week 8-12: Measurable Improvement
- Map Pack positions solidify for primary keywords
- Organic rankings improve for optimized pages
- GBP actions (calls, directions, clicks) increase 20-40%
- Review count approaches competitive threshold
- Citation consistency reaches 90%+
- **Client should see**: More phone calls, more direction requests, higher rankings

### Month 4-6: Compounding Growth
- Organic traffic from local pages increases 30-60%
- AI visibility begins showing mentions
- Content strategy produces ranking blog posts
- Link building efforts compound
- **Client should see**: Measurable increase in leads/revenue from local search

---

## ROI Estimation Framework

Help clients understand the business value of local SEO improvements.

```
==============================================================================
ROI ESTIMATION
==============================================================================

CURRENT STATE:
  Monthly GBP Impressions:        [X]
  Monthly GBP Actions:            [X] (calls + directions + clicks)
  Estimated Action-to-Lead Rate:  [X%] (industry benchmark: 15-30%)
  Estimated Lead-to-Close Rate:   [X%] (client-provided or benchmark)
  Average Customer Value:         $[X] (client-provided)

CURRENT MONTHLY VALUE:
  Actions * Lead Rate * Close Rate * Customer Value = $[X]

PROJECTED STATE (after 6 months):
  Monthly GBP Impressions:        [X] (+[X]% increase)
  Monthly GBP Actions:            [X] (+[X]% increase)
  Same conversion rates applied

PROJECTED MONTHLY VALUE:
  Actions * Lead Rate * Close Rate * Customer Value = $[X]

INCREMENTAL MONTHLY VALUE: $[X]
ANNUAL INCREMENTAL VALUE:  $[X]

ROI = (Annual Value - Annual Investment) / Annual Investment * 100
==============================================================================
```

---

## Report Delivery Format

### Deliverable Structure

The final audit report should be delivered as outlined in `templates/audit-report-template.md` with the following sections:

```
MASTER LOCAL SEO AUDIT REPORT
==============================

1.  EXECUTIVE SUMMARY
    - Overall Score and channel breakdown
    - Top 3 critical findings
    - Top 5 quick wins
    - Expected ROI summary

2.  THREE-CHANNEL SCORECARD
    - Map Pack Score with breakdown
    - Organic Score with breakdown
    - AI Search Score with breakdown
    - Overall Score

3.  PHASE-BY-PHASE FINDINGS (Phases 2-15)
    - Each phase summary with score
    - Key findings per phase
    - Phase-specific action items

4.  COMPETITIVE LANDSCAPE
    - Competitor comparison matrix
    - Opportunity matrix
    - Competitive position score

5.  PRIORITIZED ACTION PLAN
    - Critical items (immediate)
    - High priority (30 days)
    - Medium priority (60 days)
    - Low priority (90 days)
    - Quick wins highlighted

6.  30/60/90-DAY IMPLEMENTATION PLAN
    - Week-by-week task breakdown
    - Resource requirements
    - Dependencies noted

7.  KPI TRACKING FRAMEWORK
    - Baseline metrics
    - 90-day targets
    - 6-month targets
    - Tracking cadence

8.  12-MONTH MAINTENANCE PLAN
    - Monthly task list
    - Quarterly review schedule

9.  ROI ESTIMATION
    - Current vs projected value
    - Annual incremental value

10. APPENDICES
    - Full scoring rubrics
    - Keyword research data
    - Citation inventory
    - Technical crawl data
    - Raw audit data
```

### Presentation Recommendations

- **Executive presentation**: 15-20 slides covering sections 1, 2, 4, 5, 7, and 9. Focus on scores, opportunities, and ROI.
- **Implementation handoff**: Full report PDF with sections 3, 5, and 6. Include checklists and templates.
- **Ongoing reporting**: Monthly one-page scorecard with KPI tracking and progress notes.

---

## Output Format

```
==============================================================================
PHASE 16: LOCAL SEO REPORTING & KPIs
==============================================================================

Business: [Business Name]
Report Date: [YYYY-MM-DD]
Audit Period: [Start Date] to [End Date]
Auditor: Claude Code (Local SEO Auditor)

==============================================================================
THREE-CHANNEL SCORECARD
==============================================================================

  MAP PACK SCORE:        [XX]/100
  ORGANIC SCORE:         [XX]/100
  AI SEARCH SCORE:       [XX]/100
  --------------------------------
  OVERALL LOCAL SEO SCORE: [XX]/100 --- [Dominant/Competitive/Average/
                                         Below Average/Critical]

==============================================================================
FINDINGS SUMMARY (By Priority)
==============================================================================

CRITICAL ([X] items):
  1. [Finding] --- Source: Phase [X]
  2. [Finding] --- Source: Phase [X]

HIGH ([X] items):
  1. [Finding] --- Source: Phase [X]
  2. [Finding] --- Source: Phase [X]
  ...

MEDIUM ([X] items):
  [Summarized list]

LOW ([X] items):
  [Summarized list]

QUICK WINS ([X] items):
  1. [Quick win] --- Est. time: [X min] --- Impact: [Channel]
  2. [Quick win] --- Est. time: [X min] --- Impact: [Channel]
  ...

==============================================================================
30/60/90-DAY ACTION PLAN (Summary)
==============================================================================

DAYS 1-30: [X] tasks --- Focus: [Critical fixes + foundation]
DAYS 31-60: [X] tasks --- Focus: [Optimization + content]
DAYS 61-90: [X] tasks --- Focus: [Growth + AI visibility]

==============================================================================
KPI TARGETS
==============================================================================

[Insert completed KPI Tracking Framework table]

==============================================================================
ROI PROJECTION
==============================================================================

Current Monthly Value:     $[X]
Projected Monthly Value:   $[X] (6-month target)
Annual Incremental Value:  $[X]

==============================================================================
```

---

## Cross-References

This phase references ALL other skills in the Local SEO Auditor suite:

| Phase | Skill | Data Used in Reporting |
|-------|-------|----------------------|
| 1 | `/discovery-intake` | Business context, target keywords, competitor list |
| 2 | `/gbp-audit` | GBP Health Score (feeds Map Pack, Organic, AI scores) |
| 3 | `/review-audit` | Review Health Score (feeds all three channel scores) |
| 4 | `/local-citation-audit` | Citation Score (feeds all three channel scores) |
| 5 | `/local-on-page-audit` | On-Page Score (feeds all three channel scores) |
| 6 | `/local-schema-markup` | Schema implementation findings |
| 7 | `/map-pack-analysis` | Map Pack positioning, behavioral signals |
| 8 | `/technical-seo-local` | Technical health, crawl data |
| 9 | `/local-keyword-research` | Target keyword list, search volumes |
| 10 | `/local-content-strategy` | Content gaps, content plan |
| 11 | `/local-link-audit` | Link Profile Score (feeds Organic and AI scores) |
| 12 | `/local-landing-pages` | Landing page quality assessment |
| 13 | `/local-competitor-analysis` | Competitive position, opportunity matrix |
| 14 | `/ai-search-visibility` | AI Visibility Score, Social Score |
| 15 | `/site-architecture-local` | Architecture score, structural recommendations |

---

*This is the final skill in the Local SEO Auditor suite. It transforms 15 phases of detailed audit work into a single, actionable report. The quality of this report depends entirely on the thoroughness of the preceding phases. For best results, complete all phases before compiling the final report. Use the three-channel scoring model to demonstrate value across Map Pack, Organic, and AI Search --- the three channels through which local customers discover businesses in 2026.*
