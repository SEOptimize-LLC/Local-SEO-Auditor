---
name: Local Citation Audit
description: Phase 4 of the Local SEO Audit suite. Evaluates NAP consistency, citation volume and quality, platform coverage, and data aggregator presence across the citation ecosystem. Produces a scored citation health report with a prioritized building strategy bifurcated for Map Pack and AI Search channels.
version: 1.0.0
tags: [local-seo, citations, nap-consistency, business-listings, data-aggregators]
related:
  - local-gbp-audit (Phase 1)
  - local-review-strategy (Phase 2)
  - local-link-building (Phase 3)
  - local-keyword-research (Phase 5)
  - map-pack-analysis (Phase 6)
  - local-on-page-audit (Phase 7)
  - local-landing-pages (Phase 8)
---

# Phase 4: Local Citation Audit

## When to Use

Run this skill when:
- Performing a full Local SEO audit (Phase 4 in the standard sequence)
- A client reports inconsistent business information across directories
- Google Business Profile shows "info suggests different hours/address" warnings
- A business has recently moved, rebranded, or changed phone numbers
- Local rankings have dropped without obvious on-page or link-related causes
- Preparing a new client onboarding and establishing a citation baseline
- Evaluating AI Search presence and discoverability across platforms

## Channel Impact

| Channel         | Click Share | Citation Weight | Strategic Implication                                      |
|-----------------|-------------|-----------------|-------------------------------------------------------------|
| Local Map Pack  | 44%         | 6%              | Quality over quantity. 50-75 high-authority citations suffice. NAP consistency is the primary signal. |
| Local Organic   | 30%         | 10%             | Structured citations reinforce domain authority and entity recognition. Industry directories carry link equity. |
| AI Search       | Emerging    | 13%             | AI models aggregate entity data across platforms. 100+ citations increase AI mention likelihood. "Best of Local" roundup inclusion is critical. |

### Bifurcated Citation Strategy

**Map Pack Focus (6% weight):** Prioritize NAP consistency and authority. Maintain 50-75 citations on high-trust platforms. Fix inconsistencies before building new listings. One wrong NAP on a Tier 1 platform causes more damage than 20 missing Tier 3 listings.

**AI Search Focus (13% weight):** Volume and breadth matter. AI models pull entity data from diverse sources. Target 100+ citations across all tiers. Actively pursue inclusion in "Best of [Service] in [City]" roundup articles, local media mentions, and curated recommendation lists that AI models use as training and retrieval sources.

## Prerequisites

Before running this skill, you should have:
1. **Master NAP Standard** established (exact business name, address, phone, website URL)
2. **GBP Audit (Phase 1)** completed to confirm the canonical NAP on Google
3. **Business category list** from GBP and industry classification
4. **List of known existing citations** (if available from client)
5. **Any previous citation reports** from BrightLocal, Whitespark, Moz Local, or Yext

## Assessment Framework

### Step 1: Establish the Master NAP Standard

Before auditing anything, lock down the single source of truth for business identity.

```
MASTER NAP RECORD
-----------------
Business Name:    [Exact legal/marketing name as on GBP]
Address Line 1:   [Street number + street name, consistent abbreviation]
Address Line 2:   [Suite/Unit if applicable]
City:             [Full city name, no abbreviations]
State:            [Two-letter abbreviation]
ZIP:              [ZIP+4 if available]
Phone:            [Primary local number in (XXX) XXX-XXXX format]
Website:          [Full URL with https:// and trailing slash convention]
Hours:            [Standard format: Mon-Fri 8:00 AM - 5:00 PM]
Categories:       [Primary + secondary categories]
```

**Common NAP Inconsistencies to Watch:**
- "St" vs "Street" vs "St."
- "Suite" vs "Ste" vs "Ste." vs "#"
- Tracking phone numbers on some platforms but local number on others
- Old addresses persisting after a move
- DBA names vs legal names vs marketing names
- Missing or inconsistent suite/unit numbers

### Step 2: Platform Coverage Audit by Tier

#### Tier 1 Platforms (Must-Have, Audit First)
These carry the highest authority and are checked by Google and AI models first.

| Platform       | Type           | Priority | Notes                                    |
|----------------|----------------|----------|------------------------------------------|
| Google Business Profile | Search Engine | Critical | Canonical source of truth              |
| Yelp           | Review/Directory | Critical | Major AI training source               |
| Facebook       | Social/Directory | Critical | Entity validation + social signals     |
| BBB            | Trust/Authority  | High     | Trust signal for Google and AI          |
| HomeAdvisor    | Industry (Home)  | High     | If home services vertical               |
| Avvo           | Industry (Legal) | High     | If legal vertical                        |
| Healthgrades   | Industry (Medical)| High    | If medical vertical                      |
| TripAdvisor    | Industry (Hospitality)| High | If hospitality/restaurant vertical      |

