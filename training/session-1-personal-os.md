# Session 1: your personal AI system

**Length:** 90 minutes

**Outcome:** Every participant leaves with a working `about-me.md`, the three homes stood up, the skills available, and one real debrief reviewed and filed.

## 0 to 10 min: frame the job

Explain the one idea: files are memory. Show the difference between durable personal context and live work. Introduce the three homes without teaching the company layer yet.

Ask each participant to choose one real area of work and one real note they can safely use.

**You know it worked when:** Everyone can name their selected area, point to their real note, and explain where current state, history, and tasks will live.

## 10 to 20 min: create the deployed folder

Participants follow the first step in `you/README.md`. They create a new working folder, copy the personal template files, add the shared `skills/` folder, and point their agent at the deployed root.

Have them confirm the agent can list files but has not written anything yet.

**You know it worked when:** The deployed root contains `about-me.md`, `TASKS.md`, `debrief-history.log`, one area folder, and `skills/`.

## 20 to 40 min: build about-me.md

Participants run the about-me prompt. The agent interviews them in small batches, drafts the file, and waits for approval.

Coach participants to replace generic claims with concrete facts about their role, working preferences, voice, recurring people, and the work they want help with. They should remove anything they would not want the agent to act on later.

**You know it worked when:** `about-me.md` contains reviewed, specific context that would change how the agent approaches a real task.

## 40 to 55 min: stand up the three homes

Participants run the structure prompt for one real area. They review the proposed tree before approving it.

Check the routing together:

- current state is a living block in the area context file
- history is append-only in `debrief-history.log`
- open tasks live in `TASKS.md`

Do not add more areas during this block unless the first one already works.

**You know it worked when:** Each home exists, contains only its intended information type, and the participant can explain what gets overwritten and what gets appended.

## 55 to 65 min: check the skills

Participants ask the agent to read `skills/debrief/SKILL.md` and `skills/reflect/SKILL.md`, detect personal mode, and state the allowed destinations without writing.

Briefly introduce the remaining shared skills. Keep the focus on debrief and reflect because they maintain the first useful loop.

**You know it worked when:** The agent detects personal mode, names the correct three homes, and confirms that proposed writes require approval.

## 65 to 82 min: run one real debrief

Participants run debrief on the real note selected at the start. They inspect the proposal, reject any invented detail or wrong destination, and approve only the correct writes.

Facilitators check that the source note remains unchanged. If the note has no task or state change, that is fine. The debrief should reflect the source rather than manufacture activity to fill every file.

**You know it worked when:** A dated entry exists in `debrief-history.log`, any real open task is in `TASKS.md`, current state is accurate, and nothing was written before approval.

## 82 to 88 min: run reflect

Participants ask the agent to reflect on the setup session. They choose one genuine correction or working preference, or explicitly save nothing if there was no useful finding.

The agent proposes first. The participant selects what persists.

**You know it worked when:** A useful selected preference is saved to the right context file, or the participant makes a deliberate no-write decision after reviewing the findings.

## 88 to 90 min: close and commit to the habit

Each participant states when they will next run debrief and what will trigger reflect. Point them to the personal README for the ongoing loop.

**You know it worked when:** Every participant has the four required outcomes and a specific next real use, not a plan to rebuild the system later.
