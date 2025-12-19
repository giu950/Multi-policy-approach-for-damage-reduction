# Multi-policy Approach for Damage Reduction

## A Multi-policy Approach Based on Clustering for Minimizing the Damage on a Falling Ballbot

This repository contains supplementary material videos for the paper:

> **Buzzetti, G., Aractingi, M., Zappetti, D., & Iacca, G. (2025).**  
> *A Multi-policy Approach Based on Clustering for Minimizing the Damage on a Falling Ballbot.*  
> In **Proceedings of the 11th International Conference on Control, Decision and Information Technologies (CoDIT 2025)**,  
> Split, Croatia.  
> *(Proceedings to be published)*

---

## Abstract

Fall resilience remains a significant challenge for robots capable of locomotion. In the case of humanoid robots, arms can be utilized to mitigate impact damage, thereby improving resilience to falls. Although previous work has primarily focused on damage reduction strategies for legged robots, the question of minimizing fall damage in humanoid ballbots remains largely unexplored.

In this paper, we introduce a novel **multi-policy approach**, combining clustering on the initial pose and Reinforcement Learning, to reduce damage resulting from a fall in a commercial humanoid ballbot. We conduct simulations to compare our method against three baselines: (1) a curriculum learning policy,(2) a single-policy approach enhanced by clustering information, and (3) a standard single-policy baseline.

Experimental results demonstrate that our approach achieves higher success rates and greater damage reduction compared to existing alternatives.

---

## Supplementary Material

This repository provides videos to support and complement the findings presented in the paper.

### Videos

The `videos/` folder contains simulation recordings corresponding to different initial falling poses. For each pose, the behavior of the proposed approach is compared against the considered baselines and a free-fall scenario (i.e., no control actions applied).

The following initial poses are included:

- **Pose 0**  
  In this configuration, all policies—except for the curriculum learning approach—achieve lower contact forces compared to the free-fall scenario.

- **Pose 1**  
  The multi-policy approach successfully reduces contact forces with respect to free fall, while the other policies fail to do so.

- **Pose 2**  
  This configuration represents a failure case, where the applied policies lead to higher contact forces than those observed in the free-fall scenario.

---

The table below reports the **mean of the maximum contact forces** (in Newtons) obtained for each policy under different initial poses.

| Initial Pose | Free Fall (N) | Multi-policy with Clustering (N) | Single-policy with Cluster Info (N) | Single-policy w/o Cluster Info (N) | Curriculum Learning (N) |
|--------------|---------------|----------------------------------|-------------------------------------|------------------------------------|-------------------------|
| Pose 0       | 4970          | 1311                             | 2037                                | 2498                               | 6354                    |
| Pose 1       | 3392          | 1470                             | 5165                                | 5192                               | 4055                    |
| Pose 2       | 5090          | 7153                             | 11349                               | 13834                              | 9118                    |

---

## File Naming Convention

Video files follow the naming convention:
(policy)_(initial pose)

where the policy identifiers are defined as follows:

- `multipolicy`: multi-policy approach based on clustering;
- `singlepolicyclustering`: single-policy approach with clustering information;
- `singlepolicy`: single-policy approach without clustering information;
- `curriculum`: curriculum learning approach;
- `freefall`: uncontrolled free-fall scenario (no actions applied).

---

## Citation

If you use this repository or its contents in your research, please cite our work as follows:

```bibtex
@inproceedings{buzzetti2025multipolicy,
  author    = {Buzzetti, Gabriele and Aractingi, Marwan and Zappetti, Daniele and Iacca, Giovanni},
  title     = {A Multi-policy Approach Based on Clustering for Minimizing the Damage on a Falling Ballbot},
  booktitle = {Proceedings of the 11th International Conference on Control, Decision and Information Technologies (CoDIT)},
  year      = {2025},
  address   = {Split, Croatia},
  note      = {Proceedings to be published}
}

