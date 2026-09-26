---
layout: post
title: "Make Something. Now You Have a Problem."
date: 2026-07-15 23:00:00 +0200
author: Alex
description: "Abstract planning loops indefinitely. Building something - anything - ends the loop. You can't know what you're actually building until you've started building it."
tags: [process, simplicity]
---

There's a loop I've watched play out in almost every software project I've been part of:

You make something. It reveals a problem. You make something to solve the problem. That reveals another problem. You make something to solve that. Eventually, somewhere in the chain, a thing you made solves a problem without creating a new one.

That's the solution.

The thing people miss is that you can't find the solution without running the loop. You can't design your way to it in advance. You can't analyze your way there. The problems are only visible after you make something. The solution is only findable after you encounter the problems.

---

I've spent a lot of time thinking about why this is, and I think it comes down to something simple: building things reveals constraints you can't see any other way.

When you design a system on a whiteboard, you're working with a model of reality. The model is incomplete - it always is, because real systems have more moving parts than any model can capture. The incompleteness is not a failure of imagination. It's structural. You don't know what you don't know.

Building makes the unknown visible. The first version of the system is a hypothesis. It runs, it fails in ways you didn't predict, and now you have information. Real information, not imagined information. The failure mode exists in the real system, not your model of it.

This is the make → problem → make → problem → solution loop in practice. The problems aren't obstacles between you and the solution. They're the path.

---

The implication is uncomfortable: the first version is supposed to be wrong.

Not carelessly wrong - not "we didn't think about it." Wrong in the sense that it was built on incomplete information, which is the only kind of information you ever have at the start.

The first version's job is not to be right. Its job is to reveal the first problem.

This reframing changes how you should build it. You shouldn't be trying to make the first version solve every possible problem. You should be trying to make it concrete enough to reveal the most important problem you can't currently see. Small. Deployable. Observable.

The trap is building the first version as if it has to be the final version. This leads to overengineering (designing for problems you haven't encountered yet), slow delivery (trying to get it right before anyone uses it), and fragility (the extensive design covers the problems you imagined, not the ones that actually occur).

---

There's a craft to running the loop well.

The first make should be the smallest thing that creates real contact with the problem domain. Not a prototype that lives in isolation - something that touches the real data, the real users, the real system. Because the problems that matter are the ones that appear in contact with reality, not the ones that appear in contact with your assumptions.

Each subsequent make should be targeted at the most important problem revealed by the previous version. Not a complete redesign. Not fixing everything at once. The most valuable next move.

And at each stage, the question is: what is this version teaching me that I didn't know before?

If a version teaches you nothing - if everything works as expected, if no surprises appear - you built too conservatively. You stayed inside your existing model of the problem instead of pushing against its edges.

---

The loop has another property that's worth naming: it's how you know you're done.

You're done when a version doesn't generate a new problem. When the thing you built satisfies the actual constraints of the actual system and there's no residual friction pointing toward a next iteration.

This is different from "done" defined as "we built what the spec said." A spec is a model of the requirements. The real requirements are what the system actually needs to do under actual load, with actual users, in the actual environment. Those are only fully knowable by running the system.

"Done" by spec is done with your model. Done with the loop means done with reality.

---

I find this framing genuinely freeing.

It removes the pressure of having to get the design right before building. It's not supposed to be right. The first version's job is to fail informatively.

It removes the embarrassment of shipping something imperfect. The imperfections are how you find the solution. An imperfect thing that's running and revealing real problems is more valuable than a perfect design that hasn't been tested against reality.

It also removes the illusion that analysis can substitute for iteration. You can think for longer. You will not eliminate the problems you'll encounter when you build. You'll just encounter them later.

---

Make something. It will reveal a problem.

That's not a setback. That's progress.

Make the thing that solves the problem. It will reveal another problem.

Keep going. The solution is at the end of the loop.

You can't find it any other way.
