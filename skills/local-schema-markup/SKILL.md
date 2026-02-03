---
name: local-schema-markup
description: Local schema markup audit and implementation — LocalBusiness, Service, Review, FAQ, Breadcrumb, and GeoCoordinates schema with complete JSON-LD templates
version: 1.0.0
tags: [local-seo, schema, structured-data, json-ld, local-business, rich-results, audit]
related: [technical-seo-local, local-on-page-audit, gbp-audit, local-landing-pages, local-seo-audit]
---

# Phase 10: Local Schema Markup

> **Schema markup is the bridge between your website and search engines' understanding of your business.** For local SEO, proper schema tells Google exactly what your business is, where it operates, what services it offers, when it is open, and what customers think of it. Without schema, Google must infer this information from unstructured text — and inference is unreliable. With schema, you provide explicit, machine-readable data that directly feeds into Map Pack results, Knowledge Panels, and AI search answers.

---

## When to Use This Skill

- **As part of the full Local SEO Audit**: Run as Phase 10, after the technical SEO audit (Phase 9) confirms that pages are crawlable and indexable. Schema on a noindexed page is worthless.
- **As a standalone audit**: When a client wants to improve rich result eligibility, when AI search citations are a priority, or when GBP data verification through schema is needed.
- **Trigger scenarios**:
  - Business is not appearing in rich results despite having reviews and FAQs
  - AI search engines (Google AI Overviews, ChatGPT, Perplexity) are not citing the business
  - GBP data conflicts with website data — schema can resolve this
  - New location pages launched and need proper structured data
  - Client wants to appear in "best of" lists and local knowledge panels
  - Google Search Console reports structured data errors or warnings

---

## Channel Impact

| Channel        | Weight  | Rationale |
|----------------|---------|-----------|
| **Map Pack**   | **GBP 32% reinforcement** | Schema on the website linked from GBP creates a verification bridge. When schema NAP matches GBP NAP, Google's confidence in the listing increases. OpeningHoursSpecification directly feeds the critical "Openness" signal. |
| **Organic**    | **On-Page 33% enhancement** | Schema enables rich results (star ratings, FAQ dropdowns, breadcrumbs) that dramatically improve CTR. Rich results earn 30-50% more clicks than plain results. |
| **AI Search**  | **On-Page 24% + Citations 13%** | AI search engines prioritize structured data when generating local recommendations. Well-structured schema makes your business data easy for AI to extract and cite accurately. |

**Total impact**: Schema is a force multiplier. It does not have its own weight category in ranking models, but it amplifies On-Page, GBP, and Citation signals across all three channels.

---

## Prerequisites

Before beginning the schema markup audit, ensure you have:

1. **Discovery Brief from Phase 1** (`/discovery-intake`)
   - Business name, address, phone (exact NAP)
   - Business type and industry vertical
   - Service list
   - Operating hours (including special hours)
   - Service area definition

2. **Technical Audit from Phase 9** (`/technical-seo-local`)
   - Confirm target pages are indexable (no noindex, correct canonicals)
   - Confirm pages render fully (schema in CSR-only pages may not be parsed)

3. **GBP Audit from Phase 2** (`/gbp-audit`)
   - GBP primary and secondary categories
   - GBP hours (schema hours MUST match GBP hours exactly)
   - GBP phone number and address

4. **Page Inventory**
   - Homepage URL
   - All location page URLs
   - All service page URLs
   - Blog/FAQ page URLs
   - Contact page URL

---

## Assessment Framework

### 10.1 LocalBusiness Schema (25 points)

**Why This Matters**: LocalBusiness schema (and its subtypes) is the foundational structured data for any local business website. It provides Google with explicit signals about the business identity, location, contact information, and operating hours.

#### Choosing the Right Subtype

Google supports over 100 LocalBusiness subtypes. Using the most specific subtype improves relevance signals. **Always use the most specific subtype that matches the business.**

**Common Subtypes by Industry**:

| Industry | Schema Type | Note |
|----------|------------|------|
| Plumber | `Plumber` | Direct subtype of HomeAndConstructionBusiness |
| Electrician | `Electrician` | Direct subtype of HomeAndConstructionBusiness |
| HVAC | `HVACBusiness` | Direct subtype of HomeAndConstructionBusiness |
| Locksmith | `Locksmith` | Direct subtype of HomeAndConstructionBusiness |
| Roofing | `RoofingContractor` | Direct subtype of HomeAndConstructionBusiness |
| Dentist | `Dentist` | Direct subtype of MedicalBusiness |
| Attorney | `Attorney` | Direct subtype of LegalService |
| Restaurant | `Restaurant` | Direct subtype of FoodEstablishment |
| Auto Repair | `AutoRepair` | Direct subtype of AutomotiveBusiness |
| Real Estate | `RealEstateAgent` | Direct subtype of LocalBusiness |
| Hair Salon | `HairSalon` | Direct subtype of HealthAndBeautyBusiness |
| Gym | `ExerciseGym` | Direct subtype of SportsActivityLocation |
| General | `LocalBusiness` | Use ONLY when no specific subtype exists |

#### Complete JSON-LD Template: LocalBusiness

```json
{
  "@context": "https://schema.org",
  "@type": "Plumber",
  "@id": "https://www.example.com/#organization",
  "name": "ABC Plumbing",
  "legalName": "ABC Plumbing LLC",
  "description": "Full-service plumbing company serving the Dallas-Fort Worth metroplex. Licensed, insured, and available for emergency repairs 24/7.",
  "url": "https://www.example.com",
  "telephone": "+1-214-555-1234",
  "email": "info@example.com",
  "foundingDate": "1998",
  "image": [
    "https://www.example.com/images/abc-plumbing-team.jpg",
    "https://www.example.com/images/abc-plumbing-logo.png"
  ],
  "logo": {
    "@type": "ImageObject",
    "url": "https://www.example.com/images/abc-plumbing-logo.png",
    "width": 600,
    "height": 200
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main Street, Suite 100",
    "addressLocality": "Dallas",
    "addressRegion": "TX",
    "postalCode": "75201",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 32.7767,
    "longitude": -96.7970
  },
  "areaServed": [
    {
      "@type": "City",
      "name": "Dallas",
      "sameAs": "https://en.wikipedia.org/wiki/Dallas"
    },
    {
      "@type": "City",
      "name": "Fort Worth",
      "sameAs": "https://en.wikipedia.org/wiki/Fort_Worth,_Texas"
    },
    {
      "@type": "State",
      "name": "Texas"
    }
  ],
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "07:00",
      "closes": "18:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": "Saturday",
      "opens": "08:00",
      "closes": "14:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": "Sunday",
      "opens": "00:00",
      "closes": "00:00",
      "description": "Emergency service only"
    }
  ],
  "priceRange": "$$",
  "paymentAccepted": ["Cash", "Credit Card", "Check"],
  "currenciesAccepted": "USD",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Plumbing Services",
    "itemListElement": [
      {
        "@type": "OfferCatalog",
        "name": "Emergency Plumbing",
        "itemListElement": [
          {
            "@type": "Offer",
            "itemOffered": {
              "@type": "Service",
              "name": "Emergency Drain Cleaning"
            }
          }
        ]
      }
    ]
  },
  "sameAs": [
    "https://www.facebook.com/abcplumbing",
    "https://www.yelp.com/biz/abc-plumbing-dallas",
    "https://www.instagram.com/abcplumbing",
    "https://www.linkedin.com/company/abc-plumbing",
    "https://www.youtube.com/@abcplumbing"
  ],
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "bestRating": "5",
    "worstRating": "1",
    "ratingCount": "347",
    "reviewCount": "312"
  }
}
```

#### OpeningHoursSpecification — CRITICAL for "Openness" Signal

This property directly feeds Google's "Openness" filter. **Schema hours MUST match GBP hours exactly.** Any mismatch creates a data conflict that reduces Google's trust in both sources.

