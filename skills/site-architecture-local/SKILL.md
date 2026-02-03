---
name: site-architecture-local
description: Site architecture design and audit for local SEO including URL structure, internal linking, silo design, and location/service page hierarchy
version: 1.0.0
tags: [local-seo, site-architecture, url-structure, internal-linking, silo, location-pages]
related: [local-landing-pages, local-on-page-audit, technical-seo-local, local-content-strategy]
---

# Phase 15: Site Architecture for Local SEO

> **Site architecture is the scaffolding that determines how effectively search engines discover, crawl, and assign topical authority to local content.** A well-structured local site makes every page findable within 2-3 clicks, distributes link equity to money pages efficiently, and creates clear topical silos that reinforce local relevance. A poorly structured site buries local landing pages, dilutes authority, and confuses crawlers about which page should rank for which query.

---

## When to Use This Skill

- **As part of the full Local SEO Audit**: Run this as Phase 15, after individual page-level audits are complete. Site architecture is the structural layer that connects individual page optimizations into a coherent whole.
- **As a standalone audit**: When a client is redesigning their website, adding new locations, or struggling with crawl depth and indexation issues for local pages.
- **Trigger scenarios**:
  - Client is launching a new website and needs architecture guidance
  - Client is expanding from single-location to multi-location
  - Local landing pages are not getting indexed or ranking
  - Cannibalization issues between location pages and service pages
  - Site redesign or migration planning
  - Client's site has orphan pages (pages with no internal links pointing to them)
  - Flat performance despite strong content --- possible architecture bottleneck

---

## Channel Impact

| Channel        | Weight | Rationale |
|----------------|--------|-----------|
| **Map Pack**   | **Indirect** | GBP links to the website; the linked page's internal linking context signals relevance to Google. A well-structured site reinforces the GBP-to-website connection. |
| **Organic**    | **High (33% On-Page)** | Site architecture is a core component of on-page SEO. Internal linking distributes PageRank, and URL structure signals topical relevance. Proper architecture directly impacts organic rankings. |
| **AI Search**  | **Medium (24% On-Page)** | AI engines crawl site structure to understand business scope. Clear architecture with structured content makes it easier for AI engines to extract and cite information. |

---

## Prerequisites

Before beginning the site architecture audit, ensure you have:

1. **Discovery Brief from Phase 1** (`/discovery-intake`)
   - Full list of services offered
   - All locations served (physical locations and/or service areas)
   - Business type (single-location, multi-location, service area business)

2. **Keyword Research from Phase 9** (`/local-keyword-research`)
   - Service keyword clusters
   - Location keyword targets
   - Long-tail keyword groupings

3. **Current Site Crawl Data** (from `/technical-seo-local`)
   - Current URL inventory
   - Crawl depth map
   - Internal link data
   - Orphan page list

4. **Content Inventory** (from `/local-content-strategy`)
   - Existing pages by type (service, location, blog, etc.)
   - Content gaps identified

---

## Assessment Framework

---

### 15.1 URL Structure Patterns for Local SEO

The URL structure must clearly communicate the relationship between services and locations. There are three primary URL patterns for local businesses, each with distinct advantages and trade-offs.

**Pattern A: Service-First Structure**

```
/services/
/services/plumbing/
/services/hvac/
/services/electrical/
/locations/
/locations/dallas/
/locations/fort-worth/
/locations/arlington/
```

| Pros | Cons |
|------|------|
| Clean separation of content types | Location pages may lack service-specific content |
| Easy to scale with new services | Requires cross-linking between service and location silos |
| Service pages build strong topical authority | Users may need extra clicks to find service + location info |

**Best for**: Single-location businesses with many services.

**Pattern B: Location-First Structure**

```
/dallas/
/dallas/plumbing/
/dallas/hvac/
/dallas/electrical/
/fort-worth/
/fort-worth/plumbing/
/fort-worth/hvac/
```

