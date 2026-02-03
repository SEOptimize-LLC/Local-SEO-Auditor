---
name: Local Keyword Research
description: Phase 5 of the Local SEO Audit suite. Builds a comprehensive local keyword map using service+location modifiers, near-me intent, question-based queries, problem+location patterns, and comparison keywords. Produces a prioritized keyword matrix with intent classification, search volume, difficulty, and channel targeting across Map Pack, Organic, and AI Search.
version: 1.0.0
tags: [local-seo, keyword-research, search-intent, local-keywords, near-me]
related:
  - local-citation-audit (Phase 4)
  - map-pack-analysis (Phase 6)
  - local-on-page-audit (Phase 7)
  - local-landing-pages (Phase 8)
---

# Phase 5: Local Keyword Research

## When to Use

Run this skill when:
- Performing a full Local SEO audit (Phase 5 in the standard sequence)
- Onboarding a new local SEO client and establishing the keyword baseline
- Expanding service offerings and need to identify new keyword opportunities
- A client is entering a new geographic market or service area
- Content strategy needs data-driven keyword targets for local landing pages
- Reviewing keyword performance after algorithm updates
- Building the keyword foundation for Phases 6-8 (Map Pack Analysis, On-Page Audit, Landing Pages)

## Channel Impact

Keywords are the connective tissue across all three channels. Different keyword types trigger different SERP presentations:

| Keyword Type           | Map Pack Trigger | Organic Relevance | AI Search Relevance |
|------------------------|------------------|--------------------|--------------------|
| Service + City         | High             | High               | High               |
| Service + "near me"    | Very High        | Medium             | Medium             |
| "Best X in City"       | High             | High               | Very High          |
| Problem + Location     | Medium           | High               | High               |
| Question-based (PAA)   | Low              | Very High          | Very High          |
| Service + Action       | Medium           | High               | Medium             |
| Brand + Service        | Low              | Very High          | Medium             |

**Key Insight:** AI Search models heavily favor question-based and comparison queries. Optimizing for these keyword categories simultaneously serves Organic and AI Search channels.

## Prerequisites

Before running this skill, you should have:
1. **GBP Audit (Phase 1)** completed to know current GBP categories and services
2. **Client's service list** with all services offered and service areas
3. **Target geographic areas** - cities, neighborhoods, zip codes, service radius
4. **GSC access or export** - current keyword performance data (queries, clicks, impressions, position)
5. **Competitor list** from previous phases or client input
6. **Semrush/Ahrefs exports** (optional) - Keyword Gap analysis, Keyword Magic Tool exports

## Assessment Framework

### Step 1: Build the Service-Location Keyword Matrix

Create a systematic matrix combining every service with every target location.

```
KEYWORD MATRIX TEMPLATE
========================

Services (rows):          Locations (columns):
- [Primary Service 1]    - [City Name]
- [Primary Service 2]    - [Neighborhood 1]
- [Sub-service 1a]       - [Neighborhood 2]
- [Sub-service 1b]       - [Adjacent City 1]
- [Sub-service 2a]       - [County/Region]

Matrix Output:
[Service] + [Location]           -> "plumber in Austin"
[Service] + [Location] + modifier -> "emergency plumber in Austin TX"
[Service] + "near me"            -> "plumber near me"
```

**Target: 20-30 primary local keywords** from this matrix, expanded to 75-150 total keywords including long-tail variations.

### Step 2: Keyword Category Framework

Organize all keywords into these five categories:

#### Category 1: Service + Location (Core Keywords)
The foundation of local keyword targeting. Every service paired with every relevant location.

```
Pattern: [service] in [city]
         [service] [city]
         [city] [service]
         [service] in [neighborhood], [city]

Examples:
- "plumber in Austin"
- "Austin plumber"
- "plumber in East Austin, TX"
- "residential plumbing Austin"
```

#### Category 2: Service + Action (Intent-Rich Keywords)
These indicate stronger purchase intent and often trigger Map Pack results.

```
Pattern: [action] [service] [location]
         [service] [action] [location]

Actions: hire, find, call, get, schedule, book, request

Examples:
- "hire a plumber Austin"
- "schedule plumbing repair Austin"
- "get plumbing estimate Austin TX"
- "emergency plumber call Austin"
```

