---
name: Local On-Page Audit
description: Phase 7 of the Local SEO Audit suite. Performs a page-by-page evaluation of title tags, meta descriptions, heading hierarchy, content depth, local signals, E-E-A-T indicators, image optimization, and internal linking. Produces per-page and aggregate on-page scores with specific optimization recommendations.
version: 1.0.0
tags: [local-seo, on-page-seo, title-tags, meta-descriptions, content-optimization, eeat, schema]
related:
  - local-keyword-research (Phase 5)
  - map-pack-analysis (Phase 6)
  - local-landing-pages (Phase 8)
  - local-citation-audit (Phase 4)
---

# Phase 7: Local On-Page Audit

## When to Use

Run this skill when:
- Performing a full Local SEO audit (Phase 7, after Map Pack analysis)
- A client's organic rankings are underperforming despite good GBP and review profiles
- Website content has not been updated or optimized in 6+ months
- Preparing to create or revise local landing pages (feeds into Phase 8)
- After a website redesign or migration to check local SEO elements are preserved
- AI Search visibility is low despite strong traditional ranking signals

## Channel Impact

On-page signals have the highest combined weight across all three channels:

| Channel         | Click Share | On-Page Weight | Strategic Implication                                      |
|-----------------|-------------|----------------|------------------------------------------------------------|
| Local Map Pack  | 44%         | 15%            | NAP on site, local schema, title tags with location, service-area content |
| Local Organic   | 30%         | 33%            | Dominant factor. Title tags, content depth, E-E-A-T, internal linking, keyword relevance |
| AI Search       | Emerging    | 24%            | Content quality, structured data, question-answer format, comprehensive topic coverage |

**Combined Weighted Impact:** On-page optimization is the single most impactful area you can directly control. Unlike reviews (dependent on customers) or links (dependent on outreach), on-page changes are fully within the business's control and take effect quickly.

## Prerequisites

Before running this skill, you should have:
1. **Phase 5 (Keyword Research)** completed with keyword-to-page mapping
2. **Phase 6 (Map Pack Analysis)** completed to know which pages support Map Pack rankings
3. **Full site crawl data** (Screaming Frog export preferred, or DFS on_page results)
4. **GSC performance data** for current page-level metrics
5. **Access to the website** for content review

## Assessment Framework

### Step 1: Title Tag Optimization

The title tag is the single most impactful on-page element for local SEO.

```
TITLE TAG FORMULA:
==================
[Primary Service] in [City] | [Business Name]

Constraints:
- Maximum 60 characters (Google truncates at ~60)
- Primary keyword appears first
- City name included
- Business name at end (brand recognition)
- Unique per page (no duplicate titles)

Examples:
GOOD:  "Emergency Plumber in Austin | Smith Plumbing" (46 chars)
GOOD:  "Water Heater Repair Austin TX | Smith Plumbing" (47 chars)
BAD:   "Smith Plumbing - Home" (no keyword, no location)
BAD:   "Plumber | Plumbing | Austin Plumber | Best Plumber" (keyword stuffing)
BAD:   "Smith Plumbing - Emergency Plumber in Austin, Texas - 24/7 Service" (too long)
```

**Audit Checklist per Page:**
- [ ] Contains primary keyword for that page
- [ ] Contains city/location name
- [ ] Under 60 characters
- [ ] Unique across all site pages
- [ ] Business name present
- [ ] No keyword stuffing
- [ ] Compelling (would a searcher click?)

### Step 2: Meta Description Optimization

Meta descriptions do not directly impact rankings but significantly affect CTR, which is a behavioral signal.

```
META DESCRIPTION FORMULA:
=========================
[Service] in [City] - [Value Proposition]. [Call to Action]. [Trust Signal].

Constraints:
- Maximum 155 characters
- Include primary keyword naturally
- Include city/location
- Include a CTA (call, schedule, get quote)
- Include a trust signal (years in business, licensed, rated)

Examples:
GOOD:  "Professional plumbing repair in Austin, TX. Licensed & insured
        with 20+ years experience. Call (512) 555-1234 for free estimates." (139 chars)
BAD:   "Welcome to our website. We offer many services. Contact us today."
        (no keyword, no location, no specifics)
```

