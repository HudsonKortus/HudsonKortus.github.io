---
layout: about
title: About
permalink: /
subtitle: 

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
news: false # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page
---

<p>
  My name is Hudson Kortus, I am a Senior Robotics Engineering student at Worcester Polytechnic with a highly interdisciplinary skillset and the industry experience needed to jump into a small, fast moving team, and ship projects. I am deeply passionate about tough hard-tech problems related to studying and mitigating the impacts of climate change and have the skillset to contribute to almost any team. I have designed and manufactured electro mechanical systems using both Solidworks and Onshape, created PCB’s using KiCad, and have programming experience ranging from embedded C to ROS and neural networks.
</p>
<p>
  My interdisciplinary background enables me to take projects from an early concept, through mechanical design, electrical integration, and programming. I'm comfortable working across system layers from embedded firmware running on RTOS to high-level controls and sensor perception.
</p>
<p>
  Finally this experience gives me the foundation needed to rapidly specialize when needed. Because I already have such a wide conceptual framework, I can quickly dive deep into a new topic and become an expert rapidly.
</p>

<h2>
Employers
</h2>

<!-- pages/projects.md -->
<div class="employers">

<!-- Display projects without categories -->

{% assign sorted_employers = site.employers | sort: "importance" %}

  <!-- Generate cards for each project -->

  <div class="row row-cols-1 row-cols-md-3">
    {% for employers in sorted_employers %}
      {% include employers.liquid %}
    {% endfor %}
  </div>
</div>

<h2>
Projects
</h2>


<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
{% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
