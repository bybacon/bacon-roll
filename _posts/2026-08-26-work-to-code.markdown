---
layout: post
title: "Work to Code"
date: 2026-08-26 19:00:00 +0200
author: Alex
description: "Creativity is the enemy of execution. You have a way of working already in place. New inventions should come from necessity, not from what interests individuals. Consistency compounds."
tags: [culture, simplicity]
---

Creativity is the enemy of execution.

That sentence makes people uncomfortable. Creativity is supposed to be good. It's how problems get solved, how products improve, how teams grow. Nobody wants to work somewhere that suppresses creative thinking.

But there is a specific kind of creativity that consistently makes teams slower, codebases worse, and work harder to hand off. It is the creativity that invents new ways of doing things when a way of doing things already exists.

---

Every team that has been together for more than a few months has developed a way of working. How tests are structured. How code is organized. How tasks are described and tracked. How deployments happen. How decisions get made. These conventions exist because someone made a choice at some point, and the team aligned around it, and over time it became the thing that makes the codebase navigable and the work predictable.

The conventions are not perfect. They are good enough, and they are shared. That second part is the one that matters.

When a developer decides their personal approach to structuring services is better than the one the team uses, and implements it in a new service, the codebase now contains two conventions. The next developer who touches that service has to figure out which one they're looking at before they can understand the code. The developer after them might not even notice there are two, and produce a third. Six months later someone opens a PR review and spends twenty minutes on a discussion about which pattern to follow that would never have happened if the first person had just used the established convention.

The creative decision cost more than it added.

---

The principle is not "never change how you work." It is "change how you work deliberately, collectively, and for reasons you can state clearly."

If the current convention is causing real problems - friction, bugs, things that consistently go wrong - then changing it is worth the disruption. Propose the change. Talk about it. Align the team. Update the standard. Then everyone follows the new thing.

What doesn't work is individuals making local decisions that diverge from the shared convention because they prefer a different approach, or because they want to try something they read about, or because they weren't aware the convention existed. The divergence accumulate, and the shared codebase becomes a patchwork of individual preferences that nobody fully understands.

---

This applies to tools as well as patterns.

There is an endless supply of new libraries, frameworks, and approaches in software. Most of them are improvements over what came before in some dimension. Some of them will become the standard in a few years. This does not mean you should adopt them now.

Every new dependency is a surface you have to understand, maintain, and explain to other developers. Every new tool you introduce is a thing someone else has to learn before they can be productive in the part of the codebase where you used it. The cost is not just your time. It's the team's time, now and in the future.

Inventions should come from necessity, not preference. When the thing you have genuinely cannot solve the problem in front of you, reach for something new. When it can solve the problem - even if imperfectly, even if another tool would solve it more elegantly - use the thing you have. The cost of consistency is lower than the cost of fragmentation.

---

This is what "work to code" means. There is a way of working. Follow it. Make it better when it needs to be better - but make it better for everyone, through the team, not just for yourself.

The code that looks like one person wrote it, the codebase that a new developer can navigate in a day, the system where you can read any file and immediately understand what it's doing and why - this is not the product of constraint. It is the product of discipline. Everyone following the same patterns, in the same direction, over time.

Consistency is not boring. Consistency is what makes everything else possible.
