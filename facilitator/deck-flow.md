# Facilitator Deck Flow

This is visible-safe Markdown source for the *Engineer Your Harness* facilitation
deck flow. It is not a rendered deck, and it does not require PowerPoint,
screenshots, images, PDFs, or binary assets in this repository.

Use this file when preparing slides or presenter notes. Use
[`run-of-show.md`](run-of-show.md) as the operational timing guide during live
delivery.

**Lab framing:** *Engineer Your Harness - Build an AI Strategist Reasoning
Partner.* Three-hour hands-on architecture lab.

## Story spine

The deck carries one arc: frame the control problem (`prompt -> context ->
harness -> agent -> system boundary` and `agent = model + harness`), anchor it in
the regulated AI-assisted estimation scenario, turn personal judgment into
reusable baseline instructions via the M365 personalization interview, observe
the baseline in a lower-control M365 Agent Builder harness, rebuild it in GitHub
Copilot CLI as explicit files and agents, use those agents on the scenario via
Spec -> Plan -> Build, and close by comparing harness layers across Copilot CLI,
Copilot Studio, and Foundry Agent Service.

| Section | Timing | Mode | Intent | Key message | Participant action | Transition | Cut/compression rule |
|---|---|---|---|---|---|---|---|
| 1. Why this lab + core model | 0-20 | Facilitator frame + quick response | Establish architecture-control purpose and shared vocabulary | We are learning to control agent-system work; the harness is the control surface | Name one AI opportunity where control matters | Use the scenario to pressure-test the lens | Skip introductions; keep objective, formula, and layers |
| 2. Scenario setup: customer theme | 20-30 | Hands-on reading | Anchor regulated design tension without solutioning | The scenario is the pressure test, not the design task yet | Read the scenario and mark tensions, risks, evidence needs, and authority questions | Move from customer pressure to durable agent behavior | Use facilitator summary if needed; do not decompose the solution |
| 3. Agent OS Personalization | 30-50 | Hands-on M365 | Make operating judgment explicit before product setup | Durable judgment should shape the agent before any harness-specific configuration | Run the M365 personalization interview and save `agent-profile-baseline.md` | Turn the profile into portable baseline instructions | Reduce to top three interview rounds if behind |
| 4. Baseline instruction structure | 50-60 | Hands-on refinement | Lightly refine the generated profile into reusable operating rules | The baseline must travel without becoming generic persona text or scenario-specific solutioning | Edit `agent-profile-baseline.md` and separate reusable from platform-specific guidance | Test the baseline in the lower-control M365 surface | Pair instead of extending solo editing time |
| 5. M365 Agent Builder + grounding | 60-75 | Hands-on Builder | Observe how a lower-control harness expresses the baseline | Agent Builder is useful and approachable while some controls remain bounded or implicit | Apply the baseline and capture what transferred, compressed, or could not be said | A missing or blocked Learn MCP path becomes architecture evidence | Use prepared observation or facilitator demo if access fails |
| 6. Learn MCP wall | 75-80 | Facilitator-led observation | Make missing capability visible | A blocked endpoint or unavailable tool is a design signal, not a delivery failure | Record what the agent cannot see, call, or prove from this surface | Reset into a higher-control CLI surface | Narrate the prepared boundary example if needed |
| 7. Break / reset | 80-90 | Reset | Preserve energy before the CLI build-out | The wall gives enough evidence to move from product convenience to inspectable harness control | Capture one insight from the M365 surface | Move to GitHub Copilot CLI | Reduce to five minutes if behind; keep the reset message |
| 8. CLI shared instructions | 90-100 | Hands-on CLI; demo fallback | Move the baseline into durable shared CLI instructions | Higher-control surfaces make durable context visible in files | Draft `$HOME\.copilot\copilot-instructions.md` from `agent-profile-baseline.md` | Split specialist behavior out of shared rules | If setup gets messy, stop troubleshooting and switch to demo |
| 9. Strategy agent | 100-108 | Hands-on; demo fallback | Create the first role-specific accountability domain | Strategy behavior should live in `strategy.agent.md`, not be hidden in global instructions | Draft or inspect `$HOME\.copilot\agents\strategy.agent.md` and identify what moved | Add a CSA agent to show role plus tool access | Combine with CSA comparison if behind |
| 10. CSA agent + Learn MCP | 108-116 | Facilitator demo; optional follow-along | Show model + harness becoming a specialist agent with curated tool access | Role instructions, tool access, and context change what the same model can safely do | Observe `cloud-solution-architect.agent.md`, Learn MCP configuration, and capability boundaries | Confirm state before using the agents | Use prepared output if the live environment is blocked |
| 11. Restart and environment confirmation | 116-120 | Facilitator demo; optional follow-along | Prevent assumptions about active harness state | `/restart` and `/env` make custom-agent context visible before use | Verify or inspect that Strategy and CSA agents appear in context | Use the confirmed agents on the original scenario | Use prepared confirmation if command output is unavailable |
| 12. Spec -> Plan -> Build transfer | 120-150 | Follow-me demo; optional follow-along | Make the CLI build-out pay off against the scenario | Strategy and CSA agents split types of thinking, not tasks | Watch or draft a spec slice, plan slice, and 3-5 build/task slices | Convert applied agent use into comparison evidence | If short, state the pattern and move on |
| 13. Harness comparison + Foundry projection | 150-175 | Conversation-driven | Synthesize product observations into architecture judgment | Compare control layers, not product preference | Discuss key tradeoffs across tools, context, execution, permissions, memory, and orchestration | Close with human authority and system boundary | Focus on Foundry projection and 2-3 decisive controls |
| 14. Closing reflection | 175-180 | Conversation-driven | Reassert human authority and the system boundary | The model generates answers; the harness defines accountability | Answer the closing reflection | End on responsibility, not product preference | Ask only the closing prompt if behind |