#### Category 3: Near Me Keywords (Implicit Local Intent)
Google interprets "near me" using the searcher's location. These trigger Map Pack almost always.

```
Pattern: [service] near me
         [service] near me [qualifier]
         best [service] near me

Examples:
- "plumber near me"
- "24 hour plumber near me"
- "best rated plumber near me"
- "affordable plumber near me"
```

#### Category 4: Problem + Location (Solution-Seeking Keywords)
These indicate a user with a specific problem. High conversion intent.

```
Pattern: [problem] [location]
         [problem] [service needed] [location]
         how to fix [problem] [location]

Examples:
- "burst pipe repair Austin"
- "water heater not working Austin TX"
- "clogged drain Austin emergency"
- "slab leak detection Austin"
```

#### Category 5: Comparison Keywords (AI Search Critical)
These are increasingly important for AI Search visibility. AI models love structured comparisons.

```
Pattern: best [service] in [city]
         top [service] [city]
         [service] vs [service] [city]
         [service] reviews [city]
         most affordable [service] [city]

Examples:
- "best plumber in Austin"
- "top rated plumbers Austin TX"
- "most affordable plumber Austin"
- "plumber reviews Austin"
```

### Step 3: Question-Based Local Queries (PAA Opportunities)

Question keywords appear in People Also Ask boxes and are primary fodder for AI Search responses.

```
Question Patterns:
- "How much does [service] cost in [city]?"
- "What is the best [service] in [city]?"
- "How long does [service] take in [city]?"
- "Do I need a permit for [service] in [city]?"
- "Who is the most reliable [service] in [city]?"
- "What should I look for in a [service] in [city]?"
- "How do I choose a [service] near me?"
- "Is [service] worth it in [city]?"

Examples:
- "How much does a plumber charge per hour in Austin?"
- "What is the average cost of pipe replacement in Austin TX?"
- "Do I need a permit for plumbing work in Austin?"
```

**Target: 8-12 question-based keywords** for FAQ content and PAA targeting.

### Step 4: Seasonal Trend Analysis

Identify seasonal patterns in search volume for local services.

```
Seasonal Analysis Framework:
- Which services peak in which months?
- Are there weather-related search spikes? (e.g., "frozen pipe repair" in winter)
- Are there seasonal events that drive searches? (e.g., "AC repair" before summer)
- What is the off-season content opportunity?

Output: 12-month keyword calendar with volume trends
```

### Step 5: Keyword Prioritization Matrix

Score each keyword on four dimensions to create a prioritized action plan.

| Dimension        | Weight | Scoring Criteria                                      |
|------------------|--------|-------------------------------------------------------|
| Search Volume    | 25%    | Monthly local search volume relative to market size   |
| Business Value   | 30%    | Revenue potential per conversion from this keyword    |
| Ranking Feasibility | 25% | Current position + keyword difficulty + competition  |
| Channel Coverage | 20%    | Triggers Map Pack + has Organic potential + AI relevant |

**Priority Tiers:**
- **P1 (Attack Now):** High volume, high value, feasible ranking, multi-channel
- **P2 (Build Toward):** High value but competitive; needs content + link investment
- **P3 (Quick Wins):** Lower volume but easy to rank; build authority incrementally
- **P4 (Monitor):** Low feasibility now; track for future opportunities

## Scoring Rubric

Total: 100 points (applied to the keyword research deliverable quality)

| Component                    | Points | Criteria                                              |
|------------------------------|--------|-------------------------------------------------------|
| Keyword Coverage Breadth     | 20     | All 5 categories represented with sufficient depth    |
| Search Volume Data Accuracy  | 15     | Volume data sourced and validated, not estimated      |
| Intent Classification        | 15     | Every keyword tagged with correct intent type         |
| Location Granularity         | 15     | Keywords at city, neighborhood, and region levels     |
| Competitive Gap Analysis     | 10     | Identified keywords competitors rank for but client does not |
| Seasonal Trend Mapping       | 10     | Seasonal patterns documented with data                |
| Prioritization Quality       | 10     | Clear P1-P4 tiers with rationale                      |
| Question/PAA Keywords        | 5      | Minimum 8 question-based keywords identified          |

