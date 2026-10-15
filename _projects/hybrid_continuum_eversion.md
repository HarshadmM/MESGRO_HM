
---
layout: project
title: "Hybrid Continuum-Eversion Robot"
description: "A deployable hybrid robot combining eversion-based locomotion, rolling-contact-joint steering, and a lumen-compatible intervention end-effector for disaster medical scenarios."
date: 2026-09-01
categories:
  - Robotics
  - Mechatronics
  - 3D Printing
featured_image: "/assets/images/projects/hybrid-eversion-robot/featured.jpg"
---

<h2>Project Overview</h2>

<p>This MRes thesis investigated the design, fabrication, integration, and experimental evaluation of a hybrid robotic platform for medical applications in disaster scenarios. The system combines a pressure-driven everting body, a distal tendon-driven rolling-contact-joint steering module, and a compact vortex-cannon end-effector.</p>

<h2>System Architecture</h2>

<h3>Eversion-Based Deployment</h3>

<p>The robot uses a pressure-driven everting body for deployment. A transitioner cap incorporating a Reuleaux-triangle geometry and three rollers arranged at 120-degree intervals was developed to facilitate eversion.</p>

<h3>Rolling-Contact-Joint Steering Module</h3>

<p>The distal steering module consists of rigid, 3D-printed PLA segments connected by rolling-contact joints (RCJs). Four tendons routed at 90-degree intervals provide directional steering while preserving a continuous central lumen.</p>

<ul>
  <li><strong>Segment outer diameter:</strong> 47.6 mm</li>
  <li><strong>Central lumen diameter:</strong> 20 mm</li>
  <li><strong>Tendon pitch-circle radius:</strong> 21.51 mm</li>
  <li><strong>Joint spacing:</strong> 23.77 mm</li>
  <li><strong>Kinematic model:</strong> Nine active joints across ten segments</li>
  <li><strong>Modelled effective bending length:</strong> 213.93 mm</li>
  <li><strong>Final prototype:</strong> Eight active joints</li>
</ul>

<h3>Intervention End-Effector</h3>

<p>An elastically actuated vortex cannon was designed to fit inside the steering module's central lumen. All-purpose flour was used as a test payload to evaluate discharge and spread at distances of 2 cm, 5 cm, and 10 cm. Sparse spread was observed at 10 cm.</p>

<h2>Kinematic Modelling</h2>

<p>A piecewise constant-curvature (PCC) model was developed to approximate the steering module's kinematics. MATLAB was used to model tendon displacement, bending angle, curvature, and end-effector position.</p>

<p>The model assumed rigid segments, negligible tendon stretch and friction, negligible torsion and gravity, and equal rotation across active joints.</p>

<h2>Experimental Evaluation</h2>

<ul>
  <li>Evaluated eversion pressure and deployment performance.</li>
  <li>Measured steering behaviour and directional movement.</li>
  <li>Conducted position-holding tests of approximately three minutes in each tested direction.</li>
  <li>Evaluated interaction with debris and obstacles.</li>
  <li>Tested vortex-cannon payload spread at multiple distances.</li>
  <li>Integrated and experimentally evaluated the hybrid robotic prototype.</li>
</ul>

<p>The final hybrid system demonstrated approximately 20–30 degrees of steering.</p>

<h2>Engineering Contributions</h2>

<ul>
  <li>Mechanical design and CAD of the rolling-contact-joint steering module.</li>
  <li>Design and fabrication of the eversion transitioner cap.</li>
  <li>3D printing and assembly of the rigid steering segments.</li>
  <li>Tendon routing and actuation integration.</li>
  <li>PCC kinematic modelling and MATLAB simulation.</li>
  <li>Development of a lumen-compatible vortex-cannon end-effector.</li>
  <li>Experimental testing and evaluation of the integrated prototype.</li>
</ul>

<h2>Technologies</h2>

<p>SolidWorks, MATLAB, Arduino Mega 2560, RAMPS 1.4, NEMA 17 stepper motors, tendon-driven actuation, PLA 3D printing, and piecewise constant-curvature modelling.</p>

<h2>Thesis</h2>

<p><em>Deployable Hybrid Continuum-Eversion Robot for Medical Applications in Disaster Scenarios</em></p>

<p>MRes Medical Robotics and Image-Guided Intervention, Imperial College London, Hamlyn Centre for Medical Robotics.</p>
