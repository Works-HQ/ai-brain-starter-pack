# Prompt 3: Install the skills

The two skills, `debrief` and `reflect`, are what turn a folder structure into a
system that runs. They are already written for you in the `skills/` folder of this
pack. You have two ways to install them.

## Option A (recommended): copy the ready-made files

Copy `skills/debrief.md` and `skills/reflect.md` from this pack into a `Skills/`
folder inside your project. Done. In Cowork you trigger them by saying "debrief
this" or "reflect on this". (There is no slash command in Cowork, the skill's
description is what makes Claude reach for it at the right moment.)

That is the whole install. The rest of this file is only if you want Claude to
build them fresh so you understand or customise them.

## Option B: have Claude build them from scratch

Paste this in. It creates both skills tailored to your structure:

```text
Create two skills for me in this project: a debrief skill and a reflect skill.
Save each as its own markdown file in a Skills/ folder (Skills/debrief.md and
Skills/reflect.md). Start each file with a one-line description of what it does and
when to use it, then the full instructions.

Both skills work on my simple structure: an about-me.md for who I am, a CLAUDE.md
per company/area holding that thing's durable facts plus a Current State block,
TASKS.md for open tasks, and debrief-history.log for session history.

=== Skill 1: debrief ===
Purpose: at the end of a work session, capture what happened and file it into the
right home so nothing is lost. I trigger it by saying "debrief" or "debrief this".

Steps:
1. Scan the conversation for: decisions made, status changes, numbers/figures, new
   durable facts, open tasks, and things I'm now waiting on someone for.
2. Decide which files need updating.
3. Show me the plan before writing anything, and wait for my OK.
4. File each kind of information into ONE home only:
   - Full dated session narrative -> append to debrief-history.log. This is the
     ONLY place history lives. Each entry: a dated headline line, then a few bullets.
   - Current state of a company/area (status, last contact, next action, open
     threads) -> overwrite the Current State block in that company's CLAUDE.md in
     place. Do NOT stack a new dated entry under the old one.
   - A durable fact that changed (a person, a price, a rule) -> edit that line in place.
   - Open tasks -> add new ones to the right section of TASKS.md, check off
     completed ones. Open items only, this is not a journal.
5. Show me a short summary of what was captured and where.

State this cardinal rule inside the skill: history is append-only and lives ONLY
in debrief-history.log. Everything else (current state, facts, tasks) is
overwritten in place. Never append a dated session block to a CLAUDE.md or
TASKS.md. That is the rule that keeps these files lean instead of becoming a junk
drawer. Always read a file before writing to it.

=== Skill 2: reflect ===
Purpose: make the system smarter by capturing how I want you to work, not what was
decided. The motto is "correct once, never again". I trigger it by saying
"reflect", and you should also suggest it yourself when I've corrected you twice or
seemed frustrated.

Steps:
1. Scan the session for: direct corrections, style or tone preferences, process
   preferences, and anything I had to explain more than once.
2. Sort them: HIGH = a direct correction or explicit instruction (must capture);
   MEDIUM = an implied or repeated preference (should capture); LOW = a loose
   observation (note only).
3. Show me the findings and ask which to persist. Never save silently.
4. On my OK, write each into the right file: a global preference about how I work,
   my voice, or formatting -> my about-me.md; a rule specific to one company/area
   -> that area's CLAUDE.md. Prefer updating an existing line over adding a new one.
5. Confirm in one line what got saved.

Keep the two skills distinct: debrief captures WHAT happened, reflect captures HOW
to work better. Don't double up.

Write both files now, then show me the two descriptions so I know how to trigger them.
```

## The habit that matters

Run **reflect first** (catch corrections while they are fresh), then **debrief**
(file the outcomes). Do that pair at the end of a session and the system compounds
on its own: your state stays current, and Claude keeps getting better at working
the way you want.
