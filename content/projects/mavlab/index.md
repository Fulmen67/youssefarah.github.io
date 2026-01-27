---
title: "Optic-Flow-Based Obstacle Avoidance for Autonomous MAV Flight"
summary: "Monocular optic flow and divergence-based navigation for real-time obstacle avoidance and autonomous flight of micro aerial vehicles."
authors:
    - Youssef Farah
    - Rita Raminhos
    - Michele Bianconi
    - Federico Magri
    - Chris Chung
    - Francesco Branca
tags:
  - Computer Vision
  - Optical Flow
  - Path Planning
  - Robotics
  - Autonomous Drones
date: 2022-06-01
math: true
---

## Context and Motivation

Reliable obstacle avoidance is a fundamental challenge for **autonomous micro
aerial vehicles (MAVs)**, especially when operating with limited onboard sensing
and computation.

This project addresses autonomous navigation in cluttered environments using
**monocular vision only**, with a focus on an **optic-flow-based obstacle
detector** tightly integrated with a **lightweight navigation strategy**.
Unlike range sensors or stereo setups, monocular cameras offer low weight and
power consumption, but require perception and navigation algorithms that are
both robust and computationally efficient.

The work was developed and validated in the context of a real-world drone
competition, with full onboard execution on a Parrot AR/Bebop platform using
the **Paparazzi open-source autopilot**.

## Demo: Autonomous Obstacle Avoidance

{{< youtube 00dogg8mQJQ >}}


---

## Optic Flow for Obstacle Detection

The core perception module is based on **optic flow**, inspired by ecological
approaches to visual navigation.

Instead of explicitly reconstructing geometry, obstacle proximity is inferred
from the **divergence of the optic flow field**:

\[
D = \frac{\partial u}{\partial x} + \frac{\partial v}{\partial y}
\]

where \(u, v\) are the horizontal and vertical flow components. High divergence
values correspond to objects approaching the camera, providing a direct cue for
obstacle detection. 

The optic flow module:

- uses **FAST** corners for feature detection,
- tracks them with a **pyramidal Lucas–Kanade** implementation,
- estimates the flow field and then computes divergence from the tracked
  feature displacements.

To make the signal usable onboard a vibrating drone, I:

- normalized the divergence with the camera timestamp,
- added a **lag term** and **bias compensation** for noise,
- applied a **low-pass filter** to stabilise the detection signal.   

The final module provides a binary signal:

- **`object_detected = true`** when divergence exceeds a tuned threshold,
- **`object_detected = false`** otherwise,

which is then consumed by the navigation strategy.

---

## Design Trade-offs in Perception

We compared two main perception strategies for obstacle detection:   

- **YUV color-based filtering**  
  - Pros: simple to implement, effective for specific colored obstacles  
  - Cons: highly sensitive to lighting changes, strongly environment-specific,
    poor generalization to other obstacle types  

- **Optic flow / divergence**  
  - Pros: appearance-agnostic, works with any textured obstacle, aligns with
    biological navigation principles  
  - Cons: struggles with **texture-free obstacles** (e.g. smooth orange poles),
    requires tuning and filtering to handle vibration and noise  

Because the goal was a **general, reusable obstacle avoidance strategy**, we
ultimately chose **optic flow** as the main perception method, with the option
to augment it later with a lightweight color filter for texture-free obstacles.   

---

## Navigation Strategy

### Explored Approaches

Several navigation strategies were initially studied and traded off:   

- **Mapping + A\*/RTA\***  
  - Plans paths on a 2D grid using prior knowledge and camera feedback  
  - Offers optimal or near-optimal paths but at **high computational cost**  
  - Less suitable for non-static, partially known environments  

- **Control Barrier Functions (CBF)**  
  - Nonlinear control strategy that enforces safety constraints (obstacle
    locations) through a quadratic program  
  - Provides strong theoretical guarantees but requires accurate models and is
    **computationally heavy** for onboard execution  

- **Home–Explore strategy**  
  - Drone repeatedly explores from a “home base” and returns to it when
    encountering an obstacle  
  - Safe by construction but relatively slow and sensitive to false positives  

- **Modified Orange Avoider**  
  - Reactive strategy from the Paparazzi project, originally using color-based
    obstacle detection  
  - Low complexity, compatible with real-time constraints, and well-suited to a
    **binary obstacle signal** (like the one produced by the divergence module)  

Based on this trade-off, we selected the **Modified Orange Avoider** as the
navigation backbone, and adapted it to work with **optic-flow-based obstacle
detection** instead of color counts.   

---

### Modified Orange Avoider with Optic Flow

In the original Orange Avoider, the drone:  

- counts orange pixels in the image,
- if above a threshold, considers an obstacle detected,
- turns until the obstacle is no longer visible, then continues.

In our version, the **color-based trigger is replaced by optic-flow divergence**:

- when \(D\) exceeds a tuned threshold, `object_detected = true`,
- this triggers a reactive avoidance maneuver.

The key elements of the modified strategy are:

- **Backward retreat:**  
  Upon detecting an obstacle, the drone moves **backwards along its previous
  path** by a fraction of the traveled distance. This guarantees that it returns
  to a region known to be obstacle-free.

- **Heading change and re-check:**  
  After retreating, the drone changes its heading by a fixed angle and checks
  again for obstacles using the optic-flow-based detector. If an obstacle is
  still present, the heading is incrementally adjusted until a clear direction is found.

- **Out-of-bounds handling:**  
  If the drone reaches an out-of-bounds region, it performs a **180° turn**
  and avoids moving backwards immediately after this maneuver to prevent
  triggering auto-landing due to repeated boundary violations.   

This strategy is:

- simple enough to run in real time on limited onboard hardware,
- fully compatible with the binary divergence-based detection output,
- robust to moving obstacles and small changes in the environment layout.

---

## Testing and Validation

The complete system (optic flow + modified Orange Avoider) was validated:

- in simulation, to tune parameters such as divergence thresholds,
  retreat distance, and heading increment, and  
- in the **Cyberzoo** test environment, using real flight tests with physical
  obstacles and varying lighting conditions.   

The final setup successfully navigated the obstacle field using **monocular
vision only**, with all computation running onboard.

---

## Summary

This project presents a full **vision-based obstacle avoidance pipeline** for
autonomous MAVs that combines:

- **optic-flow-based divergence estimation** for appearance-independent obstacle
  detection, and
- a **modified Orange Avoider** navigation strategy that reacts safely and
  efficiently to detected obstacles.

By focusing on motion cues rather than explicit 3D reconstruction and coupling
perception with a lightweight, reactive navigation scheme, the system achieves
robust, real-time obstacle avoidance on resource-constrained aerial platforms.

