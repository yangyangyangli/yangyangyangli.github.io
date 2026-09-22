---
layout: page
title: Projects
permalink: /projects/
description: Research projects in urban energy, geospatial modelling, and life-cycle assessment.
nav: true
nav_order: 3
---

<div class="projects-landing">
  <p class="projects-landing__intro">
    Research spanning urban building energy modelling, geospatial analysis, life-cycle assessment, and applied municipal decision support.
  </p>

  <section class="project-section" aria-labelledby="flagship-projects-title">
    <p class="section-eyebrow">Peer-reviewed research</p>
    <h2 id="flagship-projects-title">Flagship Research</h2>
    <div class="project-index-grid">
      {% assign flagship_projects = site.projects | where: 'category', 'flagship-research' | sort: 'importance' %}
      {% for project in flagship_projects %}
        <article class="project-index-card">
          <a class="project-index-card__figure" href="{{ project.url | relative_url }}" aria-label="Open {{ project.title }} project page">
            <img src="{{ project.img | prepend: '/' | relative_url }}" alt="{{ project.image_alt }}" loading="lazy" decoding="async">
          </a>
          <div class="project-index-card__body">
            <p class="project-meta">{{ project.year }} · {{ project.project_type }}</p>
            <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
            <p>{{ project.description }}</p>
            <div class="project-actions">
              <a class="project-link" href="{{ project.url | relative_url }}">Project Page</a>
              <a class="project-link" href="https://doi.org/{{ project.publication_doi }}" target="_blank" rel="noopener noreferrer">Publication</a>
            </div>
          </div>
        </article>
      {% endfor %}
    </div>
  </section>

  <section class="project-section" aria-labelledby="applied-projects-title">
    <p class="section-eyebrow">Decision support</p>
    <h2 id="applied-projects-title">Applied Municipal / Federal Research</h2>
    <div class="project-index-grid">
      {% assign applied_projects = site.projects | where: 'category', 'applied-research' | sort: 'importance' %}
      {% for project in applied_projects %}
        <article class="project-index-card">
          <a class="project-index-card__figure" href="{{ project.url | relative_url }}" aria-label="Open {{ project.title }} project page">
            {% if project.external_image %}
              <img src="{{ project.external_image }}" alt="{{ project.image_alt }}" loading="lazy" decoding="async">
            {% elsif project.img %}
              <img src="{{ project.img | prepend: '/' | relative_url }}" alt="{{ project.image_alt }}" loading="lazy" decoding="async">
            {% else %}
              <span class="project-index-card__placeholder" role="img" aria-label="No approved research figure is currently available for this project">
                Approved research figure forthcoming
              </span>
            {% endif %}
          </a>
          <div class="project-index-card__body">
            <p class="project-meta">{{ project.year }} · {{ project.project_type }}</p>
            <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
            <p>{{ project.description }}</p>
            <div class="project-actions">
              <a class="project-link" href="{{ project.url | relative_url }}">Project Page</a>
              <a class="project-link" href="{{ project.report_url }}" target="_blank" rel="noopener noreferrer">UBC Report</a>
            </div>
          </div>
        </article>
      {% endfor %}
    </div>

    <ul class="supporting-project-list" aria-label="Additional applied research projects">
      <li>
        <strong>NRC Building LCA Benchmarking</strong>
        <span>Federal applied research</span>
        <!-- TODO: Add methods, results, links, and a detailed page only after NRC source material is supplied. -->
      </li>
      <li>
        <strong>Kingston GIS-Social Mapping / HART Tool project</strong>
        <span>Municipal applied research</span>
        <!-- TODO: Add verified project dates, role, methods, outputs, and official links. -->
      </li>
      <li>
        <strong>MATT Concrete “Straight Up” EPD project</strong>
        <span>Applied life-cycle assessment</span>
        <!-- TODO: Add verified project dates, role, methods, outputs, and official links. -->
      </li>
    </ul>
  </section>

  <section class="project-section" aria-labelledby="supporting-projects-title">
    <p class="section-eyebrow">Research foundations</p>
    <h2 id="supporting-projects-title">Supporting / Earlier Research</h2>
    <ul class="supporting-project-list">
      <li>
        <strong>Spatially Resolved Pea and Lentil LCA</strong>
        <span>Spatial life-cycle assessment and emissions modelling · 2022</span>
        <!-- TODO: Add a detailed page after verified project materials and links are supplied. -->
      </li>
    </ul>
  </section>
</div>
