---
title: The AI Agent Playbook
description: How I use AI agents to run a startup solo — exact prompts, workflows, schedules, and copy-paste templates to build your own agent team.
category: AI Agents
publishedAt: 2026-02-16
---

# The AI Agent Playbook
## How I Use AI Agents to Run a Startup Solo — And How You Can Too

*By Mike Molinet — Founded Branch. Now building businesses with AI agents.*

---

## Why This Playbook Exists

I run marketing, content, email, calendar, competitive intel, LinkedIn growth, and ops for my companies. No employees. No contractors. Just me and AI agents.

Not as a stunt. Because it works better.

This playbook gives you everything: the exact prompts I use, the workflows I run, the schedules, the tools, the mistakes I made, and the copy-paste templates to build your own agent team. If you've been thinking about using AI agents but don't know where to start — or you're using ChatGPT like a search engine and know there's more — this is for you.

**My thesis: The future isn't builders using AI tools. It's builders building businesses BY AI agents.**

---

## Part 1: The Agent Mindset Shift

Most people use AI like this:
1. Open ChatGPT
2. Ask a question
3. Get an answer
4. Close the tab

That's using AI as a tool. Here's how I use it:

1. Agent wakes up at 6am on a schedule
2. Scans overnight news, trending topics, and my calendar
3. Drafts today's LinkedIn post in my voice
4. Emails me the draft
5. I spend 5 minutes editing and posting

**The difference:** I didn't initiate anything. The agent operates autonomously on a schedule, like an employee who shows up at 6am and has my morning briefing ready before I'm awake.

**The mental model:** Stop thinking "AI assistant I talk to." Start thinking "employee who runs on schedules and triggers."

---

## Part 2: My Actual Agent Setup (The Full Stack)

Here's everything that runs daily. Not theoretical. This is today's setup.

### Agent 1: Chief of Staff ("Max")

**What it does:** Everything a $120K/year chief of staff would do.

**Daily schedule:**

| Time | Task | How It Works |
|------|------|-------------|
| 5am-midnight | Email triage | Scans inbox on every check-in. Flags urgent items, drafts replies, summarizes threads. |
| 6:00am | Morning intel digest | Compiles overnight AI/tech news, trending tweets, HN discussions. Emails me a briefing. |
| 6:30am | Morning briefing | Calendar preview, meeting prep for today's calls, open tasks review. |
| 6:30am | Content drafts | Today's LinkedIn post (2 versions) + Twitter draft, ready for my review. |
| 5:00pm | Meeting follow-ups | Checks calendar for meetings that ended today, drafts follow-up emails. |
| 6:00pm | Evening briefing | Tomorrow's calendar preview, meeting prep, open tasks, today's cost summary. |

**The prompt that powers email triage (steal this):**

```
You are my Chief of Staff. Check my inbox for new emails.

For each email:
1. Read the full content
2. Categorize: URGENT / NEEDS RESPONSE / FYI / SKIP
3. For NEEDS RESPONSE: draft a reply in my voice (direct, concise, no fluff)
4. For URGENT: flag it and tell me immediately

Rules:
- Emails from [list your VIP senders] are always high priority
- Meeting invites: check my calendar for conflicts before responding
- Sales outreach / cold emails: skip silently
- Newsletters: skip unless they mention [your company/name]

Output: Summary table with sender, subject, category, and your recommended action.
```

**The prompt that powers meeting follow-ups (steal this):**

```
Check my calendar for meetings that ended in the last few hours.

For each external meeting (skip internal/personal):
1. Look up the attendee(s)
2. Draft a follow-up email:
   - Subject: "Great connecting, [Name]"
   - Tone: warm but professional, not corporate
   - Reference something specific from the meeting context
   - Include 1-2 clear next steps
   - Keep it under 150 words

Skip meetings with [list people to exclude, e.g., partner/spouse].
```

### Agent 2: LinkedIn Growth Engine

