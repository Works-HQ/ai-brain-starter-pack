# Prompt: Set up a new project

Run this each time you start a real project or stand up a new business unit. It creates the operating files for that project from the templates and fills in as much context as the AI already knows.

## The prompt

Paste this into your AI, fill the `<brackets>`, send.

```text
Set up a new project called "<Project Name>".

Create a folder for it with these files, copied from operating-system/templates/:
- a context file (what it is, who is in it, where it stands)
- a tasks file (or just use GLOBAL_TASKS with a project tag)
- DECISIONS.md
- WAITING_FOR.md
- WEEKLY_UPDATE.md
- a Meetings/ subfolder

Then populate the context file as far as you can from what you already know about this project from my brain files and anything I point you to. Mark anything you are unsure about with [confirm]. Ask me up to 5 questions only if you genuinely cannot fill the context without them.

Rules:
- Do not overwrite any existing file. If one exists, leave it and tell me.
- Show me the resulting folder layout and confirm nothing existing was changed.
- Keep the context file lean. It is the live operating view, not a strategy doc.
```

## Note

If this project is a whole business in its own right, it also gets a `brain/Company.md` file for the slow-changing "what it is" picture. The project folder here holds the fast-moving operating layer (tasks, decisions, meetings). The brain holds the durable picture. Keep them separate.
