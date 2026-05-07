# Live Lab Guide

This guide preserves the required lab sequence. Do not reorder the experience to optimize for product-demo convenience; the final comparison depends on evidence from the earlier steps.

## Required sequence

| Order | Moment | What to do | Evidence to preserve |
|---:|---|---|---|
| 1 | Scenario setup | Read the regulated design scenario and mark tensions without solving it | Risks, human-authority questions, evidence needs |
| 2 | Agent OS Personalization | Use M365 Copilot as an interviewer for your operating style | Judgment, tradeoffs, red lines, communication preferences |
| 3 | Baseline instructions | Save and refine `agent-profile-baseline.md` | Portable instructions, not a generic persona prompt |
| 4 | M365 Copilot Agent Builder instructions | Apply the baseline in a lower-control surface | What instructions and grounding express well |
| 5 | Corporate grounding | Observe enterprise context and its limits | What can be seen, trusted, cited, or remembered |
| 6 | Microsoft Learn MCP endpoint wall | Notice missing or blocked capability | Boundary evidence; what the harness cannot call |
| 7 | GitHub Copilot CLI shared instructions | Move baseline behavior into `copilot-instructions.md` | Durable file-backed context |
| 8 | Strategy agent | Separate strategy-specific behavior into `strategy.agent.md` | Role-specific decision support |
| 9 | Cloud Solution Architect agent with Learn MCP | Observe CSA-specific guidance and tool access | Role + tool access as harness design |
| 10 | `/restart` and `/env` confirmation | Verify active custom-agent context | Evidence of environment state |
| 11 | Spec | Draft the objective, users, constraints, assumptions, success criteria, and out-of-scope boundaries | Governable intent |
| 12 | Plan | Name approach, risks, validation, boundaries, and revisit triggers | Reviewable architecture decisions |
| 13 | Build / tasks transfer | Define 3-5 reviewable build slices | Concrete next steps without final-solution overreach |
| 14 | Harness comparison + Foundry projection | Compare surfaces and project the layers to Foundry | Architecture tradeoffs and human authority boundaries |

## Suggested timing for a 180-minute class

| Minutes | Segment | Mode |
|---:|---|---|
| 0-20 | Open, frame the lab, introduce the core model | Facilitator frame + quick response |
| 20-30 | Scenario setup | Hands-on reading and marking |
| 30-50 | Agent OS Personalization | Hands-on interview |
| 50-60 | Baseline instruction structure | Hands-on refinement |
| 60-80 | M365 Agent Builder, grounding, and Learn MCP wall | Hands-on + observation |
| 80-90 | Break/reset | Transition |
| 90-120 | GitHub Copilot CLI shared instructions and agents | Hands-on with demo fallback |
| 120-150 | Spec -> Plan -> Build transfer | Facilitator-led or follow-along |
| 150-175 | Harness comparison and Foundry projection | Discussion |
| 175-180 | Closing reflection | Individual or group answer |

## Compression rule

If the class is behind, compress explanations but preserve the evidence needed for the Spec -> Plan -> Build transfer and final harness comparison. Do not skip the human-authority discussion.

## Closing reflection

If we succeed, what does this system make easier for humans, and what must it never decide on their behalf?
