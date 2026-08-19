# Glossary

Plain definitions for the terms used in this starter pack.

**AI brain**

The slow-changing, refined context an AI agent reads so it does not start cold. It contains useful facts about you, a company, and the people involved. It is made of files you own, not hidden chat memory.

**rented harness**

The runtime that reads your files: Claude Code, Codex, Gemini, or whatever comes next. You rent it, and it will keep changing. The brain, the skills, and the loops you build on top are yours. They are plain files, they move with you if you switch tools, and they are the part that compounds. Tool choice sits outside this method for exactly that reason.

**operating system**

The fast-changing file layer that runs current work. It holds current context, open tasks, decisions, waiting items, debriefs, meeting notes, reflections, and weekly updates. It is a working method, not software or a separate product.

**about-me.md**

Your standing personal context: who you are, what you work on, how you make decisions, how you sound, and what you want help with. Keep it short enough to trust and maintain.

**CLAUDE.md**

A context file Claude Code reads automatically. In the personal level, an area `CLAUDE.md` holds durable facts and current state. In the company level, the root `CLAUDE.md` maps the whole deployed system and its rules.

**AGENTS.md**

The Codex equivalent of the company root context file. The company package ships `CLAUDE.md` and `AGENTS.md` with identical content so either tool receives the same instructions.

**brain**

The durable company context under `brain/`. `brain/Company.md` explains the business. `brain/People/` holds short files about important working relationships. Raw source documents are kept separately in `brain/_source-docs/`.

**current state**

The truthful snapshot of what is happening now: status, last contact, next action, priorities, and open threads. It gets overwritten in place when reality changes.

**the three homes**

The personal routing rule: current state goes to an area context file, history appends to `debrief-history.log`, and open tasks live in `TASKS.md`. Each item gets one home.

**slow context**

Information that changes rarely, such as what a company does, a person's role, or your working preferences. It belongs in the brain or standing context.

**fast context**

Information that changes often, such as this week's priorities, open tasks, waiting items, and current status. It belongs in the operating layer.

**mine-your-docs**

The company setup workflow that reads copies of existing documents, inventories what they contain, and drafts refined company and People files. It cites source filenames, marks uncertain facts with `[confirm]`, and never edits the source documents.

**dual-mode skill**

A shared skill that detects whether the deployed folder uses the personal structure or the company structure, then routes its work accordingly. If it detects neither, it writes nothing and points back to setup.

**skill**

A saved workflow for a repeated task. Each skill in this pack lives at `skills/<name>/SKILL.md` and states when it should run, what it reads, what it may write, and where approval is required.

**done when (eval)**

The single line on a skill that states the observable, checkable outcome that means the skill worked. A skill without one runs forever, burns effort on every call, and cannot be handed to someone else to check. Every `SKILL.md` in this pack carries one.

**debrief**

The skill that captures what happened and files decisions, tasks, state changes, waiting items, and history into their proper homes. It shows proposed writes and waits for approval.

**reflect**

The skill that captures how the system should improve. It handles immediate correction-capture and the weekly system review. It proposes findings, then saves only what you select.

**loop**

A workflow that holds a target, checks current state against it, works the gap, and keeps what it learns somewhere the next run will read. Debrief and reflect are loops. A workflow that only repeats on a schedule and remembers nothing is not a loop, it is a timer.

**Loop Register**

A one-page file listing every loop in the system: its target, cadence, memory location, owner, and done-when line. Template at `company/operating-system/templates/LOOP_REGISTER.md`. A loop with no real target gets removed from the register, not left aspirational.

**morning sweep**

A read-and-summarise skill that turns current context, tasks, and waiting items into a short plan for the day. Its default run changes no files.

**weekly update**

A compact, dated view of progress, open loops, risks, decisions needed, follow-ups, and the next action. In company mode the skill adds the approved update to the rolling operating file.

**debrief-history.log**

The append-only personal history of meaningful work sessions. Old entries stay unchanged. It stores the dated story so current-state files remain lean.

**source documents**

Copies of real material used to seed a company brain. They live in `brain/_source-docs/`, remain read-only, and are not treated as refined context during normal work.

**30-minute test**

The rule that a newcomer should get the personal level to its first useful operation within 30 minutes. The system passes when standing context exists, the three homes work, the skills can route correctly, and one real debrief has been filed. If it takes longer, simplify the setup.
