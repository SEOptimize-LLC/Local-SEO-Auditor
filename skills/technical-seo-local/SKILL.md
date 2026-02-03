---
name: technical-seo-local
description: Technical SEO audit through a local search impact lens — crawlability, indexation, mobile, speed, HTTPS, redirects, and rendering assessed by their effect on local rankings
version: 1.0.0
tags: [local-seo, technical-seo, crawlability, indexation, mobile, core-web-vitals, page-speed, audit]
related: [local-on-page-audit, local-schema-markup, local-landing-pages, site-architecture-local, local-seo-audit]
---

# Phase 9: Technical SEO for Local

> **Every technical SEO finding in this skill is framed by its impact on local rankings.** A broken canonical tag on a blog post is a minor issue. A broken canonical tag on a location page is a CRITICAL issue that removes a money page from Google's index. This skill does not audit technical SEO generically — it audits technical SEO as a local ranking factor across all three search channels.

---

## When to Use This Skill

- **As part of the full Local SEO Audit**: Run as Phase 9, after on-page (Phase 5) and site architecture (Phase 8) audits are complete. Those phases identify the pages that matter most; this phase ensures those pages are technically accessible to search engines.
- **As a standalone audit**: When a client reports sudden local ranking drops with no obvious cause — technical issues are often the hidden culprit.
- **Trigger scenarios**:
  - Local landing pages or service pages are not appearing in Google search results
  - Site migration (domain change, CMS change, HTTP to HTTPS) has caused local ranking drops
  - Core Web Vitals scores are failing and local competitors are outranking on mobile
  - New location pages were launched but are not being indexed
  - Client switched to a JavaScript framework (React, Next.js, Angular) and local pages lost rankings
  - Google Search Console is reporting crawl errors on local pages
  - Mobile usability issues flagged in GSC for pages that target local keywords

---

## Channel Impact

Technical SEO is a foundation layer — it does not directly carry weight in ranking models, but failures in technical SEO can completely block the signals that DO carry weight.

| Channel        | Weight  | Rationale |
|----------------|---------|-----------|
| **Map Pack**   | **Indirect** | GBP links to the website. If the linked page is slow, broken, or unindexable, it weakens the GBP-to-website trust bridge. Google uses the linked page to verify business data. A broken page = broken verification. |
| **Organic**    | **Critical Foundation** | On-Page (33%) and Links (24%) are the top organic factors, but NEITHER works if pages are not crawled, indexed, and rendered. Technical failures here are binary — the page either ranks or it does not exist. |
| **AI Search**  | **On-Page 24%** | AI engines crawl and parse web pages to generate answers. JavaScript rendering issues, slow pages, and blocked crawlers prevent AI engines from accessing local content entirely. |

**Bottom line**: Technical SEO is a multiplier. A score of 0 in technical SEO makes every other optimization worthless for that page. A score of 100 does not directly boost rankings but ensures all other signals can be received.

---

## Prerequisites

Before beginning the technical SEO audit, ensure you have:

1. **Discovery Brief from Phase 1** (`/discovery-intake`)
   - Target domain and any subdomains
   - List of location/service pages (from Phase 5 or 8)
   - CMS and hosting platform information

2. **Priority Page List**
   - Homepage
   - All location pages (e.g., `/locations/dallas/`, `/service-area/fort-worth/`)
   - Top service pages (e.g., `/services/emergency-plumbing/`)
   - GBP-linked landing page(s)
   - Contact page
   - These are the "money pages" — technical issues on these pages are CRITICAL

3. **Access or Exports**
   - Google Search Console access (Coverage report, Core Web Vitals report)
   - Screaming Frog crawl export (if available — for full-site or subfolder audits)
   - robots.txt URL
   - XML sitemap URL(s)

4. **DFS MCP Tools Ready**
   - `mcp__dfs-mcp__on_page_instant_pages` — for page-level technical analysis
   - `mcp__dfs-mcp__on_page_lighthouse` — for Core Web Vitals and performance scoring

---

## Assessment Framework

The technical SEO audit is organized into seven assessment areas, each scored by local impact severity.

### Priority Classification

