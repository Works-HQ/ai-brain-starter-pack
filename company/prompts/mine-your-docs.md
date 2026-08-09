# Prompt: Mine your docs into a brain

This is the prompt that seeds your brain from a folder of real documents. You do not start from a blank template. You start from what you already have, and your AI refines it into clean files. Your originals stay untouched.

## Before you run it

1. Make one root folder for your world. Point your AI agent at it so it can read and write the files directly.
2. Drop your existing documents into `brain/_source-docs/`: decks, reports, old strategy notes, exports, transcripts, anything relevant. Do not organise it. This is your raw material.
3. Make sure your `CLAUDE.md` (and `AGENTS.md`) are in place, even half-filled.

## The prompt

Paste this into your AI, fill the `<brackets>`, send.

```text
I want you to build a brain out of the documents I have dumped in brain/_source-docs/. Read my CLAUDE.md first so you know who I am, then do this:

1. Inventory brain/_source-docs/. Group what you find by business and by person. Do not deep-read every file. Group from filenames and a light look inside. Tell me the businesses and people you can see in the dump.

2. Refine the signal into clean files:
   - one brain/Company.md per business (use the template if it exists)
   - one brain/People/<name>.md per key person (use the person template)
   Each fact in plain English, citing which source file it came from. Mark anything you are unsure about with [confirm].

3. Build one or two businesses properly, not all of them. Depth on what matters now beats breadth across everything. Ask me which one or two to start with if it is not obvious.

Rules:
- Never edit or delete anything in brain/_source-docs/. Read only. Your output is the clean files, the dump stays as reference.
- Do not overwrite an existing brain file. If one exists, leave it and tell me.
- Summarise, do not paste raw. A brain is refined signal, not a copy of the dump.
- Show me what you are about to write before you write it.
```

## After you run it

Ask your brain a real question, like "based on `brain/Company.md`, what should I be on top of this week?" If the answer is thin, that is the brain telling you what to add. That feedback loop, ask, spot the gap, add it, is how the brain compounds.
