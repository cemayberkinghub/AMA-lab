# Class Start

Welcome. This folder is the normal student path for the class.

## First-read path

1. Read [`prerequisites.md`](prerequisites.md) before the session or at the start of setup time.
2. Read [`participant-guide.md`](participant-guide.md) for the lab objective, mental model, expected outputs, and live flow.
3. Keep [`worksheets.md`](worksheets.md) open as your primary workbook during the live lab.
4. Use [`scenario-handout.md`](scenario-handout.md) when the workbook asks you to anchor on the customer scenario.
5. Use [`prompts\`](prompts/) when the workbook names a prompt file to copy.
6. Use [`references.md`](references.md) when you need the core model or vocabulary.
7. Use [`troubleshooting.md`](troubleshooting.md) if a product surface, CLI step, agent file, or environment check does not work.

## What this lab is about

You will practice moving from a broad AI ambition to controlled, reviewable agent-system work. The lab uses a regulated design scenario to compare how different harnesses shape what an agent can see, do, remember, call, produce, and hand off.

The through-scenario is **AI-Assisted Estimation and Compliance in Regulated Design Work**. The goal is not to design the final customer system. The goal is to learn how to preserve context, make harness decisions visible, keep human authority explicit, and turn agent-system work into Spec -> Plan -> Build slices.

## Files you need during class

| Need | File |
|---|---|
| Preparation and readiness | [`prerequisites.md`](prerequisites.md) |
| Participant overview | [`participant-guide.md`](participant-guide.md) |
| Live sequence summary | [`lab-guide.md`](lab-guide.md) |
| Primary workbook | [`worksheets.md`](worksheets.md) |
| Scenario handout | [`scenario-handout.md`](scenario-handout.md) |
| Copy/paste prompts | [`prompts\`](prompts/) |
| Condensed exercise map | [`exercises.md`](exercises.md) |
| Mental model and vocabulary | [`references.md`](references.md) |
| Recovery and fallback | [`troubleshooting.md`](troubleshooting.md) |

## Repository areas you can ignore during normal participation

You do **not** need to open `specs\` during normal class participation. That folder preserves source, delivery rehearsal, and feature planning provenance for maintainers and reviewers.

You also do not need `facilitator\` unless the facilitator asks you to look at delivery support material. It is visible-safe, but it is not the normal student path.

## Expected outputs

By the end of the lab, you should have enough notes to explain:

- why a prompt alone is not enough for regulated design work;
- how `prompt -> context -> harness -> agent -> system boundary` helps diagnose agent-system quality;
- why `agent = model + harness`;
- how lower-control and higher-control harness surfaces differ;
- what a responsible first Spec -> Plan -> Build slice looks like; and
- what must remain human-owned when AI assists regulated design work.
