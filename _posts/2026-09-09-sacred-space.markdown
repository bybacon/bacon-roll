---
layout: post
title: "Sacred Space"
date: 2026-09-09 19:00:00 +0200
author: Alex
description: "Respect for space and tools is essential. Don't leave a mess. The way a team treats its codebase, its backlog, and its environment is the clearest signal of how seriously they take the work."
tags: [culture]
---

The way a team treats its environment is a signal.

Not a metaphorical signal - an actual one. A codebase full of dead files and commented-out blocks and TODO comments from three years ago tells you something about the standards the team holds itself to. A backlog with hundreds of tickets nobody is going to do tells you something about the relationship the team has with its own commitments. A dev environment that takes a day to set up and breaks twice a week tells you something about how much the team values each other's time.

None of these things announce themselves as problems. They accumulate quietly, and by the time they're visible they've already shaped the culture. Once it becomes normal to leave a mess, it becomes the standard.

---

The principle is simple: respect for space and tools is essential.

This sounds obvious. It mostly goes unpracticed.

Respecting the space means leaving things in good condition when you're done with them. Merging or deleting the branch. Closing the ticket. Cleaning up the test data you generated while debugging. Not leaving a half-finished refactor in main because you got pulled onto something else. Not merging a PR with a console.log you forgot to remove. Not shipping a feature with dead code from the previous version still sitting next to it.

Respecting the tools means keeping them working. If the build is broken, fix it before you move on. If a test is flaky, fix it or delete it - a flaky test is worse than no test because it erodes trust in the entire suite. If the local dev setup has a step that doesn't work anymore, update the documentation or fix the step. Don't silently work around it and leave the next person to discover it the same way you did.

---

The problem with mess is that messes normalize.

The first dead file someone leaves in the codebase is slightly awkward. The second is less so. By the tenth, nobody thinks about it. The standard has shifted. What was a lapse is now just how things are here.

This is the mechanism by which a codebase that was clean becomes a codebase that everyone complains about. Not one bad decision. Not a single catastrophic shortcut. A thousand small lapses, each of which was low-stakes at the time, compounding until the accumulated disorder is the dominant feature of the environment.

The same mechanism runs in reverse. Every time someone cleans up a thing they didn't make a mess of - removes the dead code they found while working on something else, fixes the flaky test that was bothering everyone, updates the outdated doc - they push the standard slightly upward. The team notices, even if they don't say anything. It becomes slightly more normal to leave things clean. That also compounds.

---

The practical test is: when you're done with something, would the next person encounter the environment in better shape than you found it?

Not perfect. Not comprehensively refactored. Just better. A little cleaner, a little more organized, a little closer to the state it would be in if everyone had always cared about it.

That's not a high bar. It's a consistent one. And consistency, over time, is what determines whether the environment supports the work or fights it.

The codebase is shared space. Treat it accordingly.
