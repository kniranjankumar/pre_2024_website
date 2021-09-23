---
layout: page
title: 	Graph-based Cluttered Scene Generation and Interactive Exploration using Deep Reinforcement Learning
description: Robotics
img: /assets/img/real_clutter.jpg
---

We introduce a novel method to teach a robotic agent to interactively explore cluttered yet structured scenes, such as kitchen pantries and grocery shelves, by leveraging the physical plausibility of the scene. We propose a novel learning framework to train an effective scene exploration policy to discover hidden objects with minimal interactions.
First, we define a novel scene grammar to represent structured clutter. Then we train a Graph Neural Network (GNN) based *Scene Generation* agent using deep reinforcement learning (deep RL), to manipulate this *Scene Grammar* to create a diverse set of stable scenes, each containing multiple hidden objects.
Given such cluttered scenes, we then train a *Scene Exploration* agent, using deep RL, to uncover hidden objects by interactively rearranging the scene. 

<div class="col three caption">
<iframe width="560" height="315" src="https://www.youtube.com/embed/T2Jo7wwaXss" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

# Grammar Rules

Below is a list of all the grammar rules used in our experiments (7 objects)
<img src="{{ site.baseurl }}/assets/img/grammar_rules.png" alt="Grammar Rules" width="800"/>

<!-- <div class="img_row">
    <img class="col three left" src="{{ site.baseurl }}/assets/img/grammar_rules.png" alt="" title="Grammar Rules" style="height:864px;width:768px" />
</div> -->
<!-- ![Image](/assets/img/grammar_rules.png) -->

## Links:

1. 14 object dataset source: [https://www.turbosquid.com/3d-models/3d-model-supermarket-shelves-pack-pasta/1089057](https://www.turbosquid.com/3d-models/3d-model-supermarket-shelves-pack-pasta/1089057)

    @misc{kumar2021graphbased,
        title={Graph-based Cluttered Scene Generation and Interactive Exploration using Deep Reinforcement Learning}, 
        author={K. Niranjan Kumar and Irfan Essa and Sehoon Ha},
        year={2021},
        eprint={2109.10460},
        archivePrefix={arXiv},
        primaryClass={cs.RO}
    }