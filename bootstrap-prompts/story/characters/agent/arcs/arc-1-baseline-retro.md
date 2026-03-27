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

## Beat 1g — Create Workspaces
*Active identity: [[../identities/installer]]*

Create two new workspaces with yherda-model and agile-os imported as foundation belief systems:
- **{name}-yherda-boss-initial/** — carries forward `active`, `emerging`, and `strained` beliefs from baseline
- **{name}-yherda-boss-ideal/** — carries forward `active` and `emerging` beliefs only; starts clean of strained adaptations

Arc 1 complete. Arc 2 begins in the initial workspace.

**Belief transitions:**
- *"I have a belief architecture to build on"* — introduced as `emerging`; will earn `active` status through use
