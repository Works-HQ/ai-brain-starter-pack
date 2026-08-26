# AI Brain Starter Pack

Give your AI agent lasting memory of you and your company using plain markdown files.

Most AI work starts cold. You explain the same background, recover the same decisions, and rebuild the same working context in a new conversation. This starter pack puts that context into files the agent can read and update, so the work survives the chat.

You can get the personal level working in about 30 minutes. No database, custom app, or coding project required.

## The one idea

Files are memory.

Your conversations disappear from view. A small, routed set of files persists. One file explains who you are. Other files hold current state, history, tasks, company facts, people context, decisions, and repeatable skills.

The value is not a giant archive. It is knowing where each kind of information belongs, then using a debrief and reflection rhythm to keep those files current.

## One brain, multiple agents

The runtime is rented. The brain is owned.

Claude and Codex enter through different instruction files, but they can work from the same brain. Claude Code reads `CLAUDE.md`. Codex reads `AGENTS.md`. Both entry files should route to the same visible context, memory, tasks, history, and skills inside one folder you control.

```text
AI Brain/
  CLAUDE.md
  AGENTS.md -> CLAUDE.md
  about-me.md
  working-preferences.md
  current-context.md
  TASKS.md
  debrief-history.log
  memory/
  skills/
```

Prefer a relative symlink from `AGENTS.md` to the canonical `CLAUDE.md` when your filesystem and tools support it. Otherwise, generate an identical copy and add a drift check. Do not maintain two hand-edited sets of instructions.

Hidden tool memory can cache or point to these files, but it should never be the only copy. The owned folder is canonical. That is what lets a fresh Claude session and a fresh Codex session inherit the same approved knowledge, and lets an update made through one runtime survive when you switch to the other.

[Read the visual overview](shared-brain.html), then [set up one shared brain for Claude and Codex](SHARED-BRAIN.md).

## The two-level ladder

### Level 1: you

Start with your own context. Build `about-me.md`, give current state, history, and open tasks one home each, install the shared skills, and run one real debrief.

[Follow the personal quickstart](you/README.md).

### Level 2: your company

Once the personal loop works, add durable company knowledge, people files, a shared operating layer, and a weekly rhythm. Mine the first brain files from documents you already trust instead of filling blank templates from memory.

[Follow the company quickstart](company/README.md).

## How the brain operates

The same four steps turn scattered business knowledge into context an AI agent can use:

1. **Evidence.** Keep the original files, meeting notes, reports, and system records. They are the source material and stay untouched.
2. **Refine.** Pull out the facts, decisions, procedures, and preferences that matter. Cite the source and flag anything that conflicts or needs confirmation.
3. **Review.** A person checks the proposed knowledge, then approves, corrects, or rejects it before the working brain changes.
4. **Approved brain.** Store the checked knowledge in the right brain file. The agent can now retrieve the smallest useful slice for the next job instead of searching the whole archive.

The loop keeps running. Work creates new evidence, debriefs capture what changed, and approved lessons return to the brain. The source material remains traceable, and each future job starts from checked facts instead of another search through the archive.

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
- [`SHARED-BRAIN.md`](SHARED-BRAIN.md) connects Claude and Codex to one owned brain without duplicating the underlying knowledge.
- [`shared-brain.html`](shared-brain.html) is the model-neutral visual overview: one diagram, the core rules, and a portability test.
- [`index.html`](index.html) is a dependency-free visual overview.

## The four hard rules

- **The AI drafts, you send.** No autonomous sending of email, messages, or posts. Ever. Every reply is drafted by the AI and sent by you.
- **Manual first, automate later.** Prove a workflow is useful twice before you schedule or automate it.
- **Capture immediately, file later.** Never lose a thought to "I will remember it." Dump it in, sort it after.
- **Never overwrite the brain.** This system wraps around what you already have. It adds a layer, it never replaces your existing files.

## Tools

The system is tool-agnostic. Claude Code, Codex, and Gemini CLI are examples, not requirements. Any capable agent that can read and write files in your folder can use it.

