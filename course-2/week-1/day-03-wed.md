# Subject: Your Course 1 custom GPT was a first draft. Now build a real one.

In the first course, you built a Custom GPT or Claude Project. And it probably works... okay. It handles the basics. It saves you some time. But if you're honest, you still do a lot of editing on the output.

Today we're going from "okay" to "near-final on the first try."

The difference isn't the tool. It's how you set it up. Most people write instructions that are too vague, skip the examples entirely, and never iterate on the system prompt. They build a first draft and call it done. That's like hiring someone, giving them a one-paragraph job description, and wondering why they need constant correction.

Today you're building an assistant so well-defined that its output requires touch-ups, not rewrites.

## Picking the right task

Go back to your audit from Day 1. Look at your green tasks — the ones where AI could handle 80%+.

Pick the one that's:
- **Recurring:** You do it at least weekly
- **Structured:** It follows a similar pattern each time
- **Time-consuming:** It currently takes you 30+ minutes
- **Not creative:** The value is in the execution, not the original thinking

Good candidates: weekly reports, meeting summaries, client updates, email responses to common requests, data analysis with a standard format, onboarding docs, status updates, SOPs.

Bad candidates: strategy documents, creative campaigns, anything that requires fresh thinking every time. Those benefit from AI collaboration, not AI automation. We'll cover that later.

Got your task? Good. Let's build.

## Building a Custom GPT

If ChatGPT is your primary tool:

**1. Go to Explore GPTs → Create.**

**2. Write the system prompt.** This is the most important part. Here's a framework:

```
ROLE: You are [specific role]. You help [who] with [what].

CONTEXT: [Background about the work, the audience, the standards]

TASK: When given [input], produce [output] in the following format:
[Describe the exact format, structure, sections]

RULES:
- [Specific rule 1]
- [Specific rule 2]
- [What to always include]
- [What to never do]

EXAMPLES:
[Paste a real example of good output. This is the single most important thing you can include.]
```

The example is everything. Without it, you get generic output that roughly matches your instructions. With it, you get output that matches the actual quality and style you want.

**3. Upload reference files.** Past examples of the completed task. Templates. Style guides. Any document the AI should reference.

**4. Set conversation starters.** Write 2-3 prompts that match how you'll actually use this. Like: "Here are my notes from this week's client calls. Write the weekly update." This saves you from staring at a blank text box.

## Building a Claude Project

If Claude is your primary tool:

**1. Create a new Project.** Give it a clear, specific name. Not "Work Stuff." Something like "Weekly Client Report Generator" or "Meeting Summary Writer."

**2. Write the project description.** Same framework as above — role, context, task, rules, examples. Claude's project descriptions can be long, so don't hold back on detail.

**3. Upload reference documents.** This is where Claude really shines. Upload:
- 3-5 past examples of the completed task (the more, the better)
- The template or format you use
- Any reference material the AI needs (client list, product info, terminology)
- A "what good looks like" doc if you have one

**4. Test with real data.** Open a conversation in the project. Give it your actual input from last week. Compare the output against what you actually produced.

## The iteration loop

Your first version won't be perfect. That's fine. Here's how to dial it in:

**Round 1:** Build it, test it with real data. Look at the output. What's wrong?

**Round 2:** Fix the instructions based on what went wrong. Common fixes:
- Output too long → Add "Keep the total length under [X] words"
- Wrong tone → Add a specific example of the right tone
- Missing sections → Explicitly list required sections
- Too generic → Add more context about your specific situation
- Including stuff you don't want → Add explicit "never do X" rules

**Round 3:** Test again with different input. A good assistant works across multiple instances of the task, not just the one you designed it for.

**Round 4:** Use it for real work this week. Note what needs adjusting and refine.

Most people stop after Round 1 and conclude "it's okay but not great." The people who get to Round 3 or 4 end up with an assistant that genuinely saves them hours.

## Real examples of what people build

To spark ideas:

**A consultant** built a GPT called "Engagement Summary Writer." She feeds it her raw notes from client sessions and it produces a structured summary with key decisions, action items, owner assignments, and follow-up dates. Used to take 45 minutes. Now takes 5 minutes of review.

**A sales manager** built one called "Deal Review Analyzer." He pastes in a deal summary and it produces a structured risk assessment: deal strengths, red flags, missing information, suggested next steps. It follows the same framework his VP uses in deal reviews.

**A recruiter** built one for writing candidate outreach emails. She uploaded 20 of her best-performing outreach messages. The GPT now writes first drafts that match her voice and hit rate. She edits for 2 minutes instead of writing from scratch for 15.

Notice the pattern: structured input, structured output, narrow scope, real examples loaded.

## Today's exercise

Build your assistant. Spend 15-20 minutes on it.

1. Pick your task
2. Write the system prompt using the framework above
3. Include at least one real example of good output
4. Upload reference docs
5. Test it with real data from last week
6. Do at least two rounds of refinement

When you're done, you should have something that produces 80%+ quality output on the first try for that specific task. If it doesn't, keep iterating on the instructions.

Use it for real this week. We'll reference it again on Saturday in the lab.

## What's coming tomorrow

You've now got AI that knows who you are and an assistant that's built for your most important recurring task. But you're still writing prompts from scratch for everything else. Tomorrow we fix that with prompt libraries — reusable, parameterized prompts that you save once and use forever.

**A generic AI gives you generic output. A purpose-built AI gives you near-final work. The difference is 20 minutes of setup.**
