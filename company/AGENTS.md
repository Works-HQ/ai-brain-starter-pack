# Context Root

This is the first file your AI reads on every run. It tells the AI who you are, how you work, and where everything lives. Keep it lean. Fill the placeholders, delete the guidance notes once you have, and add to it as your world gets clearer.

`CLAUDE.md` and `AGENTS.md` in your deployed folder are identical. If you edit one, make the same edit to the other.

---

## Who I am

- **Name:** `<YOUR NAME>`
- **What I do:** `<ONE LINE: your role and the businesses you run or work across>`
- **Where I work from:** `<machines / OS, if it matters>`

`<2-4 lines: your story, what you are building, what matters to you. Enough that the AI talks to you as you, not as a generic user.>`

---

## How I decide and how I sound

- **Decision style:** `<fast and decisive / considered and thorough / data first / gut then check>`
- **Voice:** `<how you want drafts to sound: direct, warm, plain, formal. Give an example line if you can.>`
- **What I do not want:** `<corporate filler, hype, hedging, whatever grates on you>`

---

## My world

Use this as a short map. Keep durable company context in `brain/Company.md` and context about people in `brain/People/`.

- `<BUSINESS / PROJECT>`, `<one line>`, context in `brain/Company.md`
- `<BUSINESS / PROJECT>`, `<one line>`

---

## How this deployed folder is laid out

- **`brain/`** holds slow-changing context about the company and its people. Read the relevant file before doing related work. Ignore `brain/_source-docs/` on normal runs because it is raw source material, not refined context.
- **`operating-system/`** holds fast-changing state in `current-context.md`, one task list in `GLOBAL_TASKS.md`, and the working files created from `operating-system/templates/`.
- **`skills/`** holds the repeatable workflows: debrief, reflect, morning sweep, weekly update, and meeting notes.

These paths are relative to your deployed root folder. They do not point back into the starter-pack repository.

---

## The hard rules (non-negotiable)

- **The AI drafts, you send.** No autonomous sending of email, messages, or posts. Ever. Every reply is drafted by the AI and sent by you.
- **Manual first, automate later.** Prove a workflow is useful twice before you schedule or automate it.
- **Capture immediately, file later.** Never lose a thought to "I will remember it." Dump it in, sort it after.
- **Never overwrite the brain.** This system wraps around what you already have. It adds a layer, it never replaces your existing files.

---

## How to work with me

- Read the relevant brain file before working on a business or person. Do not answer from a blank slate when context exists.
- Read the current operating-system files before changing live state, tasks, decisions, or logs.
- When you are unsure, mark it `[confirm]` rather than stating a guess as fact.
- Flag anything legal, financial, HR, or otherwise sensitive for my review before filing it anywhere.
- Show me the plan before writing across any files. Wait for approval, then write only the approved changes.
- Never overwrite an existing brain file. Update approved facts in place and preserve everything else.
- No emdashes. Use commas, periods, or line breaks.

---

## A note on tools

This system is tool-agnostic. It is markdown files, a task list, and a rhythm. Any capable AI agent that can read and write files in this folder can run it. Claude Code and Codex are examples, not requirements.

If you use Gemini CLI, copy CLAUDE.md to GEMINI.md.
