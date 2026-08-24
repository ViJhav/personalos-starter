# Areas

Ongoing parts of life that never finish: health, money, home, relationships, learning, travel, hobbies, car, pets.

One folder each, with a `README.md`. Add focused subnotes when a topic outgrows the README (`areas/home/chores.md`, `areas/travel/packing-list.md`). Routines and checklists live inside their area, not in a separate top-level folder.

**Do not create areas speculatively.** Make one the first time you actually need it, starting with whichever part of life is loudest. An empty area folder is worse than no folder, because it makes the vault look maintained when it is not.

The test against `projects/`: an area never finishes. If it has an end state, it is a project.

---

## Template for `areas/<name>/README.md`

Copy this. Delete any section you do not need, most areas will not need all of them.

```markdown
# <Area>

## Current state
Where this part of life stands right now. A short paragraph.

## Standards / how I want this to go
What "good" looks like here. The bar you are actually holding yourself to,
which is often different from the bar you would state out loud.

## Open items
Things that need doing, with rough priority. This is the backlog for this
area. The weekly review pulls from here.
- [ ] item

## Recurring
Things that happen on a cadence, with when they were last done.
| Task | Frequency | Last done |
|---|---|---|
|  |  |  |

## Key facts
Account numbers you reference constantly, policy names, sizes, model
numbers, who your doctor is. The stuff you look up repeatedly.
Never credentials, passwords, or government ID numbers.

## Decisions made
Things settled here, so they do not get re-opened. Link to `decisions.md`
for the big ones rather than duplicating.

## Useful context for Claude
The most valuable section in the file. Not facts, but *how to behave* in
this area. Constraints, sensitivities, things to never suggest, things to
always check first, how much to push.

Examples of what belongs here:
- "I am vegetarian, never suggest a recipe with meat in it."
- "Do not suggest I buy equipment to solve a consistency problem."
- "Always check the balance before recommending a purchase over $200."
- "Be gentle here. This one is loaded and I avoid it when pushed."
```

The last section is the one that pays off. It is the difference between an assistant that knows facts about your life and one that knows how to be useful in it. Add to it every time you find yourself giving the same caveat twice.
