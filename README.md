# AI Operating System Starter

A free starter kit that turns Claude from a chat you start cold every time into a personal operating system that remembers your work.

If you have used Claude.ai chats and Projects, you know the pattern. Great answers, but every conversation starts from zero. You re-explain who you are, who your clients are, where things stand. This pack fixes that. It teaches you to set up a Cowork project where your context lives as files Claude reads and updates, so your work persists and your system gets smarter the more you use it. Built for people moving from Claude.ai Projects to Cowork.

## Who this is for

- You have used Claude.ai chats and Projects and you are setting up your first Cowork project.
- You are smart and busy and you do not want to become a developer to make this work.
- You keep re-explaining the same context to Claude and you are tired of it.
- You run real work (clients, projects, a business, your own life) and you want a system that holds the state for you.

## What you get

Three things, and they fit together.

- **The mental model.** The one shift that makes Cowork different from Projects, explained plainly in `theory/`.
- **A simple structure.** A folder that is your workspace, with three clear homes for information so nothing rots into a junk drawer.
- **Two skills that run it.** `debrief` and `reflect`. They file what happens and capture how you like to work, automatically, in the right place.

## The idea in 30 seconds

Two rules. That is the whole system.

**Three homes.** Every piece of information has exactly one place to live.
1. **Current state** (status, last contact, next action) lives in a company or area `CLAUDE.md`, in a "Current State" block that gets overwritten in place.
2. **History** (the dated story of what happened) lives in `debrief-history.log`, append-only.
3. **Open tasks** live in `TASKS.md`, open items only.

**Slow vs fast.** Keep two kinds of context apart. Slow context is what things *are* (who a client is, who a person is). Fast context is what is *happening now* (this week's status, today's tasks). Reference and live state never mix. That separation is why the system stays readable instead of turning into a pile.

## Quickstart

Open [START-HERE.md](START-HERE.md) and follow the numbered steps. It takes about 20 minutes to go from an empty folder to a working system.

## What's in here

- `START-HERE.md`: the 20-minute walkthrough, start here.
- `FAQ.md`: common questions and what to do once it's running.
- `GLOSSARY.md`: plain definitions for the few terms used.
- `index.html`: a visual overview of how the pieces fit.
- `theory/`: the why, in three short reads (the mental model, slow vs fast, the debrief/reflect loop).
- `prompts/`: copy-paste prompts that build your about-me, your structure, and your skills.
- `skills/`: the two ready-made skills, `debrief.md` and `reflect.md`.
- `templates/`: starting points for `about-me.md`, `TASKS.md`, and a company `CLAUDE.md`.
- `examples/`: a filled-in example (a fictional coffee company) so you can see what "good" looks like.

## Requirements

- A Claude account with Cowork.
- That is it. No coding required.

The two skills also work in Claude Code if you use it, because they ship with the right frontmatter.

### Using this with Codex or Gemini

The methodology is tool-agnostic. The structure, the prompts, and the templates are plain markdown and work anywhere. The skills load in Claude (Cowork and Claude Code). For Codex or Gemini, the only change is the context filename: name your root context file `AGENTS.md` (Codex) or `GEMINI.md` (Gemini) instead of `CLAUDE.md`. The contents are identical. Many people keep both and point one at the other with a symlink. The architecture is the product, the tool is downstream of it.

Cowork is evolving, so product features and the exact UI may change over time. If something in this pack looks different from what you see on screen, check Anthropic's current docs and trust those for live behaviour. The ideas here (the three homes, slow vs fast, the two skills) hold regardless of UI.

## Licence

MIT. Use it, fork it, adapt it, ship it. See [LICENSE](LICENSE).

---

### Built by Works

Works is an AI enablement consultancy. We install this operating layer inside teams for a living. This pack is the free, self-serve version of that work. The teaching content stays pure, no upsell baked into it.

If you want the done-with-you version, [grab a time](https://savvycal.com/Zachary-King/zac-at-works-30). Otherwise, take this, run it, and make it yours. More at [workshq.com.au](https://workshq.com.au).
