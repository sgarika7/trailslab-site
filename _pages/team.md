---
title: "trailsLAB - Team"
layout: gridlay
excerpt: "Technocritical Research on AI, Learning & Society (trailsLAB) — Team."
sitemap: false
permalink: /team/
---

# Group Members

<div class="row">
{% for member in site.data.team_members %}
  <div class="col-sm-6">
    <div class="team-card">
      <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="team-photo" alt="{{ member.name }}">
      <div class="team-body">
        <h4>{{ member.name }}</h4>
        <i>{{ member.info }}</i>
        <ul>
          {% if member.number_educ == 1 %}
            <li>{{ member.education1 }}</li>
          {% endif %}
          {% if member.number_educ == 2 %}
            <li>{{ member.education1 | markdownify }}</li>
            <li>{{ member.education2 | markdownify }}</li>
          {% endif %}
          {% if member.number_educ == 3 %}
            <li>{{ member.education1 }}</li>
            <li>{{ member.education2 }}</li>
            <li>{{ member.education3 }}</li>
          {% endif %}
          {% if member.number_educ == 4 %}
            <li>{{ member.education1 }}</li>
            <li>{{ member.education2 }}</li>
            <li>{{ member.education3 }}</li>
            <li>{{ member.education4 }}</li>
          {% endif %}
          {% if member.number_educ == 5 %}
            <li>{{ member.education1 }}</li>
            <li>{{ member.education2 }}</li>
            <li>{{ member.education3 }}</li>
            <li>{{ member.education4 }}</li>
            <li>{{ member.education5 }}</li>
          {% endif %}
        </ul>
      </div>
    </div>
  </div>
{% endfor %}
</div>
