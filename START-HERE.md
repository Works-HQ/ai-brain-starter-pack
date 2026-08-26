# Start here: build the personal level first

Your first action is to open [you/README.md](you/README.md) and follow its quickstart.

That guide takes you from an empty folder to a useful personal AI system in about 30 minutes. You will create `about-me.md`, stand up the three homes for current state, history, and open tasks, install the skills, and run one real debrief.

Do not start with the company layer. A shared system is much easier to judge once you have used the personal loop on real work.

## The two-level path

### Level 1: you

Go to [you/README.md](you/README.md).

Use this level when you still re-explain who you are, how you work, or where a piece of work stands. It gives the agent a small set of plain files it can read and update with your approval.

You are ready for Level 2 when:

- your `about-me.md` is useful
- current state, history, and open tasks have one home each
- you have run at least one real debrief
- you trust the basic filing loop

### Level 2: your company

Then go to [company/README.md](company/README.md).

Use this level when the problem has moved beyond your own memory. It adds a mined company brain, people context, shared operating files, and a weekly rhythm. It starts from real documents, not a long blank questionnaire.

## The 30-minute promise

The personal level should become useful within 30 minutes. That does not mean complete. It means the agent knows enough about you to help, the three homes exist, the skills can find them, and one real debrief has been filed correctly.

If it takes longer, stop adding structure. Remove steps, shorten files, and get one honest workflow running first.

The company level takes longer because source documents need human review. Its quickstart gives you a trustworthy first pass, then the weekly rhythm improves it through use.

## If you use Claude and Codex

Use one deployed brain, not one copy per tool. [The shared-brain guide](SHARED-BRAIN.md) shows how `CLAUDE.md` and `AGENTS.md` can route both runtimes into the same context, memory, tasks, history, and skills.

## Keep your filled-in brain private

This starter pack is public. Your filled-in brain is not. Once these files hold real names, deals, numbers, and history, they are confidential company records that happen to live in markdown.

Three rules:

- Copy this pack into a fresh private repository or a private folder. Do not fork it on GitHub: forks of public repositories are public.
- Keep credentials out of the files entirely. API keys, passwords, and tokens belong in a secrets manager or a local `.env` file, which this pack's `.gitignore` already excludes. The brain stores facts, never keys.
- Before sharing any single file outside the company, reread it as an outsider would. People files and current-state files hold candid detail by design.

## If you want the reasoning

The setup guides are enough to build the system. The [theory](theory/01-the-one-idea.md) explains why the structure works, the [FAQ](FAQ.md) handles common questions, and the [glossary](GLOSSARY.md) defines the few terms used here.
