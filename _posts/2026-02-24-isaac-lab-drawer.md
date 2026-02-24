---
title: "Control-based Motion Planning for Multi-robot-grab-and-push in Isaac Lab"
excerpt: "Demonstration of two ridge-back franka robots using a stick to manipulate object on a higher and wider platform."
---

### Simulation Results
Below is the training progress after 2000 iterations in Isaac Lab.

<video width="100%" height="auto" autoplay loop muted playsinline>
  <source src="{{ '/assets/videos/Multi-robot-grab-and-push.mp4' | relative_url }}" type="video/mp4">
</video>

**Technical Highlight:** I implemented multi-stage control-based motion planning with built-in IK controllers in Isaac Lab for a "semi" non-prehensile task.