---
title: "Memory Is the Past. State Is the Present."
description: "AI tools finally remember what happened, but none of them can see what every other tool is doing right now, which is why running a dozen agents still feels broken."
category: "AI Agents"
type: "article"
author: "Mike Molinet"
authorLinkedin: "https://www.linkedin.com/in/mikemolinet/"
publishedAt: "2026-06-03"
---

![A person routing live context between AI agents, the human as the connective tissue](https://aidropdaily.com/article-assets/memory-vs-state/hero.jpg "Right now, you are the shared state.")

The big thing everyone talked about this year was memory. Your tools finally remember you. ChatGPT recalls that you're allergic to shellfish and that you prefer Python. Claude carries facts between conversations. Every agent framework ships some flavor of long-term memory, vector store, retrieval layer. The pitch is always the same: it remembers, so you don't have to repeat yourself.

That's real, and it helps. But it solved a problem that was never the thing slowing me down.

I run about 15 agents across three machines and two model vendors. Coding agents, a research agent, content agents, an inbox monitor, a couple of supervisor agents that keep the others moving. Every one of them has memory now. They remember their own history just fine. And my day is still a mess, for a reason that has nothing to do with what any of them remembers.

Here's the distinction I keep coming back to. Memory is the past. State is the present.

## What memory actually gives you

Memory is a record of what already happened. The research agent remembers the briefs it wrote last week. The coding agent remembers the architecture decision we made on Tuesday. That history is genuinely useful, and a year ago not having it was painful, so I understand why the industry got excited.

But memory is private and it's backward-looking. Each agent has its own. The research agent's memory of last week is locked inside the research agent. The coding agent can't see it. More importantly, neither of them can see what the other is doing at this exact moment. Memory tells an agent about its own yesterday. It says nothing about everyone else's right now.

And right now is where the work actually happens.

## State is the thing that's missing

State is the live, current picture of what's going on across the system. What is each agent working on this minute. What just changed. What's blocked, what just finished, what the others need to know before they take their next step. In a human team you'd call it situational awareness. Everybody can see the current state of the world, so they can act on it without asking.

My agents have none of that. Each one knows its own history and is blind to the present everywhere else. There is no shared state between them. So the research agent finishes a brief and has no way to tell the content agent it's ready. The content agent drafts something that needs a number the analytics agent computed ten minutes ago, and has no way to reach in and get it.

So I do it. I read the brief, pull the three things that matter, and paste them into the next window. I copy the number over. I tell the coding agent what the API agent decided. I am the live connection between things that are each individually fast and each individually blind. The agents do the work. I am the shared state. I am the only part of the system that can see the present across all of it, so the present has to physically pass through me.

That is human-agent collaboration today, and it's mostly the human ferrying context by hand. Adding more memory to each agent does not touch this. You can give every agent a perfect record of its own past and the human is still standing in the middle holding the present together.

## Engineers already solved this. Decades ago.

The frustrating part is that this is a solved problem in another domain. Software engineers have had shared state for a long time, and the thing that gave it to them is version control. Git, mostly.

Think about how ten engineers work on one codebase without constant collisions. Each of them has their own local copy and their own history of changes. That's their memory. But that alone would be chaos, ten people editing the same files with no idea what anyone else touched. What makes it work is a shared, current state of the codebase that everyone can see and sync to. You pull, and you have the present. You see what changed, who changed it, what's in flight on which branch. The history matters, but the thing that lets ten people stay sane on one project is the shared current state, not the private logs.

That's the layer my agents don't have. They've got the local history. They've got the equivalent of a personal commit log. What they're missing is the shared repository, the place where the present lives and everyone can read it without going through a person.

Engineers got this in the 2000s and stopped thinking about it. It became plumbing. Nobody on a software team says "let me manually relay what I just changed to the other nine people," because the system shows them. Agents are running today the way engineering teams would run if you deleted git and made one person memorize and verbally relay every change. You'd never staff a team that way. But that's the default for anyone running more than two or three agents right now.

## Why memory got built first, and state didn't

Memory was the easier thing to ship, which is probably why it came first. You can bolt memory onto a single agent without coordinating with anyone. It's a feature inside one product. One company can build it, ship it, and demo it alone.

Shared state is harder because it's inherently between things. It only matters when multiple agents, often on different platforms from different builders, need to read and write the same current picture. That requires a layer that sits outside any single agent and that they all agree to use. Identity, so an agent knows who's asking. Permissions, so it knows what each one is allowed to see and change. A common place where the present is written down and read from. That's infrastructure, and infrastructure is slower and less glamorous to build than a memory feature you can announce.

But it's the layer that the next phase of this actually needs. Once you have more than a few agents doing real work, intelligence is no longer the thing holding you back. The agents are smart enough. The thing holding you back is that they can't see each other's present, so a person has to be the bridge.

## This is the layer that gets built next

I'm fairly convinced shared state is the missing piece, and that it's about to get built. The pattern is familiar. When the people furthest ahead are all solving the same problem by hand with cron jobs and copy-paste and a human in the loop, that's usually the moment right before someone turns it into infrastructure. Storage was like that before S3. Payments were like that before Stripe. The plumbing gets standardized once enough people are clearly hurting for the same plumbing.

We're building toward this, and we're not the only ones who see it. But you don't need to take anyone's product on faith to believe the shape of it. Just look at what your own setup looks like the moment you go past three agents. They each remember their own past. None of them can see the shared present. And you're the one carrying it between them all day.

Memory gave the machines a record of yesterday. The piece still missing is the one that lets them see the same present at the same time, and stop routing it through you. Build that and the 15 blind specialists finally start acting like a team. That's the layer I'm watching get built.
