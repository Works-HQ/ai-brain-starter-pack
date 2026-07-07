---
name: reflect
description: >
  Make the system smarter by capturing how you want to work, not what was decided.
  Run it when you have corrected the assistant or felt friction. Trigger by saying
  "reflect". The motto is "correct once, never again".
---

# Reflect

Where `debrief` captures *what happened*, this captures *how to work better*. It
turns your corrections and preferences into durable instructions, so you do not
have to give the same note twice.

## When to run

- At the end of a session where you corrected the assistant or had to redirect it.
- Any time you say "reflect".
- The assistant should also **suggest** it when you have corrected the same thing
  twice or seemed frustrated.

## Steps

### 1. Scan the session
Look for:
- **Direct corrections** ("no, do it this way", "actually...", "that's not right")
- **Style or tone preferences** ("shorter", "more direct", "no jargon")
- **Process preferences** ("always do X before Y", "never assume Z", "check A first")
- **Repeats** anything you had to explain more than once

### 2. Sort by confidence
| Tier | Signal | Action |
|------|--------|--------|
| HIGH | A direct correction or explicit instruction | Must capture |
| MEDIUM | An implied or repeated preference | Should capture |
| LOW | A loose observation | Note only, don't persist yet |

### 3. Propose, don't save
Show the findings and ask which to keep. Never write silently.
```
## Reflect: session learnings

HIGH
1. [correction] -> proposed: add to [file]
2. [preference] -> proposed: add to [file]

MEDIUM
3. [pattern] -> proposed: add to [file]

Which should I persist? (numbers, "all", or "none")
```

### 4. Persist what's approved
- A **global** preference about how you work, your voice, or formatting ->
  `about-me.md`.
- A rule specific to **one company or area** -> that area's `CLAUDE.md`.

Prefer updating an existing line over adding a new one. Be specific: "use
contractions, short sentences, no jargon" beats "be more casual".

### 5. Confirm
One line: "Now smarter about: [the thing]."

## Rules

- **Always ask before persisting.** Never silently edit instruction files.
- **Read before writing.** Check existing content so you update rather than duplicate.
- **Be specific.** A vague preference is a weak one. Capture the concrete version.
- **Stay in your lane.** Decisions, tasks, and status belong to `debrief`.
  Corrections, preferences, and patterns belong here. Don't double up.
- **Compound, don't accumulate.** Each reflection should make the system better at
  one specific thing, not add noise.

## Run order

Run `reflect` **first** (catch the corrections while they are fresh), then
`debrief` (file the outcomes). Together they are the loop that makes the system
compound: state stays current, and the assistant keeps getting better at working
the way you want.
