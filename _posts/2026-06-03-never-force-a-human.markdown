---
layout: post
title: "Never Force a Human to Do What a Robot Can"
date: 2026-06-03 17:00:00 +0200
author: Alex
description: "Every manual step in your workflow is a context switch, an error source, and a slow leak of team morale. Automate the mechanical and keep humans for the parts that require judgment."
tags: [automation]
---

There's a moment every developer eventually hits: you watch a teammate do something manually, something that happens every day, something that has been happening every day for months, and you realize a script could do it in three seconds.

They're not slow. They're not lazy. Nobody told them it could be automated. And now they've spent, by your rough mental math, something like forty hours of their life on a task that should not exist.

That's the moment I think of when I say: never force a human to do what a robot can.

---

The principle sounds obvious. It almost isn't worth saying. But look at how most engineering teams actually operate and you'll find manual steps everywhere — deployments kicked off by running a command on a server, PRs that need someone to post a Slack message when they're ready for review, weekly reports assembled by hand from three different dashboards, code style discussions in code review that a linter would have settled silently.

These manual steps don't feel expensive in the moment. Each one takes thirty seconds, a minute, maybe five. But the real cost isn't time. It's attention.

Every manual step is a context switch. It's a thing you have to remember, a thing you can forget, a thing that introduces errors when you're tired or distracted. It's a thing that builds resentment over months when you realize you've been doing it again, and again, and again.

Robots don't get tired. They don't get bored. They don't forget steps at the end of a long Friday. They're also perfectly willing to do the same thing ten thousand times without developing a quiet hatred for the process.

Humans are not like this. Humans are expensive, scarce, and badly suited for repetitive mechanical work. Wasting them on it is not just inefficient — it's a failure of judgment.

---

The places this shows up in software are predictable:

**Deployments.** If pushing to production involves a human running commands, copying environment variables, checking logs, and then posting in a channel, you've built a robot costume for your engineers. CI/CD pipelines exist. Use them.

**Code style.** If you're leaving comments like "we use single quotes here" or "please add a trailing comma" in code review, stop. That's a linter's job. Automate the formatting, add it to the pre-commit hook, and free up your reviewers to think about things that actually require judgment.

**Status updates.** Stand-up prep, sprint summaries, "what did we ship this week" — most of this is derivable from git history, ticket state, and PR comments. The words are already written. Someone just needs to collect them.

**Onboarding steps.** If your new hire has a checklist of things to request access to, accounts to create, tools to install — that checklist should be a script, or at least a script that runs the parts that can be automated and clearly flags the parts that can't.

The pattern is always the same: something mechanical, repeated, error-prone, and performed by a person who has better things to do.

---

Now, the important caveat.

Not everything should be automated. Automation is the right answer when the task is mechanical, well-defined, and repeatable. It is the wrong answer when the task requires judgment, context, or relationships.

A robot can run your tests. It cannot decide whether a failing test represents a real bug or a test that needs updating.

A robot can format a pull request description. It cannot decide whether the approach in that PR is the right one.

A robot can send a weekly summary to stakeholders. It cannot read the room in a difficult conversation about scope.

The distinction matters because over-automating the things that require human judgment is just as bad as under-automating the things that don't. If you automate the decision of whether to merge a PR, you've removed accountability, not friction. You haven't made a robot do a human's job — you've made a human do no job, which is different and worse.

The heuristic: if a person following a checklist could do it correctly every time without thinking, it should be automated. If it requires thinking — even a little — keep the human in the loop.

---

The version of this principle I come back to most is from manufacturing, not software. Toyota's production system has a concept called *jidoka*: machines should detect problems and stop themselves rather than passing defective work downstream. The goal isn't just efficiency. It's about where human intelligence gets applied.

In a factory running jidoka, humans aren't watching machines to catch errors. The machines catch their own errors. Humans are freed to do the things machines can't: improve the process, respond to novel situations, train each other.

Software teams that automate well look similar. Engineers aren't running deployments. They're improving the deployment system. They're not formatting code. They're discussing architecture. They're not writing status updates. They're making decisions that the status update should reflect.

The robot handles the mechanical. The human handles everything else.

That's not laziness. That's leverage.
