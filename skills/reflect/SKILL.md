---
name: reflect
description: Capture corrections so they do not recur and run a weekly review of how the system is working. Use after a correction, when the workflow feels wrong, or once a week. Triggers on "reflect", "correct once, never again", "weekly reflection", and "run the weekly reflect review".
---

# Reflect

Improve how the system works, not the work itself. This skill has two explicit triggers: correction-capture and weekly review.

**Done when:** every finding the user selected is written to its target file, and the user has confirmed what the system is now smarter about.

## Detect the structure first

Inspect the current folder before planning any write.

1. **Company mode:** use this when `operating-system/` exists with `operating-system/GLOBAL_TASKS.md`.
2. **Personal mode:** use this when root-level `TASKS.md`, `debrief-history.log`, or `about-me.md` shows the personal structure.
3. **Both detected:** ask which mode to use. Write nothing until the user chooses.
4. **Neither detected:** say that this folder does not contain a recognised personal or company structure. Point the user to [START-HERE](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/START-HERE.md). Write nothing.

Do not create a structure just to make the skill run.

## Trigger A: correction-capture

Use this after the user corrects an assumption, style, fact, or process. The aim is **correct once, never again**.

1. Identify direct corrections, explicit preferences, repeated friction, and weak inferences.
2. Sort them as high confidence, medium confidence, or observation only.
3. Propose a specific durable instruction for each useful finding.
4. Show the numbered findings and their target files. Ask which numbers to persist.
5. Wait. Persist only the selected findings.

## Trigger B: weekly system review

Use this when the user asks for a weekly reflection.

- In personal mode, read `debrief-history.log`, completed or changed work in `TASKS.md`, `about-me.md`, and relevant `CLAUDE.md` files.
- In company mode, read `operating-system/DEBRIEF_LOG.md`, the Done section of `operating-system/GLOBAL_TASKS.md`, the previous entries in `operating-system/REFLECTION_LOG.md`, and `operating-system/current-context.md`.

Assess what worked, what did not, repeated patterns, stalled work, missing context, and concrete changes for the coming week. Show the proposed reflection and every intended write, then ask which findings to persist. Wait for the answer.

## Route approved findings

### Personal mode

- A global preference about voice, format, or working style goes in `about-me.md`.
- A correction or rule specific to one company or area goes in that area's `CLAUDE.md`.
- Prefer editing an existing line over adding another rule.
- A weekly review must result in at least one user-selected, concrete improvement to `about-me.md` or a relevant `CLAUDE.md`. If the user selects none, write nothing.

### Company mode

- Record both correction-capture and weekly-review findings as a dated entry in `operating-system/REFLECTION_LOG.md`.
- Include the correction, the evidence, the proposed durable change, and its target file.
- Do not edit a brain or skill file during this run. Leave approved changes as explicit actions in the reflection log so they can be reviewed separately.

## Approval and quality rules

- Never write before the user selects what to persist.
- Read a target before editing it. Do not duplicate an existing instruction.
- Be specific. "Use short sentences and no jargon" is stronger than "be casual".
- Keep decisions, tasks, and status in debrief. Keep corrections, preferences, and system patterns here.
- Be direct and actionable. Do not pad the reflection with reassurance.

After writing, confirm what the system is now smarter about and name the file changed.

## Scaling to per-project folders

Company mode deliberately keeps one top-level `operating-system/REFLECTION_LOG.md`. If separate teams later need their own review histories, add per-project logs and update this routing rule after the shared weekly review has proved useful.
