---
tags: [arc, bootstrap, user]
---

# Arc 2 — Work Management Setup

**Owner:** User / Coordinator — [[../../../../belief-systems/retro#the-arc-owner-leads]]
**Want:** A wired place to store and track work
**Need:** The agent knows where tasks live and can read and write them reliably

---

## Beat 2a — Ask
*Active identity: [[../../agent/identities/installer]]*

> "How do you currently track work? Jira, Notion, Linear, a spreadsheet, nothing yet — whatever it is, tell me."

**Belief transitions:**
- *"The user's task store is known"* — introduced as `emerging` (question posed; answer pending)

---

## Beat 2b — Describe Current System
*Active identity: [[../identities/coordinator]]*

User describes their task management reality — tool, habit, or absence.

**Belief transitions:**
- *"My task tracking system is understood by the agent"* — introduced as `emerging`
- *"My current task system is sufficient for agent-assisted work"* — introduced at status reflecting their confidence: `active` if they're happy with it, `strained` if they know it's inadequate, not introduced if they have nothing yet

---

## Beat 2c — Wire
*Active identity: [[../../agent/identities/installer]]*

Based on their answer:

**If Jira with MCP:** Confirm workspace and project key. Store belief. Task store wired.
**If Jira without MCP / other tool:** Store belief with access = manual. Log task: "Wire {tool} integration." Use tasks.md as interim.
**If nothing:** Create `story/tasks.md`. Store belief: task store = tasks.md.

**Belief transitions:**
- *"The user's task store is known"* — `emerging → active`
- *"The agent can write tasks on the user's behalf"* — introduced as `active` if MCP wired; `strained` if manual fallback only

---

## Beat 2d — Receive Wiring Summary
*Active identity: [[../identities/coordinator]]*

> "Your task store is {tool/tasks.md}. I can {read/write directly / log tasks for you to action}. Any setup I couldn't complete is already in your task store."

**Belief transitions:**
- *"My task tracking system is understood by the agent"* — `emerging → active`
- *"My current task system is sufficient for agent-assisted work"* — `strained → active` if the fallback or wiring satisfies them; remains `strained` if they want the real integration first (log task; arc closes with strained belief noted)
