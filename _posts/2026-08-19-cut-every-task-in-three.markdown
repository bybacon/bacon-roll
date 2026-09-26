---
layout: post
title: "Cut Every Task in Three"
date: 2026-08-19 20:00:00 +0200
author: Alex
description: "Prepare the task. Complete the task. Leave no trace. Most people only do the middle one. The other two are what separate good work from work that makes a mess."
tags: [culture, xp]
---

Most people do the middle part of a task. They start when the work is already in front of them and stop when the visible work is done. The preparation that would have made it easier never happened. The cleanup that would have left no trace gets skipped because it feels optional.

It isn't optional. It's two-thirds of the job.

---

Every task has three parts. Prepare it. Complete it. Leave no trace.

**Prepare the task.** Before you write a line of code, before you send the message, before you start the meeting - do you actually understand what you're doing? Have you read the spec or the ticket? Do you know what done looks like? Do you have what you need to start, or are you going to discover a blocking dependency thirty minutes in and have to context-switch out to resolve it? Preparation is the work that makes the work go smoothly. Skip it and you pay for it in interruptions, wrong turns, and rework.

In practice this looks like: read the ticket fully before opening a file. Write the test before writing the implementation. Confirm the acceptance criteria with whoever wrote the spec before building. Spend ten minutes at the start of a task asking what could go wrong, so you're not surprised by it halfway through.

**Complete the task.** This is the part everyone does. Or mostly does. The actual execution - the code written, the message sent, the feature shipped. The catch here is finishing. A task that is 90% done is not done. It is a context-switch waiting to happen, a liability that will surface at the worst possible moment, a thing that costs future-you more than it would have cost present-you to simply close it. Finish things. If a task is too large to finish in one session, break it into smaller tasks that can each be fully completed. Half-done work is debt.

**Leave no trace.** This is the part that separates good work from work that makes a mess. When the task is done: close the ticket, merge and delete the branch, update the spec if reality diverged from it, pass along relevant information to whoever needs it, clean up the files you made changes on, remove any temporary scaffolding you put in place to make the work possible. The task is not complete when the feature works. It is complete when the environment is in the same state it would have been in if the task had always existed - plus the improvement the task was meant to make.

---

The reason most people skip prepare and leave-no-trace is that neither one produces visible output. Nobody sees the preparation you did before writing the code. Nobody thanks you for the branch you deleted or the ticket you closed. The reward structure points at the middle part, so the middle part is what people optimize for.

But teams that optimize for the middle part produce codebases full of half-finished work, backlogs full of stale tickets, and a constant low-level friction where the environment is always slightly worse than it should be. The shortcuts accumulate. Eventually the environment is the main obstacle to doing work, and a cleanup project appears on the roadmap as if the disorder arrived by itself.

It didn't arrive by itself. It was left, incrementally, by everyone who stopped at "complete".

---

Apply it as a habit. Before starting a task, spend a moment on preparation - even if it's just two minutes of reading to confirm you understand the goal. After finishing, spend another moment on cleanup - close the loop, leave no trace. Build both ends into your definition of done.

The work is not over when the feature ships. It is over when there is nothing left behind.
