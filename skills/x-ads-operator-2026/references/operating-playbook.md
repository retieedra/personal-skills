# Operating playbook

Use only the sections relevant to the request. Platform statements link to primary documentation; the decision procedures and examples are author recommendations. Refresh material schemas and policies when applying this 2026-09-15 research baseline.

## 1. Establish a feasible acquisition test

Start from a brief containing the account and currency, offer, audience/market, destination, business outcome, approved daily and lifetime spend, dates/timezone, data owner, and permission to change or activate anything. A limit is a ceiling, not a target to exhaust.

For a one-order business, estimate:

- Contribution before advertising = net collected revenue − product costs − fulfillment − payment costs − expected returns and other variable costs.
- Allowable acquisition cost = contribution available for acquisition within the agreed payback window − required remaining contribution.
- Allowable raw-lead cost = allowable customer acquisition cost × qualified-share of leads × close rate among qualified leads.

Use compatible customer cohorts and sufficiently mature close/return data. For example, a $120 allowable customer cost, 40% qualification rate, and 10% qualified-lead close rate implies $4.80 per raw lead. These invented figures illustrate arithmetic, not an X benchmark. Do not count a repeat customer's entire lifetime revenue as incremental first-order contribution.

Given an anticipated CPA range, divide the authorized test budget by that range to show plausible conversion counts. A $300 test at $30–$60 CPA suggests roughly 5–10 outcomes before uncertainty, which cannot support dozens of audience/creative cells. Recommend fewer comparisons, a longer permitted observation period, or explicitly exploratory evidence. Do not raise the ceiling to satisfy a platform recommendation.

## 2. Validate events and attribution

Create an event contract: business meaning; confirmed trigger; Pixel/event mapping; occurrence ID; timestamp; value/currency definition; consent state; identifier source; retry behavior; destination source of truth.

