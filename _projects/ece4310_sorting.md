---
title: "Intelligent Sorting with Eye-in-Hand Manipulator"
collection: projects
permalink: /projects/ece4310-sorting/
period: Spring 2022
abstract: "<b><i>Course project (individual), ECE4310 Programming for Robotics, Spring 2022 @ CUHK-Shenzhen.</i></b> In this project, I programmed a 6-DoF eye-in-hand manipulator with ROS to perform an intelligent sorting task: place small blocks into buckets of the same color as them. "
excerpt: "<img src='image/sorting.gif' width='600px'>"
course: true
date: 2022-04-13
toc: true
---

{% include base_path %}

- Course project (individual) of *ECE4310 Programming for Robotics, Spring 2022* at CUHK-Shenzhen. 
- Course Instructor: [Prof. Tin Lun Lam](https://sse.cuhk.edu.cn/en/faculty/tinlunlam)
- Keywords: *manipulator*, *visual servoing*, *pick-and-place*

## Introduction
In this project, I programmed a 6-degree-of-freedom serial manipulator ([Interbotix WidowX-250 6DoF](https://www.trossenrobotics.com/docs/interbotix_xsarms/specifications/wx250s.html)) with eye-in-hand camera
configuration to perform an intelligent sorting task: automatically places the different colored
pieces into the corresponding colored trash bins. 

![sorting](../image/sorting.png)

## Methodology

In this project, I used the [ROS MoveIt!](https://moveit.ros.org/) toolkit to implement most of the functions, including motion planning and obstacle avoidance. I used the [OpenCV](https://opencv.org/) package and HSV masks to detect and distinguish the differently colored targets. 

![hsv](../image/hsv.png)

I used linear regression for single pose eye-in-hand calibration (The robot was programmed to only observes and calculates the target position in a preset pose. Hence only the preset pose needs to be calibrated). 


$$\begin{bmatrix}x_{w}\\y_{w}\end{bmatrix} = \boldsymbol{k}^{\top} \begin{bmatrix}x_{c}\\y_{c}\end{bmatrix} + \boldsymbol{b}$$

Where $[x_{w}, y_{w}, 0]^{\top}$ is target's position in world frame, and $[x_{c}, y_{c}]^{\top}$ is target's position in camera image frame. In this project, coefficients $\boldsymbol{k}$ and $\boldsymbol{b}$ were computed by using least squares on multiple pairs of sampled target positions. 

You may check the [project report](/files/ECE4310%20Project%202%20Report%20(119010130).pdf) for more technical details. 

## Demonstration

Here is a video demo of real robots performing the sorting task.

{% include base_path %}
<video src="/files/sorting.mp4" controls="controls" style="max-width: 769px;">
</video>