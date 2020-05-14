---
layout: page
title: Generating realistic hand manipulations
description: 
img: /assets/img/real_hand_thumbnail.png
---

We generate realistic hand manipulations of object by using a Generative Adversarial Network by conditioning on the hand and finger pose. We adopt an encoder-decoder architecture where we input a rough rendering of the skeletal pose and get a realistic rendering of a hand as the output. We generate datasets with simulated and real human arms at different poses and use it to train our model. Given an hand pose and object pose we showcase a pipeline to generate an image conditioned on the poses.



<div class="img_row">
    <img class="col one left" src="{{ site.baseurl }}/assets/img/skeleton_hand.png" alt="" title="Pose 1"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/skeleton_hand2.png" alt="" title="Pose 2"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/skeleton_hand3.png" alt="" title="Pose 3"/>
</div>
<div class="col three caption">
    Example skeletal poses that we feed in as input to the network</div>
<div class="img_row2">
    <img class="col one left" src="{{ site.baseurl }}/assets/img/real_hand.png" alt="" title="Generated Image 1"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/real_hand2.png" alt="" title="Generated Image 2"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/real_hand3.png" alt="" title="Generated Image 3"/>
</div>
<div class="col three caption">
    Generated frames from our network
<div class="img_row2">
<div class="img_row3">
    <img class="col three right" src="{{ site.baseurl }}/assets/img/hand_move.gif" alt="" title="Object Manipulation"/>
<div class="col three caption">
    Using our network we can generate a sequence of frames that showcase an object interaction
</div>

