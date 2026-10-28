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
  .cv ul,
  .cv ol {
    list-style: none;
    padding-inline-start: 0;
  }

  .cv li::marker {
    content: "";
  }

  .cv .items {
    margin-inline-start: 0;
  }

  .cv .items li + li {
    margin-top: 0.35rem;
  }
</style>

{% al_folio_cv_render %}
