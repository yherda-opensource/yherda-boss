---
tags: [belief-system, global]
---

# Belief System — Yherda Operational

**Version:** 0.1 (draft)
**Status:** Emerging — monolithic first; decompose into composable components once shape is stable
**Tags:** #belief-system #operational #yherda

---

## Prime Directive

The beliefs required to operate within the Yherda system — not what the model is structurally (that's yherda-model) but how to work it: how to translate existing context into beliefs, how arcs and beats run in practice, how retro integrates into the operating cycle, and how to present belief state to humans without overwhelming them.

---

## Part 1 — Decompression into Beliefs

### 1. Every piece of existing context maps to a story component
Config files, memory files, working agreements, habits, rules of thumb — all of it is a belief waiting to be named. The translation layer:
- A rule → a belief (stated as what is held to be true, not as an instruction)
- A working agreement → a belief system (named collection of related beliefs)
- A habit → an `active` belief (proven through repetition)
- An aspiration → an `emerging` belief (held but not yet tested)
- A rule that was tried and abandoned → a `former` belief with evidence
- A rule that feels wrong but is still followed → a `strained` belief

### 2. Beliefs are aspirational statements, not fear statements
A belief is what a character would want to hold as true — stated as an advantage. Never model the gap ("I don't know my audience"). Model the desired state ("I know what my audience currently believes"). The starting status on the belief captures where the character actually is.

### 3. Evidence is what makes a belief credible
A belief without evidence is an assumption. Evidence is attached to the belief — an experience, a data point, an observation that validates it is grounded. When translating existing context, look for evidence: why does this rule exist? What experience produced it? That's the evidence.

### 4. Gaps in translation become tasks
Anything that can't be cleanly mapped to a story component gets logged as a task with a description of what was found and why it didn't map. Nothing is dropped — it is deferred with a clear handoff.

### 5. The retro assigns honest status, not assumed status
When decompressing existing context, don't assume `active`. Run a retro: is this still believed? Is it acted on? Is it aspirational or proven? The honest status is more valuable than the optimistic one.

The retro only reviews beliefs that were flagged — by the agent noticing drift or friction, or by the user flagging something since the last cycle. Nothing flagged, nothing reviewed. The retro is a targeted diff, not a full audit of the belief system.

---

## Part 2 — Model Operation

### 6. An arc is driven by a want and a need
The want is the surface goal — what the character says they're after. The need is the belief that must change for the want to be achievable. An arc is complete when the need is resolved — not when the want is achieved. A want achieved without the need resolving is a hollow win.

### 7. A beat produces a belief transition or it produced no story progress
A beat that ends in conversation with no belief transition captured made no measurable progress. The transition is the checksum. It doesn't have to be a full resolution — a belief moving from `strained` to `emerging` is progress. But something must shift.

### 8. Belief transitions are operations on named beliefs, not narrative summaries
A transition is: this specific named belief moved from status X to status Y at this beat. The path matters — `strained → active` after evidence is different from `emerging → active` after smooth confirmation. The path tells you how firmly the belief is held and what might strain it again.

### 9. Evidence lives on the belief, not on the transition
The transition references the belief. The belief carries the evidence. When a transition moves a belief, the evidence that caused the movement is attached to the belief — not restated on the transition.

### 10. Two transitions model a belief swap
Moving from one belief to a contradicting one requires two transitions: one moving the old belief to `strained` or `former`, one introducing the new belief at `emerging` or `active`. These are distinct operations. The old belief's fate and the new belief's arrival are separate facts.

### 11. A new belief can arrive active
Not all new beliefs start `emerging`. An a-ha moment, a strong conviction from prior experience, a belief transferred intact from another context — these can arrive directly as `active`. The status reflects how the character holds it, not how recently it was introduced.

---

## Part 3 — Retro Integration

### 12. The retro is the belief system update mechanism
A retro is not a meeting — it is the process by which belief statuses are reviewed and updated. The output of a retro is a set of belief transitions: beliefs that moved, beliefs that were confirmed, beliefs that were dropped. The retro log is a compressed record of those transitions.

### 13. The retro belief system accumulates operational learnings
Every workspace maintains a retro belief system that captures:
- What was tried and how it landed (evidence on beliefs)
- What was strained and why
- What was resolved and what resolved it
- What was deferred and what it's waiting on

This belief system is the institutional memory of how the workspace actually operates — not how it was designed to operate.

### 14. Retro items are reviewed on demand, not all at once
A retro only reviews beliefs that were explicitly flagged by the agent or the user since the last cycle. Nothing flagged, nothing reviewed. Flagged beliefs are the ones where drift, friction, or doubt was noticed in practice — not a scheduled sweep of everything. The retro is a targeted diff, not a full read.

### 15. Opting into a new belief requires evidence, not just agreement
A retro can surface a new belief as a candidate. The character opts in by confirming they hold it — but the belief arrives as `emerging` until there is evidence. Conversation agreement produces `emerging`. Demonstrated experience produces `active`. The retro doesn't manufacture `active` beliefs — it creates the conditions for them to earn that status.

### 16. The yherder is the retro sink
Belief transitions from all active identities flow back into the yherder registry after every retro. The yherder updates. Affected skills recompile. The next cycle loads from updated skills. The retro document is the human-readable decompression of the yherder update.

---

## Part 4 — Human Presentation Layer

### 17. Show the transition path when the path changes the decision
The full transition path (`strained → emerging → active`) is load-bearing when the receiver needs to know how firmly a belief is held or what might strain it again. Show it when that context changes how they act. Omit it when they only need the outcome.

### 18. From→to is a valid lossy compression
Presenting a belief shift as "from X to Y" is a lossy compression of what may be multiple transitions. It is valid when the receiver doesn't need the path — only the outcome. The judgment: does knowing the path change what the receiver does? If not, from→to is sufficient and cleaner.

### 19. Never surface more belief state than the receiver can act on
A full belief system dump is not a useful output for a human. Surface what is relevant to the current decision or question. The human presentation layer is governed by [[expression-human]] — structure carries what words don't need to say; priority surfaces when conflict is possible; beauty is the standard.

### 20. Strained beliefs surface when they are blocking
A strained belief that isn't blocking anything doesn't need to be surfaced in every interaction. Surface it when it becomes relevant — when a decision is about to be made that the strained belief would affect, or when a retro is running and the belief is due for review.

### 21. The retro summary is a beautiful compression of what changed
A retro summary doesn't list every transition — it surfaces the ones that matter: what resolved, what newly emerged, what is still strained and why. It is a compression optimized for the receiver's ability to act on it. From→to for simple shifts. Full path for complex or consequential ones.

---

## Needs Development

- Belief about how to handle belief conflicts within a belief system
- Belief about how to present the gap between initial and ideal workspace to a human
- Belief about evidence quality — what counts as strong evidence vs. weak
- Belief about when a belief system is stable enough to compile to a skill
- Composable decomposition plan — which beliefs belong together as components
