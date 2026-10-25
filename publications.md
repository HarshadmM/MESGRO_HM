---
layout: default
title: Publications, Awards & Milestones
permalink: /publications/
---

<section class="publications-page">
  <div class="container">
    <header class="publications-header">
      <p class="publications-eyebrow">Research &amp; recognition</p>
      <h1>Publications, Awards &amp; Milestones</h1>
      <p>Research, project awards, and milestones across robotics, mechatronics, and engineering.</p>
    </header>

    <section class="recognition-section" aria-labelledby="awards-heading">
      <h2 class="publications-section-title" id="awards-heading">Awards &amp; milestones</h2>
      <div class="publication-list">
        <article class="publication-card award-card">
          <p class="publication-year">March 2026 · Winner</p>
          <h2>Hackstarter Award: Open Project</h2>
          <p class="publication-venue"><strong>NeoAir</strong> won the Open Project award at Hackstarter 2026, the Imperial College Advanced Hackspace programme final.</p>
          <p class="publication-authors">Team: Amy Lai, Anton Gerasimov, Hetarth Bhatt, Harshad Malik</p>
          <div class="publication-links">
            <a href="https://imperialhackspace.com/our-events/hackstarter-26/" target="_blank" rel="noopener noreferrer">Hackstarter 2026 winners</a>
            <a href="{{ '/projects/neoair/' | relative_url }}">View the NeoAir project</a>
          </div>
        </article>
      </div>
    </section>

    <section class="publications-section" aria-labelledby="presentations-heading">
      <h2 class="publications-section-title" id="presentations-heading">Presentations</h2>
      <div class="publication-list">
        <article class="publication-card">
          <p class="publication-year">Poster presentation</p>
          <h2>Deployable Hybrid Continuum-Eversion Robot for Medical Applications in Disaster Scenarios</h2>
          <p class="publication-venue">Hamlyn Symposium on Medical Robotics</p>
          <div class="presentation-gallery" role="group" aria-label="Poster and presentation images">
            <a class="presentation-gallery-poster" href="{{ '/assets/images/projects/publications/Harshad_Malik_06062560%20HS%20poster.png' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Open the research poster at full size">
              <img src="{{ '/assets/images/projects/publications/Harshad_Malik_06062560%20HS%20poster.png' | relative_url }}" alt="Research poster titled A Deployable Hybrid Soft Robotic Platform for Emergency Medical Intervention in Extreme Environments" loading="lazy">
            </a>
            <img class="presentation-gallery-photo" src="{{ '/assets/images/projects/publications/Poster_presentation4.jpeg' | relative_url }}" alt="Harshad Malik presenting his research poster at the Hamlyn Symposium on Medical Robotics" loading="lazy">
          </div>
          <div class="publication-links">
            <a href="mailto:harshadmm10131@gmail.com?subject=Poster%20and%20thesis%20summary%20request">Request poster and/or thesis summary for detailed reading</a>
          </div>
        </article>
      </div>
    </section>

    <section class="publications-section" aria-labelledby="publications-heading">
      <h2 class="publications-section-title" id="publications-heading">Publications</h2>
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
        <h2>No publications listed yet</h2>
        <p>Journal papers, conference papers, and other published research will be listed here.</p>
      </div>
    {% endif %}
    </section>
  </div>
</section>