**Audit Checklist per Page:**
- [ ] Contains primary keyword
- [ ] Contains city/location
- [ ] Under 155 characters
- [ ] Includes CTA
- [ ] Includes differentiator or trust signal
- [ ] Unique across all site pages

### Step 3: Heading Hierarchy (H1-H6)

Proper heading structure signals content organization to search engines and AI models.

```
HEADING RULES:
==============

H1: One per page. Contains primary keyword + location.
    Example: "Expert Plumbing Services in Austin, TX"

H2: Section headings. Use for major content sections.
    Include secondary keywords and service variants.
    Examples: "Our Residential Plumbing Services"
              "Why Choose Smith Plumbing in Austin?"
              "Service Areas in Greater Austin"

H3: Subsection headings under H2s.
    Include long-tail keywords and specific services.
    Examples: "Water Heater Installation"
              "Drain Cleaning and Repair"

COMMON MISTAKES:
- Multiple H1 tags on a single page
- Skipping heading levels (H1 -> H3, no H2)
- Using headings for styling rather than structure
- H1 that does not include the primary keyword
- H1 that is identical to the title tag (waste of a ranking signal)
```

### Step 4: First 100 Words Analysis

Google gives disproportionate weight to the opening content of a page. The first 100 words should establish local relevance immediately.

```
FIRST 100 WORDS CHECKLIST:
===========================

Must Include:
- Primary keyword (naturally, within first sentence)
- City/location name
- Neighborhood or service area reference
- Core value proposition
- Local context (what makes this service local)

Example (Plumber in Austin):
"Looking for a reliable plumber in Austin? Smith Plumbing has served
homeowners and businesses across East Austin, Round Rock, and Cedar Park
for over 20 years. From emergency pipe repairs to complete bathroom
remodels, our licensed Austin plumbers deliver fast, affordable service
with upfront pricing and a satisfaction guarantee."

Analysis Points:
- Primary keyword "plumber in Austin" in first sentence
- Neighborhoods mentioned: East Austin, Round Rock, Cedar Park
- Local proof: "20 years" serving the area
- Services mentioned: emergency repairs, remodels
- Trust signals: licensed, upfront pricing, guarantee
```

### Step 5: E-E-A-T Signals for Local Businesses

Experience, Expertise, Authoritativeness, and Trustworthiness signals are increasingly important for both Organic and AI Search.

```
E-E-A-T LOCAL SIGNALS:
======================

Experience:
- Years in business mentioned on page
- Project photos and case studies from local jobs
- Before/after examples from the service area
- "Served X customers in [City]"

Expertise:
- Licenses and certifications displayed
- Industry association memberships
- Specialized training or equipment
- Technical content demonstrating knowledge

Authoritativeness:
- Awards and recognition (local and industry)
- Media mentions and press coverage
- Community involvement documentation
- Professional author bios on content pages

Trustworthiness:
- Customer testimonials with names and locations
- Star ratings and review snippets
- BBB accreditation badge
- Insurance and bonding information
- Clear contact information (NAP)
- Privacy policy and terms of service
```

### Step 6: Image Optimization with Local Context

Images provide ranking opportunities in Google Images and support content relevance signals.

