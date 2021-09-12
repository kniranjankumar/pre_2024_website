---
layout: page
title: 	Graph-based Cluttered Scene Generation and Interactive Exploration \\using Deep Reinforcement Learning
description: Robotics
img: /assets/img/real_clutter.jpg
---

We address the problem of teaching a robotic agent to interactively explore cluttered, yet structured scenes, such as kitchen pantries and grocery shelves, by leveraging clues about the physical plausibility of the scene. We propose a novel scene grammar to represent structured clutter and train Graph Neural Network (GNN) based Scene Generation Agent using deep reinforcement learning (deep RL), that can manipulate this scene grammar to create a diverse set of stable scenes with multiple hidden objects. Given such cluttered scenes, we then train a Scene Exploration Agent using deep RL to uncover hidden objects by interactively rearranging the scene. We demonstrate the generalization capabilities of our agents and provide quantitative comparisons that show the effectiveness of our approach over random and occupancy distribution minimization based exploration techniques. We also provide evidence of sim-to-real transfer by testing our exploration policy, learned in simulation, with a real UR10 robot.