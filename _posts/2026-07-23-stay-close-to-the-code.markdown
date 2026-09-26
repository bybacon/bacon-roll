---
layout: post
title: "Stay Close to the Code"
date: 2026-07-23 21:00:00 +0200
author: Alex
description: "The best engineering leaders stay close to the code. Drifting into pure management mode is how you lose both the technical judgment and the credibility that made you effective."
tags: [teams, culture]
---

There's a trajectory that happens to a lot of good engineers. They get better at their craft, take on more responsibility, start leading teams, running planning sessions, doing more code review than writing. The calendar fills up. The keyboard time shrinks.

And slowly, without anyone noticing, the thing that made them good - the direct, daily contact with the feedback loop of building software - fades out.

They're still respected. They're still effective in meetings. But their intuition about what's hard, what's risky, what's actually going on inside the system, starts to lag. They make confident recommendations that don't quite fit the current reality. They estimate things with certainty that their team quietly corrects. The gap between what they think the codebase is like and what it actually is like grows, a little each month.

This is the cost of stopping coding. It's not dramatic. It's just drift.

---

I want to be careful about what I'm arguing here because it's easy to misread.

I'm not saying technical managers or architects should be writing production features instead of doing their actual jobs. I'm not saying senior engineers who spend most of their time in design documents and code reviews are slacking. Those roles are real and the work matters.

I'm saying: if you have stopped writing code entirely - stopped opening your editor, stopped wrestling with a build failure, stopped feeling the friction of actually implementing something - you have lost something that's very hard to recover through other means.

The thing you lose is calibration.

---

Calibration is what lets you say "that'll take a day" and be right. It's what lets you read a design doc and sense that the tricky part is being glossed over. It's what lets you sit in a planning session and notice that the team is about to take on something more complicated than it looks.

Calibration comes from doing the work recently. Not watching someone else do it. Not reviewing it. Actually doing it - picking up a ticket, writing the code, running into the thing nobody mentioned in the spec, spending two hours debugging something that turned out to be a test environment issue.

When you do this regularly, even in small amounts, your internal model of the system stays current. When you stop, the model freezes. It still exists, it still feels accurate, but it's a snapshot of how things were, not how they are.

The dangerous part is that you often can't tell the difference from the inside.

---

The form this takes doesn't matter much. It doesn't have to be production code. It doesn't have to be on the main product.

Some of the most calibrated senior engineers maintain personal projects, build internal tools, write exploratory prototypes, pair with junior developers on their actual tickets. The point is contact - regular, recent, hands-on contact with the reality of building software.

What it rules out is a fully abstract relationship with the work. Design-only, review-only, strategy-only. Those roles exist and are sometimes the right fit, but they have a specific tradeoff: you become good at reasoning about code and progressively less good at understanding what it's actually like to write it.

---

There's a version of this argument that goes: "I trust my team, I don't need to be in the weeds." And that's often right. You should trust your team. You shouldn't be in the weeds of their work.

But "trusting your team" and "maintaining your own technical judgment" are not in tension. You can delegate fully and still write code. You can stay out of your team's work and still open your own editor.

What you can't do is stop coding entirely and expect your technical judgment to stay sharp. The judgment is a muscle. It atrophies without use, quietly, in a way that's hard to notice until you need it.

---

The practices that have worked for me: keeping a side project that I care about, pairing with engineers on their tickets when they want it, picking up small internal tools work that nobody else has time for, spending a few hours a week writing code just to stay in contact with what it feels like.

None of this is heroic. It's maintenance, the same way exercise is maintenance for a body that otherwise defaults to sedentary.

The code is a feedback loop. The further you get from it, the longer the loop. The longer the loop, the slower your judgment updates.

Stay close. It compounds.