```
IMAGE OPTIMIZATION:
===================

Alt Text Formula: [Service] [action/detail] in [location] - [context]
Example: "Plumber repairing burst pipe in East Austin home - Smith Plumbing"

File Name Convention: [service]-[location]-[descriptor].jpg
Example: "plumber-austin-pipe-repair.jpg"

Local Image Checklist:
- [ ] Alt text includes service keyword + location
- [ ] File names are descriptive (not IMG_4532.jpg)
- [ ] Images are compressed (WebP preferred, <200KB)
- [ ] Images have width/height attributes (CLS prevention)
- [ ] Local photos used (actual job sites, team, vehicles)
- [ ] Geo-tagged photos where possible (EXIF data with GPS)
- [ ] Hero images are locally relevant (city skyline, landmarks)

Image Types to Include on Service Pages:
1. Team/technician photos (builds trust)
2. Branded vehicle/uniform photos (brand recognition)
3. Before/after project photos (demonstrates work)
4. Local landmark context photos (geographic signals)
5. License/certification images (authority signals)
```

### Step 7: Local Content Signals in Body Copy

Beyond the first 100 words, the full page content should weave in local signals naturally.

```
LOCAL CONTENT SIGNALS:
======================

Geographic References:
- Neighborhoods served
- Adjacent cities
- County name
- Regional landmarks
- Major highways/intersections near service area

Local Context:
- Climate/weather references relevant to service
  ("Austin's summer heat puts extra strain on AC systems")
- Local building codes and regulations
  ("City of Austin plumbing permits require...")
- Local building types and construction styles
  ("Many East Austin homes built in the 1960s have galvanized pipes")
- Local events or seasonal factors
  ("SXSW season means increased demand for emergency services")

Community Signals:
- Local charity or sponsorship mentions
- Community event participation
- Local partnership references
- City-specific statistics or facts
```

### Step 8: Internal Linking Audit

Internal links distribute ranking power and help search engines understand site structure.

```
INTERNAL LINKING RULES:
========================

1. Every service page links to related services
   (e.g., "Water Heater Repair" links to "Water Heater Installation")

2. Location pages link to relevant service pages
   (e.g., "Plumber in East Austin" links to all services offered there)

3. Service pages link to relevant location pages
   (e.g., "Drain Cleaning" links to "Drain Cleaning in Austin" sub-pages)

4. Blog posts link to relevant service pages (not the other way around)

5. Homepage links to top service and location pages

Audit Points:
- [ ] No orphan pages (pages with zero internal links pointing to them)
- [ ] Service pages interlink to related services
- [ ] Location pages interlink to services in that area
- [ ] Anchor text includes target keywords (not "click here")
- [ ] Internal links use contextual placement within body copy
- [ ] No excessive linking (keep to 3-5 relevant internal links per page)
- [ ] Link depth: critical pages within 3 clicks of homepage
```

### Step 9: Schema Markup Audit

Structured data helps search engines understand page content and enables rich results.

```
REQUIRED LOCAL SCHEMA:
======================

1. LocalBusiness (or specific subtype like Plumber, Dentist, etc.)
   - name, address, telephone, url
   - openingHoursSpecification
   - geo (latitude, longitude)
   - areaServed
   - priceRange
   - image, logo

2. Service (on each service page)
   - name, description, provider
   - areaServed, serviceType

3. FAQPage (on pages with FAQ sections)
   - Question + acceptedAnswer pairs

4. Review/AggregateRating (if displaying reviews on site)
   - ratingValue, reviewCount, bestRating

5. BreadcrumbList (sitewide)
   - itemListElement for navigation path

Validation:
- Test with Google Rich Results Test
- Check Google Search Console for schema errors
- Ensure no schema spam (fake reviews, incorrect business type)
```

## Scoring Rubric

### Per-Page Score (100 points each)

| Component              | Points | Criteria                                              |
|------------------------|--------|-------------------------------------------------------|
| Title Tag              | 15     | Keyword + location + brand + under 60 chars + unique  |
| Meta Description       | 10     | Keyword + location + CTA + under 155 chars + unique   |
| H1 Tag                 | 10     | Single H1, includes primary keyword + location        |
| Heading Hierarchy      | 5      | Proper H2/H3 structure, no skipped levels             |
| First 100 Words        | 10     | Keyword + location + neighborhoods + value prop       |
| Content Depth          | 15     | 500+ words, comprehensive coverage, unique content    |
| Local Signals          | 10     | Neighborhoods, landmarks, climate, codes, local proof |
| E-E-A-T Signals        | 8      | Credentials, experience proof, trust indicators       |
| Image Optimization     | 7      | Alt text, file names, compression, local images       |
| Internal Linking       | 5      | 3-5 relevant internal links with keyword anchors      |
| Schema Markup          | 5      | Correct structured data for page type                 |

