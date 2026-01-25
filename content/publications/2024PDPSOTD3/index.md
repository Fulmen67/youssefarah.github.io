---
title: "TD3-based trajectory optimization for energy consumption minimization in UAV-assisted MEC system"
authors: 
- me
- Bofan Yang
- Jun Zhang
- Chao Xu
- Yong Chen
- Yanxiang He
date: 2024-11-17T18:00:43+08:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2024-12-01T18:00:43+08:00

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Computer Networks,Volume 255,2024,110882"
publication_short: ""

abstract: Unmanned Aerial Vehicle (UAV) assisted Mobile Edge Computing (MEC) systems provide substantial benefits for task offloading and communication services, especially in situations where traditional communication infrastructure is unavailable. Current research emphasizes maintaining communication quality while minimizing total energy consumption and optimizing UAV flight trajectories. However, several issues remain:First, the energy consumption objective function lacks comprehensiveness, neglecting the impact of UAV flight energy consumption; second, an effective Deep Reinforcement Learning (DRL) algorithm has not been employed to address the non-convexity of the objective function; third, there is insufficient discussion regarding the practical significance of the proposed approach. To address these issues, this paper formulates an objective function aimed at minimizing MEC energy consumption by considering task offloading decisions, communication delays, computational energy consumption, and UAV flight energy consumption. We propose a Population Diversity-based Particle Swarm Optimization-Double Delay Deep Deterministic Policy Gradient (PDPSO-TD3) algorithm to find the optimal solution, enhance UAV flight trajectories through optimized offloading decisions, ensure efficient communication, and minimize the total energy consumption of the MEC system. Furthermore, we discuss the practical applicability of PDPSO-TD3 in detail and present the proposed scheme. Experimental results demonstrate that compared to the Deep Deterministic Policy Gradient (DDPG) algorithm, for transmission delay, MEC energy consumption, UAV flight energy consumption, and User Equipments (UEs) access rate metrics. The proposed PDPSO-TD3 algorithm can improvement the performance by about 14.3%, 10.1%, 6.1%, and 3.3%, respectively.

# Summary. An optional shortened abstract.
summary: ""

tags: 
- 论文
- Deep Reinforcement Learning
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

links:
  - type: pdf
    url: https://www.sciencedirect.com/science/article/abs/pii/S138912862400714X

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
