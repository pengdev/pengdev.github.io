---
layout: default
title: About Me
permalink: /aboutme/
---

<div class="about-hero">
    <div class="avatar-section">
        <div class="avatar">
            <img src="/assets/img/avatar.jpg" alt="Liu Peng - Senior Software Engineer" loading="eager" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';">
            <div class="avatar-fallback" style="display: none;">LP</div>
        </div>
        <h1>Liu Peng</h1>
        <p class="title">Senior Software Engineer</p>
        <p class="subtitle">Mobile Development • Embedded Systems • Full-Stack Development</p>
    </div>
</div>

<div class="about-content">
    <section class="about-section">
        <h2>About Me</h2>
        <p>Hi, I'm <strong>Liu Peng</strong>, a senior software engineer with over 10 years of experience in mobile development, embedded systems, and full-stack applications. I specialize in creating innovative solutions that bridge hardware and software, with expertise in Android development, SDK development, multimedia streaming, and mapping technologies.</p>
        
        <p>Throughout my career, I've worked on diverse projects from consumer mobile apps to enterprise IoT solutions. I have a strong focus on quality and performance, believing in writing clean, maintainable code and creating exceptional user experiences. When I'm not coding, I enjoy contributing to open source projects and sharing knowledge with the developer community.</p>
    </section>

    <section class="experience-section">
        <h2>Professional Experience</h2>
        {% assign exp = site.data.experience %}
        {% for experience in exp limit:3 %}
            {% if forloop.first %}
                {% include experience-item.html title=experience.title company=experience.company items=experience.items class="current" %}
            {% else %}
                {% include experience-item.html title=experience.title company=experience.company items=experience.items %}
            {% endif %}
        {% endfor %}
        <div id="more-experience" style="display:none;">
        {% for experience in exp offset:3 %}
            {% include experience-item.html title=experience.title company=experience.company items=experience.items %}
        {% endfor %}
        </div>
        {% if exp.size > 3 %}
        <button id="toggle-experience" class="btn btn-secondary" type="button" style="margin-top:1rem;">
            Show all experience
        </button>
        <script>
        document.addEventListener('DOMContentLoaded', function() {
            var btn = document.getElementById('toggle-experience');
            var more = document.getElementById('more-experience');
            var expanded = false;
            btn.addEventListener('click', function() {
                expanded = !expanded;
                more.style.display = expanded ? 'block' : 'none';
                btn.textContent = expanded ? 'Show less' : 'Show all experience';
            });
        });
        </script>
        {% endif %}
    </section>

    <section class="skills-section">
        <h2>Technical Skills & Expertise</h2>
        <div class="skills-grid">
            {% for skill_category in site.data.skills %}
                {% include skill-category.html category=skill_category.category skills=skill_category.skills %}
            {% endfor %}
        </div>
    </section>

    <section class="education-section">
        <h2>Education & Certifications</h2>
        <div class="about-card-grid">
        <div class="education-item">
            <h3>Master of Science in Communications Engineering - Networking Technology</h3>
            <p class="institution">Aalto University • 2011 - 2015 • Grade: 4.04/5 • Completed with Distinction</p>
            <p>Thesis: "Developing a Solution for Multimedia Home Networking" - Focused on DLNA architecture, Digital Media Server solutions, and developing universal Android solution for multimedia home networking. Completed while working full-time at Tuxera. <a href="https://www.liupeng.eu/home-networking/" target="_blank">View Thesis</a></p>
            <p><strong>Activities:</strong> Product Development Project (PDP), CSSA-Espoo (Chinese Students and Scholars Association), Aalto University Mentoring Program</p>
        </div>
        
        <div class="education-item">
            <h3>Bachelor of Engineering in Electronic and Information Engineering</h3>
            <p class="institution">Xiangtan University • 2007 - 2011 • Grade: 3.51/4</p>
            <p>Foundation in electronic engineering, information systems, and telecommunications with focus on software development and hardware integration.</p>
            <p><strong>Achievements:</strong> First-class scholarship (twice), Third-class scholarship, Winner of 2011 national NI virtual instrument contest</p>
            <p><strong>Activities:</strong> 2011 national NI virtual instrument contest, Volunteer for computer maintenance and repairing, Website Design Competition</p>
        </div>
        </div>
    </section>

    <section class="awards-section">
        <h2>Honors & Awards</h2>
        <div class="about-card-grid">
        {% for award in site.data.awards %}
            {% include award-item.html title=award.title issuer=award.issuer description=award.description %}
        {% endfor %}
        </div>
    </section>

    <section class="interests-section">
        <h2>Interests & Activities</h2>
        <p>Beyond software development, I'm passionate about:</p>
        <ul>
            <li><strong>Open Source Contribution</strong> - Active contributor to various open source projects, particularly in the mobile and IoT domains</li>
            <li><strong>Table Tennis</strong> - Playing competitively in Finland SPTL division games</li>
            <li><strong>Photography</strong> - Capturing moments and exploring creative expression through digital art</li>
            <li><strong>Continuous Learning</strong> - Regularly attending conferences, workshops, and online courses to stay current with technology trends</li>
            <li><strong>Mentoring</strong> - Helping junior developers grow their skills and navigate their careers in tech</li>
        </ul>
    </section>
</div>
