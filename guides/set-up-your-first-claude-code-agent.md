---
title: "Set Up Your First Claude Code Agent: A Daily Briefing in 30 Minutes (No Coding)"
description: "A step-by-step, no-jargon guide to installing Claude Code and building an agent that writes you a daily briefing on your schedule and priorities. No coding needed."
category: "guides"
publishedAt: "2026-06-15"
---

## What you're going to build

By the end of this guide you will have a working agent that reads your calendar and your priorities and writes you a short morning briefing: what today looks like, your meetings in order, what to focus on, and anything that is about to fall through the cracks. It takes about thirty minutes, and you will not write a single line of code.

### What an "agent" actually means here

Forget the science fiction. An agent is just a helper you give a goal to, that can read and write files and use a few tools you connect, like your calendar and your email. You tell it what you want in plain English. It does the work and hands you the result. The folder it works in becomes a small shared workspace where you and the agent collaborate: you keep your priorities there, it leaves its output there.

### What you need before you start

- A Mac (this guide uses Mac steps; Windows is similar).
- A paid Claude plan. Claude Code requires Pro, Max, Team, or Enterprise. The free plan does not include it. Pro covers everything in this guide, including scheduling.
- About thirty minutes.

That is it. No programming background required.

## Install Claude Code on your Mac

There are two ways in. Pick whichever you prefer. Most non-technical people should use the desktop app.

### Option A: The desktop app (easiest, no terminal)

1. Download the Claude desktop app from the official link: `https://claude.ai/api/desktop/darwin/universal/dmg/latest/redirect`
2. Open the downloaded file and drag the Claude app into your Applications folder.
3. Open Claude and sign in (see "Logging in the first time" just below).
4. At the top of the app you will see three tabs: Chat, Cowork, and Code. Click the Code tab. That is Claude Code. If clicking Code asks you to upgrade, you are on the free plan and need a paid one first.

No terminal required.

### Option B: The terminal install (one command)

If you are comfortable opening Terminal, this works too:

1. Open Terminal (press Command + Space, type "Terminal," hit Enter).
2. Paste this and press Enter:
   ```
   curl -fsSL https://claude.ai/install.sh | bash
   ```
3. When it finishes, fully quit Terminal and reopen it.
4. Type `claude` and press Enter to start.

### Logging in the first time

The first time you sign in, Claude opens your web browser and asks you to log in with your Claude account. Log in there, and you are sent back to the app, now signed in. Your login is saved securely, so you only do this once.

If the browser does not open on its own, the app shows you a link. Click it, or copy and paste it into your browser.

## Open your first project folder

Claude Code always works inside one folder at a time. That folder is your agent's home base, where it reads and writes files.

In the desktop app, the Code tab first asks you to pick an environment. Choose Local, so Claude works with the files on your Mac. Then click Select folder and either pick an existing folder or create a new one called `my-daily-briefing`.

If you are in Terminal instead, type these one line at a time:

```
cd ~/Desktop
mkdir my-daily-briefing
cd my-daily-briefing
claude
```

That makes a folder called `my-daily-briefing` on your Desktop and starts Claude Code inside it.

## Understanding permissions (the 2-minute version)

### What permissions are and why they exist

Think of Claude Code like a very capable assistant who always asks before doing anything that could matter. Permissions are the rules for when it asks and when it just goes ahead. There are three kinds of actions:

- Reading (looking at a file or searching) is always safe and never needs approval.
- Writing (creating or changing a file) is medium-risk and asks you first.
- Running commands (anything that acts on your computer) is the highest-risk and always asks first.

### The setting to start with: Ask permissions

In the Code tab you start in Ask permissions mode. It is the cautious setting: Claude shows you each change before it makes it and waits for you to approve, with an Accept and a Reject button on each one. Accept the things you expect (reading your calendar, writing your briefing); reject anything that looks off. Nothing happens without your okay.

In the terminal version this same cautious setting is called Default mode.

### When you trust it: Auto accept edits

After a few sessions, when you are comfortable with the kinds of changes Claude makes, you can switch to Auto accept edits mode, which stops asking about file changes but still checks before running commands. You change modes with the mode selector in the Code tab. In the terminal version you cycle modes by pressing Shift and Tab. Start in Ask permissions until you have the rhythm.

### Three things to never let your agent touch

You do not need to memorize anything technical. For a simple briefing agent you are only ever reading your calendar, reading a short priorities file, and writing a summary. None of that is risky. As a safety habit, if Claude ever asks to do any of these, reject it:

- Delete files (a command starting with `rm`).
- Read a file with "secret," "credentials," ".env," or "key" in its name (those hold passwords and keys).
- Run something that pipes the internet straight into your computer (a command with `curl` or `wget` followed by `| bash`).

In one line: start in Ask permissions mode, accept the reads (your calendar and priorities file), and reject anything that deletes files or touches secrets. That is all you need for this guide.

## Recipe 1: Your daily schedule and priorities briefing

Goal: every morning, get a short briefing that pulls today's calendar events, lines them up against your own priorities, and flags conflicts and what to focus on.

Prep, two pieces:

1. Connect your Google Calendar. Go to `claude.ai/customize/connectors`, click the Google Calendar connector, and sign in with your Google account. Connectors you add on claude.ai automatically become available inside Claude Code. (A connector lets Claude read that service on your behalf to answer your prompts; you can disconnect any connector anytime on that same page.)
2. Make a priorities file. The easiest way is to let Claude create it for you. In the Code tab, paste this:
   ```
   Create a file called priorities.md in this folder with these lines:
   Top goal this week: finish the Q3 plan.
   Don't drop: call the dentist, review the lease.
   Protect: no meetings before 10am.
   ```
   Claude writes the file in the right place. In Ask permissions mode it asks before creating it, so click Accept. Change those lines to your real priorities anytime, either by asking Claude or by opening the file. That is the whole system. The folder is now a shared workspace: you keep the priorities, the agent reads them.

Copy-paste prompt (paste this into the Code tab while you are in the folder that holds `priorities.md`):

```
Look at my Google Calendar for today and read the file priorities.md in this
folder. Write me a short morning briefing: first a one-line summary of how
today looks, then my meetings in time order with start times, then which of my
priorities I can realistically advance today, and finally flag any conflicts,
double-bookings, or priorities that have no time blocked for them. Keep it
under 200 words, plain and skimmable. No filler.
```

Run it once to confirm the output looks right and that both your calendar and your file are being read.

One wrinkle for later: scheduling this recipe to run on its own has a catch, because the priorities file lives on your Mac. See "Make it run every morning" below.

## Recipe 2: Your morning unread-email digest

Goal: a two-minute morning digest of what landed overnight, sorted into what needs a reply, what is worth knowing, and what you can ignore.

Why this one: highest value, lowest setup. One connector, no files.

Prep: connect Gmail. Go to `claude.ai/customize/connectors`, click the Gmail connector, and sign in. That is it.

Copy-paste prompt:

```
Search my Gmail for unread messages from the last 24 hours. Give me a digest in
three groups: (1) Needs a reply from me, (2) Worth knowing, no action,
(3) Newsletters or promotions I can ignore. For each item in group 1, one line:
who it's from and what they want. Keep the whole thing under 250 words. Do not
send anything.
```

Optional, pre-draft your replies. Add this line to the prompt:

```
For the top 3 in group 1, also create draft replies in Gmail.
```

Claude writes the drafts and leaves them in your Gmail Drafts folder. Read what it wrote and hit send yourself.

One limit to state plainly: Claude can search, read, and draft email, but it cannot send email on your behalf. Every email is sent manually by you from Gmail. This is a built-in safety limit, not a setting you can change.

## Make it run every morning

Running the prompt by hand is fine. But the whole point of an agent is that it does the work without you. Claude Code can run your briefing on a schedule.

### The three ways to schedule, and which to pick

| If you want | Use this | The catch |
| --- | --- | --- |
| It to run even when your laptop is closed | A cloud routine | Cannot read files on your Mac; works with connectors only (Calendar, Gmail, Drive). Runs at most once an hour, with a daily limit set by your plan. |
| It to read files on your Mac | A Desktop scheduled task | Only runs while the app is open and the computer is awake. |
| To just test the idea for a few minutes | `/loop` | Stops when you close the session. |

For most people the answer is a cloud routine, because it just works in the background. The email digest (Recipe 2) is perfect for this, since it only needs Gmail.

### Setting up a daily routine with one line

In the Code tab, type a line like:

```
/schedule every weekday at 7am, write my morning email digest
```

Claude walks you through the details and saves it. You can see, pause, or delete your routines at `claude.ai/code/routines`, or by typing `/schedule list`.

A couple of honest notes. Scheduling is in research preview right now, so the exact limits can change; today a routine runs at most once an hour, with a daily cap that depends on your plan. A daily briefing is one run a day, so you have plenty of room. And a cloud routine runs on its own with no approval prompts, and it can use everything you connect to it, so keep its instructions tightly scoped. For the email digest, that is why the prompt ends with "Do not send anything."

### The catch: scheduled agents can't read your Desktop files

A cloud routine runs on Anthropic's servers, not on your Mac, so it cannot see `priorities.md` sitting on your Desktop. Two simple fixes:

- Keep `priorities.md` in Google Drive and add the Google Drive connector. Then the cloud routine can read it.
- Or run Recipe 1 manually each morning with one pasted line, which always sees your local file, and use a cloud routine only for the email digest.

## When something goes wrong

A few things trip up first-timers. None are serious.

- It cannot see your calendar or email. The connector was not added or not signed in. Go back to `claude.ai/customize/connectors` and confirm it shows as connected. If you do not see the connector you want, it may not be available on your plan or in your region.
- It will not log you in. In the desktop app, quit Claude, reopen it, click Code, and sign in again. In the terminal version, run `claude auth login` to restart the browser sign-in.
- "command not found" after a terminal install. Fully quit and reopen Terminal, then try `claude` again. The install adds Claude to your path, but only a fresh terminal window picks it up.

## The bigger picture

The daily briefing is small on purpose. The real skill you just built is bigger: handing a goal to an agent, giving it the right access, and trusting it inside safe limits. That is the same pattern behind every serious use of these tools, from a one-person morning routine to a team running real work through a shared workspace where people and agents collaborate side by side.

Start with the briefing. Once it is landing in your inbox every morning, you will see the next thing worth handing off. Then hand that off too.

