---
title: "Control of the Multi-joint Manipulator for Grasping on Water Surface"
collection: projects
toc: true
date: 2023-03-08
permalink: /projects/floating-manipulator/
period: Sept. 2022 - Dec. 2022
abstract: <b><i>Final year project @ CUHK-Shenzhen.</i></b> This project aimed to make a manipulator capable of grasping objects on the restless water surface. To reach this goal, a predictive control framework was proposed. The proposed framework was verified with MATLAB Simscape simulation.
excerpt: "<img src='image/grasp_sim.gif' width='600px'>"
course: false
---

{% include base_path %}

* Final year project at CUHK-Shenzhen. Completed with distinction. 
* Sept. 2022 -- Dec. 2022
* Supervisor: [Prof. Huihuan Alex Qian](https://sse.cuhk.edu.cn/en/faculty/qianhuihuan)
* Project Mentor: [Ruoyu Xu](https://xuruoyuroy.github.io/) (Ph.D. Candidate)
* Keywords: *floating-base manipulator*, *object catching*, *motion prediction*

## Background & Motivation

![usv](/images/USV.png)

This project aimed to design a control framework for the [Manipulator-assisted UAV Landing](https://arxiv.org/abs/2212.12196) project of the RAIL Advanced Marine Robotics Group. In the assisted landing task, the unmanned aerial vehicle (UAV) hovers near the unmanned surface vehicle (USV), and the manipulator mounted on the USV needs to overcome wave disturbances and capture the UAV, as domonstrated in the following animation.

![landing-demo](/images/usv-uav.gif)

[Prior research](https://ieeexplore.ieee.org/document/9636055) by the Advanced Robotics Group proposed a predictive control framework to predict and compensate for wave disturbances. When wave disturbances are compensated, the floating-base manipulator can be controlled as a fixed-base manipulator. However, this approach has a very high requirement of the manipulator’s dynamical performance since, from the manipulator base’s perspective, the manipulator is tracking the trajectory of the moving target, while the target motion relative to the manipulator base caused by wave disturbance is very rapid and irregular. Motivated by this situation, this project intended to lower the dynamical performance requirement by adopt the trajectory tracking manner to trajectory interception manner. 

## Objective

The goal of this object is to design a control framework that is capable to  

1. Predict the position of the target relative to the manipulator at a certain future moment.
2. Drive the manipulator to intercept the target at predicted position and predicted time.

## Methodology

To reach the goal, a control framework consists of three policies are proposed.  

- The first policy is **approach**. The purpose of this policy is to make the manipulator as close as possible to the target without collision, so as to reduce the difficulty of subsequent prediction and grasping. Fitting a minimal volume enclosing ellipsoid (MVEE) for sampled target position is utilized for this policy.

- The second policy is **motion prediction**. This policy utilizes [wavelet network](https://ieeexplore.ieee.org/document/1461429) to learn the underlying motion pattern from historical target motion data and predict target's position at a certain future moment.

- The third policy is **motion planning**. This policy utilizes LMA inverse kinematics and cubic polynomial trajectory generation to plan a grasping trajectory. The obtained trajectory is passed to the low-level joint PID controller for execution.  

Here is an overview of the whole control framework. You may check the [project slides](/files/ERG4901_Slides_Zixing.pdf) to learn more about the details. 

![usv](/images/method.png)



## Results

This project proposed a control framework and verified the framework through Simscape simulation. The base disturbances are generated according to pre-collected data about ship motion on disturbed water surface. The following is a sequential view of screenshots.

![sim](/images/sim.png)

And here is the complete video demo.

<video src="/files/grasp_sim.mov" controls="controls" controlslist="nodownload" style="max-width: 769px;">
</video>


## Related
* [Follow-up](/projects/confidence-aware/) of this project.
* Another [project](/projects/uav-landing/) related to manipulator-assisted UAV landing.


