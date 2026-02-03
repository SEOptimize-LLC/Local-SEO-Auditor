---
name: Local Landing Pages
description: Phase 8 of the Local SEO Audit suite. Evaluates existing service and location landing pages, scores them against a comprehensive template, identifies content gaps, detects duplicate/thin content, and produces content briefs for pages that need creation or improvement. Ensures each page provides unique, locally-specific value rather than city-name-swapped boilerplate.
version: 1.0.0
tags: [local-seo, landing-pages, content-strategy, service-pages, location-pages, content-briefs]
related:
  - local-on-page-audit (Phase 7)
  - local-keyword-research (Phase 5)
  - map-pack-analysis (Phase 6)
  - local-citation-audit (Phase 4)
---

# Phase 8: Local Landing Pages

## When to Use

Run this skill when:
- Performing a full Local SEO audit (Phase 8, the final phase)
- Phase 7 (On-Page Audit) revealed thin or missing pages for target keywords
- A client needs location-specific pages for a multi-location or service-area business
- Existing location pages are clearly template-swapped (same content with different city names)
- Content strategy planning for local SEO requires a structured approach
- AI Search visibility requires comprehensive, unique content per service/location

## Channel Impact

Landing pages are the execution layer for on-page optimization. Their quality directly determines performance across all channels:

| Channel         | Click Share | How Landing Pages Impact It                                |
|-----------------|-------------|-------------------------------------------------------------|
| Local Map Pack  | 44%         | GBP links to landing pages. Google uses page content for Map Pack justifications. Local schema on landing pages reinforces entity signals. |
| Local Organic   | 30%         | Each landing page targets a keyword cluster. Content depth, E-E-A-T, and uniqueness determine organic ranking potential. |
| AI Search       | Emerging    | AI models prefer comprehensive, well-structured pages with FAQ content. Unique local content gets cited more than boilerplate. |

**Critical Rule:** Location pages with city-name-swapped content are a negative ranking signal. Google's Helpful Content system specifically penalizes scaled, non-unique location pages. Every location page must contain genuinely unique, locally-relevant content.

## Prerequisites

Before running this skill, you should have:
1. **Phase 5 (Keyword Research)** completed with the full keyword matrix and page mapping
2. **Phase 7 (On-Page Audit)** completed with per-page scores and gap analysis
3. **Service list** with all services offered
4. **Location list** with all cities, neighborhoods, and service areas
5. **Existing site map** or crawl showing current page inventory

## Assessment Framework

### Step 1: Service Page Structure Template

Every primary service page should follow this proven structure:

```
SERVICE PAGE TEMPLATE
=====================

1. HERO SECTION
   - H1: [Service] in [City] (with location keyword)
   - Subheadline: Value proposition in one sentence
   - Primary CTA button: "Get a Free Estimate" / "Schedule Service"
   - Trust badges: Licensed, insured, years in business, rating

2. INTRODUCTION (150-200 words)
   - Primary keyword in first sentence
   - City and neighborhood mentions
   - What the service entails (customer-focused language)
   - Why choose this business for this service
   - Local context hook

3. HOW IT WORKS / SERVICE DETAILS (300-500 words)
   - Step-by-step process description
   - Local context woven in:
     * Climate factors affecting the service
     * Local building types and common issues
     * City-specific regulations or permits
     * Response times for the area
   - Technical expertise demonstration (E-E-A-T)
   - Pricing transparency (ranges or "starting at")

4. LOCAL COVERAGE SECTION (100-150 words)
   - Neighborhoods and areas served for this service
   - Embedded Google Map showing service area
   - Mention of specific neighborhoods by name
   - Drive time or response time from business location

5. FAQ SECTION (5-8 questions, 50-100 words each answer)
   - "How much does [service] cost in [city]?"
   - "How long does [service] take?"
   - "Do I need a permit for [service] in [city]?"
   - "What should I look for in a [service provider] in [city]?"
   - "Is [service] covered by homeowner's insurance?"
   - Schema: FAQPage markup on all Q&A pairs

6. LOCAL TESTIMONIALS (3-5 reviews)
   - Reviews specifically mentioning this service
   - Include reviewer name and neighborhood/area
   - Star rating displayed
   - Pulled from Google, Yelp, or first-party reviews

7. CALL TO ACTION
   - Phone number (click-to-call on mobile)
   - Contact form
   - "Serving [City] and surrounding areas"
   - Hours of operation

TOTAL TARGET: 800-1,500 words of unique content per service page
```

### Step 2: Location/Service Area Page Requirements

