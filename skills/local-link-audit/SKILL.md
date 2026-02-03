---
name: local-link-audit
description: Local link profile audit with three-channel strategy — Map Pack directory links, Organic editorial links, and AI Search citation links with competitor gap analysis
version: 1.0.0
tags: [local-seo, backlinks, link-building, link-audit, competitor-analysis, local-links]
related: [local-content-strategy, local-citation-audit, local-on-page-audit, local-competitor-analysis, local-seo-audit]
---

# Phase 11: Local Link Audit

> **Links carry different weight and require different strategies across each search channel.** At 8% of Map Pack, 24% of Organic, and 13% of AI Search, the link strategy for a local business must be channel-aware. A Chamber of Commerce link has minimal organic value but strong Map Pack trust. A local news mention has massive organic value and emerging AI citation value. This skill audits the current link profile AND builds a channel-prioritized link acquisition framework.

---

## When to Use This Skill

- **As part of the full Local SEO Audit**: Run as Phase 11, after schema markup (Phase 10) is complete. Links amplify well-structured, well-optimized pages — auditing links before the pages are ready wastes effort.
- **As a standalone audit**: When a client needs to understand their competitive link gap, when organic rankings plateau despite strong on-page work, or when building a link acquisition strategy.
- **Trigger scenarios**:
  - Client ranks well in Map Pack but poorly in organic (likely a link deficit)
  - Competitors consistently outrank despite similar on-page optimization
  - Client has never done any intentional link building
  - Organic traffic has dropped and a link profile issue (toxic links, lost links) is suspected
  - Client wants to appear in AI search recommendations and "best of" lists
  - New location launched and needs local authority signals

---

## Channel Impact

| Channel        | Weight  | Rationale |
|----------------|---------|-----------|
| **Map Pack**   | **8%**  | Links are the 5th most important Map Pack factor. Local directory links, association memberships, and Chamber of Commerce listings serve as trust signals. Volume matters less than local relevance. |
| **Organic**    | **24%** | Links are the 2nd most important organic factor (behind On-Page at 33%). Editorial links from local news, blogs, and industry sites drive organic authority. Quality and relevance are paramount. |
| **AI Search**  | **13%** | Links are the 5th most important AI Search factor. AI engines use link relationships to identify authoritative local sources. "Best of" roundup articles and local resource pages are especially valuable — AI engines treat these as curated recommendation lists. |

**Strategy implication**: A local business needs THREE types of links, not one. Directory/association links for Map Pack trust, editorial/news links for organic authority, and "best of" citation links for AI visibility.

---

## Prerequisites

Before beginning the local link audit, ensure you have:

1. **Discovery Brief from Phase 1** (`/discovery-intake`)
   - Target domain
   - Top 3-5 competitors with their domains
   - Primary service keywords
   - Target geographic area

2. **On-Page Audit from Phase 5** (`/local-on-page-audit`)
   - Linkable asset inventory (what pages are worth linking to?)
   - Current content quality assessment

3. **DFS MCP Tools Ready**
   - `mcp__dfs-mcp__backlinks_summary` — domain-level link profile overview
   - `mcp__dfs-mcp__backlinks_backlinks` — individual backlink list
   - `mcp__dfs-mcp__backlinks_competitors` — competitor link discovery
   - `mcp__dfs-mcp__backlinks_domain_intersection` — link gap analysis

---

## Assessment Framework

### 11.1 Current Backlink Profile Assessment (20 points)

**Why This Matters**: Before building new links, you must understand what you already have. The current profile reveals strengths to maintain, weaknesses to address, and toxic links to disavow.

#### Key Metrics to Assess

| Metric | What It Tells You | Good Range (Local Business) |
|--------|-------------------|----------------------------|
| **Total Backlinks** | Raw link volume | 200-5,000 (industry dependent) |
| **Referring Domains** | Unique sites linking to you | 50-500 (more important than total links) |
| **Domain Rating (DR)** | Overall domain authority | 20-50 for local businesses |
| **Dofollow/Nofollow Ratio** | Link equity distribution | 60-80% dofollow is healthy |
| **Link Velocity** | New links per month | Steady growth, no sudden spikes |
| **Anchor Text Distribution** | What text links use | Brand (40-60%), keyword (10-20%), URL (15-25%), other (10-20%) |
| **Top Linked Pages** | Which pages attract links | Homepage should not be >70% of all links |

