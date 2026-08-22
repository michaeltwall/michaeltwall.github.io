---
layout: post
title: Electrical Engineering Internship
description: Summer Internship @ drone delivery startup
abstract: Developed quad-rail buck converter with power protection for drone delivery system; responsible for complete design and layout for manufacturing.
date: 2026-08-15 12:00 -0400
categories: [Internship]
tags: [design, PCB, power systems, hardware, manufacturing, startup]
math: false
image:
  path: assets/posts/Arrive-AI-internship/PCB_Layout.png
---
{% include abstract.html %}

In Summer of 2026, I completed an 11-week Electrical Engineering internship at Arrive AI, Inc. Arrive AI is a ~50 person startup working on package recieving systems for autonomous delivery.

## Project Overview

The goal of this project was to design a power supply PCB for use in Arrive AI's drone delivery system; it must be capable of supplying adequate power to all internal systems and be ready for manufacturing. The project specifications were as follows: 48V/10A supply voltage converted into four protected outputs at 48V/6A, 12V/3A, 5V/2A, and 3.3V/2A. We were responsible for everything from conception to manufacturing. 

This project was completed with another Electrical Engineering intern, and we recieved guidance from the Senior Electrical Engineer, [Brad Sutton](https://www.linkedin.com/in/bradtsutton). The broad project constraints allowed room for experimentation and research in order to create the best solution.

## My Role

I was responsible for the following during the duration of the project:

- Circuit schematic design and part selection using Altium Designer
- Validation and testing using PSPICE simulation
- PCB layout and optimization using Altium Designer
- Manufacturing through PCBWay

---

## Design Process

#### Concept Design

![Concept Design Flowchart](/assets/posts/Arrive-AI-internship/Block_Diagram_transparent.png){: width="450"}

Concept design involved a flowchart with main parts chosen. We compared different buck converters from various suppliers, and chose the Texas Instruments LMR516xx synchronous buck converter due to limited external component requirement, ideal current limiting options, and high efficiency.

#### Schematic Design

![5V rail schematic](/assets/posts/Arrive-AI-internship/PCB_Schematic_5V_Rail.png){: width="450"}

Once our flowchart was verified, we began schematic design in Altium Designer. This involved research of optimal design and protection systems, and Texas Instruments' online calculators and tools were very helpful for this step.

PSPICE simulation tool was utilized to validate our design; steady state output, overcurrent, undercurrent, overvoltage, and undervoltage were all tested and verified to be functioning correctly.

After validation, we selected appropriate manufacturer parts to meet all circuit requirements.

#### PCB Layout

![Final PCB layout](/assets/posts/Arrive-AI-internship/PCB_Layout.png){: width="450"}

With our schematics verified and all components picked, we moved on to PCB layout. The following criteria were used when creating the layout:

- Minimize size of converter $$di/dt$$ loop, and isolate from sensitive traces
- Maximize area of high current traces
- Reduce converter feedback trace length
- Minimize overall design footprint for efficient space usage

This process involved much trial and error and redesign to achieve an optimal design. We designed our prototype on a two layer PCB, although the complete integrated carrier board will utilize four layers.

#### Manufacturing

![Final PCB 3D render](/assets/posts/Arrive-AI-internship/PCB_3D_iso.png){: width="450"}

Finally, once our PCB design was validated, we were ready for manufacturing. Our chosen manufacturer was PCBWay.

The complete board measured 132.5 x 112.5 mm (5.2" x 4.4"), and contained 104 total components.

## Takeaways



