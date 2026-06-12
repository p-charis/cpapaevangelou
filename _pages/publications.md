---
layout: archive
title: "Publications"
permalink: /publications/
---


{% include base_path %}

<p class="archive-intro">Peer-reviewed articles, book chapters, reports, and selected research outputs.</p>

{% assign publications = site.publications | sort: 'date' | reverse %}
{% assign current_year = '' %}
{% for post in publications %}
{% assign publication_year = post.date | date: '%Y' %}
{% if publication_year != current_year %}
<h2 class="archive-year">{{ publication_year }}</h2>
{% assign current_year = publication_year %}
{% endif %}
<article class="publication-entry">
<p class="publication-entry__meta">{% if post.status %}{{ post.status }} &middot; {% endif %}{% if post.venue %}<i>{{ post.venue }}</i>{% endif %}</p>
<h3><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></h3>
{% if post.authors %}<p class="publication-entry__authors">{{ post.authors }}</p>{% endif %}
<div class="publication-entry__links">
<a href="{{ post.paperurl }}">Publisher / source <span aria-hidden="true">&nearr;</span></a>
<a href="{{ base_path }}{{ post.url }}">Details <span aria-hidden="true">&rarr;</span></a>
</div>
</article>
{% endfor %}
