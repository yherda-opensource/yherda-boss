---
tags: [belief-system, global]
---

# Belief System — Yherda Migration

**Version:** 0.1
**Status:** Emerging — not yet validated
**Tags:** #belief-system #migration #yherda

---

## Prime Directive

A workspace migrates to Yherda by mapping its files to the Yherda schema. The vanilla mapping is lossless for unmodified workspaces. Every divergence from the base templates is a mapping decision — not a silent loss. The retro activity log is the source of truth for what diverged and why.

---

## Core Beliefs

### 1. The vanilla mapping is the baseline
An unmodified workspace maps directly to Yherda schema with no decisions required. The mapping table below is authoritative for standard templates. If the workspace matches the templates, migration is serialization.

### 2. The retro activity log narrates every divergence
Every template change that went through retro is recorded in `retro_activity_log.md`. When migration runs — even months later — the installer reads the log and surfaces each divergence with its reason and evidence. Migration does not rediscover drift; the log narrates it.

### 3. Unmappable extensions become migration gap tasks, not silent losses
If a workspace extension has no corresponding Yherda schema object, it is flagged as a migration gap and logged as a task. Migration proceeds with everything that can be mapped. Nothing is silently dropped. The gap task carries the divergence description and the retro activity log entry that created it.

### 4. Workspace migration overrides extend, never replace, the vanilla mapping
If a workspace has local divergences, a workspace-level `yherda-migration.md` captures the override mappings. It references the vanilla mapping as its base and specifies only what differs. The vanilla mapping remains unchanged.

### 5. Schema drift is a community signal
If multiple workspaces develop the same extension independently, that extension is a candidate for the Yherda schema. The migration gap task is the contribution path — file it, and the platform team knows what the schema is missing.

---

## Vanilla Mapping Table

| Workspace file | Yherda object | Notes |
|---|---|---|
| `{workspace}/` | Storyline | Workspace root = one storyline |
| `characters/{name}/` | Character | One character per folder |
| `characters/{name}/identities/{name}.md` | Identity | Properties: name, priority, belief systems, description |
| `characters/{name}/arcs/{arc}.md` | Arc | Properties: name, owner, want, need, beats inline |
| `belief-systems/{name}.md` | Belief System | Properties: name, version, status, scope, prime directive |
| Belief within belief system file | Belief | Properties: statement, status, evidence, priority |
| Beat within arc file | Beat | Properties: name, active identity, description |
| Belief transition within beat | Belief Transition | Properties: belief ref, previous status, new status |
| `templates/tasks.md` | Task Store | Sections map to workflow states |
| Task entry in tasks.md | Task | Properties: id, title, date, context, acceptance criteria |
| `templates/retro_log.md` | Retro Log | Candidates queue; cleared after integration |
| `templates/retro_activity_log.md` | Retro Activity Log | Append-only; every entry maps to a belief transition |

---

## Builds On

- [[yherda-model]] — the schema being mapped to
