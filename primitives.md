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
        <p class="section-intro">In-depth analysis and technical specifications for democracy primitives.</p>
        
        <div class="document-grid">
            <div class="document-card">
                <h3>📄 FlowVote Litepaper</h3>
                <p>Technical specification for liquid democracy implementation with expert delegation and transparent voting mechanisms.</p>
                <a href="/assets/documents/FlowVote-1.0.0.pdf" class="download-link" target="_blank">View PDF</a>
            </div>
        </div>
    </section>

    <section class="blog">
        <h2>Building Blocks of Modern Democracy</h2>
        <p class="section-intro">Exploring the core mechanisms and algorithms that power transparent, efficient, and expert-driven governance systems.</p>
        
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
/* Typography and spacing system */
:root {
    --spacing-unit: 1.5rem;
    --spacing-xs: calc(var(--spacing-unit) * 0.5);
    --spacing-sm: var(--spacing-unit);
    --spacing-md: calc(var(--spacing-unit) * 2);
    --spacing-lg: calc(var(--spacing-unit) * 3);
    --spacing-xl: calc(var(--spacing-unit) * 4);
    --spacing-xxl: calc(var(--spacing-unit) * 6);
}

/* Page structure and vertical rhythm */
.hero {
    margin-bottom: var(--spacing-xxl);
    text-align: center;
}

.hero h1 {
    font-size: 2.8rem;
    line-height: 1.2;
    margin-bottom: var(--spacing-md);
    color: #00ff41;
    text-shadow: 0 0 30px rgba(0, 255, 65, 0.5);
    font-family: 'Fira Code', monospace;
    font-weight: 700;
}

.hero p {
    font-size: 1.3rem;
    color: #00cc33;
    max-width: 800px;
    margin: 0 auto;
    line-height: 1.6;
    opacity: 0.9;
}

/* Section spacing and typography */
section {
    margin-bottom: var(--spacing-xxl);
}

section h2 {
    font-size: 2.2rem;
    color: #00ff41;
    font-weight: 700;
    font-family: 'Fira Code', monospace;
    text-shadow: 0 0 20px rgba(0, 255, 65, 0.5);
    margin-bottom: var(--spacing-md);
    text-align: center;
    line-height: 1.3;
}

section h2::before {
    content: '$ ls /';
    display: block;
    font-size: 1rem;
    color: #00cc33;
    margin-bottom: var(--spacing-xs);
    text-shadow: 0 0 10px rgba(0, 255, 65, 0.3);
    font-weight: 400;
}

.section-intro {
    text-align: center;
    font-size: 1.2rem;
    color: #00cc33;
    margin-bottom: var(--spacing-lg);
    max-width: 800px;
    margin-left: auto;
    margin-right: auto;
    line-height: 1.6;
    opacity: 0.9;
    font-family: 'Fira Code', monospace;
}

/* Grid system */
.document-grid,
.blog-posts {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: var(--spacing-md);
    margin-top: var(--spacing-lg);
}

/* Card components */
.document-card,
.blog-post {
    background: rgba(0, 20, 0, 0.8);
    border: 1px solid #00ff41;
    border-radius: 8px;
    padding: var(--spacing-md);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    backdrop-filter: blur(10px);
    display: flex;
    flex-direction: column;
    height: 100%;
}

.document-card::before,
.blog-post::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 2px;
    background: #00ff41;
    box-shadow: 0 0 10px rgba(0, 255, 65, 0.5);
}

.document-card:hover,
.blog-post:hover {
    background: rgba(0, 255, 65, 0.05);
    box-shadow: 0 0 30px rgba(0, 255, 65, 0.2);
    border-color: #00ff41;
    transform: translateY(-2px);
}

/* Card typography */
.document-card h3,
.blog-post h3 {
    color: #00ff41;
    font-size: 1.3rem;
    font-weight: 600;
    font-family: 'Fira Code', monospace;
    text-shadow: 0 0 10px rgba(0, 255, 65, 0.3);
    margin-bottom: var(--spacing-sm);
    line-height: 1.4;
}

.document-card p,
.blog-post p {
    color: #00cc33;
    line-height: 1.7;
    font-family: 'Fira Code', monospace;
    margin-bottom: var(--spacing-sm);
    flex-grow: 1;
}

/* Blog meta and tags */
.blog-meta {
    font-size: 0.9rem;
    color: #00cc33;
    font-family: 'Fira Code', monospace;
    margin-bottom: var(--spacing-sm);
    opacity: 0.8;
    font-style: italic;
}

.post-tags {
    margin: var(--spacing-sm) 0;
    display: flex;
    flex-wrap: wrap;
    gap: var(--spacing-xs);
}

.tag {
    display: inline-block;
    background: rgba(0, 204, 51, 0.2);
    color: #00cc33;
    padding: 0.3rem 0.6rem;
    border-radius: 4px;
    font-size: 0.8rem;
    font-family: 'Fira Code', monospace;
    font-weight: 500;
    border: 1px solid rgba(0, 204, 51, 0.3);
    transition: all 0.3s ease;
}

.tag:hover {
    background: rgba(0, 204, 51, 0.3);
    border-color: #00cc33;
}

/* Action buttons */
.download-link,
.read-more {
    display: inline-block;
    background: transparent;
    color: #00ff41;
    text-decoration: none;
    font-weight: 500;
    font-size: 1rem;
    padding: 0.8rem 1.5rem;
    border: 1px solid #00ff41;
    border-radius: 4px;
    transition: all 0.3s ease;
    font-family: 'Fira Code', monospace;
    position: relative;
    overflow: hidden;
    margin-top: auto;
    text-align: center;
}

.download-link::before {
    content: '👁 ';
    margin-right: 0.5rem;
}

.read-more::before {
    content: '> ';
    margin-right: 0.3rem;
}

.download-link::after,
.read-more::after {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: rgba(0, 255, 65, 0.1);
    transition: left 0.3s ease;
}

.download-link:hover::after,
.read-more:hover::after {
    left: 0;
}

.download-link:hover,
.read-more:hover {
    background: rgba(0, 255, 65, 0.1);
    box-shadow: 0 0 15px rgba(0, 255, 65, 0.3);
    text-shadow: 0 0 10px rgba(0, 255, 65, 0.5);
    transform: translateY(-1px);
}

/* Responsive design */
@media (max-width: 768px) {
    :root {
        --spacing-unit: 1.2rem;
    }
    
    .hero h1 {
        font-size: 2.2rem;
    }
    
    .hero p {
        font-size: 1.1rem;
    }
    
    section h2 {
        font-size: 1.8rem;
    }
    
    .section-intro {
        font-size: 1rem;
    }
    
    .document-grid,
    .blog-posts {
        grid-template-columns: 1fr;
        gap: var(--spacing-sm);
    }
    
    .document-card,
    .blog-post {
        padding: var(--spacing-sm);
    }
}

@media (max-width: 480px) {
    .hero h1 {
        font-size: 1.8rem;
    }
    
    section h2 {
        font-size: 1.5rem;
    }
    
    .document-card h3,
    .blog-post h3 {
        font-size: 1.1rem;
    }
}
</style>