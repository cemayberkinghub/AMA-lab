# Prompt: Create GitHub Copilot CLI Instructions

Use this prompt during workbook section 5, step A. Copy it into GitHub Copilot CLI to draft shared operating guidance for `copilot-instructions.md`.

## Copy/paste prompt

```text
# Lab Task: Create GitHub Copilot CLI Instructions
## Goal
Turn your Agent Operating Profile v1, baseline instruction structure, and M365 Copilot observations into shared guidance for:
$HOME\.copilot\copilot-instructions.md

## Output
Write clear global instructions as Markdown ready to copy and paste to:
$HOME\.copilot\copilot-instructions.md

## Include, where applicable
- Durable context
- Behavior rules
- What to preserve or avoid
- When to challenge
- When to escalate
- How to handle ambiguity
- How to evaluate responses

## Exclude
- Strategy-specific behavior, which belongs in `strategy.agent.md`
- CSA-specific architecture review behavior, which belongs in `cloud-solution-architect.agent.md`

## Constraints
- Applies across all agents
- Keep it concise and practical
- No duplication of role-specific logic

## Quick check
- Would multiple agents use this consistently?
- Is anything role-specific? If yes, remove it.
- Is it short and actionable?
```
