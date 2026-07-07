# Start here: your first working system in about 20 minutes

This is the ordered path from an empty folder to a personal operating system that remembers your work. Follow the steps in order. Each one is concrete and points to a real file in this pack.

If you only do one thing, do this: get `about-me.md` and the two skills running. The rest follows naturally once those three are in place.

---

## Step 0: Understand the one idea (5 min, optional but recommended)

Before you build anything, read the three short files in `theory/`. They explain the single shift that makes Cowork different and the rule that keeps the system from rotting.

- `theory/01-the-mental-model.md`: from a chat to an agent with a desk.
- `theory/02-slow-vs-fast-context.md`: the rule that stops the whole thing rotting.
- `theory/03-the-debrief-reflect-loop.md`: the loop that makes it compound.

You can skip this and go straight to building. But five minutes here makes every step after it make sense.

---

## Step 1: Create a folder and point Cowork at it

Make a new folder on your computer. Call it whatever your workspace is (your name, your business, "my-brain", anything). In Cowork, start a project pointed at that folder. That folder is now your desk. Everything Claude reads and writes lives there.

If you already have reference docs (a bio, client notes, a style guide), drop copies into the folder. Claude will read them in the next steps and fold what is useful into your structure.

**Safety note:** drop in *copies*, not your only copy of anything. An agent that can write can also overwrite. While you are learning, keep the originals somewhere else. Build trust first, then graduate to live files.

---

## Step 2: Build your about-me

Open `prompts/01-about-me.md`. Paste the prompt inside it into your Cowork project and answer the questions.

Claude interviews you in small batches and writes an `about-me.md` file at the root of your folder. This is your standing context, the file Claude reads at the start of every session. It is the old Projects "custom instructions" box, except now it is a file you own that Claude reads *and* updates.

When it shows you the draft, check it, then tell it to save. You now have standing context.

(Want to see what a finished one looks like first? Check `templates/about-me.md` for the skeleton and `examples/about-me.md` for a filled-in version.)

---

## Step 3: Set up the structure

Open `prompts/02-setup-structure.md` and paste the prompt in.

This builds the simple operating structure around you. Three homes, nothing more:

- `TASKS.md` at the root, every open task grouped by area, open items only.
- A `CLAUDE.md` for each company or area you work on, holding durable facts plus a "Current State" block.
- `debrief-history.log` at the root, the append-only journal your debrief skill will write to.

Claude reads your `about-me.md` first, then proposes a tree before creating anything. Don't front-load empty folders. You need `about-me.md`, one company `CLAUDE.md`, and `TASKS.md` on day one. Add more as you hit the need.

(Templates live in `templates/`. A worked example of a company file is at `examples/Northwind Coffee/CLAUDE.md`.)

---

## Step 4: Install the two skills

Open `prompts/03-install-skills.md`. The fastest path is option A.

Copy `skills/debrief.md` and `skills/reflect.md` from this pack into a `Skills/` folder inside your project. That is the whole install.

- **debrief** captures what happened and files it into the three homes. It never appends dated blocks to a `CLAUDE.md` or `TASKS.md`. History goes in the log, state gets overwritten, tasks stay current.
- **reflect** captures your corrections and preferences so you do not give the same note twice. The motto is "correct once, never again". It always asks before saving anything.

In Cowork you trigger them with natural language, not slash commands. You say "debrief this" or "reflect on this" and the skill's description is what makes Claude reach for it. (These same files also work in Claude Code, because they carry frontmatter.)

---

## Step 5: Do one real piece of work, then run the loop

This is the step where it clicks, so do real work, not a test.

Pick something actual. Draft a client email. Plan a project. Work through a decision. Use Claude the way you normally would, on something that matters.

Then run the loop, in this order:

1. Say **"reflect on this."** Claude proposes any corrections or preferences it noticed and asks which to keep. Approve the good ones. They go into `about-me.md` or the relevant `CLAUDE.md`.
2. Then say **"debrief this."** Claude shows you a plan, then files everything into its one home: the dated narrative into `debrief-history.log`, the current state overwritten in the right `CLAUDE.md`, new tasks into `TASKS.md`.

Watch where each piece lands. The history stacks in the log. The state gets replaced, not piled up. The tasks stay clean. That is the moment you feel it: the system filed your work for you, in the right places, and next session Claude walks in already knowing where things stand.

Run reflect first, then debrief. Every session. That pair is the engine.

---

## Step 6: Keep going

Adding to the brain IS the work. You do not maintain this system as a separate chore. You just work, and run the loop at the end of each session. Every debrief makes your state current. Every reflect makes Claude better at working the way you want.

When you want to know what to do next, or you hit a question, open `FAQ.md`. It covers what to add as you grow, the common gotchas, and how the system compounds over time.

---

## If you only do one thing

Get `about-me.md` and the two skills (`debrief` and `reflect`) running. With standing context and the loop in place, the structure builds itself around your actual work. Everything else in this pack is there to make that easier, not to gate you.
