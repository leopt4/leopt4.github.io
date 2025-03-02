---
layout: page_project
title: Kamikaze Drone - 2X UAV Project
description: Control - Navigation - Localization
img: assets/gif/project_8/intro.gif
importance: 1
category: work
---

<div class="row justify-content-sm-left">
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://www.youtube.com/embed/zn8sumGB-eM">:clapper: Demo Videos</a>
    </div>
</div>

---

The Kamikaze Drone project, developed by the UAV Center of Viettel High Technology Corporation between 2021 and 2023, was designed to equip the Vietnam People's Army. This drone features a compact design, the ability to launch via a simple launcher, and an operational range of 10 km. It can reach an attack speed exceeding 130 km/h while maintaining an accuracy of less than 2 meters.

## Project Overview
Designed as a fixed-wing aircraft, the kamikaze drone is optimized for high-speed movement. To ensure compactness and compatibility with a simple launcher, its wings can fold into the body during launch and extend into flight configuration once airborne. The takeoff process is demonstrated in the accompanying video.

Beyond its attack capabilities, the drone is also equipped for reconnaissance, target detection, and precision strikes. A forward-facing camera mounted on the aircraft provides real-time surveillance, transmitting live images to the Ground Control Station (GCS). This enables operators to select targets for engagement. Once a target is chosen on the GCS screen, the drone autonomously calculates and follows an optimized attack trajectory. During this phase, the camera functions as a key navigation component, assisting in trajectory planning and control to ensure precise strikes with the intended accuracy.

The aircraft's autopilot software has been developed and rigorously tested using the XPlane-11 simulation as well as on an actual aircraft system, successfully meeting the established objectives. The simulation results and real-world performance can be observed in the two videos below.

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-2 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/gif/project_8/simulations.gif" title="Attack simulation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Attack phase in X-Plane simulator.
</div>

**Deployment cycle:** During the reconnaissance phase, the user identifies the target area and selects its coordinates without requiring high precision. The drone then calculates and follows a trajectory that enables continuous observation of the area using its top-mounted camera. The live feed from the camera is displayed on the GCS screen, allowing the user to precisely identify the target within the image. Based on this selection, the drone computes the optimal attack trajectory and control signals to ensure accurate targeting.

If no target is detected within the observation area, the user can abort the attack phase and continue reconnaissance. Additionally, if the drone is not deployed for an attack and its battery is depleted, it can be safely recovered using a parachute in a designated area.

## Personal Contributions and Skills Development
As a techincal leader as well as a software engineer, based on product requirements, I created a product backlog, software architecture, specific flight phases for Kamikaze drone. Details are listed below
- **Takeoff Phase:** This phase involves sensor fusion and state estimation to detect the launch event and implement appropriate control strategies. To achieve this, I utilized sensor data from the IMU and airspeed sensor to accurately identify the launch moment. Additionally, I designed PID controllers to stabilize the drone post-launch and ensure it reaches the required altitude before transitioning to the next phase.
- **Attack Phase:** Designed a path planning system using camera data. Developed a control system for the aircraft during the attack phase to accurately strike the target with the desired precision.
- **Recovery Phase:** Calculated the parachute deployment point and the drone's trajectory before deployment to ensure recovery at the user's desired location.

This project has significantly enhanced my expertise in robotics, aircraft and software engineering, preparing me for a future at the forefront of technological innovation. There, we have an opportunity to work with fix-wing aircraft, sensors, deep know-how in aerodynamics of the plane and design path planning and controllers for a aircraft from that. Besides, I enhance my C programming skills through developing software for autopilot.   

## Results
<iframe width="960" height="540" src="https://www.youtube.com/embed/zn8sumGB-eM" title="Viettel Kamikaze Drone project. Launch and Attacking features" frameborder="0" style="border: 0px solid #bbb; border-radius: 10px; width: 100%;" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

In the last sense of the above video, the target consists of concentric circles with radius of 0.5 met, 1 met, 1.5 met and 2 met. It is clear that the kamikaze drone attacked target with accuracy 0.5-1 met.