---
layout: home
permalink: /
title: "Charis Papaevangelou"
excerpt: "Researcher working on the state-tech capital power dynamics and their impact on society and the environment"
redirect_from:
  - /about/
  - /about.html
---

<section class="home-hero">
  <div class="home-hero__copy">
    <p class="eyebrow">Platforms / AI / infrastructure / democracy</p>
    <h1>Charis Papaevangelou</h1>
    <figure class="home-portrait home-portrait--mobile">
      <img src="{{ '/images/profile-pic-2025.png' | relative_url }}" alt="Portrait of Charis Papaevangelou">
    </figure>
    <p class="home-hero__lead">I study how the power relations between state actors and tech firms shape technology's political economy, including their implications for our societies and the environment, and our capacity to reclaim control.</p>
    <div class="home-hero__bio">
      <p>I am a postdoctoral researcher at the University of Amsterdam's <a href="https://www.ivir.nl/">Institute for Information Law</a>, where I work within the <a href="https://algosoc.org/">Public Values in the Algorithmic Society (AlgoSoc)</a> programme. I am also affiliated with the University of Toulouse through the Horizon Europe <a href="https://forsee-project.eu/">FORSEE</a> project.</p>
      <p>My research draws from critical media, political economy, science and technology studies, and technology governance to examine how the interplay between large technology firms and state actors affects political, economic, informational, and natural environments. <br>My current interests revolve around the political economy of AI infrastructure, particularly data centres. <a href="{{ '/contact/' | relative_url }}">Get in touch</a>.</p>
    </div>
  </div>
  <figure class="home-portrait home-portrait--desktop">
    <img src="{{ '/images/profile-pic-2025.png' | relative_url }}" alt="Portrait of Charis Papaevangelou">
  </figure>
</section>

<section class="home-section" aria-labelledby="work-heading">
  <div class="section-heading">
    <div>
      <p class="eyebrow">Selected work</p>
      <h2 id="work-heading">Recent publications</h2>
    </div>
    <a class="text-link" href="{{ '/publications/' | relative_url }}">All publications <span aria-hidden="true">&rarr;</span></a>
  </div>
  <div class="home-publications">
    {% assign featured_publications = site.publications | sort: 'date' | reverse %}
    {% for post in featured_publications limit:3 %}
      <article class="publication-row">
        <p class="publication-row__meta">{% if post.date_precision == 'year' %}{{ post.date | date: '%Y' }}{% else %}{{ post.date | date: '%-d %B %Y' }}{% endif %}{% if post.status %}<br>{{ post.status }}{% elsif post.venue %}<br>{{ post.venue }}{% endif %}</p>
        <div>
          <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
          {% if post.authors %}<p class="publication-row__authors">{{ post.authors }}</p>{% endif %}
          <div class="publication-row__links">
            {% if post.paperurl %}<a href="{{ post.paperurl }}">Publication <span aria-hidden="true">&nearr;</span></a>{% endif %}
            <a href="{{ post.url | relative_url }}">Details <span aria-hidden="true">&rarr;</span></a>
          </div>
        </div>
      </article>
    {% endfor %}
  </div>
</section>

<section class="home-section currently" aria-labelledby="currently-heading">
  <div class="section-heading">
    <div>
      <h2 id="currently-heading">What I am...</h2>
    </div>
    <a class="text-link" href="{{ '/currently/' | relative_url }}">Activity log <span aria-hidden="true">&rarr;</span></a>
  </div>
  <div class="currently-grid">
    {% for item in site.data.currently.items %}
    <article class="currently-card">
      <p class="currently-card__label">{{ item.label }}</p>
      {% for entry in item.current %}
      <div class="currently-card__entry">
        <h3>{% if entry.url %}<a href="{{ entry.url }}">{{ entry.title }}</a>{% else %}{{ entry.title }}{% endif %}</h3>
        {% if entry.creator %}<p>{{ entry.creator }}</p>{% endif %}
        {% if entry.note %}<p>{{ entry.note }}</p>{% endif %}
      </div>
      {% endfor %}
      {% if item.profile_url %}<a class="currently-card__profile" href="{{ item.profile_url }}">{{ item.profile_label }} <span aria-hidden="true">&nearr;</span></a>{% endif %}
    </article>
    {% endfor %}
  </div>
</section>
