# How to Use Claude Code for Everything

## A Department-by-Department Guide with 30+ Prompts for Marketing, Sales, HR, Ops, Finance, Product, and Support

> **📥 [Download this guide as Markdown](/api/guides/claude-code-for-everything/download)** — save it, share it, drop it in your team's repo.

Most people think Claude Code is just for developers. It's not. Claude Code is one of the most powerful work tools available right now, and you don't need to write a single line of code to use it. (And if the terminal feels intimidating, Anthropic also offers Claude Cowork - a visual, non-terminal version built specifically for non-technical users.)

Anthropic's own marketing team went from 30-minute ad creation workflows to 30 seconds (their growth marketer had never written a line of code before). Their customer marketing team cut case study drafts from 2.5 hours to 30 minutes. None of these people were engineers.

This guide shows you how to use Claude Code for your actual job - whether you're in marketing, sales, HR, operations, finance, product, or support.

**Why Claude Code and not just regular Claude?** Regular Claude is a chatbot. Claude Code works directly on your files and folders. It reads your documents, analyzes your spreadsheets, creates and edits files, and remembers your preferences between sessions. That's the difference between asking a colleague a question and having them actually sit down and do the work with your real materials.

---

## Where Claude Code Adds the Most Value

| Use Case | Without Claude Code | With Claude Code | Time Saved |
|---|---|---|---|
| Draft campaign copy with 15 headline variants | 45 min in Google Docs | 5 min with a prompt + review | ~80% |
| Create a 10-page onboarding doc | 4-6 hours | 45 min of iteration and review | ~80% |
| Analyze a CSV of customer records | Half a day + Excel formulas | 15 min prompt + review | ~75% |
| Write 20 personalized outreach emails | 2-3 hours | 20 min with template prompt + editing | ~80% |
| Build a knowledge base from support tickets | 2 weeks | 3-4 hours | ~80% |
| Generate quarterly board report from data | Full day | 1-2 hours of iteration | ~75% |

---

## Quickstart: Your First 30 Minutes

| Step | What to Do | Why It Matters |
|---|---|---|
| 🔵 **1. Install Claude Code** | **Option A (easiest):** Download Claude Desktop from claude.ai - Claude Code is built in. **Option B (terminal):** Open Terminal (Mac) or Command Prompt (Windows). Paste: `curl -fsSL claude.ai/install.sh \| bash` (Mac) or `irm https://claude.ai/install.ps1 \| iex` (Windows). Type `claude` to start. | One-time setup. Takes 5 minutes. |
| 🔵 **2. Create a project folder** | In Terminal, run these three commands one at a time: `mkdir ~/Documents/MyProject` then `cd ~/Documents/MyProject` then `claude` | Claude Code works within your current folder. Different folders = different projects. |
| 🔵 **3. Set up your CLAUDE.md** | Type `/init` to auto-generate a starter CLAUDE.md, then tell Claude: *"Help me improve this CLAUDE.md. I work in [your department] and I need help with [your main tasks]. Ask me questions about my workflow."* | This is Claude's memory. It reads this file every session so it knows your context. |
| 🟢 **Bonus: Create your first skill** | Tell Claude: *"Help me create a skill for [your most repetitive task]. Walk me through what a SKILL.md file needs."* | Skills auto-activate when Claude detects a matching request. Like teaching it a new specialty. |

> 💡 **You don't need to know how to code.** You need to know how to explain your problem clearly. That's it. Think of Claude Code as a very capable colleague who needs good instructions.

> ⚠️ **What to expect on first run:** Claude will ask permission to read and write files in your folder. This is normal - it needs access to do its work. You can approve or deny each action.

---

## The 5 Concepts That Matter (Skip the Rest)

Before diving into department prompts, here's what you actually need to know:

| Concept | What It Is | Plain English |
|---|---|---|
| **CLAUDE.md** | A file Claude reads every session | Your project's instruction manual. Put your preferences, context, and rules here. |
| **Skills** | Specialized workflow templates | Like teaching Claude a new job function. It auto-loads the right skill when you ask for something matching. |
| **Output Styles** | Behavior configuration | Tell Claude to act like a marketer instead of a developer. Set `keep-coding-instructions: false` to turn off code-focused behavior. |
| **Subagents** | Delegated assistants | Give a complex task to a specialized mini-Claude with its own focus area. Great for research-heavy work. |
| **Context Window** | Claude's working memory | Gets full over long sessions. Start fresh conversations for new topics. Think of it like a whiteboard that fills up. |

