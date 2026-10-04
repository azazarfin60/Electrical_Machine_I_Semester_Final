---
title: "High Torque Cage Rotor and Induction Generator | L 47 | Electrical Machines | GATE 2022"
lecture: 159
topic: "Induction Machines"
duration: "00:45:10"
source: "https://www.youtube.com/watch?v=9wT1vMX7Md8"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 158: Miscellaneous Concepts](Lecture_158_Miscellaneous_Concepts.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 160: Single Phase Induction Motor 1 →](Lecture_160_Single_Phase_Induction_Motor_1.md)

---

# High Torque Cage Rotor and Induction Generator | L 47 | Electrical Machines | GATE 2022

- **Source**: https://www.youtube.com/watch?v=9wT1vMX7Md8
- **Duration**: 00:45:10
- **Compiled**: 2026-09-23

---

## Overview

This lecture works through examination problems on high torque cage rotors, induction generators, and parasitic harmonic phenomena. It details numerical torque evaluations for inner and outer rotor cages at standstill and rated speed. It analyzes supersynchronous induction generator speed calculations, air-gap power linearity, and rotor copper loss. Finally, it addresses cogging, crawling saddle dips, deep bar skin effect current distributions, and isolated generator excitation.

## Contents

- [[#Double Cage Torque Analysis|Double Cage Torque Analysis]]
- [[#Induction Generator Power Flow & Operating Speeds|Induction Generator Power Flow & Operating Speeds]]
- [[#Slot Depth Effects & Generator Excitation|Slot Depth Effects & Generator Excitation]]
- [[#Parasitic Phenomena Summary|Parasitic Phenomena Summary]]

---

## Double Cage Torque Analysis
_(00:02 - 15:29)_

A double cage rotor is modeled as two parallel rotor circuits:
- **Outer Cage**: High resistance $R_o$, low leakage reactance $X_o$.
- **Inner Cage**: Low resistance $R_i$, high leakage reactance $X_i$.

**Total Torque Formulation**:
The total torque is the sum of the torques developed by each cage:
$$T_{\text{total}} = T_{\text{outer}} + T_{\text{inner}}$$
Where for each cage, $T_k = \frac{3}{\omega_{sm}} \frac{V_2^2 (R_k/s)}{(R_k/s)^2 + X_k^2}$

- **At Standstill ($s=1$)**: Leakage reactance dominates. The outer cage's torque ratio over the inner cage is approximately $(R_o/R_i) \cdot (Z_i^2/Z_o^2)$. Because $Z_i \gg Z_o$ due to high inner reactance, the outer cage provides roughly 70-80% of the total starting torque.
- **At Running ($s \approx 0.05$)**: The resistive term $R/s$ dominates. The low resistance inner cage now takes over, producing roughly 80% of the normal running torque.

## Induction Generator Power Flow & Operating Speeds
_(15:43 - 20:57, 31:30 - 36:11)_

When a prime mover drives the rotor above synchronous speed ($N_r > N_s$), slip becomes negative ($s < 0$).
- **Air Gap Power Linearity**: Neglecting stator resistance and rotor leakage reactance, air-gap power $P_g$ is directly proportional to slip ($P_g \propto s$). This linear relationship allows calculating dual operating speeds directly from their respective active power outputs: $P_{g1}/P_{g2} = s_1/s_2$.
- **Power Flow**: Mechanical power $P_{\text{mech,in}} = P_g(1-s)$. Since $s < 0$, the input mechanical power must supply both the required air-gap power and the internal rotor copper losses ($P_{\text{Cu,rotor}} = |s|P_g = -sP_g$). Air gap power flows from rotor to stator.

## Slot Depth Effects & Generator Excitation
_(36:32 - 41:23)_

- **Rotor Slot Depth**: Increasing the depth of rotor slots increases the iron leakage flux path. This raises the leakage reactance ($X_2$), which in turn **reduces breakdown (pull-out) torque** ($T_{\text{max}} \propto 1/X_2$) and **degrades the operating power factor**.
- **External Resistance Control**: For a wound rotor induction generator driven at a constant speed by a prime mover, the slip is fixed. Adding external resistance via slip rings reduces the delivered air gap power without changing the operating speed.
- **Generator Excitation**: A standalone (self-excited) induction generator requires a parallel capacitor bank. It can only build up voltage if there is **residual magnetic flux** in the rotor to induce an initial small EMF.

## Parasitic Phenomena Summary
_(20:59 - 31:25)_

- **Cogging**: Standstill magnetic locking caused by integral ratios of stator and rotor slots. Prevented by skewing.
- **Crawling**: Low-speed running trap ($N \approx N_s/7$) caused by the forward-rotating 7th space harmonic torque dip. Prevented by chording (short-pitching) stator windings.
- **Deep Bar Skin Effect**: At starting (high frequency), slot leakage reactance gradient forces current to the top of the bar. This crowding reduces effective area, drastically raising AC resistance and boosting starting torque.

---

## Summary and Key Takeaways

- In a double-cage rotor, the outer cage has high resistance and low leakage reactance, producing high starting torque ($T_{\text{outer}} \gg T_{\text{inner}}$ at $s = 1$).
- At normal operating speeds, $R_2 / s$ dominates over leakage reactance, causing the low-resistance inner cage to develop the vast majority of running torque ($T_{\text{inner}} \gg T_{\text{outer}}$).
- In a deep bar rotor at standstill, depth-dependent leakage inductance forces current into the top of the conductor, increasing effective AC resistance through the skin effect.
- An induction machine operates as an induction generator when driven mechanically above synchronous speed ($s < 0$), where air-gap power is proportional to slip ($P_g \propto s$) when rotor reactance is neglected.
- Mechanical power input to an induction generator exceeds air-gap power ($P_{\text{mech, in}} = P_g (1 - s) > P_g$) because it supplies both electrical output and internal rotor copper losses ($P_{\text{Cu, rotor}} = |s| P_g$).
- Cogging is a standstill phenomenon where tooth alignment reluctance torque locks the rotor, whereas crawling is a low-speed running phenomenon caused by the forward-rotating 7th space harmonic saddle dip near $N_s / 7$.
- Increasing rotor slot depth increases leakage reactance, which reduces maximum pull-out torque and degrades the operating power factor.
- A standalone self-excited induction generator requires residual rotor magnetism and terminal shunt capacitors to initiate and sustain voltage build-up.

---

[← Lec 158: Miscellaneous Concepts](Lecture_158_Miscellaneous_Concepts.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 160: Single Phase Induction Motor 1 →](Lecture_160_Single_Phase_Induction_Motor_1.md)
