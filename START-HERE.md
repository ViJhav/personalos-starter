# Start here

**If someone sent you this folder, this file is the one to read first.** Ten minutes of setup, then a fifteen minute conversation that fills the whole thing in.

This folder is a personal operating system: a set of plain markdown files that hold your life context, which you and Claude both read and edit.

The point is that you stop re-explaining yourself. Claude reads the files at the start of every session, so it already knows what you are working on, how you like to be worked with, and what you decided last month. Nothing depends on chat memory.

## 1. Put this folder somewhere synced

Anywhere works. `~/Documents/PersonalOS` is fine. Putting it in iCloud Drive or Dropbox means it is backed up and available on your phone.

Rename the folder to whatever you want. Keep everything inside it together — the files reference each other.

## 2. Install the Claude desktop app

Download it from [claude.ai/download](https://claude.ai/download). You do not need a terminal and you do not need to install anything else.

This requires a **Pro or Max subscription**. The free tier does not include the part we need.

## 3. Open Claude Code and point it at this folder

The desktop app has a **toggle in the top left** that switches between Chat and Code.

**Switch it to Code.** That is the one with direct access to your files. Chat cannot read them.

Then:

- Click **New** to start a session.
- Choose **Local**, not cloud. Local means the files stay on your computer.
- Next to the message box there is an option to **select a folder**. Pick **this folder** — the top-level one, the one that has `START-HERE.md` and `CLAUDE.md` sitting directly inside it. Not `areas/`, not `projects/`, and not the folder that contains it.

The app keeps a list of every folder you have opened, and it grows each time you add one. Picking the wrong entry from that list is the single most common way this goes wrong, so check the name before you start.

## 4. Set the permission mode to "Accept edits"

There is a permission selector next to the send button. Set it to **Accept edits**.

This matters more than it sounds like it does. The default asks you to approve every individual change, which is sensible for code and miserable for editing your own notes. In Accept edits mode Claude makes the change and shows you what it did, and you can always look at the diff or ask it to undo.

If you would rather watch it work for the first session before trusting it, use Manual and switch over once you are comfortable.

## 5. Say "let's set this up"

Type exactly that. Claude will read `CLAUDE.md`, find the setup interview, and walk you through it one question at a time.

It will ask what you are carrying right now, which parts of life need a home, how you want to be worked with, and when a weekly review would realistically happen. Then it writes all of that into the files and deletes the interview so it does not run again.

You can stop partway. Whatever you have covered gets written down.

### If it seems clueless

If the reply is generic, or it asks what you want to work on instead of starting the interview, it is almost certainly pointed at the wrong folder. Ask it:

> Which files did you load at the start of this session?

It should name `CLAUDE.md`, `README.md`, and `current-state.md`. If it names none of those, or says the folder is empty, go back to step 3 and select the folder that has `START-HERE.md` directly inside it.

If it does name them and still did not start the interview, just say: *run the first-time setup interview in CLAUDE.md.*

## After that

Two habits, and only two:

- **Dump into `inbox.md` whenever.** Any thought, errand, link, or thing to look into. It is allowed to be messy, that is its job. Nothing else has to be tidy if this exists.
- **Do the weekly review.** Fifteen minutes, once a week. Type `/prompt weekly-review` and Claude runs it. This is the one ritual that makes the rest work.

Everything else is optional. The system is not graded on completeness and it does not require you to be perfect on any given day.

## Where your data goes

Worth knowing before you put your life in here.

- **Your files stay on your computer.** Choosing Local means nothing is uploaded or synced to Anthropic. Claude reads and writes them in place.
- **But the conversation is not local.** Claude Code is not Word or Excel — the model runs on Anthropic's servers. Anything you type, plus the parts of your files Claude actually reads to answer you, is sent there to be processed. It reads what it needs rather than shipping whole files, but treat anything you discuss as having left your machine.
- **Transcripts are saved locally** in `~/.claude/projects/`, and delete themselves after 30 days. You can delete them yourself sooner.
- **Opt out of training** in the Claude app's privacy settings if you have not already. Do this before the setup interview, not after.
- **Legal caveat worth taking seriously:** AI chat history has been treated as discoverable, so there is no reliable expectation of privacy over it. If you are involved in a dispute, a claim, or anything that could end up in litigation, keep it out of this vault and out of these conversations. Everything else is fair game.

Anthropic's own description of what leaves your machine: <https://code.claude.com/docs/en/data-usage>

## A few things worth knowing

**`CLAUDE.md` is yours to edit.** It is the instructions Claude follows in this folder, and it loads automatically every session. When Claude does something in a way you do not like, do not just correct it in the moment, tell it to write the correction into the "How to work with me" section. That is the mechanism that makes it stop happening. This compounds: most of what makes a setup like this feel good after a few months is accumulated corrections.

**Anything you say in chat is temporary. Anything in a file is permanent.** If it matters, get it into a file.

**Delete this file once you are set up.**
