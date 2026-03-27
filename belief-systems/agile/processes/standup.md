---
tags: [process, arc, global]
---

# Process Arc — Standup

**Owner:** User / Yherder — [[../agile-processes#1-every-ceremony-has-an-owner]]
**Want:** A shared current picture of what's moving and what isn't
**Need:** Status is accurate, blockers are visible, the day is oriented

---

## Beat S1 — Surface Current State
*Active identity: Scrum Master*

Read the task store. Present a clean summary of current state — no editorializing, no recommendations yet.

> "Here's where things stand:
>
> **In Progress:** {list}
> **To Do:** {list}
> **Done since last standup:** {list}
>
> Anything to update?"

**Belief transitions:**
- *"The current task state has been surfaced"* — introduced as `active`

---

## Beat S2 — Receive Updates
*Active identity: User / Yherder*

User responds naturally — completions, changes of plan, new context, blockers.

> "Oh I finished X yesterday." → mark Done
> "I'm going to do Y tomorrow." → note intent
> "Z is blocked on {reason}." → flag blocker

*No interruptions — let the user finish before applying anything.*

**Belief transitions:**
- *"The agent has received the user's current status"* — introduced as `active`

---

## Beat S3 — Apply Updates and Surface Context
*Active identity: Scrum Master*

Apply all status changes to the task store. Then — and only if there is genuine context to add — surface it briefly:

- A dependency the user may not have considered
- A belief that's relevant to something they mentioned
- A task that looks blocked but wasn't flagged

If there's nothing load-bearing to add, skip this beat silently.

**Belief transitions:**
- *"The task store reflects the user's current reality"* — introduced as `active`

---

## Beat S4 — Announce the Day
*Active identity: Scrum Master*

Surface any ceremonies scheduled for today. If any need to move or be skipped, handle it now.

> "Today: {ceremony list}. Anything to change?"

If no ceremonies: omit.

*User confirms or adjusts.*

**Belief transitions:**
- *"The day is oriented"* — introduced as `active` on confirmation; `strained` if something significant is unresolved (note and carry forward)
