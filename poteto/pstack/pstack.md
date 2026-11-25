# pstack (public plugin)

Sources (fetched 2026-10-06 Asia/Taipei):
- Repo tree: https://github.com/cursor/plugins/tree/main/pstack
- README: https://github.com/cursor/plugins/blob/main/pstack/README.md (copy: `pstack-README.md`)
- Marketplace: https://cursor.com/marketplace/cursor/pstack
- Skill frontmatter scan: `skills-frontmatter.json`

Author: Lauren Tan (@poteto). MIT license. Official home is Cursor's plugins monorepo (`cursor/plugins`), not a standalone user repo. Unofficial Claude port exists (`michael-denyer/pstack-claude`) — not used as primary source here.

## Install / update

```text
/add-plugin pstack
```

Then:

1. `/setup-pstack` — pick reasoning budget + model per role; writes `~/.cursor/rules/pstack-models.mdc` (`alwaysApply: true`).
2. Use `/poteto-mode` for any non-trivial work.

Optional companion plugin: `cursor-team-kit` (ships `/deslop`, `control-cli`, `control-ui`). Cursor built-ins `/create-skill` and `/babysit` are referenced; inside poteto-mode, the babysit **playbook** supersedes the built-in for PR-status asks.

To keep poteto-mode on across turns: pick it from `/` menu and Option/Alt+Enter (Custom Mode). Works well with Cursor `/loop`.

## Invocation note (`disable-model-invocation`)

Nearly every slash skill sets `disable-model-invocation: true` in SKILL.md frontmatter. That means the model must **not** auto-trigger them from description matching; the operator (or an explicit parent skill step) must invoke them. Exception among scanned skills: **`/setup-pstack`** does **not** set that flag.

`/poteto-mode` additionally has `mode: true` (Custom Mode eligible) and is the router that loads playbooks and calls other skills as steps need them.

