---
layout: page
title: CVAE based Motion Planning
description: 
img: /assets/img/CVAE/omnicvae.png
importance: 2
category: Academic
related_publications: 
---

### Intro:
Using CVAE to generate samples for motion planning. Input includes start, goal, and the workspace. Output is the non-unifrom sample generation.
Find the code [here](https://github.com/vishwas-hegde/Robot-Motion-Planning/tree/main/Motion%20Planning%20with%20CVAE)
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
        <img src="/assets/img/CVAE/decodersol.png" alt="Image 1" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Solution with CVAE Samples</figcaption>
    </figure>
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/rrtstarsol.png" alt="Image 2" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Solution with RRT* Sample</figcaption>
    </figure>
</div>
</center>

#### Results for Omni-directional Robot
<center>
<div style="display: flex; justify-content: center; gap: 20px;">
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/omnicvae.png" alt="Image 1" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Solution with CVAE Samples</figcaption>
    </figure>
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/rrtstaromni.png" alt="Image 2" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Solution with RRT* Sample</figcaption>
    </figure>
</div>
</center>

#### Time and Cost Comparision for Point Robot
<center>
<div style="display: flex; justify-content: center; gap: 20px;">
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/cvaevprmpoint.png" alt="Image 1" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Computation Time Comparision</figcaption>
    </figure>
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/Costcomparepoint.png" alt="Image 2" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Cost to Goal Comparision</figcaption>
    </figure>
</div>
</center>

#### Time and Cost Comparision for Omni-directional Robot
<center>
<div style="display: flex; justify-content: center; gap: 20px;">
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/omnitimecompare1.png" alt="Image 1" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Computation Time Comparision</figcaption>
    </figure>
    <figure style="text-align: center;">
        <img src="/assets/img/CVAE/omnicostcompare.png" alt="Image 2" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">Cost to Goal Comparision</figcaption>
    </figure>
</div>
</center>


---


