---
layout: default
author_profile: true
---

<style>
.intro-section {
  text-align: center;
  max-width: 700px;
  margin: 0 auto 50px;
  line-height: 1.8;
  font-size: 1.1em;
}
.intro-section p {
  margin: 0 0 16px;
  color: #444;
}
.intro-section strong {
  color: #2a7ae2;
}
.intro-section a {
  color: #2a7ae2;
  text-decoration: none;
}
.section-title {
  font-size: 1.5em;
  margin: 40px 0 25px;
  padding-bottom: 10px;
  border-bottom: 2px solid #2a7ae2;
  display: inline-block;
}
.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 25px;
}
@media (max-width: 900px) {
  .projects-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 600px) {
  .projects-grid { grid-template-columns: 1fr; }
}
.project-card {
  border: 1px solid #e0e0e0;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  transition: transform 0.2s, box-shadow 0.2s;
  background: #fff;
}
.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(0,0,0,0.12);
}
.project-image {
  width: 100%;
  aspect-ratio: 1 / 1;
  overflow: hidden;
}
.project-image img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  background: #f5f5f5;
}
.project-info {
  padding: 16px;
}
.project-info h3 {
  margin: 0 0 8px;
  font-size: 1em;
}
.project-info h3 a {
  color: #333;
  text-decoration: none;
}
.project-info h3 a:hover {
  color: #2a7ae2;
}
.project-info p {
  font-size: 13px;
  margin: 0;
  color: #666;
  line-height: 1.5;
}
.post-item {
  margin-bottom: 20px;
  padding-bottom: 20px;
  border-bottom: 1px solid #eee;
}
.post-item h3 {
  margin: 0 0 6px;
  font-size: 1.1em;
}
.post-item h3 a {
  color: #333;
  text-decoration: none;
}
.post-item h3 a:hover {
  color: #2a7ae2;
}
.post-item time {
  font-size: 13px;
  color: #888;
}
.post-item p {
  margin: 8px 0 0;
  color: #555;
  font-size: 14px;
}
</style>

<div class="intro-section">
  <p>I'm a 2nd Year CS Master's student at USC specializing in <strong>3D Perception</strong> and <strong>Sim-to-Real Robotics</strong>.</p>
  <p>This site showcases my projects, research, and technical explorations in robotics and AI.</p>
  <p>If you have any questions, reach me at <a href="mailto:yutaocao@usc.edu">yutaocao@usc.edu</a></p>
</div>

<h2 class="section-title">Projects</h2>

<div class="projects-grid">
{% for project in site.projects %}
  <div class="project-card">
    {% if project.image %}
      <div class="project-image">
        <img src="{{ project.image | relative_url }}" alt="{{ project.title }}">
      </div>
    {% endif %}
    <div class="project-info">
      <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
      {% if project.excerpt %}<p>{{ project.excerpt }}</p>{% endif %}
    </div>
  </div>
{% endfor %}
</div>

<h2 class="section-title">Recent Posts</h2>

{% for post in site.posts limit:10 %}
  <div class="post-item">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <time>{{ post.date | date: "%b %d, %Y" }}</time>
    {% if post.excerpt %}<p>{{ post.excerpt }}</p>{% endif %}
  </div>
{% endfor %}
