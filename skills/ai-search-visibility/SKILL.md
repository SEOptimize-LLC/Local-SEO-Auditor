---
name: ai-search-visibility
description: AI Search visibility audit for ChatGPT, Gemini, and Perplexity citation optimization using 2025 Whitespark AI ranking factors
version: 1.0.0
tags: [local-seo, ai-search, chatgpt, gemini, perplexity, ai-overviews, emerging-channel]
related: [local-citation-audit, local-content-strategy, review-audit, local-schema-markup, local-on-page-audit]
---

# Phase 14: AI Search Visibility Audit (NEW for 2026)

> **AI Search is a fundamentally new discovery channel with DISTINCT ranking factors.** Unlike Map Pack and Organic, where Google's algorithm directly ranks listings, AI Search surfaces businesses through citation by large language models --- ChatGPT, Google Gemini, Perplexity, and others. The signals that drive AI citation are measurably different from traditional SEO. Social signals carry 4.5x more weight in AI Search than in Map Pack. Citations carry 2x more weight. Behavioral signals carry less than half the weight. This is not an extension of existing SEO --- it is a parallel channel that requires dedicated strategy.

---

## When to Use This Skill

- **As part of the full Local SEO Audit**: Run this as Phase 14, after completing the core audits. AI Search visibility builds on top of strong foundational SEO but requires its own assessment layer.
- **As a standalone audit**: When a client asks about AI search visibility, wants to understand their presence in ChatGPT or Gemini results, or is seeing competitors mentioned in AI-generated recommendations.
- **Trigger scenarios**:
  - Client asks "Why does ChatGPT recommend my competitor but not me?"
  - Client is in a competitive market where AI-driven discovery is growing
  - Client wants to future-proof their local SEO strategy
  - Industry reports show increasing traffic from AI-powered search tools
  - Client notices AI Overviews appearing for their target keywords in Google

---

## Channel Impact --- AI Search Ranking Factors (2025 Whitespark Survey)

AI Search has its own distinct ranking factor weights. These differ significantly from Map Pack and Organic.

| Signal Category | AI Search Weight | Map Pack Weight | Organic Weight | Key Difference |
|-----------------|-----------------|-----------------|----------------|----------------|
| **On-Page SEO** | **24%** | 15% | 33% | Moderate --- AI needs citable, structured content |
| **Social Signals** | **18%** | ~0% | ~0% | **MASSIVE** --- Social is nearly irrelevant for Map Pack/Organic but is the #2 AI factor |
| **Review Signals** | **16%** | 20% | 15% | Comparable across channels, but AI weighs review engagement (helpful votes) more |
| **Citation Signals** | **13%** | 6% | 10% | **2x Map Pack weight** --- AI engines rely heavily on consistent business data across sources |
| **Link Signals** | **13%** | 8% | 24% | Moderate --- links matter but less than for Organic |
| **GBP Signals** | **12%** | 32% | 7% | Lower than Map Pack --- AI engines pull from broader sources than just GBP |
| **Behavioral Signals** | **4%** | 9% | 10% | **Much lower** --- AI engines rely less on click/engagement data |

**Strategic Implication**: A business optimized purely for Map Pack (heavy GBP focus) will underperform in AI Search. AI Search demands broader web presence --- social activity, citation breadth, and citable content.

---

## Prerequisites

Before beginning the AI Search visibility audit, ensure you have:

1. **Discovery Brief from Phase 1** (`/discovery-intake`)
   - Business name, primary services, target city/region
   - Target keywords (these will be tested in AI engines)
   - Competitor list (for comparison of AI mentions)

2. **Completed Core Audits** (recommended)
   - `/local-citation-audit` --- Citation count and consistency baseline
   - `/local-content-strategy` --- Content inventory and quality assessment
   - `/review-audit` --- Review volume and engagement metrics
   - `/local-schema-markup` --- Schema completeness assessment

3. **Access to AI Search Platforms**
   - ChatGPT (free or Plus account)
   - Google Gemini
   - Perplexity AI
   - (Optional) Microsoft Copilot, Claude

---

## Assessment Framework

---

### 14.1 AI Visibility Score --- Direct Testing

The most direct measure of AI search visibility: does the business appear when users ask AI engines for local recommendations?

**Testing Protocol**:

1. **Construct Test Queries**: Create 10-15 queries that a potential customer would ask an AI assistant:
   - "Best [service] in [city]"
   - "Who is the top [service provider] near [neighborhood/city]?"
   - "Recommend a [service] in [city] with good reviews"
   - "What [service provider] in [city] is open on weekends?"
   - "[Service] near [city] with [specific attribute like 'emergency' or '24/7']"

