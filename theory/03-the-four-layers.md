# The four layers

A useful AI setup has four layers: architecture, context, brain and skills. The order matters because each layer depends on the one below it. Start at the top and you get a clever workflow with nothing reliable to work from. Start at the bottom and each new capability has somewhere solid to stand.

## 1. Architecture: where everything lives

Architecture is the folder structure and the routing logic. It gives the AI a root, a map and clear places to look for different kinds of information.

Good architecture mirrors the work closely enough that a newcomer can navigate it. The root context file explains what the system contains, which rules apply and where to go for a given task. Smaller folders keep each area scoped. The labels matter less than the routing. The AI should not have to search the whole business to find one relevant fact.

Architecture comes first because everything else needs an address.

## 2. Context: what the AI can see now

Context is the information available when the AI acts. It includes the files loaded at the start, the current state you provide, and anything the AI is allowed to retrieve for the task.

The job is not to load everything. A huge context window can still drown the useful facts in noise. Give the AI the smallest current, relevant slice that lets it do the work properly. The architecture makes that possible by pointing it towards the right files.

Context is assembled for a task. Some of it belongs to you. Some may come from a live system or a document you have just supplied. It answers the question: what can the AI see right now?

## 3. Brain: the knowledge you keep

The brain is your owned, persistent part of the context layer. It holds the refined knowledge that should survive beyond one session: what you do, how you work, what the company knows, who owns which decisions and what has already been learned.

A document dump is raw material, not a brain. Mine your existing documents for the useful signal. Distil that signal into short files, then connect those files through the root map. Keep raw sources available for verification without forcing every task to read them in full.

The brain must also stay alive. Debriefs write decisions and changed state back into the right homes. Reflection captures corrections and working preferences. You approve those changes because the brain is the source the next session will trust.

## 4. Skills: the repeatable work

A skill is a written workflow the AI can run by name. It is a verb: debrief, reflect, prepare, review. The brain supplies the nouns the verb acts on.

This is why skills come last. A writing skill without voice context produces generic writing. A meeting skill without current company context produces a tidy summary that misses what matters. The instruction may be sound, but it has no grounded judgment underneath it.

Run the workflow manually first. Notice the real steps, the decisions that require your judgment and the points where approval matters. Once the process works, write it down as a skill. Automate later, after the manual version has proved useful. The AI drafts. You send.

## Build from the bottom

The four layers are one stack, not four separate projects:

1. Give the work a clear structure.
2. Load only the context the task needs.
3. Keep your durable knowledge refined and current.
4. Add repeatable skills on top.

Tool choice sits outside this order. Any capable agent that can read and write the files can use the same structure. Treat the runtime as rented and the brain as owned: if you change tools, the architecture and brain still belong to you.

The visible magic tends to happen in the skills. The quality comes from the layers underneath.

**Next:** [04-the-debrief-reflect-loop.md](04-the-debrief-reflect-loop.md). Keep the brain current while you work.