The table above is the master deck flow. The section blocks below are Markdown
source for facilitator slides or presenter notes. If a section block and the
table disagree, update the section block to match the table, workbook,
run-of-show, and required sequence.

## Section 1 - Why this lab + core model

- **Purpose:** Establish the lab as architecture-control practice, not a product
  tour, and install the shared mental model.
- **Key message:** A prompt alone is too small for regulated work; use
  `prompt -> context -> harness -> agent -> system boundary` to reason about
  control. Prompt lives inside context; context lives inside harness.
- **Show:**
  - Title: "Engineer Your Harness - Build an AI Strategist Reasoning Partner."
  - Today is: practice controlling agent-system work, portable judgment,
    vocabulary for customer conversations, and a reusable artifact.
  - Today is not: a tool bake-off, a final regulated AI design, a UI walkthrough,
    or a certificate exercise.
  - Core formula: `agent = model + harness`.
  - Harness layers: tools, context, knowledge, memory, execution, permissions,
    and orchestration.
- **Say:** "Today we are not proving one tool is best or designing the final
  regulated AI system. We are learning how to move from broad AI ambition to
  controlled, reviewable agent-system work."
- **Ask:** "Name one AI opportunity where control matters more than speed."
- **Do:** Capture 2-3 participant examples and connect them to context, harness,
  or system boundary.
- **Participant/workbook alignment:** Participant guide learning objective;
  workbook live delivery mode; run-of-show 0-20.
- **Transition:** "We need pressure for the model, so we will anchor the lens in
  a customer scenario before touching tools."
- **Cut/compression rule:** Skip introductions and product context; keep the
  objective, formula, and harness layers.

## Section 2 - Scenario setup: customer theme

- **Purpose:** Anchor the lab in regulated design pressure without inviting full
  solution design.
- **Key message:** The scenario is the pressure test for harness choices, not the
  design task yet. A single naive prompt hides different kinds of work with
  different accountability.
- **Show:**
  - Scenario: AI-assisted estimation and compliance in regulated design work.
  - Customer pains: slow turnaround, missed scope and rework, inconsistent
    compliance interpretation, and senior-expert bottlenecks.
  - Naive prompt: "Use AI to read the plans, apply the rules, and generate the
    estimate."
  - Watch list: tensions, risks, evidence needs, and human authority.
- **Say:** "Read for tensions: speed versus accuracy, compliance versus
  usefulness, automation versus accountable human authority. Final approval must
  remain human-owned."
- **Ask:** "Which tension should we keep watching as we move across harnesses?"
- **Do:** Give participants time to mark tensions, risks, evidence needs, and
  human-authority questions.
- **Participant/workbook alignment:** Workbook section 1; required sequence
  moment 1; run-of-show 20-30.
- **Transition:** "Now we need the agent's operating behavior to be explicit
  before we configure any product surface."
- **Cut/compression rule:** Use a facilitator summary if needed; do not decompose
  the target solution.

## Section 3 - Agent OS Personalization

