---
title: "Match the Model to the Task"
description: "Running a fleet of agents is a real recurring cost, and the discipline that keeps it sane is knowing when you can reach for the cheaper model."
category: "AI Agents"
type: "article"
author: "Mike Molinet"
authorLinkedin: "https://www.linkedin.com/in/mikemolinet/"
publishedAt: "2026-08-19"
---


Most people pick a model by asking which one is smartest. Once you are running more than a couple of agents, that stops being the useful question. The real question is which model for which job, because now you are paying for all of them, every day, and the bill adds up.

I learned this the boring way. I had an agent that ran great. It handled a recurring job for me end to end, checked its own work, and caught its own mistakes. It was on one of the expensive models and I had barely set it up. One day I moved it to a cheaper, faster model to save some money, and it got worse almost immediately. The output was sloppier, it missed steps, and at one point it dropped a part of the job it used to handle on its own.

My first instinct was the obvious one: the cheap model was too weak, put the expensive one back. That was wrong.

The expensive model had been quietly covering for me. I had given the agent almost no structure. A vague ask, no runbook, no scripts, no clear definition of what "done" looked like. The smart model was filling those gaps on its own, inferring the shape I had skipped. The cheaper model had nothing to work from. It was just as good at the actual job, it just had nothing to lean on.

So I did the thing I should have done at the start. I wrote the runbook, gave it the scripts, and spelled out the steps and the checks. Then I put it back on the cheaper model, and it ran fine. It still runs fine.

So a lot of what you pay for in a premium model is really it covering for structure you never built. Build the structure, and a cheaper model does the same job.

The rule I follow now is simple: match the model to the task.

Routine, high-frequency work goes on the cheap and fast models. Those are the jobs that run all day and follow a clear path, and you have already made them legible, so the model has an easy time.

Save the premium models for the genuine judgment calls, the hard reasoning and the ambiguous decisions where there is no clean answer. That is where the money is well spent, and once you have done the structural work, it is a small share of what your agents actually do.

This gets more true every month. Models are multiplying and converging at the same time. The gap between the cheapest capable model and the most expensive one is huge, and for a lot of tasks the cheap one is completely fine. Run a fleet and reach for the biggest model by reflex, and you are lighting money on fire for work a cheaper one would have handled.

If you want a place to start, look at where you are using a premium model out of habit. Take one routine agent and drop it to a cheaper model. If it degrades, look at your setup before you blame the model. That degradation is showing you where the structure is thin. Fix that, then run it again. Most of the time it holds.

The people who get good at running agents are the ones who can tell when the cheap model is enough. Most of the time, it is.