2. **Test Across Platforms**: Run each query in:
   - ChatGPT (GPT-4 with browsing enabled)
   - Google Gemini
   - Perplexity AI

3. **Record Results**:

```
==============================================================================
AI VISIBILITY TEST RESULTS
==============================================================================

Query                          | ChatGPT | Gemini | Perplexity | Mentioned?
-------------------------------|---------|--------|------------|----------
"Best [service] in [city]"    |  Y/N    |  Y/N   |   Y/N      | [0-3]/3
"Top [service] near [area]"   |  Y/N    |  Y/N   |   Y/N      | [0-3]/3
"Recommend [service] [city]"  |  Y/N    |  Y/N   |   Y/N      | [0-3]/3
[... repeat for all queries]  |         |        |            |
==============================================================================

VISIBILITY RATE: [X]% of queries returned a mention of the business
COMPETITOR VISIBILITY: [Comp 1: X%] [Comp 2: X%] [Comp 3: X%]
==============================================================================
```

**Scoring** (out of 25 points):
- 0 points: Business not mentioned in any AI engine for any query
- 5 points: Mentioned in 1 engine for 1-2 queries
- 10 points: Mentioned in 1-2 engines for 3-5 queries
- 15 points: Mentioned in 2+ engines for 5-8 queries
- 20 points: Mentioned in all 3 engines for most queries
- 25 points: Consistently mentioned across all engines, often as the top recommendation

---

### 14.2 "Best of Local" Listicle Presence

AI engines heavily cite "Best X in City" listicle articles when generating local recommendations. Presence on these lists is one of the strongest drivers of AI visibility.

**Assessment**:

1. Search Google for: `"best [service] in [city]"` and review the top 10 results
2. Identify listicle-style articles (Yelp Top 10, local blog roundups, niche directory lists)
3. Check if the client business is mentioned in these articles
4. Check if competitors are mentioned

**Key Sources to Check**:
- Yelp "Top 10" and "Best of" lists
- Local newspaper/magazine "Best of [City]" awards
- Niche industry "Best [Service] in [City]" blog posts
- Reddit threads recommending local businesses
- Nextdoor recommendations
- Local Facebook group recommendations

**Scoring** (out of 15 points):
- 0 points: Not present on any "Best of" lists
- 5 points: Present on 1-2 listicles
- 10 points: Present on 3-5 listicles, including at least one high-authority source
- 15 points: Present on 5+ listicles across multiple authoritative sources

---

### 14.3 Citation Breadth for AI Visibility

AI Search requires significantly broader citation coverage than Map Pack. While 50-75 citations may suffice for Map Pack competitiveness, AI engines benefit from 100+ consistent citations.

**Why More Citations Matter for AI**: AI engines aggregate data from dozens of sources to build confidence in business information. The more consistent sources confirming the business name, address, phone, services, and reviews, the more likely the AI is to cite the business with confidence.

**Assessment Using DFS MCP**:

```
TOOL: mcp__dfs-mcp__business_data_business_listings_search
USE:  Search for the business across listing platforms to count total
      citation presence and assess breadth.
PARAMETERS:
  - keyword: Business name
  - location_code: Target location code
  - limit: 50
```

**Citation Tiers for AI Visibility**:

| Tier | Citation Count | AI Impact |
|------|---------------|-----------|
| Insufficient | 0-25 | Very low AI visibility; business data not widely confirmed |
| Basic | 26-50 | Minimal AI visibility; enough for Map Pack but not AI |
| Moderate | 51-75 | Some AI visibility; business appears in some AI responses |
| Strong | 76-100 | Good AI visibility; consistent presence across engines |
| Excellent | 100+ | High AI visibility; strong data confidence for AI citation |

**Scoring** (out of 15 points):
- 0 points: Fewer than 25 citations
- 5 points: 25-50 citations
- 8 points: 51-75 citations
- 12 points: 76-100 citations
- 15 points: 100+ citations with high consistency

---

### 14.4 Social Signals Audit

Social signals are the second most important AI Search factor at 18% --- a dramatic departure from Map Pack and Organic where social signals carry negligible weight. AI engines interpret active social presence as a signal of business legitimacy and relevance.

**Assessment Areas**:

#### Facebook Business Page
- Page exists and is claimed: Y/N
- Follower count: [X]
- Post frequency: [X/month]
- Average engagement per post (likes, comments, shares): [X]
- Facebook reviews count and average rating: [X] / [X.X stars]
- Response rate to messages: [X%]
- Business info completeness (hours, services, about section): [Complete/Partial/Missing]