**24/7 Availability**:
```json
{
  "@type": "OpeningHoursSpecification",
  "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday", "Sunday"],
  "opens": "00:00",
  "closes": "23:59"
}
```

**Special Hours (holidays)**:
```json
{
  "@type": "OpeningHoursSpecification",
  "validFrom": "2025-12-24",
  "validThrough": "2025-12-25",
  "opens": "00:00",
  "closes": "00:00",
  "description": "Closed for Christmas"
}
```

**Scoring**:
- 0 points: No LocalBusiness schema present on any page
- 8 points: LocalBusiness schema present but uses generic type, missing key properties, or has NAP mismatches
- 15 points: LocalBusiness schema with correct subtype but missing some properties (geo, areaServed, openingHours)
- 25 points: Complete LocalBusiness schema with correct subtype, full NAP, geo, areaServed, openingHours matching GBP, aggregateRating, and sameAs links

---

### 10.2 Service Schema (20 points)

**Why This Matters**: Service schema tells Google exactly what services the business offers, with descriptions, pricing, and service area. This data feeds into both organic rich results and AI search answers about "who offers X service in Y city."

#### JSON-LD Template: Service (per service page)

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "serviceType": "Emergency Drain Cleaning",
  "name": "Emergency Drain Cleaning in Dallas, TX",
  "description": "24/7 emergency drain cleaning service for residential and commercial properties in Dallas-Fort Worth. Professional hydro-jetting, camera inspection, and root removal.",
  "provider": {
    "@type": "Plumber",
    "@id": "https://www.example.com/#organization"
  },
  "areaServed": {
    "@type": "City",
    "name": "Dallas",
    "sameAs": "https://en.wikipedia.org/wiki/Dallas"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Drain Cleaning Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Basic Drain Cleaning",
          "description": "Standard snake/auger drain cleaning for kitchen, bathroom, and floor drains"
        },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "price": "149",
          "priceCurrency": "USD",
          "minPrice": "99",
          "maxPrice": "249"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Hydro-Jetting",
          "description": "High-pressure water jetting for severe clogs, grease buildup, and root intrusion"
        },
        "priceSpecification": {
          "@type": "PriceSpecification",
          "price": "450",
          "priceCurrency": "USD",
          "minPrice": "350",
          "maxPrice": "650"
        }
      }
    ]
  },
  "termsOfService": "https://www.example.com/terms/",
  "availableChannel": {
    "@type": "ServiceChannel",
    "servicePhone": {
      "@type": "ContactPoint",
      "telephone": "+1-214-555-1234",
      "contactType": "customer service",
      "availableLanguage": ["English", "Spanish"]
    },
    "serviceUrl": "https://www.example.com/services/drain-cleaning/"
  }
}
```

**Implementation Rule**: Each service page should have its own Service schema with the specific service type, description, and pricing for that page. Do NOT put all services in a single schema block on the homepage.

**Scoring**:
- 0 points: No Service schema on any service page
- 8 points: Service schema on some pages but incomplete (missing areaServed, pricing, or description)
- 15 points: Service schema on most pages with good property coverage
- 20 points: Every service page has complete Service schema with pricing, areaServed, provider reference, and service descriptions

---

### 10.3 AggregateRating & Review Schema (15 points)

**Why This Matters**: Review schema enables star rating rich results in organic search. Businesses with star ratings in SERPs earn 25-35% higher click-through rates. This is one of the most visible and impactful schema types.

#### JSON-LD Template: AggregateRating (on homepage/location pages)

```json
{
  "@context": "https://schema.org",
  "@type": "Plumber",
  "@id": "https://www.example.com/#organization",
  "name": "ABC Plumbing",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "bestRating": "5",
    "worstRating": "1",
    "ratingCount": "347",
    "reviewCount": "312"
  }
}
```

#### JSON-LD Template: Individual Review (on testimonials page)

```json
{
  "@context": "https://schema.org",
  "@type": "Review",
  "itemReviewed": {
    "@type": "Plumber",
    "@id": "https://www.example.com/#organization",
    "name": "ABC Plumbing"
  },
  "author": {
    "@type": "Person",
    "name": "John D."
  },
  "datePublished": "2025-01-15",
  "reviewBody": "ABC Plumbing responded to our emergency call within 30 minutes. The technician was professional, explained the issue clearly, and had our pipes fixed in under an hour. Highly recommend for anyone in the Dallas area.",
  "reviewRating": {
    "@type": "Rating",
    "ratingValue": "5",
    "bestRating": "5",
    "worstRating": "1"
  }
}
```

**Critical Rules**:
- AggregateRating values MUST be accurate and match actual review data. Inflated ratings violate Google's policies and can result in manual actions.
- Self-serving reviews (written by the business) are against Google's guidelines.
- Reviews must be from actual customers with real names.
- Update reviewCount and ratingValue regularly (at least monthly).

**Scoring**:
- 0 points: No review or rating schema
- 5 points: AggregateRating present but values are stale, inaccurate, or on wrong page type
- 10 points: AggregateRating with current values on homepage and location pages
- 15 points: AggregateRating on homepage + individual Review schema on testimonials page, all values current and accurate

---

### 10.4 FAQPage Schema (10 points)

**Why This Matters**: FAQ schema enables rich result dropdowns in SERPs — the accordion-style expandable Q&A that takes up significant visual real estate. For local businesses, FAQ rich results with local questions dominate SERP space and pre-answer common customer queries.

#### JSON-LD Template: FAQPage

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How much does emergency plumbing cost in Dallas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Emergency plumbing service in Dallas typically ranges from $150-$500 depending on the severity and time of the call. ABC Plumbing offers a flat $89 diagnostic fee that is waived if you proceed with the repair. Weekend and after-hours calls may include a $50 emergency surcharge."
      }
    },
    {
      "@type": "Question",
      "name": "Do you offer same-day plumbing service in Fort Worth?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, ABC Plumbing offers same-day service throughout the Fort Worth area. For urgent issues like burst pipes, gas leaks, or sewage backups, we dispatch a licensed plumber within 60 minutes of your call, 24 hours a day, 7 days a week."
      }
    },
    {
      "@type": "Question",
      "name": "Are your plumbers licensed and insured in Texas?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, all ABC Plumbing technicians hold valid Texas State Plumbing Licenses and are fully insured with $2M in general liability coverage. Our master plumber license number is M-40123. We also carry workers' compensation insurance for all employees."
      }
    }
  ]
}
```