- **Purpose:** Turn personal judgment and operating style into portable agent
  context through a structured interview.
- **Key message:** Durable judgment should shape the agent before platform-
  specific setup begins. Participants are encoding professional judgment, not
  writing persona flavor.
- **Show:**
  - Step One: interview your judgment.
  - Six rounds: domain and expertise, strategic thinking style, communication
    fingerprint, strong opinions, anti-patterns and red lines, and decision
    framework.
  - Output: `agent-profile-baseline.md`.
- **Say:** "The output is source material for how the agent should reason,
  challenge, escalate, communicate, and handle ambiguity."
- **Ask:** "What judgment do you want an agent to preserve when you are not
  handholding the prompt?"
- **Do:** Have participants run the interview in M365 Copilot and save the
  generated Markdown locally as `agent-profile-baseline.md`.
- **Participant/workbook alignment:** Workbook section 2; participant guide flow
  step 2; run-of-show 30-50.
- **Transition:** "The generated profile now needs to become reusable
  instructions, not a one-off interview transcript."
- **Cut/compression rule:** Reduce to the top three interview rounds if behind,
  but still save a baseline file.

## Section 4 - Baseline instruction structure

- **Purpose:** Convert the generated profile into reusable baseline instructions.
- **Key message:** The baseline must travel across platforms without becoming
  generic persona text or scenario-specific solutioning.
- **Show:** Baseline instruction components: role and scope, operating
  principles, communication rules, challenge and escalation, evidence and
  ambiguity, and reuse guidance.
- **Say:** "Separate what belongs everywhere from what belongs only in a
  scenario, a tool, or a specialist agent."
- **Ask:** "Which part of your profile is reusable control, and which part would
  be dangerous to hard-code everywhere?"
- **Do:** Have participants refine `agent-profile-baseline.md` and mark reusable
  versus platform-specific guidance.
- **Participant/workbook alignment:** Workbook section 3; required sequence
  moment 3; run-of-show 50-60.
- **Transition:** "We will now test how much of this baseline a lower-control
  M365 harness can express."
- **Cut/compression rule:** Pair participants instead of extending solo editing
  time.

## Section 5 - M365 Agent Builder + grounding

- **Purpose:** Observe how a lower-control maker surface expresses baseline
  instructions and enterprise grounding.
- **Key message:** Agent Builder is useful and approachable, while some harness
  controls remain product-bounded or implicit.
- **Show:**
  - Agent Builder instructions area and corporate grounding prompts.
  - Three observation questions: what transferred, what compressed, and what
    could not be said.
- **Say:** "We are looking at the harness: what it can see, trust, cite,
  remember, call, and hand off."
- **Ask:** "What transferred cleanly from the baseline, and what had to be
  compressed or left implicit?"
- **Do:** Have participants paste `agent-profile-baseline.md` into Agent Builder
  instructions and capture quick observations.
- **Participant/workbook alignment:** Workbook section 4; required sequence
  moments 4-5; run-of-show 60-75.
- **Transition:** "The most useful observation may be what the surface cannot
  reach or prove."
- **Cut/compression rule:** Use a prepared observation or facilitator demo if
  access fails; do not turn this into UI training.

## Section 6 - Learn MCP wall

- **Purpose:** Make a missing or blocked capability visible as architecture
  evidence.
- **Key message:** Learn MCP is unreachable from the M365 Agent Builder surface.
  A blocked endpoint or unavailable tool is a design signal, not a delivery
  failure.
- **Show:** The attempted Learn MCP path, the blocked or missing capability, and
  a boundary note template.
- **Say:** "When the agent cannot reach needed expertise, the answer is not to
  pretend. We record the boundary and decide where that capability belongs."
- **Ask:** "What can this harness not see, call, or prove from here?"
- **Do:** Record the tool/context boundary that will matter during final
  comparison.
- **Participant/workbook alignment:** Workbook section 4 observations; required
  sequence moment 6; run-of-show 75-80.
- **Transition:** "This gives us enough evidence to reset into a surface where
  more of the harness is inspectable."
- **Cut/compression rule:** Narrate the prepared boundary example if live access
  is blocked.

## Section 7 - Break / reset

- **Purpose:** Preserve energy and mark the pivot from product convenience to
  inspectable harness control.
- **Key message:** The M365 surface gave evidence; the CLI surface will make more
  control decisions visible as files, agents, tools, and state.
- **Show:** Reset prompts: baseline file, M365 observations, Learn MCP wall, and
  scenario tensions.
