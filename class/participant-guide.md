# Participant Guide

## Welcome

In this lab, you will practice turning a broad AI opportunity into controlled, reviewable agent-system work. The goal is not to produce a final system design. The goal is to learn how senior architects reason about context, harnesses, agents, human authority, and system boundaries.

## Learning objective

By the end, you should be able to:

- Explain why a prompt alone is not enough for regulated design work.
- Compare harness/control surfaces based on what an agent can see, do, remember, call, produce, and hand off.
- Use `prompt -> context -> harness -> agent -> system boundary` to reason about agent-system design.
- Transfer a realistic AI opportunity into Spec -> Plan -> Build without over-automating.

## Mental model

Use this model throughout the lab:

```text
prompt -> context -> harness -> agent -> system boundary
```

- **Prompt**: The immediate request. Useful, but too small to carry durable control by itself.
- **Context**: The durable facts, sources, preferences, constraints, and customer information the work depends on.
- **Harness**: The visible design object around the model: instructions, tools, grounding, memory, output contracts, evaluation, and handoff rules.
- **Agent**: The model plus its harness. In this lab, `agent = model + harness`.
- **System boundary**: Where the agent's responsibility ends and accountable human, business, compliance, and operational processes begin.

**Agent OS** is the portable operating model that emerges from deliberate harness engineering. It is not a literal operating system, product feature, runtime, orchestration system, single file, or layer beside the system boundary.

For each activity, ask:

1. What is the prompt asking for?
2. What context must be present and trustworthy?
3. What must the harness control?
4. What is the resulting agent allowed to do?
5. What decisions remain outside the agent's boundary?

## Lab flow

1. Use the regulated design scenario to set context and identify tensions to watch.
2. Use `prompts/m365-personalization-interview-prompt.md` with M365 Copilot to generate a copy/paste-ready Agent Operating Profile v1.
3. Convert that profile into baseline instructions, then use them as the basis for M365 Copilot Agent Builder and observe what instructions and corporate grounding can express.
4. Pivot to GitHub Copilot CLI and split the same baseline instructions into `copilot-instructions.md`, `strategy.agent.md`, and specialist-agent guidance.
5. Use the Strategy and CSA agents to draft a focused Spec -> Plan -> Build transfer for the scenario, expressed as reviewable task slices.
6. Compare harnesses using architectural evidence and project the same layers to Foundry.

During live delivery, expect sections 1-4 and section 5 steps A-B to be hands-on. Later GitHub Copilot CLI steps and the Spec -> Plan -> Build transfer may be facilitator-led with optional follow-along. The final harness comparison is conversation-driven.

## Files you will use

| File | When to use it |
|---|---|
| `scenario-handout.md` | At the beginning, to anchor the lab to a customer scenario theme |
| `worksheets.md` | Throughout the lab; this is your primary work surface |
| `prompts/README.md` | When the workbook tells you to copy a prompt |
| `prompts/*.md` | Only at the specific workbook step that names the prompt |

## Behavior expectations

- Stay practical and evidence-oriented.
- Prefer explicit boundaries over impressive automation claims.
- Keep human authority visible.
- Do not try to solve the entire customer problem.
- Treat examples as calibration, not as the only correct answer.

## Output expectations

| Segment | Expected output |
|---|---|
| Scenario setup | Tensions, risks, and human-authority questions to watch |
| Personalization | Local `agent-profile-baseline.md` file containing the copy/paste-ready Agent Operating Profile v1 from the M365 Copilot interview |
| Baseline instructions | Cross-platform role, operating principles, communication, challenge, evidence, ambiguity, and reuse rules |
| M365 Copilot Agent Builder | Instructions derived from the baseline structure, plus notes on corporate grounding and visible harness boundaries |
| GitHub Copilot CLI build-out | Split of the baseline instructions into `copilot-instructions.md`, `strategy.agent.md`, CSA-agent guidance, Learn MCP access, `/restart`, and `/env` |
| Spec transfer | Objective, constraints, non-goals, and success signal |
| Plan transfer | Approach, risks, validation, and boundary decisions |
| Build transfer | First reviewable build tasks and explicit out-of-scope items |
| Harness comparison | Differences in context, tool access, memory, outputs, handoffs, and what projects to Foundry |
