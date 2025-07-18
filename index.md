---
layout: home
title: "Join #desh>_ - Democratically Elected System Hackers"
description: "World's first software-defined political party. Building transparent, algorithmic governance with domain experts for India's future."
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
            <li><a href="#blog">Blog</a></li>
            <li><a href="/join/">Join</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<main class="container">
    <section class="hero">
        <h1>Democratically Elected System Hackers</h1>
        <h2>World's First Software-Defined Political Party</h2>
        <p>Building transparent, algorithmic governance with domain experts who understand how to actually run a modern nation-state.</p>
        <a href="/join/" class="cta-button">Join the Movement</a>
    </section>

    <section class="features" id="about">
        <div class="feature-card">
            <h3>🔬 Domain Expertise</h3>
            <p>Our founding team consists of 100 experts across critical domains - from aviation and software to military and healthcare. We believe in technocratic leadership over traditional politics.</p>
        </div>

        <div class="feature-card">
            <h3>🔍 Transparent Governance</h3>
            <p>Every decision, vote, and policy change is tracked immutably. Our governance algorithms are open-source and auditable by anyone.</p>
        </div>

        <div class="feature-card">
            <h3>🤖 Algorithmic Selection</h3>
            <p>We use AI-powered analysis to identify and recruit the best domain experts, ensuring our team has the skills needed to solve real problems.</p>
        </div>

        <div class="feature-card">
            <h3>🌐 Open Source Politics</h3>
            <p>Like open-source software, our political platform is collaborative, iterative, and merit-based rather than personality-driven.</p>
        </div>
    </section>

    <section class="blog" id="blog">
        <h2>Decoding Democracy</h2>
        <p class="blog-intro">Exploring the intersection of technology, governance, and democratic innovation through the lens of system hackers.</p>
        
        <div class="blog-posts">
            {% for post in site.posts limit:3 %}
            <article class="blog-post">
                <h3>{{ post.title }}</h3>
                <div class="blog-meta">{{ post.meta | default: "$ cat /dev/democracy | grep insights" }}</div>
                <p>{{ post.description | default: post.excerpt | strip_html | truncate: 200 }}</p>
                <a href="{{ post.url }}" class="read-more">Read More</a>
            </article>
            {% endfor %}
        </div>
        
        {% if site.posts.size > 3 %}
        <div class="blog-archive">
            <a href="/blog/" class="archive-link">View All Posts</a>
        </div>
        {% endif %}
    </section>

    <section class="contact" id="contact">
        <h2>Ready to Build the Future?</h2>
        <p>We're looking for domain experts who want to move beyond traditional politics and actually solve India's challenges.</p>
        <p>If you're an expert in aviation, software, military, healthcare, finance, or any critical domain, we want to hear from you.</p>
        <a href="mailto:help.me@joindesh.in" class="email-link">help.me @ joindesh.in</a>
    </section>
</main>

<footer class="container">
    <p>&copy; 2025 #desh>_. Building India's future through software-defined governance.</p>
</footer>

<script>
    // Smooth scrolling for navigation links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({
                behavior: 'smooth'
            });

            // Close mobile menu after clicking a link
            const navLinks = document.getElementById('nav-links');
            navLinks.classList.remove('active');
        });
    });

    // Mobile menu toggle functionality
    const mobileMenuToggle = document.getElementById('mobile-menu-toggle');
    const navLinks = document.getElementById('nav-links');

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
</script>