**What it does:** Runs my entire LinkedIn presence.

**Daily schedule:**

| Time | Task | Details |
|------|------|---------|
| 6:30am | Post draft | Day-specific: Mon=hot take, Tue=build update, Wed=guide, Thu=story, Fri=fun |
| 9:00am | Comments (12/day) | Finds high-engagement posts from target creators, writes substantive comments |
| 10:00am | Connection requests | 15 targeted requests to founders/operators in AI/SaaS |
| 6:00pm | Metrics capture | Logs impressions, engagement, follower growth, saves, post performance |
| Sunday 6pm | Weekly content calendar | Emails me next week's 5-post plan for review |

**The prompt that powers LinkedIn commenting (steal this):**

```
You are commenting on LinkedIn posts as [Your Name].

Voice rules:
- 1-3 sentences max
- Add a new angle, counterpoint, or specific example — never just agreement
- Reference something specific from their post
- NEVER say: "Great post", "Love this", "So true", "Couldn't agree more"
- NEVER end with a question
- NEVER use emojis or self-promote
- Tone: sharp, direct, conversational. Like a smart colleague, not a fan.

Examples of GOOD comments:
- "The counterintuitive part: the companies spending the most on AI tools are often getting the least value. It's the ones who rebuild workflows around agents — not bolt them onto existing ones — that see the 10x."
- "Ran into this exact problem. Ended up solving it by treating the LLM as a coworker with a job description, not a tool with a prompt. Changed everything about the output quality."
- "This is the part most people skip. The monitoring layer. Without it you're just hoping your agents work. With it you catch drift before it costs you."

Examples of BAD comments (never write these):
- "Great insights! Thanks for sharing." ❌
- "This resonates so much with me." ❌
- "Couldn't agree more! What tools do you recommend?" ❌

Now read this post and write a comment:
[post content]
```

**The prompt that powers daily content drafts (steal this):**

```
Today is [day of week]. Write today's LinkedIn post.

Weekly cadence:
- Monday: Hot take on AI/tech news. Contrarian angle preferred.
- Tuesday: Build-in-public update. What I shipped, what broke, what I learned.
- Wednesday: Educational guide. Tactical, saveable, step-by-step.
- Thursday: Founder story/lesson. From my experience building companies.
- Friday: Product showcase or lighter take. What I built this week, or an observation.

Today's trending topics (from intel):
[paste trending topics]

Voice rules:
- Direct, no fluff. Compressed logic.
- Conversational but sharp. Anti-hype.
- Anchor insights in concrete examples.
- Never use: em dashes, "genuinely", "incredibly", motivational fluff
- Hook must be in the first 2 lines (that's all people see before "see more")
- Sweet spot: 800-1400 characters
- No CTA unless it's offering a genuinely useful resource
- Don't mention my company by name unless it's a Tuesday build update

Write TWO versions:
1. Normal voice (direct, authoritative)
2. Witty voice (same insight, but with absurdist humor or unexpected framing)

Also write a Twitter version (280 chars max, punchier).
```

### Agent 3: Content Production

**What it does:** Creates downloadable guides, carousels, and lead magnets.

**Carousel generation prompt (steal this):**

```
Create a LinkedIn carousel (6-10 slides) on this topic: [topic]

Format per slide:
- HEADLINE: Bold, 5-8 words max
- BODY: 1-3 bullet points, under 25 words total
- Keep it scannable — people swipe fast

Structure:
- Slide 1: Hook. Make them stop scrolling. Question or bold claim.
- Slides 2-8: The meat. One idea per slide. Practical, specific, actionable.
- Slide 9: Summary or "the real insight"
- Slide 10: CTA — "Follow [name] for more" + where to get the full guide

Rules:
- Every slide must be useful on its own (people screenshot individual slides)
- Optimize for SAVES — content people want to come back to
- No fluff slides. No "let's dive in" slides. Start with value immediately.
- Include specific numbers, tools, or steps — not generalities
```

