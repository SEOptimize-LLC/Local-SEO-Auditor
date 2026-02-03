---
name: local-competitor-analysis
description: Deep-dive competitive analysis across GBP, rankings, content, links, citations, and reviews for top local competitors
version: 1.0.0
tags: [local-seo, competitor-analysis, competitive-intelligence, map-pack, gap-analysis]
related: [gbp-audit, review-audit, local-link-audit, local-keyword-research, local-citation-audit, local-on-page-audit]
---

# Phase 13: Local Competitor Analysis

> **Competitive intelligence is the bridge between knowing what to optimize and knowing how much to optimize.** Every local market has its own competitive threshold --- the minimum level of reviews, links, citations, and content needed to rank. This skill systematically identifies those thresholds by dissecting the top 3-5 local competitors and mapping opportunities where the client can win.

---

## When to Use This Skill

- **As part of the full Local SEO Audit**: Run this as Phase 13, after individual signal audits (GBP, reviews, citations, links, on-page, content) have been completed. This phase synthesizes those findings into a relative competitive position.
- **As a standalone analysis**: When a client asks "Why is [Competitor X] outranking me?" or when entering a new market and needing to understand competitive intensity.
- **Trigger scenarios**:
  - Client has lost Map Pack positions to a specific competitor
  - New competitor has entered the market and is gaining visibility rapidly
  - Client is expanding into a new service area and needs competitive benchmarks
  - Pre-strategy planning to set realistic timelines and investment levels
  - Quarterly competitive monitoring to track shifts in the local landscape

---

## Channel Impact

Competitor analysis informs strategy across all three channels. The competitive gap determines effort required.

| Channel        | Relevance | Rationale |
|----------------|-----------|-----------|
| **Map Pack**   | **High**  | GBP completeness (32%), review count/velocity (20%), and citation coverage (6%) are directly comparable. Competitive thresholds define what "good enough" means in each market. |
| **Organic**    | **High**  | Link gap (24%), on-page quality (33%), and content depth are measurable competitive differentiators. Domain authority comparison reveals effort required. |
| **AI Search**  | **Medium** | Citation breadth (13%), social signals (18%), and content citability (24%) can be benchmarked against competitors. AI visibility is still emerging but measurable. |

---

## Prerequisites

Before beginning the competitor analysis, ensure you have:

1. **Discovery Brief from Phase 1** (`/discovery-intake`)
   - Top 3-5 competitors identified (from Map Pack and organic results)
   - Target keyword list (primary + secondary + long-tail)
   - Service area definition
   - Client business type (storefront vs. SAB vs. multi-location)

2. **Completed Individual Audits** (recommended but not required)
   - `/gbp-audit` --- Client GBP scores for comparison baseline
   - `/review-audit` --- Client review metrics for benchmarking
   - `/local-link-audit` --- Client backlink profile for gap analysis
   - `/local-keyword-research` --- Full keyword universe for overlap analysis
   - `/local-citation-audit` --- Client citation footprint

3. **Competitor Identification Verification**
   - Confirm competitors are true local competitors (same service area, same services)
   - Include at least one competitor that ranks above and one that ranks below the client
   - Include any competitor the client specifically mentions as a threat

---

## Assessment Framework

The competitor analysis is structured into eight assessment areas, each producing a relative comparison that feeds into the final opportunity matrix.

---

### 13.1 GBP Profile Comparison

Compare the client's GBP profile against each competitor across all auditable GBP elements.

**Data Collection Method**: Manually review each competitor's GBP listing in Google Maps, or use `mcp__dfs-mcp__business_data_business_listings_search` to pull structured data.

**Comparison Elements**:

| Element | What to Compare | Why It Matters |
|---------|----------------|----------------|
| Primary Category | Exact category match vs. target keywords | Category alignment determines which queries trigger the listing |
| Secondary Categories | Count and relevance of additional categories | Broader category coverage = broader query eligibility |
| Review Count | Total reviews across Google | Higher review count is a strong Map Pack signal (20% weight) |
| Average Rating | Star rating to one decimal place | Ratings below 4.0 suppress click-through; above 4.7 is optimal |
| Photo Count | Total owner + customer photos | Profiles with 25+ photos receive significantly more engagement |
| Post Frequency | Posts per week (check last 30 days) | Active profiles signal relevance; 2-3/week is current best practice |
| Business Hours | Opening/closing times, Mon-Sun | Determines Openness signal eligibility during competitive windows |
| Attributes | Count and types of attributes set | More attributes = richer profile = better matching |
| Description | Presence, length, keyword inclusion | Optimized descriptions improve click-through rates |
| Services Listed | Whether services/products section is populated | Additional keyword signals and user engagement |

