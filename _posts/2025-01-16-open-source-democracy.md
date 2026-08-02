---
layout: post
title: "Open Source Democracy"
meta: "$ git commit -m 'democracy: implement transparency patch'"
description: "Open source is a permission structure, not a mood. What it really gives you is read access, the right to propose, the right to fork and a written constitution — and one of those four is unavailable to a country."
tags: [open-source, governance, forking, commons]
---

**Open source is not collaboration. It is a permission structure, and three of its four permissions transfer to a country. The fourth is the interesting one.**

## The claim, stated carefully

"Run the party like an open source project" is the sort of line that sounds radical and means nothing until someone specifies it. Plenty of organisations describe themselves as open and mean that they publish a newsletter.

So here is what open source actually is, stripped of the culture around it. It is four permissions, granted in advance, to people the project has never met.

**You may read everything.** Not a summary. The source, the discussion that produced it, the objections that lost.

**You may propose a change.** Anyone. Without asking first, without knowing anyone, without a sponsor.

**You may fork.** If the maintainers reject your change and you believe they are wrong, you may take the entire work and continue it yourself.

**The rules for exercising the first three are themselves written down.** In the mature projects. This is the rarest one and the one that separates a project from a personality.

Notice what is missing from that list. Nothing about consensus, community, or everyone having a voice. Open source is not democratic in the way its advocates imply, and pretending otherwise is where the analogy usually goes wrong.

## The part that is a lie

"Given enough eyeballs, all bugs are shallow." Eric Raymond wrote that in 1997 and it became the movement's founding empirical claim: openness produces scrutiny, and scrutiny produces correctness.

It is not reliably true, and the counterexamples are severe.

Heartbleed sat in OpenSSL for around two years before it was found in 2014 — a flaw in the code securing a large fraction of the world's encrypted traffic, in a project anyone could read. Anyone could. Almost nobody did. At the time of discovery, the foundation behind it was taking in a couple of thousand dollars a year in donations and had roughly one person on it full time.

Then, in early 2024, a backdoor was found in XZ Utils, a compression library sitting quietly underneath most Linux distributions. It had been introduced by a contributor who spent about two years building a reputation, being helpful, and gradually taking over maintenance from an exhausted volunteer who had said publicly that he was struggling. It was caught because an engineer at Microsoft noticed his SSH logins had got about half a second slower and would not let it go.

Half a second. That is the margin by which one of the most patient supply chain attacks in history missed.

**Openness does not produce scrutiny. It produces the *possibility* of scrutiny, and possibility is not a mechanism.** Any design that relies on the public reading things is relying on attention, and attention is the scarcest input in any system involving humans.

This matters more for a country than for a library, because RTI taught the same lesson in a different register: the right to information is worth exactly as much as the number of people willing to file, and the state can outlast almost all of them.

## The part that works

Now the other side, because two projects have solved governance problems that political parties have not.

**Debian** has a written constitution, adopted in 1998. It defines who may decide what, how a decision is overturned, and what happens when the leadership and the membership disagree. The Project Leader is elected annually by the developers, using a Condorcet method, and can be recalled. Major decisions go to a General Resolution and are voted on by everyone with standing. This is a functioning constitutional democracy with a few thousand citizens, running continuously for over a quarter of a century, and almost nobody in political science has looked at it.

**Python** did something harder. For nearly three decades it ran on a benevolent dictator — Guido van Rossum, who created the language and held final say by informal consent. In 2018, after a bruising argument over a small syntax feature, he stepped down. What followed was not a succession crisis. The community wrote several competing governance proposals, voted on them, and adopted an elected five-member Steering Council. The founder left, the thing kept working, and the transition was itself a document anyone can read.

That is staging, executed voluntarily, by the person it cost the most. It is rarer in politics than in software by an embarrassing margin.

## The permission that doesn't transfer

Here is where the metaphor breaks, and it breaks hard enough that anyone using it should be required to say so.

**You cannot fork a country.**

Forking is what makes the rest of open source safe. It is the reason a maintainer who becomes unreasonable eventually loses: OpenOffice became LibreOffice, MySQL became MariaDB, Node briefly became io.js and then reconciled on better terms. The threat is usually enough. Maintainers behave because the community can leave and take the work with them.

Hirschman gave the two options their names in 1970: exit and voice. Open source has an unusually cheap exit, which is why its voice can afford to be messy. A country has almost no exit. Emigration is available to the wealthy and the credentialed and functionally closed to everyone else, which is another way of saying that the people with the least ability to leave have the most to lose from bad governance, and the least leverage over it.

Which yields a hard requirement rather than a nice sentiment. **When exit is unavailable, voice has to be engineered to a standard open source never needed.** The disagreement mechanisms have to be better than a mailing list. The recall mechanisms have to be real. The constitution has to be written before the founders are inconvenienced by it, because there is no fork to escape to if it isn't.

Elinor Ostrom spent a career on precisely this problem — communities managing a shared resource nobody can leave — and the design principles she drew out in 1990 read like a checklist most constitutions fail: clear boundaries on who is a member, rules matched to local conditions, those affected able to change the rules, graduated sanctions rather than a single catastrophic one, cheap and fast conflict resolution, and authority nested in layers rather than concentrated. She got a Nobel for it in 2009. It is the most useful governance literature in existence and it is almost never cited by people quoting Linus's law.

## What we take

Read access, unconditional. Not a transparency portal that publishes what it chooses. The working record, including the arguments we lost.

The right to propose, from anyone, with the reasoning attached and the rejection published when we reject it. The rejections are the interesting archive. Every party has a graveyard of ideas it declined and no party will show you the headstones.

A written constitution before we are big enough to need one, including the clause that removes us.

And an honest replacement for the fork, since we cannot offer the real thing. Everything we build gets specified openly enough that someone who thinks we have gone wrong can rebuild it without our permission and without our people. That is a weaker guarantee than a fork. It is the strongest one available at national scale, and a party that will not offer even that is asking for trust it has not earned.

Tell us where this is wrong.

**`#desh>_`**
