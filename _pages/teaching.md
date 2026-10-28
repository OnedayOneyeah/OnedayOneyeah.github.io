---
layout: page
permalink: /teaching/
title: teaching
description: Teaching assistantships in computing and deep learning.
nav: true
nav_order: 6
---

<table class="table">
  <thead>
    <tr>
      <th scope="col">Course</th>
      <th scope="col">Period</th>
    </tr>
  </thead>
  <tbody>
    {% for entry in site.data.cv.cv.sections.Teaching %}
    <tr>
      <th scope="row">{{ entry.label | escape }}</th>
      <td>{{ entry.details | remove_first: 'Teaching Assistant — ' | escape }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
