# FAQ

Common questions about setting up a personal AI operating system in Claude Cowork.

A note on product details: Cowork's interface, pricing, plan availability, and feature limits change over time. Where this guide touches those, check Anthropic's current docs for the live answer. This FAQ focuses on the method, which holds up regardless.

---

## Getting started

### Do I need to be technical to use this?

No. If you can write a note in plain English and save a file, you can run this. The files are just text. You describe what you want in normal language and the assistant does the editing. Nothing here requires code.

### What is the difference between Claude.ai Projects and Cowork?

A Project is a chat with reference docs attached. It reads those docs but does not change them, and the thinking lives in the conversation. Cowork gives the assistant a desk: a folder it can both read and write. Work persists as files in that folder, so the folder itself becomes the project and survives across sessions.

### What do I build first?

Start small. Create `about-me.md`, one `CLAUDE.md` for a company or area you work on, and two skills (debrief and reflect). That is the whole starter kit. Add more files and skills later, only when a real need shows up.

### Do I need Claude Code, or does this work in Cowork?

This works in Cowork. You do not need Claude Code. The two skill files happen to also work in Claude Code because they include frontmatter, so if you ever move between the two, the same skills come with you. But Cowork alone is enough.

---

## How it works

### What is a CLAUDE.md file and why is it named that?

A `CLAUDE.md` file is the standing context for one company or area: what it is, who is involved, and a "Current State" block for what is happening right now. The name is a convention the assistant looks for, so keeping the exact filename means it gets picked up reliably. Treat it as the home base document for that area.

### Why not just keep everything in one big notes file?

Because two different kinds of information rot at different speeds. Slow context (what things are) changes rarely. Fast context (what is happening now) changes constantly. Mix them in one file and the stale stuff buries the fresh stuff, and you stop trusting the file. Splitting them keeps each part clean.

### What are "the three homes"?

When something happens in a session, it goes to one of three places, never mixed:

1. Current state goes into the relevant `CLAUDE.md` "Current State" block, overwritten in place so it always reflects now.
2. History goes into `debrief-history.log`, appended to the bottom, never edited.
3. Open tasks go into `TASKS.md`, which holds only open items.

Reference material and live state never live in the same spot. That separation is what keeps the system readable.

### What is the difference between the debrief skill and the reflect skill?

Debrief captures what happened and files it into the three homes (current state, history, tasks). Reflect captures corrections and preferences, the "tell me once, never again" learnings about how you want things done. Run reflect first so any corrections are logged, then debrief to file the work. They do different jobs and both matter.

---

## Habits and upkeep

### How often should I run debrief and reflect?

Run them at the end of a working session, or whenever you have made real progress worth saving. There is no fixed schedule. A good rhythm is reflect first (catch the corrections), then debrief (file the outcome). If a session was just chatting with nothing to save, skip it.

### What if I forget to run them for a week?

That is fine. The system is forgiving. When you remember, just run a catch-up debrief and tell the assistant roughly what happened across that gap. It files the decisions and tasks the same way. Nothing breaks from a missed week.

### Where do meeting notes go?

Keep it simple. Run debrief and it pulls the decisions and tasks out of the meeting and files them into the three homes. If you want to keep the raw notes too, drop them as a file in the relevant area folder. The point is that the decisions and tasks get captured. The full transcript is optional.

### Won't my CLAUDE.md files get huge over time?

No, as long as you follow the one rule: overwrite current state, append history to the log. The "Current State" block stays roughly the same size because new state replaces old state. The growing pile of history lives in `debrief-history.log`, separately. If a `CLAUDE.md` is ballooning, something is being appended that should have gone to the log.

### What do I do after the basics are working?

Two directions. Add more `CLAUDE.md` files as you take on more companies or areas. And build your own skills for tasks you repeat: if you find yourself giving the same instructions often, that is a skill waiting to be written. Grow the system to match your actual work, not ahead of it.

---

## Tools and compatibility

### How do I trigger a skill in Cowork?

You ask in plain language. Say "debrief this" or "reflect on this session" and the assistant runs the matching skill. You do not type slash commands in Cowork. The skill files do carry frontmatter so they can also be triggered in Claude Code, but in Cowork natural language is how you call them.

### Can I use this with connectors (Gmail, Drive, Calendar)?

Often yes. Once a connector is set up, the assistant can work with that real account, not just talk about it. Keep it on a tight leash at first: have it draft and not send, suggest and not change, until you trust it. Which connectors are available and how to enable them changes, so check Anthropic's current Cowork docs for what is supported today.

### How is this different from a Notion or Obsidian setup?

In Notion or Obsidian, you maintain the system. You file the notes, you update the pages, you keep it tidy, and it decays the moment you get busy. Here, the assistant maintains it through the debrief and reflect loop. You do the work and the system keeps itself current as a side effect. That loop is the whole difference.

---

## Troubleshooting

### Is my data safe, and where do these files live?

These are files, kept on your machine or in your Cowork workspace depending on how you are set up. They are not a separate hosted product you are publishing to. For exactly where files are stored, how they are handled, and any data and privacy specifics, check Anthropic's current docs rather than trusting a general claim here, since those details can change.

### My CLAUDE.md is getting cluttered with dated entries. What went wrong?

Dated, stacked entries in a `CLAUDE.md` (or in `TASKS.md`) mean history is being appended where it does not belong. Those dated blocks should go to `debrief-history.log`. Move them there, reduce the `CLAUDE.md` back to a clean "Current State" block, and let debrief route new history to the log from now on.

### The assistant did not pick up my standing context. What do I check?

Confirm `about-me.md` and the relevant `CLAUDE.md` actually exist in the folder the assistant is working in, with those exact filenames. Standing context only gets read if the files are where the assistant looks. If a fact is wrong, run reflect and correct it once so it sticks.
