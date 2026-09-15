---
name: aeo-operator-2026
description: Diagnoses and improves a brand's visibility in AI answers using representative prompt panels, technical checks, evidence-led content, third-party sources, and controlled measurement. Use for AEO or GEO audits, operating plans, experiments, and performance investigations.
---

# AEO operator 2026

Improve how accurately relevant AI answers discover, describe, and recommend a business, and connect that work to qualified customer outcomes. Treat answer engine optimization (AEO) as a measured discovery program, not a promise of mentions.

Research reviewed **2026-09-15**. This is an independent synthesis, informed especially by Profound research; it is not an official Profound playbook. Read [the evidence ledger](references/research.md) when making research claims, and [the operating playbook](references/operating-playbook.md) for measurement definitions and execution examples. Recheck live platform documentation before changing controls or interpreting reports.

## 1. Frame the decision

Establish the offer, buyers, countries, languages, competitors, owned domains, conversion event, and decision horizon. Inventory authorized access to analytics, search consoles, server logs, prompt tracking, and content. Use supplied data first; state gaps and continue useful work. An audit does not imply permission to buy access, change accounts, send outreach, or publish. Honor existing authorization without repeatedly requesting it.

Choose the question: absent from consideration, inaccurately described, weak owned-source citations, poor traffic quality, or unexplained movement. A single screenshot can illustrate a failure; it cannot estimate prevalence.

## 2. Build a defensible prompt panel

Use customer questions, sales objections, site-search terms, and available real-conversation research to identify needs. Search keywords are clues, not measured AI prompt demand. Label generated prompts as synthetic and never invent volumes.

Stratify by buyer intent, product, locale, and language. Separate unbranded discovery from branded navigation and competitor comparison. Include natural phrasing variants and representative follow-ups where relevant. Keep a frozen evaluation panel; explore new prompts separately, then version additions. Preserve provenance and weighting so apparent gains cannot come from easier questions.

Measure relevant engines separately: consumer ChatGPT search, Google AI Overviews, AI Mode, Gemini, Perplexity, or Copilot as appropriate. APIs and consumer interfaces are different test conditions. Record surface, date, location, language, search mode, account context, and known model. Avoid carrying prior conversations into independent observations.

Pilot repeated runs across days and a subset within days. Let observed variance, panel breadth, decision size, and budget determine cadence. Profound's large-panel cadence study does not establish that one observation is sufficient for a small niche panel. [R1]

## 3. Define success before collecting more data

Keep these distinct, with explicit denominators:

- **Mention presence:** valid observations naming the brand / valid observations.
- **Owned citation presence:** valid observations citing an owned URL / valid observations.
- **Owned citation share:** owned citation units / all citation units, using one documented deduplication rule.
- **Recommendation and accuracy:** separately coded answer meaning, supported by excerpts and reviewed ambiguous cases.
- **Referral and conversion:** measured sessions, qualified outcomes, and revenue under a stated attribution model and window.

Report counts, missing-run coverage, platform slices, and uncertainty alongside rates. No AI Overview is a valid observed absence; a failed fetch is missing data. Do not divide site visits by synthetic prompt runs and call it CTR. Do not interpret citation share as market share.

## 4. Diagnose the constrained stage

Distinguish discovery, successful fetch, rendering, index eligibility, retrieval, visible citation, brand representation, and customer action. These are diagnostic stages, not an assertion that every engine exposes the same pipeline. A crawler hit proves neither indexing nor inclusion. A missing citation does not reveal which hidden stage failed. [R8, R9, R12]

Inspect relevant status codes, redirects, canonicalization, robots rules, indexing/snippet controls, sitemaps, internal links, text availability, and CDN/WAF behavior. Verify actual crawler identity; a spoofed user-agent test only checks that request's response. Separate search crawling from training permissions and user-initiated fetches.

For Google, check indexed/snippet eligibility and the current Search Console generative-AI inclusion control, including inheritance. Use its dedicated impressions report when available; check report coverage and aggregation. Bing citation reporting is another observation source, not a causal explanation. [R5–R10]

## 5. Improve the evidence buyers need

Resolve factual contradictions and access failures before multiplying pages. Connect each proposed edit to a documented buyer question and observed gap. Favor clear product facts, qualifications, pricing conditions, comparisons, original data with methods, firsthand examples, and genuinely useful explanations. Preserve exact entity names and meaningful domain vocabulary.

Provide a concise answer where useful, with supporting detail and evidence nearby. Use headings, tables, diagrams, or FAQs when they help the reader; no universal answer length, schema, or `llms.txt` ritual is required. Avoid fabricated statistics, review manipulation, hidden instructions, and mass near-duplicate pages. [R5, R11]

Inspect which independent sources actually inform the target category. Seek legitimate corrections, expert participation, partnerships, and editorial coverage where relevant. Distinguish company websites in general from your owned domain; a category-wide citation mix is not your brand's share. [R3, R4]

## 6. Run bounded experiments

Prioritize by buyer value, observed gap, plausible mechanism, evidence strength, cost, and reversibility. Predeclare the changed pages, primary metric, minimum useful effect, guardrails, comparison group, and review date. Prefer matched untreated topics or staggered rollout; monitor spillover.

Track publication, first observed fetch, indexing evidence, citations, and outcomes separately. Wait for plausible processing and customer-decision lag; use a declared maximum observation window rather than extending until the result looks favorable. Compare stable panels over comparable periods, accounting for releases, campaigns, and seasonality.

Expand when improvement survives uncertainty, relevant slices, and quality checks. Iterate when the hypothesized stage remains blocked. Stop or revert harmful changes. Label unresolved or uncontrolled before/after results inconclusive. Missing referral tags do not justify attributing all later direct visits to AI. [R2]

## Deliver the next decision

Return the main diagnosis, strongest evidence, prioritized actions, and a measurable next experiment. Link supporting observations and disclose uncertainty. Scale detail to the task; create only the artifacts needed to act.
