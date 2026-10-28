---
layout: default
permalink: /cv/
title: CV
nav: true
nav_order: 5
cv_pdf: /assets/rendercv/rendercv_output/Yewon_Han_CV.pdf
cv_format: rendercv # options: rendercv, jsonresume
description: Academic curriculum vitae of Yewon Han — research, publications, awards, and projects.
toc:
  sidebar: left
---

<link rel="stylesheet" href="{{ '/assets/css/al-folio-cv.css' | relative_url }}">

<style>
.cv > .card > .card-title {
  margin-bottom: 1.25rem;
}

.cv ul,
.cv ol {
  list-style: none;
  padding-inline-start: 0;
}

.cv li::marker {
  content: "";
}

.cv .list-group {
  margin: 0;
}

.cv .list-group-item {
  padding: 0;
}

.cv .list-group-item + .list-group-item {
  margin-top: 1.75rem;
}

.cv .list-group-item > .row {
  display: grid;
  grid-template-columns: 9rem minmax(0, 1fr);
  gap: 0 1.75rem;
  align-items: start;
  margin: 0;
}

.cv .list-group-item > .row > [class*="col-"] {
  width: auto;
  max-width: none;
  min-width: 0;
  padding: 0;
}

.cv .date-column {
  transform: none;
}

.cv .list-group-item > .row > .col-xs-12 {
  grid-column: 1 / -1;
}

.cv .list-group-item p {
  margin: 0;
  line-height: 1.65;
}

.cv .items {
  margin: 0.75rem 0 0;
}

.cv .items li + li {
  margin-top: 0.5rem;
}

.cv table.table-cv {
  margin: 0;
  width: auto;
}

.cv table.table-cv tr,
.cv table.table-cv td,
.cv table.table-cv th {
  border: 0;
}

.cv table.table-cv p.location {
  margin: 0.5rem 0 0;
  white-space: normal;
}

@media (max-width: 575.98px) {
  .cv .list-group-item > .row {
    grid-template-columns: minmax(0, 1fr);
    gap: 0.75rem;
  }
}

/* Override important spacing utilities in the theme's earlier cascade layer. */
@layer theme {
  .cv > .card {
    padding: 1.5rem !important;
  }

  .cv .list-group-item h6 {
    margin: 0 0 0.5rem !important;
  }

  .cv .list-group-item > .row > [class*="col-"] {
    margin-top: 0 !important;
  }

  .cv .list-group-item > .row > :first-child {
    text-align: left !important;
  }

  @media (max-width: 575.98px) {
    .cv > .card {
      padding: 1.25rem !important;
    }
  }
}
</style>

{% al_folio_cv_render %}
