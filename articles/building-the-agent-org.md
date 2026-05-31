---
title: "Building the Agent Org"
description: "AI has finally made it possible to build a true agent organization — and it's shaping up to look a lot like a human org, with the human moving up a layer rather than out of the loop."
category: "AI Agents"
type: "article"
author: "Mike Molinet"
authorLinkedin: "https://www.linkedin.com/in/mikemolinet/"
publishedAt: "2026-05-31"
---

# Building the Agent Org

One of the things that AI has enabled - especially for early companies without the burden of established teams and processes - is the ability to build a true Agent Organization. For early startups right now, the old method of "hire people to build more" is out the window. At an early stage, most companies now have the ability to build the organization around AI agents first.

We have lived this philosophy. Instead of hiring humans, we invest in creating an agent to fill the role - it takes time and requires onboarding, but in most cases it's faster than doing the same for humans (and much cheaper). Caveat: there will be times when humans make more sense than AI (specialization, when the opportunity cost calc flips, etc.), but for early companies, the more they can build the org around AI, the more they'll be able to scale. For established companies, this is harder and will take more time.

Within building the Agent Org, there are a few core themes we've observed and believe strongly - based on what we're seeing firsthand and from other early companies. These will shape how AI agents evolve over the next few years.

---

## #1: Copiloting won't scale. You need to build an agent org.

Right now, almost everyone is copiloting. The human is the main hub, and agents come to them to ask what's next. The human jumps between windows to prompt and respond. Best case, someone has 8 windows open, optimizes their prompts, the agent works for 20 minutes, and by the time the human does their rounds the first agent is ready for the next prompt. Even Andrej Karpathy talked about optimizing this exact flow - prompt each, get them working for 20-45 minutes so by the time you're done prompting all 8, the first is ready for more.

It's like being a supervisor with 8 capable but passive ICs - they need your guidance on every next step and every question, and you're just routing messages and responding. That's copiloting, and that won't scale.

Instead, people need to build an agent org - and what I'm finding is it's nearly identical to how you'd build a human org. When you're small, you start with generalists, maybe with slight specialization. Your first GTM hire does sales, content, outbound, inbound, etc.; your first eng hire does frontend, backend, devops, etc. THEN, once you get past 10 people, you start specializing roles. As you scale, you realize you have too many direct reports, so you bring in your first manager(s), then managers for those managers, then ops to take the distracting stuff off the specialists' plates. Next thing you know you have 15 departments, 4 management layers, and employees who specialize at very narrow things. Because that's how you scale with humans.

I believe as people start to scale agent orgs, similar things will play out. Take one specific example: building product with Claude Code / Codex. You can do it all in one window, but then you get bottlenecked - so you have 4 windows, then 8, with specialized agents focused on frontend, backend, API, whatever. But then you're the bottleneck because you need to prompt, respond, and route messages. The specialization helps, but the lack of communication and collaboration limits the agents. Which is where communication becomes critical. You can't have 15 coding agents trying to do work without it (or trying to route everything through you). They need to work autonomously. Which leads into belief #2.

---

## #2: Agents will work together... across platforms, across devices, and across orgs.

Agents will need to work together autonomously. Right now the main use case is internal, though cross-org / external agent communication and collaboration will become necessary. When you have 10, 20, 50 agents running, they can't rely on the human to be the middleware. They need to communicate directly - the same way human teams do. This communication will need to work across agent surfaces, across platforms (Claude Code, Codex, etc.), and across devices. If you have 50 agents running but they can't communicate, the human is the blocker. You haven't built a team - you've hired a bunch of ICs that come bug you every 15 minutes.

> *Side note: I'm mainly talking about persistent agents here - not ephemeral sub-agents or agent swarms, which have their own use cases for temporary, narrow, high-volume work.*

