---
layout: default
author_profile: true
---

<div style="text-align: center; max-width: 600px; margin: 0 auto 40px;">

I'm a 2nd Year CS Master's student at USC specializing in **3D Perception** and **Sim-to-Real Robotics**. 

This site showcases my projects, research, and technical explorations in robotics and AI.

If you have any questions

</div>

{% for project in site.projects %}
  <article style="margin-bottom: 30px;">
    {% if project.image %}
      <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" style="max-width: 100%; height: auto; margin-bottom: 15px;">
    {% endif %}
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
