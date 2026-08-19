---
name: weekly-update
description: Produce a compact company weekly update from current context, tasks, decisions, waiting-for items, and meeting notes. Use once a week. Triggers on "weekly update", "update the projects", and "run the weekly updates".
---

# Weekly Update

Turn the week's scattered signals into one compact view of progress, open loops, risk, and the next move.

**Done when:** the approved dated section is added to `operating-system/WEEKLY_UPDATE.md` above the previous entries, or the user has a conversational summary in personal mode.

## Detect the structure first

Inspect the current folder before planning any write.

1. **Company mode:** use this when `operating-system/` exists with `operating-system/GLOBAL_TASKS.md`.
2. **Personal mode:** use this when root-level `TASKS.md` and personal context files exist without the company operating system.
3. **Both detected:** ask which mode to use. Write nothing until the user chooses.
4. **Neither detected:** say that this folder does not contain a recognised personal or company structure. Point the user to [START-HERE](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/START-HERE.md). Write nothing.

Do not create a structure just to make the skill run.

## Personal mode

The personal structure does not maintain a weekly-update file. Explain that this workflow belongs to the company level, point the user to [the company setup](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/company/README.md), and write nothing. Offer a conversational summary only if the user wants one.

## Company mode

Read the top-level company signals:

- `operating-system/current-context.md`
- `operating-system/GLOBAL_TASKS.md`
- `operating-system/DECISIONS.md`
- `operating-system/WAITING_FOR.md`
- this week's files in `operating-system/meetings/`
- the previous entry in `operating-system/WEEKLY_UPDATE.md`
- any email or message exports the user explicitly provides

If a source is missing, say so. Do not infer activity from silence.

Draft one dated section with:

- Status: Green, Amber, or Red, with one line explaining why
- Since last week: progress, not activity
- Open loops
- Risks
- Decisions needed and their owners
- Follow-ups
- Suggested next action: the single most important move

Keep it to one screen. Separate facts from inference. Where a source was quiet, say "no meaningful signal this week." Draft only, never send.

## Approval gate

Show the complete proposed section and name `operating-system/WEEKLY_UPDATE.md` as the only target. Wait for approval. On approval, add the new dated section above the previous entries. If the file is missing and `operating-system/templates/WEEKLY_UPDATE.md` exists, propose creating it from that template first. Never replace or discard previous weeks.

After writing, return a short company-level read on the pattern across the work.

## Scaling to per-project folders

Company mode deliberately writes one top-level `operating-system/WEEKLY_UPDATE.md`. If the organisation later needs separate project updates, create a `WEEKLY_UPDATE.md` inside each project and change this routing rule. Keep a short cross-project summary at the top level.
