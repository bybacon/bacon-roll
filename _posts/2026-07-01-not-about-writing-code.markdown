---
layout: post
title: "It's Not About Writing Code"
date: 2026-07-01 21:00:00 +0200
author: Alex
description: "The job title says software engineer. The actual job is mostly not writing code - and the sooner you internalize that, the better you get at the parts that matter."
tags: [culture]
---

The job title says "software engineer." The popular image is someone typing fast, translating ideas into working software. The romantic version is a lone developer, coffee in hand, building something from nothing.

The reality is that a minority of actual engineering work is writing new code.

This isn't a complaint. It's just what the job is. But it catches almost every developer off guard when they start, and it keeps catching people off guard as they get more senior, because nobody talks about it directly.

---

Here is some of what software engineering actually involves:

Setting up and maintaining development environments. Debugging why the environment works on your machine and not the CI server, why the CI server works today but didn't yesterday, why the Docker image builds locally but fails in the pipeline. This work is unglamorous, often invisible, and consumes enormous chunks of engineering time at most companies.

Understanding existing systems. Before you can change code, you have to understand it. Reading documentation that's out of date or missing. Reading code that wasn't written with readability in mind. Asking questions of people who partly remember how something works. Tracing execution across services to figure out what is actually happening. The ratio of reading to writing in a mature codebase is somewhere between 10:1 and 100:1.

Navigating organizations. Getting access to the system you need to change. Finding the person who owns the component you're integrating with. Coordinating a release with a team whose schedule doesn't align with yours. Understanding which decisions you can make and which need sign-off. Software engineering in a company is engineering inside a social system, and the social system creates as much friction as the technical one.

Debugging production issues. Not the satisfying kind of debugging where you figure out a puzzle and ship a fix. The 2am kind, where something is broken and you don't know what, and there's a customer on the line, and the monitoring is telling you something is wrong but not what. The kind that requires reading logs across three services and forming hypotheses and disproving them until you find the thing.

Reviewing code and being reviewed. Calibrating feedback that is honest but constructive. Reading pull requests carefully enough to actually catch problems. Explaining your choices to reviewers who are skeptical. Addressing review comments that you disagree with. Reaching consensus on approach between people with different experience and different opinions.

Writing - documentation, runbooks, design documents, post-mortems, ADRs. Most engineering organizations have chronic documentation debt because nobody likes writing and it doesn't feel like "real work." The engineers who write well, who document things when they change them, who leave clear runbooks for the systems they build, make every other engineer around them faster.

---

I want to be clear about why this matters, because it's easy to read it as discouraging.

It matters because the engineers who excel at this job - who become genuinely valuable over time - are the ones who take all of it seriously. Not just the parts that feel like programming.

The engineer who only wants to write code and treats everything else as noise is a limited engineer. They struggle with legacy codebases, with organizational complexity, with the maintenance burden of the things they built. They're valuable in contexts that don't require the other things, but those contexts are rarer than they seem from the outside.

The engineer who understands that the job is the whole system - the code and the infrastructure and the organization and the communication - builds a completely different kind of career. They become force multipliers because they can work in the full context of what makes software ship.

---

There's a version of this that I think is particularly worth naming for people earlier in their career.

The unglamorous parts are often where the leverage is.

A great development environment that everyone on the team uses saves dozens of hours a week. A well-written runbook prevents a 3am incident from becoming a 6am incident. A clear design document prevents a month of building the wrong thing. Documentation that actually reflects how the system works cuts new hire onboarding time in half.

None of these feel like "real engineering" in the romantic sense. All of them are more impactful than the feature ticket that seemed like the important work.

The engineers who figure this out early - who treat the whole job as the job, not just the code-writing part - are the ones who end up building the most.

---

Writing code is the part of the job you were probably hired to do, and it's the part that shows up most visibly in pull requests and commit history.

It's also, genuinely, one of the smaller parts of the work.

The sooner you internalize that, the sooner you start getting good at the whole job.
