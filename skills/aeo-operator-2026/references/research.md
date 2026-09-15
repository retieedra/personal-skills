# Evidence ledger

Reviewed 2026-09-15. Twelve evidence entries covering thirteen primary sources; dates below distinguish publication, measurement, and retrieval. Dynamic documentation may change. Profound operates a commercial measurement platform: its studies are valuable first-party evidence, not independent validation or population censuses. Recommendations in this package are an operator's synthesis unless explicitly attributed.

## R1 — Sampling frequency and prompt composition

[Profound: Is once a day enough?](https://www.tryprofound.com/blog/is-once-a-day-enough), Jennifer Zou, 2026-07-08. **Vendor measurement experiment.** June 1–14, 2026; 753 prompts × seven US platforms = 5,271 configurations; parallel once- and ten-times-daily setups.

Reported portfolio visibility was 78.7% versus 80.4%; citation share 10.24% versus 9.99%. More repetitions reduced reported daily variation more for citation share than mentions. Prompt resampling showed substantial composition sensitivity.

Limits: two weeks, proprietary prompts, assumptions about independence, no representative consumer sampling. Published approximate run totals do not directly reconcile with configurations × days × nominal frequency; the displayed standard-error notation is also ambiguous. Do not reuse those formulas or imply independent replication. Directional lesson: evaluate panel composition and drift before buying repetition; estimate uncertainty from your actual data.

## R2 — Mentions, visits, and attribution lag

[Profound: The AI mention effect](https://www.tryprofound.com/blog/the-ai-mention-effect), Nikolas Laskaris, 2026-07-01. **Vendor observational panel study.** More than two million conversations plus browsing records, January–June 2026, US opt-in users, ChatGPT/Gemini/AI Overviews.

Exposure required a brand appearing in the answer but not the prompt. Seven-day visits were compared with a linear forecast from three preceding seven-day windows; recent brand interest was filtered. User-clustered bootstrap: 2,000 replicates. ChatGPT visit rate: 6.39% versus forecast 4.33%, +2.07 percentage points, 95% interval [1.67, 2.48].

This is not randomized, not purchase evidence, and does not eliminate selection bias. Only 42% of observed first visits occurred within 24 hours. Partial-June ChatGPT referral parameters appeared on 2.47% of downstream visits; that is not the fraction of all AI traffic analytics can detect. Use lag-aware outcomes; do not apply a universal uplift or attribution multiplier.

## R3 — Where citations originate

[Profound: Where do AI citations come from?](https://www.tryprofound.com/blog/where-do-ai-citations-come-from), Jasman Singh, 2026-07-30. **Vendor observational citation analysis.** April 16–July 16, 2026; 11.84 billion citations, eight engines, 8,061 active categories; 7,542 had at least 100 citations.

Domains were classified using a 3.02-million-domain map covering 98.3% of global citation volume. Industry summaries weight each category equally across 29 industries; per-engine cells have minimum coverage thresholds.

Critical denominator: “brand” means websites operated by any company, including competitors, not necessarily the tracked brand. Earned includes institutions and PR wire; social includes UGC. The classification and industry labels can be wrong or stale; region/language differences are not controlled. Use industry benchmarks to form hypotheses, not to prescribe identical channel budgets or claim an owned-site share.

## R4 — Language and geographic composition

[Profound: How query language reshapes AI citations](https://www.tryprofound.com/blog/how-query-language-reshapes-ai-citations), Davis McCain, 2026-04-21. **Vendor observational citation analysis.** March 2026; 3.25 billion citations, seven models, 14 countries, filtered to designated native-language prompts; English US/UK/Australia comparison baseline.

Reported source mixes differ substantially by model and language. The nested social-platform percentages describe shares within social citations, not all citations.

Country selection follows citation volume; language is not randomized, and prompt/customer composition can confound the comparison. A country is not linguistically uniform. The finding supports separate local-language panels, not the claim that language alone caused every observed difference. Determine local source opportunities from the actual buyer panel.

## R5 — Google's current optimization guidance

[Google Search Central: Optimizing your website for generative AI features](https://developers.google.com/search/docs/fundamentals/ai-optimization-guide), updated 2026-07-10; reviewed 2026-09-15. **Platform documentation, not an intervention study.**

Google describes indexed retrieval and query fan-out, retaining ordinary Search eligibility and quality principles. It advises useful original content and warns against multiplying pages to target every query variant. It says Google Search ignores `llms.txt` for visibility, while allowing other systems to use it. These statements apply to Google, not every engine.

The page links the Search Console inclusion control. Recheck linked documentation before giving advice; eligibility does not guarantee serving, and document guidance does not quantify the causal lift of any individual edit.

## R6 — Google generative-AI inclusion controls

[Search Console Help: Search generative AI control](https://support.google.com/webmasters/answer/16908024), reviewed 2026-09-15; page states worldwide rollout as of 2026-08-31. **Platform documentation.**

Documents an inclusion/exclusion setting for Search generative-AI features, default inclusion and parent-property inheritance. The setting is distinct from complete Search exclusion and model-training controls. Processing is not instantaneous.

Operational implication: inspect effective settings for the relevant property. Do not change a publisher's exclusion choice merely to satisfy an audit. No experimental sample or effect size applies. Verify availability and current wording during execution.

## R7 — Google generative-AI performance reporting

[Search Console Help: Generative AI performance report (Search)](https://support.google.com/webmasters/answer/16984139), reviewed 2026-09-15; page states worldwide rollout as of 2026-08-31. **Platform measurement documentation.**

Documents AI Overviews/AI Mode impressions with page, country, date, and device dimensions. The dedicated report draws from Web performance data; it is not a source of isolated AI conversions or prompt-level CTR. Property and page aggregation differ, so summing rows can disagree with chart totals. Dates use Pacific Time; recent data may be preliminary.

The page still contains a rollout caveat and notes insufficient impressions as a reason for absence. Check actual availability. Exported unavailable values may become zeros: preserve missingness from the UI/source metadata before analysis. Do not double-count this report alongside its containing Web totals.

## R8 — OpenAI crawler roles

[OpenAI: Overview of OpenAI Crawlers](https://developers.openai.com/api/docs/bots), reviewed 2026-09-15; no publication date shown. **Platform documentation.**

OAI-SearchBot serves search discovery; GPTBot concerns potential foundation-model training; ChatGPT-User performs certain user-triggered actions and does not determine Search inclusion. Search and training controls are independent. The page publishes IP ranges and notes that user-triggered robots behavior differs from automatic crawling.

Inspect relevant access policies and current official ranges, preserving the owner's choices. A successful request is access evidence, not proof of ranking, citation, or training. Bot strings and ranges change; do not freeze them in a permanent allowlist or assume all ChatGPT traffic is the same activity.

## R9 — Perplexity crawler roles

[Perplexity: Crawlers](https://docs.perplexity.ai/docs/resources/perplexity-crawlers), reviewed 2026-09-15; no publication date shown. **Platform documentation.**

PerplexityBot supports search results rather than foundation-model training. Perplexity-User supports user-requested fetches, with different robots behavior. The documentation recommends combining user-agent checks with current published IP ranges for WAF configuration.

This describes platform behavior, not a measured inclusion benefit. Test the actual relevant route and infrastructure; do not remove broad security controls because one simulated request worked. Fetch success is not an index or citation guarantee.

## R10 — Bing AI Performance

[Bing: Introducing AI Performance in Bing Webmaster Tools Public Preview](https://blogs.bing.com/webmaster/February-2026/Introducing-AI-Performance-in-Bing-Webmaster-Tools-Public-Preview), published 2026-02-10; [Bing: New AI Visibility Insights—Intents, Topics, Citation Share, Compare](https://blogs.bing.com/search/June-2026/New-AI-Visibility-Insights-in-Bing-Webmaster-Tools-Intents-Topics-Citation-Share-Compare), published 2026-06-16. Both reviewed 2026-09-15. **Official platform measurement announcements.**

The February announcement describes visible citations across Microsoft Copilot, Bing AI summaries, and select partner integrations. Average cited pages aggregates across supported surfaces. Grounding queries are retrieval key phrases; their displayed data represents a sample of citation activity. Citation counts do not establish page ranking, importance, or answer placement.

The June announcement begins a global preview rollout and defines Citation Share as a site's citations divided by all sites' citations for the same grounding query. It explicitly describes the metric as observational, not traffic share or a quality score. Changes can reflect model updates, demand, freshness, competing content, and partner refresh cycles; a comparison does not establish causation. Retain report filters and feature availability with every export, and keep these observations separate from synthetic panel rates with different populations.

## R11 — Foundational GEO experiment

[Aggarwal et al.: GEO: Generative Engine Optimization](https://arxiv.org/html/2311.09735v3), v3 2024-06-28; KDD 2024. **Academic benchmark experiment.** GEO-bench contains 10,000 queries with 8,000/1,000/1,000 train/validation/test splits, incorporating adapted search queries and synthetic questions. Main tests used five retrieved sources, GPT-3.5-turbo, and five seeds.

Content interventions improved position-adjusted attributed-word and model-judged impression metrics in this setup. The commonly repeated “up to 40%” is not traffic, conversion, or universal citation-rate uplift. The Perplexity experiment used 200 test examples with supplied source files, not an ordinary open-web ranking intervention.

Evidence enrichment is worth testing; do not manufacture quotations or statistics to imitate the benchmark. Fixed candidate sources bypass discovery constraints. Use the newer pipeline study below to understand this limitation.

## R12 — Retrieval can reverse generation-only gains

[Kim et al.: SAGEO Arena](https://arxiv.org/html/2602.12187v2), submitted 2026-02-12, revised 2026-08-07; arXiv record says accepted at KDD 2026. **Academic pipeline experiment.** 2,700 queries across nine domains; 171,003 web documents. Default pipeline: BM25 retrieval, Qwen3-Reranker-4B, GPT-5-mini; alternative components also tested.

The authors measured retrieval, reranking, and citation separately. Many body-only rewrites reduced upstream visibility; structural-field work performed differently. Targets were chosen from documents already reaching the baseline generation stage, limiting conclusions for entirely undiscovered pages.

The benchmark approximates search, excluding proprietary commercial ranking and user-behavior signals. It does not reveal any engine's production algorithm. Operator inference: preserve topical clarity and assess the whole observable path instead of treating a supplied-context citation gain as evidence of discoverability.

## Applying the evidence

Use platform documentation for current controls; use vendor studies to choose plausible questions; use experiments to motivate tests within their tested scope. When a source conflicts with another, compare dates, populations, and definitions before choosing an interpretation. None of these sources warrants a promised ranking, mention, referral, or conversion outcome. Do not describe materials dated after 2026-09-15 as reviewed evidence.
