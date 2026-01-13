---
layout: page
title: Autonomous Drone Racing with Monocular Vision
description:
img: assets/img/Project_Card/Drone_Race.jpg
importance: 11
category: work
giscus_comments: false
featured: true 
---

This project challenged each team to build a fully autonomous drone capable of completing a race through an unknown obstacle course using only a single RGB camera and noisy IMU data; no depth sensing, no prior map, and no reliable visual texture. The course consisted of three rectangular racing frames followed by an irregularly shaped gap in a textured wall. Critically, the back faces of the frames and the wall were completely textureless, making conventional on device image segmentation unreliable. After passing through all obstacles (stage 1 and 2), the drone was required to rotate 360 degrees and return through the same course (stage 3).   

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/RBE595_p5_img.png" title="Project Description" class="img-fluid rounded z-depth-2" %}
        <div class="caption">
          Image of Course and obstacles navigated by drone 
        </div>
    </div>
</div>
To solve this, our team implemented a perception and navigation stack based entirely on motion cues. We combined optical flow (RAFT) with Temporally Stacked Spatial Parallax (TS2P) to infer relative depth from monocular video in real time. Rather than relying on appearance or color, the system exploited motion parallax to distinguish foreground structures from background surfaces, allowing it to detect both regular window frames and arbitrary gaps regardless of texture or background.

From the resulting flow field, we segmented navigable free space, estimated the centroid of each opening, and fed this information into a visual servoing controller. The drone aligned itself to each target and traversed it using a minimum-snap trajectory planner. This approach enabled robust navigation through textureless geometry and eliminated any dependence on explicit depth sensors or pre-mapped environments.

Our system completed the full out-and-back course in approximately 260 seconds, the third fastest time in the class, demonstrating that reliable autonomous flight through unknown, visually ambiguous environments is possible using only a single camera and motion-based perception.

<div id="row" style="text-align: center;" >
  <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 70%; margin: 0 auto 20px auto;">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
            src="https://www.youtube.com/embed/VnGCHX8Ou1Q" 
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
    </iframe>
  </div>
</div>

<div class="PDF">
  <iframe class="pdf" 
                  src="https://hudsonkortus.github.io/assets/pdf/p5_group8.pdf">
  </iframe>
</div>
