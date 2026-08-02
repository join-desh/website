---
layout: default
title: "Primitives · #desh>_"
description: "Three open protocols that make software-defined governance real: Amplifier, Pulse and FlowVote. Read the litepapers."
permalink: /primitives/
---

<section class="hero" style="padding-bottom:2rem">
  <div class="container narrow">
    <span class="eyebrow">Primitives</span>
    <h1 style="font-size:clamp(2.4rem,6vw,4rem)">The parts of the engine.</h1>
    <p class="lede">Three open protocols: media that cannot be bought, governance that can be audited, and a vote you can lend to someone who knows more than you and take back the same afternoon. Each has a litepaper below. They are specifications rather than manifestos, and the useful response to a specification is an objection.</p>
  </div>
</section>

<section class="section" style="padding-top:1rem">
  <div class="container">
    <div class="grid grid-3">
      <div class="primitive reveal">
        <div class="p-name"><h3>Amplifier</h3><span class="badge">Media</span></div>
        <p>Reach as something earned rather than bought. Influence is metered in two units, Watts and Volts, and there is no route to purchasing either. The question the protocol exists to answer: what does a media layer look like when paid promotion is not a feature someone switched off, but a thing the design cannot express?</p>
        <a href="/assets/documents/Amplifier-1.0.0.pdf" target="_blank" rel="noopener" class="link-arrow">Read litepaper <span class="arrow">→</span></a>
      </div>
      <div class="primitive reveal">
        <div class="p-name"><h3>Pulse</h3><span class="badge">Governance</span></div>
        <p>Governance and funding as a process that runs, not an event that recurs. Participation is continuous, delegation moves as circumstances do, and money travels through contracts anyone can read. The ledger is not the point. The point is that an allocation and the argument for it are the same record.</p>
        <a href="/assets/documents/Pulse-1.0.0.pdf" target="_blank" rel="noopener" class="link-arrow">Read litepaper <span class="arrow">→</span></a>
      </div>
      <div class="primitive reveal">
        <div class="p-name"><h3>FlowVote</h3><span class="badge">Voting</span></div>
        <p>Liquid democracy, made operational. Vote on what you care about and hand the rest to someone whose judgement you trust, one domain at a time. Delegation is transitive, revocable the moment you change your mind, and verifiable without exposing who you are.</p>
        <a href="/assets/documents/FlowVote-1.0.0.pdf" target="_blank" rel="noopener" class="link-arrow">Read litepaper <span class="arrow">→</span></a>
      </div>
    </div>
  </div>
</section>

{% if site.categories.primitives %}
<section class="section" style="padding-top:0">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Deep dives</span>
      <h2>Working notes</h2>
      <p>Longer pieces on the mechanisms these protocols are assembled from.</p>
    </div>
    <div class="grid grid-3">
      {% for post in site.categories.primitives %}
      <a class="post-card reveal" href="{{ post.url }}">
        <div class="p-meta">{{ post.meta | default: post.date | date: "%b %-d, %Y" }}</div>
        <h3>{{ post.title }}</h3>
        <p>{{ post.description | default: post.excerpt | strip_html | truncate: 150 }}</p>
        <span class="link-arrow">Read <span class="arrow">→</span></span>
      </a>
      {% endfor %}
    </div>
  </div>
</section>
{% endif %}
