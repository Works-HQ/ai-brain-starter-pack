# AI Brain Starter Pack

Give your AI agent lasting memory of you and your company using plain markdown files.

Most AI work starts cold. You explain the same background, recover the same decisions, and rebuild the same working context in a new conversation. This starter pack puts that context into files the agent can read and update, so the work survives the chat.

You can get the personal level working in about 30 minutes. No database, custom app, or coding project required.

## The one idea

Files are memory.

Your conversations disappear from view. A small, routed set of files persists. One file explains who you are. Other files hold current state, history, tasks, company facts, people context, decisions, and repeatable skills.

The value is not a giant archive. It is knowing where each kind of information belongs, then using a debrief and reflection rhythm to keep those files current.

## The two-level ladder

### Level 1: you

Start with your own context. Build `about-me.md`, give current state, history, and open tasks one home each, install the shared skills, and run one real debrief.

[Follow the personal quickstart](you/README.md).

### Level 2: your company

Once the personal loop works, add durable company knowledge, people files, a shared operating layer, and a weekly rhythm. Mine the first brain files from documents you already trust instead of filling blank templates from memory.

[Follow the company quickstart](company/README.md).

## The 30-minute promise

A fresh reader should be able to make the personal level useful within 30 minutes. Useful means the agent has standing context, the three homes exist, the skills can find them, and one real debrief has updated the correct files with approval.

Thirty minutes is a design test, not a claim that your whole working life can be documented in half an hour. If the first useful loop takes longer, the structure is too complicated.

## Repository map

- [`START-HERE.md`](START-HERE.md) routes you through the setup, personal first and company second.
- [`you/`](you/README.md) is the standalone personal package. Deploy it with `skills/`.
- [`company/`](company/README.md) is the standalone company package. Deploy it with `skills/`.
- [`skills/`](skills/debrief/SKILL.md) contains five dual-mode workflows that detect the personal or company structure, each with a done-when line for what counts as finished.
- [`theory/`](theory/01-the-one-idea.md) explains the method in seven short chapters.
- [`training/`](training/facilitator-guide.md) contains ready-to-run personal and company sessions.
- [`FAQ.md`](FAQ.md) answers common setup and upkeep questions.
- [`GLOSSARY.md`](GLOSSARY.md) defines the system's terms in plain English.
- [`index.html`](index.html) is a dependency-free visual overview.

## The four hard rules

- **The AI drafts, you send.** No autonomous sending of email, messages, or posts. Ever. Every reply is drafted by the AI and sent by you.
- **Manual first, automate later.** Prove a workflow is useful twice before you schedule or automate it.
- **Capture immediately, file later.** Never lose a thought to "I will remember it." Dump it in, sort it after.
- **Never overwrite the brain.** This system wraps around what you already have. It adds a layer, it never replaces your existing files.

## Tools

The system is tool-agnostic. Claude Code, Codex, and Gemini CLI are examples, not requirements. Any capable agent that can read and write files in your folder can use it.

Claude Code reads `CLAUDE.md`. Codex reads `AGENTS.md`. If you use Gemini CLI, copy CLAUDE.md to GEMINI.md.

Think of the runtime as rented. The harness, the model, the interface: that layer belongs to whoever built it, and it will keep changing whether you like it or not. Your brain, your skills, and your loops are the part you own. They are plain files, they are portable across engines, and they are the part that keeps compounding after this quarter's model gets replaced by next quarter's.

## Where the method came from

This method grew from using AI agents on real operating work, then reducing the setup to the parts that kept earning their place. The personal layer came first: standing context, three homes, debrief, and reflect. The company layer followed when the same problem appeared across shared knowledge, decisions, people, and weekly work. The method has been taught, used, corrected, and simplified through repeated delivery. This repository is the public version of that lineage.

## Licence

MIT. Use it, adapt it, and teach it. See [LICENSE](LICENSE).

---

Built and maintained by Works (workshq.com.au). If you want this installed across your company, book an intro: https://savvycal.com/Zachary-King/zac-at-works-30