#### Audit Steps

1. Pull backlink summary via DFS MCP or Python
2. Record all key metrics above
3. Assess link quality distribution (high DR vs. low DR referring domains)
4. Check for sudden link spikes or drops (indicates spam or link loss)
5. Review anchor text for over-optimization (>30% exact match keyword anchors is a red flag)
6. Identify top 10 referring domains by authority

**Scoring**:
- 0 points: Fewer than 20 referring domains, or profile dominated by spam/low-quality links
- 5 points: 20-50 referring domains with mixed quality
- 10 points: 50-100 referring domains with reasonable quality distribution
- 15 points: 100-250 referring domains with healthy quality, velocity, and anchor distribution
- 20 points: 250+ referring domains with strong quality, diverse anchors, steady growth, and local relevance

---

### 11.2 Map Pack Link Strategy (15 points)

**Why This Matters**: Map Pack link value comes from LOCAL TRUST signals. A link from the Dallas Chamber of Commerce tells Google "this is a real, trusted Dallas business." These links do not need to be high-DR or editorially earned — they need to be locally relevant and from trusted local institutions.

#### Priority Local Trust Links

| Link Source | Trust Value | Difficulty | Notes |
|-------------|-------------|------------|-------|
| **Chamber of Commerce** | HIGH | Low | Membership usually costs $200-500/year. Provides a directory link with NAP. |
| **Better Business Bureau** | HIGH | Low | BBB accreditation costs $400-600/year. Strong trust signal. |
| **Industry Associations** | HIGH | Low-Medium | State plumbing board, local HVAC contractors association, dental society, bar association. |
| **Local Government Sites** | VERY HIGH | Medium | City business directories, county vendor lists, .gov links are extremely valuable. |
| **Local Nonprofits** | MEDIUM | Low | Sponsorship of local charities in exchange for sponsor page link. |
| **Supplier/Manufacturer** | MEDIUM | Low | Many suppliers list authorized dealers/installers on their websites. |
| **Trade School/Apprenticeship** | MEDIUM | Medium | Local trade schools may list businesses that hire graduates. |

#### Audit Steps

1. Check if the business is listed in Chamber of Commerce directory
2. Check BBB accreditation and listing status
3. Search for industry association memberships
4. Look for existing .gov and .edu links in the backlink profile
5. Check supplier/manufacturer "find a dealer" pages
6. Compare against competitors' local trust link inventory

**Scoring**:
- 0 points: No local trust links (no Chamber, BBB, associations, or government links)
- 5 points: 1-2 local trust links present
- 10 points: 3-5 local trust links including Chamber or industry association
- 15 points: 6+ local trust links spanning multiple categories (Chamber + BBB + associations + government)

---

### 11.3 Organic Link Strategy (20 points)

**Why This Matters**: Organic rankings require editorial, high-authority links that signal genuine expertise and trust. These links are harder to earn but have 3x the ranking impact of directory links for organic results.

#### Priority Editorial Link Opportunities

| Link Source | Authority Value | Difficulty | Approach |
|-------------|----------------|------------|----------|
| **Local News Outlets** | VERY HIGH | Medium-High | Expert quotes, business features, press releases for newsworthy events |
| **Local Blogs/Magazines** | HIGH | Medium | Guest posts, expert interviews, project features |
| **Community Sponsorships** | MEDIUM-HIGH | Low | Youth sports teams, school events, community festivals — sponsor pages link back |
| **Partner/Supplier Links** | MEDIUM | Low | Cross-promotion with complementary businesses (plumber + general contractor) |
| **University/College Sites** | VERY HIGH | High | Guest lectures, scholarship sponsorships, career fair participation |
| **Local Event Sponsorships** | MEDIUM-HIGH | Medium | Charity events, 5K runs, community clean-up days — event pages link sponsors |
| **HARO/Quoted Expert** | HIGH | Medium | Respond to journalist queries for expert quotes in published articles |

#### Outreach Email Templates