**Best Practices for Local FAQ Schema**:
- Include the city/service area in question text naturally
- Answer with specific local details (pricing for the area, response times, local regulations)
- 3-8 questions per page is optimal (too many and Google may ignore them)
- Questions should match real customer queries (use Google's "People Also Ask" for ideas)
- Place FAQPage schema on service pages and location pages, not just a dedicated FAQ page

**Scoring**:
- 0 points: No FAQ schema on any page
- 4 points: FAQ schema on one page (e.g., dedicated FAQ page only)
- 7 points: FAQ schema on multiple relevant pages with local questions
- 10 points: FAQ schema on service pages and location pages with locally-relevant Q&A, 3-8 questions per page

---

### 10.5 BreadcrumbList Schema (10 points)

**Why This Matters**: Breadcrumb schema creates a visual hierarchy in search results that shows the page's position in the site structure. For local businesses, this reinforces the location hierarchy: Home > Locations > Dallas > Emergency Plumbing.

#### JSON-LD Template: BreadcrumbList

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://www.example.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Locations",
      "item": "https://www.example.com/locations/"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Dallas, TX",
      "item": "https://www.example.com/locations/dallas/"
    },
    {
      "@type": "ListItem",
      "position": 4,
      "name": "Emergency Plumbing",
      "item": "https://www.example.com/locations/dallas/emergency-plumbing/"
    }
  ]
}
```

**Scoring**:
- 0 points: No breadcrumb schema
- 4 points: Breadcrumb schema on some pages but hierarchy does not reflect local structure
- 7 points: Breadcrumb schema on all key pages with logical local hierarchy
- 10 points: Complete breadcrumb schema on all pages, hierarchy reflects Home > Location > Service pattern, matches visible breadcrumbs on page

---

### 10.6 GeoCoordinates & serviceArea (10 points)

**Why This Matters**: Explicit geographic data in schema removes ambiguity about where the business operates. GeoCoordinates pin the business location; serviceArea defines the reach. This data is especially valuable for AI search engines building local knowledge graphs.

#### GeoCoordinates (within LocalBusiness)

```json
"geo": {
  "@type": "GeoCoordinates",
  "latitude": 32.7767,
  "longitude": -96.7970
}
```

**How to get coordinates**: Google Maps > right-click on business location > copy coordinates. Verify they match the GBP pin location.

#### serviceArea (for SABs and businesses serving multiple areas)

```json
"areaServed": [
  {
    "@type": "City",
    "name": "Dallas",
    "sameAs": "https://en.wikipedia.org/wiki/Dallas"
  },
  {
    "@type": "City",
    "name": "Fort Worth",
    "sameAs": "https://en.wikipedia.org/wiki/Fort_Worth,_Texas"
  },
  {
    "@type": "GeoCircle",
    "geoMidpoint": {
      "@type": "GeoCoordinates",
      "latitude": 32.7767,
      "longitude": -96.7970
    },
    "geoRadius": "50000"
  }
]
```

**Scoring**:
- 0 points: No geographic schema data
- 4 points: GeoCoordinates present but no serviceArea, or coordinates are inaccurate
- 7 points: Both GeoCoordinates and serviceArea present, coordinates match GBP
- 10 points: Full geographic schema with accurate coordinates, comprehensive serviceArea matching GBP service areas, sameAs links to Wikipedia for cities

---

### 10.7 Multi-Location Schema Handling (10 points)

**Why This Matters**: Multi-location businesses need distinct schema for each location. Using a single schema block for multiple locations creates data conflicts. Each location page must have its own complete LocalBusiness schema with unique NAP, hours, and geo data.

**Architecture**:
- **Homepage**: Organization schema with `@id` reference
- **Location pages**: Each gets its own LocalBusiness schema with `parentOrganization` linking to the Organization `@id`
- **Service pages**: Service schema with `provider` referencing the relevant location's `@id`

#### JSON-LD Template: Location Page (multi-location)

```json
{
  "@context": "https://schema.org",
  "@type": "Plumber",
  "@id": "https://www.example.com/locations/dallas/#location",
  "name": "ABC Plumbing - Dallas",
  "parentOrganization": {
    "@type": "Organization",
    "@id": "https://www.example.com/#organization"
  },
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main Street",
    "addressLocality": "Dallas",
    "addressRegion": "TX",
    "postalCode": "75201",
    "addressCountry": "US"
  },
  "telephone": "+1-214-555-1234",
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 32.7767,
    "longitude": -96.7970
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "07:00",
      "closes": "18:00"
    }
  ]
}
```

**Scoring**:
- 0 points: Single schema block for all locations, or no schema on location pages
- 4 points: Separate schema per location but missing unique properties (same hours, same phone)
- 7 points: Unique schema per location with distinct NAP and hours
- 10 points: Complete per-location schema with parentOrganization reference, unique NAP/hours/geo, and distinct aggregateRating per location

**Single-location businesses**: Award full 10 points if LocalBusiness schema is complete and correct, as multi-location handling is not applicable.

---

## Schema Priority by Page Type

| Page Type | Required Schema | Optional Schema |
|-----------|----------------|-----------------|
| **Homepage** | LocalBusiness (full), BreadcrumbList | AggregateRating, sameAs |
| **Service Page** | Service, BreadcrumbList, FAQPage | Offer/PriceSpecification |
| **Location Page** | LocalBusiness (location-specific), BreadcrumbList | AggregateRating, FAQPage |
| **Blog Post** | Article, BreadcrumbList | FAQPage, HowTo |
| **Contact Page** | ContactPoint (within LocalBusiness) | BreadcrumbList |
| **Testimonials** | Review, AggregateRating | BreadcrumbList |

---

## Validation Workflow

### Step 1: Google Rich Results Test
- URL: https://search.google.com/test/rich-results
- Test each local money page
- Verify all schema types are detected
- Check for errors and warnings

### Step 2: Schema.org Validator
- URL: https://validator.schema.org/
- Paste JSON-LD code directly
- Check for property validation errors
- Verify all required properties are present

### Step 3: Google Search Console — Enhancements
- Check for structured data errors in GSC
- Monitor "valid" vs. "valid with warnings" vs. "error" counts
- Review specific error messages and affected URLs

### Common Errors and Fixes

| Error | Cause | Fix |
|-------|-------|-----|
| `Missing field "priceRange"` | LocalBusiness without priceRange | Add `"priceRange": "$$"` (use $-$$$$ scale) |
| `Invalid value for "telephone"` | Phone without country code | Use E.164 format: `"+1-214-555-1234"` |
| `Missing field "image"` | LocalBusiness without image property | Add at least one business image URL |
| `Value for "ratingValue" out of range` | Rating value above bestRating | Ensure ratingValue <= bestRating |
| `Missing field "reviewCount"` | AggregateRating without reviewCount | Add reviewCount with current count |
| `Duplicate LocalBusiness` | Same schema on multiple pages without @id | Use unique @id for each location |
| `Invalid date format` | Wrong date in validFrom/validThrough | Use ISO 8601: "2025-12-25" |

---

## Scoring Rubric

```
==============================================================
        LOCAL SCHEMA MARKUP SCORE CALCULATION
