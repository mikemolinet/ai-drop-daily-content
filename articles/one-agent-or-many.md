---
title: "When to Run One Agent, and When to Run Many"
description: "One agent for a dependency chain, a fleet for independent streams. The real skill isn't prompting — it's matching the concurrency to the shape of the work."
category: "AI Agents"
type: "article"
author: "Mike Molinet"
authorLinkedin: "https://www.linkedin.com/in/mikemolinet/"
publishedAt: "2026-08-12"
---


My co-founder shipped our entire billing and models release last week inside a single agent session. One window, one objective, Friday night to Monday morning. He pulled every other agent off his machine to do it.

That surprised me, because most of what we do runs the other way. The two of us operate the whole company with something like forty agents going at once, all in parallel, all on different work.

Same two people, two completely opposite modes. What decides which one you want has nothing to do with the tool. It comes down to the shape of the work.


## Building wants one agent, focused

When you are building something real, deep work aimed at one hard objective, you want a single agent with your full attention on it. The work is sequential. Step two depends on step one. You are making a hundred small judgment calls an hour and the agent needs all of your context at once. Split your focus across five parallel sessions and you get five half-finished things and a headache.

This is why core engineers reach for one Claude Code session and stay there all day. They could run more. The work itself just doesn't want to be split up. A building doesn't go up faster because you added a second architect who can't see the first one's drawings.


## Running a company wants many agents at once

Now look at how you actually run operations. Outbound is finding and enriching leads. Content is shipping and pulling in traffic. Support is triaging tickets. Something is prepping your meetings. None of those depend on each other. They are independent streams that happen to share one owner: you.

That work is built for parallelism. You want a fleet, each agent owning its lane, all of them running while you sleep and surfacing the few things that actually need you. This is where an AI workspace earns its keep, a place where a person and a set of agents run the whole operation together instead of one chat window you keep circling back to.

The common mistake is running an entire business through a single agent, one task at a time, and then wondering why it feels like a bottleneck. It feels like one because it is one. You took work that was naturally parallel and forced it through a single thread.


## Match the concurrency to the work

Here is the rule I would hand my past self. Before you spin up anything, ask one question: does this work have a dependency chain, or is it a set of independent streams?

If it is a chain, deep building toward one objective, use one agent and give it everything you have. If it is streams, the many jobs a company needs running just to stay alive, use many and let them go.

Most people get this backwards at least once. They try to parallelize the one thing that needed their whole focus, or they push their entire operation through a single sequential chat. Fix the match and the same set of tools that felt clumsy an hour ago starts feeling like a team.

The models are good enough now that this is the actual skill: knowing when the work wants one deep thread and when it wants a fleet. Prompting and model choice are the easy part. Get the concurrency right and two people can run what used to take fifty.