---

## Marketing

### Campaign Copy Generation

```
Read @brand-guidelines.md and @past-campaigns/top-performers.csv for context
on our voice and what's worked before.

I need Google Ads responsive search ad copy for [product/service].

Target audience: [describe]
Key value propositions: [list 3-4]
Competitor positioning: [how we're different]

Generate:
- 15 unique headlines (30 characters max each)
- 4 descriptions (90 characters max each)
- Flag any that are too similar to each other

Save the output as campaigns/google-ads-[date].csv with columns:
Type, Text, Character Count

Then verify every headline is under 30 chars and every description
is under 90 chars. Fix any that aren't.
```

### Content Calendar Builder

```
Create a 4-week content calendar for [brand/product].

Platform: [LinkedIn / Instagram / Twitter / all]
Posting frequency: [X posts per week per platform]
Brand voice: [describe tone - casual, professional, etc.]
Key themes this month: [list 2-3 themes]
Upcoming launches or events: [list any]

For each post, include:
- Platform
- Date and time slot
- Post copy (ready to publish)
- Suggested image/visual direction
- Relevant hashtags (if applicable)

Format as a table.
```

### Email Sequence Writer

```
Read @brand-voice.md for tone guidance and @emails/best-performers/ for
examples of emails that converted well.

Write a 5-email nurture sequence for [product/service].

Goal: [convert free trial to paid / re-engage churned users / onboard new signups]
Audience: [describe]
Tone: [friendly, professional, urgent, etc.]
Key objections to address: [list 2-3]

For each email include:
- Subject line (and one A/B variant)
- Preview text
- Body copy
- CTA button text
- Suggested send timing (days after trigger)

Keep each email under 200 words.

Save each email as a separate file in emails/nurture-sequence/
(email-1-welcome.md, email-2-value.md, etc.)
```

### SEO Content Brief

```
Create an SEO content brief for the keyword: "[target keyword]"

Research what this keyword typically covers, then give me:
- Recommended title (with keyword placement)
- Target word count
- Outline with H2 and H3 headers
- 5 related keywords to include naturally
- 3 internal linking opportunities (suggest topic areas)
- Content angle that differentiates from existing top results
- Meta description (155 characters max)
```

### Campaign Performance Analysis

```
I'm going to paste campaign performance data. Analyze it and tell me:

1. Which campaigns are performing best and why
2. Which should be paused or adjusted
3. Patterns in what's working (audience, creative type, messaging)
4. Specific recommendations for next month's budget allocation
5. Any anomalies or red flags

Here's the data:
[paste CSV data or describe the metrics]
```

---

## Sales

### Personalized Outreach Generator

```
Write personalized outreach emails for these prospects.

Our product: [what you sell and key value prop]
ICP: [ideal customer profile]

For each prospect below, write a personalized email that:
- References something specific about their company or role
- Connects our value prop to their likely pain points
- Keeps it under 100 words
- Ends with a low-friction CTA (not "book a demo")

Prospects:
1. [Name, Title, Company, any context]
2. [Name, Title, Company, any context]
3. [Name, Title, Company, any context]
```

### Proposal Draft Builder

```
Create a proposal for [prospect company name].

Our product/service: [describe]
Their problem: [what they told us in discovery]
Decision makers: [names and roles]
Budget range: [if known]
Timeline: [when they need a solution]
Competitors they're also evaluating: [if known]

Structure:
1. Executive Summary (their problem, our solution, expected outcome)
2. Proposed Solution (specific to their needs)
3. Implementation Timeline
4. Pricing Options (give 3 tiers if applicable)
5. Why Us (differentiation, not generic marketing copy)
6. Next Steps

Keep it under 5 pages. Professional but not stiff.
```

### CRM Data Cleanup and Analysis

