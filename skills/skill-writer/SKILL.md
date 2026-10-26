---
name: skill-writer
description: Create or refine an agent skill from a working procedure, recurring corrections, or supplied examples. Use when asked to "turn this into a skill", "save this workflow", or improve a SKILL.md, and when five distinct repetitions of the same actionable instruction are visible and merit a skill suggestion. Not for ordinary copywriting or silently monitoring other chats.
metadata:
  author: Reti Eedra
---

# Skill writer

Build skills from work the user actually does. Don't front-load a library of imagined workflows: capture the instructions they keep repeating, the corrections that mattered, and the checks that made the result reliable. An explicit request to create a skill is enough to start; the user does not have to repeat it five times first.

## Notice a reusable pattern

Use the current conversation and relevant material already supplied or authorized. Count distinct user instructions or corrections that express the same actionable requirement in comparable situations. Paraphrases can count; quoted instructions, assistant summaries, repeated copies of the same message, and several repetitions inside one utterance do not. Reconcile later corrections instead of counting contradictory instructions as agreement.

After five visible occurrences, suggest a skill once, naming the pattern and the evidence: “You've asked for [behavior] in these five tasks. Would you like me to save it as [skill name]?” Ask before creating it unless the user already requested or authorized creation. If declined, continue the task without repeating the suggestion unless the user reopens it. Fewer than five is not a reason to interrupt with speculative suggestions.

Five is Reti's workflow preference, not a proven threshold. This file does not run a background monitor or create cross-chat memory. If the available context does not establish a count, say so; do not invent prior requests or search unrelated conversations merely to reach five. Ongoing observation requires the host to expose this instruction and the relevant history. Do not claim that installing the skill alone enables it.

## Decide what to save

Inspect existing relevant skills before creating another one. Update the closest skill when the new instruction belongs to the same workflow. A general preference such as preferred spelling may belong in an existing user-instruction file, while a procedure with inputs, decisions, and checks may deserve a skill. Explain the fit without silently editing unrelated configuration.

Extract the smallest useful procedure from the examples: when it applies, what input it needs, which decisions differ from the agent's defaults, what successful output looks like, and what must be checked. Separate recurring rules from one-time details. Infer routine choices from context; ask only for missing information that changes scope or behavior.

## Write the trigger and instructions

Use a lowercase hyphenated folder name and a SKILL.md with YAML `name` and `description`. The description is a routing instruction: describe the job, ordinary phrases or situations that should activate it, and a nearby exclusion if confusion is likely. It should work with natural language; do not require a slash command or an exact password. Several relevant skills may compose, but this skill must not force unrelated ones to load.

Write a short body that changes decisions. Give a clear default, explain consequential exceptions, and remove generic advice the agent already follows. Use plain language an undergraduate reader can understand, connecting related ideas in natural sentences while keeping operational steps easy to scan. Preserve nuance without turning each rule into a long essay.

Include concrete inputs and acceptance criteria where they help. Put optional detail in references and say when to read it. Add scripts only for repeated operations that benefit from deterministic execution; run them before calling them working. Avoid placeholder folders, unnecessary frameworks, forbidden-word lists, and speculative edge cases.

Keep user choices and authorization boundaries intact. A skill about shipping code must distinguish preparing a PR from merging it. If a review loop is requested, specify who reviews, a bounded number of rounds, observable checks, the actual verdict, and what happens when issues remain. Never claim a reviewer approved work that was not reviewed, or let passing tests grant permission to merge. Preserve a recoverable version when updating existing instructions.

## Verify behavior and finish

Check the folder name, frontmatter, local reference links, and any scripts. Then try a realistic task and a nearby case where the skill should not apply; for this skill's repetition logic, use [the acceptance cases](references/acceptance-cases.md). Separate structural validation, manual reasoning, and actual agent executions in the report. If practical, compare outputs with and without the skill using the same inputs; don't claim an improvement from file validation alone.

Revise for observed failures, not imagined completeness. Report the saved location, trigger, core behavior, checks performed, and remaining limits. Save to the user's specified repository or location; publishing, installing, and pushing follow their requested scope. When researching format or authoring choices, consult [the source notes](references/sources.md) and refresh changing platform details from primary documentation.