#### Tier 2 Platforms (Important, Build Within 60 Days)

| Platform       | Type           | Priority | Notes                                    |
|----------------|----------------|----------|------------------------------------------|
| Apple Maps     | Navigation     | High     | Growing importance for Siri/AI          |
| Bing Places    | Search Engine  | High     | Powers Copilot AI responses             |
| Nextdoor       | Community      | Medium   | Local trust + behavioral signals         |
| Chamber of Commerce | Authority | Medium   | Local authority backlink                 |
| Angi           | Industry       | Medium   | Home services vertical                   |
| Thumbtack      | Industry       | Medium   | Service-based businesses                 |
| Yellow Pages   | Directory      | Medium   | Legacy authority signal                  |
| MapQuest       | Navigation     | Medium   | Data aggregator endpoint                 |

#### Tier 3 Platforms (Volume Building, Ongoing)

| Platform Type  | Examples                                | Target Count |
|----------------|-----------------------------------------|-------------|
| Regional directories | City-specific, state directories   | 5-10        |
| Industry directories | Vertical-specific associations     | 5-15        |
| Niche directories | Specialty, certification-based      | 5-10        |
| Local media    | Newspaper directories, local blogs      | 3-5         |
| University/Gov | .edu and .gov local resource pages      | 1-3         |

### Step 3: Data Aggregator Coverage

Data aggregators push business information to hundreds of downstream directories. Gaps here cause widespread inconsistencies.

| Aggregator     | Coverage                              | Submission Method          |
|----------------|---------------------------------------|----------------------------|
| Data Axle      | Powers 100+ directories               | Direct or via Yext/BrightLocal |
| Neustar/Localeze | Powers navigation + directory sites | Direct or via Yext         |
| Foursquare     | Powers Apple Maps, Uber, Samsung, etc. | Foursquare for Business    |

**Check:** For each aggregator, verify that the Master NAP is accurately reflected. A single error at the aggregator level cascades to dozens of downstream listings.

### Step 4: Duplicate Listing Detection

Duplicate listings confuse Google, split review equity, and create NAP inconsistencies.

**Detection Method:**
1. Search Google Maps for business name + city
2. Search each Tier 1 platform for business name
3. Search by phone number across platforms
4. Search by address across platforms
5. Check for old/previous business names

**For Each Duplicate Found, Record:**
- Platform where duplicate exists
- Which NAP fields differ from Master NAP
- Whether the duplicate has reviews (complicates removal)
- Recommended action: merge, claim, remove, or suppress

### Step 5: Industry-Specific Directory Analysis

Map the relevant vertical-specific directories for the client's industry.

| Vertical        | Key Directories                                              |
|-----------------|--------------------------------------------------------------|
| Home Services   | HomeAdvisor, Angi, Houzz, Porch, Thumbtack                 |
| Legal           | Avvo, FindLaw, Justia, Lawyers.com, Martindale             |
| Medical         | Healthgrades, Vitals, WebMD, Zocdoc, RateMDs              |
| Restaurants     | TripAdvisor, OpenTable, Zomato, DoorDash, Grubhub          |
| Real Estate     | Zillow, Realtor.com, Trulia, Redfin                        |
| Automotive      | CarGurus, AutoTrader, Cars.com, RepairPal                  |
| Financial       | NerdWallet, Bankrate, SmartAsset, WalletHub                |
| Dental          | 1-800-Dentist, DentalPlans, Zocdoc                         |

### Step 6: Citation Building Strategy

**Monthly Building Targets:**
- Month 1: All Tier 1 platforms + data aggregators (10-15 citations)
- Month 2: All Tier 2 platforms (10-15 citations)
- Month 3-4: Tier 3 industry-specific (10-15 per month)
- Month 5-6: Tier 3 regional and niche (10-15 per month)
- Ongoing: Monitor, fix inconsistencies, pursue new opportunities

**AI Search Citation Expansion (beyond Month 6):**
- Target "Best of [Service] in [City]" article inclusion
- Submit to AI-indexed recommendation platforms
- Build presence on emerging AI-referenced directories
- Target 100+ total citations for AI discoverability threshold

## Scoring Rubric

Total: 100 points

