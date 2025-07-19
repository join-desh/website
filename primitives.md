---
layout: default
title: "Democracy Primitives"
description: "Exploring the fundamental building blocks of modern democratic systems"
permalink: /primitives/
---

<main class="container">
    <section class="hero">
        <h1>Democracy Primitives</h1>
        <p>The fundamental building blocks of software-defined governance</p>
    </section>

    <section class="blog">
        <h2>Building Blocks of Modern Democracy</h2>
        <p class="blog-intro">Exploring the core mechanisms and algorithms that power transparent, efficient, and expert-driven governance systems.</p>
        
        <div class="blog-posts">
            {% for post in site.categories.primitives %}
            <article class="blog-post">
                <h3>{{ post.title }}</h3>
                <div class="blog-meta">{{ post.meta | default: "$ ./democracy --analyze-primitive" }}</div>
                <p>{{ post.description | default: post.excerpt | strip_html | truncate: 200 }}</p>
                <div class="post-tags">
                    {% for tag in post.tags %}
                    <span class="tag">#{{ tag }}</span>
                    {% endfor %}
                </div>
                <a href="{{ post.url }}" class="read-more">Read More</a>
            </article>
            {% endfor %}
        </div>
    </section>
</main>

<style>
.tag {
    display: inline-block;
    background: rgba(0, 204, 51, 0.2);
    color: #00cc33;
    padding: 0.2rem 0.5rem;
    border-radius: 4px;
    font-size: 0.8rem;
    margin-right: 0.5rem;
    margin-top: 0.5rem;
}

.post-tags {
    margin-top: 1rem;
}
</style>