#### Instagram Business Profile
- Profile exists: Y/N
- Follower count: [X]
- Post frequency: [X/month]
- Average engagement rate: [X%]
- Location tags used: Y/N
- Service-related hashtags used: Y/N
- Stories/Reels activity: [Active/Inactive]

#### Other Social Platforms
- LinkedIn company page: Y/N (especially relevant for B2B services)
- YouTube channel: Y/N (video content is increasingly cited by AI)
- X/Twitter business account: Y/N
- TikTok presence: Y/N (relevant for consumer-facing businesses)
- Nextdoor business page: Y/N (highly relevant for local services)

#### Brand Mentions Across the Web

```
TOOL: mcp__dfs-mcp__content_analysis_search
USE:  Search for brand mentions across the web to assess social proof
      and brand awareness signals that AI engines use.
PARAMETERS:
  - keyword: Business name or brand
  - search_mode: "as_is"
  - limit: 50
```

**Social Signal Scoring** (out of 15 points):
- 0 points: No social media presence or completely inactive accounts
- 3 points: Social accounts exist but are inactive (no posts in 3+ months)
- 6 points: Active on 1 platform with regular posting
- 9 points: Active on 2+ platforms with regular posting and moderate engagement
- 12 points: Active on 3+ platforms with strong engagement and brand mentions
- 15 points: Strong multi-platform presence with high engagement, active community interaction, and widespread brand mentions

---

### 14.5 Content Citability Assessment

AI engines need content they can excerpt, quote, and reference. Content that is "citable" has specific characteristics that make it useful for AI-generated answers.

**Characteristics of Citable Content**:

1. **Authoritative Local Guides**: "Complete Guide to [Service] in [City]" --- comprehensive, factual, locally relevant
2. **Local Statistics and Data**: Original research, survey results, local market data that AI engines cannot find elsewhere
3. **How-To Content with Clear Steps**: Numbered, structured guides that AI can excerpt step-by-step
4. **FAQ Content with Direct Answers**: Question-answer format that AI engines can directly cite
5. **Comparison/List Content**: "X Types of [Service]" or "X Things to Know About [Service] in [City]"
6. **Expert Commentary**: Quotes, opinions, and insights from named professionals within the business

**Content Citability Audit**:

| Content Type | Present? | Count | Quality | AI-Optimized? |
|-------------|----------|-------|---------|---------------|
| Local Guides | Y/N | [X] | Low/Med/Hi | Y/N |
| Original Data/Stats | Y/N | [X] | Low/Med/Hi | Y/N |
| How-To Guides | Y/N | [X] | Low/Med/Hi | Y/N |
| FAQ Sections | Y/N | [X] | Low/Med/Hi | Y/N |
| Comparison Content | Y/N | [X] | Low/Med/Hi | Y/N |
| Expert Commentary | Y/N | [X] | Low/Med/Hi | Y/N |
| Service Area Content | Y/N | [X] | Low/Med/Hi | Y/N |

**AI Content Optimization Tips**:
- Use clear, factual language that AI engines can confidently excerpt
- Include structured data (tables, numbered lists, clear headings)
- Cite sources and provide evidence for claims
- Include the business name, city, and service naturally in content
- Create content that directly answers questions users would ask an AI assistant
- Publish content consistently (freshness signals matter for AI)

**Scoring** (out of 15 points):
- 0 points: No citable content on the website
- 3 points: Basic service descriptions only
- 6 points: Some blog content but not structured for AI citability
- 9 points: Multiple content types present with moderate quality
- 12 points: Strong content library with clear structure and local relevance
- 15 points: Comprehensive, authoritative content library that AI engines actively cite

---

### 14.6 Schema Completeness for AI Crawlers

AI engines use structured data (schema markup) to extract and verify business information. Complete schema markup significantly increases the probability of AI citation because it provides machine-readable data that AI engines can process with high confidence.

**Critical Schema Elements for AI Visibility**:

| Schema Property | Priority | AI Impact |
|----------------|----------|-----------|
| @type (LocalBusiness or subtype) | Critical | Identifies entity type for AI categorization |
| name | Critical | Business name verification |
| address (streetAddress, city, state, zip) | Critical | Location confirmation |
| telephone | Critical | Contact verification |
| openingHoursSpecification | High | Hours verification for "open now" queries |
| aggregateRating (ratingValue, reviewCount) | High | Review data for recommendation confidence |
| areaServed | High | Service area definition for geographic queries |
| priceRange | Medium | Pricing context for comparison queries |
| sameAs (social profile URLs) | Medium | Cross-platform identity verification |
| hasOfferCatalog / makesOffer | Medium | Service listing for relevance matching |
| description | Medium | Business description for context |
| image | Low | Visual identification |
| geo (latitude, longitude) | Low | Precise location data |

