---
layout: project
title: "Hybrid Continuum-Eversion Robot"
description: "A deployable hybrid robot combining eversion-based locomotion, rolling-contact-joint steering, and a lumen-compatible intervention end-effector for disaster medical scenarios."
date: 2026-09-01
categories: [Robotics, Mechatronics, 3D Printing]
featured_image: "/assets/images/projects/hybrid_robot/Front%20profile.jpg"
hero_image: "/assets/images/projects/hybrid_robot/Front_%20section%20with%20lumen%20opening.jpeg"
models:
  - file: "/assets/models/hybrid-robot/hybrid-robot.glb"
    description: "Interactive CAD assembly of the hybrid robot"
gallery_groups:
  - title: "Continuum steering directions"
    layout: "cross"
    items:
      - position: "up"
        file: "/assets/images/projects/hybrid_robot/55%20deg%20upwards.jpg"
        description: "55° upward steering"
      - position: "left"
        file: "/assets/images/projects/hybrid_robot/55%20deg%20left%20turn.jpg"
        description: "55° left turn"
      - position: "center"
        file: "/assets/images/projects/hybrid_robot/Top%20view%20of%20robot%20turning%20up%20and%20left.jpg"
        description: "Top view of the robot turning up and left"
      - position: "right"
        file: "/assets/images/projects/hybrid_robot/55%20ddeg%20righht%20turn.jpg"
        description: "55° right turn"
      - position: "down"
        file: "/assets/images/projects/hybrid_robot/Downward%20bending%20continuum.jpg"
        description: "Downward continuum bend"
  - title: "Eversion drop test"
    layout: "row"
    items:
      - file: "/assets/images/projects/hybrid_robot/Eversion%20drop%20test%201.jpg"
        description: "Eversion drop test 1"
      - file: "/assets/images/projects/hybrid_robot/Eversion%20drop%20test%202.jpg"
        description: "Eversion drop test 2"
      - file: "/assets/images/projects/hybrid_robot/Eversion%20drop%20test%203.jpg"
        description: "Eversion drop test 3"
  - title: "Eversion motion videos"
    layout: "pair"
    items:
      - file: "/assets/images/projects/hybrid_robot/evrsn_bend.mp4"
        description: "Hybrid robot eversion bending test"
      - file: "/assets/images/projects/hybrid_robot/evrsn_bend2.mp4"
        description: "Second view of the eversion bending test"
      - file: "/assets/images/projects/hybrid_robot/full_loop.mp4"
        description: "Full eversion cycle"
      - file: "/assets/images/projects/hybrid_robot/vert_mvmt_cont.mp4"
        description: "Vertical movement of the continuum section"
  - title: "Inflated and uninflated full-body views"
    layout: "stack"
    items:
      - file: "/assets/images/projects/hybrid_robot/Fully%20extended%20length.jpg"
        description: "Fully extended, inflated full-body configuration"
      - file: "/assets/images/projects/hybrid_robot/Unextended%20and%20uninflated.jpg"
        description: "Unextended and uninflated full-body configuration"
  - title: "Eversion front-end comparison"
    layout: "stack"
    items:
      - file: "/assets/images/projects/hybrid_robot/everted%20front%20end.jpg"
        description: "Everted front end"
      - file: "/assets/images/projects/hybrid_robot/uneverted%20front%20end%20of%20the%20eversion%20robot.jpg"
        description: "Uneverted front end of the eversion robot"
  - title: "Robot overview and modular components"
    layout: "pair"
    items:
      - file: "/assets/images/projects/hybrid_robot/Front%20profile.jpg"
        description: "Front profile of the hybrid robot"
      - file: "/assets/images/projects/hybrid_robot/Decoupled.jpg"
        description: "Decoupled hybrid robot components"
---

## Overview

This MRes thesis investigated a hybrid robotic platform for medical applications in disaster scenarios. The system combines a pressure-driven everting body, a tendon-driven rolling-contact-joint (RCJ) steering module, and a compact vortex-cannon end-effector.

## 1. Continuum steering module

The distal continuum section uses rigid, 3D-printed PLA segments connected by rolling-contact joints (RCJs). Four tendons, routed at 90-degree intervals, steer the module while preserving a continuous central lumen for intervention tools.