**Template 1: Local News Expert Quote**
```
Subject: Expert Source Available: [Topic] in [City]

Hi [Reporter Name],

I noticed you cover [topic/beat] for [Publication]. I'm [Name], [Title] at
[Business] — we've been serving [City] for [X] years.

I'd be happy to serve as a local expert source on topics like:
- [Relevant topic 1] (e.g., "seasonal plumbing issues in Dallas winters")
- [Relevant topic 2] (e.g., "water conservation tips for North Texas homeowners")
- [Relevant topic 3] (e.g., "how to choose a licensed contractor in Texas")

I can provide expert quotes, data from our [X] years of local experience,
or a full interview at your convenience.

Best,
[Name]
[Title, Business]
[Phone] | [Email]
```

**Template 2: Community Sponsorship**
```
Subject: Sponsorship Inquiry — [Event/Organization Name]

Hi [Contact Name],

[Business Name] would love to support [Event/Organization] as a sponsor.
We've been part of the [City] community for [X] years and believe in
supporting [cause/activity].

Could you share your sponsorship packages? We're particularly interested
in [specific tier/level] and would like to understand what recognition
(including any website listing) is included.

Thank you,
[Name]
[Title, Business]
```

**Template 3: Guest Post Pitch**
```
Subject: Guest Post Idea for [Blog/Publication Name]

Hi [Editor Name],

I'm [Name] from [Business] in [City]. I've been reading [Blog] and thought
your audience would benefit from a piece on:

"[Article Title]" — [2-3 sentence description of the article, emphasizing
value to the publication's local audience]

I can provide:
- Original content with local data and examples
- Professional photos from our projects
- [X] years of hands-on expertise in [field]

Happy to adjust the angle to fit your editorial calendar. I've attached
[writing sample / link to previous article] for reference.

Best,
[Name]
```

**Template 4: Partner Cross-Promotion**
```
Subject: Partnership Opportunity — [Complementary Business Type]

Hi [Name],

I'm [Name] from [Business] here in [City]. We frequently work alongside
[their business type] and often get asked for referrals to trusted
[their service].

Would you be interested in a mutual referral arrangement? We could:
- List each other on our "Trusted Partners" pages
- Refer clients who need [their service] / [your service]
- Co-create content on topics that span both our expertise areas

Let me know if you'd like to discuss over coffee.

Best,
[Name]
```

**Scoring**:
- 0 points: No editorial or community links in the profile
- 5 points: 1-3 editorial/community links present
- 10 points: 4-8 editorial links from local news, blogs, or community organizations
- 15 points: 8-15 editorial links with diversity across news, blogs, sponsorships, and partners
- 20 points: 15+ editorial links with strong local relevance, authority, and diversity

---

### 11.4 AI Search Link Strategy (15 points)

**Why This Matters**: AI search engines (Google AI Overviews, ChatGPT, Perplexity) build their local recommendations from curated content — particularly "best of" roundup articles, local resource pages, and authoritative recommendation lists. Being mentioned in these articles is increasingly critical for AI visibility.

#### "Best of" Roundup Link Strategy

**What AI Engines Use**: When a user asks "Who is the best plumber in Dallas?", AI engines consult:
1. Published "best of" articles (e.g., "10 Best Plumbers in Dallas 2025")
2. Local resource pages (e.g., "Dallas Homeowner's Guide to Emergency Services")
3. Review aggregation sites (Yelp, Angi, HomeAdvisor)
4. Community forums and discussion threads

**Priority AI Citation Link Sources**:

| Link Source | AI Citation Value | Approach |
|-------------|------------------|----------|
| **"Best of [City]" Articles** | VERY HIGH | Get listed in local "best of" roundup articles — these are the #1 source AI engines cite for local recommendations |
| **Local Resource Guides** | HIGH | Create or get featured in comprehensive local guides (e.g., "Complete Guide to Home Services in Dallas") |
| **Industry "Top X" Lists** | HIGH | Industry publications that rank or list top providers by market |
| **City Magazine Features** | HIGH | Local lifestyle magazines with online presence |
| **Neighborhood/HOA Sites** | MEDIUM | Recommended vendor lists for homeowner associations |
| **Nextdoor Recommendations** | MEDIUM | While not a traditional link, Nextdoor recommendations feed AI local knowledge |

**Action Items for AI Citation Links**:
1. Search for existing "best of [service] in [city]" articles — are you listed? Are competitors?
2. Identify "best of" articles where you are NOT listed but competitors ARE — these are immediate outreach targets
3. Search for local resource guides and verify your business is included
4. Create content that AI engines would cite (see Phase 12: Content Strategy)
5. Monitor AI search results for your target queries — who is being cited?

