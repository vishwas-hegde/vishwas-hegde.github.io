---
layout: page
title: Autonomous Driving Perception
description: 
img: /assets/img/computervision/autonomous/frontpage.png
importance: 3
category: Academic
related_publications: 
---

### Intro:
Building deep learning based computer vision stack for autonomous driving. The project utilizes pretrained models and KITTI dataset for inference. Visit [here](https://github.com/vishwas-hegde/Autonomous-Driving-Perception) for code.

1. **Monocular Depth Estimation**  
   Comparitive study on DepthAnything and ZoeDepth. DepthAnything provides sharper results but the output has a flickering effect.

<center>
<div style="display: flex; justify-content: center; gap: 20px;">
    <figure style="text-align: center;">
        <img src="/assets/img/computervision/autonomous/depth_output.gif" alt="Image 1" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">DepthAnything</figcaption>
    </figure>
    <figure style="text-align: center;">
        <img src="/assets/img/computervision/autonomous/depth_output_zoe.gif" alt="Image 2" style="height:200px; width:300px;">
        <figcaption style="margin-top: 5px; font-size: 14px; color: gray;">ZoeDepth</figcaption>
    </figure>
</div>
</center>
   
2. **Optical Flow**  
   NeuFlow_v2 with huggingface hub was utilized to generate optical flow.
   <center>
    <img src="/assets/img/computervision/autonomous/output_optical.gif" alt="Optical Flow" style="height:300px; width:400px;">
</center>

3. **Object Detection**
   YoloV8 was used to implement object detection.
<center>
    <img src="/assets/img/computervision/autonomous/obj_detection.gif" alt="Object Detection" style="height:300px; width:400px;">
</center>

4. **Pose Detection**
    YoloV8-Pose was implemented to detect the pose of humans.
    <center>
    <img src="/assets/img/computervision/autonomous/pose.png" alt="Pose Detection" style="height:300px; width:400px;">
</center>

