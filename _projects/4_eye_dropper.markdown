---
layout: page
title: Automatic Eye Dropper
description: 
img: /assets/img/eye_dropper_thumbnail.png
---

About 3 million Americans have glaucoma and a significant portion of them are the elderly who need help to take their eye drop medication. We design an automated eye-dropper that detects the patients eye, adminsters the eye drop and registers if the adminstration was successful. We modify a head-mounted display for this purpose and add an onboard computer that deals with the control processes.
<div class="img_row">
    <img class="col two left" src="{{ site.baseurl }}/assets/img/eye_dropper_thumbnail.png" alt="" title="eye1"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/eye_dropper_side.png" alt="" title="eye1"/>
</div>
<div class="col three caption">
    Open-Box cardboard prototype of our device. Top-view of the eye from the device(Left) Camera looks at the eye from the side(Right)</div>
<h3>Eye Region Detection</h3>
<br/>
To detect the patient's eye record a clip of the patient moving their eye. Because of the controlled nature of our setup we can compute the variance of the sequence of images and segment out the eye region. The variance can be color thresholded to give us a segmentation of the eye region. An example of the mean and variance is shown in the figure below.


<div class="img_col">
    <img class="row three left" src="{{ site.baseurl }}/assets/img/mean_eye.png" alt="" title="Mean of frames"/>
    <img class="row three right" src="{{ site.baseurl }}/assets/img/variance_eye.png" alt="" title="Variance of frames"/>
</div>
<div class="col three caption">
    Mean of the image sequence we get from the camera(Top). Variance of the image sequence(Bottom)</div>

<div class="img_row">
    <img class="col one left" src="{{ site.baseurl }}/assets/img/eye1.png" alt="" title="eye1"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/eye2.png" alt="" title="eye2"/>
    <img class="col one left" src="{{ site.baseurl }}/assets/img/eye3.png" alt="" title="eye3"/>
</div>
<div class="col three caption">
    Example cropped eye region images</div>
<h3>Blink Detection</h3>
<br/>
We want to detect eye blinks of the patient so that we can plan when to administer the eye drop and know if it was successfully delivered. To detect blinks we collect videos from 25 patients with three different eye colors at three different illumination conditions. We have a total of 75 videos each 200 frames long. We automatically annotate the frames(as open/close) by asking the participants to actively open or close their eyes and synchronizing the commands with the realtime video sequence. We crop out the eye region and train a classifier to classify each frame as open or close. We train this classifier using the annotated videos we collected and successfully detect blinks.
<h3>Eye drop tracker</h3>
<br/>
To control when and how much eye drops will be dispensed we design a motorized setup that can be controlled by the on-board computer. We 3D print the device and fix it on the head mounded device. We position the illumination such that the light from the LEDs gets total internally reflected and enters the camera. This illuminates the drop making it look as a bright white streak in the image. If we fit a line to this image using Hough Transform we get the trajectory of the water drop as shown in the figure below.
<div class="img_row">
    <img class="col three left" src="{{ site.baseurl }}/assets/img/waterdrop_hough.png" alt="" title="hough Lines"/>
</div>
<div class="col three caption">
    Trajectory of a water drop detected using Hough Line detection</div>

