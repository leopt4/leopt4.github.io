---
layout: page
title: Formation Control of Multi-Robot Systems Using Consensus Protocols
description: Multi-robot Systems - Formation Control 
img: assets/gif/project_2/4_agents_lab.gif
importance: 2
category: work
giscus_comments: false
---

Collaborator(s): Tanakrit Lertcomepeesin, Fatima Yousif, Vania Katherine Mulia, Sawera Yaseen



<div class="row justify-content-sm-left">
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://ifrosmaster.org/">:floppy_disk: Code</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://ifrosmaster.org/">:memo: Report</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://ifrosmaster.org/">:clapper: Demo Videos</a>
    </div>
</div>

---
This pioneering project by a dedicated team of five master’s students, including myself, delves into the development and implementation of **consensus protocol-based** strategies for the robust coordination and formation control of multi-robot systems. Focusing on rendezvous and formation control, we crafted a software framework utilizing graph theory for dynamic robot swarm control. My contributions spanned from conceptualization to implementation, including algorithm development, simulation and laboratory testing, and analytical evaluation. This project not only honed my skills in robotics and software development but also highlighted my ability to collaborate effectively and drive innovation in complex multi-robot systems.

## Methodology

- Developed and implemented advanced **consensus protocols** for multi-robot coordination, emphasizing rendezvous and formation control.
- **Flocking** behaviors were designed based on **Reynolds Rules** including speration and obstacle avoidance behaviors.
- Utilized graph theory for intricate network modeling, enabling structured swarm control in both distributed and semi-distributed settings.
  
<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_2/software_architecture_1.jpeg" title="software architecture" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_2/software_architecture_2.jpeg" title="software architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Software Architecture.
</div>
The project architecture shown in the figure above illustrates the implementation of a control system for coor-dinating multiple crazyflies in formation, combining elements of perception, formation control, and consensus-based protocols. The architecture follows a ROS pattern with multiple nodes communicating.
The high-level system architecture has a crazyflies simulation node that handles simulation provided by CrazySim,map server for providing map data and a central crazyflies node that integrates all these components making our system centralized and flexible.

The internal architecture of the crazyflies node includes a Perception module that processes neighbor information (as previously explained in part 1 of this project), adjacency matrix calculations from both neighbors and topology, a Formation control system with configurable formation types (Rectangle, Triangle, Line, Rendezvous implemented), similar to part 1, a Reynolds rules implementation for flocking and Consensus algorithms for coordinated movement followed by publishing velocity commands

The system was developed in Python and implemented within the **Robot Operating System (ROS2)** framework. Preliminary testing and system tuning were carried out in the **Sphero** and **CrazySim** simulation environment, with further validation performed in laboratory environment using **crazyflies** robots.

## Results
Video results from simulation and real robot demonstrate the protocols’ efficacy in achieving precise formation control and obstacle avoidance, underscoring the potential of consensus protocols in enhancing distributed robotic systems in real-world scenarios.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_2/flocking.gif" title="Flocking behavior" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_2/Rendezvous.gif" title="Rendezvous problem" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_2/FormationControl.gif" title="Consensus protocol" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The results in the CrazySim simulator. On the left, Flocking behavior. Middle, Rendezvous problem. Right, Consensus protocol.
</div>


<div class="row">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_2/3_agents_lab.gif" title="3 robots" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_2/4_agents_lab.gif" title="4 robots" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    The consensus based formation control results with CrazyFlies robots in the laboratory environment. On the left, 3 robots; Right, 4 robots.
</div>

## Impact and Future Work
Our research significantly advances the understanding and application of consensus protocols in swarm robotics, with potential implications for autonomous exploration, synchronized tasks, and efficient spatial organization. The project sets a foundation for future exploration into hardware implementations and real-world applications, promising substantial contributions to robotics and distributed control systems.