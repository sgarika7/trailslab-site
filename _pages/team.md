---

title: "TRAILSlab - Team"
layout: gridlay
excerpt: "Technocritical Research on AI, Learning & Society (trailsLAB) — Publications."
sitemap: false
permalink: /team/
-----------------

# Group Members

{% assign number\_printed = 0 %}
{% for member in site.data.team\_members %}

{% assign even\_odd = number\_printed | modulo: 2 %}

{% if even\_odd == 0 %}

<div class="row">
{% endif %}

<div class="col-sm-6">
  <div class="team-card">
    <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="team-photo" alt="{{ member.name }}">
    <div class="team-body">
      <h4>{{ member.name }}</h4>
      <i>{{ member.info }}</i>
      <ul>

{% if member.number\_educ == 1 %}

  <li> {{ member.education1 }} </li>
  {% endif %}

{% if member.number\_educ == 2 %}

  <li> {{ member.education1 | markdownify}} </li>
  <li> {{ member.education2 | markdownify}} </li>
  {% endif %}

{% if member.number\_educ == 3 %}

  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}

{% if member.number\_educ == 4 %}

  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  {% endif %}

{% if member.number\_educ == 5 %}

  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number\_printed = number\_printed | plus: 1 %}

{% if even\_odd == 1 %}

</div>
{% endif %}

{% endfor %}

{% assign even\_odd = number\_printed | modulo: 2 %}
{% if even\_odd == 1 %}

</div>
{% endif %} is this team.md is good now ?
