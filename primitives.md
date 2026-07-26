---
layout: default
title: "Primitives · #desh>_"
description: "The open protocols that make software-defined governance real: Amplifier, Pulse and FlowVote. Read the litepapers."
permalink: /primitives/
---

<section class="hero" style="padding-bottom:2rem">
  <div class="container narrow">
    <span class="eyebrow">Primitives</span>
    <h1 style="font-size:clamp(2.4rem,6vw,4rem)">The parts of the engine.</h1>
    <p class="lede">The fundamental building blocks of software-defined governance: open protocols, specified in the litepapers below.</p>
  </div>
</section>

<section class="section" style="padding-top:1rem">
  <div class="container">
    <div class="grid grid-3">
      <div class="primitive reveal">
        <div class="p-name"><h3>Amplifier</h3><span class="badge">Media</span></div>
        <p>A decentralised media protocol that transforms influence into an earned resource through Watts and Volts currencies, eliminating paid promotion while letting authentic community voices reach massive scale through earned influence.</p>
        <a href="/assets/documents/Amplifier-1.0.0.pdf" target="_blank" rel="noopener" class="link-arrow">Read litepaper <span class="arrow">→</span></a>
      </div>
      <div class="primitive reveal">
        <div class="p-name"><h3>Pulse</h3><span class="badge">Governance</span></div>
        <p>A decentralised governance and funding platform that turns democracy into a software-defined process: real-time citizen participation, dynamic delegation and resource allocation through blockchain-based smart contracts.</p>
        <a href="/assets/documents/Pulse-1.0.0.pdf" target="_blank" rel="noopener" class="link-arrow">Read litepaper <span class="arrow">→</span></a>
      </div>
      <div class="primitive reveal">
        <div class="p-name"><h3>FlowVote</h3><span class="badge">Voting</span></div>
        <p>Liquid democracy made practical: vote directly on what you care about, or delegate your vote to a trusted expert per domain. Transitive, revocable at any time, and cryptographically verifiable.</p>
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
      <h2>Building blocks of modern democracy</h2>
      <p>The core mechanisms and algorithms behind transparent, expert-driven governance.</p>
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
