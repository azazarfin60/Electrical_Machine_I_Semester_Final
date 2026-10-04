---
title: "Electrical Machines | Lec 95 | Induction Machine Construction - 1 | GATE Electrical Engineering"
lecture: 132
topic: "Induction Machines"
duration: "00:48:50"
source: "https://www.youtube.com/watch?v=Wk0b3yaoptg"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 131: Induction Machines Introduction](Lecture_131_Induction_Machines_Introduction.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 133: Induction Machine Construction 2 →](Lecture_133_Induction_Machine_Construction_2.md)

---

# Electrical Machines | Lec 95 | Induction Machine Construction - 1 | GATE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=Wk0b3yaoptg
- **Duration**: 00:48:50
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines the physical construction of three-phase induction machines with an emphasis on stator slots and squirrel cage rotors. It explains magnetic pole formation along the stator bore and derives slot leakage permeance as a function of slot geometry. The discussion compares open, semi-open, and closed slot profiles across air gap reluctance, leakage reactance, harmonic generation, and power factor. Finally, the lecture details squirrel cage rotor construction, covering conductive bars, end rings, core laminations, skewing benefits, and running performance.

## Contents

- [[#Stator Poles and Slot Leakage Reactance|Stator Poles and Slot Leakage Reactance]]
- [[#Slot Geometry Comparison|Slot Geometry Comparison]]
- [[#Slot Selection Guide|Slot Selection Guide]]
- [[#Squirrel Cage Rotor Construction|Squirrel Cage Rotor Construction]]
- [[#Core Laminations: Stator vs. Rotor|Core Laminations: Stator vs. Rotor]]
- [[#Rotor Skewing|Rotor Skewing]]

---

## Stator Poles and Slot Leakage Reactance
_(00:13 - 14:33)_

**Pole Formation Rule**:
- Whenever two adjacent conductors carry currents in opposite directions (e.g., $\otimes$ and $\odot$), their flux lines combine to emerge from or enter the stator, inducing a magnetic pole.
- Conductors carrying currents in the same direction ($\otimes$ and $\otimes$) cancel their flux in the intervening space, forming no pole.

**Slot Leakage Reactance ($X_l$)**:
Leakage flux crosses the slot directly through air, never reaching the rotor. 
- Leakage permeance is derived as: $\mathcal{P}_{\text{leakage}} \propto \frac{h}{w_s}$
- Thus, slot leakage reactance is directly proportional to slot depth ($h$) and inversely proportional to slot width ($w_s$): **$X_l \propto \frac{h}{w_s}$**.

## Slot Geometry Comparison
_(14:33 - 35:46)_

The shape of the stator slots governs the trade-off between magnetizing current (air gap reluctance) and leakage reactance.

### 1. Open Slots
- **Design**: Slot mouth width equals slot body width.
- **Leakage Reactance**: Wide opening through air $\implies$ highest reluctance to leakage flux $\implies$ **Lowest $X_l$** (Best for high torque).
- **Magnetizing Current**: Conductors are exposed. The mechanical air gap must be large to prevent contact with the rotor. Large air gap $\implies$ high gap reluctance $\implies$ **Highest $I_\mu$** (Poor no-load power factor).
- **Harmonics**: The teeth vs. wide-open slots cause extreme flux density variations $\implies$ **Highest slot harmonics**.

### 2. Semi-Open Slots
- **Design**: Slot mouth is partially closed by iron lips.
- **Characteristics**: A moderate compromise. The air gap can be smaller than open slots (reducing $I_\mu$), while leakage is higher than open slots but lower than closed slots. Harmonics are moderate.

### 3. Closed Slots
- **Design**: An iron bridge completely encloses the slot; no opening to the air gap.
- **Leakage Reactance**: The iron bridge provides a high-permeability path for leakage flux $\implies$ **Highest $X_l$** (Reduces torque, poor full-load power factor).
- **Magnetizing Current**: The stator bore is perfectly smooth, so the air gap can be mechanically minimized $\implies$ **Lowest $I_\mu$** (Best no-load power factor).
- **Harmonics**: Uniform air gap $\implies$ **Negligible slot harmonics**.
- **Winding**: Hardest to assemble (conductors must be threaded axially).

## Slot Selection Guide
- **3-Phase Induction Motors**: **Semi-open slots** (Best compromise for power factor, torque, and harmonics).
- **Synchronous Machines**: **Open slots** (A large air gap improves stability; low $X_l$ improves power transfer).
- **DC Machines**: **Open slots** (Large air gap reduces cross-magnetizing armature reaction).
- **Small/Toy Motors**: **Closed slots** (Cheap, disposable, lowest $I_\mu$).

## Squirrel Cage Rotor Construction
_(35:46 - 48:42)_

A Squirrel Cage Induction Motor (SCIM) has no wound coils on the rotor. 
- Heavy uninsulated copper or aluminum bars are embedded into rotor slots.
- **End Rings**: Heavy conducting rings at both ends permanently short-circuit all bars, forming a closed cage. They also provide mechanical strength against centrifugal forces.
- **Automatic Pole Matching**: The cage automatically adapts to mirror the number of magnetic poles ($P$) produced by the stator.

**Operating Characteristics**:
- **Smooth Air Gap**: The cage construction allows a very small mechanical air gap. This yields a low magnetizing current and excellent running power factor.
- **Poor Starting**: Because rotor resistance ($R_2$) is inherently very low, the SCIM suffers from **low starting torque** and draws very high starting current at a low starting power factor.

## Core Laminations: Stator vs. Rotor
_(40:07 - 42:00)_

Eddy current loss depends heavily on frequency ($P_e \propto f^2 t^2$). 
- The stator operates at line frequency ($f_1 = 50\text{ Hz}$). Stator laminations must be very thin ($0.35\text{ to }0.5\text{ mm}$).
- The rotor operates at slip frequency ($f_2 = s f_1 \approx 1\text{ to }3\text{ Hz}$). Rotor laminations can be safely made thicker without incurring significant eddy current losses.

## Rotor Skewing
_(42:00 - 48:42)_

Rotor slots are not cut parallel to the shaft; they are slightly twisted or skewed.
- **Why Skew?**
  1. Eliminates slot/tooth harmonics.
  2. Prevents magnetic locking (cogging) between stator and rotor teeth.
  3. Reduces magnetic hum (acoustic noise) for quieter operation.

---

## Summary and Key Takeaways

- Adjacent conductors carrying opposite current directions induce a magnetic pole between them, whereas conductors carrying identical current directions form no pole.
- Slot leakage flux and slot leakage reactance are directly proportional to slot depth and inversely proportional to slot width, giving $X_l \propto \frac{h}{w_s}$.
- Open slots have the highest air gap reluctance, require the largest magnetizing current $I_\mu$, and produce noticeable slot harmonics of order $n = \frac{2S}{P} \pm 1$.
- Open slots offer the lowest leakage reactance and easiest coil insertion, making them standard for synchronous machines and DC machines.
- Semi-open slots balance air gap reluctance, leakage reactance, and harmonic distortion, making them the preferred choice for three-phase induction motors.
- Closed slots provide the lowest magnetizing current and lowest slot harmonics, but their continuous iron bridge causes massive leakage reactance.
- Stator laminations are thinner than rotor laminations because stator frequency ($f_1 = 50\text{ Hz}$) exceeds rotor slip frequency ($f_2 = s f_1$).
- A squirrel cage rotor automatically mirrors the number of magnetic poles established by the stator field.
- Rotor conductors are skewed across the core to suppress tooth harmonics, prevent cogging, and eliminate acoustic magnetic hum.

---

[← Lec 131: Induction Machines Introduction](Lecture_131_Induction_Machines_Introduction.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 133: Induction Machine Construction 2 →](Lecture_133_Induction_Machine_Construction_2.md)
