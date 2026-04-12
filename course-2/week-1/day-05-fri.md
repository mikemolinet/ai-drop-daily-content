# Subject: Meet the AI that actually does your work. On your computer. In your files.

Everything we've built this week — custom instructions, purpose-built assistants, prompt libraries — they all share one limitation. You're still the middleman. You ask AI a question, it gives you an answer, and then *you* do something with that answer. Copy it. Paste it. Format it. Save it.

Today that changes.

I want to introduce you to Claude Cowork. And I'm not being dramatic when I say this might be the single biggest "aha moment" of this entire course.

## What Cowork actually is

Cowork is a feature inside the Claude Desktop app that turns Claude from a chatbot into a desktop agent. Instead of chatting back and forth, you point it at a folder on your computer, describe what you want done, and it does it. Directly. In your files. No uploading. No downloading. No copy-pasting.

Think about what that means.

You say: "Organize my Downloads folder by file type, rename everything with clean dates, and create a summary of what you moved." And it does that. It reads your files, creates new folders, moves things around, and writes you a report — all while you watch.

You say: "Read these six meeting transcripts and build a spreadsheet tracking every action item, who owns it, and the deadline." It opens those files, reads them, creates an Excel workbook with real formulas and formatting, and saves it wherever you want.

This is not chat. This is work.

Anthropic calls it "Claude Code for non-developers." Developers have had AI agents writing and editing code for over a year now. Cowork brings that same concept to everyone else. Point it at files. Describe the end state. Let it figure out the steps.

## How to set it up (~5 minutes)

You need three things:

1. **The Claude Desktop app.** Available for macOS and Windows. Download it from [claude.ai/download](https://claude.ai/download). This is not the website — it's a separate app that runs on your computer.

2. **A Claude Pro plan at minimum** ($20/month). This gives you access to Cowork, but with limited usage. For real, daily use, you'll want **Claude Max** ($100/month for 5x usage, or $200/month for 20x). I know that sounds steep. By tomorrow's lab, you'll understand why people happily pay it.

3. **Grant folder access.** When you start a Cowork session, Claude asks which folder it can work in. Start small. We'll talk about why in a minute.

That's it. No plugins. No API keys. No terminal commands.

## The exercise: your first Cowork task (~15 minutes)

Here's what we're going to do. This is simple on purpose — I want you to feel the difference, not get overwhelmed.

**Step 1:** Find a messy folder. Your Downloads folder is perfect. Or any folder with a mix of files you don't care deeply about. (This part matters. Read the safety section below before you pick a folder with anything irreplaceable.)

**Step 2:** Open the Claude Desktop app. Start a new Cowork session and point it at that folder.

**Step 3:** Type this (or something close to it):

> Look through this folder. Organize the files into subfolders by type (documents, images, spreadsheets, etc.). For anything older than 6 months, put it in an "Archive" subfolder. Then create a markdown file called "Organization Report" that lists everything you moved and why.

**Step 4:** Claude will show you a plan before it executes. **Read the plan.** Make sure it looks right. Then approve it.

**Step 5:** Watch it work.

That's it. That's the moment. You'll see files moving, folders being created, a report being written — all happening directly on your computer. No upload. No download. No copy-paste.

If you felt something just shift in your brain — "wait, it can just *do things* on my computer?" — that's the reaction everyone has. That's why this is Day 5.

## What else it can do

File organization is just the starting point. Here's what Cowork handles:

- **Excel workbooks** with real formulas, formatting, and multiple sheets. Not a CSV. An actual .xlsx that opens in Excel looking professional.
- **PowerPoint presentations** with themes, charts, and proper layouts.
- **Word documents** with headers, tables, and formatting.
- **Research synthesis** — give it 10 PDFs and ask it to identify themes, flag contradictions, and produce a structured summary.
- **Web search** — it can research topics online and bring findings back into your documents.
- **Cross-app workflows** — analyze data in a spreadsheet, then build a presentation from the results, all in one session.

Tomorrow we'll build three real workflows using these capabilities. Today is about understanding what's possible.

## The safety talk (please actually read this)

I need to tell you about Nick Davydov.

Nick asked Cowork to organize his wife's desktop. Reasonable request. Cowork made a plan, he approved it, and it started working. At some point, it needed to delete what looked like temporary files. He granted delete permission.

Cowork ran a terminal command — `rm -rf` — on the family photo directory. 15,000 photos. Fifteen years of memories. Gone.

Here's the critical detail: terminal deletions on macOS bypass the Trash. There is no "undo." The files don't go to a recycle bin. They're just gone.

Nick's family only recovered those photos because iCloud retains deleted files for 30 days and Apple Support helped them restore. If they hadn't been syncing to iCloud, those photos would be permanently lost.

This is not a reason to avoid Cowork. It's a reason to use it with your eyes open. Here are the rules:

1. **Start with folders you don't care about.** Downloads. Old project folders. Test directories. Build trust before you point it at anything important.
2. **Always read the plan before approving.** Claude shows you what it intends to do. Actually read it.
3. **Never grant delete permissions on folders with irreplaceable files.** If it asks to delete things and you're working in a folder with photos, financial records, or anything you can't recreate — say no.
4. **Start read-only.** You can give Cowork read-only access first to see what it *would* do, then escalate permissions once you're comfortable.

Cowork is powerful. Power requires respect.

## The honest limitations

I don't want to oversell this. Here's what you should know:

- **No memory between sessions.** Every time you start a new Cowork session, it starts fresh. It doesn't remember what it did yesterday. (This is likely to improve, but it's the reality today.)
- **Your computer must stay awake.** Sessions die if your computer sleeps or the app closes. There's no cloud execution. If you start a big task, keep your laptop plugged in with the lid open.
- **It burns through tokens fast.** Cowork uses dramatically more of your usage allowance than regular chat. This is why the Max plan exists — Pro plan users will hit limits quickly.
- **It's still a "research preview."** Anthropic launched Cowork in January 2026. It works well, but it's early. You'll hit rough edges.
- **Single-user only.** No sharing sessions with teammates. No collaboration features yet.

None of these are dealbreakers. All of them are worth knowing before you build your workflow around it.

## What's coming tomorrow

Tomorrow is lab day. We're going to build three real Cowork workflows that you'll actually keep using after this course:

1. Turn messy meeting notes into a formatted report.
2. Process a folder of receipts or documents into a structured spreadsheet with real formulas.
3. Create a presentation from an outline with proper formatting.

Each one is something you'll reach for again next week. And the week after that.

Make sure you've done today's exercise before tomorrow. You want to walk into the lab already comfortable with how Cowork feels.

**Chat answers your questions. Cowork does your work. Once you feel that difference, you don't go back.**
