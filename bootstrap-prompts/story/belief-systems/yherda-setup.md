---
tags: [belief-system, bootstrap]
---

# Belief System — Yherda Setup

**Version:** 0.2 (draft)
**Status:** Emerging
**Tags:** #belief-system #bootstrap #yherda-setup

---

## Prime Directive

The beliefs required to reason about setting up a Yherda Boss workspace correctly. The architectural knowledge that lives in the yherda-consultant and yherder identities — not what the model is, but how to instantiate it for a specific user.

---

## Core Beliefs

### 1. Three workspaces, one user
Every Yherda Boss setup produces three workspaces:
- **baseline/** — honest retro'd snapshot of where the user was; beliefs at their true status; permanent fallback
- **~/.claude/yherda/{name}-initial/** — where they actually are after reconciling existing habits with agile and yherda beliefs; carries real adaptations and compromises; the working context
- **~/.claude/yherda/{name}-ideal/** — the clean version; what the belief architecture looks like without accumulated workarounds; generated from the same retro but without carrying strained adaptations forward

### 2. Baseline is permanent, not transitional
Baseline is not a migration artifact. It is the honest snapshot of the user's belief state before Yherda Boss. It stays frozen at the retro moment — a reference point, not an active workspace. The fallback for context outside any defined domain.

### 3. Initial and ideal are maintained in parallel
The initial workspace reflects how the user actually works today. The ideal workspace reflects what the agent would recommend without inherited friction. Both are live. The gap between them is the most useful information in the system — it shows exactly where friction lives.

### 4. The comparison does the persuasion
The agent never imposes the ideal. When the initial workspace has accumulated enough adaptations to be noticeably less smooth than the ideal, the agent offers:
> "Your process has some friction with your adaptations. Do you want to try a clean context with the ideal workspace?"
The user decides. The offer is a belief transition moment for the yherder — not a criticism, an invitation.

### 5. Initial converges toward ideal or ideal updates
Over time the initial workspace either converges toward the ideal through retros, or it reveals the ideal was wrong and needs updating. Both outcomes are valid. The gap is diagnostic, not prescriptive.

### 6. The CLAUDE.md shim is the workspace selector
A pointer at the top of CLAUDE.md determines which workspace is active. Swapping the pointer switches context. Multiple workspaces (personal, company, project) can coexist — only one is active per session.

### 7. Full belief system packages install at workspace creation
When initial and ideal workspaces are created, the full `belief-systems/yherda/` and `belief-systems/agile/` packages are copied in. The workspace `CLAUDE.md` indexes all of them so Claude orients correctly on startup without hunting. All subsequent domain beliefs build on this foundation.

### 8. The workspace boundary is a belief transition
The move from baseline to initial/ideal is not administrative — it is the moment the user transitions from "I have config" to "I have a belief architecture." The Arc 1/Arc 2 boundary is load-bearing.

### 9. Arc 1 is a retro, not a discovery
The installer's first act is to run a retro on the user's existing belief state — not just capture what exists, but surface the honest status of each belief:
- Still believe it, acting on it → `active`
- Should do more with it → `emerging`
- Starting to trust it less → `strained`
- Don't want to believe it anymore → `former`
- Never really believed it, just wrote it down → `strained` from the start

What survives the retro moves into initial and ideal. What doesn't stays in baseline.

### 10. Skills are the compiled output of stable belief systems
Once a belief system is retro-validated, it compiles to a skill. The skill carries the belief system's reasoning without requiring the full context loaded inline. Bootstrapping a new user = load the right skills, run the arcs.

---

## Needs Development

- Belief about how to handle workspace conflicts (user has prior Yherda workspace)
- Belief about versioning — when does baseline get updated vs. remain frozen
- Belief about multi-workspace session switching mechanics
- Belief about when to offer the ideal workspace switch — what signals enough friction
