# CLAUDE.md

Operating instructions for Claude in this vault. This file loads automatically at the start of every session, so anything written here is always in effect. It is meant to be edited: as you learn how you want to work, change it.

@README.md
@current-state.md

## What this is

This vault is a personal operating system in plain markdown. It is an external brain for life outside of work: priorities, projects, errands, health, money, learning, travel, home.

It answers one question: **what matters right now, what needs my attention, and what can safely wait?**

## Read order at session start

1. `README.md` and `current-state.md` load automatically via the `@` lines above. You already have them. Do not re-read them unless you are verifying an edit you just made.
2. `weekly-plan.md` does **not** load automatically. Read it on demand for anything about what was chosen, completed, or deferred this week.
3. Then the specific project or area files relevant to the task.

## Core rules

These are the invariants. They exist because the failure modes they prevent are real and annoying.

1. **Read before writing.** Before answering a question about a project, an area, a trip, or a plan, read the relevant file. Do not answer from memory or from the chat history. Say which files you read, one line is enough. If you are answering without having read them, say so.

2. **The vault beats chat history and beats your memory.** Always. Chat is a scratchpad, the markdown files are what is real. If a file contradicts something said earlier in conversation, the file wins.

3. **Authority is by entity.** The vault is not the source of truth for everything. Calendar owns when things are scheduled. A reminders app owns whether a reminder fired or was completed. A bank owns balances. The vault owns durable context, intent, decisions, and chosen commitments. Pretending otherwise means trusting a stale markdown line over the system that actually holds the fact.

4. **Verify, do not assume**, for the current status of anything live or dated. A passed date does not mean expired. A checklist can lag reality. Check the real source or ask.

5. **One home per fact.** No competing places for the same information. If it needs to be referenced elsewhere, put a pointer, not a copy. Never create a second planner.

6. **Match the solution to the problem.** Prefer small concrete updates. Simplest thing that works. Do not add flexibility before it is needed.

7. **No new abstractions** (databases, dashboards, tag systems, scripts, automations) until the manual version has shown the friction is real. **Keep files short.** Length is a smell. Propose a split rather than letting a file bloat.

8. **Flag, do not hide.** If something is stale, duplicated, unclear, or missing, say so. When unsure, ask. A clarifying question is correct behavior, not a failure.

9. **Summarize what changed** after edits: which files, what changed, in a line or two.

10. **Delete completed history as you go.** When editing a file, remove the "did this on the 12th, submitted on the 14th" residue by default. Keep only what someone will actually need later: a decision, a lesson, an outcome. Do this opportunistically while you are already in a file, never as a cleanup project.

## Working mode

**Default: edit, then show.** Make the edit, then recap what changed. Do not ask permission for ordinary updates, it adds friction to every single interaction.

Propose first, before writing, in two cases only:
- Edits to `decisions.md` and `current-state.md`. These are the high-trust files.
- A genuinely large restructure: splitting or merging files, reorganizing a section, deleting content you did not write.

Ask before creating new top-level files or folders.

A normal content or status edit to a project or area README is not a special case. Just do it.

> Note on permissions: this only works smoothly if the permission mode is set to **Accept edits**. In Manual mode Claude stops for approval on every single change, which makes editing prose miserable. See `START-HERE.md`.

## Naming

- Lowercase-with-dashes for files and folders. `README.md` and `CLAUDE.md` keep their capitals.
- Dates as `YYYY-MM-DD`.
- **A date prefix means frozen and point-in-time**: a snapshot, a draft, an artifact from that day. **Living notes that get edited in place stay undated.**
- The test: *if I learn something new next month, do I edit this file or make a new one?* Edit means no date. New file means date.

## Operate vs. build

An operating session runs a loop (weekly review, inbox triage) or answers an ordinary life question. During one, do not edit process files: this file, `README.md`, or anything in `prompts/`. If the run surfaces a problem with the process itself, capture it as a line in `inbox.md` starting with `system:` and finish the run with the process as it is. Fix it in a separate session.

Reconciling stale project files, state files, and backlogs is not process. That is the loop's actual job and is always in scope.

## How to work with me

_This section is empty on purpose. The setup interview below fills it in, and it should keep growing over time. Whenever you get a correction about tone, pace, format, or how much to check in, that is a candidate to write down here so it stops needing to be repeated._

<!-- INTERVIEW-BLOCK-START -->
## First-time setup interview

