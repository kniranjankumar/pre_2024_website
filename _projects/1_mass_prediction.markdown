---
layout: page
title: 	Mass Distribution of Articulated Objects
description: Robotics
img: /assets/img/timelapse_thumbnail.jpg
---

We explore the problem of estimating the mass distribution of an articulated object by an interactive robotic agent. Our method predicts the mass distribution of an object by using the limited sensing and actuating capabilities of a robotic agent that is interacting with the object. We are inspired by the role of exploratory play in human infants. We take the combined approach of supervised and reinforcement learning to train an agent that learns to strategically interact with the object to estimate the object's mass distribution. Our method consists of two neural networks: (i) the policy network which decides how to interact with the object, and (ii) the predictor network that estimates the mass distribution given a history of observations and interactions. Using our method, we train a robotic arm to estimate the mass distribution of an object with moving parts (e.g. an articulated rigid body system) by pushing it on a surface with unknown friction properties. We also demonstrate how our training from simulations can be transferred to real hardware using a small amount of real-world data for fine-tuning. We use a UR10 robot to interact with 3D printed articulated chains with varying mass distributions and show that our method significantly outperforms the baseline system that uses random pushes to interact with the object
<div class="img_row">
    <img class="col three left" src="{{ site.baseurl }}/assets/img/2chain_movement.png" alt="" title="Two Link" style="height:160px" />
</div>
<div class="col three caption">
<iframe width="560" height="315" src="https://www.youtube.com/embed/o3zBdVWvWZw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
    
    @misc{kumar2019estimating,
    title={Estimating Mass Distribution of Articulated Objects using Non-prehensile Manipulation},
    author={K. Niranjan Kumar and Irfan Essa and Sehoon Ha and C. Karen Liu},
    year={2019},
    eprint={1907.03964},
    archivePrefix={arXiv},
    primaryClass={cs.RO}}



