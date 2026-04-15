---
id: "claude-cowork-day-10"
type: "course-lesson"
course: "claude-cowork"
course_title: "Claude Cowork"
week: 2
day: 10
lesson_type: "lesson"
title: "Your Full System — Putting It All Together"
subject: "You now have more AI working for you than most people will ever set up"
source_path: "claude-cowork/week-2/day-10.md"
---

You've covered a lot of ground. Let's make it concrete.

This lesson maps out what a fully configured Cowork setup
looks like, gives you a suggested build order if you haven't
built it yet, and is honest about what Cowork still can't do.

---

## The full system map

A mature Cowork setup has six layers. Each one builds on the
ones before it.

**Layer 1: Context files** (Lesson 4)
Your about-me.md, my-company.md, and anti-ai-writing-style.md.
These tell Claude who you are, what you're working on, and
what good output looks like. Every task runs through these.

**Layer 2: Global Instructions** (Lesson 4)
Standing orders that apply to every session — show me the plan
before acting, save to OUTPUTS, ask one question if unclear.
Short, specific, always-on.

**Layer 3: Connectors** (Lesson 5)
Gmail, Google Drive, Slack — the live connections to where
your work actually happens. Without these, Cowork is limited
to local files. With them, it has access to the substance
of your work day.

**Layer 4: Skills** (Lesson 6)
Your automated processes. Weekly summaries, email drafts,
research briefs — tasks you do the same way every time,
now executed consistently without re-explanation.

**Layer 5: Scheduled Tasks** (Lesson 7)
The recurring workflows that run without you initiating them.
Your morning digest, your weekly summary, your Monday brief.
Work that's done before you ask for it.

**Layer 6: Dispatch** (Lesson 8)
The mobile layer. Assign tasks from anywhere. Persistent
memory across sessions. The interface for a working
relationship with Claude that compounds over time.

Computer use sits outside this stack — it's the fallback
mechanism for everything else, not a layer you build on top of.

---

## A real knowledge worker's configured setup

Here's what this looks like as a concrete example:

```
Claude Workspace/
├── ABOUT ME/
│   ├── about-me.md (300 words, specific)
│   ├── my-company.md (250 words, current quarter's context)
│   └── anti-ai-writing-style.md (your don'ts list)
├── OUTPUTS/
│   ├── morning-digest-2026-04-14.md
│   ├── weekly-summary-2026-04-11.md
│   └── [everything Cowork creates lands here]
└── TEMPLATES/
    └── status-update-template.md

Connectors: Gmail ✓ | Google Drive ✓ | Slack ✓
Skills: Weekly Summary | Email Draft | Research Brief
Scheduled: Morning digest (weekdays) | Weekly summary (Fridays)
Dispatch: Paired to iPhone
```

Global Instructions (100 words):
- Read ABOUT ME files before every task
- Show plan before acting on files
- Save all deliverables to OUTPUTS
- Ask one question if unclear
- Never delete without permission
- Never send without showing draft first

---

## Suggested build order

If you're building from scratch, this sequence minimizes
friction and maximizes early wins:

**Week 1:** Setup + first tasks (Lessons 1-3)
Get Cowork installed, grant folder access, run your first
three real tasks. Confirm the basics work.

**Week 1-2:** Context files (Lesson 4)
Build about-me.md using the interview method. Write
anti-ai-writing-style.md. Set up Global Instructions.
This changes the quality of everything that follows.

**Week 2:** Two connectors (Lesson 5)
Install Gmail and Google Drive. Run one task using each.
Confirm they're working correctly.

**Week 2-3:** One Skill (Lesson 6)
Pick your single most common recurring task. Build a Skill
for it using Skill Creator. Run the debugging trick to
confirm it fires correctly.

**Week 3:** One scheduled task (Lesson 7)
Set up the morning email digest or weekly summary —
whichever is more immediately useful. Adjust the cadence
after the first few runs.

**Week 3-4:** Dispatch (Lesson 8)
Pair your phone. Use it for one week. Assign at least
three tasks from your phone before evaluating whether
it fits your workflow.

**When you need it:** Computer use (Lesson 9)
Don't set this up speculatively. Enable it the first time
you hit a task that needs it.

---

## The infrastructure mindset

The most important shift this course is trying to create
isn't a feature or a workflow. It's a way of thinking.

The people who get the most out of Cowork don't think
about prompts. They think about systems. They've built
infrastructure — context files, Skills, scheduled tasks —
that means Claude understands their work before they say
a word. The prompt becomes almost irrelevant when the
setup is right.

Once your voice, your standards, and your processes are
encoded, Claude executes them. You focus on the judgment
calls and the decisions. Claude handles the assembly.

---

## What Cowork still can't do

Be honest with yourself about the current limitations:

- **No HIPAA, FedRAMP, or FSI regulated workloads** —
  explicitly documented by Anthropic. Don't use Cowork for
  healthcare data, government systems, or regulated financial work.
- **No Audit Logs for Cowork activity** — conversation history
  is stored locally, not centrally. Enterprise compliance teams
  should note this.
- **Cowork activity not in Data Exports** — another enterprise
  consideration.
- **Windows arm64 not supported** — check your machine specs
  if you're on a newer Windows laptop.
- **Dispatch and computer use still in research preview** —
  solid but still maturing. Expect improvements.
- **Scheduled task timing is imprecise** — exact clock-time
  scheduling has limited documentation as of April 2026.
- **The app must stay open** — no cloud fallback.

None of these are reasons not to use Cowork. They're things
to know so you use it appropriately.

---

## What comes next

This course covered the full Cowork system. The natural
next pieces to explore:

**Cowork Projects** — a feature we didn't cover in this course
but worth exploring once your basics are solid. Projects give
Claude a persistent context for a specific domain of work — a
client account, a department, a recurring workflow. Instead of
a general workspace, you create a named Project with its own
instructions, files, and memory. Find it via the **Work in a
project** dropdown in the Cowork interface.

**Claude Skills: The Complete Guide** — Deep dive on writing
SKILL.md files manually, skill chaining, advanced trigger
mechanics, and 10 pre-built Skills for common knowledge work.

**Claude Dispatch: Run Tasks From Your Phone** — A focused
guide on getting the most out of Dispatch, including the
best task types for mobile and how the persistent memory
compounds over time.

**Workflow Recipes** — Individual step-by-step recipes for
specific use cases: weekly reporting, competitive research,
inbox management, document assembly, and more. Each is a
complete, copy-paste-ready workflow you can run today.

---

You've built the system. Now use it.

The only way to get better at this is to give Cowork real
work. Assign something today that you'd normally spend an
hour on. See what comes back. Adjust. Repeat.

That's the whole game.

---

*Last updated: April 2026. Cowork is evolving fast. Check
[Anthropic's release notes](https://support.claude.com/en/articles/12138966-release-notes)
for the latest changes.*
