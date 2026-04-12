---
id: "ai-201-day-08"
type: "course-lesson"
course: "ai-201"
course_title: "AI 201: Build Your AI System"
week: 2
day: 8
day_of_week: "mon"
lesson_type: "lesson"
title: "Cowork Automation: Scheduled Tasks"
subject: "AI that works while you sleep. Literally."
source_path: "course-2/week-2/day-08-mon.md"
---

Everything you've built so far has one thing in common: you had to start it. You opened a tool, typed a prompt, reviewed the output. You were the engine.

Today that changes.

Claude Cowork has a feature called `/schedule` that lets you set tasks to run automatically — hourly, daily, weekly, on specific weekdays, or on-demand. You tell it what to do and when, and it just... does it. Without you opening anything. Without you remembering. Without you being involved at all.

This is the moment Cowork stops being a smart assistant and starts being a system.

## How /schedule works

In any Cowork session, type `/schedule` followed by what you want and when. That's it. No setup wizard, no complicated configuration.

Here are real examples:

**Daily morning brief:** `/schedule` every weekday at 7:30am — "Check my Gmail inbox, summarize any emails that arrived overnight, flag anything urgent, and save the summary as a markdown file on my Desktop called today's-brief.md."

**Weekly expense report:** `/schedule` every Friday at 4pm — "Go through the Receipts folder on my Desktop, extract vendor names, amounts, and dates from every receipt added this week, compile them into an Excel spreadsheet with categories and totals, and save it to my Expense Reports folder."

**Friday presentation auto-gen:** `/schedule` every Friday at 9am — "Read the team-updates.md file in my Projects folder, create a 5-slide PowerPoint summarizing this week's progress, blockers, and next week's priorities, and save it to the Presentations folder."

Notice the pattern. You're describing an end state, not giving step-by-step instructions. "Here's what I need, here's when I need it, here's where to put it." Cowork figures out the how.

## Connected tools via MCP

Here's where it gets really interesting. Cowork can connect to external services through something called MCP connectors — think of them as bridges between Claude and the tools you already use.

Available connectors include Google Drive, Gmail, Google Calendar, Slack, DocuSign, Jira, WordPress, Microsoft 365, and more. The list is growing.

What this means practically: your scheduled task isn't limited to files on your computer. You can set up a workflow that reads your Google Calendar every morning and prepares a briefing doc with background on each person you're meeting that day. Or one that monitors a shared Google Drive folder and summarizes any new documents added by your team.

To connect these, go to Settings in Claude Desktop and look for the MCP integrations section. Each connector has a simple authorization flow — you sign in once, grant permissions, and you're connected.

## The important limitation

Here's the catch, and I'm going to be upfront about it: scheduled tasks only run when your computer is awake and the Claude Desktop app is open.

There's no cloud server running your tasks. It's all local. If your laptop goes to sleep at 2am and you have a task scheduled for 6am, it won't run until you open your laptop and Claude Desktop is active.

For most people this means: keep your computer open during work hours, or set it not to sleep. Not a dealbreaker, but worth knowing so you're not confused when a task doesn't fire.

## Why this matters

Think back to your Day 1 audit. How many of those green-circle tasks — the ones AI could handle 80%+ of — are recurring? Things you do every day, every week, every month?

That's your automation surface. And `/schedule` turns those from "tasks I do with AI help" into "tasks AI does and I review the output."

That's a fundamentally different relationship with your work. You're not delegating in real time anymore. You're building systems that run independently. The morning brief is waiting when you sit down. The expense report is done before you think about it. The presentation draft exists before the meeting is even on your mind.

This is what it means to be AI-powered instead of AI-assisted.

## Today's exercise: set up one real scheduled task (15 minutes)

Open Claude Desktop and Cowork. Think about your week. What's one task you do regularly that follows a predictable pattern? Something with clear inputs and a clear output format.

Some ideas from your audit:
- Morning email summary
- Weekly status report compilation
- Daily calendar briefing
- End-of-week file organization
- Recurring data entry or formatting

Set it up with `/schedule`. Be specific about what you want, when you want it, and where the output should go. Then let it run at least once and review the result.

Don't try to automate everything today. One task. Get it right. Trust it. Then build from there.

## What's coming tomorrow

Tomorrow we're chaining AI steps together — where the output of one task becomes the input for the next. Research → summarize → draft → refine, all in one flow. That's where you start building workflows that would take you hours but take AI minutes.

**The best AI system isn't the one you use the most. It's the one that works without you touching it at all.**
