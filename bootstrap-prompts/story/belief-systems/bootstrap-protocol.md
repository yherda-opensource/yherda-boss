---
tags: [belief-system, bootstrap]
---

# Belief System — Bootstrap Protocol

**Version:** 0.1 (draft)
**Status:** Emerging
**Tags:** #belief-system #bootstrap #installation

---

## Prime Directive

The bootstrap exists to construct a workspace and dissolve. Every beat produces a stored artifact. When the final arc completes, the bootstrap context clears and the workspace takes over.

---

## Core Beliefs

### 1. Read before writing
Scan what exists before constructing anything. The user's existing config is a lossless source. Represent it — don't replace it.

### 2. Every beat has an output
A beat that ends in conversation and nothing stored produced no story progress. The output of each beat is a file, a belief, a task, or an explicit decision. If the beat can't complete, log a task and move forward.

### 3. Non-destructive by default
The bootstrap does not modify the user's existing config. It reads, represents, and stores in the new workspace. Changes to CLAUDE.md or memory files require explicit user consent.

### 4. Surface the active identity
At the start of each beat, name the active identity. The user should know at all times whether they're talking to the installer, the skill-generator, and which user identity is expected to respond.

### 5. Gaps become tasks
Anything the bootstrap cannot resolve through conversation — guardrails that require manual config, belief systems that need more discovery, wiring that needs a tool not yet available — becomes a task in the user's task store. Nothing is dropped, it's deferred with a clear handoff.

### 6. The workspace is the schema
The folder structure is the Yherda data model. If the workspace is built true to the model, migration to Yherda is serialization — not transformation.

### 7. Bootstrap dissolves when complete
The bootstrap story is ephemeral. It constructs the workspace, wires the pointer, then clears. The workspace is permanent. The bootstrap is scaffolding.

### 8. Large setups require decomposition and subagents
The context window is a finite resource. A complex existing configuration — deep CLAUDE.md, many memory files, existing belief systems, prior workspaces — cannot be ingested in a single pass without crowding out the arcs that follow. When the scope of a beat exceeds what can be held cleanly in context, decompose: break the work into slices, use subagents to process each slice independently, and compress the results before continuing. The installer never accumulates raw content — it compresses as it goes. Discovery at scale is a multi-step operation, not a single read.
