# Weekly review

**Purpose:** turn the current state of the vault into next week's `weekly-plan.md`, surface anything that has gone stale, and bring `current-state.md` back in line with reality.
**Reads:** `current-state.md`, `weekly-plan.md`, `inbox.md`, active project READMEs, relevant area READMEs, and the calendar for the next two weeks.
**Proposes writes to:** `weekly-plan.md` (replaced), `current-state.md` (small edits), project and area READMEs, `decisions.md` if something got decided during the review.

Fifteen to twenty minutes. The goal is a plan that will actually be executed, not a thorough report.

---

## Prompt body

You are helping run a weekly review. Follow this exactly.

**Flow:** read context, triage the inbox, reconcile the outgoing week, surface what is stale, draft next week, update current state, propose, apply after approval.

**If time or energy is short**, say you are running the short path and do only this: read `current-state.md`, `weekly-plan.md`, and `inbox.md`; triage anything dated or urgent; draft next week's plan; update `current-state.md`. List what you skipped. A short review that happens beats a thorough one that does not.

### Step 1 — Read context

In this order:

1. `current-state.md` and `weekly-plan.md`. Note that `current-state.md` loads automatically, so use that copy unless something has edited it this session. `weekly-plan.md` never loads automatically, always read it.
2. `inbox.md`.
3. Each active project README listed under Active projects in `current-state.md`.
4. Any area README that came up in the inbox or is referenced in current state.
5. **The calendar**, if you have access to it, for the next 21 days. Slice it three ways: days 1 to 7 become Scheduled constraints in the new plan; days 8 to 14 become a heads-up line for anything needing lead time such as a booking, a gift, or travel prep; and scan the full window for birthdays and anniversaries, which are the classic thing that needs a week of lead time and gets noticed the day before.
6. **Ask once:** "Anything on your mind that is not written down yet?" Add the answer to `inbox.md` so it gets triaged with everything else. This catches more than the rest of the read combined.

### Step 2 — Triage the inbox

If `inbox.md` has anything in it, run the full-mode steps from `prompts/inbox-triage.md` inline. Wait for approval, apply, then continue.

Unprocessed items must not bleed into the plan.

### Step 3 — Reconcile the outgoing week

Close the loop on what actually happened before drafting anything new.

For every checked item on the outgoing plan, find its durable home and update it: mark the project action done, advance the recurring task's last-done date, update the area README. If it was plan-only and genuinely finished, let it disappear with the plan.

**Stage the successor action.** If a finished item has an obvious next step (dropped off means pick up; submitted means chase the reply; bought means the return window closes on a date), capture it now rather than letting it evaporate. This is where dropped balls actually come from.

While you are in a file reconciling it, **delete the completed action history**. The "did this on the 12th, submitted the 14th" residue that builds up under status sections. Keep the durable outcome, cut the log. Only in files you are already touching, this is not a cleanup project.

### Step 4 — Surface what is stale

Briefly list:

- Project READMEs whose next actions have not moved in two weeks or more.
- Open loops in `current-state.md` that have never been triaged.
- Anything in Waiting / not this week that has been deferred twice or more. This one needs a real call: do it, decide against it and log that, or drop it. Deferring the same item a third time with the same reason is not a decision, it is avoidance with extra steps.
- Anything in an area's Open items that has been sitting a month or more.

**Promote at least one aging item.** Each week, if any area backlog has something that has been sitting for weeks with no movement, put the oldest one on the plan even if nothing there is freshly urgent. This is the only mechanism that stops a pile growing silently while the plan chases whatever is loudest. One is a minimum, not a cap.

**Pause here** if any of this needs a real decision. Use the answers as planning assumptions. Do not edit files yet.

### Step 5 — Draft next week

Build `This week` from the reconciled project and area files plus the decisions above, not by sweeping inbox captures onto the plan.

Rules for the list:

- **Every line is genuinely happening this week.** If not, it stays in its project or area file. This single test does the work that an item cap is supposed to do.
- **Each item appears exactly once**, phrased as a finished state rather than an activity.
- **One line per real thing.** Bundle only when it is honestly one sitting. Three chores in one pass is fine. "Health admin" covering a phone call and an insurance dispute is not, it is a priority tier in disguise and it destroys per-item tracking.
- **No cap on the number of items, and no priority tiers.** If the list runs past ten, read it again as a signal, not a violation. Never trim a real commitment just to make the list shorter.

Then the Protected floor: the small minimums that happen regardless of how heavy the week is. Keep them concrete and small. "Spend time with my partner" is not a floor item, "walk after dinner on Wednesday" is. These never get deferred because something else got busy. That is the entire point of the section, and the week you defer them is the week you needed them.

Fill Scheduled constraints from the calendar. Fill Waiting / not this week with things consciously deferred (one line of why, plus a revisit date) and things blocked on someone else.

**Before dropping or deferring any line, confirm it exists somewhere durable.** If it lives only on the weekly plan, capture it to the right project or area file first. The plan gets rewritten every week, so an item that exists only there is a dropped ball waiting to happen.

Every unfinished item from the outgoing week gets an explicit call: re-chosen into This week, moved to Waiting with a reason, or left in its project file with no plan line. Say which call you made for each. Silently re-listing it is exactly what this replaces.

### Step 6 — Update `current-state.md`

Always do this, it is not optional. Check for drift:

- Deadlines that have passed.
- Events that moved from upcoming, to happening, to over.
- The `**This week:**` line, rewritten to frame the new week. This is the only place the week's framing lives, so it must never still be describing last week.
- Priorities that are no longer active, and projects to add or pause.

Propose targeted edits rather than rewriting the file. **Always bump the `_Last updated:_` date**, even if nothing else changed. It is the staleness signal.

One calibration note: be careful about labelling a week a crunch. That word should be rare and earned, meaning a genuinely hard deliverable on a hard external deadline. One busy thing is a heavier thread, not a crisis. If everything is a crunch the label stops meaning anything, and in practice it becomes a standing excuse to defer the protected floor, which is the exact failure this is guarding against. Default framing is "normal week, heavier thread: X".

### Step 7 — Propose

Output, in order: what the outgoing week closed out, the stale items and the calls made on them, the full new `weekly-plan.md` ready to paste, the proposed edits to `current-state.md`, and anything still unresolved.

**Do not edit any files yet.** This is the approval gate.

### Step 8 — Apply

After approval, replace `weekly-plan.md`, apply the `current-state.md` edits including the date bump, and apply the reconciliation edits to project and area files. Nothing else unless it was asked for.

Summarize in five to ten lines what changed.

### Rules

- A plan that will not be executed is worse than a plan admitting less is happening.
- Do not create new project folders or area files during a review. Flag the need, ask, defer.
- Do not edit `CLAUDE.md`, `README.md`, or anything in `prompts/` during a review. If the run exposes a problem with the process, add a line to `inbox.md` starting with `system:` and fix it in a separate session. Reconciling stale project and area files is content, not process, and is in scope.
- If next week is a travel week, say so and make the plan reflect that rather than a normal week.
- Stay concise. The value is the plan, not the commentary about producing it.
