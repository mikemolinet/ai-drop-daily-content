---
id: "ai-201-day-06"
type: "course-lesson"
course: "ai-201"
course_title: "AI 201: Build Your AI System"
week: 1
day: 6
day_of_week: "sat"
lesson_type: "lab"
title: "Lab: Cowork Deep Dive"
subject: "Three workflows that'll make Cowork earn its subscription."
source_path: "ai-201/week-1/day-06-sat-lab.md"
---

Yesterday you got Cowork set up and did your first task. Today we stop practicing and start building. You're going to create three real workflows — the kind of thing you'll actually reuse next week, and the week after that.

Each exercise takes 5-7 minutes. Total lab time: about 20 minutes. By the end, you'll have a meeting report, a structured spreadsheet, and a presentation deck — all created by Cowork from raw inputs you'd normally spend an hour processing yourself.

Let's go.

## What you need

- **Claude Desktop app** with Cowork enabled (you set this up yesterday)
- **A folder Cowork can access** — use the same working folder from Day 5, or create a new one
- **About 20 minutes** of uninterrupted time
- **Your computer plugged in** — Cowork sessions die if your machine sleeps mid-task

If you have your own messy meeting notes, receipts, or presentation topics, use those. If not, sample inputs are included below for each exercise. Real material always works better, but the samples will get you the same learning.

---

## Exercise 1: Messy meeting notes → clean report (5-7 minutes)

This is the "aha moment" exercise. Everyone has meeting notes that look like a crime scene — half-sentences, abbreviations only you understand, bullet points that made sense in the moment and mean nothing two days later.

You're going to hand that mess to Cowork and get back a formatted report with decisions, action items, and follow-ups.

### Steps

1. **Create a file called `meeting-notes-raw.txt`** in your Cowork folder. Paste in your own messy meeting notes, or use the sample below.

2. **Open Cowork** in Claude Desktop (click the Cowork icon or start a new Cowork session).

3. **Give it this prompt** (copy-paste, then adjust the file path if needed):

```
Read the file meeting-notes-raw.txt in my working folder. These are raw, messy notes from a team meeting. Turn them into a clean, professional meeting summary document called meeting-report.md with these sections:

- Meeting overview (date, attendees, purpose — infer from context)
- Key discussion points (organized by topic, not chronological)  
- Decisions made (only things that were actually decided)
- Action items (who owns what, with deadlines if mentioned)
- Open questions / follow-ups needed

Keep it concise. If something in the notes is ambiguous, flag it rather than guessing.
```

4. **Review the plan** when Cowork presents it. Make sure it's reading and writing to the right files. Approve it.

5. **Open the output file** and compare it to your raw notes. Notice what it caught that you might have missed. Notice what it got wrong or had to flag as unclear.

### Sample messy meeting notes (if you don't have your own)

Create `meeting-notes-raw.txt` with this content:

```
product sync mar 2
dave, sarah, mike, jennifer (late), tom on phone

- q1 numbers not great, sarah says 12% under target
- mike thinks pricing is the issue, sarah disagrees — says its onboarding
- long discussion about onboarding flow, jennifer showed mockups when she arrived
- everyone liked the simplified version (3 steps instead of 7)
- DECISION: go with jennifer's 3-step onboarding, ship by end of march
- tom's team needs API changes for this — he said 2 weeks?? might be 3
- mike wants to revisit pricing anyway in april, sarah ok with that
- ACTION dave to send jennifer's mockups to engineering by friday
- budget question — do we need extra contractor for the API work? tom to check
- sarah mentioned churn dashboard is broken again, nobody knew who owns it
- mike volunteered to fix churn dashboard this week
- next meeting: mar 9 same time
- jennifer has to present to board on mar 15, needs the onboarding metrics
  sarah to pull those numbers by mar 12
```

### What to look for

Did Cowork separate the decisions from the discussion? Did it catch all the action items — including the ones that weren't explicitly labeled? Did it flag the ambiguity in Tom's timeline ("2 weeks?? might be 3")?

This is the kind of task that takes you 20 minutes manually. Cowork does it in about 60 seconds.

---

## Exercise 2: Folder of documents → structured spreadsheet (5-7 minutes)

This one shows off Cowork's real superpower: turning a pile of unstructured documents into organized data. Receipts, invoices, contracts, research notes — anything you have a folder of, Cowork can extract the key information and build a proper spreadsheet.

### Steps

1. **Create a folder called `receipts`** (or `invoices` or `documents` — whatever matches your material) inside your Cowork working folder. Drop in 3-5 documents. These can be:
   - Actual receipts or invoices (PDF, image, or text)
   - Contracts or agreements
   - Any collection of similar documents with extractable data
   
   Don't have documents handy? Create the sample files below.

2. **Give Cowork this prompt:**

```
Look at all the files in my receipts folder. Extract the key data from each document and create an Excel workbook called expense-summary.xlsx with:

- A "Transactions" sheet with columns: Date, Vendor, Description, Category, Amount, Payment Method
- A "Summary" sheet with: total by category, grand total, and average transaction amount
- Use real Excel formulas for the totals and averages (not hardcoded numbers)
- Sort transactions by date, newest first
- If any data is unclear or missing from a document, put "NEEDS REVIEW" in that cell

Format it professionally — bold headers, currency formatting on amounts, auto-fitted column widths.
```

3. **Review the plan and approve it.**

