# Operating playbook

These procedures are proposed operating defaults, not platform requirements or measured effect sizes. Adapt them to the user's market, evidence, access, and budget. Consult [research.md](research.md) for the cited study limitations.

## Choose a tractable initial engagement

**Audit:** answer one business question using existing exports, representative pages, and a small clearly labeled panel. Deliver the mechanism worth investigating and the next collection step.

**Launch:** establish a versioned baseline, resolve access/factual failures, and test one coherent content intervention before expanding the backlog.

**Investigation:** first test whether the apparent change came from instrumentation, panel composition, model/surface changes, or business changes. Rewriting content is not the default response to an unexplained graph.

For a baseline without history, two weeks can be a planning starting point, not a statistical guarantee. Extend or reduce it based on day-to-day variation, sample coverage, seasonality, and the decision's cost. Do not automatically schedule recurring collection or paid calls without authorization.

## Panel design

Build cells for the combinations that actually matter: intent × audience/product × locale/language × engine/surface. Avoid a combinatorial grid of irrelevant cells. A regional B2B company may need purchasing, implementation, and compliance questions in two languages; a local retailer may need product availability and service-area comparisons.

Record each prompt's provenance: customer wording, internal search, sales notes, search-demand proxy, observed AI conversation, or synthetic variant. Remove personal information from exported examples. An opt-in panel is still a sample with selection effects; treat provider volume estimates as provider estimates.

Keep branded and unbranded results separately visible. A question containing the brand name makes a mention easier and measures a different task from unaided discovery. Tag prompts that explicitly require citations, since these change the response condition.

Choose either equal cell weighting or justified buyer-demand weighting and retain both where helpful. Never substitute invented market weights. Freeze a comparison panel and maintain an exploratory queue. When the panel changes, show like-for-like results on its stable intersection; do not silently splice series.

Budget example: allocate first to coverage of neglected important cells, then repeated days, then extra within-day repeats where the pilot shows decision-relevant uncertainty. Different prompts and days are not automatically independent observations. The Profound cadence results [R1] motivate this ordering but do not dictate sample counts.

## Observation record

Retain enough to reproduce classification:

- Panel/version, prompt ID/text, cell, provenance, weight.
- Engine, consumer/API surface, search/tool mode, locale, language, time zone, timestamp, known model, controlled account context.
- Outcome: answer, no AI feature, refusal, technical failure, or blocked observation.
- Raw response or permissible snapshot, visible sources, normalized URLs/domains, aliases, recommendation/accuracy labels, and reviewer notes.
- Collection/extraction version, experiment ID, and any retry linkage.

No technical failures should quietly become negative mentions. Set a bounded retry policy and keep the first failure record; do not rerun until the brand appears. No AI Overview, when the surface was successfully observed, is a valid absence. Report both overall opportunity presence and conditional presence among generated answers when useful.

## Metric contract

Let `N` be valid observations under the declared surface-specific rule, `M` observations mentioning the brand, `C` observations with an owned citation, `U` owned citation units, and `T` all citation units.

- Mention presence = `M/N`.
- Owned citation presence = `C/N`.
- Owned citation share = `U/T`; undefined when `T=0`, never an automatic zero.
- Collection coverage = valid observations / attempted observations; show exclusions by reason.
- Recommendation presence = qualifying recommendations / the chosen valid denominator. Define whether listing as an option qualifies, and keep strong endorsements separate.
- Accuracy rate = reviewed correct brand claims / reviewed brand claims. Preserve “unverifiable” as its own state; absence of claims is not perfect accuracy.

For an in-house panel, use one canonical URL per answer as a citation unit unless another unit better answers the question. Record how redirects, fragments, syndicated copies, and duplicate inline links are treated. Keep raw links. A vendor's “slot” may use a different definition; retain its original measure rather than relabeling it.

If reporting competitive share of voice, state the competitor set and normalization. Summing binary mentions for each brand counts multiple brands in one answer. The resulting share among that set is not population awareness. An owned-domain citation can coexist with no brand recommendation, and a recommendation can rely entirely on third-party sources.

For aggregated panels, report equal-prompt averages and citation-volume-weighted shares separately when they tell different stories. Publish numerator, denominator, period, panel version, and excluded cells. Illustrative example: moving from 20/100 to 30/100 is +10 percentage points and +50% relative, not “50 points.”

Use uncertainty appropriate to repeated observations: compare paired prompt cells, resample whole prompt histories and day blocks where justified, and examine engine/locale slices. Do not treat every citation link as an independent user. Small or unstable panels often deserve a range and an inconclusive result rather than a spurious significance label.

## Access and discovery investigation

Classify each checked URL by what is observable:

1. **Discovery:** linked internally, in relevant sitemaps, or observed in search/source results.
2. **Access:** actual HTTP response and delivered body; redirects, access controls, CDN challenges, timeouts.
3. **Content availability:** important facts in retrieved/rendered content, with differences documented rather than presumed equivalent across crawlers.
4. **Index/serving eligibility:** relevant console evidence, canonical and snippet settings, owner inclusion choices.
5. **Observed retrieval/citation:** actual source output where available. If retrieval is hidden, mark it unknown.
6. **Representation/action:** factual answer quality, recommendation context, suitable landing page and conversion path.

Do not infer “not indexed” from one chatbot's failure to name a page or a `site:` query alone. Log date, tool, and scope for every diagnosis. Treat direct URL fetch tests as access tests, not representative discovery prompts.

Search and training are separate permissions. The live OpenAI and Perplexity docs [R8–R9] are the authority on their agents. Prepare the smallest relevant infrastructure change for an authorized owner; do not globally disable a WAF. Check effective Google property inheritance [R6] rather than guessing from robots.txt.

## Content and reputation work

Map an answer gap to an existing page before proposing a new URL. Compare buyer needs with the actual cited evidence and ask what the organization can substantiate better: implementation instructions, limitations, compatibility, firsthand testing, price conditions, original findings, or expert interpretation.

Create an evidence record for consequential claims: claim, owner, source, date, methodology, population, and permitted wording. Replace generic superlatives with supported distinctions. Recheck product and competitor facts. Preserve useful long-form explanation; adding a short answer does not justify removing qualifications.

For third-party opportunities, record the source's relevance, observed recurrence, factual gap, relationship, and legitimate contribution available. A correction request, expert interview, useful open dataset, or real customer review is different from manufacturing endorsements. Do not buy fake independence, spam communities, or create repetitive microsites. Draft outreach only when useful; sending requires existing authorization.

## Prioritization and experiment record

Keep a small backlog scored qualitatively on buyer value, current gap, confidence in mechanism, effort, and downside. Fix broad access or factual failures ahead of speculative formatting changes. Numerical scoring is optional and should not pretend precision.

An experiment record should specify:

- Hypothesis and constrained stage; affected pages/topics.
- Exact intervention and preserved baseline/version.
- Primary metric, minimum useful effect, and business guardrail.
- Evaluation panel, comparison/holdout, time window, and missing-data rule.
- Owner, authorization, collection budget, and rollback/stop conditions.

Example hypothesis: buyers ask about migration constraints, but current documentation omits tested limitations. Add a substantiated migration guide, compare related prompts with an untreated topic cluster, and assess owned citation presence plus qualified guide conversions. Do not mix this with a site redesign and then attribute all movement to the guide.

Use randomized or staggered page/topic rollout when feasible. A matched untreated group improves a before/after comparison only if its pre-trends and exposure are credible. Difference-in-differences is descriptive without justified parallel trends and limited spillover. Domain-wide changes and model releases can contaminate controls.

Start the exposure clock with evidence of availability, while preserving the publication timestamp. Record fetch/index observations and platform changes; hidden processing may remain unknown. Set a maximum review horizon before collection. At that point: expand, revise, revert, or report inconclusive—never extend merely to hunt a positive result.

## Connect discovery with commercial outcomes

Maintain separate views for synthetic panel visibility, native platform exposure, identifiable AI referrals, and business outcomes. The populations and units differ. Import Google's dedicated impressions report [R7] and Bing citation exports [R10] with their filters, dates, aggregation rules, and missingness; do not manufacture conversions from them.

Define analytics conversions precisely: sessions with a qualifying event, qualified leads, purchases, or revenue. Report conversion rate using the matching session/user denominator and a consistent window. Preserve referrer and landing-page evidence without claiming untagged traffic is identifiable.

Use a business-appropriate lag window and allow cohorts to mature. Supplement identifiable referrals with customer-reported discovery, brand search, direct traffic, or CRM notes as separately labeled corroboration. These signals do not prove incremental AI impact. Consent-respecting causal tests or stronger observational designs are needed for that claim. Profound's visits study [R2] supports investigating lag, not assigning all subsequent traffic to a mention.

## Review and handoff

Report what changed, what the data can distinguish, and the next decision. Include the strongest counter-explanation. Expand only when relevance, correctness, user experience, and commercial guardrails survive. If no access to measurement exists, deliver an instrumented plan and specific evidence-backed fixes; call unmeasured results unmeasured.

Refresh this playbook's platform links when used. Keep a date-stamped change log in the engagement's own working records when definitions, panels, controls, or reports change; this reusable skill does not need an endless history of every client experiment.