==============================================================

LOCALBUSINESS SCHEMA (25 points max)
--------------------------------------------------------------
  Correct subtype used:         ___/ 5  (0 = generic, 5 = specific)
  NAP properties complete:      ___/ 5  (0 = missing, 5 = complete + matching GBP)
  OpeningHoursSpecification:    ___/ 5  (0 = missing, 5 = complete + matching GBP)
  Full property coverage:       ___/10  (0 = minimal, 5 = partial, 10 = comprehensive)
                                ------
  LOCALBUSINESS SUBTOTAL:       ___/25


SERVICE SCHEMA (20 points max)
--------------------------------------------------------------
  Present on service pages:     ___/ 8  (0 = none, 4 = some, 8 = all)
  Property completeness:        ___/ 7  (0 = minimal, 4 = partial, 7 = full)
  Pricing included:             ___/ 5  (0 = none, 3 = some, 5 = all services)
                                ------
  SERVICE SUBTOTAL:             ___/20


REVIEW/RATING SCHEMA (15 points max)
--------------------------------------------------------------
  AggregateRating present:      ___/ 8  (0 = missing, 4 = stale, 8 = current)
  Review schema:                ___/ 4  (0 = none, 2 = partial, 4 = complete)
  Data accuracy:                ___/ 3  (0 = inaccurate, 3 = verified accurate)
                                ------
  REVIEW SUBTOTAL:              ___/15


