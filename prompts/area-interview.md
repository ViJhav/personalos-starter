# Area interview

The deep pass that fills each area README in depth, in the user's own words. The quick setup (`prompts/setup.md`) makes the vault usable; this makes it good. Run with `/prompt area-interview`. Safe to run any number of times: each run picks up wherever the question file says things stand.

**Reads:** `areas/readme-interview.md` (the question file), every `areas/<name>/README.md`, `current-state.md`, `CLAUDE.md` § How to work with me.
**Writes:** `areas/readme-interview.md`, and an area README only after the user has seen its draft.

## Why a file, not a chat

Twelve live questions is fine. Fifty is not: answering them inline is exhausting, people rush, and the answers get thin. So this interview is **asynchronous**. You write a question file; the user fills it in over days, in fragments, whenever; you follow up; you draft. Nothing lands in a README until they have answered and seen the draft, which also means every drafted line traces back to their own words. Never invent a fact to fill a gap; leave it as a prompt instead.

## The flow, per area

Each area's heading in the question file carries its status. **This marker is the only progress record**, so update it every time a stage finishes:

1. `## Health ⏳ ROUND 1`: questions written, waiting on answers.
2. `## Health 💬 ROUND 2`: Round 1 answered, follow-ups written, waiting on answers.
3. `## Health 📝 READY TO DRAFT`: Round 2 answered (or skipped).
4. `## Health ✅ DRAFTED → areas/health/README.md (YYYY-MM-DD)`: draft shown, approved, written.

Areas move independently. Health can be drafted while Money is still on Round 1.

## Each run

1. **Read the question file** if it exists, plus every area README.
2. **Report where things stand** in at most five lines: which areas are at which stage, and what you will do now.
3. **Do the next thing for each area that has one:**
   - **No question file yet:** create `areas/readme-interview.md` (format below) with a Round 1 section for every area folder that exists. Ask which area they want to start with, and suggest the one that feels loudest.
   - **An area folder with no section in the file** (created since): add a Round 1 section for it.
   - **⏳ ROUND 1 with answers filled in:** read them, write a `### Round 2 follow-ups` subsection under that area, set the marker to 💬. If the answers left no real gaps, say so and go straight to 📝.
   - **💬 ROUND 2 with answers filled in:** set the marker to 📝.
   - **📝 READY TO DRAFT:** draft the README in chat, show it, and ask for corrections. Write it only once they approve, then set ✅.
   - **Unanswered sections:** leave them. Do not nag. Mention them once in the status line.
4. **Never re-ask** an answered question, and never regenerate a section that already has answers in it. If a question is answered blank, treat it as "skip".

## Question file format

```markdown
# Area interview

_Answer inline under each **A.** Bullet fragments are fine. Leave blank anything you'd rather skip. Where the vault already knows something it says **Vault already has:**, so just confirm or correct. No time pressure: fill a bit whenever, then tell Claude "continue the area interview"._

---

## Health ⏳ ROUND 1
**Vault already has:** <one or two lines from current-state.md and the existing README, or "nothing yet">

- **Q. Current state:** ...
  **A.**

### Round 2 follow-ups
_(added after Round 1 is answered)_
```

**"Vault already has" is required on every section.** It is what stops the user retyping what they already told you during setup. Pull it from `current-state.md`, the area's existing README, and anything else already in the vault.

## Round 1 questions

Every area gets these six, worded for the area:

- **Current state:** where does this part of life stand right now? How do you feel about it?
- **Active concerns:** anything live right now: a decision, a problem, something overdue, something you keep meaning to do?
- **Goals:** what are you moving toward here over the next 6–12 months? Anything longer-term?
- **Standards / norms:** what does "good" look like here, the bar you actually hold yourself to (which may differ from the one you'd say out loud)? Any routines or rules you follow?
- **Key facts:** the things you look up over and over: providers, plans, sizes, model numbers, who to call. **Never passwords, account numbers, or ID numbers.**
- **Useful context for an assistant:** how should I behave here? Things to always check first, never suggest, be gentle about, or push on. _This is the most valuable question in the file; say so in the question._

Then add two to four questions specific to that area. Starting points (adapt; skip any that don't fit what they've said):

- **Health:** current routine and what gets in its way · providers and recurring appointments · conditions or medications worth knowing about (only what they want here) · how hard to push on habits
- **Money:** how money is organized (accounts by type, no numbers) · what system tracks spending · big goals or worries · shared expenses and who handles what · rules for purchases
- **Home:** rent or own, and what that means for upkeep · recurring chores and how often · open projects or repairs · who does what, if shared
- **Relationships:** the people who matter most and anything an assistant should know about them · important dates · what being a good partner, friend, or family member looks like to you · anything to handle gently
- **Learning:** what you're studying and why · current commitments and deadlines · how you study best, and what derails it
- **Travel:** how you like to travel · default packing and prep habits · loyalty programs (names only) · upcoming trips
- **Work-adjacent:** what belongs here and what deliberately doesn't (work itself usually stays out) · where you're heading professionally
- **Hobbies:** what you do and how often · gear owned or wanted · what keeps you from doing more of it
- **Food:** dietary constraints, strict or soft · cooking habits · groceries and favourite places

Finish the file with:

```markdown
## Anything else
- **Q. Other areas or context** that don't fit above but an assistant should know?
  **A.**
```

## Round 2: follow-ups

Round 2 is short and specific. Three to six questions, aimed at:

- **Gaps:** something Round 1 implied but didn't say. "You mentioned a physio, what's the injury and is it still active?"
- **Contradictions:** two answers that don't fit together, or an answer that disagrees with the vault. Quote both and ask which is current. Never quietly pick one.
- **Anchors:** dates, names, amounts, or frequencies that turn a vague answer into something usable. "'Every so often' means monthly? quarterly?"
- **Making a norm actionable:** turn "I want to be better about X" into what an assistant should actually do. "Should I remind you, or only mention it when it comes up?"
- **Placement:** where a fact belongs when it could live in two areas. One home per fact.

Open the subsection with a line on why these, e.g. _"Round 1 was rich; these close gaps on dates and one contradiction."_

## Drafting

Use the template in `areas/README.md`. Keep only the sections that have real content. Put the "Useful context for an assistant" answers into **Useful context for Claude**, phrased as rules you will follow. Preserve their wording where it carries tone or intent.

If the area README already has content, **merge**: keep everything there, add what's new, and flag anything that conflicts rather than overwriting it.

Show the draft in chat with a one-line note on anything you left out and why. On approval, write it, set the ✅ marker with today's date, and say which area is next.