**Scoring**:
- 0 points: Not featured in any "best of" or local resource content
- 5 points: Listed in 1-2 "best of" articles or local guides
- 10 points: Featured in 3-5 "best of" articles with positive positioning
- 15 points: Featured in 5+ "best of" articles, local resource guides, and industry lists, with proactive monitoring and outreach

---

### 11.5 Competitor Local Link Gap Analysis (15 points)

**Why This Matters**: Understanding WHERE competitors get their links reveals the exact opportunities you are missing. The link gap is the difference between your link profile and your competitors' profiles — it shows which sites link to them but not to you.

#### Audit Steps

1. Identify top 3-5 local competitors from Phase 1 discovery
2. Pull backlink profiles for each competitor via DFS MCP
3. Run domain intersection analysis — find sites that link to 2+ competitors but NOT to you
4. Categorize gap links by type (directory, editorial, association, "best of")
5. Prioritize gap links by authority and relevance
6. Create an outreach list for the top 20 gap opportunities

#### Python: Backlink Analysis

```python
import requests
import base64
from typing import List, Dict

DFS_LOGIN = "your_login"
DFS_PASSWORD = "your_password"
DFS_AUTH = base64.b64encode(f"{DFS_LOGIN}:{DFS_PASSWORD}".encode()).decode()

def get_backlink_summary(domain: str) -> Dict:
    """
    Get backlink profile summary for a domain.
    Returns total backlinks, referring domains, DR, and distribution data.
    """
    url = "https://api.dataforseo.com/v3/backlinks/summary/live"
    headers = {
        "Authorization": f"Basic {DFS_AUTH}",
        "Content-Type": "application/json"
    }
    payload = [{"target": domain, "internal_list_limit": 10, "backlinks_filters": ["dofollow", "=", True]}]

    response = requests.post(url, headers=headers, json=payload)
    result = response.json()

    if result.get("status_code") == 20000:
        tasks = result.get("tasks", [])
        if tasks and tasks[0].get("result"):
            data = tasks[0]["result"][0]
            return {
                "domain": domain,
                "total_backlinks": data.get("external_links_count", 0),
                "referring_domains": data.get("referring_domains", 0),
                "dofollow_links": data.get("external_links_count", 0),
                "domain_rank": data.get("rank", 0),
                "broken_backlinks": data.get("broken_backlinks", 0),
                "referring_ips": data.get("referring_ips", 0),
                "referring_subnets": data.get("referring_subnets", 0)
            }
    return {"error": result.get("status_message", "Unknown error")}


def get_backlink_list(domain: str, limit: int = 100, order_by: str = "rank,desc") -> List[Dict]:
    """
    Get individual backlinks for a domain, ordered by authority.
    """
    url = "https://api.dataforseo.com/v3/backlinks/backlinks/live"
    headers = {
        "Authorization": f"Basic {DFS_AUTH}",
        "Content-Type": "application/json"
    }
    payload = [{
        "target": domain,
        "limit": limit,
        "order_by": [order_by],
        "backlinks_filters": ["dofollow", "=", True]
    }]

    response = requests.post(url, headers=headers, json=payload)
    result = response.json()

    if result.get("status_code") == 20000:
        tasks = result.get("tasks", [])
        if tasks and tasks[0].get("result"):
            items = tasks[0]["result"][0].get("items", [])
            return [{
                "source_url": item.get("url_from", ""),
                "source_domain": item.get("domain_from", ""),
                "target_url": item.get("url_to", ""),
                "anchor": item.get("anchor", ""),
                "domain_rank": item.get("rank", 0),
                "page_rank": item.get("page_from_rank", 0),
                "is_dofollow": item.get("dofollow", False),
                "first_seen": item.get("first_seen", ""),
                "link_type": categorize_link(item)
            } for item in items]
    return []


def categorize_link(item: Dict) -> str:
    """Categorize a backlink by type based on source domain patterns."""
    domain = item.get("domain_from", "").lower()
    url = item.get("url_from", "").lower()

    if any(d in domain for d in [".gov"]):
        return "government"
    elif any(d in domain for d in [".edu"]):
        return "education"
    elif any(d in domain for d in ["chamber", "bbb.org", "angieslist", "homeadvisor"]):
        return "directory/association"
    elif any(d in domain for d in ["yelp.com", "yellowpages", "manta.com"]):
        return "directory"
    elif any(phrase in url for phrase in ["best-", "top-", "best_", "top_"]):
        return "best-of-roundup"
    elif any(d in domain for d in ["patch.com", "news", "times", "tribune", "herald"]):
        return "local-news"
    else:
        return "general"


def get_competitor_link_gap(target_domain: str, competitor_domains: List[str], limit: int = 100) -> List[Dict]:
    """
    Find domains that link to competitors but NOT to the target domain.
    These are the highest-priority link acquisition targets.
    """
    url = "https://api.dataforseo.com/v3/backlinks/domain_intersection/live"
    headers = {
        "Authorization": f"Basic {DFS_AUTH}",
        "Content-Type": "application/json"
    }

    # Build targets: first is the "exclude" target, rest are competitors
    targets = {
        "1": {"target": target_domain, "intersection": False},
    }
    for i, comp in enumerate(competitor_domains[:4], start=2):
        targets[str(i)] = {"target": comp, "intersection": True}

    payload = [{
        "targets": targets,
        "limit": limit,
        "order_by": ["1.rank,desc"]
    }]

    response = requests.post(url, headers=headers, json=payload)
    result = response.json()

    if result.get("status_code") == 20000:
        tasks = result.get("tasks", [])
        if tasks and tasks[0].get("result"):
            items = tasks[0]["result"][0].get("items", [])
            gap_links = []
            for item in items:
                gap_links.append({
                    "domain": item.get("domain", ""),
                    "rank": item.get("1", {}).get("rank", 0),
                    "competitors_linking": sum(1 for k in item if k != "domain" and item[k].get("backlinks", 0) > 0),
                    "total_competitor_links": sum(item.get(k, {}).get("backlinks", 0) for k in item if k != "domain"),
                    "link_type": "gap_opportunity"
                })
            return sorted(gap_links, key=lambda x: x["rank"], reverse=True)
    return []


# Example usage:
# summary = get_backlink_summary("abcplumbing.com")
# print(f"Referring Domains: {summary['referring_domains']}")
#
# gap = get_competitor_link_gap(
#     "abcplumbing.com",
#     ["competitor1.com", "competitor2.com", "competitor3.com"]
# )
# for link in gap[:20]:
#     print(f"GAP: {link['domain']} (DR: {link['rank']}, linked to {link['competitors_linking']} competitors)")
```