### Agent 4: Business Ops

**What it does:** The unglamorous stuff that compounds.

**Weekly cost tracking prompt:**

```
Analyze my AI tool usage for the past 7 days.

Pull costs from:
- Anthropic API usage
- OpenAI API usage (if applicable)
- Any other API costs

Break down by:
- Agent/function (which agent spent what)
- Cost category (cache writes, output tokens, input tokens)
- Day-over-day trend

Flag:
- Any single job that cost more than $20
- Any agent whose costs increased >50% vs last week
- Total weekly spend vs budget of $[X]

Output: Clean summary table + recommendations for cost reduction.
```

**Competitive monitoring prompt:**

```
Research the latest developments for these competitors: [list competitors]

For each, find:
- New product launches or features (past 7 days)
- Pricing changes
- Funding news
- Key hires
- Notable customer wins or losses
- Social media buzz (positive or negative)

Sources to check: their website, Twitter, LinkedIn, TechCrunch, Product Hunt, HN

Output: One-paragraph summary per competitor, sorted by relevance. Flag anything that requires immediate attention.
```

---

## Part 3: Copy-Paste Agent Setups (Start Here)

### Starter Agent #1: Morning Briefing (15 min setup)

This is the single best first agent. It trains you to think in schedules and outputs.

**What you need:**
- An LLM (Claude, GPT-4, etc.)
- A way to run it on a schedule (cron job, Zapier, Make.com, or an agent runtime like OpenClaw)
- Email sending capability

**The prompt:**

```
Generate my morning briefing for today.

1. TODAY'S DATE AND DAY
   - What day of the week is it? Any significance? (Monday = fresh start, Friday = wrap up)

2. CALENDAR PREVIEW
   [Paste today's calendar or connect to Google Calendar API]
   - List all meetings with times and attendees
   - Flag any external meetings that need prep
   - Note any gaps > 1 hour (these are your deep work blocks)

3. MEETING PREP
   For each external meeting today:
   - Who is this person? (Check LinkedIn, past emails)
   - What's the context? (Why are we meeting?)
   - What do I want from this meeting?
   - One conversation starter based on their recent activity

4. PRIORITY TASKS
   [Connect to your task manager or paste current tasks]
   - What's the #1 thing I should do today?
   - What's overdue?
   - What can be delegated to agents?

5. YESTERDAY'S LOOSE ENDS
   - Did I promise anyone a follow-up I haven't sent?
   - Any emails I haven't responded to that are now >24h old?

Output this as a clean, scannable email. No fluff. Just the information I need to start my day sharp.
```

**Schedule:** 6:30am daily, emailed to you.

**Expected result:** You wake up to a complete briefing. No more "what am I doing today?" No more missed follow-ups. This alone is worth 30 min/day.

### Starter Agent #2: Email Triage (20 min setup)

**The prompt:**

```
Scan my inbox for emails received in the last [X hours].

For each email, output a row in this format:
| Priority | From | Subject | Category | Recommended Action |

Priority levels:
- 🔴 URGENT: Needs response within 2 hours
- 🟡 RESPOND: Needs response within 24 hours
- 🔵 FYI: Read when you have time
- ⚪ SKIP: No action needed

Categories:
- MEETING: Calendar invites, scheduling requests
- BUSINESS: Clients, partners, investors
- INTERNAL: Team, tools, services
- OUTREACH: Cold emails, sales pitches
- NEWSLETTER: Subscriptions, digests

For 🔴 and 🟡 emails, also draft a response:
- Match my tone: [describe your email voice]
- Keep responses under 100 words unless the email requires detail
- If the email asks to schedule a meeting, check my calendar and suggest 2-3 times
- If it's a sales pitch, don't respond (just skip)

VIP senders (always prioritize):
- [list 5-10 key contacts]

Output: The summary table first, then any drafted responses below.
```

