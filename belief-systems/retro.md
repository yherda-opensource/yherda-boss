---
tags: [belief-system, global]
---

# Belief System — Retro

**Version:** 0.1
**Status:** Active — starts blank; populated during operation
**Tags:** #belief-system #retro #staging

---

## Prime Directive

A staging area for belief candidates that have been identified but not yet retro'd into a belief system. Not beliefs — candidates. The retro reads from here. The yherder watches this as a gap index before reaching for external context.

---

## Schema

Each candidate entry follows this structure:

```
### [Candidate belief statement — aspirational, as if already held]

**Suggested belief system:** which belief system this probably belongs in
**Identities affected:** which identities will need to know about this
**Flagged by:** agent | user
**Flagged during:** which arc or session
**Suggested status:** emerging | active | strained
**Context:** why this was flagged; what situation surfaced it
**Evidence so far:** any evidence already available; blank if none
```

---

## Candidates

### The yherder is an active context budget manager, not just a registry

**Suggested belief system:** yherda-operational
**Identities affected:** yherder
**Flagged by:** user
**Flagged during:** bootstrap design session 2026-03-27
**Suggested status:** emerging
**Context:** The yherder operates in two context management modes. Proactive: during skill generation, reads identity references and loads relevant belief systems ahead of time before the skill-generator starts — it doesn't wait to be asked. Throttling: during operation, intercepts when an agent is about to use training data or general knowledge when a belief system already covers it ("you have context for this — use it"), and conversely signals when belief systems are loaded unnecessarily for the current beat. The yherder is the only identity with full visibility into what's loaded, what's needed, and what can be deferred.
**Evidence so far:** The lookup order already establishes the yherder as the last internal check before going external. The budget management role extends this — not just a lookup sequence but active load/defer decisions throughout a session.



### "Think hard" is an instruction to reason from belief systems rather than heuristics

**Suggested belief system:** yherda-operational
**Identities affected:** yherder, all agent identities
**Flagged by:** user
**Flagged during:** bootstrap design session 2026-03-27
**Suggested status:** emerging
**Context:** When a user adds "think hard" to a prompt, it signals: decompress the relevant belief systems carefully, check the retro queue, reason from first principles rather than pattern-matching to the nearest familiar output. The belief architecture exists to support this — the difference is whether the agent uses it or shortcuts past it. "Think hard" is the explicit instruction not to shortcut.
**Evidence so far:** Compressions in arc files that look like explanatory paragraphs — when the agent pattern-matches to "add explanation" rather than trusting the link to carry the reasoning, it's doing the heuristic thing this belief is meant to prevent.
**Open question:** "Think hard" is already a compression collision in the Claude world — it has a specific meaning in Claude's extended thinking feature. A different keyword that doesn't collide with existing Claude behavior should be chosen. Candidates TBD.

### The arc owner leads regardless of which identity is performing the beat

**Suggested belief system:** yherda-operational
**Identities affected:** yherder, installer, skill-generator, agile-consultant
**Flagged by:** user
**Flagged during:** bootstrap design session 2026-03-27
**Suggested status:** emerging
**Context:** Arc ownership determines who sets direction and pace — the owner doesn't change beat to beat, the performers do. The arc owner's character is where ideas, suggestions, and guidance originate; other characters contribute but don't lead. Agent-owned arcs (1, 6) are ones the user genuinely can't lead — scanning config, migrating to Yherda are agent-domain work. User-owned arcs (2-5) are ones where the user knows the answer and the agent serves. Performer suggestions and pushback are always responsive to the owner's lead, never preemptive.
**Evidence so far:** Arc 5 role discovery — skill-generator suggestions only unblock when user stalls or names something too broad to decompose; never offered proactively.
**Note:** This belief is targeted for yherda-model, not just yherda-operational — it's a foundational claim about how arcs work, not just how the bootstrap runs.

### Evidence accumulation is a first-class integration pattern for belief development

**Suggested belief system:** yherda-operational
**Identities affected:** yherder, skill-generator
**Flagged by:** user
**Flagged during:** bootstrap design session 2026-03-27
**Suggested status:** emerging
**Context:** Shawn has an emerging idea about using evidence as a signal capture integration mechanism — attaching signals (market observations, user behavior, data points, conversation snippets) to belief candidates as they arrive, so evidence accumulates on a candidate while it sits in the retro queue. By the time the retro runs, the decision is already half-made. Evidence does the work before the retro is called.
**Evidence so far:** The parking lot pattern — `emerging` beliefs in the retro queue aren't stalled, they're ripening. The retro pulls them when evidence feels sufficient or when a decision can no longer wait.