The developer guide specifies unsalted SHA-256 for appropriately normalized email and E.164 phone identifiers; `twclid` is not hashed. IP or user-agent matching requires another identifier. CAPI user tokens require an account manager or administrator role. Check the current reference before implementation. [CAPI documentation](https://docs.x.com/x-ads-api/measurement/web-conversions)

Test a permitted controlled journey:

1. Record the real business occurrence and expected payload locally with identifying data redacted.
2. Follow the event through browser and/or server logs, API response, and Events Manager. Inspect errors and processing results rather than assuming every HTTP success accepted every item.
3. Revisit confirmation, retry delivery, and test a second independent order; verify single-count versus new-count behavior.
4. Verify consent refusal and opt-out routes suppress disallowed collection in both browser and server paths. Check free-text descriptions, URL parameters, and product details for restricted data.
5. Reconcile within the same time basis and attribution rules. Preserve campaign URL tags for first-party analysis, but do not mistake them for causal attribution.

Record selected post-view and post-engagement windows, attribution date basis, timezone, and conversion lag. Compare mature cohorts with mature cohorts. X also notes that some opted-out iOS conversions appear at campaign/ad-group level without ad-level reporting; do not allocate the gap across creatives as if observed. [Sales reporting caveat](https://business.x.com/en/help/campaign-setup/create-website-conversions-campaign)

Hashing is a matching mechanism, not anonymization or permission. Apply the actual consent and audience policies to both ingestion paths. Avoid building events or custom audiences from sensitive categories; examine country-specific targeting rules separately rather than assuming one rule's exception permits every product. [Tracking policy](https://business.x.com/en/help/ads-policies/campaign-considerations/policies-for-conversion-tracking-and-custom-audiences), [targeting policy](https://business.x.com/en/help/ads-policies/campaign-considerations/targeting-of-sensitive-categories)

## 3. Separate creative discovery from audience testing

For each concept, write the customer problem, promised benefit, supporting proof, visual idea, CTA, and corresponding landing-page section. A useful first comparison is a concrete product demonstration versus a customer-use-case narrative with the same offer. Keep claims supportable and urgency real. X recommends testing formats and CTAs; no one format wins universally. [Traffic guidance](https://business.x.com/en/help/campaign-editing-and-optimization/optimizing-website-traffic-campaigns)

Define whether the goal is efficient delivery or an interpretable experiment. If the platform optimizes delivery between ads, the creative receiving more spend was not randomly assigned an equal opportunity. Avoid calling that allocation causal proof. For stronger comparisons, use available experiment functionality or deliberately comparable cohorts with documented residual confounding.

For an audience test, hold creative and destination constant; document geography, exclusions, placements, audience overlap, and expansion. With Optimized Targeting enabled, selected targeting may behave as input rather than a strict cohort boundary. Verify account controls and call the test what it actually compares. [Optimized Targeting explanation](https://business.x.com/en/blog/create-and-launch-sales-campaigns-in-minutes)

Precommit the primary metric and guardrails, conversion-maturity window, maximum loss, and decision rule. Monitor broken tracking and spend separately from performance evaluation. If making repeated interim comparisons, report uncertainty rather than selecting the lowest noisy CPA. Fatigue needs evidence such as declining comparable-cohort performance; a calendar alone does not prove it.

## 4. Diagnose before editing bids or budgets

- **Little delivery:** inspect eligibility, review status, dates/timezone, funding, effective status, audience constraints, and bid competitiveness before changing spend.
- **Clicks without loaded visits:** inspect redirect chains, mobile load, consent/analytics behavior, broken URLs, and misleading click affordances.
- **Visits without completions:** inspect offer clarity, form/checkout errors, and product-market fit.
- **Cheap leads without customers:** reconcile duplicates, lead quality, response time, qualification, and close lag.
- **High platform return without cash:** reconcile conversion definition, overlapping claims, refunds, repeat customers, and contribution margin.

The 2024 Sales sheet recommends allowing an initial 3–5 days with limited edits and suggests 10–20 daily conversions. These are context for expected learning, not an instruction to ignore a broken site or spend beyond the user's loss limit. Do not convert its scaling suggestions into an automatic budget rule. [Dated playbook](https://business.x.com/content/dam/business-twitter/resources/x-downloadable-guides/sales-campaign-best-practices.pdf)

## 5. Prepare safe Ads API operations

Verify application-level Ads API approval, the authenticated user's account access, and the user's authorization for this particular action. Ads API authentication uses OAuth 1.0a over HTTPS; use a maintained signing implementation and keep secrets out of generated artifacts. [Authentication](https://docs.x.com/x-ads-api/fundamentals/making-authenticated-requests)

Inventory the relationships:

- Account: advertiser context, timezone, currency, permissions.
- Funding instrument: existing source of funds referenced by the campaign; inspect whether it can fund.
- Campaign: grouping, scheduling, budget controls and funding reference.
- Line item: ad group connected to the campaign, with objective, bidding, targeting and placements.
- Promoted-post association: connects an eligible post to the line item; creating a post and promoting it are separate actions.

These are documented relationships, not instructions to create them unasked. Preserve discovered IDs as strings and resolve existing objects before creating replacements. [Campaign hierarchy](https://docs.x.com/x-ads-api/campaign-management)

Use `authenticated_user_access` to inspect account roles. The official reference distinguishes `AD_MANAGER`, `ACCOUNT_ADMIN`, and `CAMPAIGN_ANALYST`; composer permission is an additional consideration for promoted-only creative. Do not infer write permission from successful reporting. [Permissions reference](https://docs.x.com/x-ads-api/campaign-management/reference)

Treat historical sample versions, objective lists, and UI-to-enum mappings as unverified until the relevant live endpoint schema confirms them. `entity_status=PAUSED` appears in official campaign/line-item examples; request explicit paused creation when that workflow is authorized, then read back state. Paused creation is still an account mutation. Confirm effective delivery eligibility before authorized activation.

Write a change manifest with account/object IDs, before/after values, units, scope, activation state, and rollback. Currency micros are integers: $25.50 corresponds to 25,500,000 USD micros. Use integer/decimal-safe conversion and match the actual account currency. Never execute copied examples containing sample budgets.

For an uncertain write outcome, read back and reconcile before retrying so a timeout cannot silently duplicate campaigns. Stop on unresolved permission errors, schema conflicts, or ambiguous state. For throttled analytics calls, honor reset/retry headers; cap retries and report the unresolved failure. [Analytics retry guidance](https://docs.x.com/x-ads-api/analytics)

## 6. Report in defensible units

Convert `billed_charge_local_micro / 1,000,000` to account currency before calculating costs. Define each denominator:

- CPM = currency spend × 1,000 / impressions.
- Link-click rate = `url_clicks` / impressions; document the field's inclusion of earned clicks when relevant.
- Cost per observed business outcome = currency spend / deduplicated eligible outcomes.
- Attributed revenue return = attributed revenue / spend; this is not incremental profit.

API `clicks` is broader than website clicks. Retain the raw field name and paid/earned scope in exports, and do not silently mix numerator scopes. Mark zero-denominator rates undefined. Spend may remain estimated for up to three days under the documented billing behavior. [Metric definitions](https://docs.x.com/x-ads-api/analytics)

Show the business ledger alongside platform attribution and explain reconciliation gaps. Preserve the distinction between observed, attributed, and incremental results. Recommend the next bounded action with its evidence, cost ceiling, and what would change the decision. If implementation is authorized, read back the final configuration and report what actually happened.
