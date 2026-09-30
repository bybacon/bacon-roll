---
layout: post
title: "The Spec That Runs"
date: 2026-09-30 21:00:00 +0200
author: Alex
description: "Every team has two descriptions of what their software should do: the tickets and the code. Neither is authoritative. The spec that runs is - and most teams don't have one."
tags: [xp]
---

Every team has two representations of what their software should do. The first lives in the project management tool - Jira tickets, Notion pages, PRDs, whatever they're using. The second lives in the test suite. Both are supposed to describe the same behavior. They rarely do.

The ticket says "Users can filter search results by category." The test says `expect(response.body).to include('Electronics')`. These are not the same specification. One is a product intention. The other is an implementation artifact. As the product evolves, tickets stay frozen, tests get updated, and the two drift apart.

This is the default state. Most teams live with it.

Spec-driven development is the refusal to accept that drift as inevitable.

---

The core idea is simple: the spec and the test should be the same document. Not two documents that describe the same behavior. One document, in a form that is both human-readable and machine-executable.

This is what Gherkin gives you. A feature file is a requirements document that runs. It describes what the system should do, who benefits, and what specific behaviors constitute done - in language a product manager can read and a test runner can execute.

For a booking management feature start like this:

```gherkin
Feature: Booking Manager

As Molly
I want to manage Bookings for my Events
So that I can track who is attending, who is waitlisted, and who canceled

Scenario: Arthur books a spot for an available Event
  Given Molly has an available Event with open capacity
  When Arthur visits the new booking page for the Event
  And Arthur fills in his name and email address
  And Arthur submits the booking
  And Arthur confirms the booking via the email link he got
  Then Arthur should see the booking on the Event bookings list
  And The booking should be confirmed
```

That file is the spec. It describes behavior that matters to actual users in a form that survives a demo, a PM review, and a CI pipeline. The same document does all three jobs.

---

There's a second part of spec-driven development that doesn't get enough attention: the order.

The spec runs first. Before any implementation exists.

You write the feature file. You write the step definitions. You run the suite. It fails. That failure - the red - is the most important moment in the process. It proves the spec was written correctly, that the test infrastructure is wired up, and that when you write code to make it pass, the green result actually means something.

This sounds obvious. Teams skip it constantly.

The way it usually gets skipped: someone implements a feature, then writes the spec to document what they built. The spec runs green on the first try. Everyone feels good. The problem is you have no idea if that test would catch a broken implementation. You only know it doesn't catch the current one. You wrote a test that proves the present state, not one that will catch the future regression.

The red proves the spec was real. Without it, you just have green.

---

Where the spec lives matters as much as what it says.

Most teams keep specs in the test directory of the codebase, isolated from wherever product requirements live. This creates the same split in a different location: requirements in one system, tests in another.

The pattern that works is keeping specs in version control alongside everything else - treating them as the primary product artifact, not a byproduct of implementation.

For us, feature files live in a `docs/` directory with sequential IDs: `BCN-001-booking-manager.feature`, `BCN-002-authentication-manager.feature`. Each file has frontmatter tracking its status. Features move through four stages: `1_icebox` → `2_backlog` → `3_started` -> `4_done`. The stack-ranked backlog is a text file, also in git.

There is no Jira. No Linear. The spec is the story is the ticket is the test.

(bacon-tracker)[https://github.com/bybacon/bacon-tracker] is the tooling that makes this concrete:

```
rake story:feature['Booking Manager']  → features/1_icebox/BCN-001-booking-manager.feature
rake story:commit[BCN-001]             → moves to 2_backlog, adds to backlog.md
rake story:start[BCN-001]              → moves to 3_started
rake story:done[BCN-001]               → moves to 4_done
```

Git becomes the audit trail. The story file is the commit. The test run is the verification. Nothing external can drift from what the code actually does, because there is no external system.

---

The caveat: good Gherkin is harder to write than it looks.

Bad Gherkin is a Jira ticket in a different format. It's either vague ("When the user does something / Then it works"), or over-specified ("Given the database has a User record with id=4 and email='test@example.com'"), or it describes implementation instead of behavior.

Good Gherkin describes behavior at the level of abstraction where the test catches regressions that actually matter. "When Arthur submits the booking / Then the booking should be confirmed" is a behavior. "When `POST /bookings` is called with valid params / Then `response[:status]` is `confirmed`" is an implementation test wearing a Gherkin costume. The first survives refactoring. The second breaks every time you touch the internals.

The tooling creates the structure. The thinking that goes into the scenarios is still yours.

---

The deeper value of spec-driven development is not test coverage. It's clarity.

When the spec runs, you know exactly where you stand. Green scenarios are done. Red scenarios are not. There is no ambiguity about what done means, because done is defined in executable form.

That's rare in software. Most teams operate with done as a matter of interpretation - does it match the ticket? Does it match what the PM remembers from the meeting? Does it pass QA's judgment call? Each layer of interpretation is a place where the thing you built can drift from the thing that was needed.

A spec that runs eliminates most of that drift. Not by adding rigor, but by collapsing two separate representations of truth into one.
