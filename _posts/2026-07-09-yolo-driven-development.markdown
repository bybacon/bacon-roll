---
layout: post
title: "YOLO-Driven Development"
date: 2026-07-09 19:00:00 +0200
author: Alex
description: "At some point the analysis has to stop and the building has to start. The case for committing to a direction sooner, shipping smaller, and letting reality tell you what's wrong."
tags: [process, simplicity]
---

Before anyone calls the fire department: this is not an argument for deploying to production on a Friday afternoon without tests or a rollback plan.

It's an argument against a specific kind of paralysis that masquerades as rigor.

---

Here's what YOLO-driven development is not:

It's not skipping tests. Tests are cheap insurance and compound over time - skip them and you're borrowing against your future self's sanity.

It's not ignoring architecture. Structure matters. A system built without thought about how it will change becomes harder to change, exponentially, as it grows.

It's not shipping without thinking. Thinking is free. Always think.

Here's what it is:

It's the recognition that at some point, the thinking has to stop and the building has to start. And that the point where that should happen is usually earlier than it feels.

---

There's a failure mode in technical work that doesn't have a good name. It's not procrastination exactly. It's not perfectionism exactly. It's a kind of sustained indecision dressed up as thoroughness.

It looks like this: a decision that could be made in an afternoon gets escalated into a design document. The design document spawns a review process. The review surfaces concerns that spawn a second design document. The second document raises questions that require a meeting to resolve. The meeting produces action items that require more investigation. Three months later, the thing is still not built, but everyone feels like they've been working very hard.

The work was real. The rigor was real. The outcome was nothing.

---

The problem with analysis is that it has no natural stopping point.

Every software decision has uncertainty attached to it. You don't know exactly how the requirements will evolve. You don't know which edge cases will actually matter. You don't know whether the abstraction you're designing will hold up. You can always investigate more, consult more people, build more prototypes, write more documents.

The only thing that definitively ends the analysis is a decision to stop analyzing and start building.

And building produces information that no amount of analysis produces: the real friction, the real edge cases, the real user behavior. The system you imagined and the system that exists after you build it are always different. The difference is only visible after you build.

This is what "YOLO" actually means in practice. Not "don't think." It means: at some point, commit. Pick a direction. Build the thing. Let reality tell you what's wrong.

---

There's a version of this that's been formalized: the concept of a "spike" in agile, or "failing fast" in startup culture, or simply "ship a prototype." All of these are sanctioned forms of the same underlying move: accept uncertainty, make a bet, get feedback quickly.

But I find the formalized versions often inherit the bureaucratic instinct they're meant to counteract. The spike becomes a scheduled agenda item. The prototype requires approval. The "fail fast" culture still takes four months to fail.

The spirit of it is simpler: make a decision now, with the information you have now, accepting that you might need to change it. Not because the decision doesn't matter - it does - but because the cost of a reversible mistake is almost always lower than the cost of indefinite delay.

Most decisions in software are more reversible than they feel. Code can be changed. Schemas can be migrated. Architectures can be refactored. The decisions that are genuinely irreversible - public APIs, wire formats, database schemas at scale - are a small fraction of the decisions that get treated as irreversible.

---

The heuristic I use: if I've been thinking about something for more than a day and haven't reached a conclusion, I build the simplest version I can, deploy it somewhere safe, and see what happens.

Sometimes the build reveals that my analysis was missing something real and I refactor immediately. That's fine - the build took a day, the analysis was taking weeks.

Sometimes the build reveals that most of the concerns I was analyzing don't actually occur in practice. The edge case I was designing for never appears. The scale I was optimizing for never arrives. And I have something working instead of something planned.

Either way, I learn more from the build in two days than I was going to learn from the document in two weeks.

---

Ship more. Sooner. Smaller. With tests.

You will be wrong sometimes. You will refactor. That's the job.

The alternative is to be perfectly right about something that never existed.