| Pros | Cons |
|------|------|
| Strong local signals in every URL | Can create massive page counts (locations x services) |
| Each page targets a specific city+service combination | Risk of thin content if not enough unique info per location |
| Clear hierarchy for multi-location businesses | Harder to maintain consistency across locations |

**Best for**: Multi-location businesses with physical presence in each city.

**Pattern C: Combined/Flat Structure**

```
/dallas-plumbing/
/dallas-hvac/
/fort-worth-plumbing/
/fort-worth-hvac/
```

| Pros | Cons |
|------|------|
| Shortest URLs, maximum keyword density in URL | No hierarchical structure for crawlers |
| Simple to implement | Difficult to scale beyond 20-30 pages |
| Each page stands alone | No parent-child relationship signals |

**Best for**: Small service area businesses with 3-5 services and 3-5 cities.

**Recommended Approach by Business Type**:

| Business Type | Recommended Pattern | URL Example |
|--------------|-------------------|-------------|
| Single-location, 5+ services | Pattern A (Service-First) | `/services/drain-cleaning/` |
| Multi-location (2-5 locations), moderate services | Pattern B (Location-First) | `/dallas/drain-cleaning/` |
| Multi-location (5+ locations) | Pattern B with hub pages | `/locations/dallas/` + `/dallas/plumbing/` |
| Service area business (no physical locations) | Pattern A or C | `/services/plumbing/` or `/dallas-plumbing/` |
| Single service, many locations | Pattern B (simplified) | `/dallas/` , `/fort-worth/` |

---

### 15.2 Location/Service URL Matrix

For businesses serving multiple locations with multiple services, the URL matrix defines which pages to create.

**Matrix Construction**:

```
==============================================================================
LOCATION/SERVICE URL MATRIX
==============================================================================

               | Service A    | Service B    | Service C    | Service D
               | (Plumbing)   | (HVAC)       | (Electrical) | (Drain Clean)
---------------|-------------|-------------|-------------|-------------
Dallas         | /dallas/     | /dallas/     | /dallas/     | /dallas/
               |  plumbing/   |  hvac/       |  electrical/ |  drain/
Fort Worth     | /ft-worth/   | /ft-worth/   | /ft-worth/   | /ft-worth/
               |  plumbing/   |  hvac/       |  electrical/ |  drain/
Arlington      | /arlington/  | /arlington/  | /arlington/  | /arlington/
               |  plumbing/   |  hvac/       |  electrical/ |  drain/
==============================================================================

Total Pages: [Locations] x [Services] = [Total]
Page Creation Priority: Primary services first, then secondary services
Minimum Content Requirement: 800+ words unique per page
==============================================================================
```

**Critical Rule**: Every page in the matrix MUST have unique, substantive content. Do NOT create location pages that are identical except for the city name swap. Google detects and penalizes this as doorway pages. Each page needs:
- Location-specific content (local landmarks, neighborhood context, area-specific challenges)
- Unique testimonials or case studies from that area
- Service-specific information relevant to that location
- Local images (not the same stock photos across all pages)

---

### 15.3 Breadcrumb Structure

Breadcrumbs serve two purposes: user navigation and search engine hierarchy signals. Proper breadcrumb implementation reinforces the site's topical structure.

**Breadcrumb Patterns by Architecture**:

**Pattern A (Service-First)**:
```
Home > Services > Plumbing
Home > Services > Plumbing > Drain Cleaning
Home > Locations > Dallas
```

**Pattern B (Location-First)**:
```
Home > Dallas > Plumbing
Home > Dallas > Plumbing > Drain Cleaning
Home > Fort Worth > HVAC > AC Repair
```

**Implementation Requirements**:
- Use BreadcrumbList schema markup on every page
- Breadcrumbs must be visible on the page (not hidden)
- Each breadcrumb level must link to a real, indexable page
- Current page should be the final breadcrumb item (not linked)
- Breadcrumb text should match the page's H1 or be a concise version

