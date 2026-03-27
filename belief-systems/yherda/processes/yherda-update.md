---
tags: [process, arc, yherda]
---

# Process Arc — Yherda Update

**Owner:** User / Yherder — [[../../agile/agile-processes#1-every-ceremony-has-an-owner]]
**Want:** The workspace belief systems current with the community baseline
**Need:** Local divergences are known, community updates are queued for retro, nothing is adopted silently

---

## Prime Directive

The Yherda update process is the local stand-in for Scrum of Scrums. It polls GitHub for changes to yherda-boss base belief systems, diffs them against the workspace, and drops candidates into the retro queue. When the workspace migrates to Yherda, subscribed community queues are added as additional sources — the process runs unchanged.

---

## Beat U1 — Check for Updates
*Active identity: Scrum Master*

Pull the latest yherda-boss from GitHub. Identify which base belief system files changed since the last update was run.

> "Checking yherda-boss for updates..."

If no changes: confirm and close.

**Belief transitions:**
- *"The latest yherda-boss base has been retrieved"* — introduced as `active`
- *"There are no base belief system updates"* — introduced as `active` if no changes; arc closes here

---

## Beat U2 — Diff Against Workspace
*Active identity: Scrum Master*

For each changed base belief system file, compare against the workspace version:

- **Unchanged workspace:** candidate is a straightforward update — low friction to adopt
- **Locally modified workspace:** candidate requires a merge decision — surface the conflict clearly
- **New file in base:** candidate is a new belief system the workspace doesn't have yet

**Belief transitions:**
- *"The diff between base updates and workspace is complete"* — introduced as `active`

---

## Beat U3 — Check Migration Mapping
*Active identity: Scrum Master*

For each candidate, check whether the change affects the vanilla migration mapping in `yherda-migration.md`. If a base template changed in a way that shifts the schema mapping, flag it alongside the retro candidate.

**Belief transitions:**
- *"Migration mapping implications have been checked"* — introduced as `active`
- *"This update has migration mapping implications"* — introduced as `strained` per affected candidate; flagged for retro attention

---

## Beat U4 — Populate Retro Queue
*Active identity: Scrum Master*

Drop all candidates into `retro_log.md`. For each:

- State what changed in the base and why (from commit message)
- Note whether the workspace version diverges and how
- Flag any migration mapping implications
- Mark as `flagged by: github-update`

Nothing is adopted here. Retro decides.

**Belief transitions:**
- *"Base belief system update candidates are in the retro queue"* — introduced as `active`

---

## Beat U5 — Confirm
*Active identity: User / Yherder*

> "{N} update candidates added to the retro queue from yherda-boss. {M} have migration mapping implications. Nothing adopted — retro decides."

User confirms.

**Belief transitions:**
- *"The workspace is aware of available community updates"* — introduced as `active`

---

## Builds On

- [[../yherda-migration]] — migration mapping check in Beat U3
- [[../../agile/processes/sos]] — generalised version of this process; same output, broader sources
