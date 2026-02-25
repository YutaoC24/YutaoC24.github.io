---
layout: single
title: "Control-based Motion Planning for Multi-robot-grab-and-push in Isaac Lab"
excerpt: "Demonstration of two ridge-back franka robots using a stick to manipulate object on a higher and wider platform."
image: "/assets/images/ridgebackfranka.png"
---

### Simulation Results
Below is the task and trajectory demonstration for the ridge-back franka robots.

<video width="100%" height="auto" controls autoplay loop muted playsinline>
  <source src="{{ '/assets/videos/Multi-robot-grab-and-push.mp4' | relative_url }}" type="video/mp4">
</video>

**Technical Highlight:** I implemented multi-stage control-based motion planning with built-in IK controllers in Isaac Lab for a "semi" non-prehensile task.

