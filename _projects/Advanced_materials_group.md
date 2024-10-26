---
layout: page
title: Advanced Materials Group
description: 
img: assets/img/Projects/Advanced_Materials_Group/cover_photo.png
importance: 19
category: work
related_publications: false
featured: true 
---
In the Spring of 2024 I had the privilege to work in Professor Markus Nemitz’s advanced material group, a soft robotics lab at WPI. I worked on exploring the feasibility of pellet printing ultra soft TPE plastics. Pellet printing is an underexplored and deeply promising field of 3d printing that could greatly expand materials available like exotic impregnated PEEK’s and ultra soft TPE’s, as well as slashing costs and allow for easy recycling. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/Advanced_Materials_Group/clearing clog.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            xyz extruder extruding cleaning pellets after material clog
        </div>
    </div>

    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/Advanced_Materials_Group/messy_hotend.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Example of design flaw causing pellets to fall into hotend area 
        </div>
    </div>



</div>

Ultra soft plastics simply don't work on a conventional roll, especially plastics as soft as 0030. Instead, they need to be in pellet form like they would be before injection molding. There are a handful of hobbyist grade off the shelf pellet extruders but they are both extremely expensive and deeply flawed. These engineering flaws become apparent when trying to print the extra compliant pellets at relatively low temperatures. Heat creep, due to improper heat management, and poor extrusion control were the biggest issues. 


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Projects/Advanced_Materials_Group/cleaning_leadscrew.png" title="example image" class="img-fluid rounded z-depth-1" %}
        <div class="caption">
            Cleaning leadscrew after clog
        </div>
    </div>

    <div class="col-sm mt-3 mt-md-0">
       <video width="600" height="350" autoplay muted loop>
        <source src="https://hudsonkortus.github.io/assets/img/Projects/Advanced_Materials_Group/print_vidwo.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
        <div class="caption">
            Video of extruder printing soft fluidic linear actuator
        </div>
    </div>
</div>


My task in the lab was simple: Make 0030a TPE print well using an xyz pellet extruder on an e3d tool changer 3d printer. I performed multiple print setting studies to optimize the print temperature, speed, and fan levels to dramatically improve print quality. I redesigned the cooling on the extruder to eliminate heat creep melting the pellets in the reservoir. This further improved print quality. Unfortunately, after 7 weeks of me working in the lab, Professor Nemitz and the Advanced Materials Group moved to Tufts so I was unable to continue my redesign. I want to explore pellet printing in the future because it has the potential to revolutionize 3d printing