**Schedule:** Every 2-4 hours during business hours.

### Starter Agent #3: LinkedIn Content Writer (15 min setup)

**The prompt:**

```
Write today's LinkedIn post.

ABOUT ME:
- [Your name, title, company]
- [One line about what you do]
- [Your key thesis or POV]

MY VOICE:
- [3-5 bullet points describing how you write]
- [2-3 examples of posts you liked that you wrote]
- [Things you never say]

TODAY'S ANGLE:
- Check trending news in [your industry]
- Or use this topic I want to write about: [optional topic]

FORMAT:
- Hook in first 2 lines (this is all people see before "see more")
- 800-1400 characters total
- Short paragraphs (1-2 sentences each)
- End with an insight, not a CTA (unless offering something genuinely useful)
- No hashtags (they look desperate)
- No "agree?" or "thoughts?" (engagement bait)

Write the post, then tell me why you chose this angle.
```

**Schedule:** 6:30am daily. Review and post by 8am.

### Starter Agent #4: Competitive Intel (10 min setup)

**The prompt:**

```
Run my weekly competitive intelligence scan.

COMPETITORS TO TRACK:
1. [Competitor 1] — [their website] — [what they do]
2. [Competitor 2] — [their website] — [what they do]
3. [Competitor 3] — [their website] — [what they do]

FOR EACH COMPETITOR, CHECK:
- Website: Any new pages, pricing changes, or feature announcements?
- Twitter/X: What are they posting about? Any announcements?
- LinkedIn: Company page posts, employee posts mentioning new features
- Product Hunt: Any new launches?
- App stores: Version updates, new reviews mentioning features
- News: Search "[competitor name]" filtered to past 7 days

OUTPUT FORMAT:
## [Competitor Name]
**What's New:** [1-2 sentences on notable changes]
**Threat Level:** 🟢 No change / 🟡 Worth watching / 🔴 Needs response
**Action Items:** [What, if anything, should I do about this?]

ALSO:
- Are any competitors talking about features/problems I should address?
- Any gaps in the market that none of them are filling?
- Any pricing moves that affect my positioning?
```

**Schedule:** Monday mornings.

### Starter Agent #5: Meeting Follow-Up (10 min setup)

**The prompt:**

```
I just finished a meeting. Here are the details:

MEETING: [Meeting title from calendar]
ATTENDEE(S): [Names and companies]
CONTEXT: [Why we met — intro call, partnership discussion, etc.]
MY NOTES: [Paste any notes, or "no notes taken"]

Write a follow-up email:

RULES:
- Send within 2 hours of the meeting
- Subject line: Keep it natural, not corporate. "Great connecting" or reference something specific.
- Tone: Warm, professional, concise
- Structure:
  1. One sentence referencing a specific moment from the conversation (not "great meeting!")
  2. 2-3 bullet points of key takeaways or next steps
  3. Clear ask or next step with timeline
  4. Sign off naturally
- Under 150 words total
- If I didn't take notes, write a general but genuine follow-up based on the meeting context

OUTPUT: Subject line + email body, ready to send.
```

**Schedule:** Trigger after each meeting ends (check calendar every 30 min for recently ended meetings).

---

## Part 4: The Voice Profile — Your Most Important Document

The single biggest factor in agent output quality is your voice profile. Here's how to build one:

### Step 1: Collect 10 Examples of Your Writing
Find 10 emails, posts, or messages you wrote that sound most like "you." These are your training data.

### Step 2: Extract Patterns

Answer these questions by looking at your examples:

```
MY VOICE PROFILE

## How I Write
- Sentence length: [short/medium/long/varies]
- Paragraph length: [1 sentence / 2-3 sentences / long blocks]
- Vocabulary level: [simple/moderate/sophisticated]
- Tone: [formal/casual/somewhere in between]
- Humor: [never/occasionally/frequently — describe the style]

## Patterns I Use
- I tend to start sentences with: [...]
- I structure arguments as: [...]
- I use analogies from: [domain — sports, cooking, building, etc.]
- My posts usually end with: [insight/question/call to action/open loop]

## Things I NEVER Do
- Words I never use: [list them]
- Phrases I hate: [list them]
- Formatting I avoid: [emojis/hashtags/all caps/etc.]
- Tones I never take: [preachy/sycophantic/motivational/etc.]

## Examples

### Good (sounds like me):
"[paste 3-5 short examples]"

### Bad (doesn't sound like me):
"[paste 3-5 examples of writing you'd reject]"
```

### Step 3: Test and Iterate

Give the voice profile to your LLM and ask it to write something. Compare with your real writing. Where does it miss? Update the profile. After 5-10 iterations, the output should be 80-90% you. That last 10-20% is your 5-minute edit.

**Pro tip:** Keep a "rejection log." Every time an agent writes something you'd never say, add it to the "Things I NEVER Do" section. This compounds fast.

---

## Part 5: The Economics (Why This Beats Hiring)

| Function | Employee Cost | Agent Cost | What You Get |
|----------|-------------|-----------|-------------|
| Content writer (part-time) | $3-5K/month | ~$100/month API | 5 posts/week + Twitter + carousels |
| Social media manager | $4-6K/month | ~$50/month | 12 comments/day + metrics + growth |
| Executive assistant | $4-8K/month | ~$75/month | Email triage + calendar + follow-ups |
| Research analyst | $5-8K/month | ~$50/month | Daily intel + competitor monitoring |
| **Total** | **$16-27K/month** | **~$275/month** | **Same or better output** |

But cost savings aren't even the best part:

**Speed:** Agents execute in minutes, not days. Your morning briefing is ready before you wake up.

**Consistency:** No sick days, no context switching, no "I forgot." The system runs every single day.

**Scalability:** Adding a new workflow takes hours, not a hiring cycle. You write a prompt, set a schedule, done.

**Iteration speed:** Update a prompt and the improvement applies instantly across every future run. Try getting a team of 5 to change behavior overnight.

**The tradeoff:** Agents can't do relationship-heavy, high-judgment, creative-vision work. That's your job. Everything else? Agents.

---

## Part 6: Common Mistakes (And How to Avoid Them)

### Mistake 1: Automating Everything at Once
**What happens:** You spend 2 weeks setting up 10 agents. None of them work well. You give up.

**Fix:** Start with ONE agent. Get it to 80% quality. Run it for a week. Then add the next one.

### Mistake 2: No Voice Profile
**What happens:** Agent writes content that sounds generic. You spend more time editing than writing from scratch.

**Fix:** Spend 30 minutes building your voice profile (Part 4). This is the highest-ROI activity in this entire playbook. Every agent that writes in your name should reference it.

### Mistake 3: Deploying Without Review
**What happens:** Agent sends an email with a wrong fact, or posts something tone-deaf on LinkedIn.

**Fix:** Human-in-the-loop for the first 2 weeks, minimum. Every agent output gets reviewed before going external. Graduate to autonomous only after consistent quality.

### Mistake 4: Treating Agents Like Chatbots
**What happens:** You only use AI when you remember to open the tab and type something.

**Fix:** The power is in SCHEDULES and TRIGGERS. Set up cron jobs. Agent checks email at 8am, 12pm, 4pm. Agent drafts content at 6:30am. Agent captures metrics at 6pm. You don't initiate — the system runs.

### Mistake 5: No Monitoring
**What happens:** Agent quietly starts producing worse output, or costs spike, and you don't notice for weeks.

**Fix:** Build a monitoring layer from day one:
- Log every agent action
- Weekly cost report
- Quality spot-checks (review 20% of outputs weekly)
- Anomaly alerts (cost spike, unusual volume, errors)

### Mistake 6: Not Saving What Works
**What happens:** Agent produces a great email draft. You don't save it. Next week, quality is inconsistent again.