### Aggregate Site Score (100 points)

| Component              | Points | Criteria                                              |
|------------------------|--------|-------------------------------------------------------|
| Average Page Score     | 40     | Mean of all individual page scores                    |
| Title Tag Consistency  | 10     | No duplicates, formula applied consistently           |
| Sitewide Schema        | 10     | LocalBusiness + BreadcrumbList implemented correctly   |
| Internal Link Structure| 10     | No orphan pages, logical hierarchy, proper anchors    |
| Content Coverage       | 15     | All target keywords have corresponding optimized pages |
| Technical Compliance   | 15     | Mobile-friendly, fast load, no crawl errors           |

**Score Interpretation:**
- 90-100: Excellent. On-page is a competitive advantage across all channels.
- 75-89: Good. Minor optimizations needed. Focus on weakest pages first.
- 50-74: Needs Work. Significant gaps in titles, content, or local signals. 60-day plan.
- Below 50: Critical. On-page issues are materially hurting rankings. Immediate action.

## DFS MCP Data Sources

### Primary Tool: on_page_instant_pages

Crawl and analyze individual pages for on-page SEO factors.

```python
# DFS MCP Call: Analyze on-page elements
# Tool: on_page_instant_pages

params = {
    "url": "https://example.com/plumber-austin",
    "load_resources": True,
    "enable_javascript": True,
    "enable_browser_rendering": True
}

# Key response fields to extract:
# - meta.title (title tag)
# - meta.description (meta description)
# - meta.htags (h1, h2, h3 hierarchy)
# - meta.content.plain_text_word_count
# - meta.content.automated_readability_index
# - meta.images (alt text, src, dimensions)
# - meta.internal_links_count
# - meta.external_links_count
# - meta.canonical
# - meta.og_tags (Open Graph)
# - meta.schema (structured data)
# - page_timing (load speed data)
# - status_code
```

### Supporting Tool: on_page_lighthouse

For technical performance metrics that impact on-page effectiveness.

```python
# DFS MCP Call: Lighthouse performance audit
# Tool: on_page_lighthouse

params = {
    "url": "https://example.com/plumber-austin",
    "for_mobile": True,
    "categories": ["performance", "seo", "accessibility", "best-practices"]
}

# Key response fields:
# - categories.performance.score
# - categories.seo.score
# - categories.accessibility.score
# - audits (detailed audit results)
# - lighthouse_version
```

### Python Fallback: On-Page Scoring Engine

