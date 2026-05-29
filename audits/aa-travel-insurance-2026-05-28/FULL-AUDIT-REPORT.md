# SEO Audit: AA Travel Insurance and Child Pages

**Audit date:** 2026-05-28  
**Target:** https://www.aa.co.nz/insurance/travel-insurance/  
**Scope requested:** Target URL plus child pages under `/insurance/travel-insurance/`.  
**Business type detected:** Financial services / travel insurance, distributed by The New Zealand Automobile Association with product administration and underwriting partner disclosures.  
**Method:** Codex SEO audit workflow, repository instructions, deterministic runner attempt, credential checks, drift baseline check, and live web-index evidence for discoverable child pages.

## Evidence and limitations

- No reusable `.seo-cache/` data existed before this audit, so fresh evidence was gathered.
- The deterministic audit runner could not resolve `www.aa.co.nz` from the local container, and direct `curl` through the environment returned a proxy `403 Forbidden`; therefore, page HTML, headers, live robots rules, screenshots, and script-derived page metrics could not be collected from the local runtime.
- Google API credentials were not configured, so no Search Console, GA4, PageSpeed Insights, CrUX, or URL Inspection data was available.
- Backlink credentials were not configured beyond the basic Common Crawl / verification tier.
- No drift baseline existed for this URL.
- To avoid fabricating crawl, SERP, API, or performance data, all findings below distinguish between directly evidenced indexed content and recommendations requiring site-side verification.

## Child-page discovery

The following child pages were discovered in live search-index evidence for the requested path:

| Page | URL | Primary role | Evidence freshness |
|---|---|---|---|
| Travel Insurance hub | `https://www.aa.co.nz/insurance/travel-insurance` | Commercial hub / quote entry | Search result crawled 6 months ago |
| Domestic travel insurance | `https://www.aa.co.nz/insurance/travel-insurance/domestic-travel-insurance/` | Commercial product page | Search result crawled 2 months ago |
| International travel insurance | `https://www.aa.co.nz/insurance/travel-insurance/international-travel-insurance/` | Commercial product page | Search result crawled last week |
| FAQs | `https://www.aa.co.nz/insurance/travel-insurance/epidemic-and-pandemic-diseases-faqs/` | Support / consideration content | Search result crawled 2 months ago |
| Policy wording | `https://www.aa.co.nz/insurance/travel-insurance/policy-wording` | Compliance / policy support | Search result crawled 2 months ago |
| Make a claim | `https://www.aa.co.nz/insurance/travel-insurance/make-a-claim/` | Customer support / retention | Search result crawled last week |
| Contact us | `https://www.aa.co.nz/insurance/travel-insurance/contact-us/` | Support / emergency assistance | Search result crawled last week |
| About us | `https://www.aa.co.nz/insurance/travel-insurance/about-us/` | Trust / partner disclosure | Search result crawled 3 weeks ago |
| Terms and conditions | `https://www.aa.co.nz/insurance/travel-insurance/terms-and-conditions/` | Legal support | Search result crawled 2 days ago |
| Complaint process | `https://www.aa.co.nz/insurance/travel-insurance/complaint-process/` | Trust / complaints support | Search result crawled 2 days ago |
| PDF destination map | `/content/dam/nzaa/insurance/travel-insurance/leisure-travel-insurance-country-plans/AA-Travel-Insurance-Destination-map-2024.pdf` | Downloadable destination plan reference | Search result published 6 months ago |
| PDF policy documents | `/content/dam/nzaa/insurance/travel-insurance/policy-wordings/...` | Policy wording downloads | Search result published 2-6 months ago |

## Executive summary

**Estimated SEO Health Score: 72 / 100**

This score is evidence-weighted and conservative because live crawl, headers, schema validation, Core Web Vitals, and screenshots could not be measured from the container. The AA Travel Insurance section has strong commercial intent coverage, strong trust signals, clear product pages for domestic and international policies, and rich support content. The main risks are content freshness inconsistencies, likely schema underuse, weak AI-answer packaging, possible duplication across partner/legal boilerplate, and unverified technical/performance controls.

### Category scoring

