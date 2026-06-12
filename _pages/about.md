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
    <div class="home-hero__bio">
      <p>I am a postdoctoral researcher at the University of Amsterdam's <a href="https://www.ivir.nl/">Institute for Information Law</a>, where I work within the <a href="https://algosoc.org/">Public Values in the Algorithmic Society (AlgoSoc)</a> programme. I am also affiliated with the University of Toulouse through the Horizon Europe <a href="https://forsee-project.eu/">FORSEE</a> project.</p>
      <p>My research brings critical media research, science and technology studies, political economy, and technology governance into conversation. I examine how large technology firms affect political, economic, informational, and natural environments, with growing attention to AI infrastructure, digital sovereignty, and the environmental implications of artificial intelligence.</p>
    </div>
    {% include profile-links.html %}
    <div class="home-actions">
      <a href="{{ '/publications/' | relative_url }}">Publications <span aria-hidden="true">&rarr;</span></a>
      <a href="{{ '/files/june26-academic-minimal-cv.pdf' | relative_url }}">Download CV <span aria-hidden="true">&darr;</span></a>
    </div>
  </div>
  <figure class="home-portrait">
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
    {% for post in featured_publications limit:4 %}
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
      <p class="eyebrow">In rotation</p>
      <h2 id="currently-heading">Currently</h2>
    </div>
    {% if site.data.currently.updated %}<p class="currently__updated">Updated {{ site.data.currently.updated }}</p>{% endif %}
  </div>
  <div class="currently-grid">
    {% for item in site.data.currently.items %}
    <article class="currently-card">
      <p class="currently-card__label">{{ item.label }}</p>
      <h3>{% if item.url %}<a href="{{ item.url }}">{{ item.title }}</a>{% else %}{{ item.title }}{% endif %}</h3>
      {% if item.note %}<p>{{ item.note }}</p>{% endif %}
    </article>
    {% endfor %}
  </div>
</section>

<section class="home-contact" aria-labelledby="contact-heading">
  <h2 id="contact-heading">You can reach out to me at: <a href="mailto:c.papaevangelou@uva.nl">c.papaevangelou[at]uva.nl</a>.</h2>
</section>
