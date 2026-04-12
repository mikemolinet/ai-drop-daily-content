---
id: "claude-chatbot-to-coworker-day-06"
type: "course-lesson"
course: "claude-chatbot-to-coworker"
course_title: "Claude: From Chatbot to Coworker"
week: 2
day: 6
lesson_type: "lesson"
title: "Connectors: Your Tools, Connected"
subject: "Claude just read my email and pulled the right file from my Drive"
source_path: "course-3/week-2/day-06.md"
---

Welcome to Week 2. If Week 1 was about what Claude can do inside a chat window, this week is about what happens when you let Claude out of the box.

Today we connect Claude to the tools you already use. And this is where things get interesting.

## Connectors: the 2-minute explanation

Connectors let Claude access your other apps. Gmail. Google Drive. Slack. Notion. Asana. Calendar. Salesforce. Stripe. Dozens more.

Once connected, Claude doesn't just answer questions from what it knows. It answers from what YOU know - your emails, your docs, your project boards, your messages.

"Find the email thread where we discussed the vendor contract" - and Claude searches your actual Gmail and finds it.

"What did the team decide about the timeline in yesterday's Slack discussion?" - and Claude reads the actual Slack thread.

"Summarize the meeting notes from last week's product review in my Drive" - and Claude opens the actual doc.

This is the moment Claude goes from "impressive chatbot" to "informed collaborator." It's not guessing what your work looks like anymore. It's looking at it.

## Setting up your first connector

This takes about 60 seconds per tool.

**Step 1:** In Claude, click "Search and tools" (bottom left of the chat window), then "Add connectors." Or go directly to claude.ai/directory.

**Step 2:** Browse the directory. It's organized into:
- **Web connectors:** Cloud services like Gmail, Google Drive, Slack, Notion, Asana, Linear, Stripe
- **Desktop extensions:** Local tools through the Claude Desktop app

**Step 3:** Click "Connect" on the tool you want. You'll be redirected to that service's login page.

**Step 4:** Sign in with your existing credentials and grant permissions. Review what Claude is asking for - permissions are scoped to what the connector actually needs.

**Step 5:** Go back to Claude and test it. "Can you access my Gmail?" or "Search my Google Drive for the Q4 budget."

That's it. No API keys. No configuration files. No technical setup.

## What you can actually do with connected tools

Let me give you real examples, organized by the tools most of our audience uses.

**Gmail + Calendar:**
- "What meetings do I have tomorrow? For each one, find the most recent email thread with that person and summarize where we left off."
- "Find all emails from [client name] in the last month. What are the open questions I haven't responded to?"
- "Draft a follow-up to the last email from Sarah about the project timeline. Reference what she specifically asked for."

**Google Drive:**
- "Search my Drive for anything related to the Henderson proposal. Summarize what we have so far."
- "Find our brand guidelines doc and use them to review this draft I'm about to paste in."
- "Compare the Q3 and Q4 sales reports in my Drive. What changed?"

**Slack:**
- "What were the key decisions in #product-team this week?"
- "Find any messages mentioning the launch date and summarize the current status."
- "Draft a response to the latest question in #client-support."

**Project management (Asana, Linear, Jira):**
- "What are my highest priority tasks due this week?"
- "Summarize the status of the website redesign project."
- "Create a new task for reviewing the Q4 budget proposal."

The pattern: instead of opening five tabs and context-switching between apps, you ask Claude one question and it pulls from everywhere.

## Security: the question everyone asks

"Wait - I'm giving AI access to my email?"

Fair question. Here's how it works:

**Claude sees what you see.** Connecting your Gmail doesn't give Claude access to anyone else's inbox. Only yours. Same with Drive, Slack, everything.

**Permissions are scoped.** Each connector asks for specific permissions. You can see exactly what Claude can and can't do with each connected tool. Some are read-only. Some allow actions (like creating a task in Asana). You choose.

**Revocable at any time.** Disconnect any service through Claude's settings or through the service's own security settings. It's not permanent.

**Your conversations stay private.** What you discuss with Claude in a connected chat is your conversation. It's not shared with the connector services.

Should you connect everything on day one? No. Start with one tool - probably Gmail or Google Drive, since most people use those daily. See how it works. Get comfortable with it. Add more later.

## The connector that changes everything

If you connect only one tool, make it Google Drive (or whatever you use for document storage).

Here's why: Drive is where your knowledge lives. Meeting notes, proposals, research, strategy docs, client briefs. All of it sitting in folders you probably can't even navigate efficiently anymore.

Connecting Drive means Claude can search all of it instantly. "Find everything we've written about customer churn" becomes a 10-second answer instead of 20 minutes of searching through folders.

Pair that with a Project (Day 3) and you have Claude that knows your standing context AND can search your entire document library. That combination is powerful.

## Try this today

Connect one tool. Just one. The one you open most often at work.

Then ask Claude a question that requires information from that tool. Not a test question - a real one. Something you'd normally have to go look up manually.

Notice how much time you just saved.

**Connectors turn Claude from "smart assistant who doesn't know your business" into "smart assistant who can see everything you can see." Start with one tool and expand from there.**
