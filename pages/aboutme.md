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
        <p>Hi, I'm <strong>Liu Peng</strong>, a passionate software engineer with over 10 years of experience in developing innovative solutions across mobile, embedded, and web technologies. I specialize in creating user-centric applications that bridge the gap between hardware and software.</p>
        
        <p>Throughout my career, I've worked on diverse projects ranging from consumer mobile applications to enterprise IoT solutions. I believe in writing clean, maintainable code and creating solutions that not only work efficiently but also provide exceptional user experiences.</p>
        
        <p>I'm constantly learning and staying up-to-date with the latest technologies and best practices in software development. When I'm not coding, I enjoy contributing to open source projects, exploring new technologies, and sharing knowledge with the developer community.</p>
    </section>

    <section class="experience-section">
        <h2>Professional Experience</h2>
        
        {% for experience in site.data.experience %}
            {% include experience-item.html title=experience.title company=experience.company items=experience.items %}
        {% endfor %}
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
    </section>

    <section class="awards-section">
        <h2>Honors & Awards</h2>
        
        {% for award in site.data.awards %}
            {% include award-item.html title=award.title issuer=award.issuer description=award.description %}
        {% endfor %}
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
