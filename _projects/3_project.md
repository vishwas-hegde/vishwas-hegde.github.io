---
layout: page
title: LQR Control for Drone
description: 
img: /assets/img/lqr/catch.jpg
importance: 4
category: Academic
related_publications: 
---

### Intro:
This project focuses on the development of a quadrotor control system designed to intercept unauthorized UAVs using Linear Quadratic Regulation (LQR). The goal is to design a controller that enables a quadrotor to detect, track, and capture an intruding UAV within a defined airspace. The system incorporates advanced state estimation techniques, such as the Kalman filter, for real-time tracking and trajectory prediction. By minimizing the cost function involving state and control input penalties, the LQR controller optimizes performance in terms of precision and efficiency. The final design ensures that the quadrotor can autonomously intercept the UAV and return to base with minimal energy usage and maximum control precision.

Find the code [here](https://github.com/vishwas-hegde/RBE502_UAV_Interceptor/tree/main)
<center>
<img src="/assets/img/lqr/catch.jpg" height="300px">
</center>

### LQR Controller Design

1. **Cost Function Design**  
   The LQR controller's cost function was carefully designed to balance state errors (position and velocity) and control inputs (thrust and torques), ensuring a smooth, efficient interception maneuver.

2. **State Variables**  
   State variables, including position, velocity, and heading of both the quadrotor and the intruding UAV, were selected to provide comprehensive feedback for the controller.

3. **Weighting Matrices**  
   The weighting matrices for the state and control input terms were tuned to prioritize position tracking accuracy and energy efficiency, adjusting penalties on state deviations and control efforts.

4. **Tuning Process**  
   The Q-matrix (state penalty) and R-matrix (control input penalty) were iteratively adjusted through simulation, gradually refining the controller's performance for optimal tracking and minimal overshoot.

5. **Simulation & Iteration**  
   Various test scenarios with different initial conditions and UAV trajectories were simulated to fine-tune the LQR parameters, ensuring robust performance in realistic, dynamic environments.
