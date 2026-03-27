---
tags: [process, arc, global]
---

# Process Arc — Planning

**Owner:** User / Coordinator — [[../agile-processes#1-every-ceremony-has-an-owner]]
**Want:** A committed set of work for the next cycle
**Need:** The todo list reflects what the user actually believes they can and should do next

---

## Beat P1 — Surface the Backlog
*Active identity: Scrum Master*

Read the task store. Present the backlog sorted by priority. Surface any in-progress or paused work carried forward from the last cycle. Surface any bugs or flagged emergencies from alternate input sources (email flags, incident logs, or other sources wired during setup or added via retro).

> "Here's the backlog by priority:
>
> **Carried forward (In Progress / Paused):** {list}
> **Bugs / Emergencies:** {list if any}
> **Backlog:** {prioritized list}
>
> What should be in To Do for this cycle?"

**Belief transitions:**
- *"The full picture of available work has been surfaced"* — introduced as `active`

---

## Beat P2 — Select Work
*Active identity: User / Coordinator*

User selects by ID — or confirms carried-forward items. Scrum Master moves selected items to To Do.

> "Add {ID}, {ID}, and keep {ID} in progress."

*No recommendations unless the user stalls — see agile-processes belief on arc ownership.*

**Belief transitions:**
- *"The To Do list for this cycle is selected"* — introduced as `emerging` during selection; `active` on confirmation

---

## Beat P3 — Add Context to Each Item
*Active identities: Scrum Master · User / Coordinator*

For each newly selected To Do item: surface existing context, flag anything missing.

> "For {item} — here's what's already captured: {context}. Anything to add before we move forward?"

If the item has a design doc or belief system reference, confirm it's current. If not, flag as a task.

*Iterative — one item at a time until all selected items have sufficient context to act on.*

**Belief transitions (per item):**
- *"{Item} is ready to act on"* — introduced as `active` if context is complete; `strained` if gaps remain (tasks logged; item stays in To Do)

---

## Beat P4 — Establish the Sprint Belief
*Active identity: Scrum Master*

Summarize the committed cycle: what's in progress, what's to do, what's been explicitly deferred.

> "This cycle: {N} items in progress, {M} items to do. Deferred: {list with reason}. Does this feel right?"

*User confirms or adjusts.*

**Belief transitions:**
- *"We have a shared belief about what this cycle contains"* — introduced as `active` on confirmation; `strained` if the user feels overcommitted or undercommitted (adjust selection; beat repeats)

---

## Beat P5 — Surface Upcoming Ceremonies
*Active identity: Scrum Master*

Note any ceremonies due this cycle — demo, retro, any external commitments surfaced in the task store.

> "This cycle includes: {ceremony list}. Anything to schedule or reschedule?"

*User confirms or adjusts. If nothing to surface, omit this beat.*

**Belief transitions:**
- *"The cycle cadence is set"* — introduced as `active`
