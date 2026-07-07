---
name: debrief
description: >
  Capture what happened in a working session and file it into the right home so
  nothing is lost. Run it at the end of any session. Trigger by saying "debrief"
  or "debrief this".
---

# Debrief

At the end of a working session, this captures what happened and files each piece
into the one place it belongs, so your system stays current instead of scrolling
away in a chat.

## When to run

- At the end of any real working session or meeting.
- Any time you say "debrief" or "debrief this".

## The three homes (read this first)

Every piece of information has exactly one home. This is the rule that stops the
whole system rotting into a junk drawer:

1. **Current state** (status, last contact, next action, open threads for a
   company or area) lives in that area's `CLAUDE.md`, in a "Current State" block.
   It is **overwritten in place**. You never stack a new dated entry under the old one.
2. **History** (the narrative of what happened, dated) lives in
   `debrief-history.log`. It is **append-only**. This is the only place history lives.
3. **Open tasks** live in `TASKS.md`, grouped by area. **Open items only.** Done
   things come off the list.

Reference (what things *are*) and live state (what's *happening now*) never mix.

## Steps

### 1. Scan the conversation
Pull out everything worth keeping:
- Decisions made, and the why behind them
- Status changes (what moved from one state to another)
- Numbers, figures, dates, deadlines
- New durable facts (a person, a price, a rule, a contact)
- Open tasks created
- Things you are now waiting on someone else for

### 2. Decide which files to update
- Which company/area `CLAUDE.md` files have a changed current state?
- What goes in the history log?
- What tasks change in `TASKS.md`?
If a needed file does not exist yet, plan to create it.

### 3. Show the plan, then wait
Before writing anything, show a short plan: which files you will touch and what
you will add or change in each. Wait for an OK. Do not write first and explain after.

### 4. File each piece into its one home
- **Full dated session narrative** -> append to `debrief-history.log`. Format:
  ```
  > **DD Mon YYYY, [area]: [one-line headline]**
  > - [key point / decision / what shipped]
  > - [key point]
  ```
  This is the only place the narrative goes.
- **Current state of an area** -> overwrite the "Current State" block in that
  area's `CLAUDE.md`. Replace the old lines with the new reality. Do not append a
  dated version under the old one.
- **A durable fact that changed** -> edit that one line in place.
- **Open tasks** -> add new ones to the right section of `TASKS.md`, check off or
  remove completed ones. Open items only.

### 5. Summarise
Show what was captured and where:
```
## Debrief complete

Captured:
- [key points]

Updated:
- [file]: [what changed]
- [file]: [what changed]

Next actions:
- [ ] ...
```

## The cardinal rule

History is append-only and lives only in `debrief-history.log`. Everything else,
current state, facts, tasks, is overwritten in place. **Never append a dated
session block to a `CLAUDE.md` or to `TASKS.md`.** That accretion is exactly what
turns a clean system into an unreadable pile. If a `CLAUDE.md` grows a lot from a
debrief, you are appending history that belongs in the log.

## Gotchas

- **Read before you write, every time.** You may have edited a file by hand
  between sessions. Check what is there before changing it.
- **Don't duplicate tasks.** Check `TASKS.md` for an existing entry before adding
  a new one. Reword a near-duplicate rather than stacking two versions.
- **Don't debrief the debrief.** If the session was just running this skill with
  no prior work, say "nothing to debrief" rather than inventing entries.
- **Dates:** use `DD Mon` (e.g. `22 Jun`), consistently, so the log stays readable.