**Important for bot authors:** writing the words "poteto-mode" as a style hint is not enough to run the skill; the literal `/poteto-mode` command (or spawning `subagent_type: "poteto-agent"`, which reads poteto-mode's SKILL.md in full) is required.

## Subagents

| type | purpose |
|---|---|
| `poteto-agent` | End-to-end poteto style; reads poteto-mode SKILL.md (incl. principles index) before work. Do not substitute `generalPurpose`. |
| `Comment Sicko` | Read-only comment reviewer; usually via `/no-comments`. |

## Skills (slash commands)

One-line purposes from README + frontmatter:

| Command | Purpose |
|---|---|
| `/poteto-mode` | Default entry: match a playbook, run rigorous engineering workflow. |
| `/poteto-help` | New-user / which-skill help; answers then hands a prompt to type (does not start the work). |
| `/setup-pstack` | Configure models + reasoning budget per role. |
| `/how` | Walkthrough of how a subsystem works. |
| `/why` | Why it was built this way; parallel MCP evidence categories. |
| `/recall` | Rebuild recent context on a topic from chat history + shared record. |
| `/blast-radius` | What else a small change could break; prove safety by running code. |
| `/architect` | Settle types/signatures/module shape before code crosses a boundary. |
| `/arena` | N parallel attempts; graft the best parts. |
| `/swarm` | N parallel workers across slices/races; one aggregated report. |
| `/interrogate` | Multi-model adversarial review of a diff. |
| `/automate-me` | Draft a personal `*-mode` skill from how the user actually works. |
| `/make-bot-ui` | Page/dashboard whose buttons wake a Grok Bot over webhook. |
| `/reflect` | After a long task, capture the recipe as a skill edit. |
| `/correct` | Repeated agent mistakes → fix at highest level (architecture → types/lint/CI → tests → docs last); keep enforcement table. |
| `/teach` | how + why woven into one plain explanation. |
| `/tdd` | Failing test first, then fix. |
| `/benchmark-checklist` | Vet a measured number before reporting/acting (Brendan Gregg-inspired). |
| `/no-comments` | Strip comments before review; Comment Sicko findings. |
| `/typescript-best-practices` | Type-system discipline in TS syntax. |
| `/figure-it-out` | No playbook fits → design an auditable playbook. |
| `/show-me-your-work` | Decision trail TSV you can commit. |
| `/create-verification-skill` | Generate project-local verify skill + feature map + CLI. |
| `/maintain-verification-skill` | Refresh drifted feature map (source wave + one live pass). |
| `/create-formal-verification-skill` | (v0.15.27, beta) Generate a project-local skill + formal verification suite (e.g. TLA+, kani) for the highest-risk property. https://x.com/poteto/status/2111926622278521253 |
| `/unslop` | Remove AI writing tells. |
| `/bro` | Restate last message in plain language. |
| `/ketchup` | Catch up on everything since the user's last message; executive summary per action item (added 2026-10, from https://x.com/poteto/status/2109041205132816740). |
| `/in-your-own-words` | Agent restates the user's goals and problem in its own words to confirm alignment (pstack 0.15.23, from https://x.com/poteto/status/2110047236369547621). |
| `/technical-writing` | Diátaxis + Google + STE + Global English for docs/RFCs/PRs. |

Also: 24 `principle-*` leaf skills (indexed inline by poteto-mode). Core themes include laziness-protocol, foundational-thinking / data structures first, prove-it-works, encode-lessons-in-structure, never-block-on-the-human, etc. Full table in `pstack-README.md`.

**Usage notes (from @poteto 2026-10-15):** `/poteto-mode` is for hard/rigorous work, not every task; run `/setup-pstack` for budget first. Skills stay `disable-model-invocation: true` unless you invoke them (or set a personal always-on `/poteto-mode` rule). To cut cost inside poteto-mode, tell the agent not to spawn large swarms. Bots can default cloud-agent `mode` to poteto-mode via the spawn-agent tool param. Continuously tune skills and ablate stale sections. See https://x.com/poteto/status/2110496830429839869 https://x.com/poteto/status/2110498629307990461 https://x.com/poteto/status/2110498826813649079 https://x.com/poteto/status/2110535901600481520

**Usage notes (from @poteto 2026-10-16):** Installing pstack is cheap because skills stay `disable-model-invocation: true` (mix and match; use `/poteto-help`). Prompt to author a skill: `/poteto-mode create a skill that does <xyz> and eval it`. `/poteto-mode` can cover non-coding goals when code is still required. Prefer lint/delete APIs over “don’t use this” comments. See https://x.com/poteto/status/2110760668987322408 https://x.com/poteto/status/2110759504778592664 https://x.com/poteto/status/2110777496119709745 https://x.com/poteto/status/2110635971884802049

## Playbooks (under `/poteto-mode`)

23 playbooks (README count as of fetch):

| Playbook | For |
|---|---|
| investigation | Read-only how/why questions |
| bug-fix | Repro → root cause → fix with runtime evidence |
| perf-issue | Measured slowness vs baseline |
| hillclimb | Sustained metric improvement, one commit per win |
| runtime-forensics | Live symptom (leak, idle CPU, glitch) |
| trace-forensics | Captured profile/trace/heap artifact |
| feature | New/changed behavior from a named data shape |
| refactoring | Behavior-preserving structure change |
| prototype | Cheap throwaway sketch / empirical fork |
| visual-parity | Pixel-exact UI equivalence |
| authoring-a-skill | Writing/editing SKILL.md |
| eval | Blinded skill/prompt behavior tests |
| babysit | Drive PR/stack to merge-ready |
| shipping | Independent verify green stack, then land |
| autonomous-run | Long task without stopping |
| orchestrate | Standing multi-day project, stacked PRs, fleets |
| autopilot-full | Independent PRs to merged with swarm verdicts |
| autopilot-stack | Linear base-branch stack for operator to land |
| session-pickup | Resume prior agent work |
| pause-safely | Suspend cleanly for later resume |
| multi-phase-plan | Phases / stacked PRs |
| worktree-cleanup | Prune merged/abandoned worktrees (safety-gated) |
| opening-a-pr | Conventional commits PR; end of every other playbook |

## Automations

Dormant **benny** pack under `automations/benny/` (Slack triage → repro → fix with UI evidence). Not registered as slash skills; setup via `FOR_AGENTS.md`.

## Correction order (from `/correct` + @poteto posts)

Highest value first:

1. Architecture / data structures (eliminate the class of mistake)
2. Types, lint, CI checks whose errors name the fix
3. Behavior tests
4. Docs / agent rules / skills last (nothing fails when skipped)
5. Human review alone = ngmi as the primary control

Cited in X: https://x.com/poteto/status/2089067865098113024 and `/correct` announcement https://x.com/poteto/status/2106542593656111276
