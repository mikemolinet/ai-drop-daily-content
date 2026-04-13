---
id: "ai-201-day-04"
type: "course-lesson"
course: "ai-201"
course_title: "AI 201: Build Your AI System"
week: 1
day: 4
day_of_week: "thu"
lesson_type: "lesson"
title: "Prompt Libraries & Templates"
subject: "Stop writing prompts from scratch. You're wasting the best ones."
source_path: "ai-201/week-1/day-04-thu.md"
---

Yesterday you built a custom assistant for your most important recurring task. Today we're solving the other 90% of your AI use.

Think about how you currently use AI. You open ChatGPT or Claude. You stare at the text box. You type something out. You get a result. Maybe it's great. Maybe you tweak and re-prompt a few times until it is. Then you close the tab.

Next week, same task comes around. You open a new chat. You stare at the text box again. You try to remember what you typed last time. You write something similar — but not quite as good, because you forgot the specific phrasing that made it click.

This is like writing the same email from scratch every Monday morning. Nobody does that. You'd use a template. You'd save the version that worked.

But for some reason, most people treat prompts as disposable. Write it, use it, forget it.

That stops today.

## Your prompt library

A prompt library is exactly what it sounds like: a saved collection of your best prompts, organized by task, ready to grab and use whenever you need them.

Not a collection of generic prompts you found on Twitter. Your prompts. The ones you've refined through actual use. The ones that produce the output you actually want.

Here's why this matters more than it sounds: the difference between a mediocre prompt and a great one is usually 3-4 rounds of iteration. The phrasing, the constraints, the format instructions, the examples — you dial all of that in through trial and error. That iteration is valuable. When you don't save the result, you're throwing away work.

Go back to your Day 1 audit. Look at all those green and yellow tasks. Your custom assistant from yesterday handles one of them. The prompt library handles the rest.

## Building it: start with your top 5

Open a new doc — Google Docs, Notion, Apple Notes, a text file, whatever you'll actually use. (That last part is key. The fanciest system you don't check is worse than a messy doc you check daily.)

From your audit, pick the 5 tasks where you most frequently use AI or wish you did. For each one, write out the prompt that gets you the best result.

Here's the key: don't write abstract prompts. Write the actual, complete prompt you'd paste into a chat window. Include the context, the format, the constraints, the tone — everything.

A bad library entry looks like this:
> "Summarize meeting notes"

A good library entry looks like this:
> "Here are the raw notes from a [TEAM/CLIENT] meeting on [DATE]. Summarize them into the following format: (1) Key Decisions — bullet list, each with the decision and who made it. (2) Action Items — table with columns: Task, Owner, Deadline. (3) Open Questions — anything unresolved that needs follow-up. (4) Notable Quotes — any direct statements worth preserving verbatim. Keep the total summary under 500 words. Use plain language, not corporate jargon. If a deadline wasn't specified, flag it as 'TBD — needs follow-up.'"

See the difference? The second one produces near-final output every time. The first one produces something you need to heavily edit.

## Parameterized prompts: the fill-in-the-blank approach

You probably noticed the brackets in that example — [TEAM/CLIENT], [DATE]. Those are parameters. Variables. Fill-in-the-blanks.

This is what turns a good prompt into a reusable template. The structure stays the same. The specifics change each time you use it.

Think about it like a form letter. The format, tone, and instructions are locked in. The names, dates, and details get filled in before you hit send.

A few more examples of parameterized prompts:

**Weekly status update:**
> "Write a weekly status update for [PROJECT NAME]. Here's what happened this week: [PASTE RAW NOTES]. Format: (1) Progress — what moved forward and key metrics. (2) Blockers — anything stalled and why. (3) Next week — planned priorities. Tone: direct and factual, no spin. Keep it under 300 words. This goes to [AUDIENCE — e.g., 'my VP who wants headlines, not details']."

**Email response:**
> "Draft a response to this email: [PASTE EMAIL]. Context: [YOUR RELATIONSHIP TO THE SENDER AND ANY RELEVANT BACKGROUND]. Goal of my response: [WHAT YOU WANT TO ACHIEVE]. Tone: [e.g., 'warm but professional — this is a long-term client']. Keep it under [LENGTH] and don't over-apologize."

**Content brainstorm:**
> "Give me 10 ideas for [CONTENT TYPE — e.g., 'LinkedIn posts'] about [TOPIC]. Target audience: [WHO]. Each idea should include a one-line hook and a 2-sentence description of the angle. Avoid anything generic or obvious. I'd rather have 5 surprising ideas than 10 safe ones."

The parameters make each prompt infinitely reusable without being generic. You get the consistency of a template with the specificity of a custom prompt.

## Prompt chaining: when one prompt isn't enough

Some tasks are too complex for a single prompt. Not because AI can't handle them — because you get better results by breaking them into steps.

This is prompt chaining: the output of one prompt becomes the input for the next.

Here's a simple example. Say you need to write a project proposal.

**Prompt 1 — Research:** "Here's a brief description of the project: [DESCRIPTION]. Research and outline the key considerations, risks, and opportunities. Don't write the proposal yet — just give me the raw thinking."

**Prompt 2 — Structure:** "Based on this research [PASTE OUTPUT FROM PROMPT 1], create an outline for a project proposal. Include these sections: Executive Summary, Problem Statement, Proposed Solution, Timeline, Budget Considerations, Risks & Mitigations."

**Prompt 3 — Draft:** "Write the full proposal following this outline [PASTE OUTPUT FROM PROMPT 2]. Tone: [TONE]. Audience: [WHO]. Keep it under [LENGTH]."

Why not just say "write me a project proposal"? Because each step lets you review and redirect before the next one builds on it. You catch bad assumptions in the research phase instead of discovering them buried in a finished draft. You adjust the structure before the prose gets written. You stay in control.

Think of it like directing someone's work. You wouldn't say "go build the whole thing and show me when you're done." You'd check in at milestones. Same principle.

For your prompt library, save chains as sequences. Label them "Step 1," "Step 2," "Step 3" with notes about what to review between steps.

## Today's exercise

You're building your prompt library. Set a timer for 20 minutes.

1. Open a doc you'll actually revisit (not a random note you'll forget about).

2. Pick 5 recurring tasks from your Day 1 audit. At least two should be tasks your custom assistant from yesterday doesn't cover.

3. For each task, write a complete parameterized prompt. Include the brackets for fill-in-the-blank variables. Make each one specific enough that you could hand it to someone else and they'd know exactly what to paste into AI.

4. For at least one task, build a 2-3 step prompt chain instead of a single prompt.

5. Test at least two of your prompts with real data right now. Refine anything that doesn't produce good output on the first try.

When you're done, you should have a doc with 5+ reusable prompts that cover your most frequent AI tasks. Keep it open. Keep it handy. Add to it whenever you craft a prompt worth saving.

## What's coming tomorrow

So far this week, everything we've built lives in chat windows. You type a prompt, AI responds, you copy the output somewhere else. It works, but there's friction.

Tomorrow we're introducing something that changes the game entirely: Claude Cowork. Instead of chatting with AI about your work, you point AI directly at your files — on your computer — and it does the work there. No uploading, no copy-pasting, no back-and-forth. It reads your documents, edits your spreadsheets, and creates presentations right where they live. It's the moment where AI stops being a chat tool and starts being a coworker. That's tomorrow.

**The best prompt you'll ever write is the one you never have to write again. Save it, parameterize it, reuse it forever.**