**Schema Example**:
```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {"@type": "ListItem", "position": 1, "name": "Home", "item": "https://example.com/"},
    {"@type": "ListItem", "position": 2, "name": "Dallas", "item": "https://example.com/dallas/"},
    {"@type": "ListItem", "position": 3, "name": "Plumbing", "item": "https://example.com/dallas/plumbing/"}
  ]
}
```

---

### 15.4 Internal Linking Architecture

Internal linking is the mechanism that distributes PageRank and signals topical relationships. For local SEO, the internal linking strategy must connect location pages, service pages, and supporting content in a way that reinforces both topical and geographic relevance.

**Core Internal Linking Rules**:

1. **Every page should be reachable within 2-3 clicks from the homepage**. Local landing pages buried 4+ clicks deep will underperform.
2. **Contextual links are more valuable than navigational links**. A link within body content with descriptive anchor text passes more relevance than a link in the footer or sidebar.
3. **Link related pages to each other** --- service pages should link to related services, location pages should link to nearby locations.
4. **Do NOT create exhaustive cross-links** between every page. This dilutes link equity and looks unnatural. Focus on topically relevant connections.

**Internal Linking Map for Local Businesses**:

```
                         [HOMEPAGE]
                        /    |     \
                       /     |      \
              [Service Hub]  |  [Location Hub]
              /    |    \    |    /    |    \
        [Svc A] [Svc B] [Svc C]  [Loc 1] [Loc 2] [Loc 3]
             \    |    /         /    |    \
              \   |   /    [Loc1+SvcA] [Loc1+SvcB] [Loc1+SvcC]
               [BLOG]
              /    |    \
        [Post1] [Post2] [Post3]
         (links to relevant service + location pages)
```

**Linking Strategy by Page Type**:

| From Page | Link To | Anchor Text Strategy |
|-----------|---------|---------------------|
| Homepage | Service hub, Location hub, top 3 services | Descriptive: "our plumbing services" |
| Service Page | Related services, location pages for that service, relevant blog posts | Geographic: "plumbing in Dallas" |
| Location Page | All services available in that location, nearby location pages | Service-focused: "drain cleaning service" |
| Location+Service Page | Parent location page, parent service page, related blog posts | Contextual: "learn about our process" |
| Blog Post | Relevant service page, relevant location page | Natural anchor: varies by context |

**Orphan Page Detection**:

Orphan pages (pages with zero internal links pointing to them) are invisible to crawlers and users. They represent wasted content.

**Audit Process**:
1. Crawl the site to identify all indexed pages
2. Map internal links to each page
3. Flag any pages with zero inbound internal links
4. Prioritize orphan pages that target valuable keywords
5. Add contextual internal links from related pages

---

### 15.5 Silo Structure for Local SEO

Silo structure groups related content into topical clusters, reinforcing authority for each topic. For local businesses, silos should be organized by service type or location.

**Service Silo Example** (single-location):

```
PLUMBING SILO:
  /services/plumbing/                    (Hub page)
  /services/plumbing/drain-cleaning/     (Sub-service)
  /services/plumbing/water-heater/       (Sub-service)
  /services/plumbing/sewer-line/         (Sub-service)
  /blog/how-to-unclog-a-drain/           (Supporting content)
  /blog/water-heater-maintenance-tips/   (Supporting content)

HVAC SILO:
  /services/hvac/                        (Hub page)
  /services/hvac/ac-repair/              (Sub-service)
  /services/hvac/heating/                (Sub-service)
  /services/hvac/duct-cleaning/          (Sub-service)
  /blog/when-to-replace-your-ac/         (Supporting content)
```

**Location Silo Example** (multi-location):

```
DALLAS SILO:
  /dallas/                               (Location hub)
  /dallas/plumbing/                      (Service in location)
  /dallas/hvac/                          (Service in location)
  /blog/dallas-plumbing-code-updates/    (Location-specific content)

FORT WORTH SILO:
  /fort-worth/                           (Location hub)
  /fort-worth/plumbing/                  (Service in location)
  /fort-worth/hvac/                      (Service in location)
  /blog/fort-worth-home-maintenance/     (Location-specific content)
```

