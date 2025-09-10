---
title: "trailsLAB - Publications"
layout: gridlay
excerpt: "Technocritical Research on AI, Learning & Society (trailsLAB) — Publications."
sitemap: false
permalink: /publications/
---

# Publications
{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row pub-rows">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

-----
<div class="pub-funding">
  <h2>Our work is supported by the following NSF awards</h2>
 <ul>
    <li>Johri, A. (2024). Education DCL: EAGER: An Embedded Case Study Approach for Broadening Students' Mindset for Ethical and Responsible Cybersecurity. <strong>NSF Award Number 2335636</strong>.</li>
    <li>Johri, A. (2023). EAGER: Impact of Generative Artificial Intelligence (GAI) on Engineering Education Practices. <strong>NSF Award Number 2319137</strong>.</li>
    <li>Johri, A. (2020). Situated Algorithmic Thinking: Preparing the Future Computing Workforce for Ethical Decision-Making through Interactive Case Studies. <strong>NSF Award Number 1937950</strong>.</li>
  </ul>
</div>
