---
title: "Confidence-Aware Object Capture for a Floating-Base Manipulator"
collection: projects
toc: true
date: 2023-04-25
permalink: /projects/confidence-aware/
period: Jan. 2023 - May 2023
abstract: <b><i>Research project participated @ CUHK-Shenzhen RAIL.</i></b>  My final year project proposed a control framework for manipulator grasping objects under base disturbance. However, the success rate is limited due to a lack of confidence evaluation of object motion prediction. This project aims to fill this gap by introducing confidence analysis. Plus, we are pursuing a physical demonstration with a real robot.  
excerpt: "<img src='image/confidence.gif' width='600px'>"
course: false
---

{% include base_path %}

* Resaerch project participated at CUHK-Shenzhen robotics & AI lab
* Sept. 2022 -- May 2023
* Supervisor: [Prof. Huihuan Alex Qian](https://sse.cuhk.edu.cn/en/faculty/qianhuihuan)
* Project Mentor: [Ruoyu Xu](https://xuruoyuroy.github.io/) (Ph.D. Candidate)
* Keywords: *object capture*, *floating-base manipulator*, *motion planning*, *confidence analysis*

## Introduction

This project is the follow-up of my [final year project](/projects/floating-manipulator/). Although the feasibility, the control framework proposed in my final year project has a limited success rate because
* _**it lacks a proper evaluation matric of capture timing:**_ we simply predicted the target's position one second later and planned the capture trajectory accordingly, however, "one second later" may not be the best capture timing
* _**it does not consider the prediction confidence of the wavelet network:**_ the wavelet network won't always give us accurate predictions
* _**it does not guarantee that the planned capture trajectory is executable for the manipulator:**_ the dynamic performance of the manipulator may be insufficient to execute the planned trajectory

In this project, we solved the above problem by introducing confidence analysis in the control framework. In the refined **confidence-aware** control framework, we consider both prediction confidence and manipulator dynamic constraints when planning capture trajectories. Plus, we made intensive optimization so that the framework can meet the **real-time** requirement.

To the best of our knowledge, this is the first work demonstrating feasibility of a manipulator to capture a target subject to quasi-periodic base disturbance. Experiments showed our framework can achieve a 0.2 second respond time and a 80% capture success rate.

![confidence-capture](/images/confidence.gif)

This work was summerized as a jounral paper and submitted to IEEE Transactions on Robotics (T-RO). More details of this project will be revealed after the publication process.

## Publication Ongoing

Ruoyu Xu, **Zixing Jiang**, Beibei Liu, Yuquan Wang, and Huihuan Qian, “Confidence-Aware Object Capture for a Manipulator Subject to Floating-Base Disturbances”, Submitted to IEEE Transactions on Robotics (T-RO). 2023. <font color="red">(under review)</font>


## Related
Another [project](/projects/uav-landing/) related to [manipulator-assisted UAV landing](https://arxiv.org/abs/2212.12196).

![usv](/images/USV.png)