**Silo Rules**:
- Pages within a silo should link to each other freely
- Cross-silo links should be limited and intentional (hub-to-hub only)
- Blog posts should be assigned to a silo based on topic and linked accordingly
- The hub page of each silo should receive the most internal links

---

### 15.6 Navigation Design for Local Businesses

The main navigation menu must balance service visibility with location accessibility.

**Recommended Navigation Structures**:

**Single-Location Business**:
```
[Home] [Services v] [About] [Reviews] [Blog] [Contact]
         |
         +-- Plumbing
         +-- HVAC
         +-- Electrical
         +-- Drain Cleaning
```

**Multi-Location Business**:
```
[Home] [Services v] [Locations v] [About] [Reviews] [Blog] [Contact]
         |              |
         +-- Plumbing   +-- Dallas
         +-- HVAC       +-- Fort Worth
         +-- Electrical +-- Arlington
```

**Service Area Business**:
```
[Home] [Services v] [Service Areas v] [About] [Reviews] [Blog] [Contact]
         |                |
         +-- Plumbing     +-- Dallas
         +-- HVAC         +-- Fort Worth
         +-- Electrical   +-- Arlington
```

**Navigation Best Practices**:
- Keep main nav to 6-8 items maximum
- Use mega menus for businesses with many services or locations (but keep them clean)
- Include a "sticky" phone number or CTA button in the header
- Mobile navigation should mirror desktop structure
- Footer should include a complete sitemap-style link list for crawl access

---

### 15.7 URL Canonicalization for Location Pages

Location pages are prone to canonicalization issues, especially when similar content exists across multiple URLs.

**Common Issues**:

| Issue | Example | Solution |
|-------|---------|----------|
| Trailing slash inconsistency | `/dallas/` vs `/dallas` | Pick one format, redirect the other, set canonical |
| WWW vs non-WWW | `www.site.com/dallas/` vs `site.com/dallas/` | 301 redirect to preferred version |
| HTTP vs HTTPS | `http://site.com/dallas/` vs `https://site.com/dallas/` | 301 redirect HTTP to HTTPS |
| Duplicate location pages | `/locations/dallas/` and `/dallas/` | Consolidate to one URL, 301 the other |
| Parameter URLs | `/services/?location=dallas` | Canonical to clean URL, or 301 redirect |
| Pagination | `/blog/page/2/` | rel="canonical" to page 1, or self-referencing canonical |

**Audit Checklist**:
1. Check for duplicate content across location page variants
2. Verify canonical tags on all location pages (self-referencing canonicals recommended)
3. Check for redirect chains (A -> B -> C should be A -> C)
4. Verify only one version of each URL is indexed (check Google Search Console)
5. Test parameter handling (do parameter URLs create duplicate pages?)

---

### 15.8 Sitemap Structure

Local businesses benefit from organized XML sitemaps that group pages by type.

**Recommended Sitemap Organization**:

```
/sitemap.xml (sitemap index)
  |
  +-- /sitemap-pages.xml        (Core pages: home, about, contact)
  +-- /sitemap-services.xml     (All service pages)
  +-- /sitemap-locations.xml    (All location/city pages)
  +-- /sitemap-blog.xml         (Blog posts)
  +-- /sitemap-images.xml       (Image sitemap, optional)
```

**Benefits of Separate Sitemaps**:
- Easier to monitor indexation by page type in Google Search Console
- Faster identification of indexation issues (e.g., location pages not being indexed)
- Cleaner crawl priority signaling
- Easier to manage for large multi-location sites

---

## Architecture Diagram Templates

### Template 1: Single-Location Service Business

