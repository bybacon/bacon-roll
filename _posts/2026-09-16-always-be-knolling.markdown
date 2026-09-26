---
layout: post
title: "Always Be Knolling"
date: 2026-09-16 20:00:00 +0200
author: Alex
description: "Tom Sachs' knolling principle applied to software: scan for what's not in use, put it away, group like things, align everything. The discipline of leaving a codebase more organized than you found it."
tags: [culture, simplicity]
---

Tom Sachs has a rule in his studio: always be knolling. Knolling is the practice of arranging all objects at right angles to each other or parallel to the edges of the surface they're on. Everything in use is out. Everything not in use is put away. Like things are grouped. All things are aligned.

It sounds like tidiness for its own sake. It isn't. It's a working method. When your tools are arranged, you can see what you have. When you can see what you have, you can find what you need. When you can find what you need, you can work without interruption. The environment supports the work instead of fighting it.

The principle maps directly to software. Most codebases are not knolled. Most backlogs are not knolled. Most development environments are not knolled. And the cost of this disorder is paid in attention, every day, by everyone who works in them.

---

The four steps of knolling are a useful frame.

The first is to scan your environment for things not in use. In a codebase this is dead code, stale branches, unused dependencies, config keys that reference services no longer running, commented-out blocks that haven't been touched in two years, feature flags whose features shipped in 2023. These things are not harmless. They occupy cognitive space. Every developer who opens a file with dead code has to spend a moment deciding whether it's dead or whether it's doing something they don't understand. That moment, multiplied by every file and every developer and every week, is a real cost.

The second is to put away everything not in use. Delete the dead code. Delete the stale branches. Remove the unused dependencies. If it's not in active use, it shouldn't be in the working environment. The objection is always "what if we need it later" - the answer is version control. It existed. It can be recovered. The cost of deleting something you later want back is retrieving it from git. The cost of keeping everything you might want someday is a workspace that nobody can navigate without a map.

The third is to group all like things. Routes with routes, models with models, specs with specs, utilities with utilities. Conventions that everyone follows consistently. Not because the grouping is the only correct grouping, but because a consistent grouping is one that anyone can navigate without asking. Surprise is the enemy of legibility. When things are where they're expected to be, the structure disappears and the work comes forward.

The fourth is to align all things. Consistent naming, consistent formatting, consistent structure across files that do the same kind of thing. The codebase that reads like one person wrote it, even though ten people did. When code is aligned, you read the content, not the style. When it isn't, your eye keeps catching on variations - a differently named test helper, a file that organizes its methods in the opposite order from everything else.

---

The real practice is leaving things more knolled than you found them.

Not in a single heroic cleanup sprint that produces a massive PR nobody wants to review and touches every file in the project. That's not knolling. That's rearranging furniture in a way that makes the house temporarily unrecognizable.

The practice is: every time you open a file, scan for one thing that's out of place. A dead method. An unused require. An import that's listed twice. Remove it. Commit it. Move on. Over weeks, the codebase gets cleaner in proportion to how often people touch it - which is exactly the right distribution. The files you're actively working in become progressively more organized. The files you don't touch sit undisturbed.

This is the principle Sachs calls leaving no trace: when you're done with the space, it should be in better condition than when you arrived. Not perfect. Just better.

---

Backlogs need knolling too.

A backlog that hasn't been knolled is a graveyard of good intentions. Tickets opened six months ago for features that were later descoped. Bugs that reproduced on a version three releases behind. Ideas that felt important at the time but were quietly superseded by different decisions. These are not open work items. They are noise. Every planning session that involves scrolling past them is time spent on things that don't matter at the expense of things that do.

Knoll the backlog on a regular basis. Close tickets that are no longer relevant. Group related items. Archive anything that's been sitting untouched for more than a quarter. If it matters, it will surface again - and when it does, you can open a new, clearer ticket with current context. If it doesn't surface again, it didn't matter.

---

The underlying principle is that disorder has a cost, and that cost is usually invisible until it becomes significant.

No single dead method makes a codebase hard to work in. No single stale ticket makes a backlog unusable. No single misaligned file makes a codebase illegible. The accumulation does. Disorder compounds slowly and then suddenly. At some point the codebase is the thing everyone complains about, the backlog is the thing nobody trusts, and the working environment is the thing that slows everything down.

The antidote is not periodic cleanup. It is continuous, small, habitual knolling. Scan. Put away. Group. Align. Leave the space better than you found it. Do it every time you're in a file, every sprint review, every time you're setting up your environment.

The environment is not separate from the work. It is the condition of the work. Knoll it accordingly.
