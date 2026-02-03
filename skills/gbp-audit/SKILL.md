---
name: gbp-audit
description: Comprehensive Google Business Profile audit with three-tier scoring and Openness signal analysis
version: 1.0.0
tags: [local-seo, gbp, google-business-profile, map-pack, audit]
related: [discovery-intake, review-audit, local-citation-audit, local-schema-markup, map-pack-analysis]
---

# Phase 2: Google Business Profile Audit (FLAGSHIP)

> **This is the single most impactful skill in the Local SEO Auditor suite.** Google Business Profile signals are the dominant factor in Local Map Pack rankings, carrying more weight than any other individual signal category. A properly optimized GBP listing is the foundation upon which all other local SEO efforts build. Without it, no amount of citation work, on-page optimization, or review generation will compensate.

---

## When to Use This Skill

- **As part of the full Local SEO Audit**: Run this as Phase 2, immediately after completing the Discovery Intake (Phase 1). The discovery brief provides the business context, target keywords, and competitor identification needed for a thorough GBP audit.
- **As a standalone audit**: This skill can be run independently when a client specifically needs GBP optimization guidance, when diagnosing a sudden drop in Map Pack visibility, or when onboarding a new local SEO client and you need a quick-win assessment.
- **Trigger scenarios**:
  - Client reports declining Map Pack visibility or call volume
  - New client onboarding where GBP has never been professionally optimized
  - Post-suspension recovery (after a GBP listing has been reinstated)
  - Competitive audit to understand why competitors outrank in the local pack
  - Seasonal audit to adjust hours, posts, and photos ahead of peak season
  - Google algorithm update impact assessment for local search

---

## Channel Impact

GBP signals do not affect all search channels equally. Understanding where GBP optimization delivers the highest ROI helps prioritize effort and set client expectations.

| Channel        | Weight | Rationale                                                                 |
|----------------|--------|---------------------------------------------------------------------------|
| **Map Pack**   | **32%** | GBP is THE dominant ranking factor for Local Pack/Map Pack results. Category, proximity, hours, reviews, and completeness all feed directly into local pack algorithms. |
| **Organic**    | **7%**  | Minimal direct impact on traditional organic rankings. GBP data may influence Knowledge Panel display and brand SERP features, but organic rankings are driven primarily by on-page and link signals. |
| **AI Search**  | **12%** | Moderate impact, primarily schema-dependent. AI search engines (Google AI Overviews, ChatGPT search, Perplexity) pull structured business data from GBP when generating local recommendations. Well-structured GBP data increases the likelihood of AI citation. |

**Total weighted impact across all channels: ~17% of overall local search visibility.**

This means that GBP optimization alone can move the needle significantly, especially for businesses that are currently underperforming in the Map Pack.

---

## Prerequisites

Before beginning the GBP audit, ensure you have:

1. **Discovery Brief from Phase 1** (`/discovery-intake`)
   - Business name, address, phone (NAP)
   - Target keywords (primary + secondary)
   - Service area definition
   - Top 3-5 competitors identified
   - Industry vertical and business type (storefront vs. SAB)

2. **GBP Listing Access or URL**
   - Direct URL to the Google Business Profile listing
   - OR the ability to search for and locate the listing in Google Maps
   - If the business has multiple locations, identify which location(s) to audit

3. **Competitor GBP Listings**
   - URLs or search queries to locate the top 3 competitor GBP profiles
   - These are needed for the comparative analysis framework

4. **Optional but Recommended**
   - GBP Insights data export (impressions, searches, actions) for the last 6 months
   - Current photo inventory from the GBP dashboard
   - Access to the GBP management dashboard for real-time verification

---

## Assessment Framework

The GBP audit uses a three-tier assessment framework. Tiers are weighted by their empirical impact on Map Pack ranking performance, based on industry correlation studies and Google's own documentation.

---

### TIER 1 --- Critical (70% of GBP ranking impact)

Tier 1 elements are non-negotiable. A failure in any Tier 1 element can result in complete exclusion from the Map Pack, listing suspension, or severe ranking penalties. These must be addressed before ANY Tier 2 or Tier 3 optimization work begins.

---

#### 1.1 Business Name Compliance (August 2025 Enforcement)

**Why This Matters**: Google began actively enforcing its business name guidelines in August 2025. Prior to this enforcement wave, many businesses added keywords to their GBP business name (a practice known as "keyword stuffing the business name") to gain a ranking advantage. Google now penalizes this with suspensions, ranking suppression, and forced name corrections.

**The Rule**: Your GBP business name MUST match your legal/DBA business name exactly. No additional keywords, service descriptors, location modifiers, or marketing language.

**Compliant Examples**:
| Legal Business Name | GBP Name (Correct) |
|---|---|
| ABC Plumbing LLC | ABC Plumbing |
| Smith & Sons HVAC | Smith & Sons HVAC |
| Maria's Bakery Inc. | Maria's Bakery |
| TechPro Solutions | TechPro Solutions |

**Non-Compliant Examples (VIOLATIONS)**:
| Legal Business Name | GBP Name (Violation) | Issue |
|---|---|---|
| ABC Plumbing LLC | ABC Plumbing - Drain Cleaning, Repair & Service | Keyword stuffing with services |
| Smith & Sons HVAC | Smith & Sons HVAC - #1 Rated in Dallas | Marketing language + city name |
| Maria's Bakery Inc. | Maria's Bakery - Wedding Cakes & Custom Pastries | Service descriptors added |
| TechPro Solutions | TechPro Solutions - IT Support, Managed Services, Cybersecurity | Multiple keyword additions |

**Audit Steps**:
1. Search for the business in Google Maps by its known name
2. Compare the displayed GBP name against the legal/DBA name (check state business registration, website footer, or business cards)
3. Check if any keywords, service terms, or location names have been appended
4. Check competitor names for violations (document these --- can be reported)
5. If the client's name contains a legitimate keyword (e.g., "Dallas Plumbing" is the actual legal name), verify with documentation (articles of incorporation, DBA filing)

**Penalty**: Listings can be suspended immediately. Suspension recovery takes 2-8 weeks and requires proof of legal business name. During suspension, the business is completely invisible in local search.

**Scoring**:
- 0 points: Business name contains keyword stuffing or does not match legal name
- 15 points: Business name exactly matches legal/DBA name

---

#### 1.2 Business Hours & "Openness" Signal (CRITICAL FILTER)

**Why This Matters**: The "Openness" signal has evolved from a minor ranking factor to a CRITICAL FILTER in Google's local algorithm. This is arguably the most underappreciated signal change in recent local search history.

**How the Openness Filter Works**:

For **immediate-need queries** (queries where the user needs a service RIGHT NOW), Google does not merely demote closed businesses --- it **FILTERS THEM OUT ENTIRELY** from the results. This applies to queries like:
- "emergency plumber near me"
- "AC repair now"
- "24 hour locksmith"
- "dentist open today"
- "restaurant open now"
- "urgent care near me"

The mechanism is real-time: Google checks the business's stated hours against the current time in the business's timezone. If the business is listed as closed at the moment of the search, it will not appear in the local pack for immediate-need queries.

**Beyond Immediate-Need**: Even for non-urgent queries, Google shows an "Open" or "Closed" badge prominently in the local pack. Businesses showing "Closed" receive significantly fewer clicks, even if they rank in the top 3.

**Audit Steps**:

1. **Verify Current Display**: Search for the business on Google Maps RIGHT NOW. What hours does Google show? Are they marked as Open or Closed at this moment? Do the displayed hours match reality?

2. **Accuracy Check**: Compare GBP hours against:
   - The business's actual operating hours (ask the client directly)
   - Hours displayed on the business website
   - Hours on Yelp, Facebook, and other directories
   - Any signage visible in Google Street View

3. **Competitive Window Analysis**: This is a significant competitive intelligence opportunity.
   - Pull the hours for the top 3 competitors in the target market
   - Identify time windows where the client is open but competitors are closed
   - These windows represent periods of dramatically reduced competition
   - Example: If competitors close at 5 PM but the client is open until 7 PM, the 5-7 PM window has far less competition in the local pack
   - Weekend and holiday hours are especially important for many service industries

4. **Special Hours & Exceptions**:
   - Are holiday hours set for upcoming holidays?
   - Are seasonal hours properly configured (e.g., extended summer hours)?
   - Are "More hours" used for specific service types (e.g., "Delivery hours", "Drive-through hours")?

5. **Emergency/24-7 Hours**:
   - If the business offers emergency or after-hours service, is this reflected in GBP?
   - Businesses that show 24/7 availability will appear in ALL "emergency" and "now" queries
   - However, hours MUST be accurate --- if you list 24/7 but don't answer the phone at 3 AM, negative reviews and Google penalties will follow

**Impact Data**:
- Businesses with accurate, extended hours see **+15% clicks** during off-peak hours compared to those with inaccurate hours
- During competitor-closed windows, businesses with accurate "Open" status see **+40% call volume** increases
- Businesses showing "Closed" in the local pack receive **60-70% fewer clicks** than those showing "Open", even when both appear in the same pack
- Incorrect hours leading to a customer arriving at a closed business is the #1 driver of 1-star "wasted my time" reviews

**Seasonal Hours Considerations**:
- HVAC companies: Extended hours during extreme weather seasons
- Tax preparers: Extended hours during tax season (Jan-April)
- Retail: Extended hours during holiday shopping season
- Restaurants: Adjusted hours for summer/winter, holidays
- Set these PROACTIVELY, at least 2 weeks before the season begins

**Scoring**:
- 0 points: Hours are clearly inaccurate, missing, or not set
- 5 points: Hours are set but have minor inaccuracies or no special hours configured
- 10 points: Hours are accurate but no competitive analysis or seasonal optimization
- 15 points: Hours are fully accurate, special/holiday hours set, competitive windows identified and leveraged

---

#### 1.3 Primary Category Selection (Strict Filter)

**Why This Matters**: The primary category is now a STRICT FILTER in Google's local algorithm. If your primary category does not match the user's query intent, you will NOT appear in the local pack for that query --- regardless of how well-optimized every other element is.

**The Rule**: Your primary category must be the MOST SPECIFIC category that accurately describes your core business. Google offers hundreds of categories, and choosing a broad category when a specific one exists is a critical mistake.

**Common Category Mistakes by Industry**:

| Industry | Wrong Category (Too Broad) | Correct Category (Specific) |
|---|---|---|
| Plumbing | Home Improvement | Plumber |
| HVAC | Contractor | HVAC Contractor |
| Electrician | Contractor | Electrician |
| Personal Injury Law | Lawyer | Personal Injury Attorney |
| Orthodontics | Dentist | Orthodontist |
| Thai Restaurant | Restaurant | Thai Restaurant |
| Dog Grooming | Pet Store | Dog Groomer |
| Tax Preparation | Accountant | Tax Preparation Service |
| Roof Repair | Contractor | Roofing Contractor |
| Auto Body | Car Repair | Auto Body Shop |

**Audit Steps**:

1. **Check Current Category**: View the GBP listing and note the displayed primary category
2. **Keyword-Category Alignment Test**: Search each of the client's target keywords on Google Maps. For the top 3 results in each query:
   - What primary category do they use?
   - Is there a consistent category pattern among top rankers?
3. **Category Specificity Check**: Search Google's category list for more specific alternatives to the current category. Use the GMB category tool or search the Google Business Profile category database.
4. **Multi-Service Businesses**: If the business offers multiple services (e.g., plumbing AND HVAC), the primary category should match the highest-revenue or highest-priority service line. Secondary categories handle the rest.

**Scoring**:
- 0 points: Primary category is wrong, too broad, or does not match target keywords
- 8 points: Primary category is reasonable but a more specific option exists
- 15 points: Primary category is the most specific, accurate match and aligns with top-ranking competitors

---

#### 1.4 Address Verification

**Why This Matters**: Google uses the business address to calculate proximity to the searcher, which is one of the top 3 local ranking factors (alongside relevance and prominence). An inaccurate, inconsistent, or ineligible address undermines both proximity signals and trust signals.

**Requirements**:
- **Storefront businesses**: Must have a physical location where customers visit. The address must be the actual location, not a virtual office, mailbox service, or co-working space.
- **Service-Area Businesses (SAB)**: Must have a real address (can be a home address) but should HIDE the address in GBP and instead define service areas. The address still matters for proximity calculations even when hidden.
- **PO Boxes and Virtual Offices**: NOT allowed. Google actively detects and penalizes these. UPS Store addresses (Suite ###) are particularly flagged.

**Audit Steps**:
1. Verify the GBP address matches the physical location (cross-reference with Google Street View)
2. Check NAP consistency: Does this exact address format appear on the website, Yelp, Facebook, BBB, and other directories?
3. For SABs: Confirm the address is hidden in GBP and service areas are properly set
4. Check for address format inconsistencies (e.g., "Street" vs "St.", "Suite" vs "#", "Avenue" vs "Ave.")
5. Verify the map pin is placed correctly on the actual business location (misplaced pins are common and hurt proximity calculations)

**Scoring**:
- 0 points: Address is a virtual office, PO box, or clearly inaccurate
- 5 points: Address is real but has NAP inconsistencies across platforms or map pin is misplaced
- 10 points: Address is accurate, consistent across platforms, and map pin is correctly placed

---

#### 1.5 Phone Number

**Why This Matters**: The phone number is a core component of NAP (Name, Address, Phone) consistency, and it serves as the primary conversion action for most local businesses. An inconsistent or non-functional phone number damages both ranking signals and conversion rates.

**Requirements and Best Practices**:

- **Active and Working**: The number must ring through to the business. Test it during and outside business hours.
- **Consistent Across Platforms**: The exact same number must appear on the website, GBP, Yelp, Facebook, BBB, and all other directories.
- **Local Number Preferred**: A local area code sends a stronger local signal than a toll-free (800) number. If the business uses both, the local number should be the primary GBP number.
- **Call Tracking Numbers**: This is a nuanced topic.
  - **Risk**: Using a call tracking number as the primary GBP number can create NAP inconsistency if the tracking number differs from what's on the website and other directories.
  - **Best Practice**: If call tracking is required, use the same tracking number consistently across ALL platforms, or use Google's built-in call tracking in GBP (if available in your region).
  - **Never** swap tracking numbers frequently --- each change creates a new NAP citation issue.

**Audit Steps**:
1. Call the GBP phone number and verify it connects to the business
2. Compare the GBP number against the website, Yelp, Facebook, and top 5 directory listings
3. Check if it's a local or toll-free number
4. If a call tracking number is used, verify it's consistent across all platforms
5. Test after-hours call handling (voicemail, answering service, or emergency routing)

**Scoring**:
- 0 points: Phone number is disconnected, wrong, or reaches a different business
- 5 points: Phone works but has inconsistencies across platforms or uses toll-free only
- 10 points: Phone is active, consistent across all platforms, uses local area code

---

#### 1.6 Verification Status

**Why This Matters**: An unverified GBP listing has severely limited visibility in search results. Google restricts unverified listings from appearing in the local pack and limits many profile features. Verification is the absolute minimum requirement for any GBP strategy.

**Audit Steps**:
1. Check the GBP dashboard for verification status
2. If verified, check when verification was completed and whether re-verification is pending
3. If unverified, determine the fastest verification path (postcard, phone, email, video, or instant verification)
4. Check for any active suspensions or policy violations that may have revoked verification

**Scoring**:
- 0 points: Listing is unverified or suspended
- 5 points: Listing is fully verified with no pending issues

---

### TIER 2 --- High Priority (20% of GBP ranking impact)

Tier 2 elements significantly enhance GBP performance but will not cause catastrophic failure if imperfect. These should be optimized after all Tier 1 elements are confirmed as compliant.

---

#### 2.1 Business Description

**Why This Matters**: The GBP description appears in the Knowledge Panel and provides Google with additional context about the business. While it is not a direct ranking factor for the local pack, it influences click-through rates and can help Google understand service relevance.

**Optimization Guidelines**:
- **Length**: 120-160 characters for the critical first portion (what displays before "More"). Full description can be up to 750 characters.
- **Keyword Placement**: Include 1-2 primary keywords naturally in the first sentence. Do NOT keyword stuff.
- **Location Signal**: Mention the primary city/service area.
- **Structure**: Lead with what you do, then where, then why choose you.

**Template**:
```
[Primary Service] serving [City/Region]. [Value Proposition]. [Differentiator or Call-to-Action].
```

**Industry Examples**:

| Industry | Example Description |
|---|---|
| Plumber | "Full-service plumbing company serving the Dallas-Fort Worth metroplex. Licensed, insured, and available for emergency repairs 24/7. Family-owned since 1998 with over 2,000 5-star reviews." |
| Dentist | "Comprehensive family dentistry in downtown Austin. Offering preventive care, cosmetic procedures, and emergency dental services. New patients welcome, same-day appointments available." |
| Restaurant | "Authentic Thai cuisine in the heart of Portland's Pearl District. Fresh ingredients, traditional recipes, and a modern dining experience. Dine-in, takeout, and catering available." |
| Attorney | "Experienced personal injury attorneys serving Houston and surrounding areas. Free consultations, no fees unless we win. Over $500M recovered for our clients." |
| HVAC | "Trusted heating and cooling services in Phoenix, AZ. AC repair, installation, and maintenance with same-day service. Licensed, bonded, and insured with 25+ years of experience." |

**Common Mistakes**:
- Starting with "We are..." or "Welcome to..." (wastes valuable character space)
- Keyword stuffing: "plumber plumbing plumb pipe pipes drain drains..."
- Including URLs, phone numbers, or promotional pricing (against Google's guidelines)
- Copying the same description across multiple locations (duplicate content)

**Scoring**:
- 0 points: No description set, or description violates Google's guidelines
- 2 points: Description exists but is generic, too short, or lacks keywords/location
- 4 points: Description is well-written with keywords and location but could be improved
- 5 points: Description is optimized, compelling, includes keywords and location naturally, and follows the template

---

#### 2.2 Photos Audit

**Why This Matters**: Google's own data shows that businesses with photos receive 42% more requests for driving directions and 35% more click-throughs to their websites than businesses without photos. Photos are also a significant trust signal for potential customers evaluating the business.

**Quantity Benchmarks**:
- **Minimum**: 15 photos (below this, the profile appears incomplete)
- **Target**: 20-25 photos (optimal range for most businesses)
- **Maximum Useful**: 30-40 photos (beyond this, diminishing returns unless highly relevant)

**Required Photo Categories**:

| Category | Target Count | Purpose |
|---|---|---|
| Team/Staff Photos | 5-7 | Builds trust and personal connection. Show real employees in uniform or at work. |
| Company Vehicles/Equipment | 3-4 | Signals legitimacy and professionalism. Branded vehicles are especially valuable. |
| Before/After Projects | 5-8 | Demonstrates capability and quality of work. Most impactful for contractors, landscapers, home services. |
| Office/Storefront/Signage | 2-3 | Helps customers recognize the location. Exterior shots help with wayfinding. |
| Certificates/Licenses | 2-3 | Trust signals. State licenses, industry certifications, awards, BBB accreditation. |

**Quality Standards**:
- Resolution: Minimum 720px width, recommended 1200px+ width
- Lighting: Well-lit, natural or professional lighting. No dark, blurry, or poorly composed images.
- Orientation: Landscape preferred for most categories; square for team headshots
- Authenticity: NEVER use stock photos. Google can detect stock images and they damage trust.
- Relevance: Every photo should be directly related to the business, its services, or its team.

**Photo Optimization**:
- **Geo-tagging**: Photos should have EXIF location data matching the business address (most smartphone photos include this automatically)
- **File naming**: Use descriptive file names before upload (e.g., `dallas-emergency-plumber-team.jpg` not `IMG_4521.jpg`)
- **Captions**: Add descriptive captions that include the service and location when Google's interface allows
- **Freshness**: Upload new photos at least monthly. Google favors profiles with recent photo activity. A profile with 25 photos all uploaded 3 years ago is less impressive than one with 20 photos uploaded over the past 6 months.

**Photo Audit Checklist**:
1. Count total photos currently on the profile
2. Categorize existing photos by type (team, projects, office, etc.)
3. Identify missing categories
4. Assess quality of existing photos (resolution, lighting, composition)
5. Check for stock photos that need to be replaced
6. Review photo upload dates (are they recent or stale?)
7. Check for inappropriate or irrelevant photos uploaded by the public
8. Verify cover photo and logo are set and high-quality

**Scoring**:
- 0 points: 0-4 photos on the profile
- 1 point: 5-9 photos
- 2 points: 10-14 photos
- 3 points: 15-19 photos
- 4 points: 20-24 photos
- 5 points: 25+ photos with good category coverage, quality, and freshness

---

#### 2.3 Secondary Categories

**Why This Matters**: While the primary category acts as a strict filter for your most important queries, secondary categories expand the range of queries for which your listing can appear. They tell Google about the full scope of services you offer.

**Guidelines**:
- Select 5-10 most relevant secondary categories
- Each category should represent a genuine service the business provides
- Do NOT add irrelevant categories --- this dilutes relevance signals and can trigger a Google review
- Prioritize categories that match your secondary target keywords

**Industry Examples**:

| Business Type | Primary Category | Recommended Secondary Categories |
|---|---|---|
| Plumber | Plumber | Water Heater Repair Service, Drain Cleaning Service, Gas Installation Service, Bathroom Remodeler, Water Damage Restoration Service |
| HVAC | HVAC Contractor | Air Conditioning Contractor, Heating Contractor, Furnace Repair Service, Air Duct Cleaning Service, Ventilation Equipment Supplier |
| Electrician | Electrician | Lighting Contractor, Electrical Installation Service, Generator Installation Service, Solar Energy Contractor |
| Dentist | Dentist | Cosmetic Dentist, Pediatric Dentist, Emergency Dental Service, Dental Implants Provider, Teeth Whitening Service |
| Restaurant | Thai Restaurant | Asian Restaurant, Catering Service, Takeout Restaurant, Delivery Restaurant |
| Attorney | Personal Injury Attorney | Accident Attorney, Car Accident Lawyer, Workers' Compensation Attorney, Medical Malpractice Lawyer |

**Audit Steps**:
1. List all current secondary categories
2. Search each target keyword and note what secondary categories top competitors use
3. Identify missing categories that are relevant to the business
4. Flag any irrelevant categories that should be removed
5. Prioritize additions based on search volume of related keywords

**Scoring**:
- 0 points: No secondary categories set
- 2 points: 1-3 secondary categories, some relevant
- 4 points: 4-7 relevant secondary categories
- 5 points: 5-10 well-chosen secondary categories aligned with target keywords and competitor analysis

---

#### 2.4 Website Link

**Why This Matters**: The website link in GBP drives traffic and serves as a trust and relevance signal. Google crawls the linked page to verify business information consistency.

**Requirements**:
- Must use HTTPS (HTTP-only sites are flagged as "Not Secure" and receive trust penalties)
- Must load quickly (under 3 seconds on mobile)
- Must be functional (no 404 errors, redirect loops, or broken pages)
- Should link to the homepage OR a location-specific landing page (for multi-location businesses)

**Best Practices**:
- Add UTM parameters for tracking: `?utm_source=google&utm_medium=organic&utm_campaign=gbp`
- Ensure the linked page contains matching NAP information
- Page should be mobile-responsive (over 60% of local searches are on mobile)
- Page should include LocalBusiness schema markup (cross-reference with `/local-schema-markup`)

**Scoring**:
- 0 points: No website link, broken link, or HTTP-only site
- 2 points: Working HTTPS link but page has issues (slow, not mobile-friendly, no NAP)
- 3 points: Working HTTPS link to a fast, mobile-friendly page with consistent NAP and tracking parameters

---

### TIER 3 --- Optimization (10% of GBP ranking impact)

Tier 3 elements provide incremental ranking and conversion improvements. They are the "polish" that separates good GBP profiles from great ones. Address these after Tiers 1 and 2 are fully optimized.

---

#### 3.1 Google Posts (UPDATED: 2-3 per week)

**Why This Matters**: Google Posts signal that a business is active and engaged. They appear in the Knowledge Panel and can influence click-through rates. Google has increased the weight of post activity in recent algorithm updates.

**Updated Frequency Recommendation**:
- **Previous recommendation**: 1 post per week
- **Current recommendation**: 2-3 posts per week
- **Impact data**:
  - 1 post/week: ~30% engagement increase over no posts
  - 2-3 posts/week: ~45-50% estimated engagement increase over no posts
  - Daily posting: Marginal additional benefit with significantly more effort (not recommended for most businesses)

**Post Types Rotation**:

Rotate through these post types to maintain variety and cover different engagement angles:

| Post Type | Frequency | Purpose |
|---|---|---|
| Service Highlight | 1x/week | Showcase a specific service, explain benefits, include before/after |
| Seasonal Tip | 1x/week (seasonal) | Timely advice related to season (e.g., "Winterize your pipes" for plumbers in November) |
| Customer Testimonial | 1-2x/month | Share a positive review with permission, adds social proof |
| Offer/Promotion | 1-2x/month | Special pricing, seasonal discount, first-time customer offer |
| Educational | 1-2x/month | Tips, how-to advice, industry insights (positions as authority) |
| Company News | 1x/month | Awards, new team members, community involvement, certifications |

**Post Structure Template**:

```
HEADLINE: [15-20 characters, benefit-focused]
Example: "Save on AC Repair" or "Same-Day Service"

DESCRIPTION: [Up to 300 characters, 1-2 local keywords + clear CTA]
Example: "Beat the Dallas heat with our $49 AC diagnostic special.
Licensed technicians, same-day availability. Book your appointment
today and stay comfortable all summer."

IMAGE: High-quality, professional photo (not stock). Rotate images
across posts. Minimum 400x300px, recommended 1200x900px.

CTA BUTTON: Choose the most relevant:
- "Call now" (for service businesses)
- "Learn more" (for informational posts)
- "Book" (for appointment-based businesses)
- "Order online" (for restaurants/retail)
- "Get offer" (for promotions)

LINK: To relevant landing page (NOT always the homepage).
Match the post topic to the landing page.
```

**2-Week Post Rotation Calendar Example**:

| Day | Week 1 | Week 2 |
|---|---|---|
| Monday | Service Highlight: Drain Cleaning | Educational: 5 Signs You Need a Plumber |
| Wednesday | Seasonal Tip: Winter Pipe Protection | Customer Testimonial: Johnson Family Review |
| Friday | Offer: $50 Off First Service | Service Highlight: Water Heater Installation |

**Scoring**:
- 0 points: No posts in the last 30 days
- 1 point: 1 post per week average over the last month
- 2 points: 2 posts per week average over the last month
- 3 points: 3+ posts per week with good variety, quality images, and CTAs

---

#### 3.2 Q&A Section

**Why This Matters**: The Q&A section appears prominently in the GBP Knowledge Panel and in Google Maps. Unanswered questions create a poor impression, and competitor-planted negative questions can damage trust. Proactively managing this section is both a defensive and offensive strategy.

**Audit Steps**:
1. Review all existing questions and answers
2. Check for unanswered questions (must be answered within 48 hours)
3. Look for potentially malicious or competitor-planted questions
4. Check if the business owner has proactively seeded common Q&A

**Proactive Q&A Strategy**:
- Seed 5-10 commonly asked questions with well-crafted answers
- Include keywords naturally in both questions and answers
- Cover topics: pricing ranges, service areas, hours, emergency availability, licensing, warranty/guarantees
- Example seeded Q&A:
  - Q: "Do you offer emergency plumbing service in Dallas?" A: "Yes, we provide 24/7 emergency plumbing service throughout the Dallas-Fort Worth area. Call us anytime and a licensed plumber will be dispatched within 60 minutes."
  - Q: "Are you licensed and insured?" A: "Yes, ABC Plumbing is fully licensed (TX License #12345), bonded, and insured. All our technicians are background-checked and factory-trained."

**Scoring**:
- 0 points: Multiple unanswered questions, no proactive Q&A
- 1 point: All questions answered but no proactive seeding
- 2 points: All questions answered promptly, 5+ proactively seeded Q&A with keywords

---

#### 3.3 Attributes

**Why This Matters**: GBP attributes provide structured data about business characteristics that Google uses for filtering and matching. They also display as badges in the listing, building trust with potential customers.

**Key Attributes to Complete**:

| Attribute Category | Examples |
|---|---|
| Credentials | Licensed, Insured, Bonded, Certified |
| Service Options | Offers warranties, Free estimates, Emergency service available |
| Accessibility | Wheelchair accessible, Wheelchair accessible restroom, Wheelchair accessible parking |
| Payments | Accepts credit cards, Accepts cash, Financing available |
| Identity | Veteran-owned, Women-owned, Black-owned, LGBTQ+ friendly |
| Health & Safety | Mask required, Temperature check required (if applicable) |
| Amenities | Wi-Fi, Restroom, Parking (for storefront businesses) |

**Audit Steps**:
1. Review all currently set attributes
2. Identify all applicable attributes that are not yet set
3. Prioritize trust-building attributes (Licensed, Insured, Warranties)
4. Set all accessibility attributes accurately
5. Compare attributes to top competitors

**Scoring**:
- 0 points: No attributes set
- 1 point: Some attributes set but major gaps
- 2 points: All applicable attributes completed, including trust and accessibility attributes

---

#### 3.4 Service Areas (SAB only)

**Why This Matters**: For Service-Area Businesses that travel to customers (plumbers, electricians, HVAC, landscapers, etc.), service areas replace the address as the geographic signal. Properly configured service areas tell Google exactly where to show your listing.

**Guidelines**:
- Set areas that accurately reflect where you actually provide service
- Do NOT over-extend your service area --- this dilutes proximity signals. A plumber claiming to serve an entire state will rank poorly in any specific city.
- Use city/town names rather than zip codes when possible (Google's system handles cities better)
- Maximum: 20 service areas recommended
- Ideal: Focus on the 5-10 cities/areas where you want to rank most strongly

**Audit Steps**:
1. Review currently set service areas
2. Compare against actual service delivery area (ask the client where they realistically serve)
3. Check if the areas are too broad (entire metro area vs. specific cities)
4. Verify that primary target cities are included
5. Remove areas where the business does not actually provide service

**Scoring**:
- 0 points: No service areas set (for SAB businesses)
- 0.5 points: Service areas set but too broad or inaccurate
- 1 point: Service areas accurately reflect actual service delivery area, focused on priority cities

---

#### 3.5 Products/Services Feature

**Why This Matters**: The Products and Services sections in GBP provide additional structured data and keyword opportunities. They appear in the Knowledge Panel and help Google understand the full scope of what you offer.

**Best Practices**:
- List ALL services the business provides
- Write unique descriptions for each (50-150 words)
- Include pricing ranges where possible (Google favors transparent pricing)
- Link each service to the relevant page on the website
- Organize services into logical categories
- Include relevant keywords naturally in service names and descriptions

**Audit Steps**:
1. List all services currently in GBP
2. Compare against the full list of services from the website
3. Check if descriptions are unique and keyword-optimized
4. Verify pricing information is current
5. Confirm links point to relevant (and functional) landing pages

**Scoring**:
- 0 points: No services/products listed
- 1 point: Some services listed with basic descriptions
- 2 points: Comprehensive service list with optimized descriptions, pricing, and links to relevant pages

---

## Scoring Rubric

```
==============================================================
            GBP HEALTH SCORE CALCULATION
==============================================================

TIER 1 --- CRITICAL (70 points max)
--------------------------------------------------------------
  Business Name Compliance:     ___/15  (0 = violation, 15 = compliant)
  Hours Accuracy + Openness:    ___/15  (0-5-10-15 scale)
  Primary Category:             ___/15  (0 = wrong, 8 = OK, 15 = optimal)
  Address Verification:         ___/10  (0 = ineligible, 5 = inconsistent, 10 = perfect)
  Phone Number:                 ___/10  (0 = broken, 5 = inconsistent, 10 = perfect)
  Verification Status:          ___/ 5  (0 = unverified, 5 = verified)
                                ------
  TIER 1 SUBTOTAL:              ___/70


TIER 2 --- HIGH PRIORITY (20 points max)
--------------------------------------------------------------
  Business Description:         ___/ 5  (0-2-4-5 scale)
  Photos:                       ___/ 5  (0-4=0, 5-9=1, 10-14=2,
                                         15-19=3, 20-24=4, 25+=5)
  Secondary Categories:         ___/ 5  (0-2-4-5 scale)
  Website Link:                 ___/ 3  (0-2-3 scale)
  [Reserved]:                   ___/ 2
                                ------
  TIER 2 SUBTOTAL:              ___/20


TIER 3 --- OPTIMIZATION (10 points max)
--------------------------------------------------------------
  Google Posts:                  ___/ 3  (0/wk=0, 1/wk=1, 2/wk=2, 3+/wk=3)
  Q&A Section:                  ___/ 2  (0-1-2 scale)
  Attributes:                   ___/ 2  (0-1-2 scale)
  Services/Products:            ___/ 2  (0-1-2 scale)
  Service Areas (SAB only):     ___/ 1  (0-0.5-1 scale)
                                ------
  TIER 3 SUBTOTAL:              ___/10


==============================================================
  GBP HEALTH SCORE TOTAL:       ___/100
==============================================================

SCORE INTERPRETATION:
  90-100:  Excellent - GBP is fully optimized, focus on maintenance
  75-89:   Good - Minor optimizations needed, strong foundation
  50-74:   Needs Work - Significant gaps in Tier 1 or Tier 2
  25-49:   Poor - Critical issues present, immediate action required
  0-24:    Critical - Major compliance or verification failures
==============================================================
```

---

## DFS MCP Data Sources

Use the following DataForSEO MCP tools to gather competitive intelligence and verify GBP data programmatically.

### Tool 1: SERP Analysis for Local Pack Verification

```
TOOL: mcp__dfs-mcp__serp_organic_live_advanced
USE:  Search target keywords with local parameters to see GBP listing
      in SERP results. Verify local pack presence and positioning.
PARAMETERS:
  - keyword: Target keyword (e.g., "plumber near me", "emergency AC repair")
  - location_code: City/region code (e.g., 1023191 for Dallas, TX)
  - language_code: "en" (or target language)
  - device: "mobile" (preferred for local — most local searches are mobile)
  - os: "android" (optional, for mobile simulation)
```

### Tool 2: Business Listing Verification

```
TOOL: mcp__dfs-mcp__business_data_business_listings_search
USE:  Search for business listings to verify NAP data, find competitor
      GBP information, and assess listing completeness across platforms.
```

### Python Fallback: DataForSEO API Direct Calls

If the MCP tools are unavailable or you need more granular control, use these Python scripts to call the DataForSEO API directly.

**SERP Analysis (Local Pack)**:
```python
import requests
import json
import base64

# DataForSEO API credentials
DFS_LOGIN = "your_login"
DFS_PASSWORD = "your_password"
DFS_AUTH = base64.b64encode(f"{DFS_LOGIN}:{DFS_PASSWORD}".encode()).decode()

def get_local_serp(keyword: str, location_code: int, language_code: str = "en", device: str = "mobile"):
    """
    Fetch SERP results with local pack data for a given keyword and location.

    Args:
        keyword: Search query (e.g., "plumber near me")
        location_code: DataForSEO location code (e.g., 1023191 for Dallas, TX)
        language_code: Language code (default "en")
        device: "mobile" or "desktop" (mobile preferred for local)

    Returns:
        dict: SERP results including local pack items
    """
    url = "https://api.dataforseo.com/v3/serp/google/organic/live/advanced"

    headers = {
        "Authorization": f"Basic {DFS_AUTH}",
        "Content-Type": "application/json"
    }

    payload = [{
        "keyword": keyword,
        "location_code": location_code,
        "language_code": language_code,
        "device": device,
        "os": "android" if device == "mobile" else None,
        "calculate_rectangles": True
    }]

    response = requests.post(url, headers=headers, json=payload)
    result = response.json()

    if result.get("status_code") == 20000:
        tasks = result.get("tasks", [])
        if tasks and tasks[0].get("result"):
            items = tasks[0]["result"][0].get("items", [])

            # Filter for local pack results
            local_pack = [item for item in items if item.get("type") == "local_pack"]
            organic = [item for item in items if item.get("type") == "organic"]

            return {
                "local_pack": local_pack,
                "organic": organic,
                "total_items": len(items)
            }

    return {"error": result.get("status_message", "Unknown error")}


def analyze_local_pack_competitors(keyword: str, location_code: int):
    """
    Analyze local pack results to extract competitor GBP data.

    Returns competitor categories, ratings, review counts, and other GBP signals.
    """
    serp_data = get_local_serp(keyword, location_code)

    if "error" in serp_data:
        return serp_data

    competitors = []
    for item in serp_data.get("local_pack", []):
        if "items" in item:
            for listing in item["items"]:
                competitors.append({
                    "title": listing.get("title"),
                    "category": listing.get("category"),
                    "rating": listing.get("rating"),
                    "review_count": listing.get("reviews_count"),
                    "address": listing.get("address"),
                    "phone": listing.get("phone"),
                    "url": listing.get("url"),
                    "position": listing.get("rank_absolute")
                })

    return competitors


# Example usage:
# competitors = analyze_local_pack_competitors("emergency plumber", 1023191)
# for comp in competitors:
#     print(f"{comp['title']} | Category: {comp['category']} | Rating: {comp['rating']} ({comp['review_count']} reviews)")
```

**Business Listing Search**:
```python
def search_business_listings(business_name: str, location_code: int):
    """
    Search for a business across listing platforms to verify NAP consistency.

    Args:
        business_name: Name of the business to search for
        location_code: DataForSEO location code

    Returns:
        dict: Business listing data including NAP information
    """
    url = "https://api.dataforseo.com/v3/business_data/business_listings/search/live"

    headers = {
        "Authorization": f"Basic {DFS_AUTH}",
        "Content-Type": "application/json"
    }

    payload = [{
        "keyword": business_name,
        "location_code": location_code,
        "language_code": "en",
        "limit": 10
    }]

    response = requests.post(url, headers=headers, json=payload)
    result = response.json()

    if result.get("status_code") == 20000:
        tasks = result.get("tasks", [])
        if tasks and tasks[0].get("result"):
            listings = tasks[0]["result"]
            return {
                "listings": listings,
                "count": len(listings)
            }

    return {"error": result.get("status_message", "Unknown error")}


def verify_nap_consistency(business_name: str, expected_address: str, expected_phone: str, location_code: int):
    """
    Check NAP consistency across discovered business listings.

    Returns a consistency report with match/mismatch details.
    """
    listings_data = search_business_listings(business_name, location_code)

    if "error" in listings_data:
        return listings_data

    consistency_report = {
        "total_listings": listings_data["count"],
        "name_matches": 0,
        "address_matches": 0,
        "phone_matches": 0,
        "inconsistencies": []
    }

    for listing in listings_data.get("listings", []):
        name_match = business_name.lower() in listing.get("title", "").lower()
        address_match = expected_address.lower() in listing.get("address", "").lower()
        phone_match = expected_phone.replace("-", "").replace(" ", "") in listing.get("phone", "").replace("-", "").replace(" ", "")

        if name_match:
            consistency_report["name_matches"] += 1
        if address_match:
            consistency_report["address_matches"] += 1
        if phone_match:
            consistency_report["phone_matches"] += 1

        if not (name_match and address_match and phone_match):
            consistency_report["inconsistencies"].append({
                "source": listing.get("source", "Unknown"),
                "found_name": listing.get("title"),
                "found_address": listing.get("address"),
                "found_phone": listing.get("phone"),
                "name_match": name_match,
                "address_match": address_match,
                "phone_match": phone_match
            })

    return consistency_report


# Example usage:
# report = verify_nap_consistency(
#     "ABC Plumbing",
#     "123 Main St, Dallas, TX 75201",
#     "214-555-1234",
#     1023191
# )
# print(f"NAP Consistency: {report['address_matches']}/{report['total_listings']} addresses match")
```

---

## User Data Requests

To complete the most thorough audit possible, request the following data from the client or business owner:

### Required Data:
1. **GBP Insights Export** (last 6 months minimum)
   - Search queries that triggered the listing
   - Total impressions (Search + Maps)
   - Actions: website clicks, direction requests, phone calls
   - Photo views vs. competitor average
   - Month-over-month trends

2. **Current GBP Photos**
   - Full list of uploaded photos with dates
   - Which photos are owner-uploaded vs. customer-uploaded
   - Cover photo and logo identification

3. **GBP Review Summary**
   - Total review count
   - Average star rating
   - Review velocity (reviews per month, trend)
   - Response rate and average response time
   - (Detailed review analysis is handled by `/review-audit`)

### Optional but Valuable:
- Google Analytics data for the GBP-linked landing page (traffic, bounce rate, conversions)
- Call tracking data if implemented (call volume, peak times, missed calls)
- Previous GBP audit reports or optimization work history
- List of all locations (for multi-location businesses)

---

## Competitive GBP Comparison

Use this framework to systematically compare the client's GBP profile against the top 3 competitors in their market. This comparison reveals specific gaps and opportunities.

### Comparison Matrix

```
==============================================================================
COMPETITIVE GBP COMPARISON
==============================================================================

Element              | [Client]    | [Comp 1]    | [Comp 2]    | [Comp 3]
---------------------|-------------|-------------|-------------|-------------
Primary Category     |             |             |             |
Secondary Categories |   /10       |   /10       |   /10       |   /10
Total Reviews        |             |             |             |
Average Rating       |   /5.0      |   /5.0      |   /5.0      |   /5.0
Review Velocity      |   /mo       |   /mo       |   /mo       |   /mo
Photo Count          |             |             |             |
Photo Quality        | Low/Med/Hi  | Low/Med/Hi  | Low/Med/Hi  | Low/Med/Hi
Posts Frequency      |   /wk       |   /wk       |   /wk       |   /wk
Business Hours       |             |             |             |
Extended Hours?      | Y/N         | Y/N         | Y/N         | Y/N
Weekend Hours?       | Y/N         | Y/N         | Y/N         | Y/N
Attributes Count     |             |             |             |
Description Quality  | Low/Med/Hi  | Low/Med/Hi  | Low/Med/Hi  | Low/Med/Hi
Q&A Count            |             |             |             |
Services Listed      | Y/N         | Y/N         | Y/N         | Y/N
Products Listed      | Y/N         | Y/N         | Y/N         | Y/N
Website HTTPS        | Y/N         | Y/N         | Y/N         | Y/N
Name Compliant       | Y/N         | Y/N         | Y/N         | Y/N
==============================================================================

KEY FINDINGS:
- [Client advantage 1]
- [Client advantage 2]
- [Competitor advantage to close gap on]
- [Biggest opportunity gap identified]
==============================================================================
```

### How to Use the Comparison:
1. Fill in data for the client and each competitor by reviewing their GBP listings in Google Maps
2. Highlight cells where the client is behind competitors (these are priority action items)
3. Highlight cells where the client leads (these are competitive advantages to maintain)
4. Focus action items on closing the largest gaps first
5. Report competitor name violations to Google if found (competitive tactic)

---

## Output Format

The GBP audit output should follow this exact structure for inclusion in the full Local SEO Audit Report.

```
==============================================================================
PHASE 2: GOOGLE BUSINESS PROFILE AUDIT
==============================================================================

Business: [Business Name]
GBP URL: [Google Maps URL]
Audit Date: [YYYY-MM-DD]
Auditor: Claude Code (Local SEO Auditor)

------------------------------------------------------------------------------
GBP HEALTH SCORE: [XX]/100 — [Excellent/Good/Needs Work/Poor/Critical]
------------------------------------------------------------------------------

TIER 1 — CRITICAL SIGNALS (Score: [XX]/70)
------------------------------------------------------------------------------

  [P] Business Name Compliance               [XX/15]
      Status: [Compliant / VIOLATION]
      Current Name: "[displayed name]"
      Legal Name: "[legal name]"
      Action: [None needed / Remove keyword stuffing immediately]

  [P] Hours & Openness Signal                [XX/15]
      Status: [Accurate / Needs Update / NOT SET]
      Current Hours: [Mon-Sun hours summary]
      Accuracy: [Verified accurate / Discrepancies found]
      Competitor Windows: [Time windows with competitive advantage]
      Special Hours: [Set / Not set]
      Action: [Specific recommendations]

  [P] Primary Category                       [XX/15]
      Current: [Category]
      Recommended: [Category if change needed]
      Competitor Categories: [Top 3 competitor categories]
      Action: [None / Change to X]

  [P] Address Verification                   [XX/10]
      Status: [Verified / Issues Found]
      NAP Consistency: [Consistent / X inconsistencies found]
      Map Pin: [Accurate / Misplaced]
      Action: [Specific recommendations]

  [P] Phone Number                           [XX/10]
      Number: [XXX-XXX-XXXX]
      Status: [Active / Issues Found]
      Consistency: [Consistent / X inconsistencies]
      Type: [Local / Toll-free / Tracking]
      Action: [Specific recommendations]

  [P] Verification Status                    [XX/5]
      Status: [Verified / Unverified / Suspended]
      Action: [None / Verify via X method]


TIER 2 — HIGH PRIORITY (Score: [XX]/20)
------------------------------------------------------------------------------

  [P] Business Description                   [XX/5]
      Current: "[first 100 chars...]"
      Keywords Present: [Y/N — list found keywords]
      Location Mentioned: [Y/N]
      Action: [Specific rewrite recommendation or "None needed"]

  [P] Photos                                 [XX/5]
      Total Count: [X]
      Breakdown: Team [X] | Projects [X] | Vehicles [X] |
                 Office [X] | Certs [X] | Other [X]
      Quality: [Low / Medium / High]
      Freshness: [Most recent upload date]
      Action: [Add X photos in Y categories]

  [P] Secondary Categories                   [XX/5]
      Current: [List all]
      Missing: [Recommended additions]
      Remove: [Irrelevant categories to remove]
      Action: [Specific additions/removals]

  [P] Website Link                           [XX/3]
      URL: [URL]
      HTTPS: [Y/N]
      Status: [Working / Broken]
      Mobile-Friendly: [Y/N]
      Action: [Specific recommendations]


TIER 3 — OPTIMIZATION (Score: [XX]/10)
------------------------------------------------------------------------------

  [P] Google Posts                            [XX/3]
      Last Post: [Date]
      Frequency: [X/week average over last month]
      Quality: [Low / Medium / High]
      Action: [Implement X/week posting schedule]

  [P] Q&A Section                            [XX/2]
      Total Questions: [X]
      Unanswered: [X]
      Proactive Q&A: [Y/N — count]
      Action: [Answer X questions, seed Y proactive Q&As]

  [P] Attributes                             [XX/2]
      Set: [X attributes]
      Missing: [List key missing attributes]
      Action: [Add X attributes]

  [P] Services/Products                      [XX/2]
      Services Listed: [X]
      Descriptions: [Complete / Incomplete / Missing]
      Pricing: [Included / Not included]
      Action: [Add/update X services]

  [P] Service Areas (SAB)                    [XX/1]
      Areas Set: [X]
      Coverage: [Appropriate / Too broad / Too narrow]
      Action: [Adjust to X areas]


------------------------------------------------------------------------------
COMPETITIVE COMPARISON SUMMARY
------------------------------------------------------------------------------
[Insert completed comparison matrix from above]


------------------------------------------------------------------------------
PRIORITY ACTION ITEMS (Ordered by Impact)
------------------------------------------------------------------------------

IMMEDIATE (This Week):
  1. [Highest-impact Tier 1 fix]
  2. [Second highest-impact fix]
  3. [Third fix]

SHORT-TERM (Within 30 Days):
  4. [Tier 2 optimization]
  5. [Tier 2 optimization]
  6. [Tier 2 optimization]

ONGOING (Monthly Maintenance):
  7. [Post schedule implementation]
  8. [Photo upload cadence]
  9. [Q&A monitoring]
  10. [Review response process — see /review-audit]


------------------------------------------------------------------------------
ESTIMATED IMPACT
------------------------------------------------------------------------------
Current GBP Score: [XX]/100
Projected Score (after immediate fixes): [XX]/100
Projected Score (after all fixes): [XX]/100
Expected Map Pack Impact: [Significant / Moderate / Incremental]

==============================================================================
```

---

## Cross-References

This skill connects to and is reinforced by the following related skills in the Local SEO Auditor suite:

| Skill | Relationship | When to Use Together |
|---|---|---|
| `/review-audit` | **Complementary** --- Review signals carry 20% of Map Pack weight. Reviews live on GBP but are audited separately due to their complexity and distinct optimization strategies. | Always run after GBP audit. Review velocity, rating, and response patterns directly affect GBP ranking. |
| `/local-citation-audit` | **Supporting** --- NAP consistency across citations is a trust signal that reinforces GBP data accuracy. Citation inconsistencies can prevent GBP from ranking even when fully optimized. | Run when GBP audit reveals NAP inconsistencies (address or phone mismatches). |
| `/local-schema-markup` | **Reinforcing** --- LocalBusiness schema on the website linked from GBP creates a structured data bridge. Google uses schema to verify and enhance GBP data. | Run after GBP audit to ensure the linked website's schema matches GBP data exactly. |
| `/map-pack-analysis` | **Diagnostic** --- Map Pack analysis examines the competitive landscape and ranking factors holistically. GBP signals are the largest single input to Map Pack rankings. | Run to understand why the client ranks where they do in the Map Pack and what specific GBP improvements will move the needle. |
| `/local-on-page-audit` | **Connected** --- The website linked from GBP must be optimized for local search. On-page local signals (city pages, NAP in footer, LocalBusiness schema) complement GBP optimization. | Run after GBP audit to ensure the linked website supports and reinforces GBP signals. |
| `/discovery-intake` | **Prerequisite** --- Discovery provides the business context, target keywords, competitor list, and service area definitions needed for a thorough GBP audit. | Always run before GBP audit unless conducting a quick standalone assessment. |

---

## Appendix: GBP Audit Quick Reference Checklist

For experienced auditors who need a rapid-fire checklist without the detailed explanations:

```
TIER 1 QUICK CHECK:
[ ] Business name = legal name only (no keywords)
[ ] Hours set, accurate, and matching actual availability
[ ] Holiday/special hours configured
[ ] Primary category is most specific match
[ ] Address is physical (not virtual/PO box)
[ ] Address format consistent across all platforms
[ ] Map pin correctly placed
[ ] Phone number active and consistent
[ ] Local area code (not toll-free)
[ ] Listing is verified, no pending issues

TIER 2 QUICK CHECK:
[ ] Description 120-160 chars, has keywords + location
[ ] 15+ photos across all categories
[ ] No stock photos
[ ] Photos uploaded in last 3 months
[ ] 5-10 relevant secondary categories
[ ] Website link is HTTPS, fast, mobile-friendly
[ ] UTM tracking on website link

TIER 3 QUICK CHECK:
[ ] 2-3 Google Posts per week
[ ] All Q&A answered, 5+ proactive Q&As seeded
[ ] All applicable attributes set
[ ] All services listed with descriptions
[ ] Service areas set accurately (SAB only)
```

---

*This is the flagship skill in the Local SEO Auditor suite. For the complete audit workflow, begin with `/discovery-intake` (Phase 1), then proceed through this GBP audit (Phase 2), followed by `/review-audit` (Phase 3), `/local-citation-audit` (Phase 4), `/local-on-page-audit` (Phase 5), `/local-schema-markup` (Phase 6), and `/map-pack-analysis` (Phase 7).*