| Component              | Points | Criteria                                                    |
|------------------------|--------|-------------------------------------------------------------|
| NAP Consistency        | 35     | % of citations matching Master NAP exactly                  |
| Tier 1 Coverage        | 20     | Presence on all relevant Tier 1 platforms                   |
| Data Aggregator Coverage| 15    | All 3 major aggregators verified and accurate               |
| Citation Volume         | 10    | Total count relative to target (50-75 Map Pack / 100+ AI)  |
| Tier 2 Coverage        | 8      | Presence on relevant Tier 2 platforms                       |
| Duplicate Management   | 7      | No unresolved duplicates on Tier 1/2 platforms              |
| Industry Directories   | 5      | Coverage of vertical-specific directories                   |

**Score Interpretation:**
- 90-100: Excellent. Citations are a competitive advantage. Focus on AI expansion.
- 75-89: Good. Minor inconsistencies or gaps to address. 30-day fix plan.
- 50-74: Needs Work. Significant gaps or NAP issues undermining rankings. 60-day plan.
- Below 50: Critical. Citations are actively hurting rankings. Immediate remediation.

## DFS MCP Data Sources

### Primary Tool: business_data_business_listings_search

Use this to discover existing citations and check NAP consistency programmatically.

```python
# DFS MCP Call: Search for business listings
# Tool: business_data_business_listings_search

search_params = {
    "keyword": "Business Name City State",
    "categories": ["plumber", "plumbing"],  # adjust to vertical
    "filters": {
        "country": "US",
        "city": "Target City"
    }
}

# Expected response fields to extract:
# - title (business name as listed)
# - address (full address string)
# - phone (phone number as listed)
# - url (website URL as listed)
# - category (listed categories)
# - rating (if available)
# - platform/source
```

### Python Fallback: NAP Consistency Checker

```python
"""
NAP Consistency Checker
Compares discovered citations against the Master NAP standard.
"""

import re
from dataclasses import dataclass
from typing import Optional
from difflib import SequenceMatcher


@dataclass
class MasterNAP:
    business_name: str
    address_line1: str
    address_line2: Optional[str]
    city: str
    state: str
    zip_code: str
    phone: str
    website: str


@dataclass
class CitationRecord:
    platform: str
    tier: int  # 1, 2, or 3
    business_name: str
    address: str
    phone: str
    website: str
    has_reviews: bool
    review_count: int
    is_claimed: bool


def normalize_phone(phone: str) -> str:
    """Strip phone to digits only for comparison."""
    digits = re.sub(r'\D', '', phone)
    if len(digits) == 11 and digits.startswith('1'):
        digits = digits[1:]
    return digits


def normalize_address(address: str) -> str:
    """Normalize common address abbreviation variants."""
    replacements = {
        r'\bstreet\b': 'st',
        r'\bavenue\b': 'ave',
        r'\bboulevard\b': 'blvd',
        r'\bdrive\b': 'dr',
        r'\blane\b': 'ln',
        r'\broad\b': 'rd',
        r'\bsuite\b': 'ste',
        r'\bapartment\b': 'apt',
        r'\bnorth\b': 'n',
        r'\bsouth\b': 's',
        r'\beast\b': 'e',
        r'\bwest\b': 'w',
    }
    addr = address.lower().strip()
    addr = re.sub(r'[.,#]', '', addr)
    for pattern, replacement in replacements.items():
        addr = re.sub(pattern, replacement, addr, flags=re.IGNORECASE)
    addr = re.sub(r'\s+', ' ', addr)
    return addr


def check_nap_consistency(master: MasterNAP, citation: CitationRecord) -> dict:
    """Compare a citation against the master NAP and return match details."""
    name_similarity = SequenceMatcher(
        None,
        master.business_name.lower(),
        citation.business_name.lower()
    ).ratio()

    master_addr = normalize_address(master.address_line1)
    citation_addr = normalize_address(citation.address)
    address_similarity = SequenceMatcher(None, master_addr, citation_addr).ratio()

    phone_match = normalize_phone(master.phone) == normalize_phone(citation.phone)

    master_url = master.website.lower().rstrip('/').replace('https://', '').replace('http://', '').replace('www.', '')
    citation_url = citation.website.lower().rstrip('/').replace('https://', '').replace('http://', '').replace('www.', '')
    url_match = master_url == citation_url

    return {
        "platform": citation.platform,
        "tier": citation.tier,
        "name_match": name_similarity >= 0.95,
        "name_similarity": round(name_similarity, 3),
        "address_match": address_similarity >= 0.90,
        "address_similarity": round(address_similarity, 3),
        "phone_match": phone_match,
        "url_match": url_match,
        "overall_consistent": all([
            name_similarity >= 0.95,
            address_similarity >= 0.90,
            phone_match,
            url_match
        ]),
        "is_claimed": citation.is_claimed,
        "has_reviews": citation.has_reviews,
        "issues": []
    }


def generate_citation_report(master: MasterNAP, citations: list[CitationRecord]) -> dict:
    """Generate full citation audit report."""
    results = [check_nap_consistency(master, c) for c in citations]
    consistent = sum(1 for r in results if r["overall_consistent"])
    total = len(results)

    tier_coverage = {1: set(), 2: set(), 3: set()}
    for c in citations:
        tier_coverage[c.tier].add(c.platform)

    return {
        "total_citations": total,
        "consistent_citations": consistent,
        "consistency_rate": round(consistent / total * 100, 1) if total > 0 else 0,
        "tier_1_count": len(tier_coverage[1]),
        "tier_2_count": len(tier_coverage[2]),
        "tier_3_count": len(tier_coverage[3]),
        "inconsistent_listings": [r for r in results if not r["overall_consistent"]],
        "unclaimed_listings": [r for r in results if not r["is_claimed"]],
    }
```