For businesses serving multiple cities or neighborhoods, location pages must contain genuinely unique content.

```
LOCATION PAGE UNIQUENESS REQUIREMENTS
======================================

PROHIBITED (will trigger Helpful Content penalty):
- Copy-pasting service page content and swapping city names
- Using the same paragraphs with only location references changed
- Thin pages with just a city name and phone number
- Auto-generated pages with no human-written local content

REQUIRED UNIQUE ELEMENTS PER LOCATION PAGE:

1. Neighborhood Characteristics (100-150 words)
   - What makes this area unique
   - Types of homes/buildings (age, style, construction)
   - Demographics and community character
   - Why this area has specific service needs

   Example: "South Austin homes built in the 1970s and 1980s
   commonly feature copper piping that develops pinhole leaks
   due to the area's slightly acidic water supply. Many properties
   in the Zilker and Barton Hills neighborhoods also have mature
   oak root systems that can intrude into sewer lines."

2. Area-Specific Problems (100-150 words)
   - Common issues specific to this location
   - Climate or environmental factors
   - Infrastructure age and condition
   - Seasonal patterns for this area

   Example: "Cedar Park's clay-heavy soil expands and contracts
   dramatically with Central Texas drought cycles, causing foundation
   shifts that stress plumbing connections. We see a 40% increase
   in slab leak calls from Cedar Park during summer drought months."

3. Local Codes and Regulations (50-100 words)
   - City-specific permit requirements
   - Local inspection processes
   - Utility provider information
   - Relevant ordinances

4. Response Time and Coverage (50 words)
   - Actual drive time from business to this area
   - Coverage confirmation
   - Emergency availability

5. Local Proof Points (100-150 words)
   - Testimonials from customers in this specific area
   - Job count: "We've completed X jobs in [area]"
   - Case study or project highlight from the area
   - Photos from local job sites

TOTAL TARGET: 600-1,000 words of UNIQUE content per location page
```

### Step 3: Content Uniqueness Assessment

Evaluate existing location pages for duplicate or near-duplicate content.

```
UNIQUENESS SCORING:
===================

Method: Compare each location page against all other location pages
on the site. Calculate text similarity using paragraph-level comparison.

Scoring:
- 90-100% unique: Excellent. Genuinely distinct content.
- 70-89% unique: Acceptable. Some shared structural elements but
  enough unique content.
- 50-69% unique: Warning. Too much shared content. Rewrite needed.
- Below 50% unique: Critical. City-name-swap detected. Full rewrite required.

Check Points:
1. Introduction paragraph: Is it unique or swapped?
2. Service description: Same across locations?
3. FAQ answers: Identical or location-specific?
4. Testimonials: Different per location?
5. Neighborhood details: Actually about the neighborhood?
6. Problems discussed: Relevant to the specific area?
```

### Step 4: Service/Location URL Matrix

For multi-location businesses, plan the URL structure systematically.

```
URL MATRIX TEMPLATE:
====================

Single Location Business:
/[service-1]                    -> Primary service page
/[service-2]                    -> Secondary service page
/[service-1]/[sub-service]      -> Sub-service page
/service-areas                  -> Overview of all areas served
/service-areas/[city]           -> City-specific landing page

Multi-Location Business:
/locations/[city-1]             -> City 1 location page
/locations/[city-2]             -> City 2 location page
/[service]/[city]               -> Service + city combination page
  (only create if search volume justifies it)

URL Rules:
- Use hyphens, not underscores
- Lowercase only
- Include city in URL slug for location pages
- Keep URLs under 75 characters
- Avoid deep nesting (max 3 levels)
- Do NOT create a page for every service+city combination
  unless each has 50+ monthly searches

Example Matrix:
| Service          | Austin  | Round Rock | Cedar Park | Georgetown |
|------------------|---------|------------|------------|------------|
| Plumbing         | /plumber-austin | /plumber-round-rock | Combined | Combined |
| Water Heater     | /water-heater-austin | Combined | Combined | Combined |
| Drain Cleaning   | /drain-cleaning-austin | Combined | Combined | Combined |
| Emergency        | /emergency-plumber-austin | Combined | Combined | Combined |

"Combined" = covered on the main service page + service-areas overview.
Only create dedicated city pages when search volume warrants it.
```

### Step 5: Local Proof Points Audit

Assess the quality and presence of local proof points across landing pages.