**Assessment**: Cross-reference with `/local-schema-markup` audit. For AI visibility specifically, ensure `sameAs`, `aggregateRating`, `areaServed`, and `hasOfferCatalog` are implemented --- these are commonly missing even on sites with basic LocalBusiness schema.

**Scoring** (out of 15 points):
- 0 points: No schema markup present
- 3 points: Basic LocalBusiness schema (name, address, phone only)
- 6 points: LocalBusiness schema with hours, description, and geo
- 9 points: Complete LocalBusiness schema including aggregateRating and areaServed
- 12 points: Full schema with sameAs links, offer catalog, and all recommended properties
- 15 points: Complete, validated schema with no errors, covering all properties in the table above

---

### 14.7 AI Mention Monitoring Framework

Ongoing monitoring of AI mentions is essential because AI search results change as models are updated and new content is indexed.

**Monitoring Setup**:

1. **Monthly AI Query Testing**: Re-run the 10-15 test queries from Section 14.1 monthly. Track changes in mention rate.
2. **Brand Alert Setup**: Configure Google Alerts for the business name, owner name, and key service+city combinations.
3. **Content Tracking**: Monitor which website pages are being cited by AI engines (check Perplexity source links, Gemini citations).
4. **Competitor Tracking**: Monthly check of competitor AI visibility for the same queries.

**Monitoring Dashboard Template**:

```
==============================================================================
AI VISIBILITY MONITORING --- [Month/Year]
==============================================================================

Metric                     | Baseline | Current | Trend
---------------------------|----------|---------|------
AI Mention Rate (% queries)|   [X%]   |  [X%]   | +/-
ChatGPT Mentions           |   [X]    |  [X]    | +/-
Gemini Mentions            |   [X]    |  [X]    | +/-
Perplexity Mentions        |   [X]    |  [X]    | +/-
"Best of" List Presence    |   [X]    |  [X]    | +/-
Total Citations            |   [X]    |  [X]    | +/-
Social Engagement Score    |   [X]    |  [X]    | +/-
Citable Content Pages      |   [X]    |  [X]    | +/-
==============================================================================
```

---

## Scoring Rubric

```
==============================================================================
            AI SEARCH VISIBILITY SCORE
==============================================================================

Section                              | Max   | Score
-------------------------------------|-------|------
14.1 AI Visibility (Direct Test)     | /25   |  ___
14.2 "Best of" Listicle Presence     | /15   |  ___
14.3 Citation Breadth                | /15   |  ___
14.4 Social Signals                  | /15   |  ___
14.5 Content Citability              | /15   |  ___
14.6 Schema Completeness for AI      | /15   |  ___
                                     |-------|------
TOTAL AI VISIBILITY SCORE            | /100  |  ___

==============================================================================
SCORE INTERPRETATION:
  80-100: Strong AI visibility --- business is actively cited by AI engines
  60-79:  Moderate visibility --- appearing in some AI results, room to grow
  40-59:  Emerging visibility --- foundation exists but gaps in key areas
  20-39:  Low visibility --- significant investment needed in social, content,
          and citations
  0-19:   Not visible --- AI engines are not citing this business
==============================================================================
```

---

## Strategy Recommendations by Score Range

**Score 0-19 (Not Visible)**:
1. Build citation count to 75+ as immediate priority
2. Claim and activate Facebook and Instagram business pages
3. Implement complete LocalBusiness schema
4. Create 3-5 citable content pieces (local guides, FAQ pages)
5. Get listed on "Best of [City]" lists through outreach

**Score 20-39 (Low Visibility)**:
1. Expand citations to 100+ with emphasis on consistency
2. Increase social posting to 3-5x/week across 2+ platforms
3. Publish monthly authoritative local content
4. Add aggregateRating and sameAs to schema
5. Actively pursue "Best of" list placements

**Score 40-59 (Emerging)**:
1. Focus on content citability --- create content AI engines want to quote
2. Build social engagement (not just posting, but community interaction)
3. Expand schema to include full offer catalog and service area
4. Monitor and respond to AI mention trends
5. Create original local data/research content

**Score 60-79 (Moderate)**:
1. Optimize existing content for AI excerpt patterns
2. Pursue high-authority "Best of" placements
3. Increase social proof signals (review engagement, brand mentions)
4. Ensure schema is error-free and complete
5. Establish monthly AI visibility monitoring cadence

**Score 80-100 (Strong)**:
1. Maintain citation freshness and accuracy
2. Continue social engagement and content publishing cadence
3. Monitor for new AI platforms and test visibility
4. Defend "Best of" list positions
5. Track and respond to changes in AI ranking factors

