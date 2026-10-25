---
layout: default
title: About
permalink: /about/
# Gallery entries use image, alt, and caption fields; image paths are relative to the site root.
sketch_gallery:
  - image: "/assets/images/sketch1.jpg"
    alt: "Ink-and-wash sketch of a person holding a cup."
    caption: "Ink-and-wash portrait study"
  - image: "/assets/images/sketch2.jpg"
    alt: "Pencil portrait of a person wearing a knit cap."
    caption: "Pencil portrait study"
  - image: "/assets/images/sketch3.jpg"
    alt: "Pencil drawing of two figures in profile facing one another."
    caption: "Figure study"
  - image: "/assets/images/sketch4.jpg"
    alt: "Ink drawing of a fantastical long-necked creature."
    caption: "Creature study"
  - image: "/assets/images/sketch6.jpg"
    alt: "Pencil character portrait in a sketchbook outdoors."
    caption: "Sketchbook portrait"
  - image: "/assets/images/sketch_.jpg"
    alt: "Page of rough pencil studies of two character heads."
    caption: "Character studies"
physical_gallery:
  - image: "/assets/images/run_extra.jpeg"
    alt: "Harshad taking part in an outdoor running event."
    caption: "Taking part in an outdoor running event"
  - image: "/assets/images/10k.jpg"
    alt: "A Rotary Rain Run 10-kilometre race bib and medal."
    caption: "Rotary Rain Run · 10K · Goa, 2024"
half_marathon_certificates:
  - image: "/assets/images/half_marathon.jpg"
    alt: "RG Marathon 5.0 21K participation certificate and medal for Harshad Malik, Goa, 13 October 2024."
    caption: "RG Marathon 5.0 · 21K · Goa · 13 October 2024"
---

