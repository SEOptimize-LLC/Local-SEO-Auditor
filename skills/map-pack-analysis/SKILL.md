---
name: Map Pack Analysis
description: Phase 6 of the Local SEO Audit suite. Analyzes current Map Pack rankings, identifies which queries trigger local packs, assesses proximity factors, evaluates SERP features, and maps competitive positioning. Produces a Map Pack competitive position report with ranking factor attribution and opportunity gaps.
version: 1.0.0
tags: [local-seo, map-pack, local-pack, serp-analysis, google-maps, proximity]
related:
  - local-keyword-research (Phase 5)
  - local-on-page-audit (Phase 7)
  - local-landing-pages (Phase 8)
  - local-gbp-audit (Phase 1)
  - local-review-strategy (Phase 2)
---

# Phase 6: Map Pack Analysis

## When to Use

Run this skill when:
- Performing a full Local SEO audit (Phase 6, after keyword research is complete)
- A client has lost Map Pack visibility for previously-ranking keywords
- Evaluating competitive positioning in the local pack for target keywords
- Assessing the impact of a new competitor entering the local market
- Determining which ranking factors to prioritize for Map Pack improvement
- Planning a local ranking strategy for a new location or service area

## Channel Impact

The Local Map Pack captures approximately 44% of all clicks for local queries. This is the single highest-value SERP real estate for local businesses.

### Map Pack Ranking Factor Breakdown (2025 Whitespark Survey)

| Factor           | Weight | What It Means                                              |
|------------------|--------|------------------------------------------------------------|
| GBP Signals      | 32%    | Categories, completeness, posts, Q&A, attributes           |
| Review Signals   | 20%    | Volume, velocity, diversity, rating, keywords in reviews   |
| On-Page Signals  | 15%    | NAP on site, local content, schema, title tags             |
| Behavioral Signals | 9%   | CTR from SERP, calls, direction requests, dwell time       |
| Link Signals     | 8%     | Domain authority, local link relevance, anchor text        |
| Citation Signals | 6%     | NAP consistency, citation volume, authority of sources     |

**Key Insight:** GBP + Reviews = 52% of Map Pack ranking factors. If Phases 1 and 2 scored poorly, Map Pack performance will be fundamentally limited regardless of other optimizations.

### SERP Feature Landscape for Local Queries

| SERP Feature        | Frequency for Local Queries | Opportunity Level |
|---------------------|----------------------------|-------------------|
| Local Map Pack (3-pack) | 85-93% of local intent queries | Primary target  |
| Local Organic Results | 100%                       | Secondary target  |
| People Also Ask     | 60-70%                     | Content opportunity |
| AI Overview         | 15-25% (growing)           | Emerging opportunity |
| Local Services Ads  | 30-40% (service verticals) | Paid consideration |
| Knowledge Panel     | Branded queries             | GBP-driven        |
| Images              | 20-30%                     | GBP photo optimization |

## Prerequisites

Before running this skill, you should have:
1. **Phase 5 (Keyword Research)** completed with the prioritized keyword list
2. **Phase 1 (GBP Audit)** completed to understand current GBP health
3. **Business address** for proximity analysis
4. **Top 3-5 competitors** identified with their addresses
5. **Target keyword list** categorized by service and location

## Assessment Framework

### Step 1: Map Pack Trigger Analysis

Not all queries trigger a Map Pack. Determine which target keywords display local packs.

```
TRIGGER CLASSIFICATION:
=======================

Always Triggers Map Pack:
- [service] + [city]        (e.g., "plumber austin")
- [service] + "near me"     (e.g., "plumber near me")
- "best" + [service] + [city] (e.g., "best plumber austin")

Usually Triggers Map Pack:
- [problem] + [city]        (e.g., "burst pipe austin")
- [service] + [action]      (e.g., "hire plumber austin")

Sometimes Triggers Map Pack:
- [service] alone            (e.g., "plumber" - depends on user location)
- [problem] alone            (e.g., "burst pipe repair")

Rarely Triggers Map Pack:
- Informational queries      (e.g., "how to fix a leaky faucet")
- Comparison queries         (e.g., "plumber vs handyman")
- Cost queries               (e.g., "plumber cost per hour")
```

