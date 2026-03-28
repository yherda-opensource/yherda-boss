---
tags: [belief-system, global]
---

# Belief System — Expression (Agent)

**Version:** 0.2
**Status:** Emerging — not yet validated
**Tags:** #belief-system #expression #skills #meta

---

## Prime Directive

A skill is a lossy expression of a modelled business slice, optimized for efficient and lazy context loading by an agent. The lossless source lives in Yherda. The skill is a derived artifact — generated from the model, not edited directly.

---

## Core Beliefs

### 1. The three operations on the model are setup, retro, and generate-skills
- **Setup:** user expresses their business in natural language → modelled compression into Yherda schema
- **Retro:** new idea arrives → express the relevant model slice → integrate the new belief → compress back
- **Generate-skills:** decompress model into identities and beliefs → recompress into coherent workflow → express as skill

All three are the same underlying mechanic — compress/express — applied at different points in the cycle.

### 2. A skill is optimized for lazy context loading
The skill drops what the agent doesn't need to reason well and keeps what it does. A skill that carries everything the model knows defeats lazy loading — it is a model dump, not an expression.

### 3. A prompt is a bias for a skill you haven't built yet
Prompts bridge gaps heuristically. They work until the situation changes. A skill replaces the prompt by closing the gap with a real belief — one that adapts, compounds, and doesn't need to be re-stated.

### 4. A belief system is ready to generate a skill when it is stable under retro
Premature skill generation compresses a belief system that still has gaps — the skill inherits the gaps and becomes a sophisticated bias. Stability under retro is the readiness gate.

### 5. Skill identity comes from the belief system, not the task
A skill named after a task ("write-email") is a heuristic. A skill named after a belief system ("communicator", "ops-engineer") is a capability. The belief system defines what the skill can reason about — the task is just one expression of it.

### 6. Skills compound through community calibration
A skill generated from a local belief system is useful to one person. A skill validated through community retro and contributed back is useful to everyone with the same gap. The community belief system repo is the mechanism.

### 7. Belief system first — skill generation is the final step
Domain knowledge captured during a session must land in a belief system file before a skill is generated. A skill that encodes knowledge not present in any belief system is a belief gap, not a valid skill — the gap just moved into the skill where it can't be updated through retro. The sequence is: discover beliefs → write belief system → generate skill as expression of that belief system.

### 8. A skill lives in its own named folder
Skills are stored at `~/.claude/skills/{skill-name}/SKILL.md`. The folder name is the invocation name. The entry point file is always `SKILL.md`. A skill file placed directly in the skills root (e.g. `~/.claude/skills/{skill-name}.md`) is malformed — it cannot be correctly loaded or updated.

---

## Builds On

- [[expression]] — universal expression beliefs; lossless source, derived artifacts, calibrated lossiness
- [[yherda-model]] — the schema the model compresses into