```
I'm going to paste our CRM export data. Help me:

1. Identify duplicate records (by email or company name)
2. Flag incomplete records missing critical fields
3. Segment by: deal stage, industry, company size
4. Calculate: average deal cycle, win rate by source, pipeline value by stage
5. Identify stale deals (no activity in 30+ days)
6. Recommend which deals to prioritize this week

Here's the data:
[paste CSV or describe the dataset]
```

> 💡 **Data size note:** Claude can handle substantial datasets in a single paste, but very large files (50,000+ rows) should be summarized or sampled first. For big files, try: `head -1000 big-file.csv | claude "analyze this sample and tell me what patterns you see"`

### Competitive Battle Card

```
Create a competitive battle card for [competitor name] vs our product [your product].

Include:
- Side-by-side feature comparison (be honest about where they win)
- Their typical pricing vs ours
- Common objections when competing against them and how to respond
- Their weaknesses we should highlight
- Questions to ask the prospect that expose their gaps
- Win story: brief example of a deal we won against them

Format for quick reference - a sales rep should be able to scan this in 2 minutes.
```

---

## Operations

### Process Documentation

```
Read all the files in @processes/ for context on how we currently document things.

Help me document our [process name] process.

I'll describe how it works step by step. After I'm done, create:

1. A clean process document with numbered steps
2. A decision tree for common exceptions
3. A RACI chart (who's Responsible, Accountable, Consulted, Informed)
4. Estimated time for each step
5. Common failure points and how to handle them
6. Checklist version someone can print and follow

Save each output as a separate file in processes/[process-name]/

Here's how the process works:
[describe it conversationally - Claude will structure it]
```

### Meeting Notes to Action Items

```
Here are my rough notes from today's meeting. Process them into:

1. Clean summary (3-5 bullet points of key decisions)
2. Action items with owners and deadlines (table format)
3. Open questions that still need answers
4. Follow-up meeting topics (if any)

Raw notes:
[paste your messy meeting notes]
```

### Workflow Automation Planning

```
I have a repetitive workflow I want to automate or streamline.

Current process:
[describe each step, who does it, how long it takes, what tools are involved]

Help me:
1. Map the current workflow with time estimates
2. Identify which steps could be automated
3. Recommend specific tools or approaches for each automation
4. Estimate time saved per week
5. Create an implementation plan (what to automate first based on ROI)
6. Flag any steps that should stay manual (and why)
```

### SOP Template Generator

```
Create a Standard Operating Procedure for: [task name]

Department: [which team owns this]
Frequency: [how often this is done]
Tools required: [list any software/tools]
Prerequisites: [what needs to be true before starting]

Include:
- Purpose and scope
- Step-by-step instructions (detailed enough for a new hire)
- Screenshots placeholders (mark where they should go)
- Troubleshooting section for common issues
- Version history table
- Approval signatures section
```

---

## HR

### Job Description Writer

```
Write a job description for: [role title]

Department: [team]
Reports to: [manager title]
Location: [remote/hybrid/onsite, city]
Level: [junior/mid/senior]
Salary range: [if sharing publicly]

Key context:
- What this person will actually do day-to-day: [describe]
- Why this role exists now: [growth, backfill, new initiative]
- Team size and culture: [describe]

Requirements:
- Must-haves: [list real requirements, not wishlists]
- Nice-to-haves: [list genuinely helpful bonuses]

Write it in a warm, direct tone. Avoid jargon. Make someone excited about the role, not intimidated by it. Include a "What you'll do in your first 90 days" section.
```

### Onboarding Program Builder

```
Create a 30-60-90 day onboarding plan for a new [role title].

Include for each phase:
- Learning objectives
- Key meetings to schedule (and with whom)
- Tasks to complete
- Resources to review
- Milestones / success criteria
- Check-in schedule with manager

Also create:
- Day 1 welcome email template
- First week schedule (hour by hour for days 1-3, then daily for days 4-5)
- "Who's who" template the manager should fill in
- 30-day feedback survey questions

Make it practical, not overwhelming. A new hire should feel supported, not buried.
```

### Policy Document Drafter

