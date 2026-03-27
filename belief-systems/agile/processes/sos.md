---
tags: [process, arc, global]
---

# Process Arc — Scrum of Scrums

**Owner:** User / Yherder — [[../agile-processes#1-every-ceremony-has-an-owner]]
**Want:** The workspace retro queue populated with community belief candidates
**Need:** Changes from subscribed belief system sources are surfaced and ready for retro consideration

---

## Prime Directive

The SoS process polls one or more belief system sources and drops new candidates into the retro queue. The source varies — GitHub diff for local update, Yherda subscribed queues for community SoS — but the output is always the same: retro candidates with context.

---

## Beat SOS1 — Identify Sources
*Active identity: Scrum Master*

Determine which sources to poll this run:

- **Local update:** yherda-boss main branch on GitHub — diff base belief systems against workspace versions
- **Yherda community:** subscribed belief system queues — public global, tenant, or named communities
- **Both:** run in sequence

> "Polling {source list}. Checking for belief system updates."

**Belief transitions:**
- *"The update sources are identified"* — introduced as `active`

---

## Beat SOS2 — Poll Sources and Diff
*Active identity: Scrum Master*

For each source, retrieve the latest belief system state and diff against the current workspace:

- New beliefs not present in the workspace
- Updated beliefs where the statement or status changed
- Retired beliefs still active in the workspace

Collect all differences as raw candidates. Deduplicate across sources.

**Belief transitions:**
- *"The diff against subscribed sources is complete"* — introduced as `active`
- *"There are no updates available"* — introduced as `active` if diff is empty; arc closes here

---

## Beat SOS3 — Surface Candidates
*Active identity: Scrum Master*

Present the diff as a readable summary before adding anything to the retro queue.

> "Found {N} updates across {sources}:
>
> **New beliefs:** {list}
> **Updated beliefs:** {list}
> **Retired beliefs still active here:** {list}
>
> Adding all to the retro queue for consideration."

**Belief transitions:**
- *"The available updates have been surfaced"* — introduced as `active`

---

## Beat SOS4 — Populate Retro Queue
*Active identity: Scrum Master*

For each candidate, append to `retro_log.md` using the retro log schema:

- Belief statement from the source
- Suggested belief system
- Flagged by: `sos` or `github-update`
- Context: what changed and why (from the source commit message or community annotation if available)
- Evidence so far: the source community's evidence if provided

**Belief transitions:**
- *"Community belief candidates are in the retro queue"* — introduced as `active`

---

## Beat SOS5 — Confirm
*Active identity: User / Yherder*

> "{N} candidates added to the retro queue. They'll be reviewed at the next retro. Nothing has been adopted — retro decides."

User confirms or flags anything that looks wrong.

**Belief transitions:**
- *"The retro queue reflects the latest community updates"* — introduced as `active`
