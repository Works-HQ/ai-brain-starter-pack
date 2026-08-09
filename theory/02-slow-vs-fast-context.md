# Slow vs fast context

Most knowledge systems die the same way. You start tidy. You add notes. A few weeks in, you cannot tell what is current and what is stale, so you stop trusting the files. Then you stop using them. Now you have a junk drawer.

One distinction prevents this: some context changes slowly and some changes fast.

## Slow context describes

Slow context is what something **is**. Your role. A company's business model. A person's responsibilities. Your writing preferences. The shape of a project. These facts may change, but not every day.

Slow context belongs in the brain. Give each real area a short file that holds the durable facts the AI would otherwise need you to repeat. Keep the file scoped. A person file should describe that person, not become the running history of every conversation with them.

You revisit slow context when reality changes. You do not add a fresh copy every time the fact appears in your work.

## Fast context tracks

Fast context is what is **happening now**. This week's status, the next action, open threads and current tasks. It can change several times in one day.

Fast context belongs in the operating layer. The personal structure in this pack gives it three homes:

1. Current state lives in the relevant root context file and gets overwritten in place.
2. History lives in `debrief-history.log` and only gets appended.
3. Open tasks live in `TASKS.md`, with completed work removed.

Those rules keep the latest truth easy to find without throwing away the story of how you got there.

## Mixing the speeds creates rot

Imagine a company context file. The slow section says what the company sells, who owns which decisions and how work gets approved. The current-state section says a campaign is waiting on final copy and the next action is a review.

After the review, overwrite that current-state block. Do not paste a dated meeting summary beneath it. The meeting belongs in the history log. Any open action belongs in `TASKS.md`. Any genuinely durable change belongs in the slow section.

If you keep stacking dated updates in the context file, the AI has to choose between several versions of the truth. If you keep completed tasks, it cannot tell what still needs attention. If you rewrite the history log, you lose the record that explains later decisions.

The files may all contain accurate sentences. The structure still fails because the AI cannot tell which sentence has authority now.

## Use two verbs

The practical rule is simple:

**Overwrite current state. Append history.**

There is one current state, so replace the old snapshot when reality moves. There are many past events, so add each one to the record. Tasks are neither state nor history. Keep only the actions that remain open.

This split also makes maintenance easier. You can scan the current state without reading months of notes. You can review the history without mistaking an old plan for today's plan. You can open the task list and know every line still needs action.

Slow context gives the AI stable footing. Fast context tells it where things stand. Keep the two speeds separate and the system stays useful as the work changes around it.

**Next:** [03-the-four-layers.md](03-the-four-layers.md). See where both kinds of context fit in the full stack.
