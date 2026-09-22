---
layout: default
title: Home
permalink: /
nav: false
nav_order: 1
---

<style>
  .faculty-home {
    --home-accent: var(--global-theme-color);
    --home-border: color-mix(in srgb, var(--global-text-color) 16%, transparent);
    --home-surface: color-mix(in srgb, var(--global-bg-color) 94%, var(--global-text-color));
    --figure-surface: #f7f7f4;
    --figure-border: #d8d8d2;
    --figure-text: #454b52;
    padding-bottom: 2rem;
  }

  .faculty-home section {
    margin-block: clamp(3.5rem, 8vw, 6.5rem);
  }

  .faculty-home h1,
  .faculty-home h2,
  .faculty-home h3,
  .faculty-home p {
    margin-top: 0;
  }

  .faculty-home h1 {
    max-width: 58ch;
    margin-bottom: 0.85rem;
  }

  .faculty-home h2 {
    margin-bottom: 0.85rem;
  }

  .faculty-home h3 {
    margin-bottom: 0.7rem;
  }

  .home-eyebrow {
    margin-bottom: 0.85rem;
    color: var(--home-accent);
  }

  .home-section-intro {
    max-width: 70ch;
    margin-bottom: 1.75rem;
    color: var(--global-text-color-light);
  }

  .home-hero {
    display: grid;
    grid-template-columns: minmax(0, 1.05fr) minmax(340px, 0.95fr);
    gap: clamp(2rem, 4vw, 3.25rem);
    align-items: center;
    margin-top: clamp(5rem, 8vw, 6.5rem) !important;
  }

  .home-hero__identity {
    margin-bottom: 1rem;
  }

  .home-hero__summary {
    max-width: 58ch;
    margin-bottom: 1.6rem !important;
    color: var(--global-text-color-light);
  }

  .home-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.7rem;
  }

  .home-action {
    display: inline-flex;
    min-height: 2.75rem;
    align-items: center;
    justify-content: center;
    padding: 0.65rem 1rem;
    border: 1px solid var(--home-accent);
    border-radius: 0.3rem;
    color: var(--home-accent);
    text-decoration: none;
  }

  .home-action:hover,
  .home-action:focus-visible {
    background: var(--home-accent);
    color: var(--global-bg-color);
    text-decoration: none;
  }

  .home-action--primary {
    background: var(--home-accent);
    color: var(--global-bg-color);
  }

  .home-action[aria-disabled="true"] {
    border-color: var(--home-border);
    color: var(--global-text-color-light);
    cursor: not-allowed;
    opacity: 0.7;
  }

  .research-figure {
    display: flex;
    width: 100%;
    min-height: 16rem;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    border: 1px solid var(--figure-border);
    border-radius: 0.45rem;
    background: var(--figure-surface);
  }

  .research-figure--hero {
    aspect-ratio: 3 / 2;
  }

  .research-figure--card {
    min-height: 12rem;
    aspect-ratio: 4 / 3;
    border-width: 0 0 1px;
    border-radius: 0.45rem 0.45rem 0 0;
  }

  .research-figure img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .research-figure__placeholder {
    max-width: 28rem;
    padding: 2rem;
    color: var(--figure-text);
    text-align: center;
  }

  .research-figure__label {
    display: block;
    margin-bottom: 0.45rem;
  }

  .research-grid,
  .project-grid {
    display: grid;
    gap: 1rem;
  }

  .research-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .project-grid {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }

  .research-card,
  .project-card {
    border: 1px solid var(--home-border);
    border-radius: 0.45rem;
    background: var(--home-surface);
  }

  .research-card {
    padding: clamp(1.25rem, 3vw, 1.75rem);
  }

  .research-card p,
  .project-card p {
    margin-bottom: 0;
    color: var(--global-text-color-light);
  }

  .project-card {
    overflow: hidden;
  }

  .project-card__body {
    padding: 1.25rem;
  }

  .selected-publications .publications {
    margin-top: 1.5rem;
  }

  .selected-publications .bibliography {
    margin-bottom: 0;
  }

  .selected-publications .bibliography > li {
    margin-bottom: 0.75rem;
    padding-bottom: 0.75rem;
    border-bottom: 1px solid var(--home-border);
  }

  .selected-publications .bibliography > li:last-child {
    margin-bottom: 0;
    border-bottom: 0;
  }

  .applied-research {
    display: grid;
    grid-template-columns: minmax(0, 0.8fr) minmax(0, 1.2fr);
    gap: clamp(1.5rem, 5vw, 4rem);
    align-items: start;
    padding: clamp(1.5rem, 4vw, 2.5rem);
    border-block: 1px solid var(--home-border);
  }

  .institution-list {
    display: flex;
    flex-wrap: wrap;
    gap: 0.65rem;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .institution-list li {
    padding: 0.5rem 0.7rem;
    border: 1px solid var(--home-border);
    border-radius: 0.25rem;
  }

  .teaching-preview {
    display: flex;
    gap: 2rem;
    align-items: center;
    justify-content: space-between;
    padding-top: 2rem;
    border-top: 1px solid var(--home-border);
  }

  .teaching-preview h2 {
    margin-bottom: 0;
  }

  @media (max-width: 880px) {
    .home-hero,
    .applied-research {
      grid-template-columns: 1fr;
    }

    .project-grid {
      grid-template-columns: 1fr;
    }

    .project-card {
      display: grid;
      grid-template-columns: minmax(220px, 0.8fr) minmax(0, 1fr);
    }

    .research-figure--card {
      height: 100%;
      border-width: 0 1px 0 0;
      border-radius: 0.45rem 0 0 0.45rem;
    }
  }

  @media (max-width: 620px) {
    .faculty-home section {
      margin-block: 3.5rem;
    }

    .home-hero {
      grid-template-columns: minmax(0, 1fr);
      margin-top: 4.5rem !important;
    }

    .research-grid,
    .project-card {
      grid-template-columns: 1fr;
    }

    .research-figure--card {
      height: auto;
      border-width: 0 0 1px;
      border-radius: 0.45rem 0.45rem 0 0;
    }

    .teaching-preview {
      align-items: flex-start;
      flex-direction: column;
    }
  }
</style>

<div class="faculty-home">
  <section class="home-hero" aria-labelledby="home-title">
    <div>
      <p class="home-hero__identity">Yang Li, PhD</p>
      <h1 id="home-title">Geospatial methods for net-zero and low-carbon urban transitions</h1>
      <p class="home-hero__summary">
        I develop geospatial, urban building energy, and life-cycle assessment methods to understand and accelerate transitions toward net-zero and
        low-carbon cities.
      </p>
      <nav class="home-actions" aria-label="Homepage actions">
        <a class="home-action home-action--primary" href="{{ '/research/' | relative_url }}">Explore Research</a>
        <a class="home-action" href="{{ '/projects/' | relative_url }}">Selected Projects</a>
        {% if site.data.socials.cv_pdf %}
          <a class="home-action" href="{{ site.data.socials.cv_pdf | relative_url }}" target="_blank" rel="noopener noreferrer">Download CV</a>
        {% else %}
          <!-- TODO: Enable this link after a verified CV PDF is configured in _data/socials.yml. -->
          <span class="home-action" aria-disabled="true" title="CV download will be available after the verified PDF is added">Download CV</span>
        {% endif %}
      </nav>
    </div>

    <div class="research-figure research-figure--hero">
      {% assign hero_image_path = '/assets/img/projects/urban-net-zero/richmond-3d-city-model.png' %}
      {% assign hero_image = site.static_files | where: 'path', hero_image_path | first %}
      {% if hero_image %}
        <img
          src="{{ hero_image_path | relative_url }}"
          alt="Three-dimensional city model of Richmond showing the urban building stock and building heights"
          width="1800"
          height="1200"
          loading="eager"
          decoding="async"
        >
      {% else %}
        <div
          class="research-figure__placeholder"
          role="img"
          aria-label="Reserved space for a three-dimensional city model of Richmond showing the urban building stock and building heights"
        >
          <span class="research-figure__label">Research figure forthcoming</span>
          3D city model of Richmond and its urban building stock
        </div>
      {% endif %}
    </div>
  </section>

  <section aria-labelledby="research-program-title">
    <p class="home-eyebrow">Research program</p>
    <h2 id="research-program-title">From urban data to net-zero pathways</h2>
    <p class="home-section-intro">
      The program connects geospatial urban data and 2D/3D city models with urban building energy modelling, intervention scenarios, spatial life-cycle
      assessment, and municipal and policy decision support.
    </p>

    <div class="research-grid">
      <article class="research-card">
        <h3>Urban Building Energy &amp; Net-Zero Transitions</h3>
        <p>UBEM, building archetypes, retrofit, electrification, renewable energy, and district energy.</p>
      </article>
      <article class="research-card">
        <h3>Geospatial &amp; Data-Driven Urban Modelling</h3>
        <p>GIS, remote sensing, LiDAR, 2D/3D city models, open data, and GeoAI/data-driven methods.</p>
      </article>
      <article class="research-card">
        <h3>Life-Cycle Carbon &amp; Environmental Assessment</h3>
        <p>Spatial LCA, dynamic LCA, BIM-LCA, and operational and embodied impacts.</p>
      </article>
      <article class="research-card">
        <h3>Climate-Responsive Urban Technologies</h3>
        <p>Green and cool roofs, solar technologies, urban greening, microclimate, and passive strategies.</p>
      </article>
    </div>
  </section>

  <section aria-labelledby="featured-research-title">
    <p class="home-eyebrow">Featured research</p>
    <h2 id="featured-research-title">Urban-scale methods and applications</h2>
    <div class="project-grid">
      <article class="project-card">
        <div class="research-figure research-figure--card">
          {% assign pathways_image_path = '/assets/img/projects/urban-net-zero/richmond-energy-pathways.png' %}
          {% assign pathways_image = site.static_files | where: 'path', pathways_image_path | first %}
          {% if pathways_image %}
            <img
              src="{{ pathways_image_path | relative_url }}"
              alt="Urban energy pathway maps for Richmond comparing energy-efficiency retrofit, electrification, and renewable-energy scenarios"
              width="1600"
              height="1200"
              loading="lazy"
              decoding="async"
            >
          {% else %}
            <div
              class="research-figure__placeholder"
              role="img"
              aria-label="Reserved space for urban energy pathway maps comparing energy-efficiency retrofit, electrification, and renewable-energy scenarios"
            >
              <span class="research-figure__label">Research figure forthcoming</span>
              Richmond energy pathways
            </div>
          {% endif %}
        </div>
        <div class="project-card__body">
          <!-- TODO: Link this card after the verified project page is created. -->
          <h3>Pathways to Urban Net-Zero Energy Buildings</h3>
          <p>GIS-based urban building modelling to evaluate electrification, energy-efficiency retrofit, and renewable-energy pathways.</p>
        </div>
      </article>

      <article class="project-card">
        <div class="research-figure research-figure--card">
          {% assign spatial_lca_image_path = '/assets/img/projects/spatial-lca/spatial-lca-net-zero.png' %}
          {% assign spatial_lca_image = site.static_files | where: 'path', spatial_lca_image_path | first %}
          {% if spatial_lca_image %}
            <img
              src="{{ spatial_lca_image_path | relative_url }}"
              alt="Spatial map and chart showing urban net-zero potential and whole-life environmental impacts from the GIS–BIM–LCA framework"
              width="1600"
              height="1200"
              loading="lazy"
              decoding="async"
            >
          {% else %}
            <div
              class="research-figure__placeholder"
              role="img"
              aria-label="Reserved space for spatial urban net-zero potential and whole-life environmental impact results from the GIS–BIM–LCA framework"
            >
              <span class="research-figure__label">Research figure forthcoming</span>
              Spatial GIS–BIM–LCA results
            </div>
          {% endif %}
        </div>
        <div class="project-card__body">
          <!-- TODO: Link this card after the verified project page is created. -->
          <h3>Spatial GIS–BIM–LCA for Urban Net Zero</h3>
          <p>Integrating GIS, BIM, urban energy modelling, and life-cycle assessment to spatially evaluate whole-life environmental impacts.</p>
        </div>
      </article>

      <article class="project-card">
        <div class="research-figure research-figure--card">
          {% assign richmond_image_path = '/assets/img/projects/richmond-ubem/richmond-3d-model.png' %}
          {% assign richmond_image = site.static_files | where: 'path', richmond_image_path | first %}
          {% if richmond_image %}
            <img
              src="{{ richmond_image_path | relative_url }}"
              alt="Three-dimensional GIS building model of Richmond used for city-scale building energy assessment"
              width="1800"
              height="1200"
              loading="lazy"
              decoding="async"
            >
          {% else %}
            <div
              class="research-figure__placeholder"
              role="img"
              aria-label="Reserved space for a three-dimensional GIS building model of Richmond used for city-scale building energy assessment"
            >
              <span class="research-figure__label">Research figure forthcoming</span>
              Richmond urban building model
            </div>
          {% endif %}
        </div>
        <div class="project-card__body">
          <!-- TODO: Link this card after the verified project page is created. -->
          <h3>Richmond Urban Building Energy Assessment</h3>
          <p>Applied municipal research using GIS, LiDAR, building archetypes, and urban energy assessment to support city-scale decision-making.</p>
        </div>
      </article>
    </div>
  </section>

  <section class="selected-publications" aria-labelledby="selected-publications-title">
    <p class="home-eyebrow">Research outputs</p>
    <h2 id="selected-publications-title">Selected Publications</h2>
    {% include selected_papers.liquid %}
  </section>

  <section class="applied-research" aria-labelledby="applied-research-title">
    <div>
      <p class="home-eyebrow">Applied research &amp; collaboration</p>
      <h2 id="applied-research-title">Connecting research with public-sector decisions</h2>
      <p class="home-section-intro">
        Research experience across municipal, federal, and international research settings informs an applied approach to urban energy and environmental
        decision support.
      </p>
    </div>
    <ul class="institution-list" aria-label="Institutions connected with Yang Li's research experience">
      <li>National Research Council Canada</li>
      <li>City of Richmond</li>
      <li>City of New Westminster</li>
      <li>City of Kingston</li>
      <li>Lawrence Berkeley National Laboratory</li>
      <li>École Centrale de Lille</li>
      <li>KU Leuven</li>
    </ul>
  </section>

  <section class="teaching-preview" aria-labelledby="teaching-preview-title">
    <div>
      <p class="home-eyebrow">Teaching</p>
      <h2 id="teaching-preview-title">Teaching</h2>
      <!-- TODO: Add a verified teaching summary when supporting material is supplied. -->
    </div>
    <a class="home-action" href="{{ '/teaching/' | relative_url }}">View Teaching</a>
  </section>
</div>
