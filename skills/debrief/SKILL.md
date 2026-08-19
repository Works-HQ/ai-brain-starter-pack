---
name: debrief
description: Turn meeting or work-session notes into filed history, decisions, tasks, waiting-for items, and follow-up drafts. Use after any session worth capturing. Triggers on "debrief", "debrief this", "process these notes", and "file this meeting".
---

# Debrief

Turn rough notes into filed action without losing the story.

**Done when:** every decision, task, and waiting item from the session has a filed home, and a dated entry exists in history.

## Detect the structure first

Inspect the current folder before planning any write.

1. **Company mode:** use this when `operating-system/` exists with `operating-system/GLOBAL_TASKS.md`.
2. **Personal mode:** use this when root-level `TASKS.md` and `debrief-history.log` exist.
3. **Both detected:** ask which mode to use. Write nothing until the user chooses.
4. **Neither detected:** say that this folder does not contain a recognised personal or company structure. Point the user to [START-HERE](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/START-HERE.md). Write nothing.

Do not create a structure just to make the skill run.

## Extract the signal

Read the source notes fully. Pull out:

- a two or three line summary
- decisions and their reasoning
- the user's open tasks
- things waiting on other people
- follow-up drafts
- durable facts or changed current state

Do not invent a decision or task. If something was discussed but not decided, label it as discussed. Flag legal, financial, HR, and other sensitive material before proposing a write.

## Route in personal mode

Personal mode has three homes:

- Append the dated session narrative, including decisions and reasoning, to `debrief-history.log`.
- Add new open tasks to root `TASKS.md`. Remove or check completed tasks instead of keeping stale open items.
- Update an existing root or area `CLAUDE.md` only when current state or a durable fact changed. Replace the relevant current-state lines in place. Never append history there.

History is append-only in `debrief-history.log`. Check for duplicate tasks before adding one.

## Route in company mode

Use the top-level operating system, not project folders:

- summary and filing record: `operating-system/DEBRIEF_LOG.md`
- decisions: `operating-system/DECISIONS.md`
- open tasks: `operating-system/GLOBAL_TASKS.md`
- waiting on others: `operating-system/WAITING_FOR.md`

If one of these files is missing and its template exists in `operating-system/templates/`, include creation from that template in the plan. Never replace an existing file. List durable brain facts as a separate proposed update to the relevant `brain/` file and require separate approval before changing it.

Do not create another meeting-note file when the supplied source is already a note file. Draft follow-ups in the response. Never send them.

## Approval gate

Before writing, show:

- every file you plan to touch
- the exact kind of change for each file
- any sensitive or uncertain item that needs a decision
- any follow-up as a clearly labelled draft

Wait for approval. Write only the approved changes. If approval excludes a file or item, do not write it elsewhere. After writing, report what changed and what remains unresolved.

## Scaling to per-project folders

Company mode deliberately uses one top-level set of operating-system files. If the system later becomes too busy, you can create project folders with their own `DECISIONS.md`, `WAITING_FOR.md`, and meeting files, then change this routing rule. Make that change only after the top-level workflow has proved useful.
