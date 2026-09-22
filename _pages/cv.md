---
layout: default
permalink: /cv/
title: CV
nav: true
nav_order: 8
description: Curriculum vitae of Yang Li.
---

<style>
  .cv-page {
    padding-block: clamp(2.5rem, 6vw, 4.5rem);
  }

  .cv-page__header {
    max-width: 48rem;
    margin-bottom: 2rem;
  }

  .cv-page__header h1 {
    margin-bottom: 1rem;
  }

  .cv-page__header p {
    color: var(--global-text-color-light);
  }

  .cv-page__actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    margin-bottom: 2.5rem;
  }

  .cv-page__action {
    display: inline-flex;
    min-height: 2.75rem;
    align-items: center;
    justify-content: center;
    padding: 0.65rem 1.1rem;
    border: 1px solid var(--global-theme-color);
    border-radius: 0.3rem;
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .cv-page__action:hover,
  .cv-page__action:focus-visible {
    background: var(--global-theme-color);
    color: var(--global-bg-color);
    text-decoration: none;
  }

  .cv-page__action--primary {
    background: var(--global-theme-color);
    color: var(--global-bg-color);
  }

  .cv-page__preview {
    overflow: hidden;
    border: 1px solid color-mix(in srgb, var(--global-text-color) 18%, transparent);
    border-radius: 0.45rem;
    background: #f7f7f4;
  }

  .cv-page__preview object {
    display: block;
    width: 100%;
    height: min(78vh, 900px);
    min-height: 650px;
    border: 0;
  }

  @media (max-width: 700px) {
    .cv-page__preview {
      display: none;
    }

    .cv-page__actions {
      margin-bottom: 0;
    }
  }
</style>

{% assign cv_path = '/assets/pdf/Yang_Li_CV.pdf' %}

<div class="cv-page">
  <header class="cv-page__header">
    <h1>Curriculum Vitae</h1>
    <p>
      My academic CV provides details on my education, research experience, publications, projects, teaching, awards, research visits, and professional
      activities.
    </p>
  </header>

  <div class="cv-page__actions" aria-label="Curriculum vitae options">
    <a class="cv-page__action cv-page__action--primary" href="{{ cv_path | relative_url }}" target="_blank" rel="noopener noreferrer">View CV</a>
    <a class="cv-page__action" href="{{ cv_path | relative_url }}" download>Download PDF</a>
  </div>

  <div class="cv-page__preview">
    <object data="{{ cv_path | relative_url }}#view=FitH" type="application/pdf" title="Yang Li curriculum vitae PDF preview">
      <p>
        This browser cannot display the PDF preview. <a href="{{ cv_path | relative_url }}" target="_blank" rel="noopener noreferrer">View the CV</a>.
      </p>
    </object>
  </div>
</div>
