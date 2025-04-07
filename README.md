# Multi-policy-approach-for-damage-reduction
A Multi-policy Approach Based on Clustering for Minimizing the Damage on a Falling Ballbot

Fall resilience remains a significant challenge for robots capable of locomotion. In the case of humanoid robots, arms can be utilized to mitigate impact damage, thereby improving resilience to falls. Although previous work has primarily focused on damage reduction strategies for legged robots, the question of minimizing fall damage in humanoid ballbots remains largely unexplored. In this paper, we introduce a novel multi-policy approach, combining clustering on the initial pose and Reinforcement Learning, to reduce damage resulting from a fall in a commercial humanoid ballbot. We conduct simulations to compare our method against three baselines: (1) a curriculum learning policy, (2) a single-policy approach enhanced by clustering information, and (3) a standard single-policy baseline. Experimental results demonstrate that our approach achieves higher success rates and greater damage reduction compared to existing alternatives.

***
We here present some videos to better understand the behaviour of our approach.

The video folder contains recordings of different initial poses, illustrating the performance of the policies analyzed in the paper compared to a free-fall scenario (i.e., no actions applied).

* Pose 0: In this initial pose, all considered policies, with the sole exception of the curriculum learning approach, result in lower contact forces compared to the free-fall scenario.

* Pose 1: In this initial pose, the multi-policy approach successfully reduces contact forces compared to the free-fall scenario, whereas the other policies fail to do so.

* Pose 3: This initial pose represents a failure case, where the applied policy leads to higher contact forces than the free-fall scenario.

The table below presents the mean of the maximum contact forces for each policy in different initial poses.

| Initial Position | Free Fall  | Multi-policy        | Single-policy         | Single-policy        | Curriculum   |
|                  |   (N)      | with Clustering (N) | with Cluster Info (N) | w/o Cluster Info (N) | Learning (N) |
|------------------|------------|---------------------|-----------------------|----------------------|--------------|
|  Pose 0          | 4970       | 1311                | 2037                  | 2498                 | 6354         |
|  Pose 1          | 3392       | 1470                | 5165                  | 5192                 | 4055         |
|  Pose 2          | 5090       | 7153                | 11349                 | 13834                | 9118         |

## Naming convention

The files follow this naming convention:
(policy)_(initial pose)

where the policies are named as:
* multipolicy stands for the multi-policy approach;
* singlepolicyclustering stands for the single-policy approach with clustering information;
* singlepolicy stands for the single-policy approach without clustering information;
* curriculum stands for the curriculum learning approach;
* freefall stands for the approach without any action applied.
