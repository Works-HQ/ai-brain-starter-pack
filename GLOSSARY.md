# Glossary

Plain definitions for the terms you will hit while setting up your AI operating system. Where a term touches Cowork's exact features or limits, those can change, so treat the definition as the concept and check Anthropic's current docs for live specifics.

---

**Cowork**
Claude with a desk. Instead of just a chat, the assistant gets a folder it can read and write, and the work persists there as files across sessions. The folder is the project.

**Claude Code**
Anthropic's command-line version of Claude that works directly with files and tools on your machine. You do not need it for this setup. It matters here only because the same skill files (the ones with frontmatter) work in both Claude Code and Cowork.

**Project (Claude.ai)**
A chat on Claude.ai with reference documents attached. The assistant reads those docs but does not change them, and the thinking lives in the conversation rather than in persisted files. This is the thing Cowork builds past.

**CLAUDE.md**
The standing context file for one company or area: what it is, who is involved, and a "Current State" block for what is happening now. The exact filename is a convention the assistant looks for, so keep it as written.

**about-me.md**
Your own standing context, read on every run: who you are, how you work, what matters to you. It is a file you own that the assistant reads and updates over time, so it gets to know you instead of starting cold each session.

**skill**
A saved set of instructions for a task you do repeatedly, so you do not have to re-explain it each time. In Cowork you trigger a skill by asking in plain language. The starter kit includes two: debrief and reflect.

**connector / MCP**
A connector links Claude to an outside tool or account (for example email, calendar, or a drive) so it can work with your real information, not just talk about it. MCP (Model Context Protocol) is the underlying standard that makes those connections possible. Which connectors exist, what they can do, and how to set them up changes over time, so check Anthropic's current docs rather than assuming.

**the three homes**
The three places anything from a session goes, kept strictly separate: current state into a `CLAUDE.md` "Current State" block, history into `debrief-history.log`, and open tasks into `TASKS.md`. Keeping reference and live state apart is what keeps the system readable.

**current state**
The snapshot of what is happening right now in an area, kept in that area's `CLAUDE.md` "Current State" block. It is overwritten in place, so it always reflects now rather than accumulating old updates.

**slow vs fast context**
Two speeds of information. Slow context is what things are (the durable facts that rarely change). Fast context is what is happening now (the live, frequently changing stuff). The system keeps them in different files on purpose so the fast stuff does not bury the slow stuff.

**debrief**
The skill that captures what happened in a session and files it into the three homes: current state to `CLAUDE.md`, history to the log, tasks to `TASKS.md`. It never stacks dated blocks onto `CLAUDE.md` or `TASKS.md`; history goes to the log.

**reflect**
The skill that captures corrections and preferences, the "correct once, never again" learnings about how you want things done. It always asks before changing anything. Run reflect first, then debrief.

**frontmatter**
A small block of settings at the top of a skill file (name, description, and similar). It is what lets the same skill file be recognised and triggered in Claude Code as well as Cowork.

**TASKS.md**
The file that holds your open tasks, and only open tasks. Debrief adds new ones and closes finished ones here. It is not a log of everything ever done; that history belongs in `debrief-history.log`.

**debrief-history.log**
The append-only record of what has happened over time. New entries go on the bottom and old ones are never edited. This is where session history lives so your `CLAUDE.md` files stay lean.
