---
layout: post
title: "The Algorithm of Governance"
meta: "$ cat /dev/democracy | grep transparency"
description: "Four practices software borrowed from nowhere in particular and refined until being wrong stopped being fatal. Which of them survive translation into government, and the exact place the metaphor breaks."
tags: [engineering, policy, metrics, method]
---

**Everything worth stealing from software engineering exists for one reason: to make being wrong survivable.**

## What software is good at

Software is not admirable because it is fast. Most of it is slow, and the fast parts are fast for boring reasons. It is admirable because a large system, built by people who mostly have never met, changing every day, can be wrong on Tuesday and correct by Wednesday — and the mechanism for that is written down and available to anyone.

Government has no equivalent. A programme that turns out to be wrong in its second year is usually still running in its eleventh, not because anyone defends it but because the machinery for noticing and the machinery for undoing were never built. Not dismantled. Never built.

So the question isn't whether governing is *like* coding. It isn't, and I'll say exactly where the analogy breaks. The question is narrower: which specific practices make error cheap, and which of those survive translation?

There are four. It is a shorter list than the metaphor usually implies.

## 1. The change is written down before it happens

Not the decision. The *proposed* decision, in advance, with the reasoning attached, in a form someone else can object to.

This sounds trivial and it is the whole game. The reason a code review works is not that reviewers are clever. It is that writing down what you intend to do, before you do it, surfaces a good share of your own errors to you while you are still typing. The reviewer catches a second tranche. Nobody in the loop had to be exceptional.

India has a partial version of this in pre-legislative consultation policy, which asks that draft laws be published for thirty days of comment. It is honoured inconsistently and it has no teeth. The gap between that and a functioning review process is not philosophical. It is that one is mandatory and blocking, and the other is a courtesy.

## 2. Someone who knows the area has to read it

Review by a generalist is theatre. The value is entirely in the reviewer having built the thing before and remembering how it failed last time.

This is the practice that most obviously fails to translate, because legislatures are built on the opposite premise: that a representative's mandate qualifies them for any subject placed in front of them. A parliamentary standing committee is the closest existing analogue, and its members are assigned by party arithmetic rather than by what they know.

## 3. It goes out to a few before it goes out to everyone

Canary releases, staged rollouts, feature flags — the family of techniques for limiting the blast radius of a mistake. You ship to one percent, watch the instruments, and only widen when the instruments say nothing is on fire.

Pilots exist in policy and they are usually decorative. A pilot that cannot fail is not a pilot; it is a press event held early. The test is whether anyone specified, in writing and before launch, the result that would stop the rollout.

## 4. You can put it back

The one that matters most, and the one almost nothing in government has.

A revert is not an admission of incompetence. In a well-run system it is a Tuesday. The teams that revert most freely ship the most ambitious changes, precisely because the cost of being wrong has been engineered down to a few minutes. The teams that cannot revert become conservative, then sclerotic, then obsolete.

> **Ambition is downstream of reversibility. A system that cannot undo will eventually stop trying.**

Sunset clauses are the closest legislative instrument, and they are rare, and they are routinely extended without anyone re-examining the case. A rollback that requires the same effort as the original launch is not a rollback.

## Where the metaphor breaks

Now the part that would be dishonest to leave out.

**Goodhart's law eats this whole approach if you let it.** The moment a measure becomes a target, it stops measuring what it measured. Ask a hospital to reduce waiting times and it will reduce recorded waiting times. Ask a police force to reduce reported crime and reports will fall. Every one of the four practices above depends on instrumentation, and instrumentation in a system full of people who are being judged by it is a live adversarial problem, not a dashboard.

Software has a mild version of this — teams gaming their own metrics — and it is mild because the numbers usually come from machines that have no stake. In government the numbers come from the people being measured. That is a different discipline, and anyone selling you "metrics for policy" without saying so is selling you a dashboard that will be beautiful and false.

The partial answer, and it is only partial: measure things that are expensive to fake, prefer numbers collected by someone with no stake in them, and treat any metric that improves suspiciously fast as a bug report about the metric.

**The second break is worse. You cannot revert a year of someone's life.** A failed deploy costs downtime. A failed benefits transition costs people their rations, and there is no version control that gives those months back. This is why staged rollout is not one practice among four but the load-bearing one: the point of the small pilot is that the irreversible harm stays small.

And a third, which is really a warning about ourselves. **Conway's law** says a system's architecture ends up mirroring the communication structure of the organisation that built it. It holds outside software too. Build a party with a charismatic centre and you will produce centralised governance no matter what the manifesto says. The org chart is the first line of the specification, and it is written before anyone notices they are writing it.

## The test

None of this is a claim that governing is engineering. It is a claim that four specific habits make error cheap, that government has approximately none of them, and that this is a design choice rather than a law of nature.

So the version of the five tests that applies here: **does the proposal make being wrong cheaper, or does it only make being right more likely?** The second is a wish. The first is a mechanism.

Most reform is the second, which is why most reform requires better people, which is why most reform is fuel mass.

Tell us where this is wrong.

**`#desh>_`**
