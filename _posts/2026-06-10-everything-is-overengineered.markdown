---
layout: post
title: "Everything Is Overengineered"
date: 2026-06-10 19:00:00 +0200
author: Alex
description: "Pick any codebase at random and look carefully. You'll find abstractions for problems that don't exist yet and patterns applied where none were needed. Complexity is the default."
tags: [simplicity]
---

Pick a codebase at random. Any codebase, any company, any size. Look at it carefully.

I will bet you that somewhere in it, there's an abstraction that exists to handle a case that hasn't happened yet. A configuration system for options that are never changed. A plugin architecture with one plugin. A queue in front of something that could just be called directly. An interface implemented exactly once.

These things aren't bugs. They passed code review. They made sense when they were written. Someone wrote them because they were thinking ahead.

Thinking ahead is where overengineering comes from.

---

The word "overengineering" has a pejorative ring, which makes engineers defensive about it. It sounds like an accusation of gold-plating, or of not understanding the requirements, or of being clever for its own sake.

Those things happen, but they're not the main source of the problem.

The main source is good intentions applied too early. It's the architect who says "we'll probably need to swap out the database layer eventually, so let's put an interface in front of it now." It's the engineer who says "this will get more complex as the feature grows, so let's structure it to handle that." It's the team that says "we're going to scale to millions of users, so let's design for that from the start."

Each of those statements is defensible. Sometimes the database does get swapped. Sometimes the feature does get more complex. Sometimes the system does scale to millions.

But often it doesn't. And now you're paying for an architecture that was built for a future that didn't arrive, and maintaining it costs you real time every sprint.

---

The specific patterns that show up over and over:

**Microservices for teams of five.** Microservices solve real problems: independent deployability, team autonomy, isolated failure domains. They also introduce real costs: distributed tracing, inter-service communication, independent deploy pipelines, and the perennial joy of a network call failing in a way a function call never would.

These tradeoffs make sense at a certain scale. They do not make sense for a team of five people running a single product who can all fit in one Slack channel. A monolith is not a failure of imagination. It's the right architecture for a system that doesn't need the complexity of its alternative.

**Event sourcing for a CRUD application.** Event sourcing is a legitimate pattern for certain domains - financial systems where audit trails are legally required, systems where you need to reconstruct past states, complex domains with long-running processes. It is not a good fit for a system where the main operation is "user edits a record."

The pitch for event sourcing in simple systems is usually "future flexibility." You'll be able to replay events, rebuild read models, add projections. This is true, and also irrelevant if none of those capabilities are in your roadmap.

**Kubernetes for a team that doesn't need it.** I have watched small teams spend months configuring Kubernetes because that's what the industry uses, and end up with a deployment setup that requires a specialist to operate and a week to debug when something goes wrong.

Kubernetes solves hard problems at scale. It also introduces complexity that a small team will feel immediately and painfully. Three containers on a VPS with a simple deploy script will run most small products reliably for years without a Kubernetes certification.

**Abstractions for one use case.** A `UserRepository` interface implemented by exactly one `PostgresUserRepository` is not an abstraction - it's a guess about future flexibility that added indirection without adding value. If you ever need a second implementation, write the interface then. The code is right there.

---

The force that produces overengineering is not stupidity. It's the opposite: pattern recognition.

Good engineers are trained on codebases that solved hard problems. They've read about systems at Google scale, Netflix scale, Uber scale. They've studied the patterns those systems use. And when they see a new problem, their pattern-matching instinct fires: "this looks like a place where event-driven architecture helped; maybe it would help here."

The problem is that the pattern was developed in response to specific pressures at specific scale. Applying it in a context without those pressures adds the costs of the pattern without capturing its benefits.

The antidote is not to stop learning from large systems. It's to ask, for every pattern you consider: "What problem does this solve, and do I have that problem?"

Not "will I have that problem." Do I have it, now, in this codebase?

If the answer is no, the pattern does not belong here yet.

---

The rule I try to apply: build the simplest thing that solves the actual problem. Not the simplest thing that could possibly work - the simplest thing that solves *this* problem, for *these* users, at *this* scale.

When the scale changes, when new requirements arrive, when the simple thing demonstrably can't handle what you need - refactor. The refactor will be informed by real constraints, not imagined ones. It will target the actual bottleneck, not a hypothetical one.

This approach feels risky to engineers who've been burned by under-designed systems. And those burns are real. But the cost of under-engineering is usually visible: things break, performance degrades, you can't add features easily. The cost of overengineering is invisible until you're buried under it: a new hire who takes months to contribute, a migration project that absorbs a quarter, an operations burden that compounds every sprint.

Both costs are real. The industry talks about under-engineering constantly and overengineering rarely.

---

The most important word in software engineering might be "enough."

Enough abstraction to make the code readable. Enough architecture to support what you're building today and what you can see coming in the next quarter. Enough tooling to keep the system healthy without requiring a specialist to operate.

Not more. Not "this might be useful." Not "we'll probably need it."

Enough.

Everything else is debt you haven't acknowledged yet.