**Scoring**:
- 0 points: No competitor link analysis performed, or gap analysis reveals 50+ high-value missed opportunities with no plan
- 5 points: Basic competitor comparison completed but no actionable gap list
- 10 points: Full gap analysis with categorized opportunities and top 20 outreach targets identified
- 15 points: Comprehensive gap analysis with categorized, prioritized outreach list, competitor link profiles fully mapped, and strategy to close top gaps

---

### 11.6 Toxic Link Identification & Disavow (10 points)

**Why This Matters**: Toxic or spammy backlinks can trigger Google penalties (manual or algorithmic) that suppress local rankings. While Google says it ignores most spam links, an egregious profile can still cause harm.

#### Red Flags to Look For

| Signal | Severity | Action |
|--------|----------|--------|
| Links from gambling, pharma, or adult sites | HIGH | Disavow immediately |
| Links from PBN (private blog network) sites | HIGH | Disavow |
| Sudden spike of 100+ links in a day | MEDIUM-HIGH | Investigate — likely negative SEO attack |
| Links from completely irrelevant foreign-language sites | MEDIUM | Disavow if volume is significant |
| Exact-match anchor text from low-quality sites | MEDIUM | Disavow the worst offenders |
| Directory links with wrong NAP | LOW | Contact directory to correct NAP, do not disavow |
| Comment spam links | LOW | Usually nofollowed, low priority |

#### Audit Steps

1. Pull full backlink list and sort by lowest quality first
2. Identify referring domains with DR < 5 and suspicious patterns
3. Check for anchor text manipulation (>40% exact match keyword anchors)
4. Look for link velocity anomalies (sudden spikes)
5. Cross-reference against known spam domain lists
6. Create disavow file for confirmed toxic links

