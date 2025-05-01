---
layout: page_project
title: Deep Reinforecement Learning for Drone Obstacle Avoidance
description: Navigation
img: assets/gif/project_10/intro.gif
importance: 1
category: work
---

<div class="row justify-content-sm-left">
    <div class="col-sm-2 mt-3 mt-md-0">
        <a href="https://github.com/leopt4/gym-pybullet-drones-obstacle-avoidance/tree/obstacle-avoidance">:floppy_disk: Code</a>
    </div>
</div>

---

Traditional methods for UAV navigation and obstacle avoidance typically rely on a sequential, cascaded approach, which often generate point cloud maps from depth images then subsequently employed for path planning and flight control. Although they provide high interpretability and precise navigation with accurate maps, their cascaded design can lead to error accumulation. Moreover, map construction and storage demand significant computational resources, which reduces frame rates and responsiveness in dynamic
environments, ultimately decreasing obstacle avoidance efficiency.

## Project Overview
Advancements in Deep Reinforcement Learning have introduced end-to-end visual navigation frameworks. These models directly map perception tocontrol, eliminating the need for intermediate mapping and storage, reducing cumulative errors and offerring better adaptability in dynamic environment.

While traditional methods require manual tuning for different environments, DRL-based systems can generalize learned behaviors to new settings after sufficient training. This adaptability may encounter diverse and unpredictable environments during operation.

Research Questions:

• Can DRL policies learn to navigate UAVs using depth-only perception and partial observability?

• How do DRL algorithms perform under realistic noise and occlusion?

• What is the effect of temporal memory (GRU) on decision-making in obstacle-rich environments?

## Methodology and Approach
<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_10/MDP.png" title="Simple block-scheme representation of MDP" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_10/Reward_shaping.png" title="Reward Shaping" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Markov Decision Process and Problem Definition.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-11 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_10/DRL_Architecture.png" title="Software Architecture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Deep Reinforcement Learning Architecture.
</div>   

## Experiments & Results
Key Insights:

• Depth-based DRL models (PPO and TD3) can learn obstacle avoidance policies effectively in simulated UAV environments.

• PPO is more stable during training, while TD3 can converge faster but is more sensitive to hyperparameters.

Preliminary Results:

• Achieved over 87% success rate in reaching target positions without collision in structured environments.

• Training reward trends show steady improvement after 2e5 timesteps with both algorithms.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_10/ep_length.png" title="Episode Length" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_10/reward.png" title="Reward" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/project_10/success_rate.png" title="Success Rate" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Training results.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_10/Path_train_map.png" title="Train map" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/project_10/Path_test_map.png" title="Test map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Drone starts from center of the map; Goal position is random around the map. The drone need to do obstacle avoidance along the way going to the goal. Green paths are success path (reach the goal) while Red paths are crash path (collision). On the left is validation, right is test.
</div>

