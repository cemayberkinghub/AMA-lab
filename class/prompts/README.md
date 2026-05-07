# Prompt Index

Use this index with `../worksheets.md`. Open a prompt only when the workbook tells you to use it, copy the prompt into the named product surface, and save the generated output for the next workbook step.

| Workbook moment | Prompt file | Paste into | Produces | Use the output for |
|---|---|---|---|---|
| Section 2: Agent OS Personalization | `m365-personalization-interview-prompt.md` | M365 Copilot | Local `agent-profile-baseline.md` | Section 3 baseline instructions and Section 5 file generation |
| Section 5, Step A: Shared CLI instructions | `create-copilot-instructions.md` | GitHub Copilot CLI | Draft `$HOME\.copilot\copilot-instructions.md` | Shared operating rules |
| Section 5, Step B: Strategy agent | `create-strategy-agent.md` | GitHub Copilot CLI | Draft `$HOME\.copilot\agents\strategy.agent.md` | Strategy-specific behavior |
| Section 5, Step C: Cloud Solution Architect agent | `create-cloud-solution-architect-agent.md` | GitHub Copilot CLI | Draft `$HOME\.copilot\agents\cloud-solution-architect.agent.md` | CSA-specific architecture review with Learn MCP |

## If you are unsure which prompt to use

Return to the workbook step you are on. The workbook names the prompt file, the product surface, and the expected output. Do not skip ahead through the prompt folder; the sequence matters because each output becomes context for the Spec -> Plan -> Build transfer and final harness comparison.