**Action:** For each P1 and P2 keyword from Phase 5, verify whether a Map Pack appears in the SERP. Record the pack size (typically 3 results) and position on the page.

### Step 2: Current Ranking Position Assessment

For each keyword that triggers a Map Pack, determine:

```
RANKING POSITION MATRIX:
========================

| Keyword | Map Pack Position | In 3-Pack? | Organic Position | SERP Features Present |
|---------|-------------------|------------|------------------|----------------------|
| [kw1]   | #2                | Yes        | #5               | PAA, AI Overview     |
| [kw2]   | Not in pack       | No         | #12              | PAA                  |
| [kw3]   | #1                | Yes        | #3               | Images, PAA          |
```

**Categorize each keyword:**
- **Defending:** Currently in 3-pack, maintain position
- **Striking Distance:** Position 4-7 in Maps, push into 3-pack
- **Building:** Not in top 7, needs significant investment
- **Not Triggered:** Query does not show Map Pack

### Step 3: Proximity Factor Assessment

Proximity to the searcher is a ranking factor that cannot be directly optimized but must be understood.

```
PROXIMITY ANALYSIS:
===================

1. Business Location: [address]
2. City Centroid Distance: [X miles from city center]
3. Service Area Radius: [X miles]

Proximity Impact Assessment:
- Core Zone (0-3 miles): Expected strong Map Pack presence
- Mid Zone (3-7 miles): Competitive, need strong signals to compensate
- Outer Zone (7+ miles): Proximity disadvantage, must dominate other factors

Competitor Proximity Comparison:
| Competitor        | Distance to Centroid | Avg Map Pack Position |
|-------------------|---------------------|-----------------------|
| [Competitor A]    | 1.2 miles           | #1                    |
| [Client]          | 3.5 miles           | #3                    |
| [Competitor B]    | 5.1 miles           | #5                    |
```

**Key Insight:** When a competitor is closer to the centroid and outranks you, improving GBP, reviews, and on-page signals is the only path forward. When you are closer but still outranked, there is a clear signal gap to diagnose.

### Step 4: Local Pack Feature Analysis

Analyze what information and features appear in the Map Pack results for target queries.

```
FEATURE ANALYSIS PER KEYWORD:
==============================

Justifications Shown:
- Website mentions (Google pulls text from your site)
- Review mentions (Google pulls text from reviews)
- Post mentions (Google pulls text from GBP posts)
- Service mentions (from GBP services list)

Attributes Displayed:
- Business hours / "Open now"
- Price range ($, $$, $$$)
- Service options (e.g., "Offers online estimates")
- Amenities (e.g., "Wheelchair accessible")
- Health & safety (e.g., "Mask required")

Visual Elements:
- Photos shown in pack
- Logo displayed
- Street View image used

Engagement Elements:
- Star rating + review count
- "X years in business"
- Response time indicator
- Phone number displayed
```

**Action:** For each feature that competitors display but the client does not, create a specific action item tied to Phase 1 (GBP), Phase 2 (Reviews), or Phase 7 (On-Page).

### Step 5: Competitive Positioning Analysis

Build a comprehensive competitive comparison for Map Pack performance.

```
COMPETITIVE MAP PACK SCORECARD:
================================

| Factor              | Client | Comp A | Comp B | Comp C | Advantage? |
|---------------------|--------|--------|--------|--------|------------|
| GBP Completeness    | 85%    | 95%    | 70%    | 80%    | Comp A     |
| Review Count        | 47     | 123    | 89     | 35     | Comp A     |
| Avg Rating          | 4.6    | 4.8    | 4.3    | 4.9    | Comp C     |
| Review Recency      | 2 wks  | 3 days | 1 mo   | 1 wk   | Comp A     |
| Website DA          | 25     | 35     | 28     | 20     | Comp A     |
| NAP Consistency     | 90%    | 95%    | 80%    | 85%    | Comp A     |
| Photos              | 12     | 45     | 20     | 8      | Comp A     |
| GBP Posts (90 days) | 2      | 8      | 0      | 4      | Comp A     |
| Proximity (mi)      | 3.5    | 1.2    | 4.0    | 2.8    | Comp A     |
| Avg Map Pack Pos    | 3.2    | 1.5    | 4.1    | 3.8    | Comp A     |
```

