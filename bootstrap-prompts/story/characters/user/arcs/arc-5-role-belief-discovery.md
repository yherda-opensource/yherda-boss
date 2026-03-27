---
tags: [arc, bootstrap, user]
---

# Arc 5 — Role & Belief Discovery

**Owner:** User / Analyst — [[../../../../belief-systems/retro#the-arc-owner-leads]]
**Want:** A complete identity map for this user
**Need:** The user's roles named, their governing beliefs surfaced, and the right consolidation/splitting decided

---

## Beat 5a — Invite Role Articulation
*Active identity: [[../../agent/identities/skill-generator]]*

> "Tell me the different hats you wear in your work. Don't filter — just name them. Owner, builder, marketer, operator, coach, whatever they are for you."

Probe for undervalued roles: "Who handles X when it needs to happen? What frame do you use when deciding Y?"

**Belief transitions:**
- *"My operating roles can be named and organized"* — introduced as `emerging`

---

## Beat 5b — Name the Hats
*Active identity: [[../identities/analyst]]*

User articulates their roles — sometimes fluently, sometimes with surprise at what emerges.

**Belief transitions:**
- *"My operating roles can be named and organized"* — `emerging → active` as roles surface; may remain `emerging` if user feels they haven't captured everything yet
- *"I understand which roles drive most of my decisions"* — introduced as `emerging`

---

## Beat 5c — Surface Beliefs per Role
*Active identities: [[../../agent/identities/skill-generator]] · [[../identities/analyst]]*

For each role: "When you're in {role} mode — what's always true? What's the tiebreaker when things conflict? What do you know that someone new to this role wouldn't?"

*Iterative — one role at a time.*

**Belief transitions (per role, user):**
- Stable, tested beliefs stated with confidence: introduced as `active`
- Rules of thumb, usually true: introduced as `emerging`
- Instincts they can't fully articulate: introduced as `emerging` with a note; flag for retro

**Belief transitions (user, arc-level):**
- *"I understand which roles drive most of my decisions"* — `emerging → active` as belief patterns per role become clear

---

## Beat 5d — Present Consolidation
*Active identity: [[../../agent/identities/skill-generator]]*

Review the full role + belief map. Apply heuristic:
- **Merge:** beliefs compatible, context light, roles don't fight each other
- **Split:** reasoning context heavy, roles conflict, domain needs focused uncontaminated attention

> "I'd merge {A} and {B} — their beliefs are compatible and the context is light. I'd keep {C} separate — it's complex enough that mixing it with {D} would create noise. Does that match how you experience it?"

**Belief transitions:**
- *"The identity map is the right shape for the context window"* — introduced as `emerging`

---

## Beat 5e — React to Consolidation
*Active identity: [[../identities/analyst]]*

User responds to the consolidation proposal — confirms, pushes back, or refines.

*Iterative — agent revises and re-presents until user confirms.*

**Belief transitions:**
- *"The identity map is the right shape for the context window"* — `emerging → active` on confirmation; `emerging → strained` on pushback (agent revises; beat repeats)
- *"My roles have been organized in a way that feels true"* — introduced as `active` on confirmation; `strained` if anything feels off

---

## Beat 5f — Store Identities
*Active identity: [[../../agent/identities/skill-generator]]*

For each confirmed identity:
- Create `story/characters/{user-name}/identities/{identity}.md`
- Create `story/belief-systems/{domain}.md` with beliefs at confirmed status

For gaps: store what's known with beliefs at `emerging`. Log tasks for roles needing more discovery.

> "Your identity map is stored. {N} identities created. {M} tasks logged for roles that need more development. Arc 5 complete."

**Belief transitions:**
- *"The user's identity map is stored and ready for skill generation"* — introduced as `active` for complete identities; `strained` where significant gaps remain

---

## Beat 5g — Confirm Identity Map
*Active identity: [[../identities/analyst]]*

User sees the final identity map as stored.

**Belief transitions:**
- *"I have a belief architecture that reflects how I actually operate"* — introduced as `active` if the map feels complete and honest; `strained` if gaps are visible (tasks carry the remainder)
- *"I understand what the agent now knows about how I think"* — introduced as `active`