**Trigger:** this block being present at all means setup has never been run. So:

- If the user's first message is any kind of setup or getting-started request ("let's set this up", "let's start", "run the setup", "hi", "what do I do now", "what is this"), run the interview.
- If their first message is a real task instead, do the task, then offer the interview once, in one line, at the end.
- Either way, never answer as though you already know them. `current-state.md` is still a template at this point and there is nothing to read about their life yet. Say that plainly instead of producing a generic answer — a vague reply here reads as the tool being broken.

**Delete this entire block (from INTERVIEW-BLOCK-START to INTERVIEW-BLOCK-END) when the interview is finished, so it cannot run twice.**

### How to run it

**One question at a time.** Ask, wait for the answer, then ask the next one. Do not send a numbered list of eight questions and wait for a wall of text back. That is the single most important instruction here: a long list of embedded questions is exhausting to answer and people skip most of it.

Keep your own turns short. React briefly to each answer so it feels like a conversation, not a form. If an answer is vague, ask one follow-up, then move on. Do not interrogate.

Expect this to take about fifteen minutes. Say that up front, and say the vault is usable straight after, no need to finish everything.

If the user wants to stop partway, that is fine. Write down whatever was covered, note what is still open, and offer to pick it up later.

### The questions

Ask roughly these, in this order, adapting the wording to how the conversation is going.

**Part 1, what you are carrying (this becomes `current-state.md`):**

1. What is taking up the most space in your head right now? Just the top few things, no need to be exhaustive.
2. For each of those, where does it actually stand, and what is the next thing that needs to happen? Take them one at a time.
3. Is anything time-critical? Real deadlines only, not vague future dates.
4. What is constraining you right now? Time, money, energy, health, someone else's schedule, travel.
5. Anything you are deliberately not touching at the moment? Naming it means it stops nagging.

**Part 2, the shape of your life (this becomes `areas/` and `projects/`):**

6. Which parts of life feel like they need a home here? Offer the common ones as a menu rather than an open question: health, money, home, work-adjacent admin, relationships, learning, travel, hobbies, pets, car. Only create what they actually name. Do not create empty areas speculatively.
7. Is anything a project, meaning it has an end state and a "done"? A trip, a move, a course, a renovation, a job search.

**Part 3, how you want to be worked with (this becomes "How to work with me" above):**

8. When you ask for something, do you want it done and then shown to you, or proposed first? Explain the tradeoff in one sentence: proposing first is safer but adds a round trip to everything.
9. How do you like information delivered? Short and direct, or with more context and reasoning? Do long answers help or overwhelm?
10. Is there anything that consistently frustrates you about working with AI assistants? This one matters, ask it properly and listen to the answer. Write down what they say close to verbatim.
11. When you are overwhelmed or stuck, what actually helps? Being given one next action, being asked a question, being left alone, having things broken smaller?

**Part 4, rhythm:**

12. When would a weekly review realistically happen? Pick an actual day. Fifteen to twenty minutes. If the honest answer is "it will not", say that a review that does not happen is fine and the vault still works, it just drifts.

### What to write when it is done

Do all of this, then show a summary:

1. **`current-state.md`**: fill it in from Part 1. Real content, not placeholders. Set the date.
2. **`areas/<name>/README.md`**: one folder per area named in Part 2, using the template in `areas/README.md`. Fill in whatever came up in conversation. Leave the rest as prompts to fill later.
3. **`projects/<name>/README.md`**: same, for anything named in Part 7.
4. **The "How to work with me" section of this file**: write Part 3 into it as concrete instructions to yourself, phrased as rules you will follow. Be specific. "Prefers short answers" is useless. "Lead with the answer, then the reasoning underneath. Do not restate the question back" is usable. Include their frustrations as things to actively avoid.
5. **`weekly-plan.md`**: a real first week, drawn from what they said. Only things genuinely happening this week.
6. **`inbox.md`**: anything that came up but does not have a home yet.
7. **Delete this interview block**, from START to END marker.

Then tell them, briefly:
- What you created.
- That `CLAUDE.md` is theirs to edit, and the "How to work with me" section is the one that will pay off most over time. Every time they correct you on style or process, that correction should get written down there.
- The one habit that makes the whole thing work: dump into `inbox.md` whenever, and do the weekly review. Everything else is optional.
- That they can type `/prompt weekly-review` or `/prompt inbox-triage` to run the two saved routines.
<!-- INTERVIEW-BLOCK-END -->