**Scoring**:
- 0 points: Significant toxic link exposure with no disavow file
- 3 points: Some toxic links identified but disavow file incomplete
- 7 points: Toxic links identified and disavow file submitted, anchor distribution is healthy
- 10 points: Clean link profile with minimal toxic exposure, active monitoring, and current disavow file

---

### 11.7 Anchor Text Analysis (5 points)

**Healthy Anchor Text Distribution for Local Business**:

| Anchor Type | Target % | Example |
|-------------|----------|---------|
| Brand name | 40-60% | "ABC Plumbing", "ABC Plumbing Dallas" |
| Naked URL | 15-25% | "abcplumbing.com", "www.abcplumbing.com" |
| Generic | 10-15% | "click here", "learn more", "website" |
| Keyword + Local | 5-15% | "Dallas plumber", "emergency plumbing Dallas" |
| Exact match keyword | 5-10% | "emergency plumber" (KEEP THIS LOW) |

**Warning**: If exact-match keyword anchors exceed 25%, this is an over-optimization signal that can trigger algorithmic penalties.

**Scoring**:
- 0 points: Anchor distribution heavily skewed to exact-match keywords (>30%)
- 2 points: Anchor distribution has some imbalance but no severe over-optimization
- 5 points: Natural anchor distribution across all types within healthy ranges

---

## Scoring Rubric

```
==============================================================
        LOCAL LINK AUDIT SCORE CALCULATION
==============================================================

CURRENT PROFILE (20 points max)
--------------------------------------------------------------
  Referring domains volume:     ___/ 8  (0 = <20, 3 = 20-50, 5 = 50-100,
                                         8 = 100+)
  Link quality distribution:    ___/ 7  (0 = spam-heavy, 4 = mixed, 7 = strong)
  Link velocity (growth trend): ___/ 5  (0 = declining, 2 = flat, 5 = growing)
                                ------
  PROFILE SUBTOTAL:             ___/20


MAP PACK LINKS (15 points max)
--------------------------------------------------------------
  Chamber/Association links:    ___/ 6  (0 = none, 3 = 1-2, 6 = 3+)
  Government/Edu links:         ___/ 5  (0 = none, 2 = 1, 5 = 2+)
  Supplier/Partner links:       ___/ 4  (0 = none, 2 = 1-2, 4 = 3+)
                                ------
  MAP PACK SUBTOTAL:            ___/15


ORGANIC LINKS (20 points max)
--------------------------------------------------------------
  Local news/blog links:        ___/ 8  (0 = none, 4 = 1-3, 8 = 4+)
  Community sponsorship links:  ___/ 6  (0 = none, 3 = 1-2, 6 = 3+)
  Guest posts/expert mentions:  ___/ 6  (0 = none, 3 = 1-2, 6 = 3+)
                                ------
  ORGANIC SUBTOTAL:             ___/20


AI SEARCH LINKS (15 points max)
--------------------------------------------------------------
  "Best of" article features:   ___/ 8  (0 = none, 4 = 1-2, 8 = 3+)
  Local resource guide features:___/ 4  (0 = none, 2 = 1, 4 = 2+)
  Industry "Top X" lists:       ___/ 3  (0 = none, 1 = 1, 3 = 2+)
                                ------
  AI SEARCH SUBTOTAL:           ___/15


COMPETITOR GAP (15 points max)
--------------------------------------------------------------
  Gap analysis completed:       ___/ 5  (0 = not done, 5 = comprehensive)
  Outreach list created:        ___/ 5  (0 = not done, 5 = prioritized top 20)
  Strategy by channel:          ___/ 5  (0 = no plan, 5 = channel-specific plan)
                                ------
  GAP ANALYSIS SUBTOTAL:        ___/15


TOXIC LINKS (10 points max)
--------------------------------------------------------------
  Toxic link exposure:          ___/ 5  (0 = significant, 3 = minor, 5 = clean)
  Disavow file status:          ___/ 5  (0 = needed but missing, 3 = incomplete, 5 = current)
                                ------
  TOXIC SUBTOTAL:               ___/10


ANCHOR TEXT (5 points max)
--------------------------------------------------------------
  Distribution health:          ___/ 5  (0 = over-optimized, 2 = imbalanced, 5 = natural)
                                ------
  ANCHOR SUBTOTAL:              ___/ 5


==============================================================
  LOCAL LINK AUDIT SCORE:       ___/100
==============================================================

SCORE INTERPRETATION:
  90-100:  Excellent — Strong, diverse link profile with active acquisition
  75-89:   Good — Solid foundation with specific gaps to close
  50-74:   Needs Work — Missing key link types or significant competitor gap
  25-49:   Poor — Weak link profile, minimal local authority signals
  0-24:    Critical — Almost no quality links, urgent link building needed
==============================================================
```

