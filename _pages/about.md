---
layout: home
permalink: /
title: "Charis Papaevangelou"
excerpt: "Researcher working on platform power, AI infrastructure, media, and democratic governance."
redirect_from:
  - /about/
  - /about.html
---

<section class="home-hero">
  <div class="home-hero__copy">
    <p class="eyebrow">Platforms / AI / infrastructure / democracy</p>
    <h1>Charis Papaevangelou</h1>
    <p class="home-hero__lead">I study how Big Tech's platforms, AI systems, and material infrastructures reshape society and the environment.</p>
    <p class="home-hero__intro">I am a postdoctoral researcher at the University of Amsterdam's <a href="https://www.ivir.nl/">Institute for Information Law</a> within <a href="https://algosoc.org/">AlgoSoc</a>, and at the University of Toulouse through the Horizon Europe <a href="https://forsee-project.eu/">FORSEE</a> project. My work brings critical media research, STS, political economy, and technology governance into conversation.</p>
    <div class="home-actions">
      <a class="button button--primary" href="{{ '/publications/' | relative_url }}">Explore publications</a>
      <a class="button button--secondary" href="{{ '/cv/' | relative_url }}">View CV</a>
    </div>
  </div>
  <figure class="home-portrait">
    <img src="{{ '/images/profile-pic-2025.png' | relative_url }}" onerror="this.onerror=null;this.src='{{ '/images/profile_pic.jpg' | relative_url }}';" alt="Portrait of Charis Papaevangelou">
  </figure>
</section>

<section class="home-section home-section--grid" aria-labelledby="research-heading">
  <div>
    <p class="eyebrow">Research</p>
    <h2 id="research-heading">Following power from the interface to the data centre</h2>
  </div>
  <div class="home-section__body">
    <p>My research examines how large technology firms intersect with political, economic, informational, and natural environments. Alongside platform and media governance, I increasingly focus on AI's material infrastructures, environmental implications, and the politics of digital sovereignty.</p>
    <ul class="topic-list" aria-label="Research areas">
      <li>Platform governance</li>
      <li>Media policy</li>
      <li>Political economy</li>
      <li>EU digital regulation</li>
      <li>News and platforms</li>
      <li>AI infrastructures</li>
      <li>Technology & environment</li>
    </ul>
  </div>
</section>

<section class="home-section" aria-labelledby="work-heading">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Selected work</p>
      <h2 id="work-heading">Recent publications</h2>
    </div>
    <a class="text-link" href="{{ '/publications/' | relative_url }}">All publications <span aria-hidden="true">&rarr;</span></a>
  </div>
  <div class="featured-work">
    {% assign featured_publications = site.publications | sort: 'date' | reverse %}
    {% for post in featured_publications limit:3 %}
      <article class="featured-card">
        <p class="featured-card__meta">{{ post.date | date: '%Y' }}{% if post.venue %} &middot; {{ post.venue }}{% endif %}</p>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.excerpt %}<p>{{ post.excerpt | strip_html | truncatewords: 28 }}</p>{% endif %}
        {% if post.paperurl %}<a class="text-link" href="{{ post.paperurl }}">Read publication <span aria-hidden="true">&rarr;</span></a>{% endif %}
      </article>
    {% endfor %}
  </div>
</section>

<section class="home-section currently" aria-labelledby="currently-heading">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Off screen, mostly</p>
      <h2 id="currently-heading">Currently</h2>
    </div>
    {% if site.data.currently.updated %}<p class="currently__updated">Updated {{ site.data.currently.updated }}</p>{% endif %}
  </div>
  <div class="currently-grid">
    {% for item in site.data.currently.items %}
      <article class="currently-card">
        <p class="currently-card__label">{{ item.label }}</p>
        <h3>{{ item.title }}</h3>
        {% if item.note %}<p>{{ item.note }}</p>{% endif %}
        {% if item.url %}<a class="text-link" href="{{ item.url }}">Open <span aria-hidden="true">&nearr;</span></a>{% endif %}
      </article>
    {% endfor %}
  </div>
</section>

<section class="home-contact" aria-labelledby="contact-heading">
  <div>
    <p class="eyebrow">Contact</p>
    <h2 id="contact-heading">Research, collaboration, and speaking</h2>
  </div>
  <div>
    <p>I welcome conversations about research collaborations, events, and media enquiries.</p>
    <p><a class="button button--primary" href="mailto:c.papaevangelou@uva.nl">c.papaevangelou@uva.nl</a></p>
  </div>
</section>
