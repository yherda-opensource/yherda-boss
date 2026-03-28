# {name} Workspace — {initial|ideal}

This is the working context for {name}'s Yherda Boss workspace. Load this file to orient in this workspace.

---

## Workspace Purpose

**{name}-initial** — reflects how {name} actually works today; carries real adaptations and strained beliefs alongside active ones; the primary working context
**{name}-ideal** — the clean agile belief set without inherited friction; used for comparison and as a migration target over time

---

## Belief Systems

### Yherda Package (`belief-systems/yherda/`)

| File | Summary |
|---|---|
| `yherda/yherda-model.md` | Core schema — characters, identities, arcs, beats, belief systems, belief transitions |
| `yherda/yherda-operational.md` | How the agent reasons and operates within the model |
| `yherda/expression.md` | Universal beliefs about expressing an idea for a specific receiver |
| `yherda/expression-human.md` | Expression beliefs for human-readable outputs |
| `yherda/expression-agent.md` | Expression beliefs for skill generation and agent context loading |
| `yherda/yherda-migration.md` | Beliefs and mapping table for migrating this workspace to Yherda |
| `yherda/processes/yherda-update.md` | Process arc for pulling community belief updates |

### Agile Package (`belief-systems/agile/`)

| File | Summary |
|---|---|
| `agile/agile-manifesto.md` | The four values and twelve principles from agilemanifesto.org |
| `agile/agile-os.md` | Agile as a belief synchronization mechanism |
| `agile/agile-workflow.md` | Opinionated defaults — DoR, DoD, ceremony cadence, sprint structure |
| `agile/agile-processes.md` | Ceremony ownership, retro protocol, process extension model |
| `agile/processes/standup.md` | Standup ceremony arc |
| `agile/processes/planning.md` | Sprint planning ceremony arc |
| `agile/processes/grooming.md` | Backlog grooming ceremony arc |
| `agile/processes/review.md` | Sprint review ceremony arc |
| `agile/processes/retro.md` | Retrospective ceremony arc |
| `agile/processes/sos.md` | Scrum of scrums / community belief update arc |

### Domain Belief Systems (`belief-systems/`)

{Domain belief systems discovered and created during Arc 2–5 are listed here after bootstrap completes.}

---

## Characters

### Agent (`characters/agent/`)

| Identity | Belief systems | Owns |
|---|---|---|
| Scrum Master | agile-processes, agile-workflow, agile-os | standup, retro |
| Agile Consultant | agile-processes, agile-workflow, agile-os, agile-manifesto | planning, grooming, review |

### User (`characters/{name}/`)

{User identities created during Arc 5 are listed here after bootstrap completes.}

---

## Active Arcs (`characters/agent/arcs/`)

| Arc | Owner | Invoked by |
|---|---|---|
| standup.md | Scrum Master | `/scrum-master` |
| planning.md | Agile Consultant | `/agile-consultant` |
| grooming.md | Agile Consultant | `/agile-consultant` |
| review.md | Agile Consultant | `/agile-consultant` |
| retro.md | Scrum Master | `/scrum-master` |

---

## Task Store

`tasks.md` — local task board; workflow states Backlog through Done

---

## Retro

`retro_log.md` — staging area for belief candidates; cleared after retro integration
`retro_activity_log.md` — append-only audit trail of every belief transition

---

## Skills

Skills are in `~/.claude/skills/`. Invoke by name:
- `/scrum-master` — standup, retro, belief guardian
- `/agile-consultant` — planning, grooming, review

{Domain skills generated during Arc 5 are listed here after bootstrap completes.}
