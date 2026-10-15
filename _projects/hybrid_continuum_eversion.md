
---
layout: project
title: "Hybrid Continuum-Eversion Robot"
description: "A deployable hybrid robot combining eversion-based locomotion, rolling-contact-joint steering, and a lumen-compatible intervention end-effector for disaster medical scenarios."
date: 2026-09-01
categories: [Robotics, Mechatronics, 3D Printing]
---

## overview:
    title: "Project Overview"
    description: "This MRes thesis investigated the design, fabrication, integration, and experimental evaluation of a hybrid robotic platform for medical applications in disaster scenarios. The system combines a pressure-driven everting body, a distal tendon-driven rolling-contact-joint steering module, and a compact vortex-cannon end-effector."

## system_architecture:
  ### eversion_based_deployment:
    description: "The robot uses a pressure-driven everting body for deployment. A transitioner cap incorporating a Reuleaux-triangle geometry and three rollers arranged at 120-degree intervals was developed to facilitate eversion."

  ### rolling_contact_joint_steering:
    description: "The distal steering module consists of rigid, 3D-printed PLA segments connected by rolling-contact joints (RCJs). Four tendons routed at 90-degree intervals provide directional steering while preserving a continuous central lumen."
    specifications:
      segment_outer_diameter: "47.6 mm"
      central_lumen_diameter: "20 mm"
      tendon_pitch_circle_radius: "21.51 mm"
      joint_spacing: "23.77 mm"
      kinematic_model: "Nine active joints across ten segments"
      modelled_effective_bending_length: "213.93 mm"
      final_prototype: "Eight active joints"

  ### intervention_end_effector:
    description: "An elastically actuated vortex cannon was designed to fit inside the steering module's central lumen."
    test_payload: "All-purpose flour"
    test_distances:
      - "2 cm"
      - "5 cm"
      - "10 cm"
    observation: "Sparse spread was observed at 10 cm."

## kinematic_modelling:
  method: "Piecewise constant-curvature (PCC) model"
  software: "MATLAB"
  modelled_parameters:
    - "Tendon displacement"
    - "Bending angle"
    - "Curvature"
    - "End-effector position"
  ### assumptions:
    - "Rigid segments"
    - "Negligible tendon stretch and friction"
    - "Negligible torsion and gravity"
    - "Equal rotation across active joints"

## experimental_evaluation:
  ### tests:
    - "Evaluated eversion pressure and deployment performance."
    - "Measured steering behaviour and directional movement."
    - "Conducted position-holding tests of approximately three minutes in each tested direction."
    - "Evaluated interaction with debris and obstacles."
    - "Tested vortex-cannon payload spread at multiple distances."
    - "Integrated and experimentally evaluated the hybrid robotic prototype."
  steering_performance: "Approximately 20–30 degrees"

## engineering_contributions:
  - "Mechanical design and CAD of the rolling-contact-joint steering module."
  - "Design and fabrication of the eversion transitioner cap."
  - "3D printing and assembly of the rigid steering segments."
  - "Tendon routing and actuation integration."
  - "PCC kinematic modelling and MATLAB simulation."
  - "Development of a lumen-compatible vortex-cannon end-effector."
  - "Experimental testing and evaluation of the integrated prototype."

## technologies:
  - "SolidWorks"
  - "MATLAB"
  - "Arduino Mega 2560"
  - "RAMPS 1.4"
  - "NEMA 17 stepper motors"
  - "Tendon-driven actuation"
  - "PLA 3D printing"
  - "Piecewise constant-curvature modelling"

## thesis:
  title: "Deployable Hybrid Continuum-Eversion Robot for Medical Applications in Disaster Scenarios"
  degree: "MRes Medical Robotics and Image-Guided Intervention"
  institution: "Imperial College London"
  research_centre: "Hamlyn Centre for Medical Robotics"