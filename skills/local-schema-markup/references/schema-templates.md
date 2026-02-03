# Local SEO Schema Templates — Ready-to-Use JSON-LD

## 1. LocalBusiness Schema (Homepage)

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "@id": "https://example.com/#business",
  "name": "ABC Plumbing",
  "image": "https://example.com/images/logo.png",
  "description": "Licensed plumber serving Denver. Emergency drain cleaning, water heater repair, and 24/7 availability.",
  "url": "https://example.com",
  "telephone": "+15550123456",
  "email": "info@example.com",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main Street",
    "addressLocality": "Denver",
    "addressRegion": "CO",
    "postalCode": "80203",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 39.7392,
    "longitude": -104.9903
  },
  "areaServed": [
    {
      "@type": "City",
      "name": "Denver",
      "sameAs": "https://en.wikipedia.org/wiki/Denver"
    },
    {
      "@type": "City",
      "name": "Aurora"
    },
    {
      "@type": "City",
      "name": "Littleton"
    }
  ],
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "07:00",
      "closes": "21:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Saturday"],
      "opens": "08:00",
      "closes": "17:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Sunday"],
      "opens": "09:00",
      "closes": "15:00"
    }
  ],
  "priceRange": "$$",
  "paymentAccepted": "Cash, Credit Card, Check",
  "currenciesAccepted": "USD",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "127",
    "bestRating": "5",
    "worstRating": "1"
  },
  "sameAs": [
    "https://www.facebook.com/abcplumbing",
    "https://www.yelp.com/biz/abc-plumbing-denver",
    "https://www.instagram.com/abcplumbing"
  ],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Plumbing Services",
    "itemListElement": [
      {
        "@type": "OfferCatalog",
        "name": "Emergency Services",
        "itemListElement": [
          {
            "@type": "Offer",
            "itemOffered": {
              "@type": "Service",
              "name": "Emergency Drain Cleaning"
            }
          },
          {
            "@type": "Offer",
            "itemOffered": {
              "@type": "Service",
              "name": "Emergency Pipe Repair"
            }
          }
        ]
      }
    ]
  }
}
```

### LocalBusiness Subtypes

Use the most specific subtype for your industry:

| Industry | @type |
|----------|-------|
| Plumbing | `Plumber` |
| HVAC | `HVACBusiness` |
| Electrical | `Electrician` |
| Roofing | `RoofingContractor` |
| Locksmith | `Locksmith` |
| Pest Control | `LocalBusiness` (no specific subtype) |
| Cleaning | `HousePainter` or `LocalBusiness` |
| Landscaping | `LocalBusiness` |
| Auto Repair | `AutoRepair` |
| Dental | `Dentist` |
| Legal | `Attorney` or `LegalService` |
| Real Estate | `RealEstateAgent` |

Replace `"LocalBusiness"` with the appropriate subtype (e.g., `"Plumber"`).

---

## 2. Service Schema (Service Pages)

```json
{
  "@context": "https://schema.org",
  "@type": "Service",
  "name": "Emergency Drain Cleaning",
  "description": "24/7 emergency drain cleaning for residential and commercial properties in Denver. Fast response, licensed and insured.",
  "provider": {
    "@type": "LocalBusiness",
    "@id": "https://example.com/#business",
    "name": "ABC Plumbing"
  },
  "serviceType": "Drain Cleaning",
  "areaServed": [
    {
      "@type": "City",
      "name": "Denver"
    },
    {
      "@type": "City",
      "name": "Aurora"
    }
  ],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Drain Cleaning Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Residential Drain Cleaning"
        }
      },
      {
        "@type": "Offer",
        "itemOffered": {
          "@type": "Service",
          "name": "Commercial Drain Cleaning"
        }
      }
    ]
  },
  "offers": {
    "@type": "Offer",
    "price": "150.00",
    "priceCurrency": "USD",
    "priceSpecification": {
      "@type": "PriceSpecification",
      "price": "150.00",
      "priceCurrency": "USD",
      "description": "Starting price for residential drain cleaning"
    }
  }
}
```

---

## 3. FAQPage Schema (Service/Location Pages)

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How much does emergency drain cleaning cost in Denver?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Emergency drain cleaning in Denver typically costs between $150-$400 depending on the severity of the clog and time of service. After-hours emergency calls may incur an additional service fee. At ABC Plumbing, we provide upfront pricing before starting any work."
      }
    },
    {
      "@type": "Question",
      "name": "What causes most drain clogs in Denver homes?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Denver's older homes often have original cast-iron or galvanized pipes that accumulate mineral buildup over time. Common causes include grease buildup, hair accumulation, tree root intrusion (especially common in Capitol Hill and Washington Park neighborhoods), and freeze-thaw damage during winter months."
      }
    },
    {
      "@type": "Question",
      "name": "How quickly can you respond to emergency drain issues?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Our average response time for emergency drain cleaning in the Denver metro area is 30-45 minutes. We have technicians stationed throughout Denver, Aurora, and Littleton for fast coverage."
      }
    }
  ]
}
```

---

## 4. BreadcrumbList Schema (All Pages)

```json
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://example.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "Services",
      "item": "https://example.com/services/"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Drain Cleaning",
      "item": "https://example.com/services/drain-cleaning/"
    }
  ]
}
```

### Breadcrumb Patterns by Page Type

| Page Type | Breadcrumb |
|-----------|------------|
| Homepage | Home |
| Service page | Home > Services > [Service Name] |
| Location page | Home > Locations > [City Name] |
| Service + Location | Home > [City] > [Service Name] |
| Blog post | Home > Blog > [Post Title] |

---

## 5. Review/AggregateRating Schema

**Note:** Only use AggregateRating if you are collecting and displaying first-party reviews on your website. Do NOT fabricate ratings or use Google review data in schema (violates Google guidelines).

```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "@id": "https://example.com/#business",
  "name": "ABC Plumbing",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "127",
    "bestRating": "5",
    "worstRating": "1"
  },
  "review": [
    {
      "@type": "Review",
      "author": {
        "@type": "Person",
        "name": "Sarah Johnson"
      },
      "datePublished": "2026-01-15",
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "5",
        "bestRating": "5"
      },
      "reviewBody": "ABC Plumbing responded to our emergency drain issue within 30 minutes. Professional, clean, and fixed the problem quickly. Highly recommend for Denver homeowners."
    }
  ]
}
```

---

## 6. OpeningHoursSpecification (Detailed)

Ties directly to the "Openness" critical filter signal.

```json
{
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"],
      "opens": "07:00",
      "closes": "21:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Saturday"],
      "opens": "08:00",
      "closes": "17:00"
    },
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Sunday"],
      "opens": "09:00",
      "closes": "15:00"
    }
  ],
  "specialOpeningHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "validFrom": "2026-12-25",
      "validThrough": "2026-12-25",
      "opens": "00:00",
      "closes": "00:00",
      "description": "Closed on Christmas Day"
    }
  ]
}
```

### For 24/7 Emergency Services

```json
{
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": [
        "Monday", "Tuesday", "Wednesday", "Thursday",
        "Friday", "Saturday", "Sunday"
      ],
      "opens": "00:00",
      "closes": "23:59"
    }
  ]
}
```

---

## 7. GeoCoordinates and ServiceArea

### For Storefront Businesses

```json
{
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 39.7392,
    "longitude": -104.9903
  }
}
```

### For Service Area Businesses

```json
{
  "areaServed": [
    {
      "@type": "GeoCircle",
      "geoMidpoint": {
        "@type": "GeoCoordinates",
        "latitude": 39.7392,
        "longitude": -104.9903
      },
      "geoRadius": "30 mi"
    }
  ]
}
```

### For Multi-City Service Areas

```json
{
  "areaServed": [
    {
      "@type": "City",
      "name": "Denver",
      "sameAs": "https://en.wikipedia.org/wiki/Denver"
    },
    {
      "@type": "City",
      "name": "Aurora",
      "sameAs": "https://en.wikipedia.org/wiki/Aurora,_Colorado"
    },
    {
      "@type": "AdministrativeArea",
      "name": "Denver Metro Area"
    }
  ]
}
```

---

## Validation Checklist

1. Paste JSON-LD into [Google Rich Results Test](https://search.google.com/test/rich-results)
2. Fix all errors (required)
3. Address warnings (recommended)
4. Validate at [Schema.org Validator](https://validator.schema.org/)
5. Check for consistency between schema data and visible page content
6. Re-validate quarterly or after any business info changes
7. Test on both mobile and desktop

## Common Errors

| Error | Cause | Fix |
|-------|-------|-----|
| Missing required field | @type without name or address | Add all required properties |
| Invalid date format | "January 15, 2026" instead of ISO | Use "2026-01-15" format |
| Mismatched data | Schema says 4.8 rating but page shows 4.6 | Keep schema in sync with visible content |
| Review markup without reviews | AggregateRating without actual reviews on page | Only use if displaying real reviews |
| Wrong @type | Using Organization instead of LocalBusiness | Use most specific type |
