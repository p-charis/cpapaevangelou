---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---


{% include base_path %}

{% assign publications = site.publications | sort: 'date' | reverse %}
{% assign current_year = '' %}
{% for post in publications %}
  {% assign publication_year = post.date | date: '%Y' %}
  {% if publication_year != current_year %}
    <h2 class="archive-year">{{ publication_year }}</h2>
    {% assign current_year = publication_year %}
  {% endif %}
  {% include archive-single.html %}
{% endfor %}
