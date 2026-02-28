---
layout: default
title: About Me
permalink: /aboutme/
---

<div class="about-hero">
    <div class="about-hero-bg" aria-hidden="true"></div>
    <div class="avatar-section">
        <div class="avatar-ring-wrap">
            <div class="avatar">
                <img src="/assets/img/avatar.jpg" alt="Liu Peng - Senior Software Engineer" loading="eager" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
                <div class="avatar-fallback" style="display: none;">LP</div>
            </div>
        </div>
        <h1>Liu Peng</h1>
        <span class="role-badge">
            <i class="fas fa-map-marker-alt" aria-hidden="true"></i>
            Senior Software Engineer @ Mapbox
        </span>
        <p class="subtitle">Mobile Development &bull; Embedded Systems &bull; Full-Stack</p>
    </div>
</div>

<div class="about-content">
    <section class="about-section reveal-on-scroll">
        <h2>About Me</h2>
        <p>Hi, I'm <strong>Liu Peng</strong>, a senior software engineer with over 10 years of experience in mobile development, embedded systems, and full-stack applications. I specialize in creating innovative solutions that bridge hardware and software, with expertise in Android development, SDK development, multimedia streaming, and mapping technologies.</p>
        <p>Throughout my career, I've worked on diverse projects from consumer mobile apps to enterprise IoT solutions. I have a strong focus on quality and performance, believing in writing clean, maintainable code and creating exceptional user experiences. When I'm not coding, I enjoy contributing to open source projects and sharing knowledge with the developer community.</p>
    </section>

    <section class="experience-section">
        <h2>Professional Experience</h2>
        <div class="timeline-list">
        {% assign exp = site.data.experience %}
        {% for experience in exp limit:3 %}
            {% if forloop.first %}
                {% include experience-item.html title=experience.title company=experience.company items=experience.items class="current" %}
            {% else %}
                {% include experience-item.html title=experience.title company=experience.company items=experience.items %}
            {% endif %}
        {% endfor %}
        </div>
        <div id="more-experience" style="display:none;">
        <div class="timeline-list">
        {% for experience in exp offset:3 %}
            {% include experience-item.html title=experience.title company=experience.company items=experience.items %}
        {% endfor %}
        </div>
        </div>
        {% if exp.size > 3 %}
        <button id="toggle-experience" type="button">
            Show all experience
        </button>
        {% endif %}
    </section>

    <section class="skills-section">
        <h2>Technical Skills &amp; Expertise</h2>
        <div class="skills-grid">
            {% for skill_category in site.data.skills %}
                {% include skill-category.html category=skill_category.category skills=skill_category.skills %}
            {% endfor %}
        </div>
    </section>

    <section class="education-section">
        <h2>Education</h2>
        <div class="about-card-grid">
        <div class="education-item reveal-on-scroll">
            <h3>Master of Science in Communications Engineering</h3>
            <p class="institution">Aalto University &bull; 2011–2015 &bull; Grade: 4.04/5 &bull; Completed with Distinction</p>
            <p>Thesis: "Developing a Solution for Multimedia Home Networking" — Focused on DLNA architecture, Digital Media Server solutions, and developing a universal Android solution for multimedia home networking. Completed while working full-time at Tuxera. <a href="https://www.liupeng.eu/home-networking/" target="_blank" rel="noopener noreferrer">View Thesis</a></p>
            <p><strong>Activities:</strong> Product Development Project (PDP), CSSA-Espoo, Aalto University Mentoring Program</p>
        </div>
        <div class="education-item reveal-on-scroll">
            <h3>Bachelor of Engineering in Electronic and Information Engineering</h3>
            <p class="institution">Xiangtan University &bull; 2007–2011 &bull; Grade: 3.51/4</p>
            <p>Foundation in electronic engineering, information systems, and telecommunications with focus on software development and hardware integration.</p>
            <p><strong>Achievements:</strong> First-class scholarship (twice), Third-class scholarship, Winner of 2011 national NI virtual instrument contest</p>
        </div>
        </div>
    </section>

    <section class="awards-section">
        <h2>Honors &amp; Awards</h2>
        <div class="awards-grid">
        {% for award in site.data.awards %}
            {% include award-item.html title=award.title issuer=award.issuer description=award.description %}
        {% endfor %}
        </div>
    </section>

    <section class="interests-section">
        <h2>Interests &amp; Activities</h2>
        <div class="interests-grid">
        {% for interest in site.data.interests %}
            {% include interest-card.html icon=interest.icon title=interest.title description=interest.description %}
        {% endfor %}
        </div>
    </section>

    <section class="contact-cta reveal-on-scroll">
        <div class="contact-cta-inner glass-card">
            <h2>Let's Work Together</h2>
            <p>Open to interesting opportunities, collaborations, and conversations.</p>
            <a href="mailto:{{ site.social-network-links.email }}" class="btn btn-primary btn-glow">
                <i class="fas fa-envelope" aria-hidden="true"></i>
                Get in Touch
            </a>
        </div>
    </section>
</div>