FAQPAGE SCHEMA (10 points max)
--------------------------------------------------------------
  Present on relevant pages:    ___/ 5  (0 = none, 3 = FAQ page only, 5 = service+location)
  Local relevance of Q&A:      ___/ 5  (0 = generic, 3 = some local, 5 = locally-specific)
                                ------
  FAQ SUBTOTAL:                 ___/10


BREADCRUMBLIST (10 points max)
--------------------------------------------------------------
  Present on key pages:         ___/ 5  (0 = none, 3 = partial, 5 = all pages)
  Local hierarchy reflected:    ___/ 5  (0 = flat, 3 = basic, 5 = Home>Location>Service)
                                ------
  BREADCRUMB SUBTOTAL:          ___/10


GEO & SERVICE AREA (10 points max)
--------------------------------------------------------------
  GeoCoordinates accuracy:      ___/ 5  (0 = missing, 3 = present, 5 = verified match GBP)
  serviceArea coverage:         ___/ 5  (0 = missing, 3 = partial, 5 = comprehensive)
                                ------
  GEO SUBTOTAL:                 ___/10


MULTI-LOCATION HANDLING (10 points max)
--------------------------------------------------------------
  Per-location schema:          ___/ 5  (0 = shared, 3 = separate but incomplete, 5 = unique)
  @id and parentOrganization:   ___/ 5  (0 = missing, 3 = partial, 5 = properly linked)
                                ------
  MULTI-LOCATION SUBTOTAL:      ___/10