```python
"""
On-Page SEO Scoring Engine for Local Pages.
Scores individual pages against local SEO best practices.
"""

import re
from dataclasses import dataclass, field
from typing import Optional


@dataclass
class PageData:
    url: str
    title: str
    meta_description: str
    h1_tags: list[str]
    h2_tags: list[str]
    h3_tags: list[str]
    word_count: int
    first_100_words: str
    images: list[dict]  # {"alt": str, "src": str}
    internal_links: list[dict]  # {"anchor": str, "href": str}
    has_schema: bool
    schema_types: list[str]
    load_time_ms: int
    mobile_friendly: bool


@dataclass
class PageScore:
    url: str
    total_score: int
    title_score: int
    meta_score: int
    h1_score: int
    hierarchy_score: int
    first_100_score: int
    content_score: int
    local_signals_score: int
    eeat_score: int
    image_score: int
    internal_link_score: int
    schema_score: int
    issues: list[str] = field(default_factory=list)
    recommendations: list[str] = field(default_factory=list)


def score_title(title: str, keyword: str, city: str, brand: str) -> tuple[int, list[str]]:
    """Score title tag (max 15 points)."""
    score = 0
    issues = []
    title_lower = title.lower()

    if keyword.lower() in title_lower:
        score += 5
    else:
        issues.append(f"Title missing primary keyword '{keyword}'")

    if city.lower() in title_lower:
        score += 3
    else:
        issues.append(f"Title missing city name '{city}'")

    if brand.lower() in title_lower:
        score += 2
    else:
        issues.append(f"Title missing business name '{brand}'")

    if len(title) <= 60:
        score += 3
    else:
        issues.append(f"Title too long ({len(title)} chars, max 60)")

    if title_lower.index(keyword.lower()) < len(title) // 2 if keyword.lower() in title_lower else False:
        score += 2
    else:
        issues.append("Primary keyword should appear near the beginning of the title")

    return min(score, 15), issues


def score_first_100_words(text: str, keyword: str, city: str,
                           neighborhoods: list[str]) -> tuple[int, list[str]]:
    """Score the first 100 words of page content (max 10 points)."""
    score = 0
    issues = []
    text_lower = text.lower()

    if keyword.lower() in text_lower:
        score += 3
    else:
        issues.append(f"First 100 words missing primary keyword '{keyword}'")

    if city.lower() in text_lower:
        score += 3
    else:
        issues.append(f"First 100 words missing city name '{city}'")

    neighborhoods_found = [n for n in neighborhoods if n.lower() in text_lower]
    if neighborhoods_found:
        score += 2
    else:
        issues.append("First 100 words should mention specific neighborhoods")

    value_prop_signals = ["experience", "licensed", "insured", "years", "trusted",
                          "affordable", "professional", "certified", "guarantee"]
    if any(signal in text_lower for signal in value_prop_signals):
        score += 2
    else:
        issues.append("First 100 words should include a value proposition or trust signal")

    return min(score, 10), issues


def score_page(page: PageData, keyword: str, city: str, brand: str,
               neighborhoods: list[str]) -> PageScore:
    """Generate a complete on-page score for a single page."""
    all_issues = []
    all_recs = []

    # Title (15 pts)
    title_score, title_issues = score_title(page.title, keyword, city, brand)
    all_issues.extend(title_issues)

    # Meta Description (10 pts)
    meta_score = 0
    if keyword.lower() in page.meta_description.lower():
        meta_score += 3
    if city.lower() in page.meta_description.lower():
        meta_score += 2
    if len(page.meta_description) <= 155:
        meta_score += 2
    if any(cta in page.meta_description.lower() for cta in ["call", "schedule", "contact", "free", "quote"]):
        meta_score += 3

    # H1 (10 pts)
    h1_score = 0
    if len(page.h1_tags) == 1:
        h1_score += 4
        h1_text = page.h1_tags[0].lower()
        if keyword.lower() in h1_text:
            h1_score += 3
        if city.lower() in h1_text:
            h1_score += 3
    elif len(page.h1_tags) == 0:
        all_issues.append("Missing H1 tag")
    else:
        all_issues.append(f"Multiple H1 tags found ({len(page.h1_tags)})")
        h1_score += 2

    # Heading Hierarchy (5 pts)
    hierarchy_score = 5 if page.h2_tags else 2

    # First 100 Words (10 pts)
    first_100_score, first_100_issues = score_first_100_words(
        page.first_100_words, keyword, city, neighborhoods
    )
    all_issues.extend(first_100_issues)

    # Content Depth (15 pts)
    content_score = 0
    if page.word_count >= 1000:
        content_score = 15
    elif page.word_count >= 500:
        content_score = 10
    elif page.word_count >= 300:
        content_score = 5
    else:
        all_issues.append(f"Thin content ({page.word_count} words, target 500+)")

    # Local Signals (10 pts) - scored based on neighborhood mentions in full content
    local_score = min(len([n for n in neighborhoods if n.lower() in page.first_100_words.lower()]) * 3, 10)

    # E-E-A-T (8 pts) - simplified check
    eeat_score = 4 if page.word_count >= 500 else 2

    # Images (7 pts)
    image_score = 0
    images_with_alt = [img for img in page.images if img.get("alt")]
    if page.images:
        alt_ratio = len(images_with_alt) / len(page.images)
        image_score = int(alt_ratio * 7)
    else:
        all_issues.append("No images on page")

    # Internal Links (5 pts)
    link_score = min(len(page.internal_links), 5)

    # Schema (5 pts)
    schema_score = 5 if page.has_schema else 0
    if not page.has_schema:
        all_issues.append("No structured data / schema markup found")

    total = (title_score + meta_score + h1_score + hierarchy_score +
             first_100_score + content_score + local_score + eeat_score +
             image_score + link_score + schema_score)

    return PageScore(
        url=page.url,
        total_score=total,
        title_score=title_score,
        meta_score=meta_score,
        h1_score=h1_score,
        hierarchy_score=hierarchy_score,
        first_100_score=first_100_score,
        content_score=content_score,
        local_signals_score=local_score,
        eeat_score=eeat_score,
        image_score=image_score,
        internal_link_score=link_score,
        schema_score=schema_score,
        issues=all_issues,
        recommendations=all_recs,
    )
```