**GBP Comparison Matrix Template**:

```
==============================================================================
GBP COMPETITIVE COMPARISON
==============================================================================

Element              | [Client]    | [Comp 1]    | [Comp 2]    | [Comp 3]
---------------------|-------------|-------------|-------------|-------------
Primary Category     |             |             |             |
Secondary Cat Count  |     /10     |     /10     |     /10     |     /10
Total Reviews        |             |             |             |
Average Rating       |     /5.0    |     /5.0    |     /5.0    |     /5.0
Review Velocity/mo   |             |             |             |
Photo Count          |             |             |             |
Post Frequency/wk    |             |             |             |
Mon Hours            |             |             |             |
Tue Hours            |             |             |             |
Wed Hours            |             |             |             |
Thu Hours            |             |             |             |
Fri Hours            |             |             |             |
Sat Hours            |             |             |             |
Sun Hours            |             |             |             |
Attributes Count     |             |             |             |
Description Quality  | Low/Med/Hi  | Low/Med/Hi  | Low/Med/Hi  | Low/Med/Hi
Services Listed      | Y/N         | Y/N         | Y/N         | Y/N
Name Compliant       | Y/N         | Y/N         | Y/N         | Y/N
==============================================================================
```

---

### 13.2 Hours Competitive Gap --- Openness Advantage Windows

This is a high-value competitive intelligence exercise. Google filters out closed businesses for immediate-need queries. Any time window where the client is open but competitors are closed represents a period of dramatically reduced competition.

**Analysis Process**:

1. Record full operating hours for the client and each competitor (Mon-Sun)
2. Identify windows where the client is the ONLY open option among the top 5
3. Identify windows where the client is closed but competitors are open (vulnerability)
4. Calculate total "exclusive open" hours per week

**Openness Advantage Table**:

```
==============================================================================
OPENNESS ADVANTAGE ANALYSIS
==============================================================================

Time Window          | Client | Comp 1 | Comp 2 | Comp 3 | Advantage?
---------------------|--------|--------|--------|--------|----------
Weekday Before 8 AM  |  O/C   |  O/C   |  O/C   |  O/C   | Y/N
Weekday 5-7 PM       |  O/C   |  O/C   |  O/C   |  O/C   | Y/N
Weekday After 7 PM   |  O/C   |  O/C   |  O/C   |  O/C   | Y/N
Saturday Morning     |  O/C   |  O/C   |  O/C   |  O/C   | Y/N
Saturday Afternoon   |  O/C   |  O/C   |  O/C   |  O/C   | Y/N
Sunday               |  O/C   |  O/C   |  O/C   |  O/C   | Y/N
Holidays             |  O/C   |  O/C   |  O/C   |  O/C   | Y/N
==============================================================================

EXCLUSIVE WINDOWS: [X] hours/week where client is only open option
VULNERABILITY WINDOWS: [X] hours/week where client is closed but
                       competitors are open
RECOMMENDATION: [Extend hours to cover X window / Maintain current advantage]
==============================================================================
```

**Strategic Recommendations**:
- If the client has exclusive windows: Highlight these in GBP posts, run Google Ads during these windows, mention availability in the business description
- If competitors have the advantage: Recommend extending hours where operationally feasible, or at minimum setting up after-hours call forwarding

---

### 13.3 Ranking Overlap Analysis

Determine which keywords the client and competitors share, and where each party ranks.

**DFS MCP Tools**:

```
TOOL: mcp__dfs-mcp__dataforseo_labs_google_ranked_keywords
USE:  Pull all ranked keywords for the client domain and each competitor domain.
      Compare overlap and relative positions.
PARAMETERS:
  - target: Domain to analyze (e.g., "competitor.com")
  - location_code: Target location code
  - language_code: "en"
  - limit: 100-500 (start with 100, increase if needed)
```