**Fix:** Build an examples library. Every time an agent nails it, save the output as a reference example in the prompt. Every time it misses, add the failure to the "never do this" section. This is how agents get better over time.

---

## Part 7: The 30-Day Quickstart

### Week 1: Foundation
- **Day 1:** Pick your first agent (I recommend Morning Briefing — see Part 3)
- **Day 1:** Write your voice profile (Part 4) — even a rough one helps
- **Day 2:** Set up the agent and run it manually once. Review output. Adjust prompt.
- **Day 3-5:** Run it on a schedule. Review every output. Note what needs fixing.
- **Day 5:** Update the prompt based on what you learned. Save good examples.
- **Weekend:** Reflect: What did this agent save you time on? What still needs work?

### Week 2: Add Agent #2
- Pick your second agent (Email Triage or LinkedIn Content — highest impact)
- Set up, run manually, review, adjust
- Keep running Agent #1 — check outputs but don't micromanage
- Start building your "rejection log" of things agents should never do

### Week 3: Connect the Dots
- Look for connections between agents (intel feed → content draft, email triage → follow-up draft)
- Add Agent #3 if #1 and #2 are running smoothly
- Build your first monitoring check (cost report or quality review)
- Update voice profile with 2 weeks of examples

### Week 4: Optimize
- Review all agent outputs from the month. What's working? What's not?
- Kill or pause anything that's not adding value
- Double down on what's working — give those agents more context, better examples
- Plan Month 2: What's the next workflow to automate?

**By end of month:** You'll have 2-3 agents running daily, saving you 1-2 hours/day, with a clear path to adding more. The compound effect starts in Month 2, when agents begin feeding each other.

---

## Part 8: Tools & Resources

### Agent Runtimes (How to Run Agents on Schedules)

| Tool | Best For | Complexity | Cost |
|------|----------|-----------|------|
| **OpenClaw** | Full agent orchestration — cron jobs, browser automation, sub-agents, multi-agent comms | Medium | Open source |
| **Zapier / Make.com** | Simple triggers + LLM calls (no coding) | Low | $20-50/month |
| **LangChain / CrewAI** | Developers building custom agent pipelines | High | Free (+ API costs) |
| **Custom scripts + cron** | Maximum control, minimal dependencies | Medium-High | Free (+ API costs) |

### LLMs I Use

| Model | What For | Why |
|-------|---------|-----|
| **Claude Opus** | Creative content, voice-sensitive writing, complex analysis | Best at matching voice, nuanced writing |
| **Claude Sonnet** | Script execution, data processing, routine tasks | 5x cheaper, good enough for non-creative work |

### Key Principle: Use Cheap Models for Routine, Expensive Models for Voice

Don't run Opus for everything. Your email triage agent? Sonnet is fine. Your LinkedIn comment writer that needs to nail your voice? That's Opus territory. This distinction alone can cut your AI costs by 60%.

---

## The Bottom Line

You don't need a team to run a company. You need a system.

AI agents aren't the future — they're available right now. The founders who adopt this model first will have an unfair advantage that compounds every month. While competitors are hiring their 10th employee, you'll be deploying your 10th agent — at 1/50th the cost and 10x the consistency.

The question isn't whether AI agents will run most business operations. It's whether you'll be early or late.

Start with one agent. Start today.

---

## Want More?

**Follow me on LinkedIn** — I post daily about building with AI agents, founder lessons from scaling Branch to a unicorn, and real-time dispatches from building in public.

→ [linkedin.com/in/mikemolinet](https://www.linkedin.com/in/mikemolinet/)

**Try OpenClaw** — the agent runtime I use to orchestrate everything in this playbook.

→ [openclaw.com](https://openclaw.com)

**Get weekly deep dives** — Follow along as I build in public at aidropdaily.com.

→ [aidropdaily.com](https://aidropdaily.com)