4. **Open the Excel file.** Check the formulas — click on a total cell and make sure it's actually a SUM formula, not just a typed number. Check the Summary sheet. Check for any "NEEDS REVIEW" flags.

### Sample files (if you don't have real documents)

Create these text files in your `receipts` folder:

**receipt-01.txt:**
```
DOWNTOWN OFFICE SUPPLY
Mar 1, 2026
Printer paper (5 reams) - $42.50
Ink cartridges (black x2) - $67.80
Sticky notes - $8.99
Subtotal: $119.29
Tax: $10.14
TOTAL: $129.43
Visa ending 4521
```

**receipt-02.txt:**
```
uber receipt
feb 28 2026
Trip from office to airport
Distance: 23.4 mi
fare: $38.50
tip: $7.00
total charged: $45.50
personal amex
```

**receipt-03.txt:**
```
RESTAURANT — working lunch
Cafe Milano, Feb 27
2x entrees, 1x appetizer, drinks
Total with tip: $94.20
Company Visa 4521
Client: Meridian Corp (Sarah + their VP of Ops)
```

**receipt-04.txt:**
```
Adobe Creative Cloud
Monthly subscription
March 2026
$54.99/mo
Auto-charged to Visa 4521
Business software
```

### What to look for

Open that Excel file and actually check it. Are the formulas real? Does the category breakdown make sense? Did Cowork figure out the payment methods even when they were described inconsistently ("Visa ending 4521" vs. "Company Visa 4521" vs. "personal amex")?

This is a workflow you can reuse every month. Drop your receipts in a folder, run the prompt, get your expense report.

---

## Exercise 3: Outline → presentation deck (5-7 minutes)

Last one. You're going to give Cowork a topic outline and get back a formatted presentation with proper structure, speaker notes, and brand colors. This is the exercise that makes people say "wait, it can do *that*?"

### Steps

1. **Create a file called `presentation-outline.txt`** in your working folder with your topic, or use the sample below.

2. **Give Cowork this prompt:**

```
Read presentation-outline.txt and create a PowerPoint presentation called quarterly-update.pptx.

Requirements:
- Title slide with the presentation name and date
- One slide per major section from the outline
- Bullet points should be concise (no walls of text on slides)
- Add speaker notes to every slide with talking points and context I can reference while presenting
- Use this color scheme: dark navy (#1B2A4A) for headers, white backgrounds, accent color teal (#2EC4B6) for highlights
- Include a summary/next-steps slide at the end
- Professional, clean layout — no clip art, no decorative nonsense

Keep it to 8-10 slides total. If the outline has too much for that, consolidate.
```

3. **Review the plan and approve.**

4. **Open the PowerPoint.** Click through every slide. Check the speaker notes (click "Notes" at the bottom of PowerPoint). Check that the colors actually match what you asked for.

### Sample outline (if you don't have your own)

Create `presentation-outline.txt` with:

```
Q1 2026 Team Update

1. Overview & highlights
   - Revenue up 18% QoQ
   - Shipped 3 major features
   - Team grew from 12 to 15

2. Product updates
   - New onboarding flow (conversion up 23%)
   - API v2 launched, 40+ integrations
   - Mobile app redesign in progress (beta next month)

3. Customer metrics
   - NPS: 72 (up from 64)
   - Churn: 3.1% (down from 4.8%)
   - 12 new enterprise accounts

4. Challenges
   - Hiring timeline slower than planned
   - Infrastructure costs up 30% — need optimization plan
   - Support ticket volume outpacing team capacity

5. Q2 priorities
   - Launch mobile app
   - Hire 3 engineers + 1 support lead
   - Reduce infrastructure costs by 20%
   - Expand to European market (localization)

6. Ask from leadership
   - Approve expanded hiring budget
   - Green-light EU data residency investment
```

### Customizing further

Want to see Cowork flex? After it creates the deck, try a follow-up:

```
Update the presentation to use my company colors instead: primary #FF6B35, secondary #004E89, with light gray (#F5F5F5) backgrounds.
```

Watch it restyle the entire deck in seconds. That's the kind of iteration that takes 30 minutes of manual clicking through PowerPoint's color menus.

---

## Reflection

You just built three workflows that most people spend hours on every week. Take a minute to think about these:

1. **Which exercise surprised you the most?** Which output was closer to "done" than you expected?

2. **Where did Cowork need the most correction?** What did you have to fix or re-prompt? That's useful data — it tells you where to write better initial prompts next time.

3. **What's your version of these workflows?** You used sample data (or your own). What recurring task in your actual work week could use the same pattern? Meeting notes, expense reports, and presentations are just three examples. The pattern is always the same: messy input → clear prompt → structured output.

4. **How much time would these three tasks take you manually?** Be honest. Meeting report: 20 minutes? Expense spreadsheet: 30-45 minutes? Presentation: an hour? You just did all three in under 20 minutes, and most of that was reading and reviewing.

## What's coming next week

Week 1 was about building your stack by hand — custom instructions, prompt libraries, Cowork workflows. You've been the one kicking everything off.

Week 2 changes that. We're starting with **Cowork automation**: scheduled tasks that run on their own, recurring workflows that fire without you lifting a finger, and connecting Cowork to your existing tools — Gmail, Google Calendar, Slack, and more. AI that works while you don't.

Enjoy your Sunday. You've earned it.

**Three workflows. Twenty minutes. That's not using AI — that's having AI work for you. And next week, it starts working without you even asking.**
