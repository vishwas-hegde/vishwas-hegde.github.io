---
layout: page
title: LLM based Navigation Task Planning
description: 
img: /assets/img/llm/navigation/frontpage1.png
importance: 1
category: Academic
related_publications: 
---

### Intro:
Integrating Llama 3.3 70B with ROS2 Navigation stack to generate navigation waypoint sequence based on user input. Visit [here](https://github.com/vishwas-hegde/LLM-Navigation/tree/main) for code.

<center>
    <video width="1200" height="850" controls>
        <source src="/assets/img/llm/navigation/llm_navigation_demo.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</center>



### Navigation:
I have used turtlebot 3 as the robot and implemented SLAM based on Lidar data. Nav2 package was used to navigate in the map created.

### LLM:
Major focus of the project was to integrate open source LLM with the navigation stack. After researching a bit on different models on huggingface I decided to go with Llama 3 models. Initially I hosted the Llama 3.2 1B model locally, while performance was adequate I was not able to test the 70B model. To use Llama 3.3 which is the latest release of Meta, I created AI agent with phidata and Groq. Groq could offers API keys which can be used to prompt several open source LLMs.

Initial prompt contained the approximate position of different sections of the house which would be used to generate the sequence of robot poses. The robot poses generated will be parsed using an action function to get the waypoint navigation.

The initial prompt is as follows:
"You are an AI agent providing navigation instructions to a mobile robot based on user needs.",
"The kitchen is at (9.0, -3.5, 0.0), bedroom is at (-2.0, 2.0, 0), bathroom is at (-3.0, -3.0, 0), and the hall is at (2.0, -1.5, 0).",
"When I ask you to bring something you should go to either kitchen, bedroom, or bathroom and bring the item to the hall.",
"Let's say I ask you to bring water.",
"The output instructions should be in the following format: ",
"{'move1': (9.0, -3.5, 0.0), 'move2': (2.0, -1.5, 0.0), and so on}",
"Keep the response simple and make sure to provide all the move instructions in a single dictionary {}.",

### Next Steps:
1) Introducing YOLOv11 to detect the objects in the house while mapping. 
2) Providing map and object data to LLM to create the initial prompt for navigation, eliminating the need to explicitly mention different sections of house by the user.
3) Moving to the objects rather than just the room or kitchen.
