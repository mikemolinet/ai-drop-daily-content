---
id: "ai-201-day-09"
type: "course-lesson"
course: "ai-201"
course_title: "AI 201: Build Your AI System"
week: 2
day: 9
day_of_week: "tue"
lesson_type: "lesson"
title: "Multi-Step AI Workflows"
subject: "One AI step is useful. Chaining five together is transformational."
source_path: "course-2/week-2/day-09-tue.md"
---

So far you've been giving AI one task at a time. Summarize this. Draft that. Organize these files. Each one useful on its own.

But the real power shows up when you chain steps together. When the output of step one becomes the input for step two, which feeds step three. When you describe a whole workflow and let AI run through it end to end.

This is the difference between using AI as a calculator and using it as a production line.

## What a multi-step workflow looks like

Here's a concrete example. Say you need to prepare a client proposal.

Without AI chaining, you'd do this: research the client's company (20 minutes), summarize your findings (15 minutes), draft the proposal (45 minutes), refine and edit (30 minutes). That's almost two hours.

With a chained workflow in Cowork, you do this: "Research [Client Company] — their recent news, quarterly results, and strategic priorities. Summarize the key findings in 3-4 bullets. Then draft a one-page proposal for [your service] that directly addresses their priorities. Save the research summary and the proposal draft as separate files in my Client Proposals folder."

One prompt. Multiple steps. Cowork handles the research, the synthesis, the drafting, and the file creation. You review the output and refine from there. Total active time: maybe 15 minutes of review and editing instead of two hours of creation.

## Cross-app workflows

This is one of Cowork's newer and most impressive capabilities. It can work across applications in a single workflow.

Real example: "Read the Q1-sales-data.xlsx file in my Reports folder. Analyze month-over-month trends, identify the top 3 performing products, and flag any concerning declines. Then create a PowerPoint presentation with 5 slides summarizing the analysis, including a chart showing the trend data. Save both an updated Excel file with your analysis notes and the PowerPoint to my Q1 Reports folder."

Cowork reads the Excel data, does the analysis, then creates a formatted PowerPoint with that analysis baked in. Context flows from one app to the next without you copying and pasting anything.

Think about how you'd normally do this. Open Excel. Stare at numbers. Open PowerPoint. Recreate the key data points. Format slides. Go back to Excel to double-check a number. Fix the slide. That back-and-forth is exactly the kind of friction that eats hours every week.

## Using AI output as AI input

This principle extends beyond Cowork. Any time you're working with AI, you can feed output from one session into another.

For example: use Perplexity to research a topic and get sourced summaries. Copy those summaries into Claude and ask it to draft a report. Take the draft into ChatGPT and ask it to rewrite the executive summary for a C-suite audience.

Each AI adds its strength. Perplexity is great at sourced research. Claude handles nuanced writing. ChatGPT is solid at reformatting for specific audiences. You're the conductor. They're the orchestra.

## When to use one conversation vs. many

A natural question: should you do all of this in one long Cowork session, or break it into separate conversations?

**Use one long conversation when:**
- The steps are tightly connected (research feeds directly into a draft)
- Context from earlier steps matters for later ones
- You want Cowork to make judgment calls based on the full picture

**Use multiple conversations when:**
- The steps are distinct tasks (organizing files vs. writing a report)
- You want to review and adjust between steps
- One step is experimental and you don't want a bad result to pollute later steps
- You're hitting usage limits and need to be strategic about token consumption

In general, err toward one conversation for connected workflows and separate conversations for independent tasks. When in doubt, try it in one and see if the quality holds up across all the steps.

## Building your mental model

The key insight here isn't about any specific tool. It's about thinking in workflows instead of tasks.

Most people approach their work as a list of discrete tasks. Write the report. Make the slides. Send the email. Each one gets individual attention.

Power users think in chains. What feeds into what? Where does one output naturally become the next input? Where am I doing the tedious connecting work between steps?

That connecting work — the formatting, the copying, the context-switching between apps — is exactly where AI shines. Not because it's smarter than you at any single step, but because it doesn't lose context between them.

## Today's exercise: build a multi-step chain (15 minutes)

Pick one real workflow from your work. Something that involves at least three distinct steps. Here are some ideas:

- **Meeting prep chain:** Research attendees → summarize key background → generate talking points and questions → create a one-page briefing doc
- **Content creation chain:** Research a topic → outline key points → draft the piece → create social media excerpts
- **Report chain:** Gather data from multiple files → analyze trends → draft narrative summary → format as presentation
- **Client work chain:** Review client's recent communications → identify key themes and concerns → draft response or proposal

Open Cowork and describe the entire chain in one prompt. Be specific about what each step should produce and where the final outputs should be saved.

Review what comes back. Where did it nail it? Where did it miss? Refine the prompt and run it again. That refinement process is how you build workflows you can reuse every week — and eventually schedule to run automatically (hello, yesterday's lesson).

## What's coming tomorrow

Tomorrow we're going bigger: working with documents and data at scale. Not "summarize this one PDF" but "process this entire folder of documents and turn the chaos into structured data." That's when things get seriously practical.

**A single AI prompt saves you minutes. A chained AI workflow saves you hours. Build the chains.**
