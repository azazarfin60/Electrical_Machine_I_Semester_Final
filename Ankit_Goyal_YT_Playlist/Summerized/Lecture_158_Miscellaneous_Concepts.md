---
title: "Electrical Machines | Lec 111 | Miscellaneous Concepts | GATE/ESE Electrical Engineering"
lecture: 158
topic: "Induction Machines"
duration: "00:46:21"
source: "https://www.youtube.com/watch?v=WXQujFXTUl8"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 157: High Torque Cage Rotor](Lecture_157_High_Torque_Cage_Rotor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 159: High Torque Cage Rotor and Induction Generator →](Lecture_159_High_Torque_Cage_Rotor_and_Induction_Generator.md)

---

# Electrical Machines | Lec 111 | Miscellaneous Concepts | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=WXQujFXTUl8
- **Duration**: 00:46:21
- **Compiled**: 2026-09-23

---

## Overview

This lecture covers parasitic harmonic phenomena and induction generator fundamentals. It explores space harmonics caused by non-sinusoidal winding distributions and slotting. The discussion explains how harmonic fields cause crawling and cogging in squirrel-cage rotors, along with their mitigation techniques. Finally, it analyzes the operation, reactive power needs, and power flow of grid-connected and self-excited induction generators.

## Contents

- [[#Space Harmonics and Crawling|Space Harmonics and Crawling]]
- [[#Cogging (Magnetic Locking) and Skewing|Cogging (Magnetic Locking) and Skewing]]
- [[#Induction Generator Fundamentals|Induction Generator Fundamentals]]

---

## Space Harmonics and Crawling
_(00:14 - 16:25)_

Non-sinusoidal winding distributions produce space harmonics in the air-gap flux density:
$$n = 6k \pm 1$$
- **5th Harmonic ($n=5$)**: Rotates backward at $N_s/5$. Generates braking torque.
- **7th Harmonic ($n=7$)**: Rotates forward at $N_s/7$. Generates a forward motoring torque that dips sharply after $N_s/7$.

**Crawling Phenomenon**:
The superposition of the 7th harmonic torque creates a pronounced "saddle dip" in the composite torque-speed curve at roughly $1/7^{\text{th}}$ synchronous speed. If the load torque intersects this dip stably ($d T_e / dN < 0$), the motor will fail to accelerate further and remain trapped at this crawling speed ($N \approx N_s/7$). 
- Operating at crawling speed draws heavy inrush-level currents, rapidly destroying insulation.
- Since wound-rotor motors can add starting resistance to easily bypass this dip, crawling is primarily a problem for **squirrel cage** motors.
- **Mitigation**: Eliminated by short-pitching (chording) the stator coils. A coil span of $5/6$ pole pitch ($\alpha = 30^\circ$) suppresses both the 5th and 7th harmonics.

## Cogging (Magnetic Locking) and Skewing
_(16:25 - 27:43)_

**Cogging**:
Occurs when the motor refuses to start from rest. It happens if the number of stator slots ($S_s$) and rotor slots ($S_r$) are equal or share an integral multiple ($S_s = k S_r$).
- Stator and rotor teeth align perfectly, creating a path of minimum magnetic reluctance.
- The strong reluctance torque magnetically locks the teeth together. If starting torque cannot overcome this reluctance torque, the motor hums but does not turn.

**Mitigation (Skewing)**:
Cogging is prevented by:
1. Choosing relatively prime slot combinations ($S_s \neq S_r$).
2. **Skewing** the rotor slots by one stator slot pitch. 
- **Benefits of Skewing**: Completely eliminates cogging reluctance torque, smooths out space harmonics (preventing crawling), and eliminates magnetic hum.
- **Trade-offs**: Slightly reduces the effective tangential force ($k_{\text{skew}} < 1$), thereby slightly reducing induced EMF, starting torque, and breakdown torque.

## Induction Generator Fundamentals
_(27:50 - 46:14)_

An induction machine becomes a generator when driven by a prime mover above synchronous speed ($N_r > N_s$). Slip becomes negative ($s < 0$).
- **Equivalent Circuit**: The resistance parameter $R_2'/s$ becomes negative, acting as an active power source injecting real power into the stator. Air gap power flows from rotor to stator.
- **Power Factor**: Induction generators can ONLY operate at a **leading power factor**. They export real power but must always consume reactive power for core magnetization.
- **Self-Excited (SEIG)**: Standalone induction generators require a parallel capacitor bank. Voltage build-up relies on rotor residual magnetism inducing a small leading capacitor current, which recursively reinforces the magnetic field until saturation.
- **Externally Excited (Grid-Connected)**: Connected to the AC grid. The grid fixes the voltage and frequency while supplying the necessary magnetizing vars.

---

## Summary and Key Takeaways

- Space harmonics of order $r = 6k \pm 1$ rotate at speeds $N_r = N_s / r$, where order $6k+1$ rotates forward and order $6k-1$ rotates backward.
- The 7th harmonic creates a forward saddle dip around $N_s/7$, causing the motor to crawl at low speed if load torque intersects this dip stably.
- Cogging occurs at standstill when stator and rotor slot numbers share a common integer factor, locking teeth in minimum reluctance alignment.
- Cogging is prevented by selecting $S_s \neq S_r$ with no common factors, or by skewing rotor slots by one stator slot pitch.
- Skewing eliminates slot harmonics and smooths torque, but it slightly reduces fundamental induced EMF and leakage inductance.
- An induction machine operates as an induction generator when an external prime mover drives the rotor above synchronous speed ($s < 0$).
- An induction generator delivers active power to the grid but always absorbs reactive power for core magnetization.
- A standalone self-excited induction generator requires residual rotor magnetism and a shunt capacitor bank to supply lagging reactive magnetization.

---

[← Lec 157: High Torque Cage Rotor](Lecture_157_High_Torque_Cage_Rotor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 159: High Torque Cage Rotor and Induction Generator →](Lecture_159_High_Torque_Cage_Rotor_and_Induction_Generator.md)
