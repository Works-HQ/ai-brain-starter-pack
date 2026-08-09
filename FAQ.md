# FAQ

Common questions about building and running a file-based AI brain.

## Getting started

### Do I need to be technical?

No. If you can make a folder, copy a file, and review a draft, you can use this method. The files are plain markdown. Your AI agent does the first-pass writing, then you decide what is true and what gets saved.

### What do I build first?

Start with the personal level in [`you/README.md`](you/README.md). Create `about-me.md`, stand up the three homes, install the skills, and run one real debrief. Do not begin with a company-wide structure unless you already have an equivalent personal habit.

### Does the setup really take 30 minutes?

The first personal loop should. At the end of 30 minutes, the system should know enough about you to help, have one home for current state, history, and tasks, and have filed one real debrief. It will not know everything. The 30-minute test measures time to first useful operation, not completeness.

### Which AI tool do I need?

Any agent that can read and write files in a folder. Claude Code, Codex, and Gemini CLI are examples. Product interfaces and feature limits change, but the file structure does not depend on one vendor.

### Why do some packages contain both CLAUDE.md and AGENTS.md?

Different tools look for different context filenames. The company package keeps identical copies for Claude Code and Codex. If you use Gemini CLI, copy `CLAUDE.md` to `GEMINI.md`. Keep the contents aligned.

## The personal level

### What are the three homes?

Every live item from personal work goes to one place:

1. Current state goes into the relevant area `CLAUDE.md` and is overwritten in place.
2. History is appended to `debrief-history.log`.
3. Open tasks live in `TASKS.md`, with completed items removed.

The separation stops a current-state file from becoming a dated archive and stops a task list from becoming a journal.

### What is the difference between debrief and reflect?

Debrief captures what happened: decisions, state changes, tasks, waiting items, and useful history. Reflect captures how the system should work better: a correction, a preference, a recurring failure, or a weekly learning.

Run reflect when you correct the agent and during the weekly review. Run debrief after meaningful work. Both skills show proposed writes and wait for approval.

### What if I forget to debrief for a week?

Run a catch-up debrief using the notes you have. Do not invent missing detail. Mark uncertainty clearly, file open tasks, and reset the current-state file to what is true now.

### Why not keep everything in one big file?

Different information changes at different speeds. Durable facts may stay true for months. Current priorities may change today. A single file mixes those speeds, grows without a routing rule, and becomes hard to trust. A small spine of routed files is easier for you and the agent to maintain.

## The company level

### What is a company brain?

A company brain is the refined, slow-changing context the agent should know about the business and its people. In this pack it lives under `brain/`, mainly in `brain/Company.md` and `brain/People/`. It is not a dump of every document and it is not the live task list.

### What is the company operating system?

The operating system is the fast-changing layer under `operating-system/`. It holds current context, open tasks, debriefs, decisions, waiting items, meeting notes, reflections, and the weekly update. The brain explains what the company is. The operating system shows what is happening now.

### Why mine documents instead of filling a blank company template?

Your existing documents contain more evidence than memory alone. The mine-your-docs workflow inventories copies of those documents, extracts relevant facts, cites their source files, and marks uncertainty with `[confirm]`. You review the draft before anything becomes brain context.

### Which documents should I mine?

Start with at least 10 useful documents from different parts of the company. Strategy notes, product documents, sales material, customer research, role descriptions, recent reports, and meeting notes all help. Use documents you are allowed to process with your chosen tool.

### What should never happen to source documents?

The agent must not edit or delete them. Put copies in `brain/_source-docs/`, treat that folder as read-only, and write refined context elsewhere. The brain wraps around source material. It does not replace it.

### Why create a People file?

A short People file gives the agent useful context about someone's role, priorities, communication preferences, history, and open commitments. It improves drafts and meeting preparation without forcing the agent to search old notes every time. Keep it factual and appropriate to the work.

### What is the weekly rhythm?

Once a week, review current context and global tasks, generate the weekly update, run the weekly reflect review, and check decisions and waiting items. Schedule it on the calendar. Run it manually twice before automating any part.

## Skills and upkeep

### What makes the skills dual-mode?

Each shared skill checks which deployed structure exists. Personal mode routes to the three homes. Company mode routes to the top-level company operating files. If neither structure exists, the skill explains what is missing, points to the setup guide, and writes nothing.

### Can I change the skills?

Yes. Prove the supplied workflow first, then edit it when a repeated need appears. Keep the safety gates: read before writing, show the plan, wait for approval, preserve source material, and use one destination for each kind of information.

### What if the AI writes to the wrong file?

Stop the run and correct the routing rule before continuing. Move the information to its proper home, remove the incorrect copy, then run reflect so the correction becomes part of the system. Do not accept duplicate truth across several files.

### How do I know the system is going stale?

You start correcting facts that the files should already hold. Current context describes last month. Open tasks are already finished. Decisions get reopened without their reasoning. Treat each of those as a maintenance signal and repair the smallest broken file or workflow.
