---
layout: project
title: "NeoAir: MIST Catheter Placement Confirmation"
description: "A team project exploring rapid carbon dioxide based confirmation of catheter placement during minimally invasive surfactant therapy (MIST)."
date: 2026-04-17
categories: [Biomedical Engineering, "CAD & Design", Rapid Prototyping]
featured_image: "/assets/images/projects/neoair/hero_neoair_image.jpg"
hero_image: "/assets/images/projects/neoair/hero_neoair_image.jpg"
models:
  - file: "/assets/models/neoair/inline_neoair.glb"
    description: "Interactive CAD model of the inline NeoAir concept"
gallery_groups:
  - title: "Project development"
    layout: "stack"
    items:
      - file: "/assets/images/projects/neoair/Working%20on%20NeoAir.jpg"
        description: "Developing the NeoAir project concept"
  - title: "Project team"
    layout: "pair"
    items:
      - file: "/assets/images/projects/neoair/hackstarter_winning_poster.png"
        description: "NeoAir's Hackstarter winning poster"
      - file: "/assets/images/projects/about_page/NeoAir%20team.jpg"
        description: "The NeoAir project team"
---

## Project overview

NeoAir was a group project by [Yu-Chieh Amy Lai](https://www.linkedin.com/in/yu-chieh-amy-lai-4a84ba243/), [Anton Gerasimov](https://www.linkedin.com/in/anton-ger/), [Harshad Malik](https://www.linkedin.com/in/harshadmm), and [Hetarth Bhatt](https://www.linkedin.com/in/hetarth-bhatt-9a4a8123b/). The team explored ways to make catheter placement confirmation clearer during minimally invasive surfactant therapy (MIST), a treatment used for respiratory distress syndrome in preterm infants.

## Recognition

NeoAir won the **Hackstarter Award: Open Project** at the 2026 Imperial College Advanced Hackspace Hackstarter final. [See the Hackstarter 2026 winners](https://imperialhackspace.com/our-events/hackstarter-26/).

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

- [Yu-Chieh Amy Lai](https://www.linkedin.com/in/yu-chieh-amy-lai-4a84ba243/)
- [Anton Gerasimov](https://www.linkedin.com/in/anton-ger/)
- [Harshad Malik](https://www.linkedin.com/in/harshadmm)
- [Hetarth Bhatt](https://www.linkedin.com/in/hetarth-bhatt-9a4a8123b/)
