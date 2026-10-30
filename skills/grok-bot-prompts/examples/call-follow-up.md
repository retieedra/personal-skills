# Example: Reti's call-follow-up scheduler

This is the user's original workflow, lightly edited for spelling and structure. It is an example prompt to give a bot, not authorization for the prompt-writing agent to access accounts or activate a scheduler. The two Calendly links are specific to this example; their actual URLs must be learned from the connected context.

## Copy-ready prompt

```text
I want to build an email follow-up scheduler after calls.

The first step is building the context and understanding for this flow. Please access a) Attio, b) my email, c) Granola, and d) Slack.

First, go through all of my emails. Map them by email address to the different companies in Attio and identify what deal stage they were in when I sent each email. The goal is to learn the shape of the follow-up email after calls at different stages of a deal. For example, the follow-up after a discovery call is different from a follow-up later in the process.

There are also two different Calendly links for different products. Make sure you understand which link goes with which product; that context comes from Granola.

Learn the general voice and style of my follow-up emails after calls, and create a voice.md file that you will use when writing emails in the future.

This is how the flow should run:

Every hour, check whether new calls have happened through a) Calendly or b) Google Calendar when there is an external attendee. Match the call to the company in Attio and assess what stage the deal is at.

Read the call transcript as well. The transcript is the main source of truth for what happened on the call. Use it together with voice.md and relevant company data from Attio to draft the follow-up email.

First save the email in my email drafts, and send me a DM in Slack with the draft, asking for approval or feedback.

You must never send the email without my explicit approval. Only after I approve the draft should you send it. If I give feedback, revise the draft and bring it back to me for approval.
```

## How to use this example

Preserve the sequence: learn from real history, connect examples to business context, save reusable voice guidance, define a recurring trigger, gather fresh evidence, and route a draft for approval.

For a production prompt, apply the operational details in [workflow-patterns.md](../workflow-patterns.md), including historical-stage evidence, coverage reporting, duplicate prevention, and missing transcripts. Keep those details proportionate to the request rather than turning every prompt into a long checklist.
