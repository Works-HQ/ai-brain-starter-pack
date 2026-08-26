# One shared brain for Claude and Codex

Claude can be the runtime you use today and Codex another seat you use tomorrow. The durable asset is neither interface. It is one owned folder containing your context, memory, tasks, history, and repeatable skills.

Both tools should read and update that same folder.

## The architecture

```text
Claude Code                    Codex
reads CLAUDE.md                reads AGENTS.md
       \                         /
        \                       /
         one owned AI Brain folder
           about-me.md
           working-preferences.md
           current-context.md
           TASKS.md
           debrief-history.log
           memory/
           skills/
```

The two instruction entry files are maps into the same system. They are not two copies of the brain.

## Recommended layout

```text
AI Brain/
  CLAUDE.md
  AGENTS.md -> CLAUDE.md
  about-me.md
  working-preferences.md
  current-context.md
  TASKS.md
  debrief-history.log
  memory/
    MEMORY.md
    people/
    companies/
    decisions/
    patterns/
    _source-docs/
  skills/
    debrief/
      SKILL.md
    reflect/
      SKILL.md
```

Start smaller if you are following the personal quickstart. The important rule is that every runtime reaches the same authoritative files.

## Join the entry files

Make `CLAUDE.md` the canonical root instruction file.

Where relative symlinks work:

```sh
ln -s CLAUDE.md AGENTS.md
```

If symlinks are unsuitable, create `AGENTS.md` as a generated copy of `CLAUDE.md` and check that the two files still match whenever instructions change. Never maintain two hand-edited instruction files.

If you use another file-capable runtime, give it the entry filename it expects and route that file into the same brain. Do not clone the memory, tasks, history, or skills per tool.

## Keep visible files canonical

Some tools maintain hidden auto-memory or private caches. Those can be useful, but they are runtime-specific. They may point to or summarise the shared files; they should not become the only place where important knowledge lives.

Use one home for each kind of information:

- `about-me.md` for durable personal and professional context
- `working-preferences.md` for voice, decision style, and collaboration rules
- `current-context.md` for current state, updated in place
- `debrief-history.log` for dated events, appended rather than rewritten
- `TASKS.md` for open actions only
- `memory/` for atomic, sourced durable knowledge
- `skills/` for workflows that have already worked manually

## Prove that it works

1. Start a fresh Claude session in the brain root.
2. Ask it to describe who you are, what matters now, and what work is open. Check the answer against the files.
3. Start a fresh Codex session in the same root and ask the same questions.
4. Approve one small memory or current-state update through Claude.
5. Confirm that Codex can see the approved change from the shared files.
6. Approve one change through Codex and confirm that Claude can see it.

The setup is complete when both runtimes return the same current truth from the same files. If they disagree, fix the routing or remove a duplicate source before adding more automation.

## Agent-ready setup brief

Give the following brief to the file-capable agent you already use. It must inspect and propose before it writes.

```text
Build one portable, file-based AI brain that Claude and Codex can both read and update.

Outcome
- One owned root folder contains the canonical context, memory, tasks, history, and skills.
- Claude reads CLAUDE.md.
- Codex reads AGENTS.md.
- Both entry files route to the same visible files.
- Hidden tool memory is never the only copy of important knowledge.

First rule: inspect before writing.

1. Check this machine for existing Claude and Codex instructions, project roots, memory files, task files, and skill catalogues.
2. Confirm the active instruction filenames and skill paths from local support files or official product documentation.
3. Do not print secrets, tokens, private messages, or full hidden-memory contents.
4. Present a short inventory and the exact proposed file changes.
5. Wait for approval before creating, moving, merging, or changing files.

Use this target shape unless an existing system requires a careful merge:

AI Brain/
  CLAUDE.md
  AGENTS.md -> CLAUDE.md
  about-me.md
  working-preferences.md
  current-context.md
  TASKS.md
  debrief-history.log
  memory/
    MEMORY.md
    people/
    companies/
    decisions/
    patterns/
    _source-docs/
  skills/
    debrief/SKILL.md
    reflect/SKILL.md

Make CLAUDE.md canonical. Prefer a relative symlink for AGENTS.md where supported. Otherwise create a generated identical mirror and a drift check. Never maintain two hand-edited instruction files.

Preserve every existing instruction, memory, task, and skill file unless the owner explicitly approves a merge or replacement. Keep credentials out of the brain.

After approved installation, prove the system with two fresh sessions. Claude and Codex must return the same current priorities and open work from the same files. Make one approved update through each runtime and verify the other can read it.
```

## The rule to remember

The model, harness, and interface will change. Your brain should not have to start again when they do.