## DFS MCP Data Sources

### Tool 1: kw_data_google_ads_search_volume

Pull exact search volume and competition data for the keyword list.

```python
# DFS MCP Call: Get search volume for keyword list
# Tool: kw_data_google_ads_search_volume

params = {
    "keywords": [
        "plumber in austin",
        "emergency plumber austin tx",
        "best plumber austin",
        "plumber near me"
    ],
    "location_code": 1026339,  # Austin, TX (use DFS location codes)
    "language_code": "en",
    "sort_by": "search_volume",
    "date_from": "2024-01-01",  # for trend data
    "date_to": "2025-01-01"
}

# Expected response fields:
# - keyword, search_volume, competition, competition_index
# - cpc, low_top_of_page_bid, high_top_of_page_bid
# - monthly_searches (array with month-by-month volume)
```

### Tool 2: dataforseo_labs_google_keyword_suggestions

Expand the seed keyword list with Google's suggestion data.

```python
# DFS MCP Call: Get keyword suggestions
# Tool: dataforseo_labs_google_keyword_suggestions

params = {
    "keyword": "plumber austin",
    "location_code": 1026339,
    "language_code": "en",
    "include_seed_keyword": True,
    "limit": 100,
    "filters": [
        ["keyword_info.search_volume", ">=", 10]
    ]
}
```

### Tool 3: dataforseo_labs_google_keyword_ideas

Discover related keyword ideas beyond direct suggestions.

```python
# DFS MCP Call: Get keyword ideas
# Tool: dataforseo_labs_google_keyword_ideas

params = {
    "keywords": ["plumber austin", "plumbing repair austin"],
    "location_code": 1026339,
    "language_code": "en",
    "limit": 100,
    "order_by": ["keyword_info.search_volume,desc"]
}
```

### Tool 4: dataforseo_labs_search_intent

Classify all discovered keywords by search intent.

```python
# DFS MCP Call: Classify keyword intent
# Tool: dataforseo_labs_search_intent

params = {
    "keywords": [
        "plumber in austin",
        "how much does a plumber cost in austin",
        "best plumber austin reviews",
        "hire plumber austin tx"
    ],
    "language_code": "en"
}

# Expected response:
# - keyword, intent (informational, navigational, transactional, commercial)
# - intent_probability
```

### Tool 5: kw_data_dfs_trends_explore

Analyze seasonal trends for key service terms.

```python
# DFS MCP Call: Explore keyword trends
# Tool: kw_data_dfs_trends_explore

params = {
    "keywords": ["plumber", "plumbing repair", "emergency plumber"],
    "location_code": 1026339,
    "date_from": "2023-01-01",
    "date_to": "2025-01-01",
    "type": "web"
}

# Use the monthly trend data to identify seasonal peaks and valleys
```

### Python Fallback: Keyword Clustering by SERP Similarity

```python
"""
Keyword Clustering by SERP Similarity
Groups keywords that share SERP results, indicating Google treats them
as the same intent and they can be targeted on a single page.
"""

from collections import defaultdict
from itertools import combinations


def calculate_serp_overlap(serp_a: list[str], serp_b: list[str], top_n: int = 10) -> float:
    """Calculate overlap ratio between two SERP result sets."""
    set_a = set(serp_a[:top_n])
    set_b = set(serp_b[:top_n])
    if not set_a or not set_b:
        return 0.0
    intersection = set_a & set_b
    return len(intersection) / top_n


def cluster_keywords_by_serp(keyword_serp_data: dict[str, list[str]],
                              overlap_threshold: float = 0.4) -> list[list[str]]:
    """
    Cluster keywords based on SERP result overlap.

    Args:
        keyword_serp_data: dict mapping keyword -> list of ranking URLs
        overlap_threshold: minimum overlap ratio to consider keywords related

    Returns:
        List of keyword clusters (each cluster is a list of keywords)
    """
    keywords = list(keyword_serp_data.keys())
    adjacency = defaultdict(set)

    for kw_a, kw_b in combinations(keywords, 2):
        overlap = calculate_serp_overlap(
            keyword_serp_data[kw_a],
            keyword_serp_data[kw_b]
        )
        if overlap >= overlap_threshold:
            adjacency[kw_a].add(kw_b)
            adjacency[kw_b].add(kw_a)

    visited = set()
    clusters = []

    for keyword in keywords:
        if keyword in visited:
            continue
        cluster = []
        stack = [keyword]
        while stack:
            current = stack.pop()
            if current in visited:
                continue
            visited.add(current)
            cluster.append(current)
            stack.extend(adjacency[current] - visited)
        clusters.append(sorted(cluster))

    return sorted(clusters, key=lambda c: len(c), reverse=True)


def assign_cluster_primary(clusters: list[list[str]],
                            volume_data: dict[str, int]) -> list[dict]:
    """Assign a primary keyword to each cluster based on search volume."""
    result = []
    for cluster in clusters:
        sorted_by_volume = sorted(cluster, key=lambda k: volume_data.get(k, 0), reverse=True)
        result.append({
            "primary_keyword": sorted_by_volume[0],
            "primary_volume": volume_data.get(sorted_by_volume[0], 0),
            "secondary_keywords": sorted_by_volume[1:],
            "total_cluster_volume": sum(volume_data.get(k, 0) for k in cluster),
            "cluster_size": len(cluster)
        })
    return result
```

