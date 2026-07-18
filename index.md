---
layout: single
title: ""
permalink: /
author_profile: false
classes: wide
---
<!--
<div class="home-banner">
  <img
    src="{{ '/assets/images/home/banner.jpg' | relative_url }}"
    alt=""
  >
</div>
-->

<div class="home-bio">

  <div class="home-bio__photo">
    <img
      src="{{ site.author.avatar | relative_url }}"
      alt="{{ site.author.name }}"
    >
  </div>

  <div class="home-bio__text">

    <h1>{{ site.author.name }}</h1>

    {% if site.author.bio %}
      <p class="home-bio__bio">
        {{ site.author.bio }}
      </p>
    {% endif %}

    <ul class="home-author-links">

      {% if site.author.location %}
        <li>
          <i class="fas fa-fw fa-map-marker-alt" aria-hidden="true"></i>
          <span>{{ site.author.location }}</span>
        </li>
      {% endif %}

      {% if site.author.employer %}
        <li>
          <i class="fas fa-fw fa-building" aria-hidden="true"></i>
          <span>{{ site.author.employer }}</span>
        </li>
      {% endif %}

      {% if site.author.email %}
        <li>
          <a href="mailto:{{ site.author.email }}">
            <i class="fas fa-fw fa-envelope" aria-hidden="true"></i>
            <span>Email</span>
          </a>
        </li>
      {% endif %}

      {% if site.author.links %}
        {% for link in site.author.links %}
          {% if link.label and link.url %}
            <li>
              <a
                href="{% if link.url contains '://' %}{{ link.url }}{% else %}{{ link.url | relative_url }}{% endif %}"
                {% if link.url contains '://' %}
                  target="_blank"
                  rel="noopener noreferrer"
                {% endif %}
              >
                {% if link.icon %}
                  <i class="{{ link.icon }}" aria-hidden="true"></i>
                {% else %}
                  <i class="fas fa-fw fa-link" aria-hidden="true"></i>
                {% endif %}

                <span>{{ link.label }}</span>
              </a>
            </li>
          {% endif %}
        {% endfor %}
      {% endif %}

    </ul>

  </div>

</div>