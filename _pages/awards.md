---
layout: page
title: "Selected Awards"
permalink: /awards/
---

<!-- Research Recognition Section -->
<h2>Research Recognitions</h2>
<hr>
<ul>
  {% assign research_recognition = site.awards | where: "category", "Research Recognition" %}
  {% for award in research_recognition %}
    <li>
      <strong>{{ award.title }}</strong><br>
      {{ award.description }}<br>
      <small>{{ award.year }}</small>
    </li>
  {% endfor %}
</ul>

<!-- Honors Section -->
<h2>Honors and Scholarship</h2>
<hr>
<ul style="list-style-type: none; padding: 0;">
  {% assign honors = site.awards | where: "category", "Honors" %}
  {% for award in honors %}
    <li style="margin-bottom: 1em;">
      <strong>{{ award.title }}</strong> {% if award.institution %}({{ award.institution }}){% endif %}, {{ award.year }}.<br>
      <em>{{ award.description }}</em>
    </li>
  {% endfor %}
</ul>