```
TOOL: mcp__dfs-mcp__dataforseo_labs_google_domain_intersection
USE:  Find keywords where both the client and a competitor rank.
      Identifies head-to-head competition.
PARAMETERS:
  - target1: Client domain
  - target2: Competitor domain
  - location_code: Target location code
  - language_code: "en"
  - limit: 100
```

**Python Code for Competitor Keyword Overlap Analysis**:

```python
import requests
import json
import base64
from collections import defaultdict

DFS_LOGIN = "your_login"
DFS_PASSWORD = "your_password"
DFS_AUTH = base64.b64encode(f"{DFS_LOGIN}:{DFS_PASSWORD}".encode()).decode()

def get_ranked_keywords(domain: str, location_code: int, limit: int = 200):
    """
    Pull all ranked keywords for a domain in a specific location.
    """
    url = "https://api.dataforseo.com/v3/dataforseo_labs/google/ranked_keywords/live"
    headers = {
        "Authorization": f"Basic {DFS_AUTH}",
        "Content-Type": "application/json"
    }
    payload = [{
        "target": domain,
        "location_code": location_code,
        "language_code": "en",
        "limit": limit,
        "order_by": ["keyword_data.keyword_info.search_volume,desc"]
    }]
    response = requests.post(url, headers=headers, json=payload)
    result = response.json()

    keywords = []
    if result.get("status_code") == 20000:
        tasks = result.get("tasks", [])
        if tasks and tasks[0].get("result"):
            for item in tasks[0]["result"][0].get("items", []):
                kw_data = item.get("keyword_data", {})
                keywords.append({
                    "keyword": kw_data.get("keyword"),
                    "position": item.get("ranked_serp_element", {}).get("serp_item", {}).get("rank_absolute"),
                    "search_volume": kw_data.get("keyword_info", {}).get("search_volume", 0),
                    "url": item.get("ranked_serp_element", {}).get("serp_item", {}).get("url", "")
                })
    return keywords


def get_domain_intersection(domain1: str, domain2: str, location_code: int, limit: int = 100):
    """
    Find keywords where both domains rank. Returns overlap with positions.
    """
    url = "https://api.dataforseo.com/v3/dataforseo_labs/google/domain_intersection/live"
    headers = {
        "Authorization": f"Basic {DFS_AUTH}",
        "Content-Type": "application/json"
    }
    payload = [{
        "target1": domain1,
        "target2": domain2,
        "location_code": location_code,
        "language_code": "en",
        "limit": limit,
        "order_by": ["keyword_data.keyword_info.search_volume,desc"]
    }]
    response = requests.post(url, headers=headers, json=payload)
    result = response.json()

    overlaps = []
    if result.get("status_code") == 20000:
        tasks = result.get("tasks", [])
        if tasks and tasks[0].get("result"):
            for item in tasks[0]["result"][0].get("items", []):
                kw_data = item.get("keyword_data", {})
                overlaps.append({
                    "keyword": kw_data.get("keyword"),
                    "search_volume": kw_data.get("keyword_info", {}).get("search_volume", 0),
                    "domain1_position": item.get("first_domain_serp_element", {}).get("serp_item", {}).get("rank_absolute"),
                    "domain2_position": item.get("second_domain_serp_element", {}).get("serp_item", {}).get("rank_absolute"),
                    "domain1_url": item.get("first_domain_serp_element", {}).get("serp_item", {}).get("url", ""),
                    "domain2_url": item.get("second_domain_serp_element", {}).get("serp_item", {}).get("url", "")
                })
    return overlaps


def competitive_keyword_analysis(client_domain: str, competitor_domains: list, location_code: int):
    """
    Full competitive keyword analysis: overlap, gaps, and opportunities.

    Returns:
        - shared_keywords: Keywords where client and competitors both rank
        - client_only: Keywords only the client ranks for (defend these)
        - competitor_only: Keywords competitors rank for but client does not (opportunities)
        - head_to_head: Keywords where client ranks lower than competitor (improve these)
    """
    client_keywords = get_ranked_keywords(client_domain, location_code)
    client_kw_set = {kw["keyword"] for kw in client_keywords}
    client_kw_map = {kw["keyword"]: kw for kw in client_keywords}

    all_competitor_keywords = defaultdict(list)
    competitor_only_keywords = []
    head_to_head = []

    for comp_domain in competitor_domains:
        intersection = get_domain_intersection(client_domain, comp_domain, location_code)

        for item in intersection:
            kw = item["keyword"]
            client_pos = item["domain1_position"]
            comp_pos = item["domain2_position"]

            if client_pos and comp_pos and client_pos > comp_pos:
                head_to_head.append({
                    "keyword": kw,
                    "client_position": client_pos,
                    "competitor": comp_domain,
                    "competitor_position": comp_pos,
                    "gap": client_pos - comp_pos,
                    "search_volume": item["search_volume"]
                })

        comp_keywords = get_ranked_keywords(comp_domain, location_code)
        for kw in comp_keywords:
            if kw["keyword"] not in client_kw_set:
                competitor_only_keywords.append({
                    "keyword": kw["keyword"],
                    "competitor": comp_domain,
                    "position": kw["position"],
                    "search_volume": kw["search_volume"]
                })

    # Sort by search volume descending
    head_to_head.sort(key=lambda x: x.get("search_volume", 0), reverse=True)
    competitor_only_keywords.sort(key=lambda x: x.get("search_volume", 0), reverse=True)

    return {
        "client_keyword_count": len(client_keywords),
        "head_to_head_losses": head_to_head[:50],
        "competitor_only_opportunities": competitor_only_keywords[:50],
        "client_exclusive_count": len([kw for kw in client_keywords
            if not any(kw["keyword"] in [i["keyword"] for i in get_domain_intersection(client_domain, cd, location_code)]
                       for cd in competitor_domains)])
    }


# Example usage:
# results = competitive_keyword_analysis(
#     "clientsite.com",
#     ["competitor1.com", "competitor2.com", "competitor3.com"],
#     1023191  # Dallas, TX
# )
# print(f"Head-to-head losses: {len(results['head_to_head_losses'])}")
# for loss in results['head_to_head_losses'][:10]:
#     print(f"  {loss['keyword']} (vol: {loss['search_volume']}): "
#           f"Client #{loss['client_position']} vs {loss['competitor']} #{loss['competitor_position']}")
```

