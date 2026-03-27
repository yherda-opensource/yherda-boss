---
tags: [process, arc, global]
---

# Process Arc — Grooming

**Owner:** User / Coordinator — [[../agile-processes#1-every-ceremony-has-an-owner]]
**Want:** A backlog that is prioritized and ready to pull from
**Need:** The top items are fleshed out enough to execute without discovery work during planning

---

## Beat G1 — Surface the Backlog
*Active identity: Scrum Master*

Read the task store. Present the full backlog — current priority order, current status, brief description per item.

> "Here's the backlog as it stands:
>
> {prioritized list with brief context per item}
>
> Does this order still feel right?"

**Belief transitions:**
- *"The current backlog has been surfaced"* — introduced as `active`

---

## Beat G2 — Prioritize
*Active identity: User / Coordinator*

User reviews the order and adjusts. Move items up, down, defer, or remove entirely.

> "Move {ID} above {ID}." / "Park {ID} — not relevant anymore." / "That order looks right."

*Iterative — until user confirms the priority order.*

**Belief transitions:**
- *"The backlog priority reflects current intent"* — introduced as `active` on confirmation; `strained` if user is uncertain about relative priority (surface context per item; beat iterates)

---

## Beat G3 — Flesh Out Top Items
*Active identities: Scrum Master · User / Coordinator*

Starting from the top of the prioritized backlog, work through each item until it is executable:

1. Surface what's already captured — description, context, any linked belief systems or design notes
2. Identify what's missing — acceptance criteria, approach, dependencies, open questions
3. Go back and forth until both parties believe the item is ready to pull into planning without further discovery

> "For {item} — here's what we have: {context}. What's missing before we could just pick this up and go?"

*Iterative per item. Move to the next item when the current one is executable. Stop when the user is satisfied with the depth of coverage — not every item needs to be groomed every session.*

**Belief transitions (per item):**
- *"{Item} is ready to pull into planning"* — introduced as `active` when executable; `strained` if open questions remain that can't be resolved in this session (note gaps as tasks; item stays in backlog)

---

## Beat G4 — Confirm Groomed State
*Active identity: Scrum Master*

Summarize what changed — priority shifts, items fleshed out, items deferred or removed.

> "Grooming complete. {N} items re-prioritized, {M} items ready to pull, {K} items parked. Does this feel right?"

*User confirms or flags anything that landed wrong.*

**Belief transitions:**
- *"The backlog is groomed and ready for planning"* — introduced as `active` on confirmation; `strained` if significant items still feel underspecified (note and carry forward)