| Priority | Definition | Local Impact |
|----------|-----------|--------------|
| **CRITICAL** | Issue blocks indexation or rendering of a local money page | Page is invisible in search — zero local visibility |
| **HIGH** | Issue degrades performance or creates confusion for crawlers on local pages | Reduced rankings, poor user experience on mobile (60%+ of local searches) |
| **MEDIUM** | Issue affects site health but not directly a local money page | Indirect impact through crawl budget waste or site-wide trust signals |
| **LOW** | Best practice deviation with minimal local ranking impact | Cleanup item for overall site hygiene |

---

### 9.1 Crawlability (20 points)

**Why This Matters for Local**: If Googlebot cannot reach your location pages, service pages, or contact page, those pages do not exist in Google's index. Crawl issues on local money pages are the #1 hidden cause of "we don't rank at all" scenarios.

#### 9.1.1 robots.txt Analysis (8 points)

**Audit Steps**:
1. Fetch and review the robots.txt file at `[domain]/robots.txt`
2. Check for rules that block crawling of local money pages:
   - `Disallow: /locations/` — CRITICAL: blocks ALL location pages
   - `Disallow: /services/` — CRITICAL: blocks ALL service pages
   - `Disallow: /*?` — HIGH: blocks parameter URLs that may include location filters
   - `Disallow: /wp-admin/` — LOW: standard WordPress block, acceptable
3. Check for `Crawl-delay` directives — these slow Googlebot's crawl rate and can delay indexation of new pages
4. Verify `Sitemap:` directive points to the correct XML sitemap URL
5. Check for user-agent-specific rules (some sites block specific bots like `AdsBot-Google` or AI crawlers like `GPTBot` and `ClaudeBot`)

**CRITICAL Local Check**: Search for any rule that could match location or service page URLs. A single misplaced wildcard can block hundreds of local pages.

**Python: robots.txt Parser for Local Page Blocking**:
```python
import urllib.robotparser
import re
from typing import List, Dict

def audit_robots_txt(domain: str, local_pages: List[str]) -> Dict:
    """
    Parse robots.txt and check if any local money pages are blocked.

    Args:
        domain: The target domain (e.g., "https://example.com")
        local_pages: List of local page paths (e.g., ["/locations/dallas/", "/services/plumbing/"])

    Returns:
        dict: Audit results with blocked pages and recommendations
    """
    robots_url = f"{domain}/robots.txt"
    rp = urllib.robotparser.RobotFileParser()
    rp.set_url(robots_url)
    rp.read()

    results = {
        "robots_url": robots_url,
        "blocked_pages": [],
        "allowed_pages": [],
        "crawl_delay": rp.crawl_delay("Googlebot"),
        "sitemaps": rp.site_maps() or [],
        "severity": "PASS"
    }

    for page in local_pages:
        full_url = f"{domain}{page}"
        if not rp.can_fetch("Googlebot", full_url):
            results["blocked_pages"].append({
                "url": full_url,
                "severity": "CRITICAL",
                "reason": "Blocked by robots.txt — this local money page is invisible to Google"
            })
        else:
            results["allowed_pages"].append(full_url)

    # Check AI bot blocking
    ai_bots = ["GPTBot", "ClaudeBot", "PerplexityBot", "Bytespider"]
    results["ai_bot_blocking"] = {}
    for bot in ai_bots:
        blocked_count = sum(1 for page in local_pages if not rp.can_fetch(bot, f"{domain}{page}"))
        results["ai_bot_blocking"][bot] = {
            "blocked_pages": blocked_count,
            "total_pages": len(local_pages)
        }

    if results["blocked_pages"]:
        results["severity"] = "CRITICAL"
    elif results["crawl_delay"] and results["crawl_delay"] > 5:
        results["severity"] = "HIGH"

    return results

# Example usage:
# result = audit_robots_txt("https://abcplumbing.com", [
#     "/locations/dallas/", "/locations/fort-worth/",
#     "/services/emergency-plumbing/", "/services/drain-cleaning/",
#     "/contact/"
# ])
```

**Scoring**:
- 0 points: robots.txt blocks one or more local money pages from Googlebot
- 4 points: No local pages blocked but Crawl-delay is set above 5 seconds, or sitemap directive missing
- 8 points: All local pages crawlable, no excessive crawl-delay, sitemap directive present

#### 9.1.2 XML Sitemap (6 points)