---

## DFS MCP Data Sources

### Tool 1: Domain Backlink Summary

```
TOOL: mcp__dfs-mcp__backlinks_summary
USE:  Get high-level backlink profile metrics for the target domain and
      each competitor domain. Returns total backlinks, referring domains,
      domain rank, and distribution data.
PARAMETERS:
  - target: Domain to analyze (e.g., "abcplumbing.com")
```

### Tool 2: Individual Backlink List

```
TOOL: mcp__dfs-mcp__backlinks_backlinks
USE:  Pull the full list of backlinks pointing to the target domain.
      Sort by rank to identify highest-authority links first.
PARAMETERS:
  - target: Domain to analyze
  - limit: Number of backlinks to return (start with 100)
  - order_by: ["rank,desc"] to get highest-authority first
  - filters: ["dofollow", "=", true] to focus on links passing equity
```

### Tool 3: Competitor Link Discovery

```
TOOL: mcp__dfs-mcp__backlinks_competitors
USE:  Discover which domains compete with the target for backlinks.
      Reveals the local link competitive landscape.
PARAMETERS:
  - target: Target domain
```

### Tool 4: Link Gap Analysis

```
TOOL: mcp__dfs-mcp__backlinks_domain_intersection
USE:  Find domains that link to competitors but NOT to the target.
      This is the core link gap analysis tool — it reveals the exact
      opportunities being missed.
PARAMETERS:
  - targets: Dictionary with target (intersection: false) and
    competitors (intersection: true)
  - limit: 100
  - order_by: ["1.rank,desc"]
```

### Workflow: Complete Local Link Audit

```
1. Run backlinks_summary on target domain → record profile metrics
2. Run backlinks_summary on each competitor → build comparison table
3. Run backlinks_backlinks on target → categorize links by type
4. Run backlinks_domain_intersection → identify gap opportunities
5. Categorize all links: directory, association, news, blog, "best-of", toxic
6. Score each assessment area
7. Build prioritized outreach list from gap analysis
8. Compile into output format
```

---

## User Data Requests

### Required Data:
1. **Domain access** — The target domain URL
2. **Competitor domains** — Top 3-5 competitor domain URLs
3. **Existing link building history** — Any previous outreach campaigns, directories joined, sponsorships active

### Optional but Valuable:
- Google Search Console — Links report (external links, top linking sites)
- Any existing disavow file
- Current industry association memberships
- Current community sponsorships or partnerships
- Previous PR or media coverage

---

## Output Format