---

### 13.4 Content Gap Analysis

Identify content topics and page types that competitors have but the client lacks.

**Assessment Areas**:

1. **Service Pages**: Does the competitor have dedicated pages for each service? Compare page count and depth.
2. **Location Pages**: Does the competitor have city/area-specific landing pages? How many vs. the client?
3. **Blog/Resource Content**: What local content does the competitor publish? (Local guides, seasonal tips, case studies)
4. **FAQ Content**: Does the competitor have FAQ pages or sections targeting long-tail queries?
5. **Content Depth**: Word count comparison for equivalent service pages (not for padding, but for topical coverage).

**Content Gap Matrix**:

```
==============================================================================
CONTENT GAP ANALYSIS
==============================================================================

Content Type           | Client | Comp 1 | Comp 2 | Comp 3 | Gap?
-----------------------|--------|--------|--------|--------|------
Service Pages          |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
Location Pages         |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
Blog Posts (last 12mo) |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
Case Studies           |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
FAQ Sections           |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
Video Content          |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
Local Guides           |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
Avg Service Page Words |   [X]  |   [X]  |   [X]  |   [X]  | Y/N
==============================================================================
```

---

### 13.5 Backlink Gap Analysis

Use DFS MCP to compare backlink profiles and identify link building opportunities.

```
TOOL: mcp__dfs-mcp__dataforseo_labs_google_competitors_domain
USE:  Identify the top competing domains in the same keyword space.
      Validates competitor list and may reveal competitors missed
      during discovery.
PARAMETERS:
  - target: Client domain
  - location_code: Target location code
  - language_code: "en"
  - limit: 20
```

**Backlink Comparison Points**:
- Total referring domains (client vs. each competitor)
- Domain authority / domain rank comparison
- Local link sources (chambers, associations, local news, sponsors)
- Link velocity (new referring domains per month)
- Anchor text distribution comparison
- Shared link sources (sites linking to competitors but not client = outreach targets)

---

### 13.6 Review Velocity Comparison

Review signals carry 20% weight in Map Pack and 15% in Organic. Competitive review benchmarking sets targets.

**Metrics to Compare**:

