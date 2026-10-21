---
layout: post
title: "Who's Actually Out of a Job?"
date: 2026-10-21 20:30:00 +0200
author: Alex
description: "Every decade has had a tool that promised software without developers. The hard part never moved. What AI actually makes cheap is the part managers thought was theirs - and engineers can do that part too."
tags: [xp, ai, teams]
---

I ended the [last post](https://roll.bybacon.com/2026/10/14/vibes-dont-maintain.html) with a question: if the tool can do my job, what was I still for?

The people asking were mostly managers. It's worth looking at what they thought my job was - and what they thought theirs was - because I think they had both backwards.

---

Start with the claim itself: a new tool will let people build software without understanding software. It's not new. No-code wasn't tried only once. It has been tried in every decade since computers got a mouse, and it died every time.

Microsoft FrontPage, 1996. Drag a box, type some text, click publish. Nobody would ever have to code a website again. That's why web development as a profession ended in 1997.

What actually happened is that FrontPage produced websites that looked like websites and behaved like a stack of pictures. The moment someone wanted a contact form that did something, or a page that changed based on who was looking at it, a developer got called. The tool collapsed the easy part to zero and left the hard part exactly where it was. Dreamweaver - FrontPage for people with taste - did the same thing with nicer defaults. Flash let you draw your way to a website that moved, right up until the platform itself was switched off and every one of those sites went dark on the same day.

PowerPoint was never sold as a way to build software, and it never became one. What it became was the tool for click-dummies. Screen, arrow, screen, arrow, and you had an app you could click through in a meeting. Click-through prototypes - Balsamiq, InVision, later Figma - were the same idea with better fidelity. Or again, for the people with taste. The deck was never wrong, just incomplete. It just described a surface of the happy flow, and every arrow hid a hundred decisions about what happens when the thing on the other side of it fails. To be fair, nobody ever cared about the error messages anyways.

Then Stack Overflow Driven Development. Search the error, paste the top answer, move on. It freed us from writing the code and, more importantly, from the guilt of not understanding it. If the internet hadn't said it was wrong, it was good enough. The rest was up to the compiler. Those codebases worked right up until they didn't, and then nobody could (or wanted to) say why any given block was there.

Each of these had its moment, its conference talks, and its "developers are over" headlines. Each one quietly ended up back in the hands of the developers it was meant to replace - or ended, full stop.

---

Agents like Claude Code, Codex, or Copilot are the same thing with the delay removed.

FrontPage needed you to lay out the page. PowerPoint needed you to draw the arrows. Stack Overflow needed you to find the right answer and glue it in. An agent takes a sentence and does all three, in minutes, and the result runs.

That's the real change. Not what's possible - how fast and how cheaply you reach the point where it *looks* done. That point used to be weeks away. Now it's an afternoon. The distance between "looks done" and "is done" hasn't moved. It just shows up sooner and more convincingly, and the bill for crossing it arrives later and bigger.

An agent can produce far more than FrontPage or PowerPoint ever could. But it shares one trait with the managers: it knows a nice-looking UI sells better than an hour-long monologue about the state machine behind an error case. Sex sells. Ask for an app and you get the parts that demo well.

So someone has to tell it to build that state machine, its states how they transition. Then someone has to check that it's correct. That's just one example out of hundreds. A human developer built those things for two reasons: they knew they had to be built, and they knew it would come back to them if they didn't. It was part of the job. The agent doesn't care. It will tell you it built what you told it to, and it did. Thinking outside the box is your job.

---

Now the part the managers got backwards.

What did they think they brought to the table? The idea. The business case. The pitch. The deck with the arrows. What did they think we developers brought? Typing. The slow, expensive conversion of their vision into something that runs.

If that were true, they'd be right to worry about us. The typing is what got cheap.

But look at what my restaurant friend produced with an agent in an afternoon: a deck with arrows that runs. That is the manager's deliverable, delivered by the tool. Idea to surface, the first-meeting demo - the thing that used to justify a role - now costs nothing and requires no one.

What it didn't produce is everything underneath. The seatbelts. The understanding of why it was built the way it was. The ability to open the hood when it breaks. That part didn't get cheaper. It got rarer, because fewer people on the way to the demo had to touch it. It's what we developers brought to the table all along, and we're still here, still bringing it.

Here's my hypothesis, then: AI makes the manager more redundant than the engineer.

Engineers can come up with ideas too. We always could but we were busy. If we really don't write the code anymore, that's a lot of afternoons freed up to notice what's missing, sketch it, and put it in front of someone. We can sell them - a working thing is the most persuasive pitch there is, and we can produce one as fast as anyone now. And when it goes wrong, we can fix it. That last one is the whole difference. The manager with an agent gets a click-dummy. The engineer with an agent gets a product, and keeps it running.

---

So what does the engineer actually bring, if not the typing?

A stack they know deeply. Not because Rails is better than Spring Boot or Laravel in the abstract, but because when something breaks at eleven at night you have to know where to look, and that knowledge doesn't come out of a prompt.

Behavior written down before the code, as scenarios that run. If the *what* is unambiguous, the *how* is easier to read, easier to hand to an agent, and easier to verify when it comes back. The right architecture does the same for structure: the moving parts have names and places.

And a record. Our stories, specs, and decisions are markdown files in git, kept with [bacon-tracker](https://github.com/bybacon/bacon-tracker). Markdown is human-readable and trivially safe to keep - and a folder of well-written markdown is enough to rebuild the whole thing from scratch, by a person or by whatever agent is current in three years. The code is disposable. The intent isn't.

None of that is new either. It's what engineers did when the typing was the slow part, too. The tools just stripped away enough of the typing that you can finally see it was never the job.

---

*bacon-tracker is open source: [github.com/bybacon/bacon-tracker](https://github.com/bybacon/bacon-tracker).*
