# Participant Workbook

This workbook is your working surface for the lab. Use it to capture just enough evidence at each step to compare harnesses and turn the scenario into controlled, reviewable work.

> **Lab Intent:** The scenario sets the stage. Do not try to solve it at the beginning.

## Lab path

| Step | What you do | What to capture |
|---:|---|---|
| 1 | Anchor the lab context to a customer scenario | Tensions, risks, and questions to keep in mind |
| 2 | Complete the Agent OS Personalization interview | Your judgment, working style, decision posture, and red lines |
| 3 | Convert the profile into baseline instructions | Reusable instruction structure that can travel across platforms |
| 4 | Build with M365 Copilot Agent Builder | What instructions and corporate grounding can express |
| 5 | Pivot to GitHub Copilot CLI and build the multi-agent equivalent | What becomes explicit in files, instructions, agents, tools, and environment state |
| 6 | Transfer to Spec -> Plan -> Build | A responsible first slice with reviewable tasks, not a final solution |
| 7 | Compare harnesses and project to Foundry | What each surface makes easier, what it makes visible, and what carries forward |

## Live delivery mode

The lab is intentionally facilitator-led after the first hands-on build steps. Follow along where it helps, but prioritize the harness lesson over completing every artifact live.

| Segment | Mode | What this means |
|---|---|---|
| Sections 1-4 | Hands-on | Work through the scenario anchor, personalization interview, baseline file, and M365 Copilot Agent Builder setup yourself. |
| Section 5, Steps A-B | Hands-on | Update `$HOME\.copilot\copilot-instructions.md` and create `$HOME\.copilot\agents\strategy.agent.md`. |
| Section 5, Steps C-F | Facilitator demo; optional follow-along | Observe the CSA agent, Learn MCP configuration, layering check, `/restart`, and `/env`. |
| Section 6 | Facilitator demo; optional follow-along | Watch the Strategy and CSA agents turn the scenario into Spec -> Plan -> Build slices; follow along if your environment is ready. |
| Section 7 | Conversation-driven | Use your notes to compare harness/control surfaces and project the pattern to Foundry; the table is a discussion aid, not a form-completion exercise. |

## 1. Scenario setup: customer theme

### Purpose

Anchor the underlying lab context to a customer scenario. This scenario should stay in the background until you have seen both harness surfaces.

### Input

Use `scenario-handout.md`.

### Instructions

Read the scenario and mark only the tensions you want to watch during the lab.

Do not complete the full scenario challenge yet. You will return to it in Section 6 after building both harness surfaces.

### Good enough means

You have named the main risk patterns without attempting a solution.

### Avoid

Do not design the target architecture yet. Do not debate which product should solve the problem.

### Workspace

| Watch item | Notes |
|---|---|
| Where speed, accuracy, compliance, and accountability conflict | |
| Where human authority must remain explicit | |
| Where the customer is asking for too much in one system | |
| Where evidence or reviewability will matter | |
| What you want to test as you move across harnesses | |

## 2. Agent OS Personalization

### Purpose

Use M365 Copilot as an interviewer to surface the judgment and operating style that should shape agent behavior across scenarios.

### Input

Copy `prompts/m365-personalization-interview-prompt.md` into M365 Copilot and answer based on your personal style, strategic mindset, and architectural approach.

### Instructions

Have M365 Copilot interview you one question at a time. Answer so the agent can frame problems, make tradeoffs, challenge assumptions, and communicate like you would. When the interview is complete, say "generate the Markdown" and save the copy/paste-ready Agent Operating Profile v1.

If you are unsure which prompt to use, check `prompts/README.md`.

Expect questions about:

- How you think and make decisions
- Where you have strong opinions or non-obvious views
- How you distinguish useful guidance from shallow or risky guidance
- How you communicate, structure advice, and challenge assumptions
- How you handle ambiguity, tradeoffs, and incomplete context

### Output