==============================================================
  SCHEMA MARKUP SCORE:          ___/100
==============================================================

SCORE INTERPRETATION:
  90-100:  Excellent — Comprehensive schema, rich result eligible, AI-ready
  75-89:   Good — Strong schema foundation, minor gaps to fill
  50-74:   Needs Work — Key schema types missing or incomplete
  25-49:   Poor — Minimal schema, missing major opportunities
  0-24:    Critical — No meaningful schema, invisible to structured data parsers
==============================================================
```

---

## DFS MCP Data Sources

### Tool 1: Check Existing Schema on Pages

```
TOOL: mcp__dfs-mcp__on_page_instant_pages
USE:  Analyze pages to detect existing schema markup, check for errors
      in structured data, and identify which schema types are present.
PARAMETERS:
  - url: Target page URL
  - Check: structured_data field in response — lists all detected schema types
  - Cross-reference detected schema against the required schema per page type
```

### Workflow: Schema Audit via DFS MCP

```
1. Get list of all local money pages from Phase 5/8 output
2. Run on_page_instant_pages on each page
3. Extract structured_data from each response
4. Compare detected schema against required schema per page type (see Priority table)
5. Flag missing schema types as opportunities
6. Check detected schema for property completeness
7. Cross-reference NAP in schema against GBP NAP from Phase 2
8. Compile findings into output format
```

---

## User Data Requests

### Required Data:
1. **Exact NAP Information** (to verify schema matches)
   - Legal business name
   - Full address with suite/unit number
   - Phone number with country code
   - Email address

2. **Business Hours** (to verify OpeningHoursSpecification)
   - Regular hours for each day of the week
   - Special/holiday hours
   - Emergency or after-hours availability

3. **Service List with Pricing** (for Service schema)
   - All services offered
   - Price ranges for each service
   - Service descriptions

4. **Google Search Console — Enhancements Report**
   - Structured data error counts
   - Specific error messages
   - Affected URLs

### Optional but Valuable:
- Current review count and average rating (for AggregateRating verification)
- Social media profile URLs (for sameAs property)
- Business founding date
- License and certification numbers

---

## Output Format

```
==============================================================================
PHASE 10: LOCAL SCHEMA MARKUP AUDIT
==============================================================================

Domain: [domain.com]
Audit Date: [YYYY-MM-DD]
Auditor: Claude Code (Local SEO Auditor)
Pages Audited: [X pages]

------------------------------------------------------------------------------
SCHEMA MARKUP SCORE: [XX]/100 — [Excellent/Good/Needs Work/Poor/Critical]
------------------------------------------------------------------------------

SCHEMA INVENTORY (Current State)
------------------------------------------------------------------------------
  Page                    | LB  | Svc | Rtg | FAQ | BC  | Geo |
  ----------------------- |-----|-----|-----|-----|-----|-----|
  Homepage                | [x] | [ ] | [x] | [ ] | [x] | [x] |
  /locations/dallas/      | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
  /services/plumbing/     | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
  /services/drain-clean/  | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |
  /contact/               | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] |

  LB=LocalBusiness, Svc=Service, Rtg=AggregateRating,
  FAQ=FAQPage, BC=BreadcrumbList, Geo=GeoCoordinates