### Step 6: Grid-Based Ranking Concept

For businesses serving a geographic area, Map Pack rankings vary by the searcher's location. A grid-based analysis reveals ranking strength across the service area.

```
GRID ANALYSIS CONCEPT (Local Falcon Style):
=============================================

Overlay a grid of points across the service area. For each grid point,
check the Map Pack ranking for target keywords as if searching from
that location.

Grid Setup:
- Center: Business address
- Radius: Service area radius (e.g., 10 miles)
- Grid Points: 25-49 points (5x5 or 7x7 grid)
- Keywords: Top 3-5 P1 keywords

Output per grid point:
- Map Pack position (1-7 or "not ranked")
- Which competitors appear
- Distance from business location

Visualization:
- Green: Position 1-3 (in the 3-pack)
- Yellow: Position 4-7 (in Maps but not 3-pack)
- Red: Not ranked in top 7

This analysis requires Local Falcon, BrightLocal, or manual
spot-checking. DFS SERP API can approximate by setting different
location parameters.
```

### Step 7: "Openness" Filter Impact

Google increasingly filters Map Pack results by business hours. Evaluate the competitive landscape when the "Open now" filter is applied.

```
OPENNESS ANALYSIS:
==================

Client Hours: Mon-Fri 8AM-5PM

Impact Assessment:
- Weekday evenings (5PM-9PM): Client drops out, competitors [X, Y] gain
- Weekends: Client drops out, competitors [X, Y, Z] appear
- Early morning (6AM-8AM): Client drops out if emergency services needed

Recommendations:
- Extend hours if business model allows
- Add "24/7 emergency" if applicable
- Note: GBP hours MUST be accurate (violations risk suspension)
```

## Scoring Rubric

Total: 100 points

| Component                     | Points | Criteria                                                   |
|-------------------------------|--------|------------------------------------------------------------|
| Map Pack Presence (P1 KWs)    | 30     | % of P1 keywords where client appears in 3-pack            |
| Competitive Position          | 20     | Average Map Pack position vs competitors for target KWs    |
| SERP Feature Utilization      | 15     | Justifications, attributes, and features displayed         |
| Map Pack Trigger Coverage     | 15     | % of target keywords that trigger Map Pack with presence   |
| Geographic Coverage           | 10     | Ranking consistency across the service area (grid concept) |
| Feature Parity with Competitors | 10   | No competitive feature gaps (photos, attributes, etc.)     |

**Score Interpretation:**
- 90-100: Dominant. Client owns the Map Pack for most target queries.
- 75-89: Strong. In the pack for most keywords, minor gaps to close.
- 50-74: Competitive. In the pack for some keywords, clear improvement areas.
- 25-49: Struggling. Rarely in the 3-pack, significant factor gaps.
- Below 25: Invisible. Fundamental issues across GBP, reviews, or citations.

## DFS MCP Data Sources

### Primary Tool: serp_organic_live_advanced

Use with local parameters to capture Map Pack results for each target keyword.

```python
# DFS MCP Call: SERP analysis with local pack detection
# Tool: serp_organic_live_advanced

params = {
    "keyword": "plumber in austin tx",
    "location_code": 1026339,  # Austin, TX
    "language_code": "en",
    "device": "mobile",  # Mobile shows Map Pack more often
    "os": "android",
    "depth": 20,  # Top 20 organic results
    # The response includes local_pack items when present
}

# Key response fields to extract:
# - items[] where type = "local_pack"
#   - title, rating, reviews_count, url, phone
#   - position within the local pack
#   - domain, description
# - items[] where type = "organic"
#   - position, url, title, description
# - items[] where type = "people_also_ask"
#   - questions and associated URLs
# - items[] where type = "ai_overview" (if present)
#   - content, sources
```

### Python Fallback: SERP Analysis with Local Pack Detection