## User Data Requests

Ask the client or account manager for:

1. **Complete service list** - Every service offered, including sub-services and specialties
2. **Service area definition** - Cities, neighborhoods, zip codes, and radius served
3. **GSC export** - Last 12 months of query data (query, clicks, impressions, CTR, position)
4. **Semrush/Ahrefs keyword data** (if available):
   - Keyword Gap analysis vs top 3 competitors
   - Keyword Magic Tool export for primary service terms
   - Current organic keyword rankings
5. **Top 3-5 competitors** - Business names and websites
6. **Revenue by service** - Which services generate the most revenue (for business value scoring)
7. **Seasonal patterns** - Any known seasonal peaks in demand
8. **New services or areas** - Any planned expansion into new services or geographies

## Output Format

Structure the Phase 5 section of the audit report as follows:

```markdown
## Phase 5: Local Keyword Research

### Keyword Research Score: [XX]/100

### Keyword Summary
- **Total Keywords Identified:** [count]
- **Primary Keywords (P1):** [count]
- **Secondary Keywords (P2):** [count]
- **Quick Win Keywords (P3):** [count]
- **Monitor Keywords (P4):** [count]

### Keyword Matrix

| Keyword | Category | Intent | Volume | KD | CPC | Map Pack? | Priority | Target Page |
|---------|----------|--------|--------|-----|-----|-----------|----------|-------------|
| [kw]    | Service+Location | Transactional | [vol] | [kd] | [cpc] | Yes | P1 | /service-city |
| ...     | ...      | ...    | ...    | ... | ... | ...       | ...      | ...         |

### Keyword Clusters
[Table of keyword clusters with primary keyword, cluster size, total volume, and target page]

### Question Keywords (PAA Targets)
[Table of question-based keywords with volume, current PAA presence, and target FAQ section]

### Seasonal Trends
[12-month chart or table showing volume trends for top 10 keywords]

### Competitive Keyword Gaps
[Keywords where competitors rank but client does not, sorted by opportunity score]

### Recommendations
1. **Content Priorities:** [Which pages to create/optimize first based on P1 keywords]
2. **Quick Wins:** [Keywords where client ranks positions 4-15 that can be improved with on-page optimization]
3. **Content Gaps:** [Keywords with no corresponding page on the site]
4. **AI Search Optimization:** [Question and comparison keywords to target for AI visibility]
```

## Cross-References

- **Phase 4 (Citation Audit):** Ensure citation categories align with keyword verticals. Industry-specific directories should match target keyword themes.
- **Phase 6 (Map Pack Analysis):** The keyword list from this phase drives the Map Pack ranking analysis. Map Pack trigger keywords are identified here.
- **Phase 7 (On-Page Audit):** Keywords map directly to title tags, H1s, meta descriptions, and content optimization targets for each page.
- **Phase 8 (Landing Pages):** The keyword matrix defines the service/location page matrix. Each keyword cluster should map to a specific landing page.
