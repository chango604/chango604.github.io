---
title: "Soft Inductive Tactile Sensor"
category: "Research · Carnegie Mellon"
order: 1
year: "2025 – Present"
role: "Graduate researcher: sensor design, test automation, machine learning"
team: "Soft Machines Lab (advisor: Prof. Carmel Majidi)"
structure: "IMRD"
summary: "A soft sensor that combines five planar PCB coils with a magnetorheological elastomer and uses machine learning to locate where it is touched."
tagline: "Objective: build a soft, durable touch sensor that locates a contact point anywhere on its surface using only a few signal channels."
cover: "/assets/images/projects/tactile-sensor.svg"
cover_alt: "Cross-section schematic of the sensor: a magnetorheological elastomer layer above a PCB with five planar coils, connected to an inductance readout and a machine-learning model that outputs contact position."
cover_caption: "Sensor concept. Pressing the elastomer moves magnetic particles closer to the coils, which changes each coil's inductance."
skills: ["Sensor design", "2D modeling", "Robotic test automation", "INSTRON", "Python", "Machine learning"]
---

## Introduction

Robots that handle fragile objects or work beside people need skin that can feel *where* they are touched. Rigid sensors break when bent, and dense sensor grids need one wire per sensing point, which makes them hard to scale.

Soft inductive sensors avoid both problems. My objective is to design a soft sensor that locates a contact point continuously across its surface while using only **five** readout channels.

## Methods

The sensor stacks a **magnetorheological elastomer (MRE)**, a soft silicone filled with magnetic particles, on top of a PCB with **five planar coils**. When a probe presses the MRE, the particles move closer to the nearby coils and change their inductance.

I contributed to every stage of the project:

- **Design.** I modeled the sensor elements in 2D to choose the coil layout and the MRE layer.
- **Data collection.** I automated indentation tests with a robotic arm and an INSTRON load frame, so the system records each press location and force alongside the five inductance signals.
- **Analysis.** I trained machine-learning models in Python that map the five signals to the 2D position of the contact.

<!-- TODO (Changhyun): add the number of presses / positions in your dataset and the model type you used. -->

## Results

The trained model predicts the contact location continuously across the sensor surface, not just at the coil centers. Because every coil responds to presses near it, the model can interpolate between coils instead of needing a separate sensor at each point.

<!-- TODO (Changhyun): add your key numbers here, e.g. "mean localization error of X mm over a Y × Y mm area" and a photo or plot of predicted vs. true positions. -->

## Discussion

These results show that a few coils plus machine learning can replace a dense grid of sensing points, which reduces wiring and keeps the sensor soft. The next steps are to estimate contact **force** along with location and to test durability over repeated loading. We are preparing a manuscript titled *"Machine-Learning-Based Continuous Contact Localization with an Inductive Tactile Sensor."*
