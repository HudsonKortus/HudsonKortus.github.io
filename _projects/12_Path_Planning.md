---
layout: page
title: RRT* Paths and Minimum Snap Trajectory 
description: 
img: assets/img/Project_Card/RRT_Path.jpg
importance: 12
category: work
giscus_comments: false
featured: true 
---

Path planning is a vital step in robot autonomy.  In this project, we implement an RRT* path planner to find an efficient path in a large 3D environment. Next, we develop a minimum snap trajectory planner to convert the path into a smooth trajectory dynamically feasible by our aerial robot. We run this trajectory through a cascading controller to get the robot control input and tune the entire system to achieve fast, reliable trajectory generation and execution.

Below is a video of our path planner and trajectory planner on a simulated environment and a simulated drone with fully simulated dynamics. 

<div id="row" style="text-align: center;">
  <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 70%; margin: 0 auto 20px auto;">
    <iframe style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"
            src="https://www.youtube.com/embed/okSVnTHA5Ng"
            frameborder="0" 
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
            allowfullscreen>
    </iframe>
  </div>
</div>

<div class="PDF">
    <iframe class="pdf" 
                    src="https://hudsonkortus.github.io/assets/pdf/p2a_group8.pdf">
    </iframe>
</div>
