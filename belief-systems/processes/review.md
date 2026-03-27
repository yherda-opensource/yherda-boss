---
tags: [process, arc, global]
---

# Process Arc — Review

**Owner:** User / Coordinator — [[../agile-processes#1-every-ceremony-has-an-owner]]
**Want:** A clear release decision for everything ready to ship
**Need:** DoD is validated per item and the team has a shared belief about what is actually done

---

## Beat RV1 — Surface Ready for Release
*Active identity: Scrum Master*

Read the task store. Present all items in Ready for Release state.

> "Here's what's ready for release this cycle:
>
> {list with brief description of what was done per item}
>
> Let's walk through each one."

If nothing is ready for release, note it and close.

**Belief transitions:**
- *"The release candidates have been surfaced"* — introduced as `active`

---

## Beat RV2 — Validate DoD Per Item
*Active identities: Scrum Master · User / Coordinator*

For each item, walk through the Definition of Done. Confirm each criterion is met or flag where it isn't.

> "For {item} — {what was done}. DoD check: {criteria}. Anything that didn't land?"

*Iterative — one item at a time.*

**Belief transitions (per item):**
- *"{Item} meets the Definition of Done"* — introduced as `active` if all criteria met; `strained` if gaps found (note gaps; item held from release decision)

---

## Beat RV3 — Release Decision
*Active identity: User / Coordinator*

For all items that passed DoD: release or hold?

> "Everything checks out on {list}. Release?"

User decides. Items confirmed for release move to Done. Items held are flagged with reason.

**Belief transitions:**
- *"The release decision is made"* — introduced as `active`
- *"{Item} is released"* — introduced as `active` per released item
- *"{Item} is held from release"* — introduced as `strained` per held item with reason noted

---

## Beat RV4 — Deferral and Rollback
*Active identity: Scrum Master*

For any held items: determine disposition.

- **Defer** — item stays in Ready for Release; picked up next cycle
- **Rollback** — item reverted; moved back to To Do or Backlog with reason noted

> "For {held item} — defer to next cycle or roll back?"

*High level — the specifics of rollback execution are handled outside this ceremony.*

**Belief transitions (per held item):**
- *"{Item} is deferred to next cycle"* — introduced as `emerging`
- *"{Item} has been rolled back"* — introduced as `active` with reason noted

---

## Beat RV5 — Confirm and Close
*Active identity: Scrum Master*

Summarize the cycle outcome.

> "Review complete. Released: {list}. Held: {list with reason}. Rolled back: {list}."

User confirms.

**Belief transitions:**
- *"The cycle outcome is known and agreed"* — introduced as `active` on confirmation
