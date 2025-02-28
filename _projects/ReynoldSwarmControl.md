---
layout: page_project
title: Controlling a Swarm of Robots using Reynolds’ Rules
description: Multi-robot Systems - Formation Control
img: assets/gif/project_7/intro.gif
importance: 4
category: course
related_publications: false
---

Collaborator(s): Tanakrit Lertcomepeesin, Fatima Yousif, Vania Katherine Mulia, Sawera Yaseen

<div class="row justify-content-sm-left">
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/leopt4/ReynoldsSwarm.git">:floppy_disk: Code</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/leopt4/ReynoldsSwarm/blob/main/documents/Report.pdf">:memo: Report</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://www.youtube.com/embed/xKt4voA955M">:clapper: Demo Videos</a>
    </div>
</div>

---

In this exciting project undertaken at the University of Zagreb, our team of four master’s students in Intelligent Field Robotic Systems, including myself, leveraged **Craig Reynold**’s behavioral rules to control a robot swarm within a **2D simulator Stage**. The implementation begins with integrating basic Reynold’s rules such as Separation, Alignment, and Cohesion, followed by additional rules such as Navigation to a certain point and Obstacle avoidance. The robots simulated in the Stage simulator are omnidirectional points, that are evaluated in various maps to analyze their behavior across different environments.

## Innovations and Challenges
We embarked on implementing and enhancing Reynolds’ rules—Cohesion, Separation, and Alignment—introducing sophisticated navigation and obstacle avoidance capabilities to the swarm. The challenge was not just in the algorithmic design but in ensuring that these behaviors worked in harmony to simulate natural, flock-like movements in the robots. Through meticulous programming and simulation within the **ROS framework** and **Stage simulator**, we achieved a dynamic system capable of navigating complex environments with unprecedented coordination and efficiency.

Technical Highlights: Our project’s novelty lies in the intricate balance between foundational flocking behaviors and the advanced algorithms developed for navigation and obstacle avoidance. We conducted extensive simulations across diverse maps, from obstacle-laden courses to intricate mazes, to test the adaptability and robustness of our swarm algorithms. Through these tests, we fine-tuned the algorithms for real-world applicability, addressing potential field versus steer-to-avoid methods for obstacle navigation, and experimenting with prioritized acceleration allocation to manage the swarm’s collective movements effectively.

<div class="row justify-content-sm-center">
    <div class="col-sm-11 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_7/software architecture.png" title="Software Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Software Architecture.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-11 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_7/combining Acc.png" title="Combining Acc" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Acceleration Allocation Strategy.
</div>


## Results
The results in the Stage simulator:
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_7/allignment.gif" title="allignment" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_7/separation.gif" title="separation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_7/cohesion.gif" title="cohesion" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    On the left, Allignment behavior. Middle, Separation behavior. Right, Cohesion behavior.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_7/navigation.gif" title="navigation" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_7/potential_field_editted.gif" title="potential field" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_7/steer_to_avoid_editted.gif" title="steer to avoid" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    On the left, Navigation behavior. Middle, Obstacle avoidance (potential field) behavior. Right, Obstacle avoidance (steer to avoid) behavior. 
</div>

Analysis their behavior across different environments:
<iframe width="960" height="540" src="https://www.youtube.com/embed/xKt4voA955M" title="Controlling a Swarm of Robots in 2D Simulator Stage using Reynolds’ Rules" frameborder="0" style="border: 0px solid #bbb; border-radius: 10px; width: 100%;" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Impact and Future Directions
This project is a significant step towards realizing the potential of swarm robotics in practical applications, from search and rescue operations to autonomous agricultural management. The insights gained from our simulations provide valuable guidelines for transitioning these algorithms from virtual to physical robots, opening new avenues for research and development in swarm intelligence.

As we look to the future, our next phase involves hardware implementation to validate these algorithms’ efficiency in physical environments. This transition from simulation to real-world application represents not just a technical challenge but an opportunity to revolutionize how we perceive and utilize autonomous robotic systems in society.

## Personal Contribution
My role in this project spanned algorithm development (obstacle avoidance behavior), simulation testing, and data analysis, providing me with a comprehensive skill set in robotic systems design and teamwork. The experience honed my abilities in problem-solving, innovative thinking, and collaborative research, preparing me for a promising career in robotics and autonomous system development.