## User Data Requests

Ask the client or account manager for:

1. **Screaming Frog crawl export** (if site has 20+ pages) - or provide site URL for DFS crawl
2. **GSC page-level performance** - last 6 months, filtered by page
3. **Target keyword-to-page mapping** from Phase 5
4. **Brand name** as it should appear in title tags
5. **Neighborhoods and service areas** for local signal assessment
6. **Team bios and credentials** for E-E-A-T evaluation
7. **Existing schema markup** - any structured data currently implemented

## Output Format

```markdown
## Phase 7: Local On-Page Audit

### On-Page Score: [XX]/100 (Aggregate)

### Page-by-Page Scores
| Page URL | Target Keyword | Title | Meta | H1 | Content | Local | E-E-A-T | Images | Links | Schema | Total |
|----------|----------------|-------|------|----|---------|-------|---------|--------|-------|--------|-------|
| /service | [keyword]      | X/15  | X/10 | X/10| X/15   | X/10  | X/8     | X/7    | X/5   | X/5    | X/100 |

### Critical Issues (Fix Immediately)
[List of issues scoring 0 on any component, affecting P1 keyword pages]

### Title Tag Recommendations
| Page | Current Title | Recommended Title | Issue |
|------|--------------|-------------------|-------|

### Meta Description Recommendations
| Page | Current Meta | Recommended Meta | Issue |
|------|-------------|------------------|-------|

### Content Gaps
[Pages with thin content (<500 words) targeting important keywords]

### Schema Implementation Plan
[List of schema types to add per page with priority]

### Internal Linking Opportunities
[Orphan pages, missing contextual links, anchor text improvements]

### Recommendations Priority
1. **Week 1:** [Title tag and meta description fixes across all pages]
2. **Week 2:** [H1 and heading hierarchy corrections]
3. **Week 3-4:** [Content depth improvements for thin pages]
4. **Month 2:** [Schema implementation, image optimization]
5. **Ongoing:** [Internal linking improvements, E-E-A-T content additions]
```

## Cross-References

- **Phase 4 (Citation Audit):** NAP on the website must match the Master NAP standard. Schema LocalBusiness markup must encode the same NAP.
- **Phase 5 (Keyword Research):** The keyword-to-page mapping from Phase 5 drives this entire audit. Every P1/P2 keyword should have a corresponding optimized page.
- **Phase 6 (Map Pack Analysis):** Pages supporting Map Pack keywords need the strongest on-page signals. Prioritize these pages in the audit.
- **Phase 8 (Landing Pages):** Low-scoring pages or missing pages identified here become content briefs in Phase 8. The on-page audit reveals what to fix; Phase 8 defines how to fix or create it.
