---
layout: page
title: Task-Priority Kinematic Control System for a Mobile Manipulator
description: Hands-On Intervention
img: assets/img/12.jpg
importance: 1
category: work
related_publications: true
---

This project describes the design and implementation of a **kinematic control** system for a **differential-drive robot (Kobuki Turtlebot 2)** equipped with a **4 DOF manipulator (uFactory uArm Swift Pro)**. The system utilizes the **Task-Priority Redundancy Resolution Algorithm** to manage the robot’s redundant degrees of freedom and to prioritize tasks based on their importance.

The objective of this project is to enable the **Kobuki Turtlebot** and its manipulator to perform various tasks while ensuring that higher-priority tasks are executed first. The system focuses on managing multiple tasks efficiently in a simulated environment, with potential for real-world applications in autonomous robotics. The implementation was done using the **Robot Operating System (ROS)** and validated within the **Stonefish simulator** to test control strategies and task execution.

## Methodology
The project followed several key steps in implementation:
- **Kinematic Modelling:** Developed a kinematic model for both the **Kobuki Turtlebot 2** and the **uFactory uArm Swift Pro**, enabling precise motion control and task execution.
- **Task-Priority Redundancy Resolution:** Applied the **task-priority redundancy resolution** algorithm to prioritize tasks effectively and manage the robot’s redundant degrees of freedom. Higher-priority tasks were executed first while still managing lower-priority ones.
- **Behavior Trees:** Implemented **behavior trees** to manage task complexity, ensuring smooth task transitions and better system control. Behavior trees systematically handle multiple tasks while maintaining the overall robustness of the system.
- **ROS and Stonefish Simulation:** Leveraged the **ROS framework** to implement the control algorithms and used the **Stonefish simulator** for testing and validation of the system. The simulator provided a robust environment to test various task scenarios before transitioning to potential real-world applications.

## Results
The system was rigorously tested in the **Stonefish simulator**, where the **Kobuki Turtlebot 2** and **uFactory uArm Swift Pro** successfully executed a variety of tasks. The **task-priority redundancy resolution algorithm** ensured that the most important tasks were always given precedence, while the use of **behavior trees** effectively managed the complexity of the task transitions.

The video below showcases the system in action, demonstrating the implementation of the **kinematic control system** using the **task-priority redundancy resolution algorithm** for the mobile manipulator.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.liquid path="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Example YouTube Video" class="img-fluid rounded z-depth-1" width="560" height="315" caption="This is an example caption for the video." %}
    </div>
</div>

The simulation results, supported by the demonstration video, highlight the effectiveness of the **task-priority redundancy resolution** algorithm in managing the robot’s control system, offering a flexible and scalable solution for mobile manipulator tasks.

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