**Audit Steps**:
1. Locate the XML sitemap (check robots.txt, `/sitemap.xml`, `/sitemap_index.xml`)
2. Verify ALL location pages are included in the sitemap
3. Verify ALL service pages are included in the sitemap
4. Check `<lastmod>` dates — stale dates signal abandoned content
5. Check for sitemap errors in Google Search Console
6. Verify sitemap is not oversized (50,000 URLs or 50MB limit per file)
7. For multi-location businesses: check if location pages have their own sitemap segment

**Scoring**:
- 0 points: No sitemap exists, or local money pages are missing from sitemap
- 3 points: Sitemap exists with local pages but has errors or stale `<lastmod>` dates
- 6 points: Clean sitemap with all local pages, accurate `<lastmod>`, no errors

#### 9.1.3 Site Structure Depth (6 points)

**Audit Steps**:
1. Check the click depth of location and service pages from the homepage
2. Local money pages should be reachable within 2-3 clicks from the homepage
3. Location pages buried 4+ clicks deep receive less crawl priority and link equity

**Scoring**:
- 0 points: Local money pages are 5+ clicks deep or orphaned (no internal links)
- 3 points: Local pages are 3-4 clicks deep
- 6 points: Local pages are 1-2 clicks from homepage with clear navigation paths

---

### 9.2 Indexation (25 points)

**Why This Matters for Local**: Indexation issues on location and service pages are the most CRITICAL technical SEO problems for local businesses. A noindexed location page is a money page that generates zero search traffic.

#### 9.2.1 noindex Tags on Local Pages (12 points)

**CRITICAL CHECK**: Scan all location pages, service pages, and the contact page for `<meta name="robots" content="noindex">` or `X-Robots-Tag: noindex` headers.

**Common Causes**:
- CMS "Discourage search engines" setting left on after development/staging
- SEO plugin (Yoast, RankMath) accidentally set to noindex on page templates
- noindex applied to a parent template that cascades to all location pages
- Staging site settings migrated to production

**Audit Steps**:
1. Check HTTP headers and HTML meta tags for every local money page
2. Cross-reference with Google Search Console Coverage report — look for "Excluded by 'noindex' tag"
3. Search Google for `site:domain.com/locations/` to verify indexed pages
4. Compare indexed pages against known location pages — any gaps indicate indexation issues

**Scoring**:
- 0 points: ANY local money page has a noindex tag (CRITICAL — fix immediately)
- 6 points: All local pages are indexable but some secondary pages have noindex issues
- 12 points: All local and service pages are properly indexable

#### 9.2.2 Canonical Tag Issues (8 points)

**Why This Matters for Local**: Canonical conflicts between location pages are common in multi-location businesses. If `/locations/dallas/` has a canonical pointing to `/locations/`, Google ignores the Dallas page entirely.

**Audit Steps**:
1. Check every location page's `<link rel="canonical">` tag
2. Verify each page's canonical points to ITSELF (self-referencing)
3. Check for cross-location canonicals (Dallas page canonical pointing to Houston page)
4. Check for parameter-based canonical issues (`/locations/dallas/?ref=gbp` canonical to `/locations/dallas/`)
5. Look for missing canonical tags (allows Google to choose, which may not be what you want)

**Scoring**:
- 0 points: Canonical conflicts exist on local money pages
- 4 points: Canonicals are present but inconsistent (some self-referencing, some not)
- 8 points: All local pages have correct self-referencing canonical tags

#### 9.2.3 Index Bloat (5 points)

**Audit Steps**:
1. Check for thin or duplicate location pages (e.g., auto-generated pages for every zip code with identical content)
2. Look for parameter URLs being indexed (`?sort=`, `?page=`, `?ref=`)
3. Check for tag/category archive pages that create near-duplicate local content
4. Verify total indexed pages (via `site:domain.com`) is reasonable for the business size

**Scoring**:
- 0 points: Significant index bloat from thin/duplicate local pages
- 2 points: Minor bloat issues with parameter or archive pages
- 5 points: Clean index with only substantive pages indexed

---

### 9.3 Mobile Optimization (20 points)

**Why This Matters for Local**: Over 60% of local searches happen on mobile devices. Google uses mobile-first indexing, meaning the mobile version of your page is what Google evaluates for ranking. A page that looks great on desktop but breaks on mobile will rank poorly in local search.

#### 9.3.1 Mobile-First Assessment (10 points)