```python
"""
SERP Analysis for Map Pack Detection and Competitive Positioning.
Processes DFS SERP API responses to extract local pack data.
"""

from dataclasses import dataclass, field
from typing import Optional


@dataclass
class LocalPackResult:
    position: int
    title: str
    rating: Optional[float]
    review_count: Optional[int]
    phone: Optional[str]
    address: Optional[str]
    url: Optional[str]
    justification: Optional[str] = None
    attributes: list[str] = field(default_factory=list)


@dataclass
class SerpAnalysis:
    keyword: str
    has_local_pack: bool
    local_pack_position_on_page: Optional[int]  # where the pack appears in SERP
    local_pack_results: list[LocalPackResult]
    organic_positions: dict[str, int]  # domain -> position
    has_paa: bool
    paa_questions: list[str]
    has_ai_overview: bool
    serp_features: list[str]


def parse_serp_response(keyword: str, response_items: list[dict]) -> SerpAnalysis:
    """Parse a DFS SERP API response into structured analysis."""
    local_pack_results = []
    organic_positions = {}
    paa_questions = []
    serp_features = []
    has_local_pack = False
    local_pack_page_position = None
    has_paa = False
    has_ai_overview = False

    for item in response_items:
        item_type = item.get("type", "")

        if item_type == "local_pack":
            has_local_pack = True
            local_pack_page_position = item.get("rank_absolute")
            pack_items = item.get("items", [])
            for i, pack_item in enumerate(pack_items):
                local_pack_results.append(LocalPackResult(
                    position=i + 1,
                    title=pack_item.get("title", ""),
                    rating=pack_item.get("rating", {}).get("value"),
                    review_count=pack_item.get("rating", {}).get("votes_count"),
                    phone=pack_item.get("phone"),
                    address=pack_item.get("address"),
                    url=pack_item.get("url"),
                ))
            serp_features.append("local_pack")

        elif item_type == "organic":
            domain = item.get("domain", "")
            position = item.get("rank_absolute", 0)
            if domain not in organic_positions:
                organic_positions[domain] = position

        elif item_type == "people_also_ask":
            has_paa = True
            for q in item.get("items", []):
                paa_questions.append(q.get("title", ""))
            serp_features.append("people_also_ask")

        elif item_type == "ai_overview":
            has_ai_overview = True
            serp_features.append("ai_overview")

        elif item_type == "featured_snippet":
            serp_features.append("featured_snippet")

        elif item_type == "images":
            serp_features.append("images")

    return SerpAnalysis(
        keyword=keyword,
        has_local_pack=has_local_pack,
        local_pack_position_on_page=local_pack_page_position,
        local_pack_results=local_pack_results,
        organic_positions=organic_positions,
        has_paa=has_paa,
        paa_questions=paa_questions,
        has_ai_overview=has_ai_overview,
        serp_features=serp_features,
    )


def find_client_in_pack(analysis: SerpAnalysis, client_name: str) -> Optional[int]:
    """Find the client's position in the local pack (1-indexed) or None."""
    for result in analysis.local_pack_results:
        if client_name.lower() in result.title.lower():
            return result.position
    return None


def generate_map_pack_report(analyses: list[SerpAnalysis],
                              client_name: str,
                              client_domain: str) -> dict:
    """Generate a comprehensive Map Pack report across all target keywords."""
    total_keywords = len(analyses)
    pack_triggered = sum(1 for a in analyses if a.has_local_pack)
    in_three_pack = 0
    in_maps = 0
    not_ranked = 0
    positions = []

    for analysis in analyses:
        pos = find_client_in_pack(analysis, client_name)
        if pos is not None:
            positions.append(pos)
            if pos <= 3:
                in_three_pack += 1
            else:
                in_maps += 1
        elif analysis.has_local_pack:
            not_ranked += 1

    avg_position = sum(positions) / len(positions) if positions else None

    return {
        "total_keywords_analyzed": total_keywords,
        "keywords_with_map_pack": pack_triggered,
        "client_in_3_pack": in_three_pack,
        "client_in_maps_not_3_pack": in_maps,
        "client_not_in_maps": not_ranked,
        "average_map_pack_position": round(avg_position, 1) if avg_position else "N/A",
        "paa_opportunity_count": sum(1 for a in analyses if a.has_paa),
        "ai_overview_count": sum(1 for a in analyses if a.has_ai_overview),
        "keywords_needing_attention": [
            a.keyword for a in analyses
            if a.has_local_pack and find_client_in_pack(a, client_name) is None
        ],
        "striking_distance_keywords": [
            a.keyword for a in analyses
            if a.has_local_pack and (find_client_in_pack(a, client_name) or 99) in range(4, 8)
        ],
    }
```

