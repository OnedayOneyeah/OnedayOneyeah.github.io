---
layout: page
title: projects
permalink: /projects/
description: Research projects and industry–academia collaborations.
nav: true
nav_order: 3
display_categories: [research]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects project-gallery">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>

<style>
  .projects.project-gallery .row > .col {
    margin-bottom: 1.5rem;
  }

  .projects.project-gallery .card {
    height: 100%;
    overflow: hidden;
  }

  .projects.project-gallery .card > figure {
    margin: 0;
  }

  .projects.project-gallery .card img {
    display: block;
    width: 100%;
    height: auto;
    aspect-ratio: 3 / 2;
    object-fit: contain;
  }

  .projects.project-gallery .card-body {
    padding: 1.25rem 1.5rem 1.5rem;
  }

  .projects.project-gallery .card-title {
    margin: 0 0 0.75rem;
    font-size: 1.2rem;
    font-weight: 600;
    line-height: 1.45;
    letter-spacing: -0.01em;
    word-break: normal;
    overflow-wrap: break-word;
    hyphens: none;
    text-wrap: pretty;
  }

  .projects.project-gallery .card-text {
    margin-bottom: 0;
    font-size: 0.95rem;
    line-height: 1.7;
  }

  @media (max-width: 575.98px) {
    .projects.project-gallery .card-body {
      padding: 1rem 1.25rem 1.25rem;
    }

    .projects.project-gallery .card-title {
      font-size: 1.1rem;
    }
  }
</style>
