---
id: "ai-201-day-02"
type: "course-lesson"
course: "ai-201"
course_title: "AI 201: Build Your AI System"
week: 1
day: 2
day_of_week: "tue"
lesson_type: "lesson"
title: "Custom Instructions & Memory"
subject: "Your custom instructions are probably too vague. Here's how to fix them."
source_path: "course-2/week-1/day-02-tue.md"
---

In the first course, you set up custom instructions and maybe built a Custom GPT or Claude Project. If you're like most people, your custom instructions say something like "I'm a [role] at a [company]. I prefer concise responses."

That's a start. It's also why your AI output still feels generic.

Today we're going from "AI kind of knows me" to "AI knows exactly how I think, write, and work." This is the difference between a new hire on Day 1 and a trusted colleague who's been working with you for six months.

## The problem with basic custom instructions

Here's what most people's profiles look like:

*"I'm a marketing manager. I like concise answers. Don't use jargon."*

Here's what that produces: concise, jargon-free responses that could have been written for literally any marketing manager on Earth. The AI knows your job title. It doesn't know *you*.

Compare that to this:

*"I'm a B2B marketing manager at a vertical SaaS company selling to mid-market CFOs. My biggest challenge is that our product is technical but my audience isn't — I constantly translate engineering features into business outcomes. My writing style is direct and slightly informal. I use short sentences. I never start with 'In today's fast-paced...' or any variation of that. When I write emails to prospects, I lead with their specific pain point, not our features. I've been in marketing for 12 years, so don't explain basic concepts — but I'm new to AI-assisted workflows, so explain those."*

That second version produces output that sounds like it came from someone who actually knows you. The specificity is everything.

## The three layers of a great AI profile

**Layer 1: What you do (you already have this)**
Role, industry, company size, who you work with. Basic context.

**Layer 2: How you think (most people skip this)**
Your decision-making style. Your pet peeves. The phrases you hate. The frameworks you use. How you approach problems. What "good" looks like to you.

Examples:
- "I'm a first-principles thinker. When I ask for analysis, start with the underlying assumptions, not the conclusions."
- "I hate corporate buzzwords. Never use 'leverage,' 'synergy,' 'align,' or 'circle back' in anything you write for me."
- "When I ask for options, I want 3 max with clear tradeoffs. Not 7 options that all sound the same."
- "I prefer being told I'm wrong over being told what I want to hear."

**Layer 3: What you've learned from using AI (this is the advanced move)**
After using AI for weeks, you know what goes wrong. Build those fixes into your profile.

Examples:
- "Your first drafts tend to be 30% too long for my needs. Default to half the length you'd normally produce."
- "When I ask for email drafts, you always start with 'I hope this email finds you well.' Never do that."
- "You tend to hedge with 'it depends' and 'there are many factors.' Take a position. I'll push back if I disagree."
- "When working on spreadsheets, always use real formulas, never hardcoded values."

This third layer is what turns AI from a general tool into *your* tool. You're training it on your experience with it.

## Multiple profiles for multiple contexts

You probably have distinct modes at work. Writing to clients is different from internal docs. Analysis work is different from creative work. Each context needs different AI behavior.

**In Claude:** Create separate Projects for each context. Client communications, internal strategy, content creation, data analysis. Each gets its own instructions and reference docs. Upload examples of great output into each one — your best client email, your best report, your best analysis. Those examples teach Claude more than instructions ever will.

**In ChatGPT:** Build separate Custom GPTs. One for client-facing writing, one for meeting prep, one for analysis. Each has its own system prompt tuned to that specific mode.

**The power move:** Upload 5-10 examples of YOUR actual work into each project/GPT. Not templates. Not generic examples. Your real emails, reports, and docs that you were proud of. AI learns more from one real example than from ten paragraphs of instructions.

## Today's exercise: upgrade your profiles (15 minutes)

**Step 1:** Open your existing custom instructions or Claude Project from the first course. Read them fresh. Ask yourself: could this describe anyone with my job title, or is it specifically me?

**Step 2:** Add Layer 2 (how you think) and Layer 3 (what you've learned from AI). Be specific. Be opinionated. The more personality in your profile, the less generic the output.

**Step 3:** Upload at least 3 examples of your real work into a Claude Project. Past emails you liked, reports that went well, writing samples that sound like you.

**Step 4:** Test it. Take one of the green tasks from your Day 1 audit. Give a minimal prompt. Compare the output to what you would have gotten before the upgrade.

The output should feel noticeably more like something you'd actually send, not something any professional in your field might send.

## What's coming tomorrow

Tomorrow you're going to build a purpose-built AI assistant that goes way beyond what you created in the first course. Not just a custom GPT with basic instructions — a laser-focused tool with detailed system prompts, reference docs, conversation starters, and error-correction built in. The kind of thing that produces near-final work on the first try.

**Generic instructions produce generic output. Specific instructions produce output that sounds like you. The difference is 15 minutes of writing.**
