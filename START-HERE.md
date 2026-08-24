# Start here

This folder is a personal operating system: a set of plain markdown files that hold your life context, which you and Claude both read and edit.

The point is that you stop re-explaining yourself. Claude reads the files at the start of every session, so it already knows what you are working on, how you like to be worked with, and what you decided last month. Nothing depends on chat memory.

Setup is about ten minutes, then a fifteen minute conversation that fills the whole thing in.

## 1. Put this folder somewhere synced

Anywhere works. `~/Documents/PersonalOS` is fine. Putting it in iCloud Drive or Dropbox means it is backed up and available on your phone.

Rename the folder to whatever you want.

## 2. Install the Claude desktop app

Download it from [claude.ai/download](https://claude.ai/download). You do not need a terminal and you do not need to install anything else.

This requires a **Pro or Max subscription**. The free tier does not include the part we need.

## 3. Open the Code tab and point it at this folder

The desktop app has three tabs at the top: Chat, Cowork, and Code.

**Use Code.** It is the one with direct access to your files. Chat cannot read them, and Cowork is built for a different kind of task.

In the Code tab, choose **Local**, click **Select folder**, and pick this folder.

## 4. Set the permission mode to "Accept edits"

There is a permission selector next to the send button. Set it to **Accept edits**.

This matters more than it sounds like it does. The default asks you to approve every individual change, which is sensible for code and miserable for editing your own notes. In Accept edits mode Claude makes the change and shows you what it did, and you can always look at the diff or ask it to undo.

If you would rather watch it work for the first session before trusting it, use Manual and switch over once you are comfortable.

## 5. Say "let's set this up"

That is it. Claude will read `CLAUDE.md`, find the setup interview, and walk you through it one question at a time.

It will ask what you are carrying right now, which parts of life need a home, how you want to be worked with, and when a weekly review would realistically happen. Then it writes all of that into the files and deletes the interview so it does not run again.

You can stop partway. Whatever you have covered gets written down.

## After that

Two habits, and only two:

- **Dump into `inbox.md` whenever.** Any thought, errand, link, or thing to look into. It is allowed to be messy, that is its job. Nothing else has to be tidy if this exists.
- **Do the weekly review.** Fifteen minutes, once a week. Type `/prompt weekly-review` and Claude runs it. This is the one ritual that makes the rest work.

Everything else is optional. The system is not graded on completeness and it does not require you to be perfect on any given day.

## A few things worth knowing

**`CLAUDE.md` is yours to edit.** It is the instructions Claude follows in this folder, and it loads automatically every session. When Claude does something in a way you do not like, do not just correct it in the moment, tell it to write the correction into the "How to work with me" section. That is the mechanism that makes it stop happening. This compounds: most of what makes a setup like this feel good after a few months is accumulated corrections.

**Anything you say in chat is temporary. Anything in a file is permanent.** If it matters, get it into a file.

**Delete this file once you are set up.**