**Audit Steps**:
1. Test all local money pages on mobile viewport (375px width)
2. Check for horizontal scrolling (content wider than viewport)
3. Verify tap targets are at least 48x48px with adequate spacing
4. Check font sizes — body text should be minimum 16px on mobile
5. Verify viewport meta tag is set correctly: `<meta name="viewport" content="width=device-width, initial-scale=1">`
6. Check for intrusive interstitials (popups that block content on mobile — Google penalizes these)
7. Test click-to-call functionality — phone numbers must be tappable on mobile
8. Verify maps and directions links work on mobile (open in Maps app)

**Local-Specific Mobile Checks**:
- NAP information must be visible without scrolling on mobile
- Click-to-call button should be prominent above the fold
- Google Maps embed must be responsive (not fixed-width)
- Service area/location selector must work on touch devices
- Form fields (contact form, quote request) must be usable on mobile keyboards

**Scoring**:
- 0 points: Page is not mobile-friendly (not responsive, broken layout, no viewport tag)
- 5 points: Page is responsive but has usability issues (small tap targets, tiny fonts, hidden NAP)
- 10 points: Full mobile optimization with click-to-call, responsive maps, accessible NAP, proper tap targets

#### 9.3.2 Mobile Page Speed (10 points)

**Audit Steps**:
1. Run Lighthouse mobile audit on each local money page
2. Record Core Web Vitals:
   - **LCP (Largest Contentful Paint)**: Target < 2.5 seconds
   - **INP (Interaction to Next Paint)**: Target < 200 milliseconds
   - **CLS (Cumulative Layout Shift)**: Target < 0.1
3. Check mobile Performance score (target: 70+)
4. Identify largest performance bottlenecks for each page

**Scoring**:
- 0 points: Mobile Lighthouse Performance score below 40 OR any CWV metric in "Poor" range
- 5 points: Performance score 40-69 OR one CWV metric in "Needs Improvement" range
- 10 points: Performance score 70+ with all CWV metrics in "Good" range

---

### 9.4 Page Speed & Core Web Vitals (15 points)

**Why This Matters for Local**: Page speed is a confirmed Google ranking factor, and Core Web Vitals are part of the Page Experience signal. For local businesses, slow pages on mobile directly cost conversions — a user searching "emergency plumber near me" will not wait 8 seconds for a page to load.

#### 9.4.1 Core Web Vitals Assessment (10 points)

Test the following pages (prioritized by local importance):
1. Homepage
2. GBP-linked landing page
3. Top 3 location pages
4. Top 3 service pages
5. Contact page

**Thresholds**:
| Metric | Good | Needs Improvement | Poor |
|--------|------|-------------------|------|
| LCP | < 2.5s | 2.5s - 4.0s | > 4.0s |
| INP | < 200ms | 200ms - 500ms | > 500ms |
| CLS | < 0.1 | 0.1 - 0.25 | > 0.25 |

**Common Local Site Speed Killers**:
- Unoptimized Google Maps embed (loads entire Maps API — use lazy loading)
- Large hero images without responsive srcset
- Uncompressed before/after project photos
- Chat widgets loading synchronously
- Multiple tracking scripts (CallRail, Google Analytics, Facebook Pixel, etc.)
- Render-blocking CSS/JS from page builder plugins (Elementor, Divi, WPBakery)

**Scoring**:
- 0 points: Majority of local pages have "Poor" CWV scores
- 5 points: Mixed results — some pages pass, some fail
- 10 points: All local money pages pass CWV thresholds

#### 9.4.2 Speed Optimization Opportunities (5 points)

**Audit Steps**:
1. Identify image optimization opportunities (WebP/AVIF conversion, lazy loading)
2. Check for render-blocking resources
3. Evaluate third-party script impact
4. Check server response time (TTFB < 800ms)
5. Assess caching configuration (browser caching, CDN)

**Scoring**:
- 0 points: Multiple major speed optimization opportunities unaddressed
- 2 points: Some optimizations in place but significant gaps remain
- 5 points: Strong optimization with minimal remaining opportunities

---

### 9.5 HTTPS & Security (10 points)

#### 9.5.1 SSL Certificate (5 points)

**Audit Steps**:
1. Verify SSL certificate is valid and not expired
2. Check certificate covers all subdomains used (www and non-www)
3. Verify HTTP automatically redirects to HTTPS (301 redirect)
4. Check for mixed content warnings (HTTPS page loading HTTP resources)
5. Verify the GBP-linked URL uses HTTPS