| Metric | Client | Comp 1 | Comp 2 | Comp 3 | Market Avg |
|--------|--------|--------|--------|--------|------------|
| Total Google Reviews | | | | | |
| Average Rating | | | | | |
| Reviews/Month (last 6mo) | | | | | |
| Owner Response Rate | | | | | |
| Avg Response Time | | | | | |
| Negative Review % | | | | | |
| Review Recency (last review date) | | | | | |

**Competitive Review Targets**:
- To compete in Map Pack: Client needs review count within 80% of the median competitor count
- To dominate: Client needs to exceed the highest competitor count AND maintain higher velocity
- Review velocity matters more than total count for recent algorithm behavior

---

### 13.7 Citation Coverage Comparison

Compare citation presence across major directories.

**Key Directories to Check** (use `mcp__dfs-mcp__business_data_business_listings_search`):
- Google Business Profile
- Yelp
- Facebook
- BBB
- Apple Maps
- Bing Places
- Industry-specific directories (Angi, HomeAdvisor, Avvo, Healthgrades, etc.)
- Local directories (city chamber, local news, community sites)

**Citation Comparison Table**:

```
Directory          | Client | Comp 1 | Comp 2 | Comp 3
-------------------|--------|--------|--------|--------
Google             |  Y/N   |  Y/N   |  Y/N   |  Y/N
Yelp               |  Y/N   |  Y/N   |  Y/N   |  Y/N
Facebook           |  Y/N   |  Y/N   |  Y/N   |  Y/N
BBB                |  Y/N   |  Y/N   |  Y/N   |  Y/N
Apple Maps         |  Y/N   |  Y/N   |  Y/N   |  Y/N
Bing Places        |  Y/N   |  Y/N   |  Y/N   |  Y/N
[Industry Dir 1]   |  Y/N   |  Y/N   |  Y/N   |  Y/N
[Industry Dir 2]   |  Y/N   |  Y/N   |  Y/N   |  Y/N
[Local Dir 1]      |  Y/N   |  Y/N   |  Y/N   |  Y/N
[Local Dir 2]      |  Y/N   |  Y/N   |  Y/N   |  Y/N
-------------------|--------|--------|--------|--------
TOTAL              |   /10  |   /10  |   /10  |   /10
```

---

### 13.8 Technical Comparison

Brief technical benchmarking across competitor websites.

**Elements to Compare**:
- Mobile-friendliness (responsive design)
- Page speed (Core Web Vitals: LCP, FID/INP, CLS)
- HTTPS implementation
- LocalBusiness schema presence
- Sitemap presence
- Robots.txt configuration

---

## Scoring: Relative Competitive Position Score

The competitive position score measures where the client stands relative to competitors on a 0-100 scale.

```
==============================================================================
COMPETITIVE POSITION SCORE
==============================================================================

Category (Weight)           | Client Score | Market Leader | Gap
----------------------------|--------------|---------------|-----
GBP Completeness (25%)     |    /100      |    /100       |  -X
Review Strength (25%)      |    /100      |    /100       |  -X
Content Coverage (15%)     |    /100      |    /100       |  -X
Backlink Authority (15%)   |    /100      |    /100       |  -X
Citation Coverage (10%)    |    /100      |    /100       |  -X
Technical SEO (10%)        |    /100      |    /100       |  -X
----------------------------|--------------|---------------|-----
WEIGHTED TOTAL              |    /100      |    /100       |  -X

INTERPRETATION:
  80-100: Market leader position — focus on defense and maintenance
  60-79:  Strong contender — targeted improvements can achieve leadership
  40-59:  Mid-pack — significant investment needed across multiple areas
  20-39:  Behind the competition — prioritize high-impact gaps first
  0-19:   Major competitive disadvantage — foundational work required
==============================================================================
```

---

## Opportunity Matrix

The culminating deliverable: a prioritized matrix of competitive opportunities.

```
==============================================================================
OPPORTUNITY MATRIX
==============================================================================

Opportunity                | Impact | Effort | Priority | Competitor Ref
---------------------------|--------|--------|----------|---------------
[e.g., Add 50 reviews]    | High   | Medium | 1        | Comp 1 has 200
[e.g., Build 10 local     |        |        |          |
 backlinks]               | High   | High   | 2        | Comp 2 has 45 RDs
[e.g., Create 5 location  |        |        |          |
 pages]                   | Medium | Medium | 3        | All comps have them
[e.g., Extend Sat hours]  | Medium | Low    | 4        | Only open option
[e.g., Add schema markup] | Medium | Low    | 5        | 2/3 comps have it
[e.g., Increase post freq]| Low    | Low    | 6        | Comp 3 posts 3x/wk
==============================================================================

LEGEND: Impact = ranking/traffic effect, Effort = time/cost to implement
PRIORITY: Impact/Effort ratio (High impact + Low effort = highest priority)
==============================================================================
```

