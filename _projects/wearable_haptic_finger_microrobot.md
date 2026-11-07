---
layout: project
title: "Wearable Haptic Interface for Microrobot Teleoperation"
description: "A microrobotic teleoperation project that evolved from a wearable finger prototype into a magnetic-encoder glove for operator-side joint-angle sensing and haptic feedback."
date: 2025-12-12
featured_homepage: true
categories: [Microrobotics, Control, Microactuation, Mechatronics, Haptics, Medical Robotics, "CAD & Design", 3D Printing, Arduino]
featured_image: "/assets/images/projects/haptic/Mechanical%20prototype.jpeg"
models:
  - file: "/assets/models/haptic-glove/haptic%20glove2.glb"
    description: "Interactive CAD assembly of the magnetic-encoder glove prototype from August 2026."
  - file: "/assets/models/haptic-glove/haptic-glove.glb"
    description: "Earlier CAD assembly of the wearable haptic glove."
gallery_groups:
  - title: "Initial wearable prototype"
    placement: "haptic-interface-design"
    layout: pair
    items:
      - file: "/assets/images/projects/haptic/haptic_glove_very%20first%20prototype.jpg"
        description: "Early wearable haptic-glove prototype and control hardware."
      - file: "/assets/images/projects/haptic/Mechanical%20prototype.jpeg"
        description: "Mechanical prototype of the wearable haptic finger."
      - file: "/assets/images/projects/haptic/mech_prototype2.jpeg"
        description: "Second view of the initial wearable finger prototype."
  - title: "Magnetic-encoder redesign · August 2026"
    placement: "prototype-evolution"
    layout: pair-large
    items:
      - file: "/assets/images/projects/haptic/new_magnetic%20encoder%20based.png"
        description: "Side view of the segmented glove redesigned around magnetic encoders."
      - file: "/assets/images/projects/haptic/Top%20view%20of%20new%20segmented%20glove%20with%20magnetic%20encoders.png"
        description: "Top view of the segmented glove with magnetic encoders."
---

## Overview

This MRes group project focused on human-in-the-loop teleoperation of a simulated 200 μm microrobot in a medical-intervention scenario. The operator interface evolved from a wearable haptic finger into a segmented glove.

At this scale, visual feedback alone can make subtle contact forces difficult to judge. The wearable interface explored tactile feedback as one part of a wider microrobotic control and actuation system.

<details class="project-system-details">
<summary>Overall system and contributions by other members</summary>
<div class="project-system-details-content">
<p>The team connected FSR sensing and wearable haptic feedback to a C# interface and a MATLAB/Simulink microrobot simulation. The microrobot was simulated; the physical prototype was the wearable interface and its feedback hardware.</p>
<ul>
<li><strong>Dr. Belal</strong>, Lecturer (Assistant Professor) at the University of Bath — project supervisor.</li>
<li><strong><a href="https://www.linkedin.com/in/haoyun-feng-061340393/">Haoyun Feng</a></strong> — MATLAB and integration.</li>
<li><strong>Yacui Zhao</strong> — overall project oversight, drawing on previous experience, and PID.</li>
<li><strong>Xueyi Fu</strong> — electronics.</li>
<li><strong>Cai Jingtong</strong> — PID and control with Yacui Zhao.</li>
</ul>

<figure class="hybrid-media">
<img src="{{ '/assets/images/projects/haptic/simulink_feedback_path.png' | relative_url }}" alt="MATLAB/Simulink teleoperation model showing coordinate transformation, safety and control logic, microrobot model, haptic feedback, and data transmission." class="gallery-image" data-zoomable loading="lazy" decoding="async">
<figcaption>Control model: MATLAB and integration by Haoyun Feng; PID and control by Yacui Zhao and Cai Jingtong.</figcaption>
</figure>

<figure class="hybrid-media">
<img src="{{ '/assets/images/projects/haptic/teleoperation_control_interface.png' | relative_url }}" alt="Four time-series plots showing the FSR sensor channels S1–S4 during operation." class="gallery-image" data-zoomable loading="lazy" decoding="async">
<figcaption>Live FSR traces from the integrated system: electronics by Xueyi Fu and MATLAB integration by Haoyun Feng.</figcaption>
</figure>

<figure class="hybrid-media">
<img src="{{ '/assets/images/projects/haptic/fsr_sensor_operating_principle.png' | relative_url }}" alt="FSR sensor process from finger pressure and resistance change through a voltage divider and Arduino analog inputs to serial data." class="gallery-image" data-zoomable loading="lazy" decoding="async">
<figcaption>FSR sensing and its electronics, associated with Xueyi Fu’s electronics contribution.</figcaption>
</figure>

