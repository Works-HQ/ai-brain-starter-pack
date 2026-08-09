# Level 1: give your AI a useful memory of you

This is the smallest useful version of the AI Brain Starter Pack. In about 30 minutes, you will create standing context about yourself, give current state, history, and open tasks one home each, install the shared skills, and run one real debrief.

You do not need the rest of the repository to complete this level. This package is `you/` plus `skills/`.

## Before you start

You need:

- a new folder for your deployed system
- an AI agent that can read and write files in that folder
- one real piece of work to debrief, such as meeting notes or a completed work session
- 30 minutes

Claude Code, Codex, and Gemini CLI are examples. The method only needs an agent that can work with local markdown files.

Use copies while you learn. Do not point an agent at the only copy of an important document.

## Quickstart

### 1. Make the deployed folder, 2 minutes

Create a new folder outside this starter package. This is the folder your AI will work in from now on.

Copy these package files into it:

- `about-me.md`
- `templates/TASKS.md`, renamed to `TASKS.md`
- `templates/company-CLAUDE.md`, copied into one area folder and renamed as that folder's `CLAUDE.md`
- the entire sibling `skills/` folder

Create one empty file at the deployed root named `debrief-history.log`.

### 2. Fill your standing context, 8 minutes

Point your AI agent at the deployed folder. Open `prompts/01-about-me.md` from this package and give the prompt to the agent.

Answer only what you know. The agent must ask before it saves the draft. A short, accurate `about-me.md` beats a polished biography.

### 3. Stand up the three homes, 7 minutes

Open `prompts/02-setup-structure.md` and give the prompt to the agent. Ask it to work inside your deployed folder.

Keep the first version small:

- current state lives in one area `CLAUDE.md` and is overwritten in place
- history is appended to `debrief-history.log`
- open tasks live in `TASKS.md`, with completed work removed

Read `three-homes.md` in this package if you want a worked explanation. A finished fictional area file is in `examples/Northwind Coffee/CLAUDE.md`.

### 4. Check the skills, 3 minutes

Confirm the deployed `skills/` folder contains five subfolders, each with a `SKILL.md` file. Start with `debrief` and `reflect`. The other skills can wait until the basic loop works.

Tell your agent: `Read skills/debrief/SKILL.md and skills/reflect/SKILL.md. Confirm that you can use them in personal mode. Do not write anything yet.`

### 5. Run one real debrief, 8 minutes

Put a real meeting note or work note into the deployed folder. Tell the agent: `Run debrief on this note.`

The agent should show its proposed writes and wait for approval. Check that:

- the dated account goes to `debrief-history.log`
- any changed current state updates the relevant `CLAUDE.md` in place
- open tasks go to `TASKS.md`

Approve only the correct changes. Then ask the agent to make them.

### 6. Close the loop, 2 minutes

Tell the agent: `Reflect on this setup session.` Choose any correction or preference worth keeping. The agent should ask before changing `about-me.md` or an area `CLAUDE.md`.

You now have a working personal level.

## The deployed layout this produces

```text
your-folder/
  about-me.md
  TASKS.md
  debrief-history.log
  one-area/
    CLAUDE.md
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

This deployed layout is deliberately smaller than the package you copied from. The package contains prompts, templates, and examples. Your deployed folder contains your real context and working files.

## You know it worked when

- your agent can describe who you are and what you are working on without a fresh explanation
- every current-state update, history entry, and open task has one clear home
- one real debrief has changed the right files, after your approval
- your source note still exists unchanged

If one of those is false, fix the structure before adding more files or automation.

## Keep it alive

Run reflect when you correct the agent or during a weekly review. Run debrief after meaningful work. That is enough to keep the first level current.

When this works for you and you need shared company memory, add the standalone company package as a separate next step.

Optional reading: [the one idea](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/theory/01-the-one-idea.md) and [the 30-minute test](https://github.com/Works-HQ/ai-brain-starter-pack/blob/main/theory/07-the-30-minute-test.md).