---

## DFS MCP Data Sources

| Tool | Purpose |
|------|---------|
| `mcp__dfs-mcp__dataforseo_labs_google_competitors_domain` | Identify top competing domains in the same keyword space |
| `mcp__dfs-mcp__dataforseo_labs_google_domain_intersection` | Find shared keywords between client and each competitor |
| `mcp__dfs-mcp__dataforseo_labs_google_ranked_keywords` | Pull all ranked keywords for any domain to compare coverage |
| `mcp__dfs-mcp__business_data_business_listings_search` | Search business listings for citation and GBP comparison |
| `mcp__dfs-mcp__serp_organic_live_advanced` | Verify current SERP positions for target keywords |

---

## Output Format

```
==============================================================================
PHASE 13: LOCAL COMPETITOR ANALYSIS
==============================================================================

Business: [Client Business Name]
Competitors Analyzed: [Comp 1], [Comp 2], [Comp 3]
Analysis Date: [YYYY-MM-DD]
Auditor: Claude Code (Local SEO Auditor)

------------------------------------------------------------------------------
COMPETITIVE POSITION SCORE: [XX]/100
------------------------------------------------------------------------------

[Insert GBP Comparison Matrix]
[Insert Openness Advantage Analysis]
[Insert Keyword Overlap Summary]
[Insert Content Gap Matrix]
[Insert Backlink Gap Summary]
[Insert Review Velocity Comparison]
[Insert Citation Coverage Comparison]
[Insert Technical Comparison]

------------------------------------------------------------------------------
OPPORTUNITY MATRIX (Top 10 Prioritized Actions)
------------------------------------------------------------------------------
[Insert completed Opportunity Matrix]

------------------------------------------------------------------------------
KEY FINDINGS
------------------------------------------------------------------------------
STRENGTHS (Defend):
  1. [Area where client leads competitors]
  2. [Area where client leads competitors]

WEAKNESSES (Close Gap):
  1. [Largest competitive gap with recommended action]
  2. [Second largest gap with recommended action]
  3. [Third largest gap with recommended action]

QUICK WINS (High Impact + Low Effort):
  1. [Quick win opportunity]
  2. [Quick win opportunity]

==============================================================================
```

---

## Cross-References

| Skill | Relationship | When to Use Together |
|-------|-------------|----------------------|
| `/gbp-audit` | **Input** --- Client GBP scores provide the baseline for GBP comparison. Competitor GBP data collected here enriches the GBP audit findings. | GBP audit should be completed first; competitor analysis adds the relative context. |
| `/review-audit` | **Input** --- Client review metrics provide baseline. Competitor review velocity sets the target the client must reach or exceed. | Review audit provides depth; competitor analysis provides the benchmark. |
| `/local-link-audit` | **Input** --- Client backlink profile is the baseline. Backlink gap analysis here identifies specific outreach targets (sites linking to competitors but not client). | Link audit assesses quality; competitor analysis identifies acquisition opportunities. |
| `/local-keyword-research` | **Input** --- Target keyword list drives the ranking overlap analysis. Competitor-only keywords discovered here feed back as new keyword opportunities. | Keyword research defines the battlefield; competitor analysis shows who controls each position. |
| `/local-citation-audit` | **Input** --- Client citation footprint provides the baseline. Citation coverage comparison here identifies directories where competitors are present but client is not. | Citation audit checks accuracy; competitor analysis checks coverage breadth. |
| `/local-on-page-audit` | **Input** --- Client on-page quality provides baseline. Content gap and technical comparison here identify specific page-level improvements. | On-page audit assesses the client site; competitor analysis reveals what "good" looks like in this market. |

---

*This skill synthesizes findings from multiple individual audits into a relative competitive picture. For best results, complete Phases 2-12 before running this analysis. The opportunity matrix produced here directly feeds into the action plan generated in `/local-seo-reporting` (Phase 16).*
