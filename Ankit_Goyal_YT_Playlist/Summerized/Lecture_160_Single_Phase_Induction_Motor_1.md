---
title: "Single Phase Induction Motor-1 | Induction Machine | Lec 112 | GATE & ESE | Ankit Goyal"
lecture: 160
topic: "Induction Machines"
duration: "00:36:02"
source: "https://www.youtube.com/watch?v=FvAqndJj0ok"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 159: High Torque Cage Rotor and Induction Generator](Lecture_159_High_Torque_Cage_Rotor_and_Induction_Generator.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 161: Single Phase Induction Motor 2 →](Lecture_161_Single_Phase_Induction_Motor_2.md)

---

# Single Phase Induction Motor-1 | Induction Machine | Lec 112 | GATE & ESE | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=FvAqndJj0ok
- **Duration**: 00:36:02
- **Compiled**: 2026-09-23

---

## Overview

This lecture introduces the single-phase induction motor using double revolving field theory. It shows how disconnecting one phase wire from a three-phase stator leaves a single-phase winding. The pulsating air-gap MMF resolves into forward and backward rotating fields of equal amplitude. The lecture analyzes rotor equivalent circuits, slips, and torques produced by both fields. It proves why starting torque is zero and explains how an initial mechanical push produces self-acceleration. Finally, it constructs the complete running equivalent circuit and torque-speed characteristics.

## Contents

- [[#Double Revolving Field Theory|Double Revolving Field Theory]]
- [[#Starting & Running Torque Characteristics|Starting & Running Torque Characteristics]]
- [[#Complete Equivalent Circuit|Complete Equivalent Circuit]]

---

## Double Revolving Field Theory
_(00:12 - 14:10)_

A single-phase induction motor has a pulsating magnetic field. According to **Double Revolving Field Theory**, this pulsating MMF can be mathematically resolved into two rotating magnetic fields of equal amplitude ($F_m/2$) rotating in opposite directions at synchronous speed ($N_s$ and $-N_s$):
$$f(\theta, t) = \frac{F_m}{2} \cos(\theta - \omega t) + \frac{F_m}{2} \cos(\theta + \omega t)$$

Assuming the rotor rotates forward at speed $N$:
- **Forward Slip**: $s = \frac{N_s - N}{N_s}$
- **Backward Slip**: $s_b = \frac{-N_s - N}{-N_s} = \frac{N_s + N}{N_s} = 2 - s$

The rotor experiences two distinct sets of induced EMFs, currents, and impedances:
- **Forward Rotor Impedance**: $R_2/s + jX_2$
- **Backward Rotor Impedance**: $R_2/(2-s) + jX_2$

## Starting & Running Torque Characteristics
_(14:13 - 35:55)_

**At Standstill ($s = 1$)**:
- The forward slip and backward slip are equal ($s = 1$, $2-s = 1$).
- The forward and backward rotor impedances are identical, so their induced currents and resulting MMFs are identical.
- The forward torque $T_f$ and backward torque $T_b$ are equal and opposite.
- **Net Starting Torque is Zero**: $T_{\text{net}} = T_f - T_b = 0$. A single-phase induction motor is **not self-starting**.

**Under Running Conditions**:
- If the rotor is given an initial forward push, $s$ drops below 1 and $(2-s)$ rises above 1.
- The effective forward rotor resistance $R_2/s$ increases, causing $T_f$ to rise.
- The effective backward rotor resistance $R_2/(2-s)$ decreases, causing $T_b$ to fall.
- **Net Torque is Positive**: $T_f > T_b \implies T_{\text{net}} > 0$. The motor will self-accelerate and continue to run in the direction of the initial push.
- The resulting torque-speed curve is symmetric in the 1st and 3rd quadrants, crossing the origin.

## Complete Equivalent Circuit
_(28:08 - 35:55)_

To model the single-phase motor, the standard induction motor equivalent circuit is modified. The single magnetizing branch and rotor branch are split into two series sections, representing the forward and backward fields.
All rotor and magnetizing parameter values are halved ($/2$):

$$Z_{\text{in}} = (R_1 + jX_1) + Z_f + Z_b$$
Where:
- **Forward Branch ($Z_f$)**: $\frac{j X_m}{2} \parallel \left( \frac{R_2'}{2s} + j\frac{X_2'}{2} \right)$
- **Backward Branch ($Z_b$)**: $\frac{j X_m}{2} \parallel \left( \frac{R_2'}{2(2-s)} + j\frac{X_2'}{2} \right)$

---

## Summary and Key Takeaways

- Disconnecting one supply line from a star or delta stator reduces a three-phase motor to single-phase operation across a single terminal voltage.
- A single-phase pulsating MMF $F_m \cos\theta \cos\omega t$ resolves into forward and backward revolving fields of magnitude $F_m / 2$ rotating at $+N_s$ and $-N_s$.
- For a rotor running at speed $N$, the forward slip is $s = (N_s - N)/N_s$ and the backward slip is $s_b = 2 - s$.
- The rotor equivalent impedances are $R_2 / s + j X_2$ for the forward field and $R_2 / (2 - s) + j X_2$ for the backward field.
- At standstill ($s = 1$), forward and backward currents and power factors are equal, making forward torque equal to backward torque ($T_f = T_b$).
- The net starting torque is zero ($T_{\text{start}} = 0$), so an unassisted single-phase induction motor is not self-starting.
- An initial forward push makes $s < 1$ and $2 - s > 1$, which increases $T_f$ above $T_b$ and accelerates the rotor in the direction of the push.
- The net torque-speed curve is symmetric in the first and third quadrants, passing through zero at $N = 0$.
- The complete running equivalent circuit places the stator impedance in series with the forward parallel branch $Z_f$ and the backward parallel branch $Z_b$.

---

[← Lec 159: High Torque Cage Rotor and Induction Generator](Lecture_159_High_Torque_Cage_Rotor_and_Induction_Generator.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 161: Single Phase Induction Motor 2 →](Lecture_161_Single_Phase_Induction_Motor_2.md)
