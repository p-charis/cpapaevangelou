---
layout: home
permalink: /
title: "Charis Papaevangelou"
excerpt: "Researcher working on platform governance, media policy, and the political economy of digital infrastructures."
redirect_from:
  - /about/
  - /about.html
---

<section class="home-hero">
  <div class="home-hero__copy">
    <p class="eyebrow">Media, platforms, and democratic governance</p>
    <h1>Charis Papaevangelou</h1>
    <p class="home-hero__lead">I study how digital platforms reshape media, public communication, and democratic governance.</p>
    <p class="home-hero__intro">I am a postdoctoral researcher at the University of Amsterdam's <a href="https://www.ivir.nl/">Institute for Information Law</a> and part of <a href="https://algosoc.org/">AlgoSoc</a>. My current work examines how European platform regulation is changing the relationship between news organisations and technology platforms.</p>
    <div class="home-actions">
      <a class="button button--primary" href="{{ '/publications/' | relative_url }}">Explore publications</a>
      <a class="button button--secondary" href="{{ '/cv/' | relative_url }}">View CV</a>
    </div>
  </div>
  <figure class="home-portrait">
    <img src="{{ '/images/profile_pic.jpg' | relative_url }}" alt="Portrait of Charis Papaevangelou">
  </figure>
</section>

<section class="home-section home-section--grid" aria-labelledby="research-heading">
  <div>
    <p class="eyebrow">Research</p>
    <h2 id="research-heading">Power and accountability in the platform society</h2>
  </div>
  <div class="home-section__body">
    <p>My research sits at the intersection of media studies, political economy, platform governance, and digital regulation. I am particularly interested in the institutional dependencies that emerge between platforms, news media, regulators, and civil society.</p>
    <ul class="topic-list" aria-label="Research areas">
      <li>Platform governance</li>
      <li>Media policy</li>
      <li>Political economy</li>
      <li>EU digital regulation</li>
      <li>News and platforms</li>
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