Save the results into a local file named `agent-profile-baseline.md`. Keep this file in the same local folder as this workbook and the `prompts\` folder if you want to use the relative paths shown later in Section 5.

### Good enough means

You have an Agent Operating Profile v1 Markdown draft that describes how the agent should reason, communicate, challenge, escalate, and handle ambiguity across scenarios.

### Avoid

Do not skip the interview and draft from scratch. Do not treat the generated Markdown as final without turning it into baseline instructions in the next step.

## 3. Baseline Instruction Structure

### Purpose

Convert the generated Agent Operating Profile v1 into a reusable baseline instruction structure that can travel across harnesses and scenarios. Think of this as the practical constitution for the agent's baseline behavior, written as instructions.

### Input

Use `agent-profile-baseline.md` and any refinements you make during validation.

### Instructions

Review the generated profile, tighten vague language, and make changes directly within the `agent-profile-baseline.md` file. Turn it into instructions that can be reused across platforms. Separate what belongs everywhere from what is platform- or scenario-specific.

### Good enough means

You have a baseline instruction structure that can become M365 Copilot Agent Builder instructions (and later split into `copilot-instructions.md` and specialist agent files).

### Avoid

Do not make this a generic persona prompt. Do not bake one customer scenario or product surface into the baseline.

### Workspace

| Baseline instruction component | What to include | Notes |
|---|---|---|
| Role and scope | What the agent is for, and what it is not for | |
| Operating principles | Strong opinions, decision style, tradeoffs, and quality bar | |
| Communication rules | Tone, structure, level of detail, and challenge style | |
| Challenge and escalation rules | When to push back, slow down, ask, or flag risk | |
| Evidence and ambiguity rules | How to handle weak context, uncertainty, assumptions, and sources | |
| Reuse guidance | What belongs across platforms vs. what should stay platform- or scenario-specific | |

## 4. M365 Copilot Agent Builder

### Purpose

Apply the baseline instructions in a lower-control product harness and observe what that surface expresses well.

### Input

Use `agent-profile-baseline.md`.

### Instructions

Copy the contents from `agent-profile-baseline.md` into the "M365 Copilot Agent Builder -> New Agent -> Instructions" block. Add or consider corporate grounding. Capture what the surface can express through instructions and Microsoft 365 work context.

### Good enough means

You can say what transferred cleanly, what had to be compressed, and what corporate grounding makes easier.

### Avoid

Do not turn this into a feature walkthrough. Stay focused on harness controls.

### Workspace

Review these capabilities when creating your agent. Take a few quick notes--on paper, in your head, or in this doc--because you will use these observations for comparison later in the lab.

| M365 Copilot observation | Notes |
|---|---|
| Execution: Model choice | |
| Context: Instructions (behavior) | |
| Knowledge: Enterprise data | |
| Knowledge: External websites | |
| Memory: What gets remembered? | |
| Tools: MCP Server, external | |
| Permission: User identity, policy guardrails | |
| What changes if this were Copilot Studio? | |

## 5. GitHub Copilot CLI build-out

### Purpose

Move the same operating model into a higher-control surface where shared instructions, role-specific agents, tools, local files, MCP configuration, and environment state are more explicit.

### Input

Use `agent-profile-baseline.md`, your M365 Copilot Agent Builder observations, and the prompt files in `prompts\`. The simplified prompts below assume GitHub Copilot CLI is running from the local folder that contains `agent-profile-baseline.md`, `worksheets.md`, and the `prompts\` subfolder; otherwise, update the paths before running them.

### Instructions

Use AI to draft each file, then review and correct the output. Your job is to decide what belongs in shared CLI instructions, what belongs in a strategy agent, what belongs in a CSA agent, and what should remain outside the agent harness.

Use `prompts/README.md` as the index for the prompt files in Steps A-C.

If the GitHub Copilot CLI setup, file paths, or custom-agent behavior get messy, stop troubleshooting and watch the facilitator demo. Capture what the harness makes visible or difficult; that observation is the learning objective.

### Good enough means

You can explain why `copilot-instructions.md`, `strategy.agent.md`, and `cloud-solution-architect.agent.md` should not collapse into one file, and you can point to what `/restart` and `/env` make visible.

### Avoid

Do not overclaim orchestration. Multiple specialist agents are present, but this is not yet an automated handoff workflow.

### Step A: Map shared guidance to `copilot-instructions.md`

Use the following prompt in GitHub Copilot CLI to draft shared instructions from your baseline file, workbook observations, and prompt template:

```text
Use `.\agent-profile-baseline.md`, `.\worksheets.md`, and `.\prompts\create-copilot-instructions.md` to draft the global instructions file at `$HOME\.copilot\copilot-instructions.md`.
```

### Step B: Break out `strategy.agent.md`

Use the following prompt in GitHub Copilot CLI to separate strategy-specific behavior into a custom agent file and avoid duplication with the global instructions.

```text
Use `.\agent-profile-baseline.md`, `$HOME\.copilot\copilot-instructions.md`, and `.\prompts\create-strategy-agent.md` to draft `$HOME\.copilot\agents\strategy.agent.md`.
Keep shared guidance in `copilot-instructions.md`; put only strategy-specific decision framing, tradeoff posture, challenge behavior, and communication style in the Strategy agent.
```

> **Insight:** The strategy agent would be a powerful place to add Work IQ, but company policy prevents us from adding this today. Also, your current user context is your public GitHub account, which does not have access to your corporate work data.

### Step C: Add a Cloud Solution Architect agent with Learn MCP

Facilitator demo; follow along if your environment is ready.

This step adds a second GitHub Copilot CLI custom agent. The aha is that once shared base instructions exist, adding another specialist agent is a separate file-backed harness decision: easy to inspect, easy to attach an MCP server to, and a first glimpse of multi-agent design without introducing orchestration yet.

Use the following prompt in GitHub Copilot CLI to separate cloud solution architect-specific behavior into a custom agent file and avoid duplication with both the global instructions and the strategy agent instructions. This CSA agent configures access to the Microsoft Learn MCP Server.

```text
Use `.\agent-profile-baseline.md`, `$HOME\.copilot\copilot-instructions.md`, `$HOME\.copilot\agents\strategy.agent.md`, and `.\prompts\create-cloud-solution-architect-agent.md` to draft `$HOME\.copilot\agents\cloud-solution-architect.agent.md`.
Keep shared guidance and strategy-specific behavior out of the CSA agent; include CSA-specific architecture review behavior and Microsoft Learn MCP Server configuration.
```

### Step D: Check the layering

Facilitator demo; follow along if your environment is ready.

After drafting the shared instructions and agent files, use this table to make the file-layering decision explicit. The goal is not to capture more notes; the goal is to decide what belongs in shared CLI instructions, what belongs in the strategy agent, and what belongs in the CSA agent.

Use this prompt if you want GitHub Copilot CLI to review the layering before you fill the table:

```text
Use `.\agent-profile-baseline.md`, `$HOME\.copilot\copilot-instructions.md`, `$HOME\.copilot\agents\strategy.agent.md`, and `$HOME\.copilot\agents\cloud-solution-architect.agent.md` to review the file layering.
For each guidance candidate below, recommend whether it belongs in shared CLI instructions, the Strategy agent, the CSA agent, or outside the harness. Flag duplication or unclear ownership.
Return the result as a Markdown table.
```

| Guidance candidate | Keep in `copilot-instructions.md`? | Move to `strategy.agent.md`? | Move to `cloud-solution-architect.agent.md`? | Why? |
|---|---|---|---|---|
| Durable context | | | | |
| General operating rules | | | | |
| Strategy-specific reasoning style | | | | |
| Microsoft portfolio technical depth | | | | |
| Microsoft Learn MCP Server access | | | | |
| Escalation rules | | | | |
| Communication fingerprint | | | | |
| Evaluation expectations | | | | |

### Step E: Prepare for Spec -> Plan -> Build and harness comparison

Before moving to the scenario transfer and final harness comparison, carry forward the GitHub Copilot CLI observations that matter most: where configuration lives, what role-specific behavior moved into `strategy.agent.md`, what Microsoft architecture review behavior moved into `cloud-solution-architect.agent.md`, how the Learn MCP Server was attached, what remains configurable, and what review or evaluation expectations are visible enough to inspect.

| GitHub Copilot CLI observation | Notes |
|---|---|
| Execution: Model choice | |
| Context: Instructions (behavior) | |
| Knowledge: Enterprise data | |
| Knowledge: External websites | |
| Knowledge: GitHub repository, local files | |
| Memory: What gets remembered? | |
| Tools: MCP Server, external, shell, python | |
| Permission: User identity, policy guardrails | |
| Can we use Work IQ? | |

### Step F: Restart and confirm agent context

After:

- Updating `$HOME\.copilot\copilot-instructions.md` (Global instructions)
- Creating `$HOME\.copilot\agents\strategy.agent.md` (Strategy agent)
- And creating `$HOME\.copilot\agents\cloud-solution-architect.agent.md` (CSA agent)

Restart the Copilot environment with `/restart` and then use `/env` to confirm the custom agents appear in context.

> **Confirm:** Does GitHub Copilot CLI now show the Strategy and Cloud Solution Architect agents?

### Output

Complete this sentence:

> GitHub Copilot CLI helps make the Agent OS inspectable by separating __________ into `$HOME\.copilot\copilot-instructions.md`, __________ into `$HOME\.copilot\agents\strategy.agent.md`, __________ into `$HOME\.copilot\agents\cloud-solution-architect.agent.md`, and __________ into explicit files, MCP configuration, or task flow.

## 6. Spec -> Plan -> Build transfer

### Purpose

Now use the agents you just built against the scenario. The goal is not to produce the final answer; the goal is to separate specification intent, planning decisions, and reviewable build slices.

### Input

Use your scenario watch items, `agent-profile-baseline.md`, M365 Copilot observations, GitHub Copilot CLI build-out notes, and the Strategy and CSA agents.

### Spec Kit reference

Use AI to draft each layer, then review and correct the output. Your job is not to manually write a perfect spec, plan, or task list. Your job is to notice what belongs in each layer and make the agent-system work more explicit before asking for a final deliverable.

> **Insight:** [GitHub Spec Kit](https://github.com/github/spec-kit) provides a more advanced and formalized capability for this same pattern: it turns the Spec -> Plan -> Tasks pattern into a governed workflow with structured artifacts, task generation, and review discipline. In this lab, the workbook keeps the pattern lightweight so you understand the control move before relying on formal tooling.

### Instructions

This section is usually facilitator-led. Draft a small spec, plan, and build/task set if you are following along, but do not design the final customer solution.

### Good enough means

You have a narrow objective, explicit constraints, an approach, a validation method, and 3-5 reviewable build slices.

### Avoid

Do not make the MVP "automate the whole process." Do not jump directly to a polished recommendation.

### Step A: Name why a final answer is premature

| Question | Response |
|---|---|
| What would a single-prompt or final-answer approach likely miss? | |
| Which concern is most at risk: context, harness, agent responsibility, orchestration, evaluation, or system boundary? | |
| What visible work product would make the improvement inspectable? | |

### Step B: Specification slice

Use a simplified prompt like:

```text
As the Strategy agent, use the customer scenario, baseline instructions, and lab observations to draft a concise specification slice.
Do not solve the scenario yet.
Separate the specification concerns from the solution.
Use these categories: objective, primary users, user value, constraints, assumptions, success criteria, and out-of-scope boundaries.
Keep the output good enough for lab discussion.
Write the result as Markdown.
```

| Spec concern | Draft |
|---|---|
| Objective | |
| Primary users or stakeholders | |
| User value | |
| Constraints | |
| Assumptions | |
| Success criteria | |
| Out of scope | |

### Step C: Planning decisions

Use a simplified prompt like:

```text
As the Strategy agent, use the specification slice to draft a concise planning slice.
Do not create the final architecture brief.
Name the recommended approach, durable context needed, harness or control-surface assumptions, tradeoffs, validation method, and revisit trigger.
Make clear which decisions must be made before build/task execution.
If any architecture, platform, compliance, or implementation-risk question materially affects the plan, identify the question to route to the CSA agent.
Write the result as Markdown.
```

| Planning decision | Draft |
|---|---|
| Recommended approach | |
| Durable context needed | |
| Harness or control-surface assumptions | |
| Tradeoffs to expose | |
| Validation or review method | |
| Revisit trigger | |

### Step D: Build / task slices

Define build slices that create reviewable Markdown artifacts or decision outputs. Do not jump directly to the final answer.

Use a simplified prompt like:

```text
As the CSA agent, use the specification slice and planning slice to propose 3-5 reviewable build/task slices.
Each slice should produce a reviewable artifact or decision output, name its dependency, and state what review evidence would prove it is useful.
Make clear how each slice surfaces architecture and risk concerns so reviewers can inspect context, tools, permissions, memory, evaluation, and human authority before any final solution is implemented.
Do not include app code, setup work, CI, or a final polished recommendation.
Keep the slices architecture- and risk-reviewable.
Write the result as Markdown.
```

| Build / task slice | Artifact or decision output | Depends on | Review evidence |
|---|---|---|---|
| | | | |
| | | | |
| | | | |

### Step E: Architecture tradeoffs

| Tradeoff | Prompt-centric approach | Harness/control-pattern approach |
|---|---|---|
| Context durability | | |
| Repeatability | | |
| Human decision boundary | | |
| Evaluation | | |

### Output

Complete this sentence:

> This work should not start with a final answer because the most important design decisions are __________, __________, and __________.

### Cut line if time is short

If the live session is running short, do not complete the full worksheet. Capture the pattern in one sentence:

> Spec -> Plan -> Build is a way to break agent-system work into intent, approach, and reviewable slices: Strategy frames intent and tradeoffs, CSA verifies architecture risk and build slices, and humans retain accountable decisions.

## 7. Harness comparison and Foundry projection

### Purpose

Compare **M365 Copilot Studio** and **GitHub Copilot CLI** as different harness/control surfaces, then project the same harness layers to Microsoft Foundry.

Section 4 uses **M365 Copilot Agent Builder** as the hands-on maker surface because it is fast, approachable, and complete enough for this lab's baseline exercise. Section 7 intentionally uplifts the M365 side to **M365 Copilot Studio**: an enterprise/pro-user surface in the same Copilot universe with stronger connector, governance, orchestration, and environment controls. The comparison is meant to make harness tradeoffs starker, not to treat Agent Builder feature gaps as the whole M365 story.

### Input

Use your lab observations, build-out notes, and Spec -> Plan -> Build transfer.

### Instructions

Compare what each surface makes explicit or leaves implicit. Spend the most energy on what would carry forward into Microsoft Foundry.

### Good enough means

You can name at least two architecture tradeoffs that are not product preference. At least one should involve tool/MCP access, context durability, role separation, review evidence, human handoff, or how the same harness layer would be implemented in Foundry.

### Avoid

Do not rank products by feature count or interface preference.

### Workspace

| **Layer** | **M365 Copilot Studio** | **GitHub Copilot CLI** |
|---|---|---|
| **1. Model + execution runtime** | Microsoft-managed LLM orchestration: Copilot runtime, generative orchestrator planner, and multi-model abstraction | Explicit model selection via Copilot backend (`/model`), LLM client in CLI runtime, and agent execution loop |
| **2. Tool layer: what the agent can do** | Connectors for M365 and third-party systems, Power Automate flows, MCP servers, and API plugins | `tools:` in `.agent.md`, MCP servers, plugins, shell execution, Python, search, fetch, read, and edit tools |
| **3. Context / knowledge layer: what the agent sees** | Dataverse, SharePoint, Outlook, Teams, Graph grounding, and enterprise knowledge sources | Repo files, `.github/` artifacts such as `copilot-instructions.md` and `agent.md`, `skill.md`, workspace files, and file attachments |
| **4. Permission / governance layer: what it cannot do** | DLP policies, Entra identity, connector classification, and environment governance | Tool restrictions in `.agent.md`, filesystem scope, and approval model such as `--yolo` vs. gated execution |
| **5. Memory layer: what it remembers** | Conversation history, Dataverse state, and thread/session context | Session state, repo state through files and git, and persisted CLI memory such as session files |
| **6. Execution / orchestration layer: how it runs** | Topic routing, agent flows, connected agents, and generative orchestration planner | Subagents in `.agent.md`, parallel dispatch patterns, hooks, plan mode, and orchestration logic |

### Synthesis

Given the scenario, your baseline instructions, and the Spec -> Plan -> Build transfer, what is the most important harness tradeoff?

- What does M365 Copilot Studio make easier?
- What does GitHub Copilot CLI make easier?
- Project to Microsoft Foundry:
  - Which harness layers still apply?
  - How are some of those layers implemented?
- Which limitation would matter most for the first responsible slice of work?

> **Key takeaway:** Does low-code vs. pro-code actually matter here, or is the real distinction control over context, tools, memory, permissions, and reviewability?

## Closing reflection

If we succeed, what does this system make easier for humans, and what must it never decide on their behalf?
