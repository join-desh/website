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
                <h3>📡 Amplifier</h3>
                <p>Decentralized media protocol that transforms influence into an earned resource through Watts and Volts currencies, eliminating paid promotion while enabling authentic community voices to achieve massive reach through earned influence.</p>
                <a href="/assets/documents/Amplifier-1.0.0.pdf" class="btn-base btn-secondary btn-pdf btn-responsive" target="_blank" aria-label="View Amplifier Litepaper PDF document">View PDF</a>
            </div>
            <div class="document-card">
                <h3>⚡ Pulse</h3>
                <p>Decentralized governance and funding platform that transforms democracy into a software-defined process, enabling real-time citizen participation, dynamic delegation, and resource allocation while eliminating traditional representatives through blockchain-based smart contracts.</p>
                <a href="/assets/documents/Pulse-1.0.0.pdf" class="btn-base btn-secondary btn-pdf btn-responsive" target="_blank" aria-label="View Pulse Litepaper PDF document">View PDF</a>
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
                <div class="blog-meta">{{ post.meta | default: post.date | date: "%B %d, %Y" }}</div>
                <p>{{ post.description | default: post.excerpt | strip_html | truncate: 200 }}</p>
                <div class="post-tags">
                    {% for tag in post.tags %}
                    <span class="tag">#{{ tag }}</span>
                    {% endfor %}
                </div>
                <a href="{{ post.url }}" class="btn-base btn-secondary btn-arrow btn-responsive" aria-label="Read more about {{ post.title }}">Read More</a>
            </article>
            {% endfor %}
        </div>
    </section>

</main>

<style>
/* Typography and spacing system */
:root {
    --spacing-unit: 2rem;
    --spacing-xs: calc(var(--spacing-unit) * 0.5);
    --spacing-sm: var(--spacing-unit);
    --spacing-md: calc(var(--spacing-unit) * 2);
    --spacing-lg: calc(var(--spacing-unit) * 3);
    --spacing-xl: calc(var(--spacing-unit) * 4);
    --spacing-xxl: calc(var(--spacing-unit) * 6);
    --spacing-xxxl: calc(var(--spacing-unit) * 8);
}

/* Mobile spacing adjustments */
@media (max-width: 768px) {
    :root {
        --spacing-unit: 1.5rem;
        --spacing-sm: 1.2rem;
        --spacing-md: 1.8rem;
        --spacing-lg: 2.4rem;
    }
}

/* Page structure and vertical rhythm */
.hero {
    margin-bottom: var(--spacing-xxxl);
    text-align: center;
    padding: var(--spacing-xl) 0;
}

.hero h1 {
    font-size: 3.2rem;
    line-height: 1.1;
    margin-bottom: var(--spacing-lg);
    color: #00ff41;
    text-shadow: 0 0 40px rgba(0, 255, 65, 0.4);
    font-family: 'Fira Code', monospace;
    font-weight: 700;
    letter-spacing: -0.02em;
}

.hero p {
    font-size: 1.4rem;
    color: #00cc33;
    max-width: 700px;
    margin: 0 auto;
    line-height: 1.7;
    opacity: 0.85;
    font-weight: 300;
}

/* Section spacing and typography */
section {
    margin-bottom: var(--spacing-xxxl);
    padding: 0 var(--spacing-sm);
}

section h2 {
    font-size: 2.4rem;
    color: #00ff41;
    font-weight: 600;
    font-family: 'Fira Code', monospace;
    text-shadow: 0 0 25px rgba(0, 255, 65, 0.3);
    margin-bottom: var(--spacing-xl);
    text-align: left;
    line-height: 1.2;
    letter-spacing: -0.01em;
    position: relative;
    padding-left: var(--spacing-md);
}

