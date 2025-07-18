---
layout: home
title: "About DESH - Democratically Elected System Hackers"
description: "Learn about the world's first software-defined political party and our mission to bring domain expertise to governance."
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
            <li><a href="/#blog">Blog</a></li>
            <li><a href="/join/">Join</a></li>
            <li><a href="/#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<main class="container">
    <section class="hero">
        <h1>About DESH</h1>
        <h2>Democratically Elected System Hackers</h2>
        <p>We are the world's first software-defined political party, applying engineering principles to governance and democracy.</p>
    </section>

    <section class="features">
        <div class="feature-card">
            <h3>🎯 Our Mission</h3>
            <p>To replace career politicians with domain experts who actually understand the systems they're governing. We believe India needs aviation experts running aviation policy, not politicians making uninformed decisions.</p>
        </div>

        <div class="feature-card">
            <h3>🔧 Our Approach</h3>
            <p>We apply software engineering principles to politics: version control for policies, peer review for legislation, continuous integration for governance, and transparent, auditable decision-making processes.</p>
        </div>

        <div class="feature-card">
            <h3>👥 Our Team</h3>
            <p>100 founding members who are experts across critical domains - from aviation and software to military and healthcare. Each member brings real-world experience solving complex problems in their field.</p>
        </div>

        <div class="feature-card">
            <h3>🌍 Our Vision</h3>
            <p>A technocratic democracy where decisions are made based on evidence, expertise, and measurable outcomes rather than political rhetoric and electoral calculations.</p>
        </div>
    </section>

    <section class="blog">
        <h2>Why Software-Defined Politics?</h2>
        <div class="blog-intro">
            <p>Traditional politics operates like legacy code - functional but inefficient, opaque, and prone to corruption bugs. We're building Democracy 2.0 with modern engineering practices.</p>
        </div>
        
        <div class="blog-posts">
            <article class="blog-post">
                <h3>🔍 Transparent by Design</h3>
                <p>Every decision, vote, and policy change is tracked immutably. Our governance algorithms are open-source and auditable by anyone. No more black-box politics.</p>
            </article>

            <article class="blog-post">
                <h3>⚡ Rapid Iteration</h3>
                <p>Like software development, we believe in rapid prototyping, testing, and iteration. Pilot programs, A/B testing for policies, and continuous improvement based on real-world data.</p>
            </article>

            <article class="blog-post">
                <h3>🤝 Collaborative Development</h3>
                <p>Politics should be collaborative like open-source projects. Pull requests for policy changes, peer review by domain experts, and community-driven development of solutions.</p>
            </article>
        </div>
    </section>

    <section class="contact">
        <h2>Join the System Hackers</h2>
        <p>Are you a domain expert tired of watching politicians make uninformed decisions in your field?</p>
        <p>We're building a movement of system hackers who want to debug democracy and implement evidence-based governance.</p>
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
            const target = this.getAttribute('href').substring(1);
            if (target) {
                window.location.href = '/#' + target;
            }
        });
    });

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
</script>