<figure class="hybrid-media">
<img src="{{ '/assets/images/projects/haptic/arduino_fsr_erm_circuit.png' | relative_url }}" alt="Arduino circuit with four FSR channels, two ERM vibration motors using transistor drivers and diode protection, and a servo." class="gallery-image" data-zoomable loading="lazy" decoding="async">
<figcaption>Wearable sensor and actuator circuit; electronics by Xueyi Fu.</figcaption>
</figure>

<figure class="hybrid-media">
<img src="{{ '/assets/images/projects/haptic/vibration_operating_principle.png' | relative_url }}" alt="Four-stage vibration feedback path from input signal through vibration-level mapping and PWM output to ERM motor actuation." class="gallery-image" data-zoomable loading="lazy" decoding="async">
<figcaption>Vibration mapping and ERM actuation: electronics by Xueyi Fu, within the integrated system developed with Haoyun Feng.</figcaption>
</figure>
</div>
</details>

## Microrobotic control and actuation

The control path connected Arduino sensor inputs and wearable actuators, a C# serial interface, and a MATLAB/Simulink microrobot simulation, with UDP carrying data between the interface and simulation. Operator inputs informed the simulated robot, while simulation outputs returned to the glove's physical actuators. The microrobot remained simulated; the physical prototype was the wearable interface and its feedback hardware.

## Haptic interface design

I developed and compared three wearable-finger concepts:

1. A segmented finger made from TPU.
2. A segmented finger made from PLA.
3. A continuous TPU finger.

The concepts followed shared design goals: preserve finger movement and comfort during longer use, keep the device functional and low cost, and provide space for cable routing and a microcontroller. The design work also considered a compact component housing and the practicalities of fabricating and assembling the prototype.

<div class="project-gallery-anchor" data-gallery-anchor="haptic-interface-design" aria-hidden="true"></div>

## Haptic sensing and feedback

In the first prototype, the system used four force-sensitive resistors (FSRs), read through Arduino analog inputs A0–A3 and voltage-divider circuits. As the finger interface bent or compressed, the FSR readings changed. The project software normalized the sensor values and used them in the feedback loop.

The team considered a flex sensor strip, but its size and distributed resistance response made it difficult to identify where bending occurred and map the reading clearly to finger motion. Point-pressure FSRs offered a more localized sensing area. Their response is nonlinear, so calibration is needed before sensor values can represent motion or contact consistently.

The feedback concept combined coin-style eccentric rotating mass (ERM) motors for vibration with a servo-driven soft tube for bending or tension cues. A C# interface handled serial-port selection and sensor monitoring, and bridged data over UDP to MATLAB/Simulink, where the simulated microrobot ran. Arduino handled the sensor and actuator connection at the hardware end.

## Prototype evolution: magnetic-encoder glove (early August 2026)

The first prototype left operator-side finger joint-angle sensing as an important unresolved issue. I proposed using magnetic encoders to measure those angles directly at the operator's hand. Haoyun Feng and I then developed a redesigned, segmented-glove prototype around that approach in early August 2026.

This iteration reflects my growth as a designer: I used the sensing requirement to shape the glove's mechanical layout and segmentation. The gallery shows side and top views of the redesigned prototype together.

<div class="project-gallery-anchor" data-gallery-anchor="prototype-evolution" aria-hidden="true"></div>

## My contribution

My individual work focused on mechanical modelling and design across the wearable prototypes. I:

- Created CAD models and developed the three initial mechanical concepts.
- Proposed magnetic encoders for operator-side joint-angle sensing and worked with Haoyun Feng on the segmented-glove redesign.
- 3D-printed prototype parts and contributed to mechanical iteration.
- Coordinated work across a five-person team with different technical specialisms.
- Considered comfort, fatigue, cable routing, microcontroller accommodation, cost, and manufacturability in the design.

The sensing, software, and integrated control system were developed as a group project; the points above describe my personal contribution.

## Integration and lessons learned

Connecting the wearable hardware to the simulation required a data path in both directions: sensor readings travelled from the device to the simulation, while simulation outputs returned to the hardware for feedback. The team reported that the MATLAB-to-C# path was stable, while the C#-to-MATLAB direction could introduce delays or queued packets. That latency matters for a real-time haptic loop.

The prototype used PTFE tubes within the project timeframe. Future iterations could compare them with more flexible silicone or polyurethane channels, refine sensor calibration, and improve the timing and reliability of the bidirectional communication.

## Technologies and methods

- CAD and mechanical modelling
- TPU and PLA design concepts
- 3D printing
- PTFE tubing and mechanical haptic interaction
- Arduino, analog FSR sensing, magnetic encoders, and ERM vibration motors
- C# serial interface and UDP communication
- MATLAB/Simulink microrobot simulation
- Cross-disciplinary project management
