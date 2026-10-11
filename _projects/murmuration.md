---
layout: page
title: Murmuration
description: Flocking simulation created with compute shaders
img: assets/img/project/murmuration_thumb.png
importance: 3
category: school
---

<iframe
  src="https://drive.google.com/file/d/178fGEuo2hGYPteX3Lrp5EZfVW7C8n0AG/preview"
  style="width: 100%; aspect-ratio: 16 / 9; border: 0;"
  class="rounded z-depth-1"
  allow="autoplay"
  allowfullscreen>
</iframe>


<a href="https://github.com/edpaley/IMDM327-Final" target="_blank" class="btn btn-sm z-depth-0" role="button" style="border: 1px solid; margin-right: 6px;">
  <i class="fa-brands fa-github"></i> Code
</a>



For my final, I propose Murmuration, a single-user virtual reality experience. I’ve always
loved birds. After growing up with screeching birdy siblings, I sometimes wonder how. My
family’s parrots, Tommy and Gandy, are up at the crack of dawn every day, yelling and banging
for their breakfast veggies. They get jealous of each other and will hold a grudge. Last winter, I
watched a movie with Gandy on my lap. Later, when I was putting them to bed, Tommy
punished me, biting my finger hard. Over a year later, she is still getting reparations, ever since
that night she poops on my shoulder when I’m home. They have personalities and moods, just
like people. Unlike squirrels, deer, and other animals I see regularly, birds feel like individuals,
each with their own routine, home, and family. It’s why flocks amaze me. I’m used to talking to
Gandy or seeing a sparrow or two hopping around outside, but when an incomprehensible
number of crows fly overhead, I have to stop and watch. My goal for Murmuration was to
capture the awe inspired by the largest of flocks on Earth.

The core architecture of the titular murmuration–the flock–is built upon a Boids
simulation. Each boid, or bird in this case, relies on the positions and velocities of nearby birds.
As in a standard boid simulation, birds interact through three rules: cohesion, separation, and
alignment. Unlike previous projects I’ve worked on, optimization was one of the highest
priorities to capture the sheer number of birds. I wrote the boid logic as a compute shader kernel
so that many threads could run in parallel. Additionally, at the beginning of each frame, boids are
sorted into cubic cells, and each boid only performs distance checks on adjacent cells. Each bird
is displayed as a 32x32 texture particle using Unity’s VFX Graph package. I used ShaderGraphs
to create a circular ground plane and blend between it and a URP dynamic skybox texture. The
VR rig was quite simple since it was a headset-only experience, requiring nearly no modification
from the default XR rig.

My biggest discovery this semester was the compute shader. I feel that it had a huge
impact on my Unity skill tool belt. It also just made me feel like I was cheating the system,
unlocking a secret that makes iterating through objects faster and the impossible possible. I
didn’t find it to be too difficult either; it really does seem like the possibilities are endless.
Towards the end of the project, I began to look into VFX Graphs, which were even more
intuitive due to the node-based interface. The sample scene showed awesome potential, and I
will definitely continue to explore it.
