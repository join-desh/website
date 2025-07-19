---
layout: home
title: "Join DESH - Become a System Hacker"
description: "Join the world's first software-defined political party. We're looking for 100 domain experts to form our founding team."
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
            <li><a href="/primitives/">Primitives</a></li>
            <li><a href="/#blog">Blog</a></li>
            <li><a href="/join/" class="active">Join</a></li>
            <li><a href="/#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<main class="container">
    <section class="hero">
        <h1>Join the Movement</h1>
        <h2>Become a System Hacker</h2>
        <p>We're recruiting 100 domain experts to form the founding team of India's first software-defined political party.</p>
    </section>

    <section class="features">
        <div class="feature-card">
            <h3>🎯 Who We're Looking For</h3>
            <p><strong>Domain Experts</strong> with 10+ years of hands-on experience in critical fields: aviation, software, military, healthcare, finance, infrastructure, education, agriculture, and more.</p>
        </div>

        <div class="feature-card">
            <h3>📋 Requirements</h3>
            <p><strong>Proven Track Record:</strong> You've solved real problems in your domain<br>
            <strong>Evidence-Based Thinking:</strong> You make decisions based on data and research<br>
            <strong>Transparency Commitment:</strong> You're willing to work in the open</p>
        </div>

        <div class="feature-card">
            <h3>🔍 Selection Process</h3>
            <p><strong>1.</strong> Submit expertise portfolio<br>
            <strong>2.</strong> Peer review by existing domain experts<br>
            <strong>3.</strong> Technical interview and problem-solving assessment<br>
            <strong>4.</strong> Background verification and ethics screening</p>
        </div>

        <div class="feature-card">
            <h3>🚀 What You'll Do</h3>
            <p><strong>Policy Development:</strong> Create evidence-based policies in your domain<br>
            <strong>System Design:</strong> Architect transparent governance processes<br>
            <strong>Peer Review:</strong> Evaluate proposals from other domain experts</p>
        </div>
    </section>

    <section class="blog">
        <h2>Critical Domains We Need</h2>
        <div class="blog-intro">
            <p>India needs experts who understand how to actually run the systems that keep a modern nation-state functioning.</p>
        </div>
        
        <div class="blog-posts">
            <article class="blog-post">
                <h3>🛩️ Infrastructure & Transportation</h3>
                <div class="blog-meta">$ systemctl status infrastructure</div>
                <p><strong>Aviation:</strong> Pilots, ATC, Safety Engineers<br>
                <strong>Railways:</strong> Operations Managers, Engineers<br>
                <strong>Highways:</strong> Traffic Engineers, Urban Planners<br>
                <strong>Ports:</strong> Logistics Experts, Maritime Engineers</p>
            </article>

            <article class="blog-post">
                <h3>💻 Technology & Security</h3>
                <div class="blog-meta">$ ps aux | grep critical_systems</div>
                <p><strong>Software:</strong> System Architects, DevOps Engineers<br>
                <strong>Cybersecurity:</strong> Security Researchers, Incident Response<br>
                <strong>Telecommunications:</strong> Network Engineers, 5G Specialists<br>
                <strong>AI/ML:</strong> Machine Learning Engineers, Data Scientists</p>
            </article>

            <article class="blog-post">
                <h3>🏥 Social Systems</h3>
                <div class="blog-meta">$ service social_systems status</div>
                <p><strong>Healthcare:</strong> Public Health Specialists, Medical Administrators<br>
                <strong>Education:</strong> Curriculum Designers, EdTech Experts<br>
                <strong>Finance:</strong> Economists, Financial Engineers<br>
                <strong>Agriculture:</strong> Agricultural Scientists, Supply Chain Experts</p>
            </article>
        </div>
    </section>

    <section class="contact">
        <h2>Ready to Debug Democracy?</h2>
        <p>If you're a domain expert who's tired of watching politicians make uninformed decisions in your field, we want to hear from you.</p>
        <p>Send us your expertise portfolio and let's build a government that actually works.</p>
        <a href="mailto:help.me@joindesh.in" class="email-link">help.me @ joindesh.in</a>
        
        <div style="margin-top: 3rem; padding: 2rem; border: 1px solid #00cc33; border-radius: 8px; background: rgba(0, 20, 0, 0.5);">
            <h3 style="color: #00ff41; margin-bottom: 1rem; font-size: 1.2rem;">Application Template</h3>
            <div style="color: #00cc33; font-family: 'Fira Code', monospace; font-size: 0.9rem; line-height: 1.6;">
                <p><strong>Subject:</strong> Domain Expert Application - [Your Field]</p>
                <p><strong>Include:</strong></p>
                <p>• Your domain of expertise and years of experience</p>
                <p>• 3-5 real problems you've solved in your field</p>
                <p>• Publications, patents, or notable achievements</p>
                <p>• Why you believe in evidence-based governance</p>
                <p>• Your vision for improving your domain in India</p>
            </div>
        </div>
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