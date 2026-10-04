---
title: "Electrical Machines | Lec 110 | High Torque Cage Rotor | GATE/ESE Electrical Engineering"
lecture: 157
topic: "Induction Machines"
duration: "00:25:10"
source: "https://www.youtube.com/watch?v=EEnOc4EMEUo"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 156: Braking of Induction Motor](Lecture_156_Braking_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 158: Miscellaneous Concepts →](Lecture_158_Miscellaneous_Concepts.md)

---

# Electrical Machines | Lec 110 | High Torque Cage Rotor | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=EEnOc4EMEUo
- **Duration**: 00:25:10
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines high starting torque squirrel cage induction motors. It explains how deep bar and double cage rotor constructions overcome the poor starting torque of standard cage machines without external slip rings. The discussion demonstrates how slot leakage flux gradients induce an automatic skin effect, raising effective rotor resistance at stand-still. It then details the construction of double cage rotors, tracing how current shifts between cages from starting to running, and derives the composite torque-speed characteristics and parallel per-phase equivalent circuit model.

## Contents

- [[#The Conflicting Resistance Requirements|The Conflicting Resistance Requirements]]
- [[#Deep Bar Rotor Construction|Deep Bar Rotor Construction]]
- [[#Double Cage Rotor Construction|Double Cage Rotor Construction]]
- [[#Equivalent Circuit & Torque Characteristics|Equivalent Circuit & Torque Characteristics]]

---

## The Conflicting Resistance Requirements
_(00:12 - 04:00)_

Squirrel cage motors lack slip rings, meaning external resistance cannot be added. However, induction motors require conflicting rotor resistance profiles:
- **At Starting ($s=1$)**: High $R_2$ is needed to produce high starting torque ($T_{\text{st}} \propto R_2$) and to limit inrush current.
- **At Running ($s \approx 0$)**: Low $R_2$ is needed to minimize $I^2R$ copper losses and maintain high efficiency.

To solve this, deep bar and double cage designs exploit the **skin effect** to automatically vary rotor resistance based on slip frequency.

## Deep Bar Rotor Construction
_(04:00 - 12:40)_

In a deep bar rotor, the conductor bars are tall and narrow.
- **Leakage Reactance Gradient**: Leakage flux crossing the slot increases with depth. The bottom of the bar links all flux above it, so leakage reactance is highest at the bottom and lowest at the top ($X_{\text{bottom}} \gg X_{\text{top}}$).
- **At Starting ($50\text{ Hz}$)**: Reactance dominates ($X_2 \gg R_2$). Current takes the path of least reactance, crowding into the top edge of the bar (Skin Effect). This reduces the effective cross-sectional area, greatly increasing the AC resistance ($R_{\text{ac}} \gg R_{\text{dc}}$) and thus boosting starting torque.
- **At Running ($\sim 2\text{ Hz}$)**: Reactance is negligible. Current distribution is dictated by resistance alone. It spreads uniformly across the entire bar, returning resistance to its low DC value ($R_{\text{dc}}$) for efficient running.

## Double Cage Rotor Construction
_(12:40 - 19:59)_

A double cage rotor uses two physically separate squirrel cages in the same slot.
- **Outer Cage**: Small cross-section or high-resistivity material (e.g., brass). Placed near the air gap. **High resistance, low leakage reactance**.
- **Inner Cage**: Large cross-section copper. Placed deep in the slot. **Low resistance, high leakage reactance**.

**Operation**:
- **At Starting**: High rotor frequency makes the inner cage's high leakage reactance act as a choke. Most current flows through the **outer cage**. Its high resistance provides high starting torque.
- **At Running**: Low rotor frequency makes leakage reactance negligible. Current divides based on resistance. The bulk of the current flows through the **inner cage**. Its low resistance ensures high efficiency.

## Equivalent Circuit & Torque Characteristics
_(19:59 - 25:02)_

- **Torque Superposition**: The total torque is the algebraic sum of the individual cage torques ($T_{\text{total}} = T_{\text{inner}} + T_{\text{outer}}$). The outer cage provides the high starting torque peak, while the inner cage provides the high breakdown torque near synchronous speed, resulting in a broad, flat torque-speed curve.
- **Equivalent Circuit**: The two cages are modeled as two parallel branches connected across the magnetizing reactance.
  - Inner branch: $Z_{\text{inner}} = R_2'/s + jX_2'$
  - Outer branch: $Z_{\text{outer}} = R_3'/s + jX_3'$
  - Total rotor impedance: $Z_2 = Z_{\text{inner}} \parallel Z_{\text{outer}}$

---

## Summary and Key Takeaways

- Squirrel cage motors intrinsically possess low starting torque, which deep bar and double cage designs elevate internally.
- In deep bar rotors, slot leakage flux increases with depth, causing leakage reactance to be lowest at the top of the bar and highest at the bottom ($X_{\text{top}} \ll X_{\text{bottom}}$).
- At starting line frequency ($50\text{ Hz}$), current crowds into the upper section of the deep bar via skin effect, reducing effective cross-sectional area and sharply increasing AC resistance.
- Elevated starting resistance increases starting torque ($T_{\text{st}} \propto R_2$) while limiting starting current.
- Under normal low-slip running conditions, the resistive term $R_2'/s$ dominates leakage reactance, restoring uniform current distribution and low rotor copper losses.
- Double cage rotors utilize two concentric cages connected in parallel by common end rings.
- The outer cage has high resistance and low leakage reactance ($R_{\text{outer}} \gg R_{\text{inner}}$, $X_{\text{outer}} \ll X_{\text{inner}}$), dominating starting operation.
- The inner cage has low resistance and high leakage reactance, carrying the bulk of the rotor current during running conditions to maintain high efficiency.
- In the per-phase equivalent circuit, a double cage rotor is modeled as two parallel branches connected across the magnetizing reactance: $Z_2 = (R_2'/s + jX_2') \parallel (R_3'/s + jX_3')$.

---

[← Lec 156: Braking of Induction Motor](Lecture_156_Braking_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 158: Miscellaneous Concepts →](Lecture_158_Miscellaneous_Concepts.md)
