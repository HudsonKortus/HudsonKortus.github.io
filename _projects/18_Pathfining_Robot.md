---
layout: page
title: Pathfinding Autonomous Robot
description:
img: assets/img/Project_Card/TurtuleBot.jpg
importance: 18
category: work
featured: true 
---

<p>
For Unified Robotics IV, I worked with a team of 3 to program a turtle bot capable of navigating and mapping an arbitrary maze, and then using that map to navigate to any location. We programmed the turtle bot using ROS and utilizing SLAM for mapping. Once a map was built we used a Monte-Carlo Particle filter to localize as we navigated our newly created map.
</p>



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/TurtuleBot.png" title="example image" class="img-fluid rounded z-depth-2" %}
        <div class="caption">
            TurtuleBot navigating Maze
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/turtleBotInMaze.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            TurtleBot autonomously mapping maze using slam 
        </div>
    </div>

</div>


<p>
The turtle bot's only external sensor was an extremely noisy LIDAR sensor. Noisy LIDAR data can be combined with less noisy motor encoder data using a Kalman Filter to get a better estimate of the maze.The LIDAR continuously updates the configuration space (area the turtle bot can fit through) and unknown frontiers we want the turtle bot to explore. As the turtle bot exports new areas, the configuration space grows and the frontiers shrink. Once the turtle bot as explored all frontiers, it saves the Maze as a map that can be used later.
</p>


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/Rviz2.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Rviz displaying C space, known walls, and unknown space
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/turtleBotInMaze2.jpeg" title="example image" class="img-fluid rounded z-depth-1"%}
        <div class="caption">
            TurtleBot navigating maze
        </div>
</div>

<p>Using the map, the turtle bot can be picked up and placed anywhere in the maze, localize itself, and navigate to any other area. It does this with a Monte-Carlo particle filtering where random particles are spawned into the known map. The program then compares each particle's sensor states with the real ones, and then reproduces more particles based on how closely they match the real sensor states.</p>
