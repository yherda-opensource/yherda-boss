# Yherda Boss

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

A belief-driven AI workspace bootstrap. Sets up your working model locally with Claude — ceremonies, roles, team agreements, and skills — with a migration path to Yherda when you're ready to collaborate.

---

## Agent entry point

`bootstrap-prompts/bootstrap.md`

Tell your agent: **"Read the README and follow the agent entry point."**

That's it. The bootstrap handles everything from there.

---

## What this does

Yherda Boss walks you through a structured setup conversation with Claude. By the end you have:

- A working model of how you operate — roles, beliefs, ceremonies, team agreements
- A set of skills Claude can invoke to support your workflow
- A cadence for standup, planning, grooming, review, and retro
- A migration path to Yherda when you're ready to collaborate with others

The vault works as-is for solo operation. Yherda adds value when you have a team.

---

## What you need

- Claude (claude.ai or Claude Code)
- This repo cloned locally
- Optionally: Obsidian for browsing the belief systems

---

## Structure

```
belief-systems/
  yherda/        ← platform and expression belief systems
  agile/         ← agile beliefs and process arc templates
  retro.md       ← working retro log; starts blank
bootstrap-prompts/
  bootstrap.md   ← agent entry point
  story/         ← bootstrap arc story; characters, identities, arcs, beats
```

---

## Community

Discussions are open. If you find a belief that doesn't hold, a process that needs a beat, or a pattern worth sharing — that's what the discussion board is for.

Belief systems and process templates are community-maintained. Extensions developed in your workspace can be contributed back via PR once they're stable.
