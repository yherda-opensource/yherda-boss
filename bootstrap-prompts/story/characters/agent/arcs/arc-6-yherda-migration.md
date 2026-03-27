---
tags: [arc, bootstrap, agent]
---

# Arc 6 — Yherda Migration

**Owner:** Agent / Installer — [[../../../../belief-systems/retro#the-arc-owner-leads]]
**Want:** The working model transferred to Yherda
**Need:** The user understands what Yherda adds and has chosen the right account structure before migration begins — fidelity validated, nothing dropped

---

## Beat 6a — Establish the Vault as Complete
*Active identity: [[../identities/installer]]*

> "Everything you've set up works as-is. Your vault runs locally with Claude — ceremonies, roles, team agreements, skills. You don't need to go further than this if you're working solo or with agents only."

Establish clearly: the vault is not a stepping stone. It is a valid long-term working model.

**Belief transitions:**
- *"The vault is sufficient for solo operation"* — introduced as `active`
- *"Yherda is an upgrade, not a requirement"* — introduced as `active`

---

## Beat 6b — Read the Vault for Collaboration Signal
*Active identity: [[../identities/installer]]*

Read the working model from Arcs 1-5. Look for collaboration signals: human collaborators named in roles, team agreements involving external parties, belief systems that reference others.

If signals found, surface them:
> "I can see you're working with {collaborators}. Were you thinking of setting this up so they could work from the same model?"

If no signals found:
> "It looks like this is a solo setup — agents and you. Yherda is available when that changes."

**Belief transitions:**
- *"The agent understands my collaboration context"* — introduced as `emerging`

---

## Beat 6c — Receive Collaboration Intent
*Active identity: [[../../user/identities/groundwork]]*

User responds — solo, small team of partners, or larger organization.

**Belief transitions:**
- *"The agent understands my collaboration context"* — `emerging → active`
- *"I understand when Yherda becomes relevant to how I work"* — introduced as `active` if they see the fit; `emerging` if still evaluating; arc closes here if they want to defer — vault stays the working model

---

## Beat 6d — Recommend Account Structure
*Active identity: [[../identities/yherda-consultant]]*

Based on collaboration intent, reason to a recommendation:

**Solo or agents only:**
> "A personal account is all you need. Free tier covers it."

**Small team of partners (photographer, editor, collaborators):**
> "You'll want to share belief systems across accounts. That works in the community tier — just be aware that what you share between accounts is visible to the broader community. If any of that work needs to stay private, a tenant is the better fit."

**Privacy required or organization with multiple users:**
> "Based on what I see in your working model, a tenant makes sense. That's a private space — your belief systems, your team, your skills. Starts at $2,000/year, five seats, expandable in blocks of five."

**Belief transitions:**
- *"I understand which Yherda account structure fits how I work"* — introduced as `emerging`

---

## Beat 6e — React to Recommendation
*Active identity: [[../../user/identities/groundwork]]*

User responds to the recommendation — agrees, pushes back, or needs more information.

**Belief transitions:**
- *"I understand which Yherda account structure fits how I work"* — `emerging → active` on agreement; `strained` if they disagree or have concerns (agent clarifies; beat iterates)
- *"I am ready to set up a Yherda account"* — introduced as `active` on agreement; arc defers if not ready — vault stays the working model, belief logged as `emerging`

---

## Beat 6f — Build Migration Manifest
*Active identity: [[../identities/installer]]*

Traverse the workspace. Build manifest: all characters, identities, belief systems with statuses, arcs, beats, task store location.

**Belief transitions:**
- *"The workspace is ready to migrate"* — introduced as `emerging`

---

## Beat 6g — Review Manifest
*Active identity: [[../../user/identities/groundwork]]*

> "Here's what I'm about to migrate. {N} characters, {M} identities, {K} belief systems, {J} arcs. Confirm and I'll proceed."

User reviews — confirms completeness or flags gaps before transfer begins.

**Belief transitions:**
- *"The workspace accurately represents what I've built"* — introduced as `active` on confirmation; `strained` if gaps found (agent addresses; beat repeats)
- *"The workspace is ready to migrate"* — `emerging → active` on confirmation; `emerging → strained` if gaps found

---

## Beat 6h — Map to Yherda Model
*Active identity: [[../identities/installer]]*

One-to-one mapping — workspace structure is the schema:

| Workspace | Yherda |
|---|---|
| workspace/ | storyline |
| characters/{name}/ | character |
| identities/{name}.md | identity |
| belief-systems/{name}.md | belief system |
| arcs/{arc}.md | arc (beats and transitions inline) |
| belief in .md file | belief (with stored status) |
| evidence: line | evidence |

Note any items that don't map cleanly. Log as tasks.

**Belief transitions:**
- *"The workspace is ready to migrate"* — `active` if mapping is clean; `strained` if gaps found (tasks logged; proceed with mappable content)

---

## Beat 6i — Transfer
*Active identity: [[../identities/installer]]*

Call Yherda MCP in sequence: storyline → characters → identities → belief systems → beliefs (with status preserved) → arcs → beats → transitions. Install and configure MCP server connection.

Log any errors as tasks. Partial migration is acceptable; gaps must be tracked.

**Belief transitions:**
- *"The workspace content exists in Yherda"* — introduced as `emerging` during transfer; `active` on completion; `strained` if errors occurred

---

## Beat 6j — Validate Fidelity
*Active identity: [[../identities/installer]]*

Read back from Yherda. Compare against manifest. Surface any gaps.

**Belief transitions:**
- *"The Yherda representation is a lossless migration of the workspace"* — introduced as `active` if validation passes; `strained` if gaps found (tasks carry remaining work)

---

## Beat 6k — Review Migration Results
*Active identity: [[../../user/identities/groundwork]]*

> "Migration complete. {N} items transferred successfully. {M} gaps found — logged as tasks."

User reviews results. Confirms or flags concerns.

**Belief transitions:**
- *"My workspace is now in Yherda without loss"* — introduced as `active` on confirmation; `strained` if gaps are concerning (agent clarifies; beat may iterate)
- *"The local vault and Yherda are in sync"* — introduced as `active`

---

## Beat 6l — Dissolve
*Active identity: [[../identities/installer]]*

> "Your workspace is now in Yherda. The local vault remains your lossless source. Yherda is the live version for collaboration, community features, and skill generation at scale.
>
> Bootstrap complete. Clearing bootstrap context. Loading your workspace from Yherda."

Bootstrap context clears. Load the migrated storyline as prime context.

**Belief transitions:**
- *"The bootstrap is complete"* — introduced as `active`

---

## Beat 6m — Begin
*Active identity: [[../../user/identities/yherder]]*

The user's first act in their live workspace.

**Belief transitions:**
- *"I am working within a belief architecture that will compound over time"* — introduced as `emerging` — this belief earns its `active` status through use, not through the bootstrap