```
Draft a company policy for: [policy topic, e.g., remote work, PTO, expense reimbursement]

Company context:
- Size: [number of employees]
- Industry: [your industry]
- Current approach: [how this is handled now, if at all]
- Key concerns: [what prompted this policy]

Include:
- Purpose and scope
- Policy details (clear, specific, no ambiguity)
- Eligibility
- Procedure for requests/approvals
- Exceptions and how they're handled
- FAQ section (anticipate the questions employees will ask)
- Effective date and review schedule

Write it clearly. An employee should understand exactly what's allowed and what isn't without asking their manager to interpret it.
```

### Interview Question Set

```
Create a structured interview question set for: [role title]

Interview stages: [phone screen, technical, culture fit, hiring manager, etc.]

For each stage, provide:
- 5-7 questions tailored to that stage
- What good answers look like (scoring rubric)
- Red flags to watch for
- Follow-up probes for vague answers

Focus areas:
- [Skill 1 to evaluate]
- [Skill 2 to evaluate]
- [Cultural value to assess]

Include at least 2 behavioral questions (STAR format) and 1 scenario-based question per stage.
```

---

## Finance

### Report Generator

```
I'm going to paste our financial data. Create a [monthly/quarterly] report that includes:

1. Executive summary (3-4 sentences a CEO can scan)
2. Revenue analysis: trends, growth rate, comparisons to prior period
3. Expense breakdown by category with % of total
4. Key ratios: gross margin, burn rate, runway (if applicable)
5. Variance analysis: budget vs actual for top 5 line items
6. Cash flow summary
7. 3 recommendations based on the data

Format with clear headers and tables. Use bullet points for insights.

Here's the data:
[paste financial data]
```

### Budget Planning Template

```
Help me build a [annual/quarterly] budget for [department or company].

Current context:
- Last period's total spend: [amount]
- Headcount: [current and planned]
- Revenue target: [if relevant]
- Major planned initiatives: [list]
- Known cost changes: [rent increase, tool renewals, etc.]

Create:
1. Line-item budget template with categories
2. Monthly breakdown
3. Assumptions section (document what each estimate is based on)
4. Scenario modeling: base case, growth case, conservative case
5. Approval workflow section

Format as a table I can paste into a spreadsheet.
```

### Financial Data Analysis

```
Analyze this financial dataset and provide:

1. Trend analysis: what's improving, what's declining, what's flat
2. Anomaly detection: any numbers that look unusual
3. Cohort analysis (if customer data): retention, LTV, payback period
4. Forecasting: project next 3 months based on current trends
5. Benchmarking context: how do these numbers compare to typical [industry] metrics

Be specific with numbers. Don't just say "revenue is growing" - say "revenue grew 12% MoM, accelerating from 8% the prior month."

Here's the data:
[paste data]
```

---

## Product

### PRD (Product Requirements Document)

```
Write a PRD for: [feature name]

Context:
- Problem we're solving: [user pain point]
- Who it's for: [user persona]
- How they solve it today: [current workaround]
- Why now: [what changed, why this is a priority]

Include:
1. Problem statement and user stories
2. Proposed solution (high-level)
3. Requirements: must-have, should-have, won't-have (MoSCoW)
4. Success metrics (how we'll know it worked)
5. Edge cases and open questions
6. Dependencies and risks
7. Rough scope estimate (S/M/L/XL)

Write it so an engineer can start technical planning from this doc.
```

### User Research Synthesis

```
I'm going to paste notes from [X] user interviews. Synthesize them into:

1. Key themes (ranked by frequency)
2. Direct quotes that best illustrate each theme
3. Pain points (severity: high/medium/low)
4. Feature requests mentioned (with count of who mentioned each)
5. Surprises: anything unexpected or counterintuitive
6. Personas: do the interviewees cluster into distinct user types?
7. Recommended next steps (what to build, what to research more)

Interview notes:
[paste all interview notes]
```

### Roadmap Communication

```
Help me turn our product roadmap into a communication for [audience: executives / customers / the team].

Current roadmap items:
[list features/initiatives with rough timelines]

Create:
- For executives: 1-page summary focused on business impact and strategic alignment
- For customers: blog post or changelog entry focused on what's coming and why they should be excited
- For the team: detailed breakdown with context on priorities and sequencing

Each version should explain the "why" behind our choices, not just the "what."
```

