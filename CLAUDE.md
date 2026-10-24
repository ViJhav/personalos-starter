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

_This section is empty on purpose. The setup fills it in, and it should keep growing over time. Whenever you get a correction about tone, pace, format, or how much to check in, that is a candidate to write down here so it stops needing to be repeated._

_Setup status: run /prompt setup to check what is still open. It only asks about what is missing._

## Setup

Setup lives in `prompts/setup.md` (the quick interview) and `prompts/area-interview.md` (the deep pass for each area). Both work out from the files what is already done and only ask about the rest, so they are safe to rerun and to stop halfway.

- If the user's message is any kind of setup or getting-started request ("let's set this up", "continue setup", "hi", "what do I do now", "what is this"), run `prompts/setup.md`.
- If `current-state.md` is still the template and their message is a real task, do the task, then offer setup once, in one line, at the end. Do not answer as though you already know them: say plainly there is nothing about their life in the vault yet, rather than producing a generic answer that reads as the tool being broken.
- "Continue the area interview" (or similar) runs `prompts/area-interview.md`.