| Design parameter | Value |
| --- | --- |
| Segment outer diameter | 47.6 mm |
| Central lumen diameter | 20 mm |
| Tendon pitch-circle radius | 21.51 mm |
| Joint spacing | 23.77 mm |
| Kinematic model | Nine active joints across ten segments |
| Modelled effective bending length | 213.93 mm |
| Final prototype | Eight active joints |

A piecewise constant-curvature (PCC) model was implemented in MATLAB to relate tendon displacement to bending angle, curvature, and end-effector position. It assumed rigid segments, negligible tendon stretch and friction, negligible torsion and gravity, and equal rotation across the active joints.

## 2. Eversion system

The robot deploys through a pressure-driven everting body. I designed a transitioner cap with a Reuleaux-triangle profile and three rollers arranged at 120-degree intervals to guide the material as the robot everts.

The prototype evaluation included eversion pressure and deployment tests, steering behaviour, position holding, and interaction with debris and obstacles. Position-holding tests lasted approximately three minutes in each tested direction; the observed steering range was approximately 20–30 degrees.

<figure class="hybrid-media">
  <img src="{{ '/assets/images/projects/hybrid_robot/Everting%20slo%20motion.gif' | relative_url }}" alt="Slow-motion view of the hybrid robot eversion test" loading="lazy">
  <figcaption>Slow-motion view of the eversion test.</figcaption>
</figure>

<figure class="hybrid-media">
  <img src="{{ '/assets/images/projects/hybrid_robot/top%20view%20eversion.gif' | relative_url }}" alt="Top-down view of the robot during eversion" loading="lazy">
  <figcaption>Top-down view of the eversion test.</figcaption>
</figure>

## 3. Vortex-cannon end-effector

An elastically actuated vortex cannon was designed to fit inside the continuum module's central lumen. This kept the intervention tool integrated with the robot while preserving the lumen-compatible design.

<figure class="hybrid-media">
  <img src="{{ '/assets/images/projects/hybrid_robot/slow-motion%20shot.gif' | relative_url }}" alt="Slow-motion view of the hybrid robot eversion test" loading="lazy">
  <figcaption>Slow-motion view of vortex cannon shot controlled from a base established at 3m distance from the robot tip, with tip to target distance of 8cm.</figcaption>
</figure>

Payload trials used all-purpose flour at distances of 2 cm, 5 cm, and 10 cm. The spread was sparse at 10 cm.

## Integrated system

The project brought together the pressure-driven everting body, tendon-steered continuum section, and lumen-compatible end-effector into one deployable platform for medical applications in disaster scenarios.

## My Engineering Contributions

- Designed the RCJ steering module and its CAD model.
- Designed and fabricated the eversion transitioner cap.
- 3D-printed and assembled the rigid steering segments.
- Integrated tendon routing and actuation.
- Built the PCC kinematic model and MATLAB simulation.
- Developed the lumen-compatible vortex-cannon end-effector.
- Tested and evaluated the integrated prototype.

## Technologies

SolidWorks, MATLAB, Arduino Mega 2560, RAMPS 1.4, NEMA 17 stepper motors, tendon-driven actuation, PLA 3D printing, and piecewise constant-curvature modelling.

## Thesis

**Title:** *Deployable Hybrid Continuum-Eversion Robot for Medical Applications in Disaster Scenarios*  
**Degree:** MRes Medical Robotics and Image-Guided Intervention  
**Institution:** Imperial College London, Hamlyn Centre for Robotic Surgery

## Research institute, laboratories and supervision

The thesis research was based at the [Hamlyn Centre for Robotic Surgery](https://www.linkedin.com/company/hamlyn-centre-for-robotic-surgery/posts/?feedView=all) at Imperial College London. I worked primarily with the HARMS Lab, with co-supervision from the SUPER Lab.

<div class="project-lab-affiliations" aria-label="Thesis research laboratories">
  <figure>
    <img src="{{ '/assets/images/projects/lab%20logos/Logo_HARMS_Hamlyn.png' | relative_url }}" alt="HARMS Lab logo" loading="lazy">
    <figcaption>Primary research lab: HARMS</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/images/projects/lab%20logos/SUPER%20Logo%20Lockup%20Colour.png' | relative_url }}" alt="SUPER Lab logo" loading="lazy">
    <figcaption>Co-supervising lab: SUPER</figcaption>
  </figure>
</div>

**Primary supervisor:** Professor George Mylonas  
**Co-supervisor:** Dr Joshua Brown (SUPER Lab)
