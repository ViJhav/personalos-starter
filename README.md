# PersonalOS

A personal operating system in plain markdown. An external brain for life outside of work: priorities, projects, routines, errands, health, money, learning, travel, home.

> What matters right now, what needs my attention, and what can safely wait?

## Start here

This repository is an **empty skeleton**, not my vault. Every file is a template: you fill it in, and it becomes yours. There is no code, no database, and nothing to install beyond a Claude subscription.

**Read [`START-HERE.md`](START-HERE.md) first.** It walks through the ten-minute setup, then a short interview (`prompts/setup.md`) fills in the rest by asking you questions, followed by a deeper one you answer at your own pace. Both are safe to stop and rerun.

Download it with **Code → Download ZIP** above, or clone it. Either way, rename the folder to whatever you like and delete the `.git` directory if you would rather not keep it under version control.

If you want the reasoning behind all of this rather than the files, start with the guide: **<https://www.viyatjhaveri.com/guide/ai-dev/>**

Shared as-is under the MIT license, because it was useful to me and might be useful to you. It is not a product and I do not maintain it as one, so issues are turned off. If you build something good with it, I would genuinely like to hear about it: `me@viyatjhaveri.com`.

## Where things live

| File / folder | Purpose |
|---|---|
| `CLAUDE.md` | How Claude should behave in this vault. Loads automatically every session. Edit it as you learn what you want. |
| `current-state.md` | High-signal snapshot of life right now. |
| `weekly-plan.md` | This week's commitments. The most-used file. |
| `inbox.md` | Triage area for anything uncategorized. Allowed to be messy. |
| `decisions.md` | Log of meaningful decisions, so they do not get re-litigated. |
| `areas/` | Ongoing parts of life that never finish (health, money, home). Routines live inside their area. |
| `projects/` | Time-bound efforts with a "done". One folder each. |
| `prompts/` | Saved routines. Run one with `/prompt <name>`. |
| `extras/` | Optional tools that sit beside the vault, e.g. `extras/packing-page/`, a one-file tap-through packing checklist. |

## Two layers

**Durable**: `CLAUDE.md`, `decisions.md`, area and project READMEs. Long-lived, stable, holds the *context*. This is what lets you resume something after six weeks away without rebuilding it in your head.

**Execution**: `weekly-plan.md`, `inbox.md`. Short-lived, refreshed constantly, helps you decide *what to do now*.

Keeping these separate is most of the design. The execution layer is allowed to be wrong and get rewritten weekly. The durable layer is not.

## areas/ vs projects/

**Areas** are ongoing responsibilities that never finish: health, money, home, relationships, learning. One folder each with a `README.md`, plus focused subnotes when a topic outgrows it.

**Projects** are time-bound and have an end state: a trip, a course, a move, a renovation. One folder each, named with the date it started.

Checklists and routines live inside their area (`areas/travel/packing-list.md`), not in a separate top-level folder.

Do not create either speculatively. Make one the first time you actually need it.

## Review rhythm

- **Daily, optional**: glance at `weekly-plan.md`. That is all.
- **Weekly**: run `/prompt weekly-review`. Fifteen to twenty minutes. The one ritual that matters.
- **Whenever**: dump into `inbox.md`, and run `/prompt inbox-triage` when it gets full. Log a decision when you make one worth not re-thinking.

The system is not graded on completeness. A messy week is fine. The review should produce clarity, not guilt.

## The trust model

The default flow is:

```text
you capture  ->  Claude proposes  ->  you approve  ->  Claude writes
```

As you get comfortable, collapse it. `CLAUDE.md` starts you at "edit, then show" for ordinary changes and "propose first" for the two files where a bad edit actually costs something.

What not to do is start at full automation. Do not wire Claude up to silently rewrite your life files from your email and calendar on day one. Trust is easy to lose here and slow to rebuild. Automate the boring repeated parts only after the manual version is something you rely on.

## Anti-goals

This should not become:

- A personal bureaucracy, or a second job.
- A giant dashboard.
- A fragile pile of automation you do not trust.
- A place where *everything* has to be tracked.
- Competing planners, where two systems both claim to own the same task.
- Something that only works if you are perfect every day.

When in doubt, do less. Optimize for retrieval, clarity, and action, not for a system that looks impressive.

> PersonalOS exists to turn scattered life context into calm, trusted, actionable state.
