---
layout: page_project
title: Autonomous Exploration in 3D environment
description: Planning, TARE global planner, Falco local planner
img: assets/gif/project_5/intro_2.gif
importance: 1
category: course
---

Collaborator(s): Atharva Patwe


<div class="row justify-content-sm-left">
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/leopt4/turtlebot_exploration_planning">:floppy_disk: Code</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/leopt4/turtlebot_exploration_planning/blob/main/documents/HOP_Report.pdf">:memo: Report</a>
    </div>
</div>

---

This project aims to deal with the **autonomous exploration** task in intricate three-dimensional (3D) environments to a turtlebot platform using onboard sensors - Depth Camera and Lidar. In terms of global planner, we use Technologies for Autonomous Robot Exploration [(TARE)](https://www.cmu-exploration.com/tare-planner) planner while we apply [(Falco)](https://frc.ri.cmu.edu/~zhangji/publications/JFR_2020.pdf): Fast likelihood-based collision avoidance without a prior map for local planner, which were developed by CMU. In experiments, our systems autonomously explore environments at a high degree of complexity, with **StoneFish** simulator and **Kobuki** turtlebot robot.

## Methodology
While implementing the mentioned methodology, two ROS nodes were developed. - Global Planner, Local Planner. The overall architecture is depicted in the figure below. 

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_5/architecture.png" title="architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Planner node architecture.
</div>

I. Lidar Plugin 
   
   Initially, we intended to use a depth camera for the system to obtain a 3D point cloud. However, during development, we encountered problems synchronizing depth camera data and estimated state of the robot, so we decided to use lidar as a sensor for the system. Since lidar provides 2D data while the system evolves with 3D, we further developed this plugin, which helps convert lidar’s 2D data into 3D data. Basically, the plugin extends the obtained 2D point cloud in the Z direction to get elevation data. This is a situational solution, suitable for lab testing environments. Currently, we are still looking for a solution to synchronize depth camera data and robot status. 
<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_5/laserPlugin.png" title="laserPlugin" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The red line is the Lidar measurement while white point cloud is output of the Lidar plugin.
</div>

II. Global Planner 
   
   Global planner is calculated every 1 second and sends next way point to local planner. Output of the local planner is presented below is output of the glocbal planner. 
<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_5/path 1.png" title="global path" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_5/global path.png" title="global path" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    (Left) The white point cloud is sensor scan; The red point cloud is collision extracted from sensor scan; The green point cloud is frontier; The colored point cloud on the ground is candidate viewpoints, viewpoints which are brighter color are considered to see more frontier; The green cubes are selected viewpoints; The green line is local path. (Right) Green cubes are subspace in the global planner; The green line connecting all subspace and local planning horizon is the global path
</div>

III. Local Planner 
   
   The path groups are pre-generated offline, and a voxel grid is used for collision checks. The correspondences between voxels and paths are pre-established and stored in an adjacency list. During operation, perception sensor data points are processed to label occluded paths. The algorithm then selects the path group with the highest probability $P(x_B\|x_s)$. The computational complexity of the online processing algorithm is O(mnh), where m is the number of perception sensor data points, n is the number of paths in a path group, and h is the number of path groups. Result of the local planner is showed in Figure 10.

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_5/local path.png" title="Local Path" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The green point cloud is collision; The red point cloud on the ground is feasible path from local planner..
</div>

## Results
<iframe width="960" height="540" src="https://www.youtube.com/embed/pbIP6ElIu-U" title="Viettel Kamikaze Drone project. Launch and Attacking features" frameborder="0" style="border: 0px solid #bbb; border-radius: 10px; width: 100%;" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Personal Contribution and Future Directions
My role in this project is to understand TARE and Falco planner as well as the package implemetation. From that, I applied these planners and package to StoneFish simulator, fine-tuned system parameters. The project provided me with a comprehensive knowledge in TARE path planning which utilizes a hierarchical framework to improve exploration efficiency. The experience honed my abilities in problem-solving, innovative thinking, and collaborative research, preparing me for a promising career in path planning for robotics.

The TARE planner works with a 3D omni-directional sensor such as 3D lidar. In terms of future direction, we are developing the planner working a depth camera. In order to deal with it, field of view, waypoints allocation strategy should be modified.