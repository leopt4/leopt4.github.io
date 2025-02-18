---
layout: page_project
title: Task-Priority Kinematic Control for a Mobile Manipulator
description: Intervention, Pick and Place task
img: assets/gif/project_1/intro.gif
importance: 1
category: work
related_publications: false
---

Collaborator(s): Atharva Patwe

<div class="row justify-content-sm-left">
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/leopt4/turtlebot_taskpriority_manipulation.git">:floppy_disk: Code</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/leopt4/turtlebot_taskpriority_manipulation/blob/main/documents/HOI_report.pdf">:memo: Report</a>
    </div>
    <!-- <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://ifrosmaster.org/">:clapper: Demo Videos</a>
    </div> -->
</div>

---

This project describes the design and implementation of a **kinematic control** system for a **differential-drive robot (Kobuki Turtlebot 2)** equipped with a **4 DOF manipulator (uFactory uArm Swift Pro)**. The system utilizes the **Task-Priority Redundancy Resolution Algorithm** to manage the robot’s redundant degrees of freedom and to prioritize tasks based on their importance.

The objective of this project is to enable the **Kobuki Turtlebot** and its manipulator to perform various tasks while ensuring that higher-priority tasks are executed first. The system focuses on managing multiple tasks efficiently in a simulated environment, with potential for real-world applications in autonomous robotics. The implementation was done using the **Robot Operating System (ROS)** and validated within the **Stonefish simulator** to test control strategies and task execution.

## Methodology
The project followed several key steps in implementation:
- **Kinematic Modelling:** Developed a kinematic model for both the **Kobuki Turtlebot 2** and the **uFactory uArm Swift Pro**, enabling precise motion control and task execution.
- **Task-Priority Redundancy Resolution:** Applied the **task-priority redundancy resolution** algorithm to prioritize tasks effectively and manage the robot’s redundant degrees of freedom. Higher-priority tasks were executed first while still managing lower-priority ones.
- **Behavior Trees:** Implemented **behavior trees** to manage task complexity, ensuring smooth task transitions and better system control. Behavior trees systematically handle multiple tasks while maintaining the overall robustness of the system.
<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_1/life.png" title="Behavior tree of the pick and place task" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Behavior tree of the pick and place task.
</div>
- **ROS and Stonefish Simulation:** Leveraged the **ROS framework** to implement the control algorithms and used the **Stonefish simulator** for testing and validation of the system. The simulator provided a robust environment to test various task scenarios before transitioning to potential real-world applications.
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_1/node.png" title="Node graph" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Node graph.
</div>
## Results
The system was rigorously tested in the **Stonefish simulator**, where the **Kobuki Turtlebot 2** and **uFactory uArm Swift Pro** successfully executed a variety of tasks. The **task-priority redundancy resolution algorithm** ensured that the most important tasks were always given precedence, while the use of **behavior trees** effectively managed the complexity of the task transitions.

The video below showcases the system in action, demonstrating the implementation of the **kinematic control system** using the **task-priority redundancy resolution algorithm** for the mobile manipulator.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/project_1/intervention_simulation.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}

    </div>
</div>
<div class="caption">
    Pick and Place task result in the StoneFish simulation .
</div>

The simulation results, supported by the demonstration video, highlight the effectiveness of the **task-priority redundancy resolution** algorithm in managing the robot’s control system, offering a flexible and scalable solution for mobile manipulator tasks.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="assets/video/project_1/Intervention_turtlebot.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}

    </div>
</div>
<div class="caption">
    Pick and Place task result in the Kobuki Turtlebot robot in the laboratory environment.
</div>

