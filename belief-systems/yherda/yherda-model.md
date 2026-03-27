---
tags: [belief-system, global]
---

# Belief System — Yherda Model

**Version:** 0.1 (draft)
**Status:** Emerging — not yet validated
**Tags:** #belief-system #model #shared #foundation

---

## Prime Directive

A story is a lossless compression of a complete idea. Every element of the model exists to preserve fidelity from the originator's intent to the receiver's understanding. Nothing in the model is decorative.

---

## The Model Hierarchy

### Story
The container. Holds a complete idea — the thing being compressed. A story is not a narrative; it is the structured architecture of an idea including all the beliefs required to transfer it intact.

- Has characters
- Has belief systems (story-level — extend global belief systems with context specific to this story)

### Character
A participant in the story. Characters hold beliefs, take on identities, and move through arcs. A character is not a persona — it is an agent whose belief state changes over time.

- Belongs to a story
- Has identities
- Has arcs

### Identity
A role a character takes within the story. Identities define how a character reasons — what belief systems they operate within. A character can hold multiple identities. An identity is cross-domain — the same identity (e.g. "operator", "decision-maker") can appear in any story. See [[expression-agent]] for how identities generate skills.

- Belongs to a character
- References one or more belief systems
- Cross-domain — reusable across stories

### Arc
A character's journey from one belief state to another. An arc has a want (the surface goal) and a need (the belief that must change). The arc is complete when the need is resolved — not when the want is achieved.

- Belongs to a character
- Has beats
- Has a starting belief state and a target belief state

### Beat
A single step in an arc. A beat is the smallest unit of story progress — one thing that happens that moves the character toward or away from the belief transition. Beats are ordered within an arc.

- Belongs to an arc
- Has belief transitions

### Belief Transition
The moment a belief changes on a beat. A belief transition is the checksum — proof that something actually shifted. Without a belief transition, the beat produced no story progress regardless of what happened. References a specific belief.

- Belongs to a beat
- References a belief
- Has evidence

### Belief
A statement of what a character holds to be true. Beliefs have states — they can be held, challenged, or resolved. A belief is not binary; it has a trajectory. Beliefs live in belief systems.

- Belongs to a belief system
- Has evidence (optional — validates that the belief is grounded)
- Referenced by belief transitions

### Evidence
What makes a belief credible. Evidence is attached to a belief and validates that the belief is grounded in something real — an experience, a data point, an observation. Without evidence a belief is an assumption.

- Belongs to a belief and referenced by belief transitions
- Validates that a belief transition actually held

### Belief System
A named collection of related beliefs. Belief systems are the unit of compression and reuse. They can be global (cross-domain, shared across stories) or story-level (extend a global belief system with specific context). Belief systems generate skills when stable. See [[expression-agent]].

- Global belief systems live in `belief-systems/` at vault root
- Story-level belief systems live in `workspaces/{story}/belief-systems/`
- Referenced by identities
- Generate skills when retro-validated

---

## Folder Structure (derived from model)

```
workspaces/
  {story}/
    story/                     ← lossless source; canonical; never derived
      characters/
        {character}/
          arcs/
            {arc}.md           ← beats inline; belief transitions inline within beats
          identities/
            {identity}.md      ← references belief systems
      belief-systems/          ← story-level; extend global belief systems
    human/                     ← beautiful decompression for human reading
    agent/                     ← recollection-optimized decompression for Claude

belief-systems/                ← global; cross-domain; shared
skills/                        ← generated from validated belief systems
  belief-systems/              ← governs skill generation behavior
bootstrap-prompts/             ← derived from belief systems; what users receive
  belief-systems/              ← governs bootstrap generation behavior
```

## Representation Principle

Three layers — one source:
- **story/** is the lossless source. Edit here only. Never optimized for any channel.
- **human/** is a beautiful compression derived from story/ — expressive, narrative, fits on one page for simple stories, folder structure for complex ones
- **agent/** is a deliberately engineered bias derived from story/ — tuned to how a specific model reasons; one compression per model (claude, copilot, codex) if needed

Human and agent layers are generated, not edited. If the story changes, regenerate both. Drift between layers = loss of fidelity.

## The Agent Compression is an Engineered Bias

The agent/ folder is not a summary — it is a calibrated bias introduced into a model's configuration. The distinction from a prompt heuristic:

- A **prompt heuristic** is an accidental bias — it bridges a gap without understanding the gap
- An **agent compression** is a deliberate bias — derived from a lossless source, tuned to a specific model's reasoning strengths, validated through retro, replaceable without touching the source

Each model may get a different compression. Claude reasons differently than Copilot. The story/ folder holds the truth. The agent/ folder holds the engineered bias that makes that truth legible to a specific model at lowest context cost.

**When to use single page vs folder in human/:**
A story fits on one page when a human can hold the full arc in working memory while reading. When characters, identities, or arcs multiply beyond that threshold, decompress into folders. The threshold is the reader's working memory, not a line count.

---

## Priority

Priority is a single field with consistent meaning across the model:

- **On a belief** — signals it's a value; load-bearing across all decisions; tiebreaker when beliefs conflict
- **On a belief system** — signals which frame is primary when systems conflict
- **On an identity** — signals context load order; high priority identities establish the reasoning frame before lower priority ones add nuance

Priority is explicit in **story/** — every belief, belief system, and identity carries a priority value. This is the design surface.

Priority becomes **load order** in **agent/** — the compression is sequenced by priority so the most load-bearing beliefs consume context first, leaving maximum window for situational reasoning. The optimization target: every token doing belief work, remainder free for the situation.

Priority is **selectively visible** in **human/** — surface it only when knowing it changes how the reader understands or uses the content. If the structure makes the hierarchy self-evident, the number adds noise. If two beliefs feel equal weight but one outranks the other in a conflict, surface it. The test: does seeing the priority help the human make a better decision?

This judgement — what to show and what to let structure carry — is itself a belief governed by the human compression belief system. See [[expression-human]].

---

## Key Principles

- **Beats contain belief transitions inline** — a beat file describes what happened and what belief shifted; no separate folder needed
- **Evidence lives on the belief** — not on the transition; the transition references the belief which carries the evidence
- **Identities are cross-domain** — the same identity file can be linked from any character in any story
- **Belief systems are the unit of reuse** — not characters, not arcs; belief systems are what migrate to Yherda, generate skills, and feed the community

---

## Migration Note

This model maps directly to the Yherda platform data model. When Yherda is ready, vault contents import as-is. The folder structure is the schema.
