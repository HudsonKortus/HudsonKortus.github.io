---
layout: page
title: Hospital Navigation Website
description:
img: assets/img/Project_Card/Soft_Eng.png
importance: 14
category: work
giscus_comments: false
featured: true 
---

I was the lead software engineer for CS3733 (Software Engineering) with Professor Willson Wong where we built a full-stack application for Mass General Brigham hospitals in just five weeks.

We built a fully functional hospital navigation website for the Mass General Brigham hospital systems. Including google maps integration, indoor 3d maps of floorplans with directions, specialist directories, and service requests; Deploying it all on AWS for the world to use.

As the lead software engineer I led my team of 11 developers using Agile methodology, coordinating daily standups, managing sprint planning, and reviewing pull requests to ensure our codebase remained clean and functional. I also contributed directly to the frontend and backend tasks, implementing depth-first search logic, designing reusable React components, and dynamic integration with the google maps mobile app.

Beyond coding, I led Git and code quality tutorials, created a style guide and official review documentation, and supported the team with design prototypes in Figma.

We were required to take the website down at the end of the class, but below are some screenshots of the user interface as well as the user guide. Check out the repository too! <a href="https://github.com/rohan908/team-o-copy">github.com/rohan908/team-o-copy</a>

<div class="carousel-container" style="margin-bottom: 2rem;">
    <div class="carousel-wrapper" style="position: relative; width: 100%; max-width: 1000px; margin: 0 auto; cursor: pointer;" onclick="nextImage()">
        <img id="carouselImage" src="{{ '/assets/img/Projects/Soft_Eng_Carousel/1.png' | relative_url }}" alt="Hospital Navigation Screenshot" style="width: 100%; height: auto; border-radius: 8px; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
        <div style="text-align: center; margin-top: 0.5rem; color: var(--global-text-color);">
            <span id="imageCounter">1 / 5</span>
            <p style="font-size: 0.9rem; margin-top: 0.25rem;">Click image to view next</p>
        </div>
    </div>
</div>

<script>
    const images = [
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/1.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/2.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/3.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/4.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/5.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/6.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/7.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/8.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/9.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/10.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/11.png" | relative_url }}',
        '{{ "/assets/img/Projects/Soft_Eng_Carousel/0.png" | relative_url }}',
    ];
    let currentIndex = 0;

    function nextImage() {
        currentIndex = (currentIndex + 1) % images.length;
        document.getElementById('carouselImage').src = images[currentIndex];
        document.getElementById('imageCounter').textContent = `${currentIndex + 1} / ${images.length}`;
    }
</script>

<div class="PDF">
    <iframe class="pdf" 
                    src="https://hudsonkortus.github.io/assets/pdf/CS3733_final_report.pdf">
    </iframe>
</div>
