---
layout: post
title: "The Curse of the Clever Solution"
date: 2026-09-03 18:00:00 +0200
author: Alex
description: "Clever code is satisfying to write and painful to read. The author spent an hour finding the elegant path. Every future reader spends an hour reconstructing it. Write for the reader."
tags: [simplicity, culture]
---

There is a specific kind of dread that comes from opening a file and finding something ingenious.

Not clever in the "oh, that's tidy" way. Clever in the "I have to read this four times before I understand what it does, and even then I'm not sure I understand why" way. Metaprogramming that generates methods at load time. A chain of functional transforms that reduces fifty lines to three but requires deep familiarity with the paradigm to follow. A macro that behaves differently depending on context you have to trace three files to discover.

The author of this code was clearly smart. And they're probably gone.

---

The problem with clever code is not that it's wrong. Usually it works. The problem is the asymmetry it creates between writing and reading.

Writing a clever solution is satisfying. You've found the elegant path through a complex space. The code does something non-trivial and it does it briefly. It feels like mastery of the problem, of the language, of the particular trick being applied.

Reading someone else's clever solution is different. You don't have the context they had when they wrote it. You don't know which alternatives they considered and rejected. You don't know the constraint that made brevity important. You have the code and the behavior and nothing else. And the code is the most compressed possible representation of the decision, which makes it the hardest possible thing to understand.

The author spent an hour finding the clever path. Every reader spends an hour per encounter trying to reconstruct it.

---

This shows up in predictable forms.

In dynamic languages, it's the method that generates other methods - ten lines of metaprogramming replacing three hundred lines of repetition. The author was right that the repetition was bad. The metaprogramming is, technically, less code. But now every developer who works in this area needs to understand the generation mechanism before they can understand any of the generated methods. The cognitive cost is front-loaded, mandatory, and invisible until someone tries to debug something that doesn't behave the way the template says it should.

In type systems, it's the constraint that encodes a business rule as a compile-time invariant. Theoretically elegant. In practice, you spend twenty minutes reading error messages that describe structural problems in the type machinery rather than the actual mistake you made.

In algorithms, it's the O(n log n) solution to a problem that only ever runs on twenty items. The O(n²) version would have been slower by microseconds and readable by everyone. Instead someone reached for the sophisticated approach, and now the obvious fix - adding a special case for empty input - requires understanding the entire algorithm before you can safely insert it.

The common thread: the cleverness solves a real problem, but the complexity it introduces doesn't pay for itself.

---

There are situations where cleverness is the right call. A parser, a serialization library, a compiler - these are systems where sophistication is the product. The whole point is to do something non-trivial, and the code reflects that. In these cases, complexity is justified and the audience expects it.

Similarly: performance-critical paths where the clever solution is measurably better and the alternatives are genuinely unacceptable. If you've benchmarked the naive approach and it can't meet the requirement, the sophisticated one is not an indulgence - it's a constraint. Document the benchmark. Leave a breadcrumb for the reader who comes after you.

Sometimes the smart solution is the right one. But "right" should mean *necessary*, not *preferred*. You chose it over simpler alternatives for a reason you can explain, not because it was more interesting to write.

---

The test I've started applying: if I had to hand this code to a developer who is competent but unfamiliar with this part of the system, how long before they understand it well enough to change it safely?

For most business logic, the answer should be minutes. A few hours if the domain is genuinely complex. If the answer is "days" or "only after reading the design document from 2019," you've built a trap.

Code outlives its authors. The developer who writes something clever and moves on has made a decision that every future reader will pay for. That's not craftsmanship. It's debt with no due date - it just sits there, compounding as slower changes, more bugs, and more time spent reading before anyone can write.

---

Write the boring version first. If it's too slow, measure. If it's too long, find the repetition and extract it cleanly. If it still can't be simple, make it as clear as possible and leave a note explaining why.

The reader who comes after you is often you, six months later. They deserve better than a puzzle.
