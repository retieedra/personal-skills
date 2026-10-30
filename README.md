# Personal skills

Research-backed AI skills by [Reti Eedra](https://retieedra.com). Practical instructions for writing with an individual voice, designing Grok bot workflows, operating answer-engine optimization, and running disciplined X Ads experiments.

## The collection

- **[Grok bot prompts](skills/grok-bot-prompts/SKILL.md)** — turn workflow ideas and meeting notes into copy-ready bot prompts, with context-building, voice learning, recurring steps, and explicit approval boundaries.

- **[Skill writer](skills/skill-writer/SKILL.md)** — turn repeated instructions and working procedures into focused skills, with natural-language triggers and practical checks. Suggest saving a workflow after five distinct visible repetitions; ask before creating unless already authorized.

- **[Anti-AI writing](skills/anti-ai-writing/SKILL.md)** — preserve the writer's voice, ideas, and linguistic choices while editing away generic model defaults. Informed by research on linguistic diversity and AI-assisted writing.
- **[AEO operator 2026](skills/aeo-operator-2026/SKILL.md)** — diagnose visibility across answer engines, build a defensible measurement program, and run evidence-led improvements. Includes Profound research and platform documentation.
- **[X Ads operator 2026](skills/x-ads-operator-2026/SKILL.md)** — plan, measure, and improve campaigns with explicit economics, conversion instrumentation, creative tests, and spending boundaries.

Each skill has a short `SKILL.md` entry point and supporting references. Start with the entry point; open the deeper material when the task needs it.

## Use a skill

Download or clone this repository, then copy the **whole skill folder**, including all supporting files and directories, into your agent's skills directory. For a local Codex setup, that directory is `~/.codex/skills/`.

```sh
git clone https://github.com/retieedra/personal-skills.git
mkdir -p ~/.codex/skills
cp -R personal-skills/skills/anti-ai-writing ~/.codex/skills/
```

Replace `anti-ai-writing` with another skill folder to install it. You can also read the instructions and adapt them to your own workflow.

Example requests:

- “Use grok-bot-prompts to turn these meeting notes into a post-call follow-up bot prompt. Learn my voice first, save email drafts, and ask for approval in Slack before sending.”

- “Use anti-ai-writing to edit this essay. Keep my phrasing where it carries my voice; use these two earlier pieces as references.”
- “Use aeo-operator-2026 to diagnose our answer-engine visibility and propose a measurable first experiment.”
- “Use x-ads-operator-2026 to audit these campaign exports against our target acquisition cost. Recommend changes without launching anything.”

## Research and maintenance

Research snapshot: **15 September 2026**. Source ledgers distinguish research findings, vendor observations, platform documentation, and operating recommendations. A year in a skill's name identifies the research snapshot; it does not make every underlying source a 2026 study.

The writing research includes two different papers: Sourati and colleagues' *The shrinking landscape of linguistic diversity in the age of large language models* in **Nature Human Behaviour**, and Chen and colleagues' *Stylometric detection of AI-generated texts: evidence from human and machine-written essays* in **Digital Scholarship in the Humanities**. Their findings and limitations are documented separately in the writing skill's references.

Recheck platform behavior and documentation before relying on changing controls, APIs, or numeric defaults. The skills do not promise AI-detector outcomes, search inclusion, or advertising returns.

The research papers and documentation remain with their respective authors and publishers. This repository contains original practical instructions and source summaries, not reproductions of the papers.
