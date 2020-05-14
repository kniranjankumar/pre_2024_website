---
layout: page
title: Motion Textures
description: 
img: /assets/img/meshwarp_thumbnail.jpg
---

With the advent of mobile cameras the number of photographs take every year has exploded. It has been estimated that at least 1.2 trillion photos will be taken in 2017. Although photographs are static, frozen instances of time, we often associate movement with certain elements contained in it. For example, if a waterfall is contained in the image, we can’t help but supplement it with the dynamic flowing motion of water. 
Elements such as waterfalls, clouds, smoke and fire have a unique pattern of movement that could often be looped around to create a continuous infinite video. These video clips can be viewed as textures in time or motion textures. Being able to generate motion textures out of static images would let people to selectively animate parts of a photograph, enriching it to create a pleasant viewing experience.

<h3>Mesh manipulation</h3>
<br/>
To create consecutive frames of the image we deform it by deconstructing the image region as a mesh and perturbing the vertices of the mesh.


    1. Get user input to segment the region of interest
    2. Get user input for motion direction
    3. Interpolate across the motion region to generate a flow field
    4. Select a set of points such that they lie in the motion region
    5. Move the mesh points in the direction specified by the flow field.
    6. Interpolate new triangle pixels from the triangles in the original image


<div class="img_row">
    <img class="col two left" src="{{ site.baseurl }}/assets/img/meshwarp.jpg" alt="" title="Waterfall Mesh"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/spline_waterfall.png" alt="" title="Waterfall Spline"/>
</div>
<div class="col three caption">
    Mesh that's used to deform the image(Left). Blue lines mark the direction of flow and red points represent the static regions of the masked image. A smooth flow field is created from this input with spline interpolation(Right)</div>

<h3>Spline Interpolation</h3>
<br/>
Another approach we tried was to use a Thin plate spline to generate a smooth flow field with typically fewer user interactions

    1. Select a few stationary and mobile marker points.
    2. Use TPS to interpolate between pixel displacement to create a smooth warp.
    3. Motion is spread over multiple frames to get a smooth transition over frames
    4. We deform the original source image everytime to get the new frames

We offer two approaches to segment the image.
<br/>
1. Interactive segmentation with grab-cut
2. CNN based image segmentation 

We showcase some of our results below
<div class="img_row">
    <img class="col two left" src="{{ site.baseurl }}/assets/img/Smoke-output.gif" alt="" title="Waterfall Mesh"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/waterfall2.gif" alt="" title="Waterfall Spline"/>
</div>
<div class="col three caption">
