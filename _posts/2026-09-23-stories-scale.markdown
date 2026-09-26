---
layout: post
title: "Stories Scale"
date: 2026-09-23 20:00:00 +0200
author: Alex
description: "When the team is small, user stories are overhead. When it grows, they become the only reliable way to coordinate work without everyone stepping on each other."
tags: [xp, teams]
---

When a team is small enough, you don't need stories.

Two or three people, shared context, constant communication - you can carry the product in your heads. You have the same Slack conversation, you attended the same meeting with the customer, you know what you're building and why. You write code, you show each other, you ship.

Stories feel like overhead at this stage. Filling out templates, writing acceptance criteria, running refinement sessions - it all seems like process for the sake of process. Why write down what everyone already knows?

This feeling is accurate. At that scale, stories are overhead.

The problem is that teams don't stay small. And when they grow, the thing that worked before stops working, and nobody is quite sure why.

---

What happens when teams grow is not complicated: people stop knowing what everyone else knows.

A second team gets formed to work on a different part of the product. Developers join who weren't in the original customer conversations. A product manager is hired specifically because the founding engineers don't have time to talk to customers anymore. The CEO is no longer in the room when features get scoped.

The shared context that made informal communication work evaporates, incrementally, over months. Nobody notices it happening until the demo where two teams show features that contradict each other. Or the release where a feature shipped without the edge case that the customer specifically asked for. Or the planning meeting where nobody can remember why a particular decision was made.

These failures are not failures of intelligence or effort. They're failures of information distribution. The people who knew, couldn't tell everyone who needed to know, fast enough, clearly enough, durably enough.

Stories are the solution to this problem.

---

A user story, written well, is a portable unit of shared understanding.

It carries what the feature is, who it's for, why they need it, and what "done" looks like. It can be read by a developer who wasn't in the planning session. It can be referenced by a QA engineer testing six weeks later. It can be used by a product manager explaining scope to a stakeholder who asks why a feature works the way it does.

None of this requires a sophisticated project management tool. It requires that someone, before work starts, wrote down: who needs this, what they need, and how we'll know when we've delivered it.

The format that makes stories most durable is the BDD scenario - not because it produces better test coverage, but because it forces the story to be concrete. "As a user, I want to filter search results" is not a story. It's a wish. "Given I have searched for a product, When I apply a category filter, Then only results in that category are shown" is a story. It's testable, unambiguous, and reviewable by anyone who needs to understand what was built and why.

Concrete stories survive the conversation they came from. Vague ones don't.

---

The word I keep coming back to is *durable*.

Informal communication is fast and cheap but perishable. The conversation in Slack about what the feature should do is gone in a week. The decision made in the hallway doesn't exist unless someone wrote it down. The context the founding engineer has in their head leaves when they leave.

Stories are durable by design. They're a record of what was decided and why, in a form that can be shared, searched, and referenced later. They're the mechanism by which knowledge about what you're building survives beyond the moment it was created.

This matters more as the team grows because the distance between "person who decided" and "person who implements" increases. At two people that distance is zero. At twenty people, it can be significant. At fifty, the person implementing something may have never spoken to the person who requested it.

Stories are how information crosses that distance without degrading.

---

There's a consequence to all of this that's worth saying directly: the discipline of writing stories pays dividends before the team is big enough to obviously need them.

Teams that practice writing concrete acceptance criteria get better at understanding what they're building before they build it. The act of writing "Given... When... Then..." exposes ambiguity in requirements that would otherwise surface during implementation, during QA, or during the demo. Catching it earlier is cheaper.

Teams that wait until they're large enough to need stories are already behind. The habit of clear communication has to be built at small scale, or it won't be there when the team grows.

The time to start writing good stories is when you don't think you need them. By the time you obviously need them, you needed them three months ago.

---

Stories don't scale your team for you. Nothing does that. But they do make it possible for a growing team to maintain alignment without requiring that everyone be in every room for every decision.

That's not a small thing. Most of what slows down large engineering teams is not technical - it's the cost of getting everyone pointed at the same goal, working from the same understanding, measuring against the same definition of done.

Stories are infrastructure for shared understanding. Like other infrastructure, they feel like overhead until you don't have them.

Then they feel like something you can't do without.
