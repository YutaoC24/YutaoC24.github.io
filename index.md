---
layout: default
author_profile: true
---

<div style="text-align: center; max-width: 600px; margin: 0 auto 40px;">

I'm a 2nd Year CS Master's student at USC specializing in <strong>3D Perception</strong> and <strong>Sim-to-Real Robotics</strong>. 

This site showcases my projects, research, and technical explorations in robotics and AI.

If you have any questions

</div>

## Projects

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px;">
{% for project in site.projects %}
  <div style="border: 1px solid #ddd; padding: 20px; aspect-ratio: 1/1; display: flex; flex-direction: column; justify-content: space-between;">
    {% if project.image %}
      <div style="overflow: hidden; border-radius: 8px; margin-bottom: 15px; height: 200px;">
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}" style="width: 100%; height: 100%; object-fit: cover;">
      </div>
    {% endif %}
    <h3 style="margin: 10px 0;"><a href="{{ project.url }}">{{ project.title }}</a></h3>
    {% if project.excerpt %}<p style="font-size: 14px; margin: 0;">{{ project.excerpt }}</p>{% endif %}
  </div>
{% endfor %}
</div>

## Recent Posts

{% for post in site.posts limit:10 %}
  <article>
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <time>{{ post.date | date: "%b %d, %Y" }}</time>
    {% if post.excerpt %}<p>{{ post.excerpt }}</p>{% endif %}
  </article>
{% endfor %}