```
PROOF POINTS CHECKLIST PER PAGE:
================================

Testimonials:
- [ ] 3-5 testimonials displayed
- [ ] Testimonials mention the specific service
- [ ] Testimonials include customer first name and area
- [ ] Testimonials are recent (within 12 months)
- [ ] Star rating displayed

Case Studies / Project Highlights:
- [ ] At least 1 local project described
- [ ] Before/after photos included
- [ ] Specific location/neighborhood mentioned
- [ ] Problem, solution, and outcome described
- [ ] Approximate project details (timeline, scope)

Photos:
- [ ] Real job site photos (not stock)
- [ ] Team/technician photos
- [ ] Branded vehicle photos
- [ ] Local landmark or context photos
- [ ] Photos are geo-tagged and properly alt-tagged

Trust Signals:
- [ ] License numbers displayed
- [ ] Insurance information
- [ ] BBB badge or rating
- [ ] Industry association logos
- [ ] Years in business
- [ ] Number of jobs completed / customers served
```

### Step 6: Embedded Maps and Geo Elements

```
GEO ELEMENTS PER LANDING PAGE:
===============================

Service Pages:
- Embedded Google Map showing service area boundary
- Service area list (cities, neighborhoods, zip codes)
- "We proudly serve [list of areas]" section

Location Pages:
- Embedded Google Map centered on the specific city/area
- Directions or "We're located X minutes from [area]"
- Nearby landmarks referenced
- Local area zip codes listed

Technical:
- Map embeds use lazy loading (performance)
- Maps do not dominate above-the-fold content
- Geo-metadata in page schema (GeoCoordinates)
- areaServed schema on location pages
```

### Step 7: Internal Linking Between Location/Service Pages

```
INTERNAL LINKING STRATEGY:
==========================

DO:
- Link from each service page to the most relevant location page
  "We offer [service] across Austin, including [East Austin],
  [South Austin], and [Cedar Park]." (contextual links)

- Link from each location page to top 2-3 service pages
  "Our [city] team specializes in [service 1], [service 2],
  and [service 3]." (contextual links)

- Link from blog posts to relevant service and location pages
  "If you're experiencing [problem] in [city], our [service]
  team can help." (contextual link)

DO NOT:
- Create a massive link matrix at the bottom of every page
  linking to every other service/location page
- Use sidebar widgets with 50+ links to all pages
- Create "related pages" sections with excessive links
- Use exact-match anchor text excessively

Target: 3-5 contextual internal links per page, naturally placed
within body content, using varied but relevant anchor text.
```

## Scoring Rubric

### Landing Page Scorecard (per page, 100 points)

| Component                | Points | Criteria                                                |
|--------------------------|--------|---------------------------------------------------------|
| Content Uniqueness       | 20     | 90%+ unique vs other location pages on the site         |
| Content Depth            | 15     | 800+ words (service) / 600+ words (location) of quality content |
| Local Specificity        | 15     | Neighborhood details, local problems, area-specific content |
| Page Structure           | 10     | Follows the service page template structure              |
| FAQ Section              | 10     | 5-8 locally-relevant questions with schema markup        |
| Local Proof Points       | 10     | Testimonials, case studies, photos from the area         |
| CTA Effectiveness        | 5      | Clear, prominent, action-oriented calls to action        |
| Geo Elements             | 5      | Embedded map, service area details, geo-schema           |
| Internal Linking         | 5      | 3-5 contextual links to related service/location pages   |
| Visual Quality           | 5      | Real photos (not stock), properly formatted, fast-loading |

### Aggregate Landing Page Score

| Component                | Points | Criteria                                                |
|--------------------------|--------|---------------------------------------------------------|
| Average Page Score       | 30     | Mean of all individual landing page scores               |
| Coverage Completeness    | 25     | All P1/P2 keywords have a corresponding landing page     |
| Content Uniqueness (site)| 20     | No city-name-swapped pages, all content genuinely unique  |
| URL Structure            | 10     | Logical, clean, consistent URL hierarchy                  |
| Internal Link Network    | 15     | Pages properly interlinked with contextual anchors        |

**Score Interpretation:**
- 90-100: Excellent. Landing pages are a competitive moat.
- 75-89: Good. Most pages are strong, a few need content improvements.
- 50-74: Needs Work. Thin content, uniqueness issues, or missing pages.
- Below 50: Critical. Landing page strategy needs a complete overhaul.

## Content Brief Template

For pages scoring below 75 or pages that need to be created, generate a content brief:

