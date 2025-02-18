---
layout: page_project
title: Feature-based SLAM using an EKF
description: Hands-On Localization
img: assets/gif/project_6/demo_2.gif
importance: 6
category: work
related_publications: false
---

Collaborator(s):


<div class="row justify-content-sm-left">
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/patweatharva/ROS-LLM/tree/more_contrib_pi/">:floppy_disk: Code</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/patweatharva/ROS-LLM/blob/more_contrib_pi/documents/report.pdf">:memo: Report</a>
    </div>
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://www.youtube.com/watch?v=zJ5sWc6eFO8">:clapper: Demo Videos</a>
    </div>
</div>

---

This project explores the implementation of **Feature-Based SLAM** (Simultaneous Localization and Mapping) using an **Extended Kalman Filter (EKF)** to localize a **differential drive mobile robot** in a simulated environment. SLAM is a core challenge in robotics, enabling a robot to construct a map of its surroundings while simultaneously estimating its position within that map.

In this implementation, **point features** in the environment are used to estimate both the robot's state and the environment’s map. The project employs **input displacement** and **constant velocity motion models** to address the SLAM problem. Observed features are stored in **2D Cartesian space**, while **Iterative Closest Neighbors Nearest (ICNN)** is applied for **data association**, ensuring that observed features are correctly matched with previously mapped landmarks.

# Methodology

- **Extended Kalman Filter (EKF)**: The EKF is used as a recursive estimator to predict the robot’s state and update the estimate based on observed environmental features. The filter's ability to handle noisy sensor data makes it an essential part of the SLAM process.
- **Motion Models**: Both **input displacement** and **constant velocity** motion models were used to simulate the robot's movement. These models help estimate the robot's state as it navigates through the environment.

- **Feature Observation**: Environmental features were observed in **polar space** but stored in **Cartesian space**. This method provided flexibility in handling different observation models, allowing the system to adapt to changing environments.

- **Data Association with ICNN**: The **ICNN** algorithm was implemented for data association, ensuring that observed features are correctly matched with previously identified landmarks. This association is critical for improving the accuracy of the SLAM system and avoiding incorrect mapping of features.

# Results

The **FEKF SLAM algorithm** was tested in simulation to assess its robustness in solving the SLAM problem for a differential drive robot. The results showed that the algorithm efficiently handled prediction and updates while incorporating new features to refine the localization over time.

The integration of the **EKF** with feature-based SLAM enabled the robot to map its environment more accurately, even without prior knowledge of the surroundings. The system consistently improved localization accuracy with each iteration, providing reliable performance in mapping unknown environments.

# Demonstration

Below are visual demonstrations of the **Feature-based SLAM** system in action. The left image shows the robot's localization results in simulation, while the right image highlights the system performing **feature-based SLAM** with the **EKF algorithm**.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/gif/project_6/demo.gif" title="Simulation result showing robot localization with EKF" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_6/Figure_2.png" title="Feature-based SLAM in action with EKF algorithm" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: Simulation result showing robot localization with EKF. Right: Feature-based SLAM in action with the EKF algorithm.
</div>

<!-- # Conclusion
The implementation of **Feature-Based SLAM using EKF** demonstrates a solid foundation for advancing SLAM in autonomous robots. The integration of feature observations, motion models, and data association with **ICNN** helped to enhance the mapping accuracy and localization in environments without prior map knowledge. This approach lays the groundwork for solving more complex SLAM problems and paves the way for further research and development in autonomous navigation. -->