---

## Customer Support

### Knowledge Base Builder

```
Help me create a knowledge base from our support data.

I'll paste our most common support tickets/questions. For each one, create:

1. Article title (searchable, matches how customers phrase it)
2. Short answer (1-2 sentences for quick scanning)
3. Detailed walkthrough with numbered steps
4. Troubleshooting section (if X doesn't work, try Y)
5. Related articles to link to

Common support questions:
[paste your top 15-20 support questions or ticket categories]
```

### Response Template Library

```
Create customer support response templates for these scenarios:

1. [Scenario: e.g., customer requesting a refund]
2. [Scenario: e.g., bug report acknowledgment]
3. [Scenario: e.g., feature request response]
4. [Scenario: e.g., account cancellation]
5. [Scenario: e.g., billing question]

For each template:
- Empathetic opening (acknowledge their situation)
- Clear explanation or resolution
- Next steps
- Warm close

Tone: [friendly and professional / casual / formal]
Include [placeholders] for personalization fields.

Each template should be under 150 words. Support reps should be able to customize in under 30 seconds.
```

### Support Ticket Analysis

```
I'm going to paste a batch of recent support tickets. Analyze them for:

1. Top issue categories (with volume for each)
2. Sentiment breakdown (frustrated, neutral, positive)
3. Resolution time patterns (what takes longest to resolve)
4. Escalation patterns (what gets escalated most)
5. Self-service opportunities (which issues could be deflected with better docs)
6. Product feedback signals (what bugs or feature gaps are customers hitting)
7. Recommendations for reducing ticket volume

Support tickets:
[paste ticket data]
```

---

## Power User Tips

These come from Anthropic's best practices guide and real-world usage. They work regardless of your department.

### 1. Give Claude a Way to Check Its Work

The single highest-leverage habit. Instead of reviewing everything yourself, tell Claude what "done" looks like.

```
Write the Q1 marketing report. When you're done:
- Verify all percentages add up to 100%
- Check that every claim has a supporting data point
- Confirm the executive summary matches the detailed findings
- List anything you're uncertain about
```

### 2. Explore First, Then Execute

Don't jump straight to "write me a policy doc." Start with exploration.

```
Before writing anything, review the employee handbook files in this folder.
Summarize our current PTO policy, identify gaps, and suggest what a
new policy should cover. Then I'll tell you which direction to go.
```

### 3. Reference Specific Files and Examples

Instead of describing what you want, show Claude. Use `@filename` to reference files directly, or pipe data in with `cat data.csv | claude`.

```
Look at @proposals/acme-q4.md.
Use that structure and tone to write a new proposal for [prospect],
but adjust the pricing section for their smaller team size.
```

### 4. Use CLAUDE.md to Save Repeated Context

If you're explaining the same things every session, put them in your CLAUDE.md file:

```markdown
# Marketing Team Context
- Brand voice: professional but warm, never corporate
- Always use Oxford comma
- Target audience: mid-market SaaS companies, 50-500 employees
- Competitor mentions: always acknowledge, never trash-talk
- Approved tools: HubSpot, Google Analytics, Figma
```

### 5. Create Skills for Recurring Workflows

If you do the same type of work regularly (weekly reports, meeting notes, content briefs), create a skill for it. Claude will auto-activate the right process when it detects a matching request.

```
Help me create a skill for processing weekly sales reports.
I get a CSV export from HubSpot every Monday. I need it turned into
a summary with: pipeline changes, deal movement, rep activity, and
a 3-sentence executive summary. Walk me through setting up a SKILL.md.
```

### 6. Start Fresh When Quality Drops

Claude's context window fills up over long sessions. If responses get vague or repetitive, start a new conversation. Think of it like clearing a cluttered whiteboard.

### 7. Stack Context for Complex Tasks

For big projects, layer your context:

```
Read these files before starting:
1. @company-overview.md (who we are)
2. @brand-guidelines.md (how we communicate)
3. @q4-results.csv (the data)

Now create the annual report following the structure in @report-template.md.
```

---

## Common Mistakes and How to Avoid Them

