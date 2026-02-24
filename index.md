---
layout: default
author_profile: true
---

I'm a 2nd Year CS Master's student at USC specializing in **3D Perception** and **Sim-to-Real Robotics**. 

This site showcases my projects, research, and technical explorations in robotics and AI.

If you have any questions

## Projects

{% for project in site.projects %}
  <article>
    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
    {% if project.excerpt %}<p>{{ project.excerpt }}</p>{% endif %}
  </article>
{% endfor %}

## Recent Posts

{% for post in site.posts limit:10 %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <time>{{ post.date | date: "%b %d, %Y" }}</time>
    {% if post.excerpt %}<p>{{ post.excerpt }}</p>{% endif %}
  </article>
{% endfor %}
