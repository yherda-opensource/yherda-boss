---
tags: [ceremony, arc, global]
---

# Ceremony Arc — Retro

**Owner:** User / Yherder — [[../agile-processes#1-every-ceremony-has-an-owner]]
**Want:** A groomed, integrated set of belief updates
**Need:** The working model reflects what the team has actually learned since the last retro

---

## Beat R1 — Surface the Retro Log
*Active identity: Scrum Master*

Read the retro log. Surface all candidates — wins, misses, process observations. Present as a flat list without editorializing.

> "Here's what's in the retro log since our last retro. {N} items. Let me read them out."

**Belief transitions:**
- *"The retro log has been surfaced"* — introduced as `active`

---

## Beat R2 — Groom the Log
*Active identity: User / Yherder*

User reviews the surfaced list. Adds anything missing, removes anything that doesn't belong or has already been resolved.

> "Is there anything missing from this list? Anything here that shouldn't be?"

*Iterative — until user confirms the list is complete and clean.*

**Belief transitions:**
- *"The retro log is groomed and ready for discussion"* — introduced as `active` on confirmation; `strained` if significant items are missing or disputed (agent updates log; beat repeats)

---

## Beat R3 — Select for Discussion
*Active identity: User / Yherder*

User selects which items to discuss this retro. Not everything needs to be discussed — some items may be deferred, some may be obvious enough to integrate directly.

> "Which of these do you want to work through? We can defer anything that isn't ready."

**Belief transitions:**
- *"The retro agenda is set"* — introduced as `active`

---

## Beat R4 — Flesh Out Retro Item
*Active identities: Scrum Master · User / Yherder*

For each selected item, iterate:

1. **State the belief** — write it as an aspirational statement, as if already held
2. **Assign status** — `active` if confident and tested; `emerging` if promising but unproven; `strained` if it conflicts with something currently held
3. **Define evidence criteria** — what would confirm this belief is holding? what would signal it's breaking down?
4. **Name affected identities** — which identities will reason differently if this belief is adopted?
5. **Identify impacted skills** — which skills will need to be re-expressed?
6. **SOS candidate check** — would another team with a similar context benefit from this belief without modification?

> "Let's work through {item}. How would you state this as a belief you already hold?"

*Iterative per item — one at a time until all selected items are fully specified.*

**Belief transitions (per item):**
- *"{Belief statement}"* — introduced at assigned status with evidence criteria noted

---

## Beat R5 — SOS Nomination
*Active identity: Scrum Master*

For any item flagged as an SOS candidate:

> "This looks like it could be useful to other teams. Want to nominate it to the community SOS belief system?"

If yes: mark for publication. Log task to submit PR to community SOS repo.

**Belief transitions:**
- *"This belief is worth sharing with the community"* — introduced as `active` for nominated items

---

## Beat R6 — Show What Changed
*Active identity: Scrum Master*

Present a summary of all belief changes from this retro — new beliefs introduced, statuses updated, beliefs retired.

> "Here's what changed this retro: {N} new beliefs, {M} status updates, {K} retired. {Summary of changes}."

**Belief transitions:**
- *"The team has a shared view of what changed this retro"* — introduced as `active`

---

## Beat R7 — Update the Yherder
*Active identity: Scrum Master*

Update the yherder registry with any new belief systems, identity changes, or priority shifts that resulted from this retro.

**Belief transitions:**
- *"The yherder reflects the current belief architecture"* — introduced as `active`

---

## Beat R8 — Regenerate Affected Skills
*Active identity: Scrum Master · Yherder*

Yherder reviews the belief changes and determines which skills are affected. For each affected skill, decide: re-express now or defer to next retro.

> "Based on what changed, {N} skills are affected: {list}. I'd re-express {these} now — the belief change is significant enough to affect how the agent reasons. I'd defer {these} — the change is minor and the current expression still holds."

*User confirms or adjusts the recommendation.*

**Belief transitions:**
- *"Affected skills have been re-expressed or deferred with reason"* — introduced as `active`

---

## Beat R9 — Confirm and Close
*Active identity: User / Yherder*

> "Retro complete. {Summary}. Retro log cleared of integrated items. Deferred items remain for next retro."

User confirms. Retro log updated — integrated items removed, deferred items flagged.

**Belief transitions:**
- *"This retro's learning is integrated into the working model"* — introduced as `active` if complete; `strained` if significant items were deferred (note reason; carry forward)
