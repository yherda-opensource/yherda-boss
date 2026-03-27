---
tags: [belief-system, global]
---

# Belief System — Agile Processes

**Version:** 0.1
**Status:** Emerging — not yet validated
**Tags:** #belief-system #agile #processes #ceremonies

---

## Prime Directive

A ceremony is a structured arc with an owner, a set of beats, and a defined output. The output is always a belief state change — not a list of action items, not a status update. If no beliefs changed, the ceremony produced nothing.

---

## Core Beliefs

### 1. Every ceremony has an owner
The owner sets direction and pace. Other identities perform beats within the ceremony but do not lead. The owner's character is where decisions originate.

### 2. The retro is the most load-bearing ceremony
Standup verifies alignment. Planning sets direction. Demo validates delivery. Retro is the only ceremony that updates the model itself. Everything else operates within the belief architecture — retro is how the architecture improves.

### 3. The retro log is the input queue, not the agenda
Items in the retro log are candidates — flagged during operation, not yet integrated. The retro grooms the log first, then selects for discussion. The agenda is determined by what's in the log, not by what feels important on the day.

### 4. A retro item is not complete until the belief is fully specified
A retro item that produces "we should do better at X" is not complete. Complete means: belief statement written, status assigned (active/emerging/strained), evidence criteria defined, affected identities named, impacted skills identified.

### 5. Scrum of scrums candidates are beliefs worth sharing
A belief that holds in one team's context and is likely to hold in others is a scrum of scrums candidate. Publishing it to the community SOS belief system makes it available for subscription. The test: would another team with a similar context benefit from this belief without modification?

### 6. Skill regeneration follows belief integration
When a retro integrates a new belief, the yherder determines which skills are affected and which need to be re-expressed. Not all belief changes require skill updates — only those where the change affects how the agent reasons in that domain.

### 7. Process extensions are introduced through retro, not by editing base templates
The base process arcs in `processes/` are community-maintained templates. A team that wants to extend a process — adding an email flag input to planning, for example — does so by adding a beat to their local copy of the arc, not by modifying the base template. The extension is a retro output: belief specified, evidence criteria defined, local arc updated. If the extension is a scrum of scrums candidate, it is nominated for the community base template via PR. This keeps the base templates stable and the community learning visible.

---

## Ceremony Process Map

| Ceremony | Owner | Agent identity | Output |
|---|---|---|---|
| Standup | User / Yherder | Scrum Master | Alignment on current belief state |
| Planning | User / Coordinator | Agile Consultant | Committed belief set for the sprint |
| Demo | User / Coordinator | Agile Consultant | Validated delivery beliefs |
| Retro | User / Yherder | Scrum Master | Updated belief systems; regenerated skills |

---

## Builds On

- [[agile-workflow]] — cadence and scheduling
- [[agile-os]] — belief synchronization interpretation
- [[agile-manifesto]] — the foundation
