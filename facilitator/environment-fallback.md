# Environment Fallback

Run preflight at least one business day before the lab and again 30 minutes before start. During the session, spend no more than 10 minutes troubleshooting before switching to fallback.

## Readiness checks

| Surface | Ready when | Fallback if unavailable |
|---|---|---|
| M365 Copilot / Agent Builder | Facilitator can create or open an agent and edit instructions | Facilitator demo or prepared observations |
| Corporate grounding | Relevant enterprise content is visible and queryable | Discuss grounding assumptions using sample observations |
| Learn MCP wall | Participants can observe missing or blocked endpoint in the lower-control surface | Narrate the wall and ask what the harness cannot call |
| GitHub Copilot CLI | CLI starts and can inspect expected instruction context | Pair participants or use facilitator demo |
| Custom agents | Strategy and CSA agent files are visible after restart | Use prepared agent behavior examples |
| Learn MCP access in CSA path | CSA agent can reach or be configured for Learn MCP | Use prepared query/result excerpt and record blockage |
| `/restart` and `/env` | State refresh and environment context are visible | Narrate restart purpose and continue with prepared output |

## Participation modes

| Mode | Use when | Facilitation rule |
|---|---|---|
| Individual work | Most participants have required surfaces | Keep outputs comparable through `class\exercises.md` |
| Paired work | Readiness is mixed | Pair by access, not seniority |
| Facilitator demonstration | Access is broadly blocked | Make participants observe controls and fill comparison tables |
| Prepared observation | Tool behavior is slow or unreliable | Use observations to debrief architectural implications |

## Recovery language

Use this when switching paths:

> This tool state gives us enough evidence. We are preserving the architecture lesson by switching to the fallback path instead of spending class time on product support.

## After any fallback

Ask participants to record what the surface could see, call, remember, produce, and prove; then ask what the next harness would need to make durable.
