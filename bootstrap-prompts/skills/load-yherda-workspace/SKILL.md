# Skill — /load-yherda-workspace

Load a Yherda Boss workspace as the active context for this session.

---

## When to invoke

Invoke this skill at the start of any session where you want to work within a Yherda belief architecture. If no workspace is active, you are working without a belief model — invoke this first.

---

## What this skill does

1. List all available workspaces under `~/.claude/yherda/`
2. Present the list to the user
3. User selects a workspace
4. Read the selected workspace's `CLAUDE.md` and load it as active context
5. Confirm which workspace is now active and what it contains

---

## Execution

**Step 1 — List workspaces**

Read the contents of `~/.claude/yherda/`. Each subdirectory is a workspace. Present them:

> "Available workspaces:
>
> {N}. {workspace-name} — {one-line description from workspace CLAUDE.md if available}
> ...
>
> Which workspace do you want to load?"

If no workspaces found:
> "No Yherda workspaces found at ~/.claude/yherda/. Run the Yherda Boss bootstrap to create one."
Stop here.

**Step 2 — Load selected workspace**

Read `~/.claude/yherda/{selected}/CLAUDE.md`. This file is the AEO-ready index for the workspace — belief systems, characters, active arcs, task store, skills.

Write `~/.claude/yherda/.active` with the selected workspace name. This satisfies the session hook so tool use proceeds normally.

Confirm:
> "Loaded: {workspace-name}
>
> Belief systems: {count} ({list names})
> Characters: {agent identities} | {user identities}
> Active arcs: {list}
> Skills: {list invocation names}
>
> Ready. What would you like to work on?"

---

## Context priority for this session

Once a workspace is loaded, follow this lookup order before answering any question or taking any action:

1. **What the user just said** — their current message, intent, and any explicit context they've provided. This always comes first.
2. **Active workspace belief systems** — reason from the belief systems loaded from the workspace. If a belief system covers the domain, use it. Do not substitute training data when a belief exists.
3. **Retro log** (`retro_log.md` in the active workspace) — before reaching for training data or external sources, check the retro queue. A pending candidate may already capture the decision. If so, surface it: "We haven't formally decided on this yet — want to work with the candidate or retro on it first?"
4. **Training data / general knowledge** — only when none of the above has an answer.
5. **Internet / external sources** — only when training data is also insufficient, and only when the user has not indicated the answer should come from the workspace model.

The workspace model exists so that reasoning stays grounded in what this user actually believes — not in what Claude would default to. Defaulting past the belief systems to training data is a context leak. The retro queue is the last internal check before that happens.

---

## Session hook

The bootstrap installs a PreToolUse hook that blocks tool use until a workspace is loaded. It checks for `~/.claude/yherda/.active` — a marker file the workspace loader writes on activation.

The hook script lives at `~/.claude/hooks/require-yherda-workspace.sh`. It is registered in `~/.claude/settings.json` during bootstrap.

To disable: remove the hook entry from `~/.claude/settings.json`.

**On workspace load**, this skill writes `~/.claude/yherda/.active` with the selected workspace name so the hook passes.

**On `/clear`**, the marker is not automatically removed — the hook will not re-block mid-session. To enforce re-selection on the next session, the marker can be removed manually or via a SessionStart hook if desired.

---

## Workspace switching

To switch workspaces mid-session, invoke `/load-yherda-workspace` again. The new workspace replaces the current active context.
