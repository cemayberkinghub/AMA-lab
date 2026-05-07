# References

## Core model

Use this model throughout the lab:

```text
prompt -> context -> harness -> agent -> system boundary
```

In this lab:

```text
agent = model + harness
```

## What each layer means

| Element | Meaning | Design question |
|---|---|---|
| Prompt | The immediate instruction or request | Is this ask clear enough for the current turn? |
| Context | Durable facts, constraints, preferences, sources, and assumptions | What must be present and trustworthy? |
| Harness | The operating frame around the model: instructions, tools, grounding, memory, output contracts, evaluation, and handoff rules | What controls make behavior repeatable and inspectable? |
| Agent | The model operating through its harness | What responsibility should this agent own? |
| System boundary | Where agent responsibility ends and human, business, compliance, and operational accountability begins | What must remain outside the agent? |

## Agent OS

Agent OS is the portable operating model created by deliberate harness engineering. It is not a literal operating system, product feature, runtime, orchestration system, single file, or a separate layer beside the system boundary.

Agent OS can include:

- durable context and constraints;
- identity, judgment, and communication preferences;
- behavioral principles and red lines;
- role boundaries and human-owned decisions;
- tool assumptions and limitations;
- memory, handoff, and evaluation expectations.

## Harness questions

When comparing surfaces, ask what each surface lets the agent:

- see;
- do;
- remember;
- call;
- produce;
- hand off;
- prove; and
- refuse or escalate.

## Regulated design safety reminders

The agent may help summarize requirements, identify gaps, cite sources, propose reviewer questions, and prepare evidence packets. It must not certify compliance, approve safety-critical designs, commit price, waive exceptions, or silently learn from corrections without governance.

## Spec -> Plan -> Build

Spec -> Plan -> Build is a control pattern:

- **Spec** makes intent, users, value, constraints, assumptions, success criteria, and non-goals explicit.
- **Plan** makes approach, risks, validation, sequence, tradeoffs, and revisit triggers explicit.
- **Build / tasks** turns the plan into reviewable slices with dependencies and evidence.

Use the pattern to prevent a broad AI ambition from becoming an unreviewable final answer.
