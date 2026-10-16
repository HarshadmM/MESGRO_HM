---
layout: project
title: "Hybrid Continuum-Eversion Robot"
description: "A deployable hybrid robot combining eversion-based locomotion, rolling-contact-joint steering, and a lumen-compatible intervention end-effector for disaster medical scenarios."
date: 2026-09-01
categories: [Robotics, Mechatronics, 3D Printing]
---

## Overview

This MRes thesis investigated a hybrid robotic platform for medical applications in disaster scenarios. The system combines a pressure-driven everting body, a tendon-driven rolling-contact-joint (RCJ) steering module, and a compact vortex-cannon end-effector.

## System Architecture

### Eversion-based deployment

The robot deploys using a pressure-driven everting body. A transitioner cap with a Reuleaux-triangle geometry and three rollers arranged at 120-degree intervals was developed to guide eversion.

### Rolling-contact-joint steering

The distal steering module uses rigid, 3D-printed PLA segments connected by RCJs. Four tendons, routed at 90-degree intervals, steer the module while preserving a continuous central lumen.

| Parameter | Value |
| --- | --- |
| Segment outer diameter | 47.6 mm |
| Central lumen diameter | 20 mm |
| Tendon pitch-circle radius | 21.51 mm |
| Joint spacing | 23.77 mm |
| Kinematic model | Nine active joints across ten segments |
| Modelled effective bending length | 213.93 mm |
| Final prototype | Eight active joints |

### Intervention end-effector

An elastically actuated vortex cannon was designed to fit inside the steering module's central lumen. Tests used all-purpose flour as the payload at distances of 2 cm, 5 cm, and 10 cm. At 10 cm, the spread was sparse.

## Kinematic Modelling

A piecewise constant-curvature (PCC) model was implemented in MATLAB to relate tendon displacement to bending angle, curvature, and end-effector position. The model assumed rigid segments, negligible tendon stretch and friction, negligible torsion and gravity, and equal rotation across the active joints.

## Experimental Evaluation

The prototype was evaluated through tests of eversion pressure and deployment, steering behaviour, position holding, interaction with debris and obstacles, and vortex-cannon payload spread. Position-holding tests lasted approximately three minutes in each tested direction. The observed steering range was approximately 20–30 degrees.

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
