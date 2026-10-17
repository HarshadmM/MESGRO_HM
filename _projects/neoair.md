---
layout: project
title: "NeoAir: MIST Catheter Placement Confirmation"
description: "A team project exploring rapid carbon dioxide based confirmation of catheter placement during minimally invasive surfactant therapy (MIST)."
date: 2026-04-17
categories: [Medical Robotics, Biomedical Engineering, Device Design, Rapid Prototyping]
featured_image: "/assets/images/projects/neoair/balloon-simulation-setup.jpeg"
hero_collage:
  - file: "/assets/images/projects/neoair/balloon-simulation-setup.jpeg"
    description: "Balloon-based simulated respiratory setup for the detector demonstration"
  - file: "/assets/images/projects/neoair/inline-detector-demo.jpeg"
    description: "Inline detector being operated during a bench demonstration"
  - file: "/assets/images/projects/neoair/inline-colourimetric-cross-section.png"
    description: "Cross-section of the inline colourimetric detector concept"
  - file: "/assets/images/projects/neoair/electronic-device-cad.png"
    description: "CAD render of the electronic detector housing"
  - file: "/assets/images/projects/neoair/electronic-device-section.png"
    description: "Section view of the electronic detector concept"
  - file: "/assets/images/projects/neoair/preliminary-cost-model.png"
    description: "Team's preliminary cost crossover estimate for the two concepts"
gallery_groups:
  - title: "Bench demonstration"
    layout: "pair"
    items:
      - file: "/assets/images/projects/neoair/balloon-simulation-setup.jpeg"
        description: "Balloon and tubing used as a simulated respiratory setup"
      - file: "/assets/images/projects/neoair/inline-detector-demo.jpeg"
        description: "Inline detector and syringe during a bench demonstration"
  - title: "Inline colourimetric detector"
    layout: "stack"
    items:
      - file: "/assets/images/projects/neoair/inline-colourimetric-cross-section.png"
        description: "CAD cross-section showing the luer connections, spacer, filter and pH indicator"
  - title: "Electronic detector concept"
    layout: "pair"
    items:
      - file: "/assets/images/projects/neoair/electronic-device-cad.png"
        description: "Outer CAD housing for the electronic concept"
      - file: "/assets/images/projects/neoair/electronic-device-section.png"
        description: "Internal section view of the electronic concept"
  - title: "Preliminary cost comparison"
    layout: "stack"
    items:
      - file: "/assets/images/projects/neoair/preliminary-cost-model.png"
        description: "The team's presentation estimated a cost crossover at about 15 uses, using its stated component costs."
---

## Project overview

NeoAir was a group project by Amy Lai, Anton Gerasimov, Harshad Malik and Hetarth Bhatt. The team explored ways to make catheter placement confirmation clearer during minimally invasive surfactant therapy (MIST), a treatment used for respiratory distress syndrome in preterm infants.

The design brief focused on a practical problem: catheter placement can be difficult to confirm quickly, while an infant remains awake and may move. The background presentation cites a 20–30 second window for an initial catheterisation attempt; the [OPTIMIST-A protocol](https://pmc.ncbi.nlm.nih.gov/articles/PMC4236682/) describes pausing and allowing recovery when placement is not achieved in that period.

## Design direction

The team developed two complementary concepts for detecting carbon dioxide (CO₂) in aspirated gas. The aim was to give the operator a placement cue before surfactant delivery and to reduce the extra steps and attention required during the procedure.

### Inline colourimetric detector

The inline concept places a pH indicator and filter inside a compact adapter between the catheter and syringe. Its cross-section shows the indicator, spacer and luer-lock connections. The proposed workflow uses manual aspiration and a visible colour change as a qualitative CO₂ cue. The team presented this as a lightweight, single-use option adapted around familiar syringe components.

### Electronic detector

The second concept packages the detector in a reusable housing. The CAD work explores the outer shell and internal layout, including a button and a spring-loaded aspiration mechanism. The intended direction was to automate aspiration and provide a quantitative CO₂ measurement, with the trade-offs of a larger device and a less familiar workflow.

Published work has also investigated CO₂ detection for MIST catheter location confirmation. In a small study, capnography distinguished tracheal from esophageal placement; this informed the project direction, but does not validate the NeoAir concepts. [Read the study](https://pubmed.ncbi.nlm.nih.gov/36720984/).

## Prototype demonstration and trade-offs

The supplied presentation shows an inline detector bench demonstration using a balloon-and-tubing setup as a simulated respiratory system. This was a concept demonstration, not testing with patients or clinical validation.

The team's comparison weighed simplicity and low per-use cost against automation and reusability:

| Inline colourimetric concept | Electronic concept |
| --- | --- |
| Single-use and based on familiar syringe components | Reusable, with a new workflow for operators to learn |
| Manual aspiration | Spring-loaded automatic aspiration was proposed to reduce operator workload |
| Lightweight; qualitative CO₂ indication | Bulkier; intended to provide quantitative CO₂ measurement |

The presentation's preliminary cost model used a £220 fixed cost for the electronic concept and £15 per inline use, giving an estimated cost crossover at about 15 uses. This is the team's model, not a measured lifecycle cost.

## Next steps

The presentation identifies realistic simulation, calibration and maintenance planning, miniaturisation, sterility, manufacturing feasibility and further validation studies as remaining work. Those steps would be needed before judging performance or suitability for clinical use.

## Project team

Amy Lai · Anton Gerasimov · Harshad Malik · Hetarth Bhatt