**Scoring**:
- 0 points: No SSL, expired certificate, or GBP links to HTTP URL
- 2 points: SSL valid but mixed content warnings or redirect issues
- 5 points: Full HTTPS with proper redirects, no mixed content

#### 9.5.2 Security Headers (5 points)

**Audit Steps**:
1. Check for HSTS header (Strict-Transport-Security)
2. Verify Content-Security-Policy is set
3. Check X-Frame-Options (prevents clickjacking)
4. Verify X-Content-Type-Options is set

**Scoring**:
- 0 points: No security headers set
- 2 points: Some security headers present
- 5 points: All recommended security headers properly configured

---

### 9.6 Redirects (5 points)

**Why This Matters for Local**: Redirect chains on location pages dilute link equity and slow page load. A 302 (temporary) redirect on a location page tells Google the page is temporary — which can prevent it from ranking.

**Python: Redirect Chain Detector**:
```python
import requests
from typing import List, Dict

def detect_redirect_chains(urls: List[str], max_redirects: int = 10) -> List[Dict]:
    """
    Detect redirect chains for a list of URLs. Flags chains longer than 1 hop
    and identifies 302 redirects that should be 301s.

    Args:
        urls: List of URLs to check (local money pages)
        max_redirects: Maximum redirects to follow before flagging as loop

    Returns:
        list: Redirect chain analysis for each URL
    """
    results = []

    for url in urls:
        chain = []
        current_url = url
        seen = set()

        try:
            for i in range(max_redirects):
                if current_url in seen:
                    chain.append({"url": current_url, "status": "LOOP DETECTED", "severity": "CRITICAL"})
                    break
                seen.add(current_url)

                response = requests.head(current_url, allow_redirects=False, timeout=10)
                status = response.status_code

                if status in (301, 302, 303, 307, 308):
                    redirect_type = "permanent" if status in (301, 308) else "temporary"
                    next_url = response.headers.get("Location", "")
                    chain.append({
                        "url": current_url,
                        "status": status,
                        "redirect_type": redirect_type,
                        "redirects_to": next_url,
                        "severity": "HIGH" if redirect_type == "temporary" else "LOW"
                    })
                    current_url = next_url
                else:
                    chain.append({"url": current_url, "status": status, "final": True})
                    break

            chain_length = len(chain) - 1  # subtract final destination
            results.append({
                "original_url": url,
                "chain_length": chain_length,
                "chain": chain,
                "severity": "CRITICAL" if chain_length > 3 else "HIGH" if chain_length > 1 else "PASS",
                "has_302": any(hop.get("redirect_type") == "temporary" for hop in chain)
            })
        except requests.RequestException as e:
            results.append({
                "original_url": url,
                "error": str(e),
                "severity": "HIGH"
            })

    return results

# Example usage:
# chains = detect_redirect_chains([
#     "http://example.com/locations/dallas/",
#     "https://www.example.com/services/plumbing",
#     "https://example.com/contact"
# ])
# for chain in chains:
#     if chain["chain_length"] > 0:
#         print(f"REDIRECT CHAIN ({chain['chain_length']} hops): {chain['original_url']}")
```

**Audit Steps**:
1. Check all local money pages for redirect chains (more than 1 redirect hop)
2. Identify 302 redirects that should be 301s on permanent pages
3. Check HTTP-to-HTTPS redirect is a single 301 (not a chain through www)
4. Verify old location page URLs redirect to new ones (if site was restructured)
5. Check for redirect loops

**Scoring**:
- 0 points: Redirect loops or chains longer than 3 hops on local pages, or 302 on permanent local pages
- 2 points: Minor redirect chains (2 hops) or a few unnecessary 302s
- 5 points: Clean redirects — single-hop 301s where needed, no chains or loops

---

### 9.7 Rendering & JavaScript (5 points)

**Why This Matters for Local**: Single-page application (SPA) frameworks like React, Angular, and Vue.js can hide content from Googlebot if server-side rendering (SSR) is not implemented. If your location page content is rendered entirely via client-side JavaScript, Google may see a blank page — and a blank page cannot rank.

**Audit Steps**:
1. View source (not inspect element) on each local money page — is the content in the HTML, or is it loaded by JavaScript?
2. Use Google's URL Inspection Tool (in GSC) to see how Google renders the page
3. Check for critical content (NAP, services, reviews) that requires JavaScript to display
4. Test with JavaScript disabled — can Google still see the essential local content?
5. For React/Next.js/Nuxt sites: verify SSR or static generation is working for local pages