```markdown
### Content Brief: [Page Title]

**Target URL:** /[url-slug]
**Primary Keyword:** [keyword] (Volume: [X], KD: [X])
**Secondary Keywords:** [kw2], [kw3], [kw4]
**Search Intent:** [transactional/commercial/informational]
**Target Word Count:** [800-1500]

**Title Tag:** [60 chars max]
**Meta Description:** [155 chars max]
**H1:** [heading text]

**Content Outline:**
1. Introduction (150-200 words)
   - Key points to cover: [...]
   - Local context to include: [...]

2. Service Details (300-500 words)
   - Process steps: [...]
   - Local factors: [...]
   - Pricing guidance: [...]

3. Local Coverage (100-150 words)
   - Neighborhoods to mention: [...]
   - Response time claims: [...]

4. FAQ Section (5-8 questions)
   - Q1: [question] -> Key answer points: [...]
   - Q2: [question] -> Key answer points: [...]
   - Q3: [question] -> Key answer points: [...]
   - Q4: [question] -> Key answer points: [...]
   - Q5: [question] -> Key answer points: [...]

5. Testimonials to Include
   - Source: [Google/Yelp], Review text: [excerpt], Reviewer: [name/area]

6. Photos Needed
   - [List of photo types and subjects needed]

7. Internal Links to Include
   - Link to [page] with anchor text "[text]"
   - Link to [page] with anchor text "[text]"
   - Link to [page] with anchor text "[text]"

**Schema Markup:** [FAQPage, Service, LocalBusiness]
**Competitive Reference:** [URLs of top-ranking competitor pages to study]
```

## DFS MCP Data Sources

This phase primarily uses data from previous phases rather than direct DFS MCP calls. However, the following tools support content gap analysis:

### Supporting Tool: on_page_instant_pages

Crawl existing landing pages to extract current content for uniqueness comparison.

```python
# DFS MCP Call: Crawl existing landing page
# Tool: on_page_instant_pages

params = {
    "url": "https://example.com/plumber-austin",
    "load_resources": True,
    "enable_javascript": True,
    "enable_browser_rendering": True
}

# Extract: plain text content, word count, headings, images, links
```

### Supporting Tool: content_analysis_search

Find "Best of" roundup articles and competitor content for reference.

```python
# DFS MCP Call: Find competitor and roundup content
# Tool: content_analysis_search

params = {
    "keyword": "best plumber in austin",
    "search_mode": "as_is",
    "limit": 20
}

# Use to identify: competitor page structures, "Best of" articles
# for AI Search targeting, content depth benchmarks
```

### Python Fallback: Content Uniqueness Checker

```python
"""
Content Uniqueness Checker for Location Pages.
Detects city-name-swapped content across location pages.
"""

import re
from difflib import SequenceMatcher
from itertools import combinations


def extract_text_blocks(content: str, min_words: int = 20) -> list[str]:
    """Split content into paragraph-level text blocks."""
    paragraphs = re.split(r'\n\s*\n', content)
    blocks = []
    for p in paragraphs:
        cleaned = p.strip()
        if len(cleaned.split()) >= min_words:
            blocks.append(cleaned)
    return blocks


def remove_location_tokens(text: str, locations: list[str]) -> str:
    """Remove location names to detect city-name-swapped content."""
    result = text.lower()
    for loc in locations:
        result = result.replace(loc.lower(), "[LOCATION]")
    return result


def check_uniqueness(pages: dict[str, str],
                      locations: list[str]) -> list[dict]:
    """
    Check content uniqueness across location pages.

    Args:
        pages: dict mapping URL -> page text content
        locations: list of city/location names to normalize

    Returns:
        List of comparison results with similarity scores
    """
    results = []
    urls = list(pages.keys())

    for url_a, url_b in combinations(urls, 2):
        raw_similarity = SequenceMatcher(
            None, pages[url_a].lower(), pages[url_b].lower()
        ).ratio()

        normalized_a = remove_location_tokens(pages[url_a], locations)
        normalized_b = remove_location_tokens(pages[url_b], locations)
        normalized_similarity = SequenceMatcher(
            None, normalized_a, normalized_b
        ).ratio()

        is_name_swapped = (normalized_similarity > 0.85 and
                           raw_similarity < normalized_similarity - 0.05)

        results.append({
            "page_a": url_a,
            "page_b": url_b,
            "raw_similarity": round(raw_similarity, 3),
            "normalized_similarity": round(normalized_similarity, 3),
            "likely_name_swapped": is_name_swapped,
            "uniqueness_score": round((1 - normalized_similarity) * 100, 1),
            "action": "rewrite" if is_name_swapped else
                      "review" if normalized_similarity > 0.6 else "ok"
        })

    return sorted(results, key=lambda r: r["normalized_similarity"], reverse=True)


def generate_page_inventory(pages: dict[str, dict]) -> list[dict]:
    """
    Generate a landing page inventory with gap analysis.

    Args:
        pages: dict mapping URL -> {"word_count": int, "has_faq": bool,
               "testimonial_count": int, "has_map": bool, "image_count": int}
    """
    inventory = []
    for url, data in pages.items():
        score = 0
        issues = []

        # Content depth
        wc = data.get("word_count", 0)
        if wc >= 800:
            score += 15
        elif wc >= 500:
            score += 8
        else:
            issues.append(f"Thin content: {wc} words (target 800+)")

        # FAQ
        if data.get("has_faq"):
            score += 10
        else:
            issues.append("Missing FAQ section")

        # Testimonials
        tc = data.get("testimonial_count", 0)
        if tc >= 3:
            score += 10
        elif tc >= 1:
            score += 5
        else:
            issues.append("No testimonials on page")

        # Map
        if data.get("has_map"):
            score += 5
        else:
            issues.append("No embedded map")

        # Images
        ic = data.get("image_count", 0)
        if ic >= 3:
            score += 5
        elif ic >= 1:
            score += 2
        else:
            issues.append("No images on page")

        inventory.append({
            "url": url,
            "word_count": wc,
            "partial_score": score,
            "issues": issues,
            "needs_brief": score < 30
        })

    return sorted(inventory, key=lambda p: p["partial_score"])
```

