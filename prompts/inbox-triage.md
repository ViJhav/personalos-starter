# Inbox triage

**Purpose:** get every item in `inbox.md` into a real home. Never apply silently.
**Reads:** `inbox.md`, `current-state.md`, `weekly-plan.md`, and any project or area file an item clearly points at.
**Proposes writes to:** project READMEs, area files, `decisions.md`, `weekly-plan.md`. Clears processed items from `inbox.md` only after approval.

**Two modes.** *Quick* is a short pass during the week: classify and park, skip the deep context read. *Full* is a thorough pass, usually before a weekly review: read full context, surface ambiguity, split items that are secretly two things. Default to quick if the inbox has five items or fewer, otherwise ask.

---

## Prompt body

You are helping process the PersonalOS inbox. Follow this exactly.

### Step 1 — Read context

**Quick mode:** read `inbox.md` and `weekly-plan.md`. Skim the folder names in `projects/` and `areas/` so you know what destinations exist. That is all.

**Full mode:** read `current-state.md`, `weekly-plan.md`, `inbox.md`, the folder names in `projects/` and `areas/`, and any project or area README an inbox item clearly points at.

### Step 2 — Classify each item

For each item, propose exactly one category. Do not invent new categories.

| Category | Where it goes |
|---|---|
| **Next action** for a specific project | That project's README, under Next actions |
| **Next action** with no project | The relevant `areas/<area>/README.md` under Open items. Put it on `weekly-plan.md` only if it is genuinely happening this week |
| **Area update** | The relevant area README or subnote |
| **Decision** worth not re-litigating | `decisions.md`, with the full date / decision / reasoning / tradeoffs structure |
| **Backlog idea** | The relevant area README or project README. Do not create a global backlog file, it becomes a place things go to die |
| **Feedback or observation** (how something went) | Distilled into the relevant area or project file as a short "what worked, what to change" line. Capture the lesson, not the raw log |
| **Reference** (a fact, no action) | An existing notes file, or a proposed new one. Ask before creating new files |
| **Calendar or reminder** | Say so, and give the exact title and date so it can be added to the real calendar or reminders app. Those apps own it, not the vault |
| **Done, or nothing, or bin** | Mark for removal. This is a good outcome and should be common |

Some items are two things wearing a trenchcoat. Split them.

If an item is genuinely ambiguous: in quick mode, leave it in the inbox and flag it for a full pass, do not stall. In full mode, ask rather than guessing.

### Step 3 — Make parked items action-ready

When something is being parked rather than done, spend a moment making it decidable later.

If an item is "look into X" and one or two facts would make it obvious what to do, fetch them now and write them into the parked line: the price, whether they deliver, whether the thing needs an appointment, when the window closes. The reason to do this at parking time is that the friction which stopped it the first time is usually a missing fact, and it will stop it again next month for the same reason.

Do not over-research. One or two facts, then park it.

### Step 4 — Propose

Output a single table: the item, the proposed category, the exact destination, and the exact text that would be written.

**Do not edit any files yet.** Wait for approval.

### Step 5 — Apply

After approval, make the approved edits and remove the processed items from `inbox.md`.

**Every processed item must end with a destination.** No "needs a home" limbo, and nothing gets quietly left in the inbox to be dealt with later. If something genuinely has no home, bin it or ask. An item that survives triage unprocessed is a failure of this routine, because the whole value of the inbox is trusting that things put there get handled.

Then summarize in a few lines: what moved where, what was binned, what is still open.

### Rules

- Do not create new project folders or area files during triage. Flag the need and ask.
- The weekly plan is a commitment surface, not a store. An item reaches it only if it is due this week or has genuinely nowhere else to live. Everything else waits in its area or project file until it is timely.
- Bin things freely. A triage that keeps everything has not done its job.
- Stay concise. The value is in the routing, not the commentary.