| Mistake | Why It Happens | What to Do Instead |
|---|---|---|
| **Vague prompts** | "Make this better" gives Claude nothing to work with | Be specific: "Shorten this to 200 words, make the tone more casual, and add a CTA" |
| **Not reviewing output** | Claude is good but not infallible | Always review, especially for facts, numbers, and company-specific details |
| **One giant prompt** | Trying to get everything in one shot | Break complex work into steps. Explore → plan → execute → review. |
| **Ignoring CLAUDE.md** | Repeating context every session | Invest 10 minutes setting up your CLAUDE.md. It pays back immediately. |
| **Never starting fresh** | Long conversations degrade quality | New conversation for new topics. Use `claude -c` to continue, `claude` for fresh. |
| **Copy-paste without adapting** | Taking Claude's output as final | Treat output as a strong first draft. Your expertise + Claude's speed = great work. |
| **Not using files** | Typing everything into the prompt | Put reference docs in your project folder. Use `@filename` to reference them. |

---

## Honest Limitations

| Limitation | Reality | Workaround |
|---|---|---|
| **Can't access your cloud apps** | Claude works on local files. It can't log into your CRM, Google Drive, or Slack directly. | Export data as CSV/text, put it in your project folder, then point Claude at it. |
| **Context window fills up** | Long sessions = declining quality. You'll notice responses getting vaguer or less accurate. | Start fresh conversations. Keep sessions focused on one topic. |
| **Not always accurate** | Claude can make confident-sounding mistakes, especially with specific numbers or recent events. | Always verify facts, figures, and anything you'll publish publicly. |
| **Terminal can be intimidating** | The command-line interface isn't familiar for everyone. | Follow the quickstart above. Once you type `claude`, you're just having a conversation. Cursor IDE also works as a visual wrapper. |
| **Subscription required** | Claude Code requires a Claude Pro ($20/mo) or Team plan. | Worth it if you use it regularly. The time savings from even one workflow usually justify the cost in week one. |
| **Works best with clear instructions** | "Do something creative" produces mediocre results. Specific context produces great results. | Treat Claude like a capable new hire: give clear briefs, show examples, explain what "good" looks like. |
| **Can't replace your judgment** | Claude doesn't know your company culture, political dynamics, or strategic context the way you do. | Use Claude for the 80% (drafting, analysis, formatting). Add the 20% that only you can (judgment, relationships, context). |

---

## How to Use This Guide

### Getting Started (do these first)

| Priority | Action | Time | Impact |
|---|---|---|---|
| 1 | Follow the Quickstart above. Install Claude Code and create your first CLAUDE.md. | 30 min | Foundation for everything else |
| 2 | Pick the ONE prompt from your department section that matches your most painful recurring task. Try it. | 15 min | Immediate proof of value |
| 3 | Iterate on the output. Give Claude feedback. Ask for revisions. Get it to 90%. | 15 min | Builds your prompting instinct |

### Going Deeper (once you've got the basics)

| Priority | Action | Time | Impact |
|---|---|---|---|
| 4 | Create an Output Style that matches your department's communication needs. | 20 min | Better default behavior |
| 5 | Build your first Skill for a weekly recurring workflow. | 30 min | Compounds every week |
| 6 | Try cross-department prompts. Marketing person? Try the Data Analysis prompt from Finance. | 10 min | Expands what you think is possible |
| 7 | Set up a second project folder for a different workstream. | 5 min | Clean separation, better context |

---

## Tool Landscape

Claude Code isn't the only AI tool for knowledge work. ChatGPT, Gemini, and Copilot all have their strengths. What sets Claude Code apart is the file system access (it reads and writes your actual files), the persistent memory (CLAUDE.md), and the skill/subagent architecture that lets you build reusable workflows. If you're already using another AI tool for quick questions and brainstorming, Claude Code is the upgrade for structured, repeatable work on real documents and data.

---

*v1.0 — February 2026*

Free to share. Built by Mike Molinet — with AI, of course.

- Substack: mikemolinet.substack.com
- LinkedIn: linkedin.com/in/mikemolinet
- GitHub: github.com/mikemolinet
- Twitter: @mikemolinet