| Category | Weight | Score | Weighted contribution | Rationale |
|---|---:|---:|---:|---|
| Technical SEO | 22% | 70 | 15.4 | Indexed child pages are discoverable, but robots, canonicals, redirects, status codes, XML sitemap coverage, pagination, and headers could not be verified. |
| Content Quality | 23% | 78 | 17.9 | Strong trust, policy, contact, claims, FAQs, benefit summaries, and disclaimers; freshness conflicts reduce confidence. |
| On-Page SEO | 20% | 74 | 14.8 | Clear page targeting for domestic/international/support pages; opportunities remain for title/meta alignment, comparison tables, and internal-link modules. |
| Schema / Structured Data | 10% | 55 | 5.5 | FAQ, InsuranceAgency/FinancialProduct, BreadcrumbList, Organization, and ContactPoint opportunities are high; live schema could not be validated. |
| Performance / CWV | 10% | 65 | 6.5 | Image-heavy commercial pages and third-party quote flows are likely risk areas, but lab/field data was unavailable. |
| AI Search Readiness | 10% | 76 | 7.6 | Good factual Q&A and policy references; needs clearer extractable summaries, citations, update dates, and llms.txt/AI bot verification. |
| Images | 5% | 65 | 3.3 | Search-index snippets expose multiple imagery modules; dimensions, alt text, formats, lazy loading, and hero LCP impact were not verifiable. |
| **Total** | **100%** |  | **71.0 ≈ 72** |  |

## Top critical and high-priority findings

### Critical: Refresh or retire stale campaign content on the Travel Insurance hub

The hub page indexed evidence references a promotion requiring purchase before **30 November 2025**. As of the audit date, **28 May 2026**, this is expired. The domestic page evidence references a different campaign period of **16 February 2026 to 29 March 2026**, also expired by the audit date. Expired campaign copy can reduce user trust, weaken YMYL quality signals, and create compliance risk for a financial-services product.

**Recommendation:** Replace expired promotional modules with evergreen value propositions or a current campaign controlled by a CMS expiry date. Add QA checks that flag dates in the past before publication.

### High: Resolve partner/underwriter messaging inconsistencies across pages

Search-index evidence shows older hub copy stating that policies are issued and managed by AWP Services / Allianz Partners and underwritten by Mitsui Sumitomo, while newer child pages state policies are issued and underwritten by Zurich Australian Insurance Limited and distributed/administered by Cover-More for policies from 1 December 2025. The policy wording page explains the transition, but the hub page evidence appears stale.

**Recommendation:** Make the hub page match the current product state, then keep historical underwriter references in a clearly labelled “policies issued before 1 December 2025” section. This is especially important for SEO quality because insurance pages are YMYL content where accuracy, recency, and responsibility signals are weighted heavily.

### High: Add or validate structured data for FAQs, breadcrumbs, organization, contacts, and financial products

The FAQs page contains many expandable Q&A sections, and the contact page contains phone numbers, emergency assistance numbers, hours, and email addresses. These are strong candidates for valid `FAQPage`, `BreadcrumbList`, `Organization`, and `ContactPoint` JSON-LD. Product pages may also support careful `FinancialProduct` / `Service` style markup, subject to compliance review.

**Recommendation:** Validate existing JSON-LD in Rich Results Test and Schema.org validator. If absent, add page-specific JSON-LD to support rich results and AI retrieval. Avoid marking legal disclaimers as FAQ answers unless the exact visible Q&A content is represented.

### High: Improve comparison and decision support on domestic and international product pages

The domestic and international pages explain cover options and plan benefits, but snippets indicate mostly prose and repeated “Get a quote” CTAs. Users comparing insurance products need clear plan-level comparison, eligibility, exclusions, optional covers, and quote triggers.

**Recommendation:** Add above-the-fold comparison tables for Domestic, Domestic Cancellation, International Essentials, International Comprehensive, and Annual Multi-Trip options. Include “best for” guidance, cover highlights, key exclusions, and prominent links to policy wording.

### High: Create a current topical content layer around travel insurance use cases

The section has support pages but limited visible informational content targeting high-intent questions such as travel insurance for cruises, pre-existing medical conditions, snow sports, rental cars, domestic cancellation, travel alerts, family travel, and destination-specific requirements.

**Recommendation:** Build a travel insurance advice hub under the same path with expert-reviewed guides that internally link to product, FAQ, policy wording, and quote pages. Use compliance-reviewed “last reviewed” dates and named reviewers where possible.

## Page-by-page findings

### 1. Travel Insurance hub

**Strengths:** The hub addresses broad “travel insurance” intent, includes AA member discount messaging, domestic/international entry points, benefits, FAQs, phone support, policy wording references, and brand trust.

**Issues:** Indexed evidence appears stale: expired 2025 promotion, older Allianz/Mitsui partner references, and older phone number `0800 630 115` compared with newer child-page phone number `0800 808 203`. This page is the highest-priority page to refresh because it is the gateway for the section.

**Actions:**
- Update campaign and partner copy immediately.
- Add “Last reviewed” and “Product information effective from” dates.
- Add a compact “Domestic vs International vs Annual Multi-Trip” comparison module.
- Add breadcrumb and product/service schema after validation.
- Add internal links to FAQs, policy wording, claims, contact, complaint process, and relevant guide pages.

### 2. Domestic travel insurance

**Strengths:** Targets domestic insurance intent, explains Domestic, Domestic Cancellation, and Annual Multi-Trip options, includes AA member discount, cancellation, missed connection/travel delay, emergency assistance, rental vehicle excess, optional covers, contact details, partner disclosure, and policy wording links.

**Issues:** The indexed campaign “Take out a policy before 29 March” is expired by 28 May 2026. The page is content-rich but should be easier to scan for plan differences.

**Actions:**
- Remove or refresh expired promotion.
- Add a plan comparison table and FAQ schema for visible Q&A.
- Add internal links to domestic-specific use cases: road trips, rental cars, domestic cruises, events, family travel, weather disruption, and cancellation.

### 3. International travel insurance

**Strengths:** Clear international product targeting, three plan options, strong benefit details, medical-condition guidance, rental-vehicle excess, optional covers, cruise cover, phone support, financial strength rating, and current partner disclosure.

**Issues:** The page likely competes in a high-value market where comparison, destination intent, medical-condition questions, and cruise/snow/adventure modifiers matter. Search evidence does not show a destination-driven internal content architecture from this page.

**Actions:**
- Add comparison table for Essentials, Comprehensive, Annual Multi-Trip.
- Add “popular international cover questions” block linking to FAQs.
- Create and internally link to destination/use-case pages where compliant: Australia, Pacific Islands, USA/Canada, Europe, cruises, skiing/snowboarding, adventure activities, business travel, pre-existing medical conditions.

### 4. FAQs / epidemic-and-pandemic-diseases-faqs

**Strengths:** The FAQ page has many visible Q&A modules covering contact, emergency assistance, dependent children, group travellers, policy changes, delays/missed connections, valuables, medical conditions, pregnancy, cruise cover, snow sports, business pack, cancellation plus, adventure cover, and motorcycle/moped cover.

**Issues:** The URL slug focuses on epidemic and pandemic diseases, but indexed content now appears to be a broad travel insurance FAQ. This slug-content mismatch may suppress relevance for generic “travel insurance FAQs” queries and confuse internal linking.

**Actions:**
- Consider a cleaner canonical FAQ URL such as `/insurance/travel-insurance/faqs/`, with a 301 redirect from the old pandemic FAQ slug if appropriate.
- Validate FAQPage schema for visible questions and answers.
- Add jump links, table of contents, and concise answer summaries.
- Link every answer to the relevant product or policy wording section.

### 5. Policy wording

**Strengths:** Directly supports YMYL compliance and user confidence. It explains the current policy wording effective 1 December 2025 and historical policies issued before that date.

**Issues:** The page is critical to purchase confidence but may be too document-led for users comparing policies quickly. Search snippets expose multiple PDF policy documents, including older PDFs, which may create duplicate or stale-document risk if not clearly controlled.

**Actions:**
- Ensure the current policy PDF is indexable and older PDFs are labelled, linked only from historical sections, and canonical/noindex decisions are deliberate.
- Add a summary table of current documents by policy type and effective date.
- Add `lastReviewed`/`dateModified` where appropriate and visible.

### 6. Make a claim

**Strengths:** Strong support intent; explains documents required, online claims, claim form fallback, email, postal address, and contact hours.

**Issues:** Claim content includes transitional language for policy numbers starting with 8 and historical provider references. It should be highly scannable for stressed users and AI assistants.

**Actions:**
- Add a “Start here” decision tree: policy starts with 8 / older policy / emergency / standard claim.
- Add ClaimAction-style internal UX copy, but validate schema carefully because Schema.org support for insurance claims may need conservative markup.
- Ensure contact details match the contact page.

### 7. Contact us

**Strengths:** Contains customer-service numbers, hours, email, and emergency-assistance numbers for multiple countries.

**Issues:** Multiple providers and historical emergency numbers are present; the page must prevent users from choosing the wrong number. Phone numbers and hours are prime structured-data targets.

**Actions:**
- Separate current policy contacts from pre-1 December 2025 contacts in clearly labelled cards.
- Add `ContactPoint` schema for sales, service, claims, and emergency assistance if validated.
- Add click-to-call formatting and visible time zone.

### 8. About us

