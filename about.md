---
layout: default
title: About
permalink: /about/
---

<section class="about">
  <div class="container">
    <div class="about__header">
      <h1>About me</h1>
      <p>{{ site.description }}</p>
    </div>

    <div class="about__body">
      <div class="about__bio">
        <div class="prose">
          {{ site.about_bio | markdownify }}
        </div>

        <h2 class="about__subhead">Education</h2>
        <ul class="about__edu" role="list">
          <li><strong>M.S., Mechanical Engineering</strong> — Carnegie Mellon University, 2025 – present</li>
          <li><strong>B.S., Mechanical Engineering (Robotics and Mechatronics)</strong> — Virginia Tech, 2019 – 2025</li>
        </ul>

        <h2 class="about__subhead">Skills</h2>
        {% include skills-grid.html %}

        <div class="about__social">
          <a href="{{ '/resume/' | relative_url }}">Resume</a>
          {% for social in site.social_links %}
          <a href="{{ social.url }}" target="_blank" rel="noopener noreferrer">
            {% include icons/{{ social.icon }}.html %}
            {{ social.label }}
          </a>
          {% endfor %}
        </div>
      </div>

      {% if site.avatar and site.avatar != "" %}
      <div class="about__avatar">
        <img src="{{ site.avatar | relative_url }}" alt="Portrait of {{ site.title }}">
      </div>
      {% endif %}
    </div>
  </div>
</section>
