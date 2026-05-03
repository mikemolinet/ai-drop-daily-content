---
title: "AI's Biggest Bottleneck Right Now: The Human Middleware"
description: "Eight AI agents, all individually capable, none of them talking to each other. The bottleneck isn't intelligence — it's the human sitting in the middle, copying context between windows."
category: "AI Agents"
type: "article"
author: "Mike Molinet"
authorLinkedin: "https://www.linkedin.com/in/mikemolinet/"
publishedAt: "2026-04-16"
---

# AI's Biggest Bottleneck Right Now: The Human Middleware

I have eight AI agents running right now. They write code, research industry developments, draft content, monitor my inbox, scope features, coordinate handoffs between each other.

They're good. Individually, they're very good. I can hand one a vague brief at 9 AM and come back to a finished research doc 20 minutes later. Another watches my calendar, reads the attendee list, and has background context ready before I join a call. A third writes code in a day that previously would've taken a week+.

But here's what my day actually looks like.

Agent A finishes a research brief. It pings me. I read it, pull out the three things that matter, paste them into Agent B's conversation window. Agent B drafts something. I review it, realize it needs data from Agent C's output, so I go copy that, bring it back. Agent C needs context from something Agent A found an hour ago, but Agent C doesn't know Agent A exists.

I'm not doing work. I'm routing messages between things that do work.

The agents don't share state. They don't talk to each other. They have no idea the others exist. The only shared context in the entire system is me, a human sitting in the middle, copying and pasting between windows.

I've become the middleware between my own tools.

---

## This Problem Is 2,000 Years Old

Jack Dorsey and Roelof Botha published an essay on Block's blog in March called "From Hierarchy to Intelligence." They traced a line from the Roman Army to the modern corporation and made a point I keep coming back to.

The Roman Army organized into groups of eight soldiers, led by one guy. Ten of those groups formed a century. Six centuries made a cohort. Ten cohorts made a legion. At every level, a named commander aggregated information from below and relayed decisions from above. The structure (8 → 80 → 480 → 5,000) was an information routing protocol. It existed because one human can effectively coordinate somewhere between three and eight other humans. That's it. That was the entire constraint.

The Prussian military formalized it further after getting destroyed by Napoleon. They invented the General Staff, a dedicated class of officers whose job wasn't to fight but to route information, pre-compute decisions, and maintain alignment across units. This was middle management before the term existed.

When railroads exploded in the 1850s, they borrowed the whole playbook. Every corporation on earth still runs on that blueprint. The fundamental constraint hasn't changed in two millennia: humans need layers to coordinate, and those layers slow everything down.

Dorsey and Botha: "The question was never whether you needed layers. The question was whether humans were the only option for what those layers do."

For two thousand years, the answer was yes. It might not be anymore.

---

## The Org Chart Nobody Drew

I didn't realize I'd recreated this problem until I looked at my own setup and saw it.

Imagine a team where every person reports directly to one manager. No shared tools, no cross-functional communication, no project management system. Just eight people doing their jobs in isolation, and one person trying to hold the entire context graph in their head.

The individuals aren't allowed to talk to each other or work on shared documents. They can only communicate back to the manager, and then the manager communicates to the others.

Every handoff goes through that one person. Every piece of context gets manually relayed. Every bottleneck traces back to the same node.

Nobody would design a team this way. You'd look at it and immediately say this doesn't scale. That one person becomes the constraint. The team's output is capped by one person's bandwidth.

That's what it looks like when you're running multiple AI agents right now. Whether you're an engineer with a coding agent, a research agent, and a documentation agent. A marketer with a content agent, an analytics agent, and a scheduling agent. An executive with a briefing agent, an email agent, and a strategy agent. The pattern is the same.

The agents are the team. They're capable, fast, increasingly autonomous. But the coordination layer between them is you. Clicking between windows, remembering which agent has which context, manually bridging every gap.

---

## Intelligence Isn't the Bottleneck

The AI industry is pouring billions into making models smarter. Bigger context windows, better reasoning, faster inference. That stuff matters.

But the constraint most people hit isn't intelligence. The agents are smart enough. The code agent writes (somewhat) decent code. The research agent finds real insights. The content agent drafts things you can actually use.

The constraint is plumbing.

There's no shared state layer where Agent A's output automatically becomes Agent B's input. There's no event system where finishing one task triggers the next. There's no way for agents to ask each other questions without routing through you.

Y Combinator just released their Summer 2026 Requests for Startups, and one of the categories is called "Company Brain." Their framing: "The biggest blocker to AI automation of companies is no longer the models. They just got so good so quickly. Now the blocker is the domain knowledge."

