---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-hero">
    <div class="projects-hero-bg" aria-hidden="true"></div>
    <h1>Projects &amp; <span class="gradient-text">Work</span></h1>
    <p>A showcase of my technical work across mobile development, multimedia streaming, mapping technologies, and research projects.</p>
</div>

<div class="projects-filter" role="group" aria-label="Filter projects by category">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="featured">Featured</button>
    <button class="filter-btn" data-filter="research">Research</button>
    <button class="filter-btn" data-filter="demos">Demos</button>
    <button class="filter-btn" data-filter="academic">Academic</button>
</div>

<div class="projects-content">
    <section class="featured-projects" data-section="featured">
        <h2><i class="fas fa-star" aria-hidden="true"></i> Featured Projects</h2>
        <div class="featured-grid">
            {% for project in site.data.projects.featured %}
                <div class="featured-project reveal-on-scroll">
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
                                <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer" class="project-link">
                                    <i class="fas fa-external-link-alt" aria-hidden="true"></i>
                                    {{ link.text }}
                                </a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>

    <section class="research-projects" data-section="research">
        <h2><i class="fas fa-flask" aria-hidden="true"></i> Research &amp; Development</h2>
        <div class="projects-grid">
            {% for project in site.data.projects.research %}
                <div class="project-card reveal-on-scroll">
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
                                <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer" class="project-link">
                                    <i class="fas fa-external-link-alt" aria-hidden="true"></i>
                                    {{ link.text }}
                                </a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>

    <section class="demo-projects" data-section="demos">
        <h2><i class="fas fa-code" aria-hidden="true"></i> Demo &amp; Prototype Projects</h2>
        <div class="projects-grid">
            {% for project in site.data.projects.demos %}
                <div class="project-card reveal-on-scroll">
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
                                <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer" class="project-link">
                                    <i class="fas fa-external-link-alt" aria-hidden="true"></i>
                                    {{ link.text }}
                                </a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>

    <section class="academic-projects" data-section="academic">
        <h2><i class="fas fa-graduation-cap" aria-hidden="true"></i> Academic &amp; Research Projects</h2>
        <div class="projects-grid">
            {% for project in site.data.projects.academic %}
                <div class="project-card reveal-on-scroll">
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
                                <a href="{{ link.url }}" target="_blank" rel="noopener noreferrer" class="project-link">
                                    <i class="fas fa-external-link-alt" aria-hidden="true"></i>
                                    {{ link.text }}
                                </a>
                            {% endfor %}
                        </div>
                    {% endif %}
                </div>
            {% endfor %}
        </div>
    </section>
</div>
