---
tags: [arc, bootstrap, agent]
---

# Arc 1 — Baseline Retro

**Owner:** Agent / Installer — [[../../../../belief-systems/agile/agile-processes#1-every-ceremony-has-an-owner]]
**Want:** An honest snapshot of where the user actually is
**Need:** Every existing belief retro'd to its true status before anything new is built on top of it

---

## Beat 1a — Scan Global Config
*Active identity: [[../identities/installer]]*

Scan the user's global environment only:
- `~/.claude/CLAUDE.md` — extract beliefs, rules, working agreements
- `~/.claude/projects/` memory files — extract named beliefs and patterns
- Any existing workspace or belief system files the user points to

Do not scan project-specific CLAUDE.md files yet — those come in Beat 1a2. Keep global and project-level config separate throughout.

If scope is large, decompose: map what exists first, read selectively based on user direction. Use subagents for large configs — compress results before continuing.

Organize global findings as a retro belief list: one belief per item, source noted, all starting as candidate status pending retro.

**Belief transitions:**
- *"I have a candidate belief set from this user's global config"* — introduced as `emerging` (found something) or `strained` (found nothing; starting fresh)

---

## Beat 1a2 — Scan Project Config
*Active identity: [[../identities/installer]]*

Scan project-specific CLAUDE.md files under the user's code directories. Group findings by project — do not flatten into the global list.

For each project: extract beliefs, rules, and working patterns that appear to be in force. Note which beliefs appear across multiple projects.

Present a summary grouped by project:

> "I found project-specific config in {N} projects. Here's what each one appears to believe:
>
> **{project-name}:** {belief summary}
> ..."
>
> "Some beliefs appear across multiple projects: {list}. Do you want to promote any of these to your common workspace? And are there projects different enough from each other that they'd warrant separate workspace contexts?"

User responds — promoted beliefs carry forward into the workspace retro; project-specific beliefs stay scoped to that project and are noted as tasks if they need workspace treatment later.

**Belief transitions:**
- *"I understand which beliefs are common across my work and which are project-specific"* — introduced as `emerging`; `active` once user confirms what promotes

---

## Beat 1b — Present for Retro
*Active identity: [[../identities/installer]]*

Present the candidate belief list to the user as a retro:

> "Here's everything I found that you appear to believe about how you work. For each one, tell me where you actually are with it."

Frame the retro questions clearly:
- Still believe it, acting on it → `active`
- Should do more with it, not there yet → `emerging`
- Starting to trust it less → `strained`
- Don't want to believe it anymore → `former`
- Never really believed it, just wrote it down → `strained`

**Belief transitions:**
- *"The user's existing beliefs are ready for retro"* — introduced as `active`

---

## Beat 1c — Run the Retro
*Active identities: [[../identities/installer]] · [[../../user/identities/yherder]]*

User reviews each belief candidate and assigns honest status. Agent updates in real time.

*Iterative — one belief at a time or in clusters; repeat until the list is exhausted.*

**Belief transitions (user, per belief):**
- Each belief lands at the status the user assigns — `active`, `emerging`, `strained`, or `former`
- The path matters: a belief the user immediately assigns `strained` is different from one that starts `active` then gets revised to `strained` after reflection — note which happened

**Belief transitions (user, arc-level):**
- *"My existing beliefs have been honestly assessed"* — introduced as `emerging` during retro; `active` when the list is exhausted and nothing feels unaddressed

---

## Beat 1d — Serialize Baseline
*Active identity: [[../identities/installer]]*

Store the retro'd belief list as **baseline/** workspace. Group beliefs by theme. Record honest status for each. Note source.

Baseline is now frozen — a reference point, not an active workspace.

**Belief transitions:**
- *"My starting point is captured honestly"* — introduced as `active`

---

## Beat 1e — Confirm Baseline
*Active identity: [[../../user/identities/yherder]]*

> "I've stored your existing beliefs at their honest status in your baseline workspace. Nothing was changed in your config — this is a clean snapshot of where you are. Does this feel like an accurate picture?"

User confirms or flags anything that landed wrong.

*Iterative if needed — agent adjusts baseline until user confirms.*

**Belief transitions:**
- *"My starting point is captured honestly"* — `active` on confirmation; `strained` if user spots misrepresentation (agent corrects; beat repeats)

---

## Beat 1f — Identify What Carries Forward
*Active identities: [[../identities/yherda-consultant]] · [[../../user/identities/yherder]]*

Review the retro'd baseline together. Identify which beliefs carry forward:
- `active` beliefs → carry forward as-is
- `emerging` beliefs → carry forward; will develop through subsequent arcs
- `strained` beliefs → carry forward to initial workspace; held lightly; candidates for resolution
- `former` beliefs → stay in baseline only; inform the ideal workspace by their absence

> "Here's what I'd carry into your new workspace and what I'd leave in baseline. Does that feel right?"

**Belief transitions:**
- *"I know what I'm building on and what I'm leaving behind"* — introduced as `active` on confirmation; `strained` if the user is uncertain about any item (discuss; resolve or note as task)

---

## Beat 1g — Create Workspace Structure
*Active identity: [[../identities/installer]]*

Create both workspaces at:
- `~/.claude/yherda/{name}-initial/` — carries forward `active`, `emerging`, and `strained` beliefs from baseline
- `~/.claude/yherda/{name}-ideal/` — carries forward `active` and `emerging` beliefs only

In each workspace, copy the full belief system packages from the vault:
- `belief-systems/yherda/` — yherda-model, yherda-operational, expression, expression-human, expression-agent, yherda-migration; processes/yherda-update
- `belief-systems/agile/` — agile-manifesto, agile-os, agile-workflow, agile-processes; processes/standup, planning, grooming, review, retro, sos

Also copy templates from `bootstrap-prompts/templates/` into each workspace:
- `retro_log.md`, `retro_activity_log.md`, `tasks.md`

**Belief transitions:**
- *"The workspace file structure exists"* — introduced as `active`

---

## Beat 1h — Adopt Agile Beliefs
*Active identities: [[../identities/agile-consultant]] · [[../../user/identities/yherder]]*

Present the full agile belief systems as a summary — agile-manifesto, agile-os, agile-workflow, agile-processes — covering what each contains and what it means to hold these beliefs.

For the **ideal workspace**: adopt silently. No retro needed — the ideal is the clean version.

For the **initial workspace**: run a mass retro. Present all agile beliefs as a single set:

> "Here are the agile beliefs I'm proposing for your working context. Any you want to push back on, modify, or hold more lightly? We can adjust the whole set at once — you don't need to go belief by belief."

User responds with any exceptions or modifications. Uncontested beliefs arrive as `emerging` (not yet tested in this context). Beliefs the user confirms from experience arrive as `active`.

**Belief transitions:**
- *"The agile belief foundation is established in this workspace"* — introduced as `active` in ideal; `emerging` in initial (earning `active` through use)

---

## Beat 1i — Install Agent Character
*Active identity: [[../identities/installer]]*

Create an agent character in both workspaces using the agile character template. Install two identities:

**Scrum Master** — ceremony orchestrator and belief guardian
- Belief systems: agile-processes, agile-workflow, agile-os
- Owner of: standup arc, retro arc

**Agile Consultant** — planning and delivery advisor
- Belief systems: agile-processes, agile-workflow, agile-os, agile-manifesto
- Owner of: planning arc, grooming arc, review arc

Copy all process arcs from `belief-systems/agile/processes/` into `characters/agent/arcs/` in each workspace.

**Belief transitions:**
- *"The agent has the identities needed to run ceremonies"* — introduced as `active`

---

Arc 1 complete. Arcs 2–5 run in the initial workspace. Wiring, skill generation, and handoff happen at the close of Arc 5 once the user identity map is known.