Claude Code reads `CLAUDE.md`. Codex reads `AGENTS.md`. If you use Gemini CLI, copy CLAUDE.md to GEMINI.md.

Those are entry doors, not separate brains. Route them to the same files. Prefer one canonical instruction file with a symlink or generated mirror instead of maintaining several hand-edited versions.

Think of the runtime as rented. The harness, the model, the interface: that layer belongs to whoever built it, and it will keep changing whether you like it or not. Your brain, your skills, and your loops are the part you own. They are plain files, they are portable across engines, and they are the part that keeps compounding after this quarter's model gets replaced by next quarter's.

## Where the method came from

This method grew from using AI agents on real operating work, then reducing the setup to the parts that kept earning their place. The personal layer came first: standing context, three homes, debrief, and reflect. The company layer followed when the same problem appeared across shared knowledge, decisions, people, and weekly work. The method has been taught, used, corrected, and simplified through repeated delivery. This repository is the public version of that lineage.

## Further reading

When you are ready to go deep, these are the pieces worth your time. Different builders arriving at the same idea from different directions: files, context, and a rhythm that keeps them current.

For the method in long form, start with our own walkthrough: [The AI Brain Layer](https://workshq.com.au/resources/ai-brain-layer/) on the Works site.

**Company brains in the wild**

- [GBrain, by Garry Tan](https://github.com/garrytan/gbrain). An open-source company brain from the President of Y Combinator, MIT licensed, with a [companion eval repo](https://github.com/garrytan/gbrain-evals). The closest open build of the same idea. Read the structure, then notice how much of it is plain files.
- [How We Built Our Knowledge Base, by Cerebras](https://www.cerebras.ai/blog/how-we-built-our-knowledge-base). An engineering team's version of the same problem. Their core call: extract from where information already lives instead of forcing everything into one platform, and scope context per project so answers stay high-signal.
- [The 5-Layer Company Brain, by Eric Siu](https://x.com/ericosiu/status/2060415100603781497) and his follow-up, [Everything You Need to Build a Company Brain](https://x.com/ericosiu/status/2089762541412950164). Capture, retrieval, source truth, permissions, and feedback, then skills, evals, and loops. The second piece is the best single argument for giving every skill a definition of done.

**Context and method**

- [Context is King, by Alex Lieberman](https://x.com/businessbarista/status/2061983277263601672). Why the operator who manages context best gets the most out of AI, with a framework that maps almost one-to-one onto the files in this pack.
- [AI Strategy Should Be a Skill Library, by Hiten Shah](https://x.com/hnshah/status/2062647149582750101). The case for codified, repeatable workflows as the asset you actually own. The `skills/` folder here is this argument in practice.
- [AI Second Brains Decay, by Cole Medin](https://www.linkedin.com/posts/cole-medin-727752184_ai-second-brains-are-incredibly-useful-but-activity-7491493447535800321-6elJ). State versus event, and why brains rot without an update rhythm. This is the exact problem the debrief and reflect loop exists to solve.

**The bigger picture**

- [How to Build an AI-Native Services Company, by Y Combinator](https://youtu.be/gSNFJbgoaHI). Eleven minutes on where this way of working is heading commercially.
- [Jeff Dean at Princeton](https://www.youtube.com/watch?v=UTTeXZrpMR0). The Chief Scientist of Google DeepMind on one human directing a hundred agents, and why context is the bottleneck.
- [How Teams Actually Scale With AI, Tiago Forte and Rachel Woods](https://www.youtube.com/watch?v=nvuAt8sl7Ag). The human side: how teams adopt this without it collapsing into one enthusiast's side project.
- [How to Get Your Company AI-Pilled, by Geoff Charles](https://x.com/geoffintech/status/2042002590758572377). Ramp's VP of Product on driving adoption inside a real company.

## Licence

MIT. Use it, adapt it, and teach it. See [LICENSE](LICENSE).

---

Built and maintained by Works (workshq.com.au). If you want this installed across your company, book an intro: https://savvycal.com/Zachary-King/zac-at-works-30
