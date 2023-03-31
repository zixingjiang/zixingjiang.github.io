---
layout: archive
title: "Selected Projects"
permalink: /projects/
author_profile: true
toc: true
---
<!-- # Selected Projects -->

Here is a showcase of some of my previous and ongoing projects. You can view the project profiles through the links. Please note that this page is not updated frequently. If you want to keep track of my latest activities, you may check my [GitHub](https://github.com/zixingjiang).

<!-- Here I list some of my previous and ongoing projects. You can view the project profiles via the links. _PS: The project list may not always be up to date as I usually put projects here after I get a demo_.

:heavy_exclamation_mark: Some profiles on this page are not completed yet. Working on ... -->

<!-- :pushpin: This page is still under construction. There are some profiles that have not been completed yet. I will finish them at my spare time.  -->

{% include base_path %}


## Research & Final Year Projects
---
{% for post in site.projects%}
  {% if post.course == false%}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}


## Course Projects
---

{% for post in site.projects%}
  {% if post.course == true%}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}

## Toy Project

I'm currently working on a codebase focusing on basic robotics algorithms. Reference: [PyhtonRobotics](https://github.com/AtsushiSakai/PythonRobotics).