---
layout: post
title: "Liquid Democracy, and What Went Wrong Last Time"
meta: "$ ./democracy --mode=liquid --delegate=expert"
description: "Delegate your vote per domain, to someone who knows more, and take it back whenever you like. It has been tried at scale once. Three things went wrong, and only one of them was a software problem."
categories: [primitives, democracy-theory]
tags: [liquid-democracy, delegation, voting-systems, flowvote]
---

**The idea is good enough that it has been tried. That is more than most governance proposals can say, and it means we get to skip the speculation and read the telemetry.**

## The idea

You get one vote. Today you spend it once every five years on a person who will then decide several thousand questions on your behalf, most of which neither of you has thought about.

Liquid democracy unbundles that. Vote yourself on the questions you care about. On the rest, name someone whose judgement you trust — and name a different someone per subject, so your cousin the cardiologist holds your health vote and nobody holds your view on spectrum policy just because they hold your view on hospitals. The delegation passes along: if your cardiologist delegates paediatric questions onward, your vote follows. And you can pull it back at any moment, including on a single question, without a conversation.

Representative democracy with the term length set to zero and the granularity set to one subject. Put that way it is hard to argue against, which is usually the point at which you should go and find out whether anyone has tried it.

## Somebody tried it

Germany's Pirate Party ran liquid democracy for real, on software called LiquidFeedback, from around 2010. Not a pilot with forty students. A national political party with tens of thousands of members, at a moment when it was winning seats — Berlin in 2011, then three more state parliaments in 2012.

By 2013 it had failed to enter the Bundestag and the project was effectively over. The software was not why the party collapsed; that had more to do with the ordinary things that kill new parties. But the experiment ran long enough to produce data, and the data says three specific things.

## Failure one: the votes pooled

The central worry about delegation is that it concentrates, and it did.

Researchers who analysed the Pirate Party's LiquidFeedback data found a small number of "super-voters" holding delegated power far out of proportion to their number. A handful of accounts could swing a great many issues on their own. That is exactly the thing the design was meant to avoid, arriving through the front door: if delegation is frictionless and reputation is visible, everyone routes to the same few visible people.

Two honest qualifications, because the finding gets quoted badly in both directions. The same researchers found no evidence that the super-voters actually voted differently from the general membership, or that they used the power abusively. And concentration is not obviously worse than the status quo — a member of parliament also holds a great many delegated votes, holds them for five years, and cannot have them withdrawn on Tuesday.

Still, the honest reading is: **liquid democracy does not abolish the concentration of political power. It makes concentration voluntary, visible, and revocable.** Those are real improvements and they are smaller than the pitch implies.

## Failure two: almost nobody showed up

Of a party with tens of thousands of members, a minority ever registered on the system and a much smaller minority used it regularly. Deciding things turns out to be work, and most people, given a frictionless mechanism for participating in everything, participate in nothing.

There was a structural reason, and it is the more instructive one. Under German party law, certain decisions have to be taken by member assemblies. LiquidFeedback could not be binding, so it functioned as an elaborate opinion poll that the party's formal organs were free to ignore — and sometimes did.

**Participation follows consequence.** People do not turn up for a mechanism whose output is advisory, and no amount of interface design fixes that. Any deployment of this that is not wired to a real decision will produce the same graph.

## Failure three: it cannot keep a secret

This is the deep one, and it is where the software problem actually lives.

The secret ballot exists because a vote you can prove you cast is a vote someone can buy or beat out of you. It is not a nicety; it is the single most important voting technology of the last two centuries.

Liquid democracy is in direct tension with it. To pass a delegated vote along a chain, the system has to know who delegated to whom. To let you verify your vote was counted, it has to give you something. LiquidFeedback resolved this by making activity substantially visible within the system, on the reasoning that a political party is not a state and that accountability mattered more there than secrecy.

For a party of volunteers, defensible. For anything with real stakes attached, unacceptable. A visible delegation graph is a coercion map: it shows an employer, a landlord, a moneylender or a caste association exactly whose vote to lean on and whether the leaning worked.

**This is the requirement that decides whether the idea is deployable at all:** delegation has to be transitive and revocable and verifiable, while remaining unlinkable to a person by anyone, including the people running it. That is a cryptography problem rather than a governance problem, and unlike the first two failures it is the kind of problem that has answers.

It is the problem [FlowVote](/primitives/) exists to answer, and the litepaper should be read as a claim to be attacked rather than a description of something finished.

## Against the five tests

**Exhaust velocity, or fuel mass?** Velocity, if it works. It does not ask anyone to be more civic-minded. It changes what one informed person's judgement is worth by letting it carry weight it currently cannot.

**Removes the choke point, or polices it?** Removes one and creates another. It deletes the five-year bundling of every question into one candidate. It creates the super-voter. That trade is favourable only because the new choke point can be dissolved by anyone, unilaterally, in a second.

**Survives bad people?** Not yet. With a visible delegation graph, a coercive actor wins. Fix the cryptography and it survives; leave it and it is a prayer.

**Orbital economics?** Yes. Expensive to specify and verify, nearly free to run. The marginal cost of the ten millionth delegation is nothing.

**Staging plan?** Weakest answer. What dissolves a super-voter who has held a domain for fifteen years and become the person everyone routes to by default? Automatic delegation expiry is the obvious candidate — delegations lapse unless renewed, so accumulated power decays rather than compounds. We think that is right. We are not confident, and it is the part of the design most worth arguing with us about.

Four and a half out of five, with the failing marks in known places. That is roughly the honest position, and it is a better one than the last decade of writing on this subject has generally offered.

Tell us where this is wrong.

**`#desh>_`**
