# Prompt 3: Install the skills

This pack ships five ready-made skills: `debrief`, `reflect`, `morning-sweep`,
`weekly-update`, and `meeting-notes`. Each skill lives in its own folder:

```text
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

Each `SKILL.md` starts with YAML frontmatter containing its `name` and
`description`. The description tells your agent when to use the skill.

## Install

Copy the whole `skills/` folder from this pack into the root of your deployed
folder. Keep every skill in its subfolder instead of flattening the files. The
result should look like `myfolder/skills/debrief/SKILL.md`.

Start by asking your agent:

```text
Read skills/debrief/SKILL.md and skills/reflect/SKILL.md. Confirm that you can
use them in personal mode. Do not write anything yet.
```

## Trigger

Ask for the workflow in plain language, such as `debrief this` or `reflect on
this`. Your agent matches the request to the skill's frontmatter description.
In Claude Code-style interfaces that support slash invocation, you can also use
`/debrief`, `/reflect`, or the matching `/<name>` command.

Run `reflect` first to catch corrections, then run `debrief` to file the
outcomes.
