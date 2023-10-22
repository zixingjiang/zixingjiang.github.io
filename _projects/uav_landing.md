---
title: "Precise Landing of UAV on Disturbed Aquatic Surface Platforms"
collection: projects
permalink: /projects/uav-landing/
period: Sept. 2020 - Sept. 2021
abstract: <b><i>Research project participated @ CUHK-Shenzhen RAIL.</i></b> This project developed a novel tethered landing method that makes the UAV capable of landing on a small disturbed platform. This project also designed a capture system to implement the proposed tethered landing method.  
excerpt: "<img src='image/landing.png' width='600px'>"
course: false
date: 2022-10-05
toc: true
---

{% include base_path %}

* Research project participated at CUHK-Shenzhen Robotics & AI Lab. 
* Sept. 2020 -- Sept. 2021
* Supervisor: [Prof. Huihuan Alex Qian](https://sse.cuhk.edu.cn/en/faculty/qianhuihuan)
* Project Mentor: [Chongfeng Liu](https://chongfengliu.github.io/) (Ph.D. Candidate)
* Keywords: *UAV landing*, *mechanical design*

## Introduction

Landing unmanned aerial vehicles (UAVs) precisely on small marine platforms, which suffer from wave disturbance, is a challenging task. If landing purely by the UAV itself, there are high requirements for state estimation as well as UAV flight control algorithms to predict and track the passive irregular motion of the platform under wave disturbance. 

In this project, we designed a set of auxiliary mechanisms to help UAVs land. Inspired by [kites](https://en.wikipedia.org/wiki/Kite), we proposed a novel **tethered landing** method: _When landing, the UAV throws a roped block, and the platform captures the block, creating a tethered connection between the UAV and the platform. Afterward, the UAV retrieves the rope to help to land._ The complete landing process is demonstrated by the figure below. 


![tethered](../image/tethered-landing.gif)

To implement the proposed tethered landing method, we fabricated a set of mechanisms including a winch system deployed on UAV and a magnetic catcher deployed on the platform. The winch system is used to throw and retrieve the roped block. The bottom of the block has a metal sheet attached to it so that it can be attracted by the magnetic catcher. The magnet arrangement on the catcher is optimized to provide the largest possible magnetic attraction and magnetic field area with limited weight and volume (check [the paper](https://ieeexplore.ieee.org/document/9812270) for more details). After the block is attached to the magnets, the alignment mechanism on the catcher aligns the block to the center of the catcher and locks it in place to create a firm tethered connection. The system overview is shown below. 

![system](../image/system.png)

## Applications

The proposed landing method is promising for single/multiple UAV marine platfroms. 

![landing](../image/landing.png)

Besides, we applied the tethered landing method to design an end effector for our [manipulator-assisted UAV landing](https://arxiv.org/abs/2212.12196) project. 

![usv](/images/USV.png)




## Demonstration

Here is a video demonstrating how the proposed tethered landing method works.

<div style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe src="/files/uav-landing.mp4" style="position: absolute; width: 100%; height: 100%; border: none;" sandbox="" allowfullscreen></iframe>
</div>

## Publication
- Chongfeng Liu, **Zixing Jiang**, Ruoyu Xu, Xiaoqiang Ji, Lianxin Zhang, and Huihuan Qian, "Design and Optimization of a Magnetic Catch System for Precise UAV Landing on Disturbed Aquatic Surface Platform", _2022 IEEE International Conference on Robotics and Automation (ICRA)_, IEEE, 2022, pp. 1162-1168. <a href="https://ieeexplore.ieee.org/document/9812270"><i class="fas fa-fw fa-file-pdf zoom" aria-hidden="true"></i></a>

## Related
Other projects related to [manipulator-assisted UAV landing](https://arxiv.org/abs/2212.12196):
- [Control of the Multi-joint Manipulator for Grasping on Water Surface](/projects/floating-manipulator/)
- [Confidence-Aware Object Capture for a Floating-Base Manipulator](/projects/confidence-aware/)