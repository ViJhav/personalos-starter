# Setup

The first-time setup, written so it is safe to run any number of times. Run it with `/prompt setup`, or by saying "let's set this up" or "continue setup".

**Reads:** every root file, `areas/`, `projects/`, `areas/readme-interview.md` if it exists.
**Writes:** the same files, adding to what is there. Never overwrites something the user already wrote.

## The rule that makes this rerunnable

**Work out what is already done from the files themselves, every run. Never assume a fresh start, and never assume a part is finished because it was asked about.** There is no separate progress file to fall out of sync: the vault's content is the progress.

So each run goes: check state → report it in a few lines → do only what is missing → write by adding, not replacing.

## Step 0: migrate an older copy

Earlier versions of this vault kept the interview inside `CLAUDE.md`, between `<!-- INTERVIEW-BLOCK-START -->` and `<!-- INTERVIEW-BLOCK-END -->`, and deleted it when done. If that block is still there, the setup was started under the old version and possibly not finished.

- Delete the block (from the START marker to the END marker, nothing outside them). This prompt replaces it.
- If `CLAUDE.md` has no line pointing at `prompts/setup.md`, add this one directly under the "How to work with me" heading's italic note: `_Setup status: run /prompt setup to check what is still open. It only asks about what is missing._`
- Everything else the old interview already wrote stays exactly as it is. It counts as done in Step 1.

Say in one line that you did this, then carry on.

## Step 1: check what is already done

Read the files and mark each part **done**, **partial**, or **open**:

| Part | Done when |
|---|---|
| 1. What you are carrying | `current-state.md` has real content in Active priorities and at least one other section (not just the template's placeholder lines), and a date set |
| 2. Shape of your life | at least one `areas/<name>/README.md` or `projects/<name>/README.md` exists |
| 3. How to work with you | the "How to work with me" section of `CLAUDE.md` has real rules in it, not just the italic note |
| 4. Rhythm | a weekly review day is written down (in `README.md` § Review rhythm or `weekly-plan.md`), and `weekly-plan.md` has a real week in it |
| 5. Deep area interview | every area folder has a ✅ DRAFTED heading in `areas/readme-interview.md` (see `prompts/area-interview.md`) |

Partial means some of it is there: e.g. `current-state.md` has priorities but no constraints, or two areas exist but the user named a third that has no folder yet.

Then tell them, in at most five lines: which parts are done, which are partial or open, and what you will do next. Example: _"Parts 1 and 2 are done (current-state is filled in, you have health, money, and travel). Part 3 is half there: you said what frustrates you, but not how you like answers delivered. Parts 4 and 5 are open. I'll start with the gap in Part 3, about 5 minutes."_

If everything is done, say so, and stop. Do not rerun anything "to be safe".

## Step 2: fill the gaps, one question at a time

**Ask only about what is missing.** For a partial part, ask the specific missing question, not the whole part again. Before asking anything, say what the vault already has on it in one line, so the user confirms or corrects instead of repeating themselves.

**One question at a time.** Ask, wait, then ask the next one. Never send a numbered list of questions. Keep your own turns short and react briefly to each answer. If an answer is vague, ask one follow-up, then move on.

**Write as you go, not at the end.** After each part is answered, write it to its file immediately. That is what makes stopping halfway safe: whatever was covered is already on disk, and the next run picks up from there. If the user wants to stop, stop. Say which parts are still open and that `/prompt setup` continues from there.

### Part 1: what you are carrying (→ `current-state.md`)

1. What is taking up the most space in your head right now? The top few things.
2. For each one, where does it stand and what is the next thing that needs to happen? One at a time.
3. Is anything time-critical? Real deadlines only.
4. What is constraining you right now? Time, money, energy, health, someone else's schedule, travel.
5. Anything you are deliberately not touching? Naming it means it stops nagging.

### Part 2: the shape of your life (→ `areas/` and `projects/`)

6. Which parts of life need a home here? Offer a menu: health, money, home, work-adjacent admin, relationships, learning, travel, hobbies, pets, car. Create only what they name.
7. Is anything a project, with an end state and a "done"? A trip, a move, a course, a renovation, a job search.

Each area gets `areas/<name>/README.md` from the template in `areas/README.md`, filled with what came up and the rest left as prompts. Projects the same, in `projects/`. If a folder already exists, add to it; do not recreate it.

### Part 3: how you want to be worked with (→ "How to work with me" in `CLAUDE.md`)

8. When you ask for something, do you want it done and then shown, or proposed first? (Proposing first is safer but adds a round trip to everything.)
9. How do you like information delivered? Short and direct, or with more context? Do long answers help or overwhelm?
10. What consistently frustrates you about working with AI assistants? Ask this one properly and write the answer down close to verbatim.
11. When you are overwhelmed or stuck, what actually helps? One next action, a question, being left alone, things broken smaller?

Write these as rules you will follow, specific enough to act on. "Prefers short answers" is useless; "Lead with the answer, then the reasoning. Do not restate the question" is usable. Frustrations become things to actively avoid. Add to the section; never rewrite rules already there.

### Part 4: rhythm (→ `README.md` § Review rhythm, `weekly-plan.md`)

12. When would a weekly review realistically happen? An actual day, 15–20 minutes. If the honest answer is "it won't", say that's fine: the vault still works, it just drifts.

Then write a real first week into `weekly-plan.md`, only what is genuinely happening this week. Anything that came up without a home goes in `inbox.md`.

### Part 5: the deep area interview

Parts 1–4 make the vault usable. Part 5 makes it good: it fills each area README in depth, in the user's own words, through a question file they answer at their own pace instead of live in chat.

When Parts 1–4 are done (or the user asks for it directly), explain it in two sentences and offer to start: _"Next is the deep pass: I'll write a question file for your areas that you fill in over a few days, whenever, then I ask a few follow-ups and draft each README from your answers. Want me to make the file now?"_ If yes, run `prompts/area-interview.md`.

## Step 3: close out

Show a short summary: which files you wrote or added to this run, and which parts are still open, if any. Then, only the first time Parts 1–4 are all done:

- `CLAUDE.md` is theirs to edit, and "How to work with me" is the section that pays off most. Every correction on style or process should get written there.
- The one habit that makes it work: dump into `inbox.md` whenever, and do the weekly review. Everything else is optional.
- `/prompt weekly-review` and `/prompt inbox-triage` run the two saved routines.
