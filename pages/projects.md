---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-hero">
    <h1>Projects & Work</h1>
    <p>A showcase of my technical work across mobile development, multimedia streaming, mapping technologies, and research projects.</p>
</div>

<div class="projects-content">
    <section class="featured-projects">
        <h2>Featured Projects</h2>
        <div class="featured-grid">
            {% for project in site.data.projects.featured %}
                <div class="featured-project">
                    <div class="project-header">
                        <h3>{{ project.title }}</h3>
                        {% if project.badge %}
                            <span class="project-badge {{ project.badge_type }}">{{ project.badge }}</span>
                        {% endif %}
                    </div>
                    <p class="project-tech">{{ project.tech }}</p>
                    <p class="project-description">{{ project.description }}</p>
                    {% if project.links %}
                        <div class="project-links">
                            {% for link in project.links %}
                                <a href="{{ link.url }}" target="_blank" class="project-link">{{ link.text }}</a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>

    <section class="research-projects">
        <h2>Research & Development</h2>
        <div class="projects-grid">
            {% for project in site.data.projects.research %}
                <div class="project-card">
                    <div class="project-header">
                        <h3>{{ project.title }}</h3>
                        {% if project.badge %}
                            <span class="project-badge {{ project.badge_type }}">{{ project.badge }}</span>
                        {% endif %}
                    </div>
                    <p class="project-tech">{{ project.tech }}</p>
                    <p class="project-description">{{ project.description }}</p>
                    {% if project.links %}
                        <div class="project-links">
                            {% for link in project.links %}
                                <a href="{{ link.url }}" target="_blank" class="project-link">{{ link.text }}</a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>

    <section class="demo-projects">
        <h2>Demo & Prototype Projects</h2>
        <div class="projects-grid">
            {% for project in site.data.projects.demos %}
                <div class="project-card">
                    <div class="project-header">
                        <h3>{{ project.title }}</h3>
                        {% if project.badge %}
                            <span class="project-badge {{ project.badge_type }}">{{ project.badge }}</span>
                        {% endif %}
                    </div>
                    <p class="project-tech">{{ project.tech }}</p>
                    <p class="project-description">{{ project.description }}</p>
                    {% if project.links %}
                        <div class="project-links">
                            {% for link in project.links %}
                                <a href="{{ link.url }}" target="_blank" class="project-link">{{ link.text }}</a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>

    <section class="academic-projects">
        <h2>Academic & Research Projects</h2>
        <div class="projects-grid">
            {% for project in site.data.projects.academic %}
                <div class="project-card">
                    <div class="project-header">
                        <h3>{{ project.title }}</h3>
                        {% if project.badge %}
                            <span class="project-badge {{ project.badge_type }}">{{ project.badge }}</span>
                        {% endif %}
                    </div>
                    <p class="project-tech">{{ project.tech }}</p>
                    <p class="project-description">{{ project.description }}</p>
                    {% if project.links %}
                        <div class="project-links">
                            {% for link in project.links %}
                                <a href="{{ link.url }}" target="_blank" class="project-link">{{ link.text }}</a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>
</div> 