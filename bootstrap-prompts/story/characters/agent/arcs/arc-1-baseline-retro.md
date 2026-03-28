---
tags: [arc, bootstrap, agent]
---

# Arc 1 — Baseline Retro

**Owner:** Agent / Installer — [[../../../../belief-systems/retro#the-arc-owner-leads]]
**Want:** An honest snapshot of where the user actually is
**Need:** Every existing belief retro'd to its true status before anything new is built on top of it

---

## Beat 1a — Scan
*Active identity: [[../identities/installer]]*

Scan the user's environment:
- `~/.claude/CLAUDE.md` — extract beliefs, rules, working agreements
- `~/.claude/projects/` memory files — extract named beliefs and patterns
- Any existing workspace or belief system files the user points to

If scope is large, decompose: map what exists first, read selectively based on user direction. Use subagents for large configs — compress results before continuing.

Organize findings as a retro belief list: one belief per item, source noted, all starting as candidate status pending retro.

**Belief transitions:**
- *"I have a candidate belief set from this user's existing config"* — introduced as `emerging` (found something) or `strained` (found nothing; starting fresh)

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

## Beat 1j — Wire User Identities to Ceremony Beats
*Active identity: [[../identities/installer]]*

Using the identities produced in Arc 5, wire user roles to ceremony beats:

| Ceremony | User identity | Agent identity |
|---|---|---|
| Standup | Yherder | Scrum Master |
| Planning | Coordinator | Agile Consultant |
| Grooming | Coordinator | Agile Consultant |
| Review | Coordinator | Agile Consultant |
| Retro | Yherder | Scrum Master |

Update each process arc with the correct user identity references. If a user identity from Arc 5 maps more naturally to a ceremony beat than the defaults above, use it — the table is a starting point, not a constraint.

**Belief transitions:**
- *"The ceremony arcs are wired to the right identities for this user"* — introduced as `active`

---

## Beat 1k — Generate Skills (Initial Workspace)
*Active identity: [[../identities/skill-generator]]*

For the initial workspace only, generate skills for all agent identities into `~/.claude/skills/`:
- `/scrum-master` — from scrum-master identity + agile-processes + agile-workflow
- `/agile-consultant` — from agile-consultant identity + agile-workflow + agile-manifesto

Also generate skills for any user identities from Arc 5 that are complex enough to warrant one.

Each skill is a lazy-loading expression: enough context to reason from the identity's belief systems without loading them all inline.

**Belief transitions:**
- *"The workspace has invokable skills"* — introduced as `active`

---

## Beat 1l — Wire CLAUDE.md
*Active identity: [[../identities/installer]]*

Create `CLAUDE.md` in each workspace root. This is the AEO-ready index — what Claude loads automatically when working in this workspace. Include:
- Workspace name and purpose (initial vs. ideal)
- Belief systems index: list each belief system file with one-line summary
- Characters: agent (scrum-master, agile-consultant) and user identities
- Active arcs: standup, planning, grooming, review, retro
- Task store location
- Retro log location

Then update the global `~/.claude/CLAUDE.md`:
1. Back up existing file to `~/.claude/CLAUDE.md.backup`
2. Add a workspace shim section at the top:

```
# Yherda Workspace
See ~/.claude/yherda/{name}-initial/CLAUDE.md for working context.
```

Everything else in the global CLAUDE.md stays intact below the shim.

**Belief transitions:**
- *"Claude will load the right context on startup"* — introduced as `active`

---

## Beat 1m — Close and Hand Off
*Active identity: [[../identities/installer]]*

> "Your workspace is set up. Here's what you have:
>
> **~/.claude/yherda/{name}-initial/** — your working context; agile belief foundation, ceremonies wired, skills ready
> **~/.claude/yherda/{name}-ideal/** — the clean version; same structure, no inherited friction
>
> Your global CLAUDE.md now points here. In any new session, Claude will orient from your workspace automatically.
>
> To start working: invoke `/scrum-master` for a standup, `/agile-consultant` for planning. Retro is how the model improves — the retro log is at `retro_log.md`.
>
> Bootstrap complete."

Hand off to `/scrum-master` to run the first standup.

**Belief transitions:**
- *"I have a belief architecture to build on"* — introduced as `active`
- *"The bootstrap is complete"* — introduced as `active`