## User Data Requests

Ask the client or account manager for:

1. **Target keyword list** from Phase 5 (minimum P1 and P2 keywords)
2. **Business address** (exact, for proximity analysis)
3. **Service area radius** in miles
4. **Top 3-5 competitors** with names and addresses
5. **Known ranking changes** - any recent shifts in Map Pack visibility
6. **Business hours** - current hours as listed on GBP
7. **Local Falcon or BrightLocal data** (if available) for grid-based analysis
8. **Target neighborhoods** within the service area

## Output Format

Structure the Phase 6 section of the audit report as follows:

```markdown
## Phase 6: Map Pack Analysis

### Map Pack Score: [XX]/100

### Map Pack Summary
- **Keywords Analyzed:** [count]
- **Keywords with Map Pack:** [count] ([%])
- **Client in 3-Pack:** [count] ([%])
- **Client in Maps (not 3-Pack):** [count]
- **Client Not in Maps:** [count]
- **Average Map Pack Position:** [X.X]

### Keyword-Level Map Pack Results
| Keyword | Map Pack? | Client Position | Comp A Pos | Comp B Pos | Comp C Pos | Features |
|---------|-----------|-----------------|------------|------------|------------|----------|
| [kw]    | Yes       | #2              | #1         | #3         | --         | PAA, Img |

### Ranking Factor Attribution
| Factor          | Client Score | Comp A | Comp B | Gap Analysis           |
|-----------------|-------------|--------|--------|------------------------|
| GBP (32%)       | [score]     | [score]| [score]| [specific gaps]        |
| Reviews (20%)   | [score]     | [score]| [score]| [specific gaps]        |
| On-Page (15%)   | [score]     | [score]| [score]| [specific gaps]        |
| Behavioral (9%) | [score]     | [score]| [score]| [specific gaps]        |
| Links (8%)      | [score]     | [score]| [score]| [specific gaps]        |
| Citations (6%)  | [score]     | [score]| [score]| [specific gaps]        |

### Proximity Assessment
[Map or table showing proximity analysis with business and competitor locations]

### Competitive Feature Gaps
[Table of features competitors display that client does not, with action items]

### Opportunity Prioritization
1. **Quick Wins:** [Changes that can improve Map Pack position within 30 days]
2. **Medium-Term:** [60-90 day improvements based on factor gaps]
3. **Strategic:** [Longer-term positioning changes]

### Striking Distance Keywords
[Table of keywords where client is positions 4-7 in Maps, with specific actions to push into 3-pack]
```

## Cross-References

- **Phase 1 (GBP Audit):** GBP signals are 32% of Map Pack rankings. GBP score directly constrains Map Pack performance.
- **Phase 2 (Review Strategy):** Review signals are 20% of Map Pack. Review gaps identified here should be cross-referenced with Phase 2 recommendations.
- **Phase 3 (Link Building):** Link signals contribute 8% to Map Pack. Local link building priorities should align with Map Pack keyword targets.
- **Phase 4 (Citation Audit):** Citation signals are 6% of Map Pack. NAP consistency issues from Phase 4 directly impact Map Pack rankings.
- **Phase 5 (Keyword Research):** This phase consumes the keyword list from Phase 5. Keywords not triggering Map Pack should be redirected to Organic/AI Search strategies.
- **Phase 7 (On-Page Audit):** On-page signals are 15% of Map Pack. The on-page audit should prioritize pages targeting Map Pack keywords.
- **Phase 8 (Landing Pages):** Landing pages serve as the "website result" that Google references for Map Pack justifications and rankings.
