---
id: "claude-cowork-day-05"
type: "course-lesson"
course: "claude-cowork"
course_title: "Claude Cowork"
week: 1
day: 5
lesson_type: "lesson"
title: "Connectors — Connect the Tools You Already Use"
subject: "Claude just read my email and pulled the right file from Drive"
source_path: "claude-cowork/week-1/day-05.md"
---

So far, Cowork has been working with files on your local machine.
That's useful — but most of your actual work lives elsewhere.
In Gmail. In Google Drive. In Slack. In your calendar.

Connectors are how Cowork reaches those tools.

---

## What a connector actually is

A connector is a structured, two-way integration between Cowork
and an external service. When you install a Gmail connector,
Cowork can read your emails, search your inbox, and draft
replies — not by opening a browser and clicking around, but
through a direct, precise API connection.

This matters because it makes Cowork more reliable and more
accurate on tasks involving those tools. When Cowork uses a
connector, it's talking directly to the service. When it doesn't
have a connector, it has to fall back to browser control or
screen interaction — which is slower and less precise.

The rule Cowork follows internally: **connector first, browser
second, screen last.** We'll cover what that means in practice
in Lesson 9.

---

## Where to find connectors

The connector directory lives at
[claude.com/connectors](https://claude.com/connectors).

There are 200+ connectors across 9 pages, organized by category:
Productivity, Communication, Financial Services, Sales & Marketing,
Data, and more. Most are community-built and reviewed by Anthropic.
Each connector has its own third-party terms — Anthropic doesn't
own your connected data, the connector provider does. Worth a
quick read for anything involving sensitive information.

---

## The connectors most knowledge workers should set up first

You don't need all 200. Start with the ones that connect to
where your work actually lives.

**Gmail** — Read, search, and draft emails. Cowork can check
your inbox for urgent messages, draft replies based on context,
summarize threads, and flag what needs your attention.

**Google Drive** — Read, search, and create documents and
spreadsheets. Cowork can pull files from Drive, synthesize
across multiple documents, and save outputs back to Drive.

**Slack** — Available on Team and Enterprise plans. Cowork can
read channels, search conversations, draft messages, and
summarize what you missed.

**Zoom** — Added in the April 2026 GA launch. Cowork can pull
meeting summaries, transcripts, and action items from Zoom calls.

Those four cover the majority of where knowledge work actually
happens. Install the ones that apply to your stack and skip
the rest for now.

---

## How to install a connector

1. Go to claude.com/connectors
2. Find the connector you want — use the category filter to
   narrow it down
3. Click the connector to open its detail page
4. Click Install
5. Complete the OAuth authorization flow — you'll be redirected
   to the service (Google, Slack, etc.) to grant permission
6. Return to Cowork — the connector is now active

The whole process takes about two minutes per connector.

---

## What Cowork can do once Gmail is connected

Here's a real task to try immediately after installing Gmail:

```
Check my Gmail inbox for emails received in the last 24 hours.
For each one, give me: sender, subject, time received, and a
one-sentence summary of what it's about.

Then tell me which ones look like they need a response today,
and which can wait.

Show me your assessment before doing anything else.
```

Or a more powerful version:

```
I need to respond to the three most important emails in my
inbox from the last 48 hours. Find them, summarize each one,
and draft a reply to each based on the context in the email
thread. Show me all three drafts before sending anything.
```

Cowork will read your actual inbox, assess urgency, and write
replies that reflect your context — because it has your
about-me.md and your writing style file loaded.

---

## An important note on permissions

When you install a connector, you're granting that connector
access to the relevant service. For Gmail, that means Cowork
can read your emails. For Drive, it can read your files.

A few things to know:

You control which connectors are active. You can disable or
remove any connector at any time in Cowork Settings.

On Enterprise plans, admins can control which connectors are
available to which teams through per-tool connector controls.

If you're working with sensitive data — legal documents,
financial records, health information — think carefully about
which connectors you enable and which files you give Cowork
access to. Cowork is not yet certified for HIPAA, FedRAMP, or
financial services regulated workloads.

---

## What happens when a connector fails

Connectors occasionally have issues — service outages,
expired auth tokens, API changes. When a connector is
unavailable, Cowork doesn't stop. It falls back to browser
control automatically and tries to complete the task through
your browser instead.

This fallback is less precise than a connector, but it means
Cowork keeps working even when integrations have hiccups. You
may notice Cowork opening a browser tab to accomplish something
it would normally do through a connector — that's the fallback
in action.

---

## You're connected. Now let's automate.

Connectors are the bridge between Cowork and your digital
work environment. With Gmail and Drive connected, Cowork has
access to the actual substance of your work — not just the
files you've manually dropped into a folder.

Next lesson: Skills. How to teach Cowork your specific processes
so you never have to explain them again.