```
==============================================================================
PHASE 11: LOCAL LINK AUDIT
==============================================================================

Domain: [domain.com]
Audit Date: [YYYY-MM-DD]
Auditor: Claude Code (Local SEO Auditor)

------------------------------------------------------------------------------
LOCAL LINK SCORE: [XX]/100 — [Excellent/Good/Needs Work/Poor/Critical]
------------------------------------------------------------------------------

BACKLINK PROFILE SUMMARY
------------------------------------------------------------------------------
  Total Backlinks:        [X]
  Referring Domains:      [X]
  Domain Rank:            [X]
  Dofollow Ratio:         [X%]
  Link Velocity:          [+X/month avg over last 6 months]
  Anchor Distribution:    Brand [X%] | URL [X%] | Keyword [X%] | Generic [X%]


COMPETITOR COMPARISON
------------------------------------------------------------------------------
  Domain              | Ref. Domains | DR   | Quality    | Gap vs Client
  --------------------|-------------|------|------------|---------------
  [client.com]        | [X]         | [X]  | [H/M/L]   | —
  [competitor1.com]   | [X]         | [X]  | [H/M/L]   | [+/-X domains]
  [competitor2.com]   | [X]         | [X]  | [H/M/L]   | [+/-X domains]
  [competitor3.com]   | [X]         | [X]  | [H/M/L]   | [+/-X domains]


MAP PACK LINKS (Score: [XX]/15)
------------------------------------------------------------------------------
  [P] Local Trust Links                         [XX/15]
      Chamber of Commerce: [Listed / Not listed]
      BBB: [Accredited / Not accredited]
      Industry Associations: [List memberships]
      Government Links: [List .gov links]
      Supplier Links: [List]
      Action: [Join X, apply to Y]


ORGANIC LINKS (Score: [XX]/20)
------------------------------------------------------------------------------
  [P] Editorial & Community Links               [XX/20]
      Local News Mentions: [X links from Y outlets]
      Blog Features: [X guest posts / mentions]
      Sponsorship Links: [X active sponsorships]
      Partner Links: [X partner cross-links]
      Action: [Outreach to X outlets, sponsor Y events]


AI SEARCH LINKS (Score: [XX]/15)
------------------------------------------------------------------------------
  [P] Citation-Worthy Links                     [XX/15]
      "Best of" Articles: [X features in Y articles]
      Missing From: [List "best of" articles featuring competitors but not client]
      Resource Guides: [X features]
      Industry Lists: [X features]
      Action: [Outreach to X articles, get listed in Y guides]


COMPETITOR LINK GAP — TOP 20 OPPORTUNITIES
------------------------------------------------------------------------------
  #  | Domain                  | DR  | Links to Comps | Type
  ---|-------------------------|-----|----------------|------------------
  1  | [domain.com]            | [X] | [X/3 comps]    | [directory/news/etc]
  2  | [domain.com]            | [X] | [X/3 comps]    | [type]
  ...
  20 | [domain.com]            | [X] | [X/3 comps]    | [type]


TOXIC LINK ASSESSMENT (Score: [XX]/10)
------------------------------------------------------------------------------
  Toxic Links Found:      [X]
  Severity:               [Low / Medium / High]
  Disavow Status:         [Current / Needs update / Not created]
  Action:                 [Create/update disavow file with X domains]


------------------------------------------------------------------------------
LINK BUILDING PRIORITY FRAMEWORK
------------------------------------------------------------------------------

IMMEDIATE (Week 1-2):
  1. [Join Chamber of Commerce / BBB if not member]
  2. [Submit to X industry associations]
  3. [Contact X "best of" articles for inclusion]

SHORT-TERM (Month 1-3):
  4. [Outreach to local news for expert quotes]
  5. [Identify and sponsor X community events]
  6. [Guest post pitches to X local blogs]
  7. [Partner cross-promotion with X businesses]

ONGOING (Monthly):
  8. [Monitor for new "best of" articles — get listed]
  9. [HARO/expert quote responses — X per week]
  10. [Community engagement for natural link opportunities]

ESTIMATED MONTHLY LINK ACQUISITION TARGET: [X-Y new referring domains/month]

==============================================================================
```

---

## Cross-References

| Skill | Relationship | When to Use Together |
|---|---|---|
| `/local-content-strategy` | **Complementary** — Content (Phase 12) creates linkable assets that attract editorial links naturally. Without great content, outreach has nothing to offer. | Run content strategy immediately after link audit to create assets that close link gaps. |
| `/local-citation-audit` | **Related but distinct** — Citations (Phase 4) are directory listings focused on NAP consistency. Link audit covers a broader range of link sources including editorial, community, and "best of" links. | Citations handle structured directory links; link audit handles everything else. |
| `/local-competitor-analysis` | **Data source** — Competitor analysis (Phase 6) provides the competitive context; link gap analysis reveals specific link-level advantages competitors hold. | Use competitor analysis data to focus link gap analysis on the right competitors. |
| `/local-on-page-audit` | **Foundation** — Strong on-page content (Phase 5) makes pages link-worthy. Weak content means outreach emails get ignored. | Ensure on-page quality before launching link outreach campaigns. |
| `/local-content-strategy` | **Next step** — Phase 12 creates the content that attracts links. The link audit identifies what types of links are needed; content strategy creates the assets to earn them. | Always run content strategy after link audit to align content creation with link gaps. |

---

*Phase 11 reveals the link landscape and builds a channel-aware acquisition strategy. For the content assets that will attract these links naturally, proceed to `/local-content-strategy` (Phase 12).*
