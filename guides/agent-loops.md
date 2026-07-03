---
title: "How to Build Agent Loops That Finish the Job"
description: "One-shot prompts give you a draft; a loop gives you a result. A practical guide to building agent workflows with a real feedback signal and a stop condition that holds."
category: "guides"
type: "guide"
publishedAt: "2026-07-03"
---

Most people talk to an AI agent the way they'd use a search box. Ask once, read the answer, move on. That works for lookups. It falls apart the moment the job is something the first attempt probably will not nail: fixing a flaky test suite, tightening a landing page, getting a report to actually hold up. For that kind of work, the agent needs a way to try, check, learn, and go again. That is a loop.

A loop is the difference between an agent that produces a draft and an agent that produces a result.

## One-shot prompts vs. loops

A one-shot prompt asks for a single pass:

> Make this page load faster.

You get one attempt. Maybe it helps, maybe it doesn't, and you have no idea unless you go measure it yourself. A loop builds the checking and the retry into the instruction:

> Find the slowest page. Make one focused change. Measure it again under the same conditions. Keep the change only if it helped. Repeat until every page hits the target or another pass stops making a real difference.

Same goal, completely different behavior. The second version can run unattended and come back with something you can trust, because it checked its own work along the way. It knows what "faster" means, it verifies each change, and it knows when to stop.

## The four questions every loop answers

A good loop comes down to four plain answers, written down before the agent starts:

### 1. What is it trying to accomplish?

State the target in concrete terms. Not "improve the docs" but "every code example in the README runs against the current API without errors." A vague goal produces a loop that never knows whether it is done.

### 2. How will it know if the latest attempt worked?

This is the part most people leave out, and it is the part that makes a loop a loop. The agent needs a real signal: a test that passes, a number that moves, a check that a human or another agent can reproduce. If the agent grades its own homework with no external check, it can convince itself it succeeded.

### 3. What should it do with what it learned?

Keep the change if it helped. Roll it back if it didn't. Log what happened so the next pass builds on evidence instead of starting over. A loop that forgets the last attempt is a one-shot prompt running on repeat.

### 4. When should it stop?

Every loop needs a brake. Stop when the target is met, when another pass stops producing a meaningful improvement, or when a set budget of attempts runs out. Without this, you get an agent that "improves" a working page until it breaks, or burns tokens polishing something that was already done.

## What this looks like running

Say the target is every page under 200 milliseconds, measured the same way each time. The loop runs like this:

- Pass 1: the slowest page is /dashboard at 890 ms. The agent defers offscreen images, measures again: 610 ms. Better, so it keeps the change.
- Pass 2: /dashboard is still slowest at 610 ms. It splits the JavaScript bundle, measures: 410 ms. Keep.
- Pass 3: 410 ms down to 240 ms after caching a slow query. Keep.
- Pass 4: 240 ms to 232 ms. That is under a 5 percent gain, so the brake fires. This page is done, and the loop moves to the next slowest one or stops.

Four passes, each with a measured number, each decision made on evidence, and a clear reason it ended. That is the whole game.

## When a loop is worth it

Loops cost more time and more tokens than a single pass, so use them for the jobs where one pass rarely gets you there. The tell is that each of these has an obvious signal to loop against:

- Stabilizing a flaky suite, signal: 50 consecutive green runs
- Fixing production errors, signal: the error stops appearing in the logs
- Refactoring toward a stated architecture, signal: the tests stay green after each step
- Getting a piece of writing to a defined bar, signal: a rubric another reader can score

For a quick lookup or a single clear edit, a one-shot prompt is the right tool, and reaching for a loop just adds overhead. The skill is knowing which kind of job you have.

## The stop condition is the hard half

If you take one thing from this, take this: the stop condition is where loops succeed or fail. An agent that can iterate will happily iterate forever. It will "improve" past the point of improvement, second-guess a good answer, and spend your budget making a thing worse.

So be specific about the brake, and tie it to the same signal from question two. "Stop when no page improves by more than 5 percent over the last pass, or after six passes, whichever comes first" is a real condition: a threshold plus a hard cap. "Stop when it looks good" is not. Restraint has to be written into the loop. Left alone, the agent will keep going.

Watch for the opposite failure too: an agent gaming the signal. If the check is "the page loads faster," an agent can win that number by deferring something the user actually needs, hitting the metric while hurting the experience. The check has to measure the thing you care about, because a proxy that's easy to move is exactly what an agent will exploit.

## Make your loops reusable

Once you have a loop that works, it is worth more than the one job it just did. The instruction, the check, and the stop condition together are a small playbook, and playbooks are the kind of thing a team should share rather than each person rebuilding from memory. Put your working loops where the whole team and their agents can reach them, and the person who figured out the right way to run a production error sweep writes it down once while everyone's agents run it the same way. That shared state is human-agent collaboration doing real work. The alternative, where every good loop lives in one person's chat history, wastes the best thing loops give you.

## Start with one

Begin with one recurring task where the first attempt is rarely the final answer. Write the four answers, run it, watch where it drifts, and tighten the brake:

- Goal: the concrete target, stated so "done" is unambiguous
- Check: the reproducible signal that says an attempt worked
- Learn: keep, roll back, and log so each pass builds on the last
- Stop: a threshold and a hard cap, tied to the check

You stop asking an agent for an answer and start giving it a way to earn one.
