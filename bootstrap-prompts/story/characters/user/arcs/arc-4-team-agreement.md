---
tags: [arc, bootstrap, user]
---

# Arc 4 — Team Agreement Setup

**Owner:** User / Coordinator — [[../../../../belief-systems/agile/agile-processes#1-every-ceremony-has-an-owner]]
**Want:** A shared understanding of what "ready" and "done" mean for this team
**Need:** DoR and DoD beliefs grounded in how this team actually works — confirmed, not inherited

---

## Beat 4a — Introduce DoR
*Active identity: [[../../agent/identities/agile-consultant]]*

Present the concept of Definition of Ready with plain-language explanation. Present base beliefs from agile-os.

> "Before work starts, we agree a piece of work is ready when these things are true. Here's a base set — tell me what to add, change, or remove for your situation."

**Belief transitions:**
- *"DoR is a useful concept for how I work"* — introduced as `emerging`

---

## Beat 4b — Receive and React to DoR
*Active identity: [[../identities/coordinator]]*

User encounters the DoR concept and base beliefs.

**Belief transitions:**
- *"DoR is a useful concept for how I work"* — `emerging → active` if they recognize its value; `strained` if they've tried it and it created bureaucracy ("nobody ever checked the list")
- *"I have a DoR that reflects how my team actually works"* — introduced as `strained` (base beliefs are a starting point, not their DoR yet)

---

## Beat 4c — Refine DoR
*Active identities: [[../../agent/identities/agile-consultant]] · [[../identities/coordinator]]*

User reviews each base DoR belief: confirm, correct, add, drop.

*Iterative — repeat until user is satisfied.*

**Belief transitions (per DoR belief, user):**
- Confirmed without friction: introduced as `active`
- "Yes but we do it differently": introduced as `strained → active` with their version as evidence
- Rejected outright: introduced as `former` — candidate, not their belief
- User adds new belief: introduced as `emerging` (untested) or `active` (proven in their context)

**Belief transitions (user, arc-level):**
- *"I have a DoR that reflects how my team actually works"* — `strained → active` when refinement is complete

---

## Beat 4d — Introduce DoD
*Active identity: [[../../agent/identities/agile-consultant]]*

Same pattern as Beat 4a applied to Definition of Done.

**Belief transitions:**
- *"DoD is a useful concept for how I work"* — introduced as `emerging`

---

## Beat 4e — Receive and React to DoD
*Active identity: [[../identities/coordinator]]*

**Belief transitions:**
- *"DoD is a useful concept for how I work"* — `emerging → active` or `strained` based on experience
- *"I have a DoD that reflects how my team actually works"* — introduced as `strained`

---

## Beat 4f — Refine DoD
*Active identities: [[../../agent/identities/agile-consultant]] · [[../identities/coordinator]]*

Same pattern as Beat 4c applied to DoD.

*Iterative — repeat until user is satisfied.*

**Belief transitions:**
- *"I have a DoD that reflects how my team actually works"* — `strained → active` when complete

---

## Beat 4g — Introduce Working Agreement
*Active identity: [[../../agent/identities/agile-consultant]]*

Present working agreement concept and base items: handling blockers, scope change, disagreements, production incidents.

**Belief transitions:**
- *"A working agreement makes collaboration more reliable"* — introduced as `emerging`

---

## Beat 4h — Receive and Refine Working Agreement
*Active identity: [[../identities/coordinator]]*

User reviews, adds, changes, removes.

**Belief transitions:**
- *"A working agreement makes collaboration more reliable"* — `emerging → active` if they engage meaningfully; `strained` if they're skeptical ("agreements don't survive contact with reality")
- *"My team has an explicit working agreement"* — introduced as `emerging` during refinement; `active` when confirmed

---

## Beat 4i — Store and Handoff
*Active identity: [[../../agent/identities/installer]]*

Store confirmed DoR, DoD, and working agreement as `story/belief-systems/team-agreement.md` with status per belief. Log guardrails that require human action as tasks.

**Belief transitions:**
- *"The team agreement is stored and the agent can act on it"* — introduced as `active`

---

## Beat 4j — Confirm and Review Tasks
*Active identity: [[../identities/coordinator]]*

> "Team agreement stored. Setup tasks for things I couldn't wire directly are in your task store. Arc 4 complete."

User reviews the task list generated during this arc.

**Belief transitions:**
- *"I know what still needs to be done to fully establish our agreements"* — introduced as `active` if task list is clear; `strained` if tasks feel vague or overwhelming (agent clarifies; beat iterates)
