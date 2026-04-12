---
id: "ai-101-day-14"
type: "course-lesson"
course: "ai-101"
course_title: "AI 101"
week: 3
day: 14
day_of_week: "tue"
lesson_type: "lesson"
title: "Analysis: Making Sense of Data, Docs, and Research"
subject: "You have an analyst on call. You're just not using them."
source_path: "week-3/day-14-tue.md"
---

# Day 14 — Analysis: Making Sense of Data, Docs, and Research
---

A friend of mine is a VP at a mid-size SaaS company. Last quarter, her team spent three days putting together a competitive analysis. They read through four competitors' websites, pulled pricing data, compared feature sets, and assembled it into a deck.

She ran the same exercise with Claude in about twenty minutes.

Not a perfect replacement. She still needed to verify claims and add her team's strategic perspective. But the assembly work, the part that took three days, was done before her coffee got cold.

This is where AI goes from "neat trick" to "I can't imagine working without this."

Let's start with the most common one: summarizing long documents. You've got a 40-page report and you need the key points in five minutes. Paste it in (or upload the PDF if your tool supports it) and say: "Summarize this document. Give me the 5 most important findings, any recommendations made, and anything surprising or counterintuitive."

That last part matters. Asking for what's surprising forces AI to go beyond a generic summary. You get the stuff you'd actually want to highlight in a meeting.

Now try comparison analysis. Say you're evaluating three vendors for a new tool. Paste in whatever you've got on each, proposals, pricing sheets, feature lists, even their websites. Then say:

"Compare these three vendors across these criteria: price, implementation time, integration with Salesforce, and customer support quality. Present it as a table with a recommendation at the bottom. Note where the data is incomplete."

That last instruction, "note where data is incomplete," is critical. Remember what we said about AI being a brilliant intern? Interns who don't flag gaps are dangerous. AI won't flag gaps unless you tell it to.

Here's one that surprises people: spreadsheet analysis. Export a CSV from your CRM or financial system. Paste it in. Ask questions like:

"What are the top 5 accounts by revenue growth quarter over quarter?"
"Which product category has the highest return rate?"
"What patterns do you see in this data that I might be missing?"

You don't need to build a pivot table. You don't need to remember VLOOKUP syntax. Just ask the question in English.

One technique I use constantly: the second opinion. You've already done your analysis. You have your recommendation. Before you present it, paste your work into AI and say: "Here's my analysis of X. What am I missing? What are the weakest points in my reasoning? What would a skeptic challenge?"

This isn't about letting AI make the decision. It's about stress-testing your thinking before someone else does it in the meeting. Think of it as a red team you can access in thirty seconds, which is exactly what we'll dig into in the next lesson.

The key with all of this is giving AI the raw material. You learned in Week 2 that context is king. For analysis, that means pasting in the actual documents, the actual data, the actual situation. Vague questions get vague analysis. Specific inputs get specific insights.

A quick note on privacy: don't paste confidential financial data or personally identifiable information into free-tier AI tools without checking your company's policy. Most paid tiers (ChatGPT Plus, Claude Pro) have stronger data handling commitments, but know the rules before you paste.

**AI is the best analyst you've ever had, if you give it the raw material.**