## User Data Requests

Ask the client or account manager for:

1. **Complete service list** with descriptions of each service
2. **All locations/service areas** with any unique characteristics known
3. **Existing customer testimonials** organized by service and location
4. **Job site photos** organized by service type and location
5. **Local knowledge** - common problems per area, building types, weather factors
6. **Competitor URLs** - top 3 competitor service/location pages to benchmark
7. **Brand guidelines** - tone of voice, terminology preferences, CTA preferences
8. **Pricing information** - what pricing details can be shared publicly
9. **Certifications and licenses** for E-E-A-T content
10. **Case studies or project highlights** per service/location

## Output Format

```markdown
## Phase 8: Local Landing Pages

### Landing Page Score: [XX]/100 (Aggregate)

### Page Inventory
| URL | Type | Target Keyword | Word Count | Uniqueness | Score | Status |
|-----|------|----------------|------------|------------|-------|--------|
| /service-1 | Service | [kw] | [count] | [%] | [X/100] | Optimize |
| /city-1 | Location | [kw] | [count] | [%] | [X/100] | Rewrite |
| [missing] | Service | [kw] | -- | -- | -- | Create |

### Content Uniqueness Report
| Page A | Page B | Raw Similarity | Normalized Similarity | City-Swap? | Action |
|--------|--------|---------------|----------------------|------------|--------|

### URL Matrix
[Service x Location matrix showing existing pages, planned pages, and combined pages]

### Content Briefs Needed
[Count] pages need new content briefs:
1. [URL] - [reason] - Priority: [P1/P2/P3]
2. [URL] - [reason] - Priority: [P1/P2/P3]

### Detailed Content Briefs
[Full content brief for each page needing creation or major revision,
using the Content Brief Template above]

### Recommendations
1. **Immediate:** [Fix city-name-swapped pages - these are actively harmful]
2. **Week 1-2:** [Create content briefs for missing P1 keyword pages]
3. **Week 3-4:** [Write and publish highest-priority new pages]
4. **Month 2:** [Optimize existing pages scoring below 75]
5. **Month 3:** [Add proof points, photos, and FAQ sections to all pages]
6. **Ongoing:** [Monthly content freshness updates, new testimonials, seasonal content]
```

## Cross-References

- **Phase 4 (Citation Audit):** Landing pages should contain consistent NAP matching the Master NAP standard. Location pages should link to relevant citation profiles where appropriate.
- **Phase 5 (Keyword Research):** The keyword matrix from Phase 5 defines which landing pages need to exist. Every P1/P2 keyword cluster should map to a landing page.
- **Phase 6 (Map Pack Analysis):** Landing pages are the website component of Map Pack rankings. Pages targeting Map Pack keywords need the strongest local signals and content depth.
- **Phase 7 (On-Page Audit):** Phase 7 scores existing pages; Phase 8 provides the fix plan. Low-scoring pages from Phase 7 become content briefs in Phase 8. The on-page template from Phase 7 defines the optimization targets; the landing page template here defines the content strategy.
