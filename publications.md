---
layout: default
title: Publications
permalink: /publications/
---

<section class="publications-page">
  <div class="container">
    <header class="publications-header">
      <p class="publications-eyebrow">Research &amp; writing</p>
      <h1>Publications</h1>
      <p>Research papers and conference contributions related to robotics, mechatronics, and engineering.</p>
    </header>

    {% assign publications = site.publications | sort: "year" | reverse %}
    {% if publications.size > 0 %}
      <div class="publication-list">
        {% for publication in publications %}
          <article class="publication-card">
            {% if publication.year %}
              <p class="publication-year">{{ publication.year }}</p>
            {% endif %}

            <h2>{{ publication.title | escape }}</h2>

            {% if publication.authors %}
              <p class="publication-authors">{{ publication.authors | escape }}</p>
            {% endif %}

            {% if publication.venue %}
              <p class="publication-venue">{{ publication.venue | escape }}</p>
            {% endif %}

            {% if publication.abstract %}
              <div class="publication-abstract">{{ publication.abstract | markdownify }}</div>
            {% endif %}

            {% if publication.doi or publication.paper_url or publication.pdf_url %}
            <div class="publication-links">
              {% if publication.doi %}
                <a href="https://doi.org/{{ publication.doi | escape }}" target="_blank" rel="noopener noreferrer">DOI</a>
              {% endif %}
              {% if publication.paper_url %}
                <a href="{{ publication.paper_url | escape }}" target="_blank" rel="noopener noreferrer">Read paper</a>
              {% endif %}
              {% if publication.pdf_url %}
                <a href="{{ publication.pdf_url | relative_url }}" target="_blank" rel="noopener noreferrer">PDF</a>
              {% endif %}
            </div>
            {% endif %}
          </article>
        {% endfor %}
      </div>
    {% else %}
      <div class="publications-empty">
        <h2>Publications will appear here</h2>
        <p>This section is ready for journal papers, conference papers, and other published research.</p>
      </div>
    {% endif %}
  </div>
</section>