**Red Flags**:
- Location page HTML source shows only `<div id="root"></div>` with no content
- NAP information loaded via API call after page render
- Service descriptions rendered by JavaScript widget
- Reviews pulled from third-party widget without server-side pre-rendering

**Scoring**:
- 0 points: Local money page content is entirely client-side rendered with no SSR fallback
- 2 points: Most content is in HTML but some local elements (reviews, maps) require JS
- 5 points: All critical local content is in the initial HTML response (SSR, static, or traditional server-rendered)

---

## Scoring Rubric

```
==============================================================
        TECHNICAL SEO (LOCAL) HEALTH SCORE CALCULATION
==============================================================

CRAWLABILITY (20 points max)
--------------------------------------------------------------
  robots.txt (local pages):     ___/ 8  (0 = blocking, 4 = issues, 8 = clean)
  XML Sitemap:                  ___/ 6  (0 = missing/incomplete, 3 = issues, 6 = clean)
  Site Structure Depth:         ___/ 6  (0 = buried, 3 = deep, 6 = shallow)
                                ------
  CRAWLABILITY SUBTOTAL:        ___/20


INDEXATION (25 points max)
--------------------------------------------------------------
  noindex on Local Pages:       ___/12  (0 = CRITICAL block, 6 = partial, 12 = clean)
  Canonical Tags:               ___/ 8  (0 = conflicts, 4 = inconsistent, 8 = correct)
  Index Bloat:                  ___/ 5  (0 = significant, 2 = minor, 5 = clean)
                                ------
  INDEXATION SUBTOTAL:          ___/25


MOBILE OPTIMIZATION (20 points max)
--------------------------------------------------------------
  Mobile-First Assessment:      ___/10  (0 = broken, 5 = issues, 10 = optimized)
  Mobile Page Speed:            ___/10  (0 = poor CWV, 5 = mixed, 10 = all good)
                                ------
  MOBILE SUBTOTAL:              ___/20


PAGE SPEED & CWV (15 points max)
--------------------------------------------------------------
  Core Web Vitals:              ___/10  (0 = poor, 5 = mixed, 10 = all pass)
  Speed Optimization:           ___/ 5  (0 = unoptimized, 2 = partial, 5 = optimized)
                                ------
  PAGE SPEED SUBTOTAL:          ___/15


HTTPS & SECURITY (10 points max)
--------------------------------------------------------------
  SSL Certificate:              ___/ 5  (0 = missing/expired, 2 = issues, 5 = clean)
  Security Headers:             ___/ 5  (0 = none, 2 = partial, 5 = complete)
                                ------
  HTTPS SUBTOTAL:               ___/10


REDIRECTS (5 points max)
--------------------------------------------------------------
  Redirect Health:              ___/ 5  (0 = chains/loops, 2 = minor, 5 = clean)
                                ------
  REDIRECTS SUBTOTAL:           ___/ 5


RENDERING (5 points max)
--------------------------------------------------------------
  JS Rendering:                 ___/ 5  (0 = CSR only, 2 = partial SSR, 5 = full SSR)
                                ------
  RENDERING SUBTOTAL:           ___/ 5


==============================================================
  TECHNICAL SEO (LOCAL) SCORE:  ___/100
==============================================================

SCORE INTERPRETATION:
  90-100:  Excellent — Technical foundation is solid, no local pages at risk
  75-89:   Good — Minor issues, no critical blockers for local pages
  50-74:   Needs Work — Some local pages may have indexation or speed issues
  25-49:   Poor — Critical technical issues are blocking local page visibility
  0-24:    Critical — Fundamental technical failures, local pages likely invisible
==============================================================
```

---

## DFS MCP Data Sources

### Tool 1: Page-Level Technical Analysis

```
TOOL: mcp__dfs-mcp__on_page_instant_pages
USE:  Analyze individual local money pages for technical issues including
      meta tags, canonical tags, response codes, redirect chains, and
      on-page elements.
PARAMETERS:
  - url: Target page URL (e.g., "https://example.com/locations/dallas/")
  - Check: status_code, meta_robots, canonical, redirect_chain, page_timing
```

### Tool 2: Core Web Vitals & Performance

```
TOOL: mcp__dfs-mcp__on_page_lighthouse
USE:  Run Lighthouse audits on local money pages to get Core Web Vitals
      scores, performance metrics, mobile usability data, and accessibility scores.
PARAMETERS:
  - url: Target page URL
  - device: "mobile" (ALWAYS test mobile for local — this is non-negotiable)
  - categories: ["performance", "accessibility", "best-practices", "seo"]
```

### Workflow: Batch Audit of Local Pages

```
1. Identify all local money pages from Phase 5/8 output
2. Run on_page_instant_pages on EACH page — check indexation signals
3. Run on_page_lighthouse on top 5-10 priority pages — check CWV
4. Flag any page with:
   - status_code != 200 → CRITICAL
   - meta_robots contains "noindex" → CRITICAL
   - canonical != self → HIGH
   - redirect_chain length > 1 → HIGH
   - LCP > 4.0s → HIGH
   - Mobile performance < 40 → HIGH
5. Compile findings into output format below
```

---

## User Data Requests

### Required Data:
1. **Google Search Console — Coverage Report**
   - Pages with errors (4xx, 5xx, redirect errors)
   - Pages excluded by noindex
   - Pages with canonical issues
   - Crawled but not indexed pages (critical for new location pages)

2. **Google Search Console — Core Web Vitals Report**
   - URLs in "Poor" and "Needs Improvement" categories
   - Field data vs. lab data comparison
   - Mobile vs. desktop CWV performance

3. **Screaming Frog Crawl Export** (if available)
   - Full site crawl or subfolder crawl of `/locations/` and `/services/`
   - Export columns: URL, Status Code, Indexability, Canonical, Title, H1, Response Time, Word Count
   - Filter for: non-200 status codes, non-indexable pages, non-self canonicals

### Optional but Valuable:
- Hosting provider and plan details (shared hosting = slower)
- CDN configuration (Cloudflare, Fastly, etc.)
- Recent site changes or migrations
- CMS and page builder used (WordPress + Elementor vs. custom React, etc.)
- Any known staging environment URLs (to check for accidental indexation)

---

## Output Format

```
==============================================================================
PHASE 9: TECHNICAL SEO FOR LOCAL
==============================================================================

Domain: [domain.com]
Audit Date: [YYYY-MM-DD]
Auditor: Claude Code (Local SEO Auditor)
Pages Audited: [X local money pages]

------------------------------------------------------------------------------
TECHNICAL SEO SCORE: [XX]/100 — [Excellent/Good/Needs Work/Poor/Critical]
------------------------------------------------------------------------------

CRITICAL FINDINGS (Fix Immediately)
------------------------------------------------------------------------------
  [C] [Issue description]
      Page(s) Affected: [URLs]
      Local Impact: [How this blocks local rankings]
      Fix: [Specific remediation steps]

  [C] [Issue description]
      Page(s) Affected: [URLs]
      Local Impact: [How this blocks local rankings]
      Fix: [Specific remediation steps]


CRAWLABILITY (Score: [XX]/20)
------------------------------------------------------------------------------
  [P] robots.txt                                [XX/8]
      Status: [Clean / Blocking local pages / Crawl-delay set]
      Blocked Local Pages: [List or "None"]
      AI Bot Blocking: [GPTBot: Y/N, ClaudeBot: Y/N]
      Action: [Specific fix or "None needed"]

  [P] XML Sitemap                               [XX/6]
      URL: [sitemap URL]
      Local Pages Included: [X/Y pages]
      Issues: [List or "None"]
      Action: [Specific fix or "None needed"]

  [P] Site Structure Depth                      [XX/6]
      Avg Click Depth (local pages): [X clicks]
      Deepest Local Page: [URL — X clicks]
      Action: [Specific fix or "None needed"]


INDEXATION (Score: [XX]/25)
------------------------------------------------------------------------------
  [P] noindex Issues                            [XX/12]
      Blocked Local Pages: [List or "None"]
      Source of Block: [Meta tag / X-Robots-Tag / Plugin setting]
      Action: [Remove noindex from X pages]

  [P] Canonical Tags                            [XX/8]
      Issues Found: [X pages with canonical conflicts]
      Details: [List problematic pages and their canonical targets]
      Action: [Fix canonicals on X pages]

  [P] Index Bloat                               [XX/5]
      Indexed Pages: [X total]
      Expected: [Y estimated]
      Thin/Duplicate: [List if found]
      Action: [noindex thin pages, block parameters]


MOBILE OPTIMIZATION (Score: [XX]/20)
------------------------------------------------------------------------------
  [P] Mobile-First Assessment                   [XX/10]
      Viewport: [Set / Missing]
      Responsive: [Y/N]
      Tap Targets: [Pass / X failures]
      Click-to-Call: [Working / Not implemented]
      Action: [Specific fixes]

  [P] Mobile Page Speed                         [XX/10]
      Avg Mobile Performance: [XX/100]
      LCP: [Xs] | INP: [Xms] | CLS: [X.XX]
      Worst Page: [URL — score]
      Action: [Top 3 speed improvements]


PAGE SPEED & CWV (Score: [XX]/15)
------------------------------------------------------------------------------
  [P] Core Web Vitals                           [XX/10]
      Pages Passing: [X/Y]
      Failed Pages: [URLs with specific failing metrics]
      Action: [Prioritized speed fixes]

  [P] Speed Optimization                        [XX/5]
      Opportunities: [Image optimization, JS deferral, etc.]
      Estimated Impact: [X seconds LCP improvement]
      Action: [Top 3 optimizations]


HTTPS & SECURITY (Score: [XX]/10)
------------------------------------------------------------------------------
  [P] SSL Certificate                           [XX/5]
      Status: [Valid / Expired / Missing]
      Mixed Content: [Y/N — X resources]
      HTTP→HTTPS Redirect: [301 / Missing / Chain]
      Action: [Specific fixes]

  [P] Security Headers                          [XX/5]
      HSTS: [Set / Missing]
      CSP: [Set / Missing]
      X-Frame-Options: [Set / Missing]
      Action: [Add missing headers]


REDIRECTS (Score: [XX]/5)
------------------------------------------------------------------------------
  [P] Redirect Health                           [XX/5]
      Chains Found: [X chains on local pages]
      302 on Permanent Pages: [X pages]
      Loops: [None / X loops detected]
      Action: [Flatten chains, convert 302→301]


RENDERING (Score: [XX]/5)
------------------------------------------------------------------------------
  [P] JavaScript Rendering                      [XX/5]
      Framework: [WordPress / React / Next.js / etc.]
      SSR Status: [Full SSR / Partial / CSR Only]
      Content in HTML Source: [Y/N for local content]
      Action: [Implement SSR / None needed]


------------------------------------------------------------------------------
PRIORITY ACTION ITEMS (Ordered by Local Impact)
------------------------------------------------------------------------------

CRITICAL (Fix This Week — Local Pages at Risk):
  1. [Highest-impact fix — likely indexation or crawl block]
  2. [Second critical fix]

HIGH (Fix Within 30 Days):
  3. [Mobile or speed fix]
  4. [Redirect or canonical fix]
  5. [Security fix]

MEDIUM (Fix Within 90 Days):
  6. [Optimization item]
  7. [Cleanup item]

==============================================================================
```

---

## Cross-References

| Skill | Relationship | When to Use Together |
|---|---|---|
| `/local-on-page-audit` | **Complementary** — On-page audit (Phase 5) identifies the content on local pages; this skill ensures those pages are technically accessible. | Run on-page first to identify money pages, then technical audit to verify they are crawlable and indexable. |
| `/site-architecture-local` | **Prerequisite data** — Site architecture audit (Phase 8) maps the internal link structure. Technical SEO checks that crawlers can follow those links. | Architecture identifies structural issues; technical SEO identifies crawler-level blocks. |
| `/local-schema-markup` | **Connected** — Schema markup (Phase 10) is embedded in the HTML. If pages have rendering issues (9.7), schema may not be parsed. | Run technical audit first to ensure pages render fully before validating schema. |
| `/local-landing-pages` | **Dependent** — Landing page quality (Phase 7) depends on pages being indexed and fast. A perfect landing page with a noindex tag is invisible. | Technical audit validates the foundation; landing page audit evaluates the content. |
| `/local-seo-audit` | **Parent** — This skill is Phase 9 of the comprehensive local SEO audit workflow. | Always run as part of the full audit sequence. |

---

*Phase 9 focuses on the technical foundation that enables local page visibility. For content quality on those pages, see `/local-on-page-audit` (Phase 5) and `/local-landing-pages` (Phase 7). For schema implementation on technically sound pages, proceed to `/local-schema-markup` (Phase 10).*