```
==============================================================================
SITE ARCHITECTURE: SINGLE-LOCATION SERVICE BUSINESS
==============================================================================

                            [HOMEPAGE]
                     /     /    |    \     \
                    /     /     |     \     \
            [About] [Services] [Reviews] [Blog] [Contact]
                     /  |  \              /  |  \
                    /   |   \            /   |   \
              [Svc A] [Svc B] [Svc C] [Post] [Post] [Post]
               /  \                      |
              /    \                     |
        [Sub-Svc] [Sub-Svc]      (links to service pages)

URL STRUCTURE:
  /                          Homepage
  /services/                 Services hub
  /services/plumbing/        Service page
  /services/plumbing/drain/  Sub-service page
  /about/                    About page
  /reviews/                  Reviews/testimonials
  /blog/                     Blog index
  /blog/post-title/          Blog post
  /contact/                  Contact page

CLICK DEPTH: All pages reachable in 2-3 clicks
TOTAL PAGES: 15-30 typical
==============================================================================
```

### Template 2: Multi-Location Service Business

```
==============================================================================
SITE ARCHITECTURE: MULTI-LOCATION SERVICE BUSINESS
==============================================================================

                              [HOMEPAGE]
                    /       /     |     \       \
                   /       /      |      \       \
           [About] [Services] [Locations] [Blog] [Contact]
                   /  |  \    /   |   \
                  /   |   \  /    |    \
           [Svc A] [Svc B] [Loc 1] [Loc 2] [Loc 3]
                            / | \
                           /  |  \
                   [Loc1   [Loc1   [Loc1
                    SvcA]   SvcB]   SvcC]

URL STRUCTURE:
  /                              Homepage
  /services/                     Services hub
  /services/plumbing/            Service page (general)
  /locations/                    Locations hub
  /locations/dallas/             Location page (city hub)
  /locations/dallas/plumbing/    Location + service page
  /blog/                         Blog index
  /contact/                      Contact page

CLICK DEPTH: Location+Service pages at 3 clicks max
TOTAL PAGES: 30-100+ depending on locations x services
CRITICAL: Each location+service page needs unique content
==============================================================================
```

### Template 3: Service Area Business (No Physical Locations)

```
==============================================================================
SITE ARCHITECTURE: SERVICE AREA BUSINESS
==============================================================================

                            [HOMEPAGE]
                     /     /    |    \     \
                    /     /     |     \     \
            [About] [Services] [Areas] [Blog] [Contact]
                     /  |  \   / | \
                    /   |   \ /  |  \
              [Svc A] [Svc B] [City1] [City2] [City3]
                                |
                          [City1+SvcA]
                          (only for top
                           service+city combos)

URL STRUCTURE:
  /                              Homepage
  /services/                     Services hub
  /services/plumbing/            Service page
  /service-areas/                Service areas hub
  /service-areas/dallas/         City page
  /dallas-plumbing/              City+service (flat, for top combos only)
  /blog/                         Blog index

CLICK DEPTH: All pages within 2-3 clicks
TOTAL PAGES: 20-50 typical
NOTE: Do NOT create city+service pages for every combination.
      Only create them for high-volume, high-priority targets.
==============================================================================
```

---

## Scoring Rubric

```
==============================================================================
            SITE ARCHITECTURE SCORE
==============================================================================

Element                               | Max   | Score
--------------------------------------|-------|------
URL Structure (logical, consistent)   | /15   |  ___
Crawl Depth (pages within 2-3 clicks) | /15   |  ___
Internal Linking (contextual, strategic)| /20  |  ___
Orphan Pages (none found)             | /10   |  ___
Breadcrumb Implementation             | /10   |  ___
Navigation Design (clear hierarchy)   | /10   |  ___
Canonicalization (no duplicates)       | /10   |  ___
Sitemap Structure (organized by type) | /10   |  ___
                                      |-------|------
TOTAL ARCHITECTURE SCORE              | /100  |  ___

==============================================================================
SCORE INTERPRETATION:
  85-100: Excellent architecture --- well-structured, crawlable, scalable
  70-84:  Good --- minor structural improvements needed
  50-69:  Needs Work --- significant gaps in linking, depth, or organization
  30-49:  Poor --- restructuring required for local SEO effectiveness
  0-29:   Critical --- fundamental architecture issues blocking performance
==============================================================================
```

