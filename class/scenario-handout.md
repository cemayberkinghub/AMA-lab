# Scenario: AI-Assisted Estimation and Compliance in Regulated Design Work

You are supporting a services-led customer operating in a highly regulated design and construction environment. Their teams produce technical designs and cost estimates that must satisfy strict safety and compliance standards, local regulator interpretation, and internal quality review by senior experts.

The customer competes on speed, accuracy, and consistency, but the current process is manual, fragmented, and difficult to scale. They are exploring whether AI can meaningfully improve how work gets done without compromising safety, compliance, or accountability.

## Business problem

| Challenge | Why it matters |
|---|---|
| Slow turnaround | Design and estimation cycles take days or weeks |
| Missed scope and rework | Incomplete estimates and overlooked components create overruns and change orders |
| Inconsistent compliance outcomes | Requirements vary by jurisdiction and interpretation |
| Expert bottlenecks | Senior reviewers are overloaded and cannot scale every review |

The customer's starting intuition is:

```text
This feels like a problem AI should be able to help with.
```

## Initial AI vision

The customer imagines an AI-driven system that can read technical plans, apply relevant rules and standards, generate a first-pass design and cost estimate, and learn from expert corrections over time.

## Why the first prompt is not enough

```text
Use AI to read the plans, apply the rules, and generate the estimate.
```

That prompt hides multiple domains and risks:

- Perception, estimation, compliance interpretation, review, approval, and feedback learning are different kinds of work.
- Safety and regulatory interpretation require evidence, confidence boundaries, and accountable judgment.
- Local requirements cannot be treated as uniform.
- Expert corrections cannot become automatic learning without governance and validation.
- Final approval must remain human-owned.

## Return-to-scenario challenge

Do not complete this full challenge during initial scenario setup. Use it as the return point after you have created baseline instructions, observed both harness surfaces, and are ready for the Spec -> Plan -> Build transfer.

Do not design the final system. Decide how to approach the problem responsibly.

Define:

1. Distinct problem domains embedded in the request.
2. Which parts involve perception, judgment, accountability, or regulatory interpretation.
3. What would be risky to automate first.
4. What could create early value without over-promising.
5. Where human authority must remain explicit.
6. What the smallest meaningful MVP slice should prove.
7. What must be explicitly out of scope in the first phase.

## Closing prompt

If we succeed, what does this system make easier for humans, and what must it never decide on their behalf?
