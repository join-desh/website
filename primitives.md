---
layout: default
title: "Democracy Primitives"
description: "Exploring the fundamental building blocks of modern democratic systems"
permalink: /primitives/
---

<header>
    <nav class="container">
        <a href="/" class="brand">
            <div class="logo">desh</div>
            <div class="tagline-header">Not left. Not right. Forward.</div>
        </a>
        <button class="mobile-menu-toggle" id="mobile-menu-toggle">Menu</button>
        <ul class="nav-links" id="nav-links">
            <li><a href="/about/">About</a></li>
            <li><a href="/vision/">Vision</a></li>
            <li><a href="/primitives/" class="active">Primitives</a></li>
            <li><a href="/#blog">Blog</a></li>
            <li><a href="/join/">Join</a></li>
            <li><a href="/#contact">Contact</a></li>
        </ul>
    </nav>
</header>

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

<footer class="container">
    <p>&copy; 2025 #desh>_. Building India's future through software-defined governance.</p>
</footer>

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
<script
>
    // Mobile menu toggle functionality
    const mobileMenuToggle = document.getElementById('mobile-menu-toggle');
    const navLinks = document.getElementById('nav-links');

    if (mobileMenuToggle && navLinks) {
        mobileMenuToggle.addEventListener('click', function () {
            navLinks.classList.toggle('active');

            // Update button text
            if (navLinks.classList.contains('active')) {
                this.textContent = 'Close';
            } else {
                this.textContent = 'Menu';
            }
        });

        // Close mobile menu when clicking outside
        document.addEventListener('click', function (e) {
            if (!e.target.closest('nav') && navLinks.classList.contains('active')) {
                navLinks.classList.remove('active');
                mobileMenuToggle.textContent = 'Menu';
            }
        });
    }

    // Smooth scrolling for anchor links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = this.getAttribute('href').substring(1);
            if (target) {
                window.location.href = '/#' + target;
            }
        });
    });
</script>