---
title: "Online Actor-critic Reinforcement Learning Control for Uncertain Surface Vessel Systems with External Disturbances"
collection: publications
category: Journal Articles
permalink: /publication/2022-03-01-paper-OAC-RL-USV-ED
# excerpt: 'This paper is about the number 2. The number 3 is left for future work.'
date: 2022-01-03
venue: 'International Journal of Control, Automation and Systems, Vol. 20, No. 3, pp. 1029-1040, 2022.'
# slidesurl: 'http://academicpages.github.io/files/slides2.pdf'
paperurl: 'https://link.springer.com/article/10.1007/s12555-020-0809-7'
# citation: 'Your Name, You. (2010). &quot;Paper Title Number 2.&quot; <i>Journal 1</i>. 1(2).'
---

This article addresses a trajectory tracking control approach for an uncertain surface vessel using the new cascade structure of adaptive reinforcement learning (ARL) algorithm and kinematic controller, feed-forward term. Since a surface vessel is decoupled by kinematic sub-system and dynamic sub-system, the cascade control system is an ideal method for obtaining the tracking problem. In the proposed control structure, the dynamic control loop is designed to be the optimized method of the corresponding dynamic sub-system and the kinematic control loop is implemented by a nonlinear controller combining with feed-forward term. The online actor-critic architecture is considered in ARL algorithm to overcome the challenge of solving the Hamilton-Jacobi-Bellman (HJB) equation. Additionally, the proposed controller is able to handle the difficulty of the non-autonomous optimal control problem by designing the ARL technique for the corresponding system with a small number of state variables. Based on theoretical analysis, the ARL based control design has been made to guarantee the uniformly ultimately bounded (UUB) stability of the closed system. Finally, the simulation results are illustrated to verify the effectiveness of the proposed control scheme.