**Strengths:** Adds trust context: AA has guided journeys for more than 120 years, positions AA as a trusted brand, and explains Cover-More / Zurich roles.

**Issues:** The page can do more to demonstrate E-E-A-T for insurance: governance, review process, regulatory details, partner responsibilities, and product-update cadence.

**Actions:**
- Add compliance/reviewer notes for product content.
- Add “how AA Travel Insurance is provided” diagram.
- Link to privacy, terms, policy wording, complaints, and financial strength pages.

### 9. Terms and conditions

**Strengths:** Covers privacy, policy terms, website terms, and data-sharing distinctions for post- and pre-1 December 2025 policies.

**Issues:** Legal pages are support pages, but they can still cause stale trust signals if provider names diverge from product pages.

**Actions:**
- Cross-check all partner names, dates, NZBN/FSP references, and privacy links.
- Add table of contents and anchors to improve usability.

### 10. Complaint process

**Strengths:** Complaint handling details and response expectations support trust and regulated-service transparency.

**Issues:** Search evidence emphasizes historical Allianz contact details, which may or may not be correct for current policies. The page should clearly segment current versus historical complaint pathways.

**Actions:**
- Place current complaints contact first, historical pathway second.
- Add “which process applies to me?” decision support.
- Link back to policy wording, contact, and claims pages.

## Technical SEO

### What appears positive

- Multiple child pages are indexed and discoverable in search results.
- Core commercial and support pages exist under a coherent `/insurance/travel-insurance/` directory.
- PDFs are discoverable, which can help users and search engines find policy documents.

### What could not be verified

- HTTP status codes, canonical tags, robots meta, X-Robots-Tag, sitemap entries, redirect chains, hreflang, Open Graph/Twitter metadata, mobile rendering, security headers, and JavaScript dependency for primary content.
- Whether the URL with query parameter `?gad=1` canonicalizes correctly to the clean domestic page.
- Whether PDF policy documents have deliberate index/canonical/noindex handling.

### Recommendations

1. Run a full crawler from an unrestricted network and export status, canonical, indexability, title, meta, H1, word count, inlinks, and outlinks for all `/insurance/travel-insurance/` URLs.
2. Verify XML sitemap inclusion for the hub, product pages, FAQs, claims, contact, policy wording, terms, and complaint pages.
3. Confirm clean canonical URLs for all query-parameter variants and trailing-slash variants.
4. Validate that quote CTAs do not block crawlable informational content or rely on JavaScript for core copy.
5. Ensure all PDFs linked from the section are current or deliberately historical.

## Content quality and E-E-A-T

AA has strong brand authority and the section includes important YMYL trust elements: policy wording, financial strength ratings, partner disclosures, privacy references, claims process, contact details, and complaints process. The most important content-quality weakness is inconsistency over time. Several pages show current Zurich/Cover-More wording, while the hub and some historical sections show Allianz/Mitsui references. The policy transition is legitimate, but the presentation must be precise and consistent.

**Recommended E-E-A-T upgrades:**

- Add visible `Last reviewed` dates to product, FAQ, policy, contact, and claims pages.
- Add reviewer attribution such as “Reviewed by AA Travel Insurance product/compliance team”.
- Add a content-change log for major policy transitions.
- Create concise, plain-English policy summaries while keeping “read the Policy Wording” disclaimers.
- Link each benefit claim to the relevant policy wording or disclosure.

## On-page SEO

**Primary keyword targets by page:**

| Page | Suggested primary target | Secondary targets |
|---|---|---|
| Hub | travel insurance NZ | AA travel insurance, travel insurance quote, domestic and international travel insurance |
| Domestic | domestic travel insurance NZ | NZ travel insurance, domestic cancellation cover, rental vehicle excess NZ |
| International | international travel insurance NZ | overseas travel insurance, annual multi-trip travel insurance, cruise cover, medical conditions |
| FAQs | travel insurance FAQs | travel insurance medical conditions, cruise cover, cancellation cover, travel delay insurance |
| Policy wording | AA travel insurance policy wording | travel insurance policy document, cover limits, exclusions |
| Make a claim | AA travel insurance claim | travel insurance claims NZ, claim form, online claims portal |
| Contact | AA travel insurance contact | emergency assistance, travel insurance phone number |

**Recommended on-page templates:**

- Title: keep under roughly 55-60 characters where possible and place the unique intent first.
- Meta description: answer user intent and include proof points such as AA member discount, 24/7 emergency help, or policy wording availability.
- H1: one clear H1 matching the page intent.
- H2s: include “Cover options”, “What’s included”, “Optional cover”, “Before you buy”, “FAQs”, and “Policy wording”.
- Internal links: use descriptive anchor text, not repeated generic “Find out more” or “Get a quote” only.