section h2::before {
    content: '';
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 4px;
    height: 60%;
    background: linear-gradient(to bottom, #00ff41, rgba(0, 255, 65, 0.3));
    border-radius: 2px;
}

.section-intro {
    font-size: 1.1rem;
    color: #00cc33;
    margin-bottom: var(--spacing-xl);
    max-width: 800px;
    line-height: 1.8;
    opacity: 0.8;
    font-family: 'Fira Code', monospace;
    font-weight: 300;
    margin-left: var(--spacing-md);
}

/* Grid system with generous spacing */
.document-grid,
.blog-posts {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
    gap: var(--spacing-xl);
    margin-top: var(--spacing-xl);
    padding: 0 var(--spacing-md);
}

/* Card components - minimal and spacious */
.document-card,
.blog-post {
    background: transparent;
    padding: var(--spacing-lg) 0;
    transition: all 0.4s ease;
    position: relative;
    display: flex;
    flex-direction: column;
    border-left: 1px solid rgba(0, 255, 65, 0.1);
    padding-left: var(--spacing-lg);
    margin-left: var(--spacing-sm);
}

.document-card:hover,
.blog-post:hover {
    transform: translateX(var(--spacing-xs));
    border-left-color: rgba(0, 255, 65, 0.4);
}

.document-card:hover::before,
.blog-post:hover::before {
    opacity: 1;
    transform: translateX(0);
}

.document-card::before,
.blog-post::before {
    content: '';
    position: absolute;
    left: -1px;
    top: 0;
    bottom: 0;
    width: 3px;
    background: linear-gradient(to bottom, #00ff41, rgba(0, 255, 65, 0.2));
    opacity: 0;
    transform: translateX(-10px);
    transition: all 0.4s ease;
    border-radius: 0 2px 2px 0;
}

/* Card typography with breathing room */
.document-card h3,
.blog-post h3 {
    color: #00ff41;
    font-size: 1.5rem;
    font-weight: 500;
    font-family: 'Fira Code', monospace;
    text-shadow: 0 0 15px rgba(0, 255, 65, 0.2);
    margin-bottom: var(--spacing-md);
    line-height: 1.3;
    letter-spacing: -0.01em;
}

.document-card p,
.blog-post p {
    color: #00cc33;
    line-height: 1.8;
    font-family: 'Fira Code', monospace;
    margin-bottom: var(--spacing-lg);
    flex-grow: 1;
    font-weight: 300;
    opacity: 0.9;
}

/* Blog meta with subtle styling */
.blog-meta {
    font-size: 0.9rem;
    color: rgba(0, 204, 51, 0.6);
    font-family: 'Fira Code', monospace;
    margin-bottom: var(--spacing-md);
    font-style: italic;
    font-weight: 300;
}

.post-tags {
    margin: var(--spacing-md) 0 var(--spacing-lg) 0;
    display: flex;
    flex-wrap: wrap;
    gap: var(--spacing-sm);
}

.tag {
    display: inline-block;
    background: transparent;
    color: rgba(0, 204, 51, 0.7);
    padding: 0.4rem 0;
    font-size: 0.85rem;
    font-family: 'Fira Code', monospace;
    font-weight: 400;
    border: none;
    transition: all 0.3s ease;
    position: relative;
}

.tag::before {
    content: '#';
    opacity: 0.5;
    margin-right: 0.2rem;
}

.tag:hover {
    color: #00cc33;
    transform: translateX(4px);
}

/* Clean button styling to match minimal design */
.document-card .btn-base,
.blog-post .btn-base {
    margin-top: var(--spacing-sm);
    align-self: flex-start;
    
    /* Override heavy button styling */
    background: transparent !important;
    border: none !important;
    box-shadow: none !important;
    backdrop-filter: none !important;
    padding: 0.8rem 0 !important;
    min-height: auto !important;
    min-width: auto !important;
    border-radius: 0 !important;
    
    /* Clean typography */
    font-family: 'Fira Code', monospace !important;
    font-size: 0.95rem !important;
    font-weight: 400 !important;
    color: #00ff41 !important;
    text-shadow: none !important;
    text-decoration: none !important;
    
    /* Subtle underline effect */
    position: relative;
    transition: all 0.3s ease !important;
}

.document-card .btn-base::after,
.blog-post .btn-base::after {
    content: '';
    position: absolute;
    bottom: 0.6rem;
    left: 0;
    width: 0;
    height: 1px;
    background: #00ff41;
    transition: width 0.3s ease;
}

.document-card .btn-base:hover,
.blog-post .btn-base:hover {
    background: transparent !important;
    border: none !important;
    box-shadow: none !important;
    transform: translateX(8px) !important;
    color: #00ff41 !important;
    text-shadow: 0 0 10px rgba(0, 255, 65, 0.4) !important;
}

.document-card .btn-base:hover::after,
.blog-post .btn-base:hover::after {
    width: 100%;
}

/* Icon styling for buttons */
.document-card .btn-base::before,
.blog-post .btn-base::before {
    margin-right: 0.6rem !important;
    font-size: 0.9em !important;
    opacity: 0.8;
    transition: all 0.3s ease !important;
}

.document-card .btn-base:hover::before,
.blog-post .btn-base:hover::before {
    opacity: 1;
    transform: translateX(2px) !important;
}

/* Focus states for accessibility */
.document-card .btn-base:focus,
.blog-post .btn-base:focus {
    outline: 2px solid rgba(0, 255, 65, 0.5) !important;
    outline-offset: 4px !important;
    background: transparent !important;
    box-shadow: none !important;
}

.document-card .btn-base:focus-visible,
.blog-post .btn-base:focus-visible {
    outline: 2px solid #00ff41 !important;
    outline-offset: 4px !important;
    transform: translateX(4px) !important;
}

/* Remove ripple effects and other heavy animations */
.document-card .btn-base::after:not(:hover),
.blog-post .btn-base::after:not(:hover) {
    display: none;
}

/* Ensure clean active state */
.document-card .btn-base:active,
.blog-post .btn-base:active {
    transform: translateX(4px) !important;
    background: transparent !important;
    box-shadow: none !important;
}

/* Responsive design with maintained spaciousness */
@media (max-width: 768px) {
    :root {
        --spacing-unit: 1.5rem;
    }
    
    .hero {
        padding: var(--spacing-lg) 0;
    }
    
    .hero h1 {
        font-size: 2.4rem;
    }
    
    .hero p {
        font-size: 1.2rem;
    }
    
    section {
        padding: 0 var(--spacing-xs);
    }
    
    section h2 {
        font-size: 2rem;
        padding-left: var(--spacing-sm);
    }
    
    .section-intro {
        font-size: 1rem;
        margin-left: var(--spacing-sm);
    }
    
    .document-grid,
    .blog-posts {
        grid-template-columns: 1fr;
        gap: var(--spacing-lg);
        padding: 0 var(--spacing-sm);
    }
    
    .document-card,
    .blog-post {
        padding: var(--spacing-md) 0;
        padding-left: var(--spacing-md);
        margin-left: var(--spacing-xs);
    }
}

@media (max-width: 480px) {
    .hero h1 {
        font-size: 2rem;
    }
    
    section h2 {
        font-size: 1.7rem;
    }
    
    .document-card h3,
    .blog-post h3 {
        font-size: 1.3rem;
    }
    
    .document-grid,
    .blog-posts {
        grid-template-columns: 1fr;
        gap: var(--spacing-md);
    }
}
</style>
