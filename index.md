---
layout: default
---

<div class="hero-personal">
  <div class="container">
    <div class="hero-content">
      <div class="hero-info-wrapper">
        <div class="hero-text">
           <h1 class="hero-name">{{ site.author | default: "Your Name" }}</h1>
           <p class="hero-title">Robotics & Mechatronics</p>
        </div>
        
        <div class="hero-actions">
          <a href="{{ '/about/' | relative_url }}" class="btn-secondary">
            About
          </a>
        </div>
      </div>
    </div>
  </div>
</div>

<section class="projects-showcase">
  <div class="container">
    <div class="section-header">
      <h2>Featured Research Projects</h2>
      <p class="section-subtitle">Selected work in deployable robotics and haptic interaction</p>
    </div>
    
    <div class="projects-grid-featured">
      {% assign featured_projects = site.projects | where: "featured_homepage", true | sort: "date" | reverse %}
      {% for project in featured_projects %}
        <div class="project-card-featured">
          <div class="project-media">
            {% if project.featured_image %}
              <img src="{{ project.featured_image | relative_url }}" alt="{{ project.title }}" class="project-image">
            {% elsif project.models.first %}
              <div class="model-preview-small">
                <model-viewer 
                  src="{{ project.models.first.file | relative_url }}"
                  alt="{{ project.title }}"
                  camera-controls
                  auto-rotate
                  class="preview-model-small">
                </model-viewer>
              </div>
            {% else %}
              <div class="project-placeholder-small">
                <i class="fas fa-robot"></i>
              </div>
            {% endif %}
            
            <div class="project-overlay">
              <a href="{{ project.url | relative_url }}" class="project-link-overlay">
                <i class="fas fa-arrow-right"></i>
              </a>
            </div>
          </div>
          
          <div class="project-info-featured">
            <div class="project-categories-small">
              {% for category in project.categories limit:2 %}
                <span class="category-tag-small">{{ category }}</span>
              {% endfor %}
            </div>
            
            <h3 class="project-title-featured">
              <a href="{{ project.url | relative_url }}">{{ project.title }}</a>
            </h3>
            
            <p class="project-excerpt-small">{{ project.description | truncate: 80 }}</p>
            
            <div class="project-features-small">
              {% if project.models %}
                <span class="feature-badge-small" title="3D Models">
                  <i class="fas fa-cube"></i>
                  {{ project.models.size }}
                </span>
              {% endif %}
              
              {% if project.schematics %}
                <span class="feature-badge-small" title="Schematics">
                  <i class="fas fa-microchip"></i>
                  {{ project.schematics.size }}
                </span>
              {% endif %}
              
              {% if project.code_files %}
                <span class="feature-badge-small" title="Code Files">
                  <i class="fas fa-code"></i>
                  {{ project.code_files.size }}
                </span>
              {% endif %}
            </div>
          </div>
        </div>
      {% endfor %}
    </div>

    <div class="showcase-actions">
      <a href="{{ '/projects/' | relative_url }}" class="btn-primary-large">
        <i class="fas fa-th"></i>
        View All Projects
      </a>
    </div>
  </div>
</section>

<section class="homepage-recognition">
  <div class="container">
    <div class="section-header">
      <h2>Awards &amp; Milestones</h2>
      <p class="section-subtitle">Recent recognition and research presentations</p>
    </div>

    <div class="publication-list homepage-recognition-list">
      <article class="publication-card">
        <p class="publication-year">March 2026 · Winner</p>
        <h2>Hackstarter Award: Open Project</h2>
        <p class="publication-abstract"><strong>NeoAir</strong> won the Open Project award at Hackstarter 2026, the Imperial College Advanced Hackspace programme final.</p>
      </article>

      <article class="publication-card">
        <p class="publication-year">Poster presentation</p>
        <h2>Hamlyn Symposium on Medical Robotics</h2>
        <p class="publication-abstract">Presented my hybrid continuum-eversion robot research at the symposium.</p>
      </article>
    </div>

    <div class="showcase-actions">
      <a href="{{ '/publications/' | relative_url }}" class="btn-primary-large">
        <i class="fas fa-book-open"></i>
        View Publications
      </a>
    </div>
  </div>
</section>

<section class="skills-section">
  <div class="container">
    <div class="section-header">
      <h2>Technical Expertise</h2>
    </div>

    <div class="skills-grid">
      <div class="skill-category">
        <h3><i class="fas fa-cube"></i> Mechanical Design</h3>
        <div class="skill-tags">
          <span class="skill-tag">SolidWorks</span>
          <span class="skill-tag">CAD</span>
          <span class="skill-tag">3D Printing</span>
          <span class="skill-tag">Prototyping</span>
        </div>
      </div>
      <div class="skill-category">
        <h3><i class="fas fa-robot"></i> Robotics</h3>
        <div class="skill-tags">
          <span class="skill-tag">Continuum Mechanisms</span>
          <span class="skill-tag">Tendon-driven Actuation</span>
          <span class="skill-tag">Deployable Systems</span>
          <span class="skill-tag">Kinematic Modelling</span>
        </div>
      </div>
      <div class="skill-category">
        <h3><i class="fas fa-microchip"></i> Electronics &amp; Control</h3>
        <div class="skill-tags">
          <span class="skill-tag">Arduino</span>
          <span class="skill-tag">Stepper Motors</span>
          <span class="skill-tag">Motor Drivers</span>
          <span class="skill-tag">Hardware Integration</span>
        </div>
      </div>
      <div class="skill-category">
        <h3><i class="fas fa-chart-line"></i> Simulation &amp; Research</h3>
        <div class="skill-tags">
          <span class="skill-tag">MATLAB</span>
          <span class="skill-tag">Experimental Analysis</span>
          <span class="skill-tag">Technical Writing</span>
          <span class="skill-tag">LaTeX</span>
        </div>
      </div>
    </div>
  </div>
</section>
