---
name: meeting-notes
description: Turn rough notes into a clean meeting record and prepare its action items for debrief. Use right after a meeting. Triggers on "meeting notes", "clean up these notes", "structure this meeting", and "make a meeting note".
---

# Meeting Notes

Turn rough notes into one clean, findable record without losing signal. This skill creates the record. Debrief files the decisions, tasks, and waiting-for items afterward.

**Done when:** the cleaned note is filed at its approved destination, and the extracted action items are listed for debrief.

## Detect the structure first

Inspect the current folder before planning any write.

1. **Company mode:** use this when `operating-system/` exists with `operating-system/GLOBAL_TASKS.md`.
2. **Personal mode:** use this when root-level `TASKS.md` exists with a personal root or area `CLAUDE.md`.
3. **Both detected:** ask which mode to use. Write nothing until the user chooses.
4. **Neither detected:** say that this folder does not contain a recognised personal or company structure. Point the user to [START-HERE](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/START-HERE.md). Write nothing.

Do not create a structure just to make the skill run.

## Build the record

Read the raw notes fully. If the meeting's date, title, or area is unclear, ask. Preserve the raw notes and then structure:

- date, area, attendees, and meeting type
- a two or three line summary of what happened
- decisions made
- the user's tasks
- things waiting on other people
- follow-up drafts
- durable facts worth reviewing for the brain

Do not invent a decision or task. If something was discussed but not decided, label it as discussed. Flag legal, financial, HR, and other sensitive content before proposing a write. Draft follow-ups, never send them.

## Route the note

- **Personal mode:** create `meetings/YYYY-MM-DD-title.md`.
- **Company mode:** create `operating-system/meetings/YYYY-MM-DD-title.md` using the shape in `operating-system/templates/MEETING_NOTE.md`.

Use a short lowercase filename with hyphens for the title. Never overwrite an existing note. If the target exists, propose a distinct filename or ask the user.

## Approval gate

Show the complete cleaned note and its exact destination before writing. Wait for approval. Write only the approved note. Then list the extracted action items and offer to run debrief. Do not run debrief or change any other file without a separate request and approval.

## Scaling to per-project folders

Company mode deliberately uses one top-level `operating-system/meetings/` folder. If the meeting volume later becomes hard to scan, split notes into project folders and update this routing rule after the shared workflow has proved useful.