## Schema and structured data

Because direct HTML access failed, current schema could not be confirmed. The following schema plan should be validated before deployment:

- `Organization` for The New Zealand Automobile Association.
- `BreadcrumbList` on all child pages.
- `FAQPage` on the FAQ page and possibly selected product FAQs where the questions and answers are visible on-page.
- `ContactPoint` for sales/customer service, claims, and emergency assistance.
- Conservative `Service` or `FinancialProduct` markup for Travel Insurance product pages after legal/compliance review.
- `WebPage` with `dateModified`, `reviewedBy`, and `about` properties where supported by implementation standards.

## Performance and Core Web Vitals

Performance could not be measured because local fetch and PageSpeed/CrUX API access were unavailable. Based on page patterns visible in indexed snippets, priority performance checks should include:

- Hero image optimization on the hub, domestic, and international pages.
- Lazy loading below-the-fold images and icons.
- Responsive image dimensions and WebP/AVIF use.
- Third-party quote widgets and analytics impact on INP.
- Font loading and render-blocking CSS.
- Mobile above-the-fold LCP element identification.

## Image SEO

Search-index snippets expose multiple image modules such as travel imagery, icons, member-benefit imagery, and product-adjacent promotional graphics. Without HTML access, alt text, dimensions, byte size, and lazy loading could not be verified.

**Recommendations:**

- Use descriptive alt text for meaningful images, e.g. domestic travel scenery, international travel imagery, and member benefit cards.
- Mark decorative icons as decorative where appropriate.
- Compress hero images and preload only the true LCP image.
- Avoid text-only promotional images unless the same promotion text is available as accessible HTML.

## AI Search / GEO readiness

The section has several assets that are valuable for AI answers: FAQs, policy wording, contact numbers, emergency assistance, plan descriptions, and financial strength disclosures. To improve answer-engine visibility:

- Add concise summaries near the top of each product page.
- Use tables for plans, eligibility, optional covers, exclusions, and claim pathways.
- Add visible dates and source links to policy wording.
- Create stable anchors for high-intent questions.
- Verify AI crawler access and consider `llms.txt` if aligned with site policy.
- Avoid relying solely on expandable accordions if answer text is not present in initial HTML.

## Internal linking architecture

Recommended travel-insurance section architecture:

```text
/insurance/travel-insurance/
  /domestic-travel-insurance/
  /international-travel-insurance/
  /faqs/  (or canonical replacement for the current pandemic FAQ slug)
  /policy-wording
  /make-a-claim/
  /contact-us/
  /complaint-process/
  /about-us/
  /terms-and-conditions/
  /guides/
    /travel-insurance-for-cruises/
    /travel-insurance-for-medical-conditions/
    /domestic-travel-insurance-for-road-trips/
    /travel-insurance-for-snow-sports/
    /travel-insurance-for-rental-cars/
    /annual-multi-trip-travel-insurance/
```

## Prioritized roadmap

### Fix immediately

1. Remove expired campaigns from hub and domestic pages.
2. Reconcile current versus historical underwriter/administrator references on all pages.
3. Verify current phone numbers and emergency numbers across hub, contact, claim, and FAQ pages.
4. Crawl the section from an unrestricted environment and validate indexability, canonicals, sitemap coverage, and status codes.

### Fix within one week

1. Add comparison tables to hub, domestic, and international pages.
2. Add/validate FAQ, BreadcrumbList, Organization, and ContactPoint schema.
3. Rename or canonicalize the broad FAQ experience away from the legacy epidemic/pandemic-only slug if appropriate.
4. Add last-reviewed dates and compliance-review attribution.

### Fix within one month

1. Build a travel insurance guide hub for high-intent use cases.
2. Improve policy wording page with current/historical document table.
3. Improve claims and complaints pages with decision trees.
4. Run performance and image optimization work after measuring CWV.

### Backlog

1. Add llms.txt / AI-crawler policy if aligned with corporate policy.
2. Add visual QA screenshots for desktop and mobile templates.
3. Build automated stale-date checks for promotional copy.
4. Monitor rankings and conversions by page template after updates.

## Final note

This audit intentionally avoids claiming live crawl, schema, header, Core Web Vitals, or Search Console findings because those data sources were unavailable in the execution environment. The recommendations are based on the indexed evidence available on 2026-05-28, repository SEO methodology, and standard YMYL SEO best practices for insurance content.
