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
        <div class="blog-posts">
            {% for post in site.categories.primitives %}
            <article class="blog-post">
                <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
                <div class="blog-meta">{{ post.meta }}</div>
                <p>{{ post.description }}</p>
                <div class="post-tags">
                    {% for tag in post.tags %}
                    <span class="tag">#{{ tag }}</span>
                    {% endfor %}
                </div>
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