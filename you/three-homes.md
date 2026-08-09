# The three homes

Fast-moving information needs three homes. One for current state, one for history and one for open tasks. When each fact has one clear destination, you and your AI can tell what is true now, what happened before and what still needs action.

## Home 1: current state

Current state lives in the root context file for the relevant company or area. In this pack that file is usually `CLAUDE.md`. The same content can live in `AGENTS.md` or `GEMINI.md` if your tool uses a different filename.

Keep one `Current State` block with the latest status, last meaningful contact, next action and open threads. When reality changes, overwrite that block in place. Do not add a second dated block beneath it.

There is only one current state. The file should answer "where does this stand now?" without making you read its history.

Use [company-CLAUDE.md](templates/company-CLAUDE.md) as the starting shape.

## Home 2: history

History lives in `debrief-history.log`. It is append-only.

Each meaningful session or event gets a dated entry with what happened, what changed and what was decided. Add new entries consistently at the top or bottom. Do not rewrite old entries to match the current story. They are the record of what was known and done at the time.

History explains how you arrived at the current state. It does not compete with the current state. When you need today's answer, read the context file. When you need the sequence behind that answer, read the log.

The filled example at [debrief-history.log](examples/debrief-history.log) shows the format.

## Home 3: open tasks

Open tasks live in `TASKS.md`. The file contains open items only.

Group tasks by company or area. Write each item as a concrete action. When the action is complete, remove it. The completed work already belongs in the history log if it matters.

Keeping old checkmarks feels harmless, but it turns the task list into another archive. Then both you and the AI have to scan past finished work to find what remains. The task list has one job: show what still needs action.

Start from [TASKS.md](templates/TASKS.md).

## Worked example: Northwind Coffee

Northwind Coffee meets with a packaging supplier. During the meeting, the supplier confirms that the new compostable bags can arrive in time for the spring release. Northwind chooses the smaller trial run. The production lead needs to send final artwork on Thursday.

The same meeting produces three different writes.

### Update the current state

In `Northwind Coffee/CLAUDE.md`, replace the existing `Current State` block with the latest snapshot:

```markdown
## Current State
- **Status:** Compostable packaging trial confirmed for the spring release.
- **Last contact:** 10 August, supplier confirmed the production window.
- **Next action:** Send final bag artwork on Thursday.
- **Open threads:** Confirm the delivery booking after artwork approval.
```

The previous state disappears from this block. That is intentional. The file now shows the truth as of today.

### Append the history

In `debrief-history.log`, add the event without changing earlier entries:

```text
10 August, Northwind Coffee: packaging trial confirmed
- Supplier confirmed compostable bags can arrive for the spring release.
- Decided to use the smaller trial run.
- Final artwork is due Thursday.
```

This is the dated record. It stays even after the packaging arrives and the current state moves on.

### Add the open task

In `TASKS.md`, add only the action that remains open:

```markdown
## Northwind Coffee
- [ ] Send final bag artwork to the packaging supplier by Thursday.
```

When the artwork is sent, remove the task. The history entry still records why it existed.

## File by meaning, not by source

One meeting can update all three homes because each home answers a different question:

- Current state: where does this stand now?
- History: what happened and what did we decide?
- Tasks: what still needs action?

Do not copy the full meeting note into all three files. Extract the useful part for each home. Overwrite current state. Append history. Keep tasks open-only. That small discipline keeps the system readable long after the first week.
