# Research ledger

Reviewed **2026-09-15**. These are primary X sources, not independent effectiveness studies. Pages were accessed directly through web research. Unless stated below, a dependable publication or revision date was not visible; access date must not be presented as publication date. “Current” means available when checked, not tested against every advertising account.

## Sources and operational conclusions

### 1. Sales campaign setup

[Create a website sales campaign](https://business.x.com/en/help/campaign-setup/create-website-conversions-campaign)

The URL retains “conversions,” while the page describes the Sales objective and Web conversions goal. It documents campaign-budget optimization, conversion-event selection, and Autobid with impression billing as X's recommended defaults. Select an active event that represents the business outcome. Account eligibility and current UI still control availability; recommendations are not performance promises.

### 2. Website conversion tracking

[Conversion tracking for websites](https://business.x.com/en/help/campaign-measurement-and-analytics/conversion-tracking-for-websites)

Pixel and server-to-server Conversion API are complementary; the page documents event parameters and `conversion_id` deduplication. It also distinguishes configured events and attribution settings. Use this for product-level behavior and verify the exact implementation with the developer reference. Do not infer that raw events, attributed conversions, and settled orders must match.

### 3. CAPI implementation

[Web conversions](https://docs.x.com/x-ads-api/measurement/web-conversions)

Documents existing-event reuse for Pixel/CAPI deduplication, matching identifiers, request structure, and account-role prerequisites. Its testing section was effectively empty when accessed, and sample code includes historical values; do not treat those examples as production-ready. Validate the actual integration and current endpoint rather than asserting that reading this guide proves deduplication works.

### 4. Campaign objects

[Campaign Management](https://docs.x.com/x-ads-api/campaign-management)

Explains funding instruments, campaigns, line items, targeting, and promoted content. Examples use older API versions and historical dates. Its overview objective list differs from other documentation; copying the list into a 2026 implementation would falsely imply completeness. The hierarchy is useful, but verify each operation's current schema and account capabilities.

### 5. Campaign reference and permissions

[Campaign Management API Reference](https://docs.x.com/x-ads-api/campaign-management/reference)

The indexed official reference documents `authenticated_user_access` and distinguishes campaign administrators/managers, analysts, creative managers, and composer permission. Direct page opening intermittently failed during research, while indexed excerpts were readable. Resolve the live reference before writing executable mutations. Examples of funding-instrument creation can be sandbox-specific; they do not establish permission to create a production payment method.

### 6. Reporting definitions

[Analytics](https://docs.x.com/x-ads-api/analytics)

The metric glossary distinguishes broad `clicks` from `url_clicks`, which can include earned clicks, and identifies billed spend in currency micros. It describes billing estimates up to three days and response-header-driven retries. Legacy derived-metric examples coexist with newer fields, so label units and denominators explicitly. Do not extend general metric-finalization language into a guarantee about late business conversions.

### 7. Authentication

[Making Authenticated Requests](https://docs.x.com/x-ads-api/fundamentals/making-authenticated-requests)

Ads API access requires approved application access and an authorized user's credentials, using OAuth 1.0a over HTTPS. Normal X API access or possession of a bearer token does not by itself establish Ads API access. Path examples contain historical version numbers; resolve the supported version before implementation. Keep app access, account role, and user authorization as three separate checks.

### 8. Tracking and audience policy

[Policies for conversion tracking and custom audiences](https://business.x.com/en/help/ads-policies/campaign-considerations/policies-for-conversion-tracking-and-custom-audiences)

Sets notice, consent, opt-out, and sensitive-data restrictions for these products. Server-side collection is not an exception to privacy choices. Review the actual event payload and audience origin, including URL parameters and free text, rather than treating a hash as permission to share data.

### 9. Sensitive-category targeting

[Targeting of Sensitive Categories](https://business.x.com/en/help/ads-policies/campaign-considerations/targeting-of-sensitive-categories)

Restricts sensitive-category targeting, personal information in creative, and copy implying knowledge of sensitive attributes. Country-specific exceptions appear on the page and do not automatically override separate conversion/custom-audience rules. Check the policy applicable to the actual product, market, certification, and targeting method before proposing such targeting.

### 10. Optimized Targeting

[Create and launch Sales campaigns in minutes](https://business.x.com/en/blog/create-and-launch-sales-campaigns-in-minutes)

The product announcement says Optimized Targeting is enabled by default for Sales and may reach beyond selected audiences. Its uplift claims cite internal beta results, without enough experimental detail to serve as universal expectations. Record this feature's actual state when interpreting audience experiments; do not promise the announcement's averages to a new advertiser.

### 11. Dated Sales recommendations

[Sales Campaign Best Practices](https://business.x.com/content/dam/business-twitter/resources/x-downloadable-guides/sales-campaign-best-practices.pdf)

The one-page document explicitly identifies its source as **X Best Practices, 2024**. Suggestions include approximately 10–20 daily conversions, a 3–5-day initial learning period, and limited editing cadence. These are dated platform recommendations, not a mandatory universal minimum, proof of statistical significance, or authorization to increase spend. Smaller accounts need a feasible experiment, not a fabricated guarantee of learning.

### 12. Traffic and creative diagnostics

[Optimizing for website traffic campaigns](https://business.x.com/en/help/campaign-editing-and-optimization/optimizing-website-traffic-campaigns)

Discusses testing creative formats and CTA approaches, matching expectations to the destination, and click-versus-landing-page discrepancies. It contains older Website Card terminology and setup language; use current format specifications before production. Link clicks can occur before the destination finishes loading, so investigate technical and intent losses rather than labeling every discrepancy fraud.

## What the evidence does not establish

No source here establishes a universally profitable bid, conversion volume, audience size, creative count, scaling percentage, or guaranteed 2026 outcome. Financial formulas, experiment boundaries, diagnostic sequencing, and rollout controls in the skill are the author's operating recommendations. Validate them against the advertiser's data and authorization. This ledger is a research baseline, not a certification by X.
