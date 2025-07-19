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

    <section class="documents">
        <h2>Research Documents</h2>
        <p class="blog-intro">In-depth analysis and technical specifications for democracy primitives.</p>
        
        <div class="document-grid">
            <div class="document-card">
                <h3>📄 FlowVote Litepaper</h3>
                <p>Technical specification for liquid democracy implementation with expert delegation and transparent voting mechanisms.</p>
                <a href="/assets/documents/FlowVote-1.0.0.pdf" class="download-link" target="_blank">Download PDF</a>
            </div>
        </div>
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

.documents {
    margin-bottom: 4rem;
}

.document-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.document-card {
    background: rgba(0, 20, 0, 0.3);
    border: 1px solid #00cc33;
    border-radius: 8px;
    padding: 2rem;
    transition: all 0.3s ease;
}

.document-card:hover {
    background: rgba(0, 20, 0, 0.5);
    border-color: #00ff41;
    transform: translateY(-2px);
}

.document-card h3 {
    color: #00ff41;
    margin-bottom: 1rem;
    font-size: 1.2rem;
}

.document-card p {
    color: #cccccc;
    margin-bottom: 1.5rem;
    line-height: 1.6;
}

.download-link {
    display: inline-block;
    background: #00cc33;
    color: #000000;
    padding: 0.75rem 1.5rem;
    text-decoration: none;
    border-radius: 4px;
    font-weight: 500;
    transition: all 0.3s ease;
}

.download-link:hover {
    background: #00ff41;
    transform: translateY(-1px);
}

.download-link::before {
    content: '⬇ ';
    margin-right: 0.5rem;
}
</style>