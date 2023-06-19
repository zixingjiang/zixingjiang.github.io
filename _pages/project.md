---
layout: archive
title: "Selected Projects"
permalink: /projects/
author_profile: true
toc: true
---

Here is a showcase of some of my previous and ongoing projects. You can view the project profiles through the links. I may not update this page very often. So if you want to keep track of my latest activities, you may check my [GitHub](https://github.com/zixingjiang).

{% include base_path %}


## Research & Final Year Projects
---
<!-- {% for post in site.projects%}
  {% if post.course == false%}
    {% include archive-single.html %}
  {% endif %}
{% endfor %} -->

{% assign sortedProjects = site.projects | sort: 'date' | reverse %}

{% for post in sortedProjects %}
  {% if post.course == false %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


## Course Projects
---
<!-- {% for post in site.projects%}
  {% if post.course == true%}
    {% include archive-single.html %}
  {% endif %}
{% endfor %} -->

{% for post in sortedProjects %}
  {% if post.course == true %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Toy Project

For learning purpose, I'm currently working on a codebase focusing on basic robotics algorithms. Reference: [PythonRobotics](https://github.com/AtsushiSakai/PythonRobotics).