---
layout: post
title: "Vibes Don't Maintain"
date: 2026-10-14 21:00:00 +0200
author: Alex
description: "A friend built an app for his restaurant with Claude Code and asked me to host it. What he had was a click-dummy. The parts of software you can see are the cheap part. The parts you can't are the product."
tags: [xp, ai]
---

Since ChatGPT took off, people have been coming up to me to say some version of "you people will be out of a job soon."

Most of them were managers. They knew it was provocative, and they wanted to see how I'd react - partly to test the waters on whether this was a real scenario. What they had in common was that none of them had a clear idea of what software development actually is. Not what it looks like from the outside. What it is.

Last week I got the best version of that conversation I've had so far.

---

A friend of mine owns a restaurant. He told me he'd built an app for it with Claude Code - a web app to manage tasks and processes for his staff. He was proud of it, and he had every right to be. He had never written a line of code and he had a thing on a screen that did what he described.

I had a look. It was nice. Clean layout, sensible flow, data that persisted between page loads so it felt like a working system.

Then I started poking. No responsive layout - it broke on the phones his staff would actually use. No dark mode 🏴‍☠️. No login, so no notion of who did what. No settings. No translations, in a kitchen where half the team doesn't speak the language the app was written in. No error states. No handling of the empty case, the duplicate case, the two-people-edit-the-same-thing case. The data "persisted" in a way that would survive a refresh and not much else.

It was a click-dummy. A prototype. A perfectly good proof of concept for a first round of conversations about whether the idea holds up - which is a real and valuable thing to have.

Then he asked me if I could host it for him and do ops.

---

This is the biggest misunderstanding people have about software, and it has nothing to do with AI.

People see the surface. They see the parts that work. They don't see the parts that run when something goes wrong, the parts that exist to stop things going wrong, or the parts that have never once executed in production because they're there for a worst case someone sat down and imagined.

The seatbelt and the airbag in your car have, with luck, never done anything. That doesn't make them useless. You don't buckle up because the law says so or because the car beeps at you. You buckle up because you understand that one day you might need it. Software is mostly seatbelts. The happy path - the thing the demo shows - is the smallest part of the codebase.

My friend, understandably, didn't see that. His read was that the app works 100% as intended, so 90% of the work is done. The rest is hosting. And I shouldn't overcomplicate it.

---

Here's how that version plays out.

The prototype came almost free and almost instantly. He decides the product is done. He might even get it in front of users - his staff start using it for real shifts, real tasks, real schedules.

Then something goes wrong. The database file corrupts. A dependency update breaks something. Someone finds the app on the open internet and has a look around. An edge case fires that nobody wrote down. Or my personal favorite: daylight saving time, and every shift in the schedule is off by an hour.

Everything goes boom.

He doesn't know what he built. He doesn't know why it was built the way it was - the reasoning lived in a chat session that's gone. He doesn't know what to look for or where to start looking. There is no spec, no test, no document, no commit message that explains the intent of anything.

At that point he has two options. Find someone to fix it and prepare to hand them all his money, because the first week of that engagement is pure archaeology. Or flee the country.

That is what "vibes don't maintain" means in practice. The vibe got him to the demo. Nothing carried forward from there.

---

None of this is "don't use AI." We use it every day. But two things are true at the same time.

First: AI does not make you a software engineer if your background is baking bread, any more than your oven at home makes you a chef. It makes execution cheap. It does nothing about knowing what to execute, or what to do when the execution fails.

Second: shit in, shit out. If the input is a loose description of what the happy path looks like, the output is a happy path. The AI will not invent the seatbelts for you. It doesn't know you'll need them, because you didn't.

What survives a boom is not the code. It's the record of what the code was supposed to do - the stories, the specs, the decisions - written down somewhere a human or an agent can read them back. Ours are markdown files in git, kept with [bacon-tracker](https://github.com/bybacon/bacon-tracker). My friend has a chat history he can't find anymore.

That record is what you're paying for. Not the click-dummy.

There's a second question hiding in his request, and in all those "you'll be out of a job" conversations: if the tool really can do my job, what exactly was I still for? But that's for another day.

---

I called him the next day. I told him I got myself a Thermomix - the one with AI - and was planning to open a restaurant the week after.

He laughed. Then he went quiet for a second.

I hope he got it. But knowing him I think he did not.