DETAILED FINDINGS
------------------------------------------------------------------------------

  [P] LocalBusiness Schema                      [XX/25]
      Type Used: [Specific subtype or "LocalBusiness (too generic)"]
      NAP Match: [Matches GBP / MISMATCH — details]
      Hours Match: [Matches GBP / MISMATCH — details]
      Missing Properties: [List]
      Action: [Specific implementation/fix]

  [P] Service Schema                            [XX/20]
      Pages With Schema: [X/Y service pages]
      Missing Pages: [List URLs without Service schema]
      Property Gaps: [pricing, areaServed, etc.]
      Action: [Add schema to X pages, add Y properties]

  [P] Review/Rating Schema                      [XX/15]
      AggregateRating: [Present/Missing — current values]
      Accuracy: [Matches actual reviews / STALE / INFLATED]
      Review Schema: [Present/Missing on testimonials page]
      Action: [Update values, add to X pages]

  [P] FAQPage Schema                            [XX/10]
      Pages With FAQ Schema: [List]
      Local Relevance: [High/Medium/Low]
      Q&A Count: [X questions across Y pages]
      Action: [Add to X pages, localize questions]

  [P] BreadcrumbList Schema                     [XX/10]
      Pages With Breadcrumbs: [X/Y pages]
      Hierarchy Quality: [Reflects local structure / Flat / Missing]
      Action: [Implement on X pages with local hierarchy]

  [P] GeoCoordinates & serviceArea              [XX/10]
      Coordinates: [Present/Missing — accurate/inaccurate]
      serviceArea: [Present/Missing — comprehensive/partial]
      GBP Match: [Coordinates match GBP pin / MISMATCH]
      Action: [Add/fix coordinates and service areas]

  [P] Multi-Location Handling                   [XX/10]
      Location Count: [X locations]
      Per-Location Schema: [Unique/Shared/Missing]
      @id References: [Properly linked / Not linked]
      Action: [Create unique schema per location]


VALIDATION RESULTS
------------------------------------------------------------------------------
  Google Rich Results Test: [X errors, Y warnings across Z pages]
  Schema.org Validator: [X errors, Y warnings]
  GSC Enhancements: [X errors reported]
  Specific Errors: [List top errors and affected URLs]


------------------------------------------------------------------------------
IMPLEMENTATION PRIORITY
------------------------------------------------------------------------------

IMMEDIATE (This Week):
  1. [Fix NAP mismatches in existing schema]
  2. [Add LocalBusiness schema to homepage if missing]
  3. [Fix validation errors flagged by Google]

SHORT-TERM (Within 30 Days):
  4. [Add Service schema to all service pages]
  5. [Add FAQPage schema with local Q&A]
  6. [Implement BreadcrumbList across all pages]

ONGOING:
  7. [Update AggregateRating monthly]
  8. [Add FAQ schema as new Q&A content is created]
  9. [Validate schema after any page template changes]

==============================================================================
```

---

## Cross-References

| Skill | Relationship | When to Use Together |
|---|---|---|
| `/gbp-audit` | **Data source** — GBP hours, NAP, and categories from Phase 2 MUST match schema exactly. Any mismatch reduces trust in both data sources. | Always cross-reference GBP data when implementing or auditing schema. |
| `/technical-seo-local` | **Prerequisite** — Phase 9 confirms pages are crawlable and render properly. Schema on a noindexed or JS-blocked page is invisible to Google. | Run technical audit first to ensure schema will be parsed. |
| `/local-on-page-audit` | **Complementary** — On-page content (Phase 5) provides the unstructured text; schema provides the structured version. Both must align. | Schema should reflect the same services, hours, and NAP as the page content. |
| `/review-audit` | **Data source** — Review audit (Phase 3) provides the accurate review count and rating for AggregateRating schema. | Use review audit data to set accurate AggregateRating values. |
| `/local-citation-audit` | **Consistency check** — Citation NAP (Phase 4) should match schema NAP. Schema is the canonical structured representation of your business data. | Cross-reference citation NAP with schema NAP for consistency. |

---

*Phase 10 ensures your business data is machine-readable across all search channels. For the content that surrounds this schema, see `/local-on-page-audit` (Phase 5). For the link profile that amplifies schema-enhanced pages, proceed to `/local-link-audit` (Phase 11).*
