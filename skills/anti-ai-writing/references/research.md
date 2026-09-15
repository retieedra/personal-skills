# Research notes

Research checked: **15 September 2026**. These notes distinguish observed findings from editorial extrapolation. Papers were read; analyses and datasets were not independently replicated.

## Citation correction

The supplied OUP URL identifies **Chen et al. (section 2)**, not the requested Nature Human Behaviour paper by **Sourati et al. (section 1)**. Their exact citations follow. Do not attach the OUP DOI to the Sourati title; neither paper validates this skill.

## 1. Linguistic diversity and rewriting

**Zhivar Sourati, Farzan Karimi-Malekabadi, Meltem Ozcan, Colin McDaniel, Alireza Ziabari, Jackson Trager, Ala N. Tak, Meng Chen, Fred Morstatter, and Morteza Dehghani.** “The shrinking landscape of linguistic diversity in the age of large language models.” *Nature Human Behaviour*, **24 August 2026**. [Publisher](https://www.nature.com/articles/s41562-026-02550-0); [final author manuscript, v2](https://arxiv.org/html/2502.11266v2); [version history](https://arxiv.org/abs/2502.11266).

**Inspected:** Abstract, three studies, discussion, and methods in v2. The February 2025 v1 described four studies; these notes follow the final version.

**Methods and findings:** Seven datasets, over 880,000 texts. Longitudinal Reddit, Patch, and arXiv analyses associate inferred AI prevalence with lexical/syntactic variance changes; predictive relationships were nonsignificant for Patch. GPT-3.5, Llama 3, and Gemini rewrites also weakened some classifiers and lexical associations with measured author attributes. Significant complexity-variance reductions ranged from 21% to 50%.

**Limits:** Observational trends and Granger prediction do not establish causation. Older models, selected domains, and generic prompts limit generalization. Classifier changes do not demonstrate changed identities. Semantic similarity and a small human check cannot guarantee preserved nuance.

**Editorial extrapolation:** Preserve meaningful stylistic variation. Between-text convergence is different from shorter sentences or fewer unique words within one text; a more elaborate rewrite can still homogenize a collection.

## 2. Stylometry, not an editing prescription

**Rongzhi Chen, Shizhao Xiong, Jingqi He, and Gordon J. Ross.** “Stylometric detection of AI-generated texts: evidence from human and machine-written essays.” *Digital Scholarship in the Humanities*, advance article fqag064, **23 June 2026**. [Full publisher article and supplied URL](https://academic.oup.com/dsh/advance-article/doi/10.1093/llc/fqag064/8714041).

**Inspected:** Full HTML abstract, data, methods, four analyses, discussion, and limitations.

**Methods and findings:** The study compares 2,173 Aeon essays with 2,173 GPT-4o mini essays generated from matching titles using one fixed prompt. Function-word profiles feed Burrows' Delta variants, support-vector machines, and random forests. Experiments examine author aggregation, text length, training-set size, and transfer across topics. Random forests generally perform strongest; short samples produce more false positives. The generated collection is stylistically more uniform under this setup.

**Limits:** One model, prompt regime, and long-form essay genre; no validation for mixed authorship, human post-editing, or multilingual writing. Treating human essays as distinct authors is a dataset assumption. Classification performance here does not establish reliable authorship judgments for arbitrary drafts.

**Editorial extrapolation:** None of these results supports a forbidden-word list, deliberate randomness, or a detector score as a measure of writing quality. The paper is relevant context for stylistic regularity, not instructions for avoiding classification.

## 3. Assistance depends on model and interface

**Vishakh Padmakumar and He He.** “Does Writing with Language Models Reduce Content Diversity?” *International Conference on Learning Representations (ICLR)*, **2024**; initial preprint **11 September 2023**. [Official proceedings](https://proceedings.iclr.cc/paper_files/paper/2024/hash/02dec8877fb7c6aa9a79f81661baca7c-Abstract-Conference.html); [full author manuscript, v3](https://arxiv.org/html/2309.05196v3).

**Inspected:** Full manuscript, including recruitment, lexical/content measures, results, and Appendix D limitations.

**Methods and findings:** Thirty-eight US native-English writers with professional writing or editing experience produced 300 argumentative essays across ten topics. Conditions used no assistance, base GPT-3, or instruction-tuned InstructGPT in a continuation-suggestion interface. InstructGPT reduced collective lexical and content diversity; base GPT-3 did not show the same effect. The distributional changes came mainly from model-contributed text, with user-contributed text comparatively stable.

**Limits:** Two older models, a selected writer population, one genre, and one suggestion interface. Findings do not show that all models and collaboration patterns have the same effect. Personalized or conversational interventions were not tested.

**Editorial extrapolation:** Preserve a user's independently chosen direction and compare edits against their own wording. This is a plausible safeguard, not an experimentally established remedy. Claims about “AI writing” should name the relevant setting instead of assuming a universal effect.

## 4. Cultural convergence can accompany richer vocabulary

**Dhruv Agarwal, Mor Naaman, and Aditya Vashistha.** “AI Suggestions Homogenize Writing Toward Western Styles and Diminish Cultural Nuances.” *CHI 2025*, conference **26 April–1 May 2025**; inspected author manuscript v3 dated **12 March 2025**. [Publication DOI](https://doi.org/10.1145/3706598.3713564); [full author manuscript](https://arxiv.org/html/2409.11360v3).

**Inspected:** Experiment design, recruitment, lexical and semantic analyses, content coding, discussion, and limitations.

**Methods and findings:** A randomized between-subjects experiment involved 118 participants from India and the US, four English writing tasks, and 472 essays. GPT-4o autocomplete was compared with unaided writing. Embedding, classification, lexical, and qualitative analyses found assisted Indian writing converging toward the US comparison group, including shifts in cultural references. Productivity benefits were larger for US participants. Indian lexical diversity increased even as some group differences diminished.

**Limits:** Country is an incomplete proxy for culture; two national samples cannot represent their internal diversity or the world. Tasks were in English and the Indian recruitment pool was limited. Group-level comparisons do not demonstrate identical changes in every writer. Suggested personalization mitigations were not tested.

**Editorial extrapolation:** Preserve culturally situated expressions and examples. Increasing vocabulary variety alone does not protect cultural distinctiveness; avoid treating American conventions as neutral defaults.

## 5. Individual quality and collective diversity can diverge

**Anil R. Doshi and Oliver P. Hauser.** “Generative AI enhances individual creativity but reduces the collective diversity of novel content.” *Science Advances* **10(28), eadn5290, 12 July 2024**. [Publisher](https://doi.org/10.1126/sciadv.adn5290); [UCL publication record](https://discovery.ucl.ac.uk/id/eprint/10195027/); [author manuscript, v3](https://arxiv.org/pdf/2312.00506v3).

**Inspected:** Publisher results/discussion and author-manuscript methods, results, and tables. The March 2024 manuscript has a slightly different title: “Generative artificial intelligence enhances creativity but reduces the diversity of novel content.”

**Methods and findings:** After exclusions, 293 UK participants wrote eight-sentence stories with no AI ideas, an optional single GPT-4 idea, or up to five ideas. Six hundred separate evaluators provided 3,519 assessments. AI access improved novelty, usefulness, and writing ratings, particularly for participants with lower baseline creativity scores. Assisted stories were also more semantically similar to one another.

**Limits:** Short fiction, three prompts, predominantly nonprofessional writers, and fixed suggestions. Creativity ratings are not universal measures of writing quality. The experiment does not establish that assistance always harms creativity, or evaluate a personalized editing workflow.

**Editorial extrapolation:** Judge usefulness and originality separately. A polished individual draft can be valuable while a collection converges. Retaining the user's starting idea is sensible editorial practice, not a tested guarantee.

## 6. Detector output is not a quality or identity test

**Weixin Liang, Mert Yuksekgonul, Yining Mao, Eric Wu, and James Zou.** “GPT detectors are biased against non-native English writers.” *Patterns* **4(7), 100779, 10 July 2023**. [Publisher](https://doi.org/10.1016/j.patter.2023.100779); [full author manuscript, v3](https://arxiv.org/html/2304.02819v3).

**Inspected:** Results, detector-access details, sample construction, and limitations.

**Methods and findings:** Seven detectors, accessed 15 March 2023, were evaluated on 91 TOEFL essays from a Chinese educational forum and 88 US eighth-grade essays. Average false-positive classification was 61.22% for the TOEFL sample, much higher than for the US comparison sample. Word-choice interventions changed classifications, illustrating sensitivity to linguistic features rather than a dependable provenance signal.

**Limits:** Small, differently sourced cohorts have age, task, and proficiency differences; these are not controlled estimates for all native and non-native writers. Detector versions are historical, and the results do not benchmark tools available in 2026.

**Editorial extrapolation:** Do not use detector scores to grade authenticity, proficiency, or quality. Do not “correct” a language learner's distinctive voice merely because it scores suspiciously, or introduce mistakes to manipulate a score. Edit for the user's communicative purpose.

## What the skill does and does not inherit from this evidence

The sources motivate attention to three different outcomes: variation across writers, the substance and quality of an individual draft, and unreliable inferences about authorship. They are not interchangeable metrics.

The skill's minimal edits, voice notes, factual checks, and restraint are **editorial recommendations extrapolated from these concerns**. These papers do not test the skill, demonstrate that it reverses homogenization, or establish optimal sentence lengths, punctuation frequencies, vocabulary lists, or ratios of simple to complex syntax. Do not describe the workflow as a validated intervention or diagnose a person's culture, personality, or identity from their prose.
