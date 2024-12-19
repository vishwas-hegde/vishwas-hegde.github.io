---
layout: page
title: CVAE based Motion Planning
description: 
img: assets/img/conveyorgrasp/clutter_grasp-giff.gif
importance: 2
category: Academic
related_publications: 
---

### Intro:
Using CVAE to generate samples for motion planning. Input includes start, goal, and the workspace. Output is the non-unifrom sample generation.

#### Training Data:
Data obtained with optimal planners is used to train the CVAE. Only the samples of the path from start to goal are selected.

<center>
<figure style="text-align: center;">
    <div style="display: flex; justify-content: center; gap: 20px;">
        <img src="/assets/img/CVAE/input1.png" alt="Input 1" style="height:200px; width:200px;">
        <img src="/assets/img/CVAE/input2.png" alt="Input 2" style="height:200px; width:200px;">
    </div>
    <figcaption style="margin-top: 10px; font-size: 14px; color: gray;">Input Dataset</figcaption>
</figure>
</center>


#### Results for Point Robot
<center>
<div style="display: flex; justify-content: center; gap: 20px;">
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/decodersol.png" alt="Image 1" style="height:200px; width:200px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Solution with CVAE Samples</figcaption>
    </figure>
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/rrtstarsol.png" alt="Image 2" style="height:200px; width:200px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Solution with RRT* Sample</figcaption>
    </figure>
</div>
</center>


---


