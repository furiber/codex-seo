# Action Plan: AA Travel Insurance SEO Audit

**Audit date:** 2026-05-28  
**Target section:** `https://www.aa.co.nz/insurance/travel-insurance/` and child pages.

## Critical priorities

1. **Refresh stale promotions.** Remove or replace expired promotions on the Travel Insurance hub and Domestic Travel Insurance page. The indexed hub evidence references a 30 November 2025 promotion, and the domestic page evidence references a 29 March 2026 campaign.
2. **Reconcile provider disclosures.** Align all current-policy pages to the current Zurich / Cover-More disclosure while preserving Allianz / Mitsui Sumitomo information only in clearly labelled historical policy sections.
3. **Verify contact consistency.** Confirm the correct current phone number, email, claims, and emergency-assistance details across the hub, FAQ, claims, and contact pages.
4. **Run unrestricted crawl validation.** From a network that can reach `www.aa.co.nz`, verify status codes, canonicals, robots, XML sitemap coverage, meta robots, schema, headings, titles, meta descriptions, and internal links for all travel-insurance child pages.

## High priorities

1. **Add decision-support modules.** Add comparison tables for Domestic, Domestic Cancellation, Essentials, Comprehensive, and Annual Multi-Trip products.
2. **Add/validate schema.** Implement or validate `BreadcrumbList`, `Organization`, `ContactPoint`, `FAQPage`, and compliance-approved product/service schema.
3. **Improve FAQ URL relevance.** Consider canonicalizing the broad FAQ page to `/insurance/travel-insurance/faqs/` if the current pandemic-focused slug no longer reflects the page content.
4. **Add visible review signals.** Add “last reviewed”, “effective from”, and compliance-review attribution to product and support pages.
5. **Control PDF indexing.** Ensure current policy PDFs are findable and older PDFs are clearly labelled historical, with deliberate canonical/noindex choices.

## Medium priorities

1. **Build travel-insurance guides.** Create expert-reviewed guide content for cruises, medical conditions, domestic road trips, snow sports, rental vehicles, annual multi-trip policies, family travel, travel disruption, and destination requirements.
2. **Improve support UX.** Add decision trees to claims, contact, and complaints pages so users can identify the correct pathway by policy issue date or policy number.
3. **Optimize AI-answer packaging.** Add concise summaries, tables, jump links, stable anchors, and source links to policy wording.
4. **Measure and improve CWV.** Run PageSpeed/CrUX or Lighthouse checks after network access is available, then optimize hero images, third-party quote flows, scripts, fonts, and mobile rendering.

## Low priorities

1. Add `llms.txt` or documented AI-crawler policy if it matches AA policy.
2. Add desktop/mobile screenshot regression checks for commercial templates.
3. Add CMS stale-date validation for campaign components.
4. Monitor Search Console performance after updates and compare impressions/clicks by page type.

## Suggested implementation sequence

| Week | Workstream | Deliverables |
|---|---|---|
| 0-1 | Accuracy and compliance | Updated promotions, provider disclosures, contact details, current/historical policy segmentation |
| 1-2 | Technical validation | Crawl export, sitemap/indexability fixes, canonical handling, schema validation |
| 2-4 | Conversion/on-page UX | Comparison tables, support decision trees, FAQ URL/canonical updates, internal-link improvements |
| 4-8 | Content expansion | Expert-reviewed guide hub and use-case pages |
| Ongoing | Measurement | CWV monitoring, stale-date checks, Search Console reporting, ranking/conversion review |
