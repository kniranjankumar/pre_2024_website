---
layout: page
title: 	Mass Distribution of Articulated Objects
description: Robotics
img: /assets/img/timelapse_thumbnail.jpg
---

We explore the problem of estimating the mass distribution of an articulated object by an interactive robotic agent. Our method predicts the mass distribution of an object by using limited sensing and actuating capabilities of a robotic agent during an interaction with the object. Inspired by the role of exploratory play in human infants, we take the combined approach of supervised and reinforcement learning to train an agent such that it learns to strategically interact with the object for estimating its mass distribution. Our method consists of two neural networks: (i) the policy network which decides how to interact with the object, and (ii) the predictor network that estimates the mass distribution given a history of observations and interactions. Using our method, we train a robotic arm to estimate the mass distribution of an object with moving parts (e.g. an articulated rigid body system) by pushing it on a surface with unknown friction properties. We show the robustness of our method across different physics simulators and robotic platforms. We further test our method on a real robot platform with 3D printed articulated chains with varying mass distributions. We present results that demonstrate that our method significantly outperforms the baseline agent that uses random pushes to interact with the object.
<div class="img_row">
    <img class="col three left" src="{{ site.baseurl }}/assets/img/2chain_movement.png" alt="" title="Two Link" style="height:160px" />
</div>
<div class="col three caption">
<iframe width="560" height="315" src="https://www.youtube.com/embed/pJhufIKuNcg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
    
    @misc{kumar2019estimating,
    title={Estimating Mass Distribution of Articulated Objects through Non-prehensile Manipulation},
    author={K. Niranjan Kumar and Irfan Essa and C. Karen Liu},
    year={2019},
    eprint={1907.03964},
    archivePrefix={arXiv},
    primaryClass={cs.RO}