## User Data Requests

Ask the client or account manager for:

1. **Master NAP confirmation** - Exact business name, address, phone, and website URL as it should appear everywhere
2. **Previous citation reports** - Any existing reports from BrightLocal, Whitespark, Moz Local, or Yext
3. **Known listings** - A list of platforms where they know they have listings
4. **Recent changes** - Any name, address, or phone number changes in the past 2 years
5. **Multiple locations** - Whether additional locations exist that could create confusion
6. **Tracking numbers** - Any call tracking numbers in use and where they are deployed
7. **Industry vertical** - To identify the correct industry-specific directories

## Output Format

Structure the Phase 4 section of the audit report as follows:

```markdown
## Phase 4: Citation Audit

### Citation Health Score: [XX]/100

### Master NAP Standard
| Field          | Value                          |
|----------------|--------------------------------|
| Business Name  | [exact name]                   |
| Address        | [full address]                 |
| Phone          | [formatted phone]              |
| Website        | [full URL]                     |

### Citation Summary
- **Total Citations Found:** [count]
- **NAP Consistent:** [count] ([%])
- **NAP Inconsistent:** [count] ([%])
- **Duplicates Detected:** [count]
- **Unclaimed Listings:** [count]

### Platform Coverage
| Tier | Target | Found | Consistent | Gap |
|------|--------|-------|------------|-----|
| Tier 1 | [X] | [Y] | [Z] | [list missing] |
| Tier 2 | [X] | [Y] | [Z] | [list missing] |
| Tier 3 | [X] | [Y] | [Z] | [list missing] |

### Data Aggregator Status
| Aggregator | Status | NAP Accurate | Action Needed |
|------------|--------|-------------|---------------|
| Data Axle  | [status] | [Y/N]    | [action]      |
| Neustar    | [status] | [Y/N]    | [action]      |
| Foursquare | [status] | [Y/N]    | [action]      |

### Inconsistencies Found
[Table of each inconsistent listing with platform, field, expected value, found value]

### Duplicate Listings
[Table of duplicates with platform, duplicate NAP, recommended action]

### Recommendations
1. **Immediate (Week 1-2):** [Fix Tier 1 inconsistencies, claim unclaimed Tier 1 listings]
2. **Short-term (Month 1):** [Data aggregator corrections, Tier 2 cleanup]
3. **Medium-term (Month 2-3):** [Tier 3 building, industry directory expansion]
4. **AI Search Expansion (Month 4-6):** [Volume building toward 100+ target, roundup article outreach]
```

## Cross-References

- **Phase 1 (GBP Audit):** The canonical NAP on GBP is the Master NAP standard. Any GBP inconsistencies must be resolved before citation work begins.
- **Phase 2 (Review Strategy):** Review platforms are also citation sources. Ensure NAP is consistent on all review platforms identified in Phase 2.
- **Phase 3 (Link Building):** Many citation sources also provide backlinks. Coordinate with link building to avoid duplicate outreach.
- **Phase 5 (Keyword Research):** Category-specific citations should align with target keyword verticals.
- **Phase 6 (Map Pack Analysis):** Citation consistency directly impacts Map Pack rankings. Cross-reference Map Pack performance with citation health.
- **Phase 7 (On-Page Audit):** NAP on the website must match the Master NAP. Schema markup should encode the same NAP values.
- **Phase 8 (Landing Pages):** Location pages should include consistent NAP and link to relevant citation profiles.
