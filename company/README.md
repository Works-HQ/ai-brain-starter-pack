# Level 2: build a company brain

This level turns the personal system into shared company memory and a weekly operating rhythm. You will mine real documents into a durable company file, create context for one important person, stand up the operating files, and schedule a weekly review.

Complete the personal level first, or arrive with an equivalent system that already has standing context, clear homes for live work, and a working debrief habit.

You do not need the rest of the repository to complete this level. This package is `company/` plus `skills/`.

## Before you start

You need:

- a new folder for the deployed company system
- an AI agent that can read and write files in that folder
- at least 10 real company documents copied into a safe working folder
- permission to use those documents with your chosen AI tool
- a person who will review every proposed brain fact

Use copies of source documents. The mining workflow treats them as read-only.

## Quickstart

### 1. Copy the company package, 5 minutes

Copy the contents of this `company/` folder into your deployed root. Copy the sibling `skills/` folder into that same root.

Keep both `CLAUDE.md` and `AGENTS.md`. Fill the placeholders in both with the same information and keep the files identical. If you use Gemini CLI, copy CLAUDE.md to GEMINI.md.

### 2. Create the live operating files, 5 minutes

Inside `operating-system/`, copy these templates up one level and remove the placeholder examples you do not need:

- `templates/DEBRIEF_LOG.md` to `DEBRIEF_LOG.md`
- `templates/DECISIONS.md` to `DECISIONS.md`
- `templates/REFLECTION_LOG.md` to `REFLECTION_LOG.md`
- `templates/WAITING_FOR.md` to `WAITING_FOR.md`
- `templates/WEEKLY_UPDATE.md` to `WEEKLY_UPDATE.md`
- `templates/LOOP_REGISTER.md` to `LOOP_REGISTER.md`, prefilled with debrief and reflect

Keep `templates/MEETING_NOTE.md` as the source for future meeting files. Create an empty `operating-system/meetings/` folder when you file the first meeting.

Use `templates/PERSON_CONTEXT.md` as an alternate home for person context scoped to a project rather than the brain.

### 3. Add source documents, 5 minutes

Put copies of at least 10 real documents into `brain/_source-docs/`. Useful inputs include strategy notes, sales decks, product documents, meeting notes, customer research, role descriptions, and recent reports.

Do not organise the dump first. The inventory step does that work without changing your originals.

### 4. Mine the company brain, 10 minutes for the first pass

Open `prompts/mine-your-docs.md` and give it to the agent. Tell it to start with one company and one person.

Review the proposed `brain/Company.md` and `brain/People/<name>.md` carefully. Remove unsupported claims. Keep `[confirm]` beside anything that needs checking. Approve the files only when they match the source documents and your direct knowledge.

The first pass does not need to capture everything. It needs to be trustworthy enough that the agent can answer a real company question without guessing.

### 5. Run the weekly rhythm, 5 minutes

Choose a recurring weekly time and put it in the calendar used by your team. This lives in your calendar, not in these files. The session should cover:

1. Run `morning-sweep` or review `current-context.md` and `GLOBAL_TASKS.md`.
2. Run `weekly-update` and approve the new update.
3. Run the weekly `reflect` review and approve useful changes.
4. Check that decisions, waiting items, and company facts still have one home each.
5. Walk the `LOOP_REGISTER.md`: confirm each loop still has a real target, and update its done-when line if the work has changed.

Manual first, automate later. Run this rhythm by hand twice before scheduling any agent action.

## The deployed layout this produces

```text
company-folder/
  CLAUDE.md
  AGENTS.md
  brain/
    Company.md
    People/
      one-person.md
      _Person-template.md
    _source-docs/
      README.md
      copied-source-files
  operating-system/
    current-context.md
    GLOBAL_TASKS.md
    DEBRIEF_LOG.md
    DECISIONS.md
    REFLECTION_LOG.md
    WAITING_FOR.md
    WEEKLY_UPDATE.md
    LOOP_REGISTER.md
    templates/
      MEETING_NOTE.md
      other-source-templates.md
  prompts/
    mine-your-docs.md
    new-project.md
  skills/
    debrief/
      SKILL.md
    reflect/
      SKILL.md
    morning-sweep/
      SKILL.md
    weekly-update/
      SKILL.md
    meeting-notes/
      SKILL.md
```

The package also includes a fictional example under `examples/`. It shows the expected depth, but it is not part of your deployed system.

## You know it worked when

- `brain/Company.md` contains sourced facts from real documents, not blank prompts or invented claims
- one important person has a useful file in `brain/People/`
- the agent can state the current priority, open tasks, recorded decisions, and waiting items from the right files
- a recurring weekly review is on the calendar
- `LOOP_REGISTER.md` lists debrief and reflect with a real target and a done-when line each
- no source document was edited or deleted

If the company brain cannot pass those checks, keep the workflow manual and correct the files before expanding it.

Optional reading: [from you to your company](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/theory/05-from-you-to-your-company.md) and [the four layers](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/theory/03-the-four-layers.md).