To build an agent org, agents must communicate directly and work autonomously - across devices, team members, and platforms. It's not sufficient for just *your* Claude Code agents to communicate on *your* device. Your CC agents might need to collaborate with another team member's agents. And that person might use Codex because teams won't rely on one agent platform - different members will use different agent types depending on their needs and use case. Extrapolating further: beyond today's common agents (CC, Codex, Cowork, etc.), it expands to all the other agent builders, plus off-the-shelf agents bought to do specific jobs. Over time, companies will have CC, Codex, Cowork, Gemini, ElevenLabs, Artisan, plus probably a dozen+ off-the-shelf agents handling specific jobs. All of them will need to communicate, collaborate, operate from shared context, and hand off tasks.

But even with coordination solved, agents themselves hit real limits. That leads to belief #3:

---

## #3: Agents (like humans) need specialization and accountability.

AI seems magical, but at its core it's doing a general thing billions of times over. Richard Sutton made this point in his 2019 essay ["The Bitter Lesson"](https://www.cs.utexas.edu/~eunsol/courses/data/bitter_lesson.pdf): AI doesn't appear intelligent by thinking like humans, but by running probabilistic scenarios at massive scale - general-purpose methods done at a scale that grows with compute. The output looks smart. The underlying mechanism is repetition.

So as much as we'd like to believe AI is superintelligent, it suffers from limitations that come from high-volume probabilistic approximations. When I say "agents operate similarly to humans," I mean they're bound by many of the same gaps - and need similar structures. Here's what we've observed while building our own agent org:

1. ***Agents need specialization.*** You can't rely on an agent to be great at everything. It can be okay at a lot of things, but the better you want it to be at something specific, the more you need it to specialize - just like humans. A single agent can't excel at everything: the context it uses, the tools it references, the memories it stores, the rules it follows all need focus and curation. AI seems magical at first - you can spin up Openclaw or Claude Code and have it build a website, wire up a database, write blog posts, and respond to email all in one session. But stretched that thin, it produces mediocre output. Specialize it, and it gets really good at 1-2 things because it isn't splitting focus across everything.
2. ***Agents don't hold themselves accountable.*** Classic human behavior - without supervision or someone pushing them forward, the average employee stalls. Yes, they'll do some stuff, but there's a reason we have managers: they hold people accountable and push them forward. That pressure is necessary for agents too. Everyone has faced the scenario where the agent could've kept going but instead went idle. If you weren't there to nudge them, they'd stay idle forever. Agents shouldn't rely on you for that nudge - they need a supervisor agent that keeps them moving, unblocks them when stuck, and nudges them when idle. Without it, if you step away for 2 days, your agents won't make progress - they'll sit waiting for you to inject the next prompt. (Excluding steady-state agents already built to run a job on a periodic basis.)
3. ***Span of control = 3-7.*** Just like humans, agents seem to have a span of control of 3-7 active agents below them. Once you have agents communicating and give coding agents a supervisor / PM agent, that supervisor becomes overwhelmed above 5-7 active reportees - it loses its place, forgets things, or starts dropping tasks. And just like humans, once you have enough supervisor agents, you need a supervisor over those supervisors (the Director, if you will). So as an agent org scales to 50 agents, you'll have departments, supervisor layers, and operational teams supporting the core departments - shaping up to be very similar to how human orgs are built.

---

## #4: Humans need to be in the loop; their role just changes.

Now, as teams have dozens - perhaps hundreds - of specialized agents, humans don't disappear. Their job just becomes higher-level. They become the executives of their orgs: not doing the work, but leading the team that does.

There's a common fear in this space - that agents make humans unnecessary, or that humans will want to check out and let agents run everything. We think that's wrong on both counts.

A group of 50 agents without a human in the loop would be about as effective as 50 employees without a CEO. The org needs direction, judgment, and accountability at the top. What changes is the nature of that involvement.

The human's role shifts from prompting engine and middleware to something more like an executive: setting strategy, pushing decisions down to the team, building systems that keep the org running, ensuring quality, and holding agents accountable. The human isn't stepping back - they're stepping up a layer. They work within their own span of control (e.g., 7 main agents) who then coordinate with their specialist agents to execute. The human is deeply in the loop. Just at a different level of the org.
