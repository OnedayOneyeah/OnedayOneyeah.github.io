---
layout: page
permalink: /teaching/
title: teaching
description: Teaching assistantships in computing and deep learning.
nav: true
nav_order: 6
---

I have served as a teaching assistant for the following courses. Spring and Fall correspond to the first and second semesters, respectively.

<table class="table">
  <thead>
    <tr>
      <th scope="col">Course</th>
      <th scope="col">Teaching Assistantship</th>
    </tr>
  </thead>
  <tbody>
    {% for entry in site.data.cv.cv.sections.Teaching %}
    <tr>
      <th scope="row">{{ entry.label | escape }}</th>
      <td>{{ entry.details | escape }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
