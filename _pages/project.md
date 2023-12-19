---
layout: archive
title: "Selected Projects"
permalink: /projects/
author_profile: true
toc: true
---

Here is a showcase of some of my previous and ongoing projects. This page may be outdated since I don't update it frequently. 

{% include base_path %}


## Research & Final Year Projects
---

{% assign sortedProjects = site.projects | sort: 'date' | reverse %}

{% for post in sortedProjects %}
  {% if post.course == false %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


## Course Projects
---

{% for post in sortedProjects %}
  {% if post.course == true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Toy Project

For learning purpose, I'm currently working on a codebase focusing on basic robotics algorithms. Reference: [PythonRobotics](https://github.com/AtsushiSakai/PythonRobotics).