---
name: morning-sweep
description: Build today's brief from current context, tasks, waiting-for items, and any connected calendar or inbox. Use first thing each morning. Triggers on "morning sweep", "what's important today", and "build my day".
---

# Morning Sweep

Read what matters and return a one-screen plan for today. The default is read-and-summarise with zero file writes.

**Done when:** the user has a one-screen brief covering today's shape, top 3, calendar, replies needed, overdue items, and parked work.

## Detect the structure first

Inspect the current folder before reading or planning.

1. **Company mode:** use this when `operating-system/` exists with `operating-system/GLOBAL_TASKS.md`.
2. **Personal mode:** use this when root-level `TASKS.md` exists with a personal root or area `CLAUDE.md`.
3. **Both detected:** ask which mode to use. Write nothing until the user chooses.
4. **Neither detected:** say that this folder does not contain a recognised personal or company structure. Point the user to [START-HERE](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/START-HERE.md). Write nothing.

## Read the available signals

### Personal mode

Read root `TASKS.md` and the current-state blocks in relevant `CLAUDE.md` files. Use `debrief-history.log` only when recent history is needed to understand an open item.

### Company mode

Read these top-level files when present:

- `operating-system/GLOBAL_TASKS.md`
- `operating-system/WAITING_FOR.md`
- `operating-system/current-context.md`
- `operating-system/DECISIONS.md` when a pending decision affects today

If a calendar or inbox is connected and the user has allowed access, include today's meetings and replies. If either source is unavailable, say so. Never claim to have read a source you could not access.

## Build the brief

Choose the top three priorities based on due dates, work blocking other people, and work that moves the most important outcome. Respect anything the user explicitly parked.

Return:

- Today's shape
- Top 3
- Calendar with preparation flags
- Needs a reply today
- Overdue to chase
- Parked

Keep it to one screen. Never send a message, email, or post.

## Write behavior

The default morning sweep writes nothing. Do not update tasks, context, or waiting-for files while summarising.

Only offer a persistent file if the user explicitly asks to save the sweep. In personal mode the target is root `DAILY_SWEEP.md`. In company mode the target is `operating-system/DAILY_SWEEP.md`. Show that one-file plan and wait for approval before writing. Overwrite only the previous daily sweep, never another file.

## Scaling to per-project folders

Company mode deliberately reads the top-level operating system. If the volume later demands project folders, the sweep can read their task and waiting-for files too, but the final plan should still be one cross-company view.
