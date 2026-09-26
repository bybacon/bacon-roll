---
layout: post
title: "Don't Hire the Smartest People. Hire the Laziest."
date: 2026-06-17 19:00:00 +0200
author: Alex
description: "Lazy engineers solve problems with less code, fewer meetings, and simpler systems. The hardest worker on the team is often the one creating the most unnecessary work for everyone else."
tags: [teams, culture]
---

This advice is counterintuitive enough that I need to define what I mean before people stop reading.

I don't mean people who do low-effort work, coast on others, or avoid hard problems. Those people exist and they're a drain on every team they touch.

I mean something different: people who are deeply, constitutionally unwilling to do work that doesn't need to exist. People who, when faced with a manual process, immediately ask why it's manual. People who, when asked to do something repetitive, start thinking about how to not do it again.

That kind of laziness is an engineering superpower.

---

The smart people trap is real.

Smart engineers love problems. They're good at solving them, they enjoy solving them, and they have excellent reasons for why each solution is the right one. They will build you a distributed message queue when a database table would suffice. They will introduce a service mesh because the architecture *might* need it in three years. They will spend two weeks designing an elegant abstraction over something you use twice.

This is not malicious. It's genuine. The abstraction is elegant. The message queue *is* more scalable in theory. The service mesh *would* be necessary if the system grew tenfold.

But the system probably won't grow tenfold. The abstraction serves the future you imagined, not the present you have. And now you have a codebase that a new hire needs three months to navigate, and an ops burden that consumes half your Fridays, and a quarterly migration project every time the underlying technology shifts.

Smart people will justify all of this. They're smart; they're very good at justifications.

---

Lazy people think about the work before doing it.

This is the core of it. A lazy engineer, confronted with a problem, asks: do I actually have to solve this? Is there a simpler version of this problem? Can I solve the simple version and see if that's enough?

They have a low tolerance for work that creates more work. They hate manual deployments because every manual deployment is a future manual deployment. They hate complex abstractions because complex abstractions need complex debugging. They hate systems that require maintenance because maintenance is a tax on everything else you want to do.

This impatience with unnecessary work is, in practice, the force that creates good tooling. The deploy pipeline that saves everyone an hour a day got built by someone who was tired of spending an hour a day deploying. The test framework that makes writing tests fast got built by someone who found writing slow tests unbearable. The documentation that actually helps got written by someone who was tired of answering the same questions.

Laziness, properly channeled, is automation, simplification, and leverage in disguise.

---

There's a useful distinction Bill Gates supposedly made (whether or not he said it, the point holds): he'd hire a lazy person to do a difficult job because they'd find the easy way to do it.

The flip side is equally true: a clever person will find a complex way to do an easy job, and be proud of it.

I've hired and worked with both kinds of engineer. The lazy ones get frustrated by unnecessary complexity and tend to remove it. They produce simpler code because simple code is less work to write and maintain. They automate the boring parts because they don't want to do the boring parts. They push back on scope because more scope is more work.

The clever ones produce impressive solutions to problems that didn't need to be solved that way. They're a pleasure to work with in some contexts and an absolute liability in others, specifically in contexts where the correct answer is "we don't need that."

---

The interview signal for laziness is different from what most interviews test for.

It's not about how well someone solves a hard algorithm problem. It's about what questions they ask before they solve it. It's about whether they push back: "Do we actually need to handle that case?" It's about what they delete when they improve existing code, not just what they add.

Some of the best engineers I've worked with leave code review comments that just say "can we remove this?" Some of the questions they ask in planning sessions are "what happens if we just don't build that?" Some of the pull requests they open are deletions, not additions.

None of this would score well on a traditional technical interview. All of it makes teams faster, codebases healthier, and products simpler.

---

The most underrated skill in software engineering is knowing what not to build.

It's rare because it requires resisting the pull toward cleverness, resisting the pull toward completeness, resisting the satisfying feeling of having written something sophisticated. It requires looking at a problem and deliberately choosing the boring solution.

Lazy engineers do this naturally. They don't want to maintain the sophisticated solution. They don't want to explain it to the next hire. They don't want to debug it at 2am.

So they don't build it.

And the system is better for it.

Hire the lazy ones.