---

## DFS MCP Data Sources

| Tool | Purpose |
|------|---------|
| `mcp__dfs-mcp__business_data_business_listings_search` | Count and assess citation breadth across listing platforms |
| `mcp__dfs-mcp__content_analysis_search` | Search for brand mentions, "Best of" list presence, and social proof signals across the web |
| `mcp__dfs-mcp__serp_organic_live_advanced` | Check which "Best of [City]" listicle pages rank for target queries (these feed AI citations) |

---

## Output Format

```
==============================================================================
PHASE 14: AI SEARCH VISIBILITY AUDIT
==============================================================================

Business: [Business Name]
Audit Date: [YYYY-MM-DD]
Auditor: Claude Code (Local SEO Auditor)

------------------------------------------------------------------------------
AI VISIBILITY SCORE: [XX]/100 --- [Strong/Moderate/Emerging/Low/Not Visible]
------------------------------------------------------------------------------

14.1 DIRECT AI VISIBILITY TEST                              [XX/25]
     Mention Rate: [X%] across [X] test queries
     ChatGPT: [X/15 queries] | Gemini: [X/15] | Perplexity: [X/15]
     Top Competitor Mention Rate: [X%] ([Competitor Name])

14.2 "BEST OF" LISTICLE PRESENCE                            [XX/15]
     Lists Found: [X]
     Sources: [List sources where business appears]
     Competitor Presence: [Comp 1: X lists] [Comp 2: X lists]

14.3 CITATION BREADTH                                       [XX/15]
     Total Citations: [X]
     Consistency Rate: [X%]
     Target for AI Visibility: 100+
     Gap: [X citations needed]

14.4 SOCIAL SIGNALS                                         [XX/15]
     Facebook: [Followers] | [Posts/mo] | [Engagement]
     Instagram: [Followers] | [Posts/mo] | [Engagement]
     Other Platforms: [List active platforms]
     Brand Mentions Found: [X]

14.5 CONTENT CITABILITY                                     [XX/15]
     Citable Content Pieces: [X]
     Content Types Present: [List types]
     AI-Optimized Content: [X pieces]

14.6 SCHEMA COMPLETENESS                                    [XX/15]
     Schema Present: Y/N
     Properties Implemented: [X/14]
     Missing Critical Properties: [List]

------------------------------------------------------------------------------
PRIORITY ACTIONS FOR AI VISIBILITY
------------------------------------------------------------------------------

IMMEDIATE (Weeks 1-4):
  1. [Highest-impact action]
  2. [Second action]
  3. [Third action]

SHORT-TERM (Months 2-3):
  4. [Action]
  5. [Action]

ONGOING (Monthly):
  6. [Recurring action]
  7. [Recurring action]

==============================================================================
```

---

## Cross-References

| Skill | Relationship | When to Use Together |
|-------|-------------|----------------------|
| `/local-citation-audit` | **Critical Input** --- AI Search weights citations at 13% (2x Map Pack). Citation count and consistency from the citation audit directly determines AI visibility. The AI audit adds the requirement for 100+ citations. | Always run citation audit first. AI audit adds the higher citation target. |
| `/local-content-strategy` | **Critical Input** --- Content citability (24% of AI ranking) depends on the content strategy. The AI audit assesses content through the lens of "would an AI engine cite this?" | Content strategy defines what to create; AI audit defines how to make it citable. |
| `/review-audit` | **Supporting** --- Review signals carry 16% of AI ranking weight. Review engagement metrics (helpful votes, owner responses) matter more for AI than raw count. | Review audit covers the fundamentals; AI audit emphasizes engagement signals. |
| `/local-schema-markup` | **Supporting** --- Schema completeness directly affects AI crawlers' ability to extract and verify business data. The AI audit adds AI-specific schema priorities (sameAs, aggregateRating, hasOfferCatalog). | Schema audit covers implementation; AI audit prioritizes which properties matter most for AI engines. |
| `/local-on-page-audit` | **Supporting** --- On-page SEO carries 24% of AI ranking weight. Content structure, heading hierarchy, and factual clarity all affect AI citability. | On-page audit assesses traditional optimization; AI audit assesses content from an AI citation perspective. |

---

*AI Search is the fastest-evolving channel in local SEO. The ranking factors and best practices in this skill are based on 2025 Whitespark survey data and current AI engine behavior as of early 2026. This skill should be reviewed and updated quarterly as AI search platforms evolve. For the complete audit workflow, this phase follows Phase 13 (Competitor Analysis) and feeds into Phase 15 (Site Architecture) and Phase 16 (Reporting).*
