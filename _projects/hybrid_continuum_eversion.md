---
layout: project
title: "Hybrid Continuum-Eversion Robot"
description: "A deployable hybrid robot combining eversion-based locomotion, rolling-contact-joint steering, and a lumen-compatible intervention end-effector for disaster medical scenarios."
date: 2026-09-01
categories: [Robotics, Mechatronics, 3D Printing]
# Add hero_gif and featured_image after placing the animated project GIF in assets.
# hero_gif: "/assets/images/projects/hybrid_robot/intro.gif"
# featured_image: "/assets/images/projects/hybrid_robot/intro.gif"
hero_gif_alt: "Hybrid continuum-eversion robot prototype"
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

## 3. Vortex-cannon end-effector

An elastically actuated vortex cannon was designed to fit inside the continuum module's central lumen. This kept the intervention tool integrated with the robot while preserving the lumen-compatible design.

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
**Institution:** Imperial College London, Hamlyn Centre for Medical Robotics
