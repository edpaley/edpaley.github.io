---
layout: page
title: Stairactals
description: Recursive staircases where every step becomes a staircase of its own, built with Blender Geometry Nodes.
img: assets/img/project/depth2.png
importance: 2
category: school
related_publications: false
---

<a href="https://github.com/edpaley/Stairactals/releases/latest" target="_blank" class="btn btn-sm z-depth-0" role="button" style="border: 1px solid; margin-right: 6px;">
  <i class="fa-solid fa-download"></i> Download
</a>
<a href="https://github.com/edpaley/REPO_NAME" target="_blank" class="btn btn-sm z-depth-0" role="button" style="border: 1px solid;">
  <i class="fa-brands fa-github"></i> Code
</a>

<iframe
  src="https://www.youtube.com/embed/VIDEO_ID"
  style="width: 100%; aspect-ratio: 16 / 9; border: 0; margin-top: 1rem;"
  class="rounded z-depth-1"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
  allowfullscreen>
</iframe>
<div class="caption">
    Depth animating from 0 to 2 in the interpolated version.
</div>

## Overview

Fractal Stairs is a procedural staircase generator built with Blender Geometry Nodes. Starting from a simple flight of stairs, the system recursively replaces each step with a smaller staircase of its own, and each of those steps with another, producing a self-similar form that becomes more intricate with every level of depth.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project/depth0.png" title="Depth 0" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project/depth1.png" title="Depth 1" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project/depth2.png" title="Depth 2" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Depth 0, 1, and 2 with 5 steps. Each level turns every step into a staircase of its own.
</div>

## Two Versions

**Standard:** Depth is a whole number. Each increment adds a full level of recursion, subdividing every step into a new staircase.

**Interpolated:** Depth is a float. Fractional values blend between recursion levels, so the next generation of steps grows smoothly out of the previous one instead of appearing all at once. This makes depth animatable: keyframing it produces a staircase that continuously unfolds into finer detail.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project/interpolated.png" title="Interpolated depth" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project/modifier-panel.png" title="Modifier panel" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: depth 0.5 in the interpolated version, with the next level of steps partially formed.<br>
    Right: all parameters are exposed in the modifier panel.
</div>

## How It Works

The node tree builds a base staircase, then repeatedly places scaled copies of that staircase onto each step, with the depth input controlling how many times this happens. Length, width, steps, and depth are exposed in the modifier panel, so the structure can be adjusted without opening the node tree.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project/node-tree.png" title="Node tree" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Geometry Nodes tree.
</div>

## Get It

The .blend file, setup instructions, and parameter reference are available on [GitHub](https://github.com/edpaley/REPO_NAME){:target="_blank"}.

**Tools:** Blender, Geometry Nodes
