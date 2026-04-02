---
tags: [belief-system, agile, arcs]
---

# Belief System — Arc Boundaries

**Version:** 0.1
**Status:** Emerging — surfaced during live bootstrap session
**Tags:** #belief-system #agile #arcs #skills

---

## Prime Directive

An arc is everything the agent does in one uninterrupted run between two human decision points. Arc boundaries exist to make skills invocable, context lean, and human gates explicit.

---

## Core Beliefs

### 1. An arc boundary is a human gate or a context budget concern — whichever comes first
Human gates are hard boundaries. The agent stops and waits; the human acts; a new prompt begins the next arc. Context budget is a soft boundary — if an arc is long enough to degrade reasoning, split it. Don't pre-split; let pressure tell you when.

### 2. An arc is the agent's uninterrupted run — not a phase, not a role
A single arc may involve multiple identities executing in sequence. The boundary is not where the identity changes — it's where the human gate is. Everything between two human decision points is one arc.

### 3. Skills are generated from arcs, not from roles
A skill answers: "agent, it's your turn — here's what you do." It runs to completion and stops at the human gate. A skill generated from a role rather than an arc carries the full role belief context into every invocation, whether needed or not. Arc-scoped skills stay lean.

### 4. The meta-arc is the Director's shot list — never a skill
The meta-arc documents the full sequence and where the human gates are. It is an index, not an executable. The Director loads it as workspace context; individual arc skills are what get invoked.

### 5. Don't pre-split arcs for context budget
Split arcs when context pressure actually surfaces — not in advance. A premature split forces the operator to remember and invoke two things where one would have sufficed. Let practice determine the right granularity.

### 6. Belief contexts load when the identity becomes active — not at workspace load
Loading the workspace loads the index (character map, shot list, team agreement). Belief contexts for each identity load when that identity's arc is invoked. Bulk-loading all belief contexts at session start defeats lazy loading.

---

## Builds On

- [[agile-processes]] — ceremony ownership; arcs as structured workflows with owners and outputs
- [[../yherda/expression-agent]] — lazy context loading; skill as optimized expression of a belief context