<div class="hero-personal">
  <div class="container">
    <div class="hero-content about-hero-content">
      <div class="about-hero-profile">
        <img class="about-hero-portrait"
          src="{{ '/assets/images/self_portrait.jpeg' | relative_url }}"
          alt="Portrait of Harshad Malik"
          loading="eager">
        <div class="about-hero-copy">
          <h1 class="hero-name">Harshad Malik</h1>
          <p class="hero-title">Medical Graduate | Robotics Engineer &amp; Researcher</p>
          <p class="hero-description">
            I bring a medical perspective to robotics: grounding engineering in
            clinical needs, then using design, prototyping, and research to explore
            what technology can make possible.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="container">
  <section class="about-accordion">
    <h2>Background &amp; Core Values</h2>
    <div class="project-description-content">
      <p>
        My medical training gave me a grounding in anatomy, physiology, and clinical
        context. I bring that knowledge into design by starting with the person and
        task: considering a client's anatomy and remaining movement when developing
        a partial-hand prosthesis, and the practical demands of medical intervention
        when exploring deployable robotics. It is why medical and surgical robotics
        feel like a natural place to bring medicine and engineering together.
      </p>
      <p>
        My research training at Imperial College London's Hamlyn Centre for
        Medical Robotics gave me a way to carry that perspective into engineering.
        I proposed my MRes thesis topic to my primary supervisor, Professor George
        Mylonas, and developed it from a paper proposal into a project on a
        deployable hybrid continuum-eversion robot for medical applications in
        disaster scenarios. That work connected clinical purpose with CAD,
        mechanical design, prototyping, modelling, integration, and experimental
        testing.
      </p>
      <p>
        I aim to apply science, technology, and rigorous research for the
        betterment of humanity. I also believe knowledge carries a responsibility:
        to pass practical skills and values to coming generations, and to guide
        them in asking questions and reasoning from scientific principles.
      </p>
    </div>
  </section>

  <section class="about-accordion">
    <h2>Education</h2>
    <div class="project-description-content">
      <p>
        <strong>MRes Medical Robotics and Image-Guided Intervention</strong><br>
        Imperial College London · Distinction<br>
        Research project mark: 75%.
      </p>
      <p>
        <strong>MBBS</strong><br>
        Smolensk State Medical University · 2018–2024<br>
        Final marks: 95.34.
      </p>
    </div>
  </section>

  <section class="about-accordion">
    <h2>Research Interests</h2>
    <div class="project-description-content">
      <ul>
        <li>Continuum and deployable robotics</li>
        <li>Prosthetics and assistive technology</li>
        <li>Biomimetic mechanisms and mechanical design</li>
        <li>Search-and-rescue and field robotics</li>
        <li>Mechatronics and robotic actuation</li>
        <li>Medical and surgical robotics</li>
      </ul>
    </div>
  </section>

  <section class="about-accordion" aria-labelledby="beyond-engineering-heading">
    <h2 id="beyond-engineering-heading">Beyond Engineering</h2>
    <div class="project-description-content">
      <section class="about-subsection" aria-labelledby="physical-heading">
        <h3 id="physical-heading">Physical pursuits &amp; achievements</h3>
        <p>Running gives me a different kind of challenge outside the lab.</p>
        {% assign physical_items = page.physical_gallery %}
        {% assign certificate_items = page.half_marathon_certificates %}
        {% if physical_items.size > 0 or certificate_items.size > 0 %}
          <div class="about-gallery-carousel" data-about-gallery>
            <button class="about-gallery-control" type="button" data-gallery-prev aria-label="Scroll physical activities gallery left" disabled>
              <i class="fas fa-chevron-left" aria-hidden="true"></i>
            </button>
            <div class="about-gallery-track" data-gallery-track role="list" aria-label="Running and race achievements" tabindex="0">
              {% for item in physical_items %}
                <figure class="about-gallery-card" role="listitem">
                  <img src="{{ item.image | relative_url }}" alt="{{ item.alt | escape }}" loading="lazy">
                  {% if item.caption %}
                    <figcaption>{{ item.caption | escape }}</figcaption>
                  {% endif %}
                </figure>
              {% endfor %}
              {% for item in certificate_items %}
                <figure class="about-gallery-card about-gallery-card--certificate" role="listitem">
                  <img src="{{ item.image | relative_url }}" alt="{{ item.alt | escape }}" loading="lazy">
                  {% if item.caption %}
                    <figcaption>{{ item.caption | escape }}</figcaption>
                  {% endif %}
                </figure>
              {% endfor %}
            </div>
            <button class="about-gallery-control" type="button" data-gallery-next aria-label="Scroll physical activities gallery right">
              <i class="fas fa-chevron-right" aria-hidden="true"></i>
            </button>
          </div>
        {% else %}
          <div class="about-gallery-empty">Running and race achievements will appear here.</div>
        {% endif %}
      </section>

      <section class="about-subsection" aria-labelledby="sketches-heading">
        <h3 id="sketches-heading">Sketches</h3>
        {% assign sketch_items = page.sketch_gallery %}
        {% if sketch_items and sketch_items.size > 0 %}
          <div class="about-gallery-carousel" data-about-gallery>
            <button class="about-gallery-control" type="button" data-gallery-prev aria-label="Scroll sketches gallery left" disabled>
              <i class="fas fa-chevron-left" aria-hidden="true"></i>
            </button>
            <div class="about-gallery-track about-gallery-track--art" data-gallery-track role="list" aria-label="Sketches" tabindex="0">
              {% for item in sketch_items %}
                <figure class="about-gallery-card about-gallery-card--art" role="listitem">
                  <img src="{{ item.image | relative_url }}" alt="{{ item.alt | escape }}" loading="lazy">
                </figure>
              {% endfor %}
            </div>
            <button class="about-gallery-control" type="button" data-gallery-next aria-label="Scroll sketches gallery right">
              <i class="fas fa-chevron-right" aria-hidden="true"></i>
            </button>
          </div>
        {% else %}
          <div class="about-gallery-empty">Sketches will appear here.</div>
        {% endif %}
      </section>

      <section class="about-subsection" aria-labelledby="prosthetics-society-heading">
        <h3 id="prosthetics-society-heading">Prosthetics Society</h3>
        <p>
          I enjoy sharing practical knowledge. I taught members of the
          <a href="https://www.linkedin.com/company/imperial-college-london-prosthetics-society/posts/?feedView=all">
            Imperial College London Prosthetics Society
          </a>
          about cable transmission mechanisms used in prosthetic devices.
        </p>
        <figure class="about-feature-figure">
          <img
            src="{{ '/assets/images/projects/about_page/teaching%20cable%20management.jpeg' | relative_url }}"
            alt="Teaching members of the Imperial College London Prosthetics Society about cable transmission mechanisms"
            loading="lazy">
          <figcaption>Sharing practical cable-transmission design with the Prosthetics Society.</figcaption>
        </figure>
      </section>

      <section class="about-subsection" aria-labelledby="languages-heading">
        <h3 id="languages-heading">Languages</h3>
        <p>Language learning is one of the ways I connect with people and cultures beyond engineering:</p>
        <ul>
          <li><strong>English, Hindi, and Marathi:</strong> fluent</li>
          <li><strong>Russian:</strong> advanced/native</li>
          <li><strong>Japanese:</strong> intermediate; JLPT N4 certified, with N3 understood</li>
        </ul>
      </section>
    </div>
  </section>

  <section class="about-accordion">
    <h2>Contact</h2>
    <div class="project-description-content">
      <ul>
        <li>
          <strong>Email:</strong>
          <a href="mailto:harshadmm10131@gmail.com">harshadmm10131@gmail.com</a>
        </li>
        <li>
          <strong>GitHub:</strong>
          <a href="https://github.com/HarshadmM">HarshadmM</a>
        </li>
        <li>
          <strong>LinkedIn:</strong>
          <a href="https://www.linkedin.com/in/harshadmm">Connect with me</a>
        </li>
      </ul>
    </div>
  </section>
</div>