---

## DFS MCP Data Sources

| Tool | Purpose |
|------|---------|
| `mcp__dfs-mcp__serp_organic_live_advanced` | Check which pages rank for target keywords to identify cannibalization |
| `mcp__dfs-mcp__dataforseo_labs_google_ranked_keywords` | Identify all ranked pages to map against architecture |

**Note**: Site architecture auditing primarily relies on crawl data rather than DFS API data. Use Screaming Frog, Sitebulb, or similar crawlers for internal link mapping and orphan page detection. DFS tools supplement by verifying which pages are actually ranking.

---

## Output Format

```
==============================================================================
PHASE 15: SITE ARCHITECTURE FOR LOCAL SEO
==============================================================================

Business: [Business Name]
Website: [URL]
Business Type: [Single-location / Multi-location / SAB]
Audit Date: [YYYY-MM-DD]
Auditor: Claude Code (Local SEO Auditor)

------------------------------------------------------------------------------
ARCHITECTURE SCORE: [XX]/100
------------------------------------------------------------------------------

CURRENT STATE:
  URL Pattern: [Describe current structure]
  Total Indexed Pages: [X]
  Max Crawl Depth: [X clicks]
  Orphan Pages Found: [X]
  Canonicalization Issues: [X]

RECOMMENDED ARCHITECTURE:
  [Insert appropriate architecture diagram template]

RECOMMENDED URL STRUCTURE:
  [Insert URL pattern recommendation with examples]

LOCATION/SERVICE MATRIX:
  [Insert completed matrix if multi-location/multi-service]

------------------------------------------------------------------------------
PRIORITY ACTIONS
------------------------------------------------------------------------------

CRITICAL (Blocks Performance):
  1. [e.g., Fix 12 orphan location pages --- add internal links]
  2. [e.g., Reduce crawl depth from 5 to 3 for service pages]

HIGH (Significant Impact):
  3. [e.g., Implement breadcrumb schema on all pages]
  4. [e.g., Restructure navigation to expose location pages]

MEDIUM (Optimization):
  5. [e.g., Create separate XML sitemaps by page type]
  6. [e.g., Add contextual cross-links between related services]

==============================================================================
```

---

## Cross-References

| Skill | Relationship | When to Use Together |
|-------|-------------|----------------------|
| `/local-landing-pages` | **Dependent** --- Landing page design must align with the architecture. The architecture defines where each landing page lives in the hierarchy; the landing page skill defines what goes on each page. | Architecture defines structure; landing pages define content and layout for each node. |
| `/local-on-page-audit` | **Complementary** --- On-page audit assesses individual page quality. Architecture audit assesses how pages relate to each other and how authority flows between them. | Both are needed for a complete organic optimization picture. |
| `/technical-seo-local` | **Input** --- Technical audit provides crawl data (depth, internal links, orphan pages) that feeds directly into the architecture assessment. | Technical audit generates the data; architecture audit interprets and recommends structural changes. |
| `/local-content-strategy` | **Complementary** --- Content strategy defines what content to create. Architecture defines where that content lives and how it connects to the rest of the site. | Content strategy without architecture guidance risks creating orphan content. |
| `/local-keyword-research` | **Input** --- Keyword clusters inform the service silo structure and location/service URL matrix. Each silo should map to a keyword cluster. | Keyword research defines the topics; architecture organizes them into a crawlable, authoritative structure. |

---

*Site architecture is the structural foundation that supports all other local SEO efforts. For the complete audit workflow, this phase follows Phase 14 (AI Search Visibility) and precedes the final Phase 16 (Reporting and KPIs). Architecture recommendations should be implemented early in any SEO engagement because they affect the effectiveness of all subsequent content and optimization work.*
