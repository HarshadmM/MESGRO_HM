---
layout: project
title: "Wearable Haptic Finger for Microrobot Teleoperation"
description: "A low-cost, modular wearable haptic finger interface for human-in-the-loop control of a simulated microrobot approximately 200 μm in size."
date: 2025-12-12
categories: [Robotics, Mechatronics, Haptics, Medical Robotics, 3D Printing]
featured_image: "/assets/images/projects/haptic/Mechanical%20prototype.jpeg"
models:
  - file: "/assets/models/haptic-glove/haptic-glove.glb"
    description: "Interactive CAD assembly of the haptic-glove"
gallery:
  - file: "/assets/images/projects/haptic/Mechanical%20prototype.jpeg"
    description: "Mechanical prototype of the wearable haptic finger."
  - file: "/assets/images/projects/haptic/mech_prototype2.jpeg"
    description: "Second view of the wearable finger prototype."
---

## Overview

This MRes group project explored a wearable finger interface for haptic interaction during teleoperation of a simulated microrobot approximately 200 μm in size. At this scale, visual feedback alone can make subtle contact forces difficult to judge. The project investigated how a human operator could receive tactile cues while controlling a microrobot in a simulated medical intervention.

The group combined a wearable mechanical design, embedded sensing, and a software link between the hardware and a MATLAB/Simulink microrobot simulation. The prototype also explored PTFE tubing and its backlash as part of the mechanical haptic interaction.

## Mechanical design

I developed and compared three wearable-finger concepts:

1. A segmented finger made from TPU.
2. A segmented finger made from PLU.
3. A continuous TPU finger.

The concepts followed shared design goals: preserve finger movement and comfort during longer use, keep the device functional and low cost, and provide space for cable routing and a microcontroller. The design work also considered a compact component housing and the practicalities of fabricating and assembling the prototype.

## Sensing and haptic feedback

The system used four force-sensitive resistors (FSRs), read through Arduino analog inputs A0–A3 and voltage-divider circuits. As the finger interface bent or compressed, the FSR readings changed. The project software normalized the sensor values and used them in the feedback loop.

The team considered a flex sensor strip, but its size and distributed resistance response made it difficult to identify where bending occurred and map the reading clearly to finger motion. Point-pressure FSRs offered a more localized sensing area. Their response is nonlinear, so calibration is needed before sensor values can represent motion or contact consistently.

The feedback concept combined coin-style eccentric rotating mass (ERM) motors for vibration with a servo-driven soft tube for bending or tension cues. A C# interface handled serial-port selection and sensor monitoring, and bridged data over UDP to MATLAB/Simulink, where the simulated microrobot ran. Arduino handled the sensor and actuator connection at the hardware end.

## My contribution

My individual work focused on the wearable finger’s mechanical modelling and design. I:

- Created CAD models and developed the three mechanical concepts.
- 3D-printed prototype parts and contributed to mechanical iteration.
- Coordinated work across a five-person team with different technical specialisms.
- Considered comfort, fatigue, cable routing, microcontroller accommodation, cost, and manufacturability in the design.

The sensing, software, and integrated control system were developed as a group project; the points above describe my personal contribution.

## Integration and lessons learned

Connecting the wearable hardware to the simulation required a data path in both directions: sensor readings travelled from the device to the simulation, while simulation outputs returned to the hardware for feedback. The team reported that the MATLAB-to-C# path was stable, while the C#-to-MATLAB direction could introduce delays or queued packets. That latency matters for a real-time haptic loop.

The prototype used PTFE tubes within the project timeframe. Future iterations could compare them with more flexible silicone or polyurethane channels, refine sensor calibration, and improve the timing and reliability of the bidirectional communication.

## Technologies and methods

- CAD and mechanical modelling
- TPU and PLU design concepts
- 3D printing
- PTFE tubing and mechanical haptic interaction
- Arduino, analog FSR sensing, and ERM vibration motors
- C# serial interface and UDP communication
- MATLAB/Simulink microrobot simulation
- Cross-disciplinary project management