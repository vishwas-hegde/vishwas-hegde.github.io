---
layout: page
title: Grasping from Conveyor Belt
description: 
img: assets/img/conveyorgrasp/clutter_grasp-giff.gif
importance: 1
category: Academic
related_publications: 
---

### Intro:
A Gazebo simulation to Detect, Track, Synthesize and Execute grasp for objects on a moving conveyor belt using ROS2 Humble.

<center>
<img src="/assets/img/conveyorgrasp/clutter_grasp-giff.gif" alt="Clutter Grasping Simulation" style="height:200px; width:200px;">
</center>

---

### Workflow Steps:

1. **Object Detection and Center Extraction**  
   - When an object is spawned in the workspace, the YOLO server processes the overhead camera feed.  
   - The YOLO server provides the center coordinates of the bounding box for the detected object.

2. **Object Prioritization**  
   - The center values of the detected objects (from the overhead camera) are added to a priority queue.  
   - Objects are prioritized for processing based on the queue order (e.g., first detected).

3. **Robot End-Effector Movement**  
   - The first element (highest priority object) is extracted from the queue.  
   - The robot end-effector moves to the predefined grasp window based on the object's center coordinates provided by the overhead camera.

4. **In-Hand Pose Correction**  
   - When the object appears under the in-hand camera feed, the YOLO server processes the feed and provides the object's center coordinates again.  
   - These updated center values are used to correct the pose of the robot end-effector.

5. **Grasp Execution**  
   - The robot end-effector moves down to grasp the object.

6. **Object Placement**  
   - The object is dropped into the designated bin.

7. **Home Position or Next Object**  
   - After placing the object, the robot moves:  
     - To the home position, or  
     - To the center of the next object in the queue.