They describe the company brain as a system that "pulls knowledge out of all these fragmented sources, structures it, keeps it current, and turns it into an executable skills file for AI." Not a chatbot over documents. A living map of how work actually gets done, how decisions are made, how one team's output feeds into another team's input.

They're calling it a new primitive. Anyone who's been duct-taping agent workflows together knows exactly what they mean.

---

## The Copilot Trap

Dorsey and Botha made another point worth sitting with. Most organizations using AI today are giving people copilots. A coding assistant. A writing helper. A research tool in a browser tab.

Their words: "That makes the existing structure work slightly better without changing it."

You've made each node in the network smarter, but the network topology is identical. The same human routes information between the same siloed tools. You just made each tool faster at the thing it already does.

It's the difference between giving every soldier a better sword versus replacing the messengers on horseback with radios. One is an incremental improvement to what exists. The other changes how coordination works.

Most people running AI agents right now are in the better-sword phase. Each individual agent is capable. The coordination model hasn't been touched.

Garry Tan, YC's CEO, open-sourced his personal AI setup recently. He's shipping 40+ features in 60 days, part-time, while running YC full-time. He built a system called gbrain, a self-wiring knowledge graph where his agents ingest meetings, emails, tweets, and voice calls while he sleeps. He's running 21 autonomous cron jobs. He built the coordination layer himself because it doesn't exist as a product.

When the most connected person in the startup ecosystem has to build his own agent plumbing from scratch, the infrastructure gap is real.

---

## What Comes Next

Right now, the AI agent conversation is mostly about coding. Every demo is "watch this agent write a React app." But coding is a controlled environment: one language, one repo, one clear output. The coordination problem there is relatively contained. Agents can update Github with their files and other agents can pull those same files. It's not real-time but at least there's some amount of a shared state.

Think about what happens when agents move into every function. Sales qualifying leads. Finance reconciling invoices. Ops flagging supply chain disruptions. Marketing optimizing spend. Legal reviewing contracts. Each individually achievable today. But the sales agent closing a deal affects the ops agent's capacity planning. The finance agent's budget revision changes what marketing can spend. Legal flags a clause sales needs to know about before the next call.

That cross-functional coordination doesn't scale linearly. Every new agent multiplies the routing complexity. And right now, every one of those routes goes through a human.

Diana Hu, a YC partner, taught a Startup School session on building AI-native companies this month. Two of her slides are blunt:

**Make your company queryable.** Every action produces an artifact the system can learn from. Record meetings. Minimize DMs. Embed agents in comms. Provide models with as much context as you would provide a colleague.

**No more human middleware.** If your organization is queryable, artifact-rich, and legible to AI, you should have almost no human middleware. Your velocity is only as fast as your information flow. Every layer of human routing you remove is a direct speed gain.

YC's RFS has a separate category called "Software for Agents," arguing every major software category needs to be rebuilt for agents as first-class users. Block, whether you read their 40% layoff as cost-cutting or thesis-execution, is restructuring around three roles instead of a management hierarchy, betting AI can replace what hierarchy does. Inside the YC orbit and adjacent to it, multiple signals are pointing the same direction.

---

## What the Coordination Layer Looks Like

So what would it actually take?

At minimum: a shared state layer that lets agents read each other's outputs without human copy-paste. An event bus where completing one task can trigger the next. Identity and permissions so agents can interact with each other's tools directly. Some kind of context protocol so Agent C can pull what Agent A learned two hours ago without me relaying it.

Think less "AI platform" and more "infrastructure primitive." The way S3 solved storage or Stripe solved payments. Not the application on top. The plumbing underneath that makes applications possible.

Nobody has built this yet. There are early pieces: Google's A2A protocol, Anthropic's MCP, a handful of startups working on agent communication layers. But the full coordination fabric, the thing that would let six agents on different platforms share state, trigger workflows, and resolve dependencies without routing through a human? It doesn't exist.

The people furthest ahead, the ones running real multi-agent setups day to day, are building their own with duct tape and cron jobs. That's usually the sign an infrastructure layer is about to emerge.

---

## The Diagnosis

I started this by describing my own setup. Copying context between windows. Being the only shared state in a system of increasingly capable machines. Spending my day routing messages instead of making decisions.

That turns out to be a specific instance of a much older problem. For two thousand years, the only way to coordinate complex work was to route information through layers of humans. We built every organization on earth around it. And now, for the first time, there's a plausible alternative, but the infrastructure to actually implement it barely exists.

We've proven that individual agents can do real work. That debate is over. The next question isn't whether agents are useful. It's whether they can work together without a human manually stitching every interaction.

Right now, they can't. And the people who've gone deepest on AI agents, across every role, every industry, are all hitting the same wall.

The bottleneck isn't intelligence. It's coordination. And whoever builds the layer that solves it will change how work gets done.