- **Say:** "Do not discard the M365 evidence. We will use it after the CLI
  build-out and scenario transfer."
- **Ask:** "What one observation should survive into the comparison?"
- **Do:** Invite one quick note, then prepare the CLI surface.
- **Participant/workbook alignment:** Workbook transition from section 4 to
  section 5; run-of-show 80-90.
- **Transition:** "Now we move the same operating model into GitHub Copilot CLI."
- **Cut/compression rule:** Reduce break to five minutes if behind; do not cut
  the reset message.

## Section 8 - CLI shared instructions

- **Purpose:** Move portable baseline behavior into durable shared CLI
  instructions.
- **Key message:** Higher-control surfaces make durable context visible in files
  instead of hiding it in a chat.
- **Show:**
  - `$HOME\.copilot\copilot-instructions.md` as shared rules.
  - `$HOME\.copilot\agents\` as role-specific behavior.
  - Workbook Step A prompt and what belongs in shared instructions.
- **Say:** "Shared instructions should hold reusable operating rules, not every
  role-specific behavior or every scenario detail."
- **Ask:** "What should every Copilot CLI agent inherit before any specialist
  role is added?"
- **Do:** Have participants draft or inspect
  `$HOME\.copilot\copilot-instructions.md` from `agent-profile-baseline.md`.
- **Participant/workbook alignment:** Workbook section 5 Step A; required
  sequence moment 7; run-of-show 90-100.
- **Transition:** "Once shared behavior is visible, we can move
  strategy-specific judgment into its own agent file."
- **Cut/compression rule:** If setup gets messy, stop troubleshooting and switch
  to facilitator demo.

## Section 9 - Strategy agent

- **Purpose:** Create the first role-specific accountability domain in the CLI
  harness.
- **Key message:** Strategy behavior belongs in `strategy.agent.md`, not hidden
  in global instructions. Each agent is a different accountability domain.
- **Show:** `$HOME\.copilot\agents\strategy.agent.md`, the workbook Step B
  prompt, and examples of strategy-specific decision support.
- **Say:** "We are not splitting tasks. We are decomposing types of judgment so
  each can be inspected, governed, and trusted."
- **Ask:** "What moved out of the shared baseline because it is
  strategy-specific?"
- **Do:** Have participants draft or inspect the Strategy agent and identify what
  changed from global instructions.
- **Participant/workbook alignment:** Workbook section 5 Step B; required
  sequence moment 8; run-of-show 100-108.
- **Transition:** "Now add a second specialist to show role plus curated tool
  access."
- **Cut/compression rule:** Combine with the CSA agent comparison if behind.

## Section 10 - CSA agent + Learn MCP

- **Purpose:** Show model + harness becoming a specialist architecture agent with
  curated tool access.
- **Key message:** Role instructions, tool access, and context change what the
  same model can safely do.
- **Show:**
  - `$HOME\.copilot\agents\cloud-solution-architect.agent.md`.
  - Learn MCP Server configuration and the role/tool boundary.
  - Demo-only third agent: `identity-interviewer.agent.md`.
- **Say:** "This is the payoff from separating shared rules from specialist
  behavior. Learn MCP, which was blocked in M365 Agent Builder, is reachable
  here."
- **Ask:** "What capability is added here that was not available in the
  lower-control surface?"
- **Do:** Facilitator demo of the CSA agent and Learn MCP setup; optional
  participant follow-along if ready.
- **Participant/workbook alignment:** Workbook section 5 Step C; required
  sequence moment 9; run-of-show 108-116.
- **Transition:** "Before using these agents, we need to prove what harness state
  is actually active."
- **Cut/compression rule:** Use prepared output if the live environment is
  blocked.

## Section 11 - Restart and environment confirmation

- **Purpose:** Make file layering and active custom-agent state visible before
  applied agent use.
- **Key message:** The layering check shows what belongs in each file;
  `/restart` and `/env` prove which harness state is active.
- **Show:** File-layering table, CLI observations to carry forward, `/restart`,
  `/env`, and expected Strategy and CSA agent context.
- **Say:** "If we cannot point to the file layer or verify the environment
  state, we cannot claim the agent behavior changed."
- **Ask:** "What belongs in shared instructions, Strategy, CSA, or outside the
  harness, and what changed in the environment that we can prove?"
- **Do:** Review the layering decision, then inspect environment output or
  prepared confirmation.
- **Participant/workbook alignment:** Workbook section 5 Steps D-F; required
  sequence moment 10; run-of-show 116-120.
- **Transition:** "Now we return to the original scenario and use the agents we
  just built."
- **Cut/compression rule:** Use prepared confirmation if command output is
  unavailable; keep the state-confirmation lesson.

## Section 12 - Spec -> Plan -> Build transfer

- **Purpose:** Make the GitHub Copilot CLI build-out pay off against the scenario
  by splitting types of thinking, not tasks.
- **Key message:** Strategy and CSA agents now turn customer pressure into intent
  (Spec), planning decisions (Plan), and reviewable build slices (Build) without
  pretending to solve the whole system.
- **Show:**
  - SPEC with Strategy agent: intent, tensions, explicit out-of-scope boundaries.
  - PLAN with Strategy agent: decisions, risks, validation, reversible versus
    irreversible choices.
  - BUILD with CSA agent: 3-5 reviewable slices and the smallest meaningful MVP
    slice.
- **Say:** "This is where the scenario comes back. The agents do not produce the
  final answer; they help separate what must be specified, planned, and
  reviewed."
- **Ask:** "What would a final-answer prompt miss, and what first slice would
  make the work inspectable?"
- **Do:** Facilitator demo or optional follow-along: draft a spec slice, plan
  slice, 3-5 build/task slices, and one architecture tradeoff.
- **Participant/workbook alignment:** Workbook section 6; required sequence
  moments 11-13; participant guide flow step 5; run-of-show 120-150.
- **Transition:** "Now that both surfaces have been used on the same scenario,
  the comparison has evidence."
- **Cut/compression rule:** If short, state the one-line Spec -> Plan -> Build
  pattern and move on.

## Section 13 - Harness comparison + Foundry projection

- **Purpose:** Convert product observations and applied agent use into
  architecture judgment using the harness-layer mapping and Microsoft stack.
- **Key message:** The closing comparison is about control layers, not product
  preference. Reframe low-code versus pro-code into who operates the system, what
  problem it governs, and where boundaries apply.
- **Show:**
  - Layer mapping across Copilot CLI, Copilot Studio, and Foundry Agent Service.
  - Control dimensions: tools, context, execution, permissions, memory, and
    orchestration.
  - Microsoft stack projection: maker UX, developer UX, runtime/orchestration,
    control plane, and hosted execution.
- **Say:** "Same layers, different defaults. The control you trade in one column
  shows up as friction in another. Customers buy products; architects sell
  control across layers."
- **Ask:** "Which tradeoff matters most after applying the agents to the
  scenario?"
- **Do:** Facilitate discussion across context, tools, memory, permissions,
  outputs, handoffs, and first-slice limitations.
- **Participant/workbook alignment:** Workbook section 7; required sequence
  moment 14; run-of-show 150-175.
- **Transition:** "The final question is not what the agent can do. It is what
  humans remain accountable for."
- **Cut/compression rule:** Focus on Foundry projection and 2-3 decisive controls.

## Section 14 - Closing reflection

- **Purpose:** Reassert human authority and the system boundary.
- **Key message:** The model generates answers, but the harness defines
  accountability. Success means making human work easier without surrendering
  accountable decisions.
- **Show:** Closing reflection: "If we succeed, what does this system make easier
  for humans, and what must it never decide on their behalf?"
- **Say:** "Carry the model forward: prompt, context, harness, agent, system
  boundary. The strongest design move may be naming where the agent stops."
- **Ask:** "What must this system never decide on behalf of humans?"
- **Do:** Take one or two responses and close on responsibility rather than
  product preference.
- **Participant/workbook alignment:** Workbook closing reflection; participant
  guide behavior expectations; run-of-show 175-180.
- **Transition:** End.
- **Cut/compression rule:** Ask only the closing prompt if behind.

## Global presenter notes

- Use the deck flow to carry the live story, not to over-script every sentence.
- If behind, cut explanation before cutting participant production.
- Keep workbook sections 1-4 and workbook section 5 steps A-B hands-on when
  possible; later CLI, Spec -> Plan -> Build, and comparison moments may be
  facilitator-led or conversation-driven.
- Do not place final harness comparison before Spec -> Plan -> Build; the applied
  multi-agent transfer is the payoff from the CLI build-out.
- The `identity-interviewer.agent.md` is demo-only - shown to illustrate the org
  chart pattern, not built by participants.
- Do not add screenshots, rendered decks, native presentation files, PDFs,
  images, or binary assets to this repository.
