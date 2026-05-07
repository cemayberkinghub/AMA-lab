# Exercises

Use this as a condensed exercise map. The primary workbook is [`worksheets.md`](worksheets.md), with the full scenario in [`scenario-handout.md`](scenario-handout.md) and copy/paste prompts in [`prompts\`](prompts/).

If the facilitator asks you to work in the full workbook, use `worksheets.md` instead of this summary.

## 1. Scenario setup

Read the scenario summary:

> A regulated design and construction customer wants AI to read technical plans, apply rules and standards, generate first-pass design/cost estimates, and learn from expert corrections.

Do **not** solve the scenario yet. Mark tensions to watch.

| Watch item | Notes |
|---|---|
| Speed, accuracy, compliance, and accountability conflict | |
| Where human authority must remain explicit | |
| Where the customer is asking for too much in one system | |
| Where evidence or reviewability will matter | |
| What you want to test across harnesses | |

## 2. Agent OS Personalization

Use M365 Copilot as an interviewer. Ask it to help capture your Agent OS baseline context. It should ask one question at a time and produce Markdown only after you ask it to generate the final profile.

Save the result locally as `agent-profile-baseline.md`.

Good enough means the profile captures how you reason, challenge assumptions, handle ambiguity, communicate, and name red lines.

## 3. Baseline instruction structure

Review `agent-profile-baseline.md` and separate reusable operating rules from product-specific or scenario-specific details.

| Baseline component | What to include | Notes |
|---|---|---|
| Role and scope | What the agent is for and not for | |
| Operating principles | Strong opinions, tradeoffs, quality bar | |
| Communication rules | Tone, structure, challenge style | |
| Escalation rules | When to slow down, ask, or flag risk | |
| Evidence rules | Sources, assumptions, uncertainty | |
| Reuse guidance | What travels across platforms | |

## 4. M365 harness observation

Apply the baseline in the M365 surface and capture observations.

| M365 observation | Notes |
|---|---|
| Instructions / behavior | |
| Enterprise grounding | |
| External knowledge or MCP access | |
| Memory or session continuity | |
| Permissions and policy guardrails | |
| What remains implicit | |

## 5. GitHub Copilot CLI build-out

Use the same baseline to observe a higher-control file-backed harness.

| Step | Output to draft or inspect | Question |
|---|---|---|
| Shared instructions | `$HOME\.copilot\copilot-instructions.md` | What belongs everywhere? |
| Strategy agent | `$HOME\.copilot\agents\strategy.agent.md` | What belongs in strategy-specific behavior? |
| CSA agent | `$HOME\.copilot\agents\cloud-solution-architect.agent.md` | What belongs in Microsoft architecture review and Learn MCP access? |
| State check | `/restart` and `/env` | What changed in active context? |

Layering check:

| Guidance candidate | Shared instructions | Strategy agent | CSA agent | Outside harness | Why |
|---|---|---|---|---|---|
| Durable context | | | | | |
| General operating rules | | | | | |
| Strategy-specific reasoning | | | | | |
| Microsoft technical depth | | | | | |
| Learn MCP access | | | | | |
| Escalation rules | | | | | |
| Evaluation expectations | | | | | |

## 6. Spec -> Plan -> Build transfer

Return to the scenario. Do not produce a final architecture recommendation. Create a responsible first slice.

### Spec slice

| Spec concern | Draft |
|---|---|
| Objective | |
| Primary users or stakeholders | |
| User value | |
| Constraints | |
| Assumptions | |
| Success criteria | |
| Out of scope | |

### Plan slice

| Planning decision | Draft |
|---|---|
| Recommended approach | |
| Durable context needed | |
| Harness/control-surface assumptions | |
| Tradeoffs to expose | |
| Validation or review method | |
| Revisit trigger | |

### Build / task slices

| Build slice | Artifact or decision output | Depends on | Review evidence |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

## 7. Harness comparison and Foundry projection

| Layer | M365 Copilot Studio / Agent Builder side | GitHub Copilot CLI side | Foundry projection |
|---|---|---|---|
| Model and runtime | | | |
| Tools / MCP / connectors | | | |
| Context and knowledge | | | |
| Permissions and governance | | | |
| Memory and state | | | |
| Orchestration and handoff | | | |
| Review evidence | | | |

Final reflection:

> This work should not start with a final answer because the most important design decisions are __________, __________, and __________.
