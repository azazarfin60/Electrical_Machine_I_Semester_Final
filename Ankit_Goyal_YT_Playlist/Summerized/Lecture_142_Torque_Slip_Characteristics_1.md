---
title: "Torque Slip Characteristics - 1 | L 39 | Electrical Machines | GATE 2022 | Ankit Sir"
lecture: 142
topic: "Induction Machines"
duration: "01:20:24"
source: "https://www.youtube.com/watch?v=jhmeR1x2eco"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 141: Torque Slip Characteristics 3](Lecture_141_Torque_Slip_Characteristics_3.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 143: Torque Slip Characteristics 2 →](Lecture_143_Torque_Slip_Characteristics_2.md)

---

# Torque Slip Characteristics - 1 | L 39 | Electrical Machines | GATE 2022 | Ankit Sir

- **Source**: https://www.youtube.com/watch?v=jhmeR1x2eco
- **Duration**: 01:20:24
- **Compiled**: 2026-09-23

---

## Overview

This lecture solves key numerical problems on 3-phase induction motors with a focus on torque-slip characteristics and power flow. It covers developed torque, breakdown conditions, and the distinction between maximum torque and maximum mechanical power. Worked examples demonstrate the use of normalized torque ratios to solve exam problems without requiring absolute terminal voltages. The session also analyzes external rotor resistance control, plugging mode dynamics, time harmonics in inverter supplies, and full energy audits.

## Contents

- [[#Problem Setup and Parameter Scaling|Problem Setup and Parameter Scaling]]
- [[#Maximum Torque vs. Maximum Mechanical Power|Maximum Torque vs. Maximum Mechanical Power]]
- [[#Torque Ratio Problem Solving|Torque Ratio Problem Solving]]
- [[#External Resistance and Speed Control|External Resistance and Speed Control]]
- [[#Plugging Mode & Time Harmonics|Plugging Mode & Time Harmonics]]
- [[#Power Flow Balance Analysis|Power Flow Balance Analysis]]

---

## Problem Setup and Parameter Scaling
_(00:13 - 09:54)_

For exam problems where stator parameters are not provided, we ignore $R_1$ and $x_1$.

**Base Problem:**
A 4-pole, 50 Hz motor with standstill parameters $r_2 = 0.1\,\Omega, x_2 = 0.9\,\Omega$.
- Synchronous Speed: $N_s = 1500\text{ rpm}$
- Breakdown Slip: $s_{mT} = \frac{r_2}{x_2} = \frac{0.1}{0.9} = 0.1111$

At 4% slip ($s = 0.04$), calculate developed torque and mechanical power:
$$T_{\text{dev}} = \frac{3}{\omega_s} \frac{V_2^2 (r_2/s)}{(r_2/s)^2 + x_2^2} \quad \text{and} \quad P_{\text{mech}} = T_{\text{dev}} \omega_r$$

## Maximum Torque vs. Maximum Mechanical Power
_(09:57 - 14:47)_

A classic mistake is assuming maximum mechanical power occurs at the breakdown torque slip $s_{mT}$.

1. **Maximum Torque** occurs when $r_2/s = x_2$:
   $$s_{mT} = \frac{r_2}{x_2}$$
2. **Maximum Mechanical Power** occurs when the equivalent mechanical load matches the source impedance:
   $$R_2'\left(\frac{1}{s_{mP}} - 1\right) = |Z_{\text{source}}| = \sqrt{r_2^2 + x_2^2}$$
   $$s_{mP} = \frac{r_2}{r_2 + \sqrt{r_2^2 + x_2^2}}$$

**Conclusion**: Since $\sqrt{r_2^2 + x_2^2} > x_2$, it follows that $s_{mP} < s_{mT}$. Maximum mechanical power occurs at a slightly higher rotor speed than maximum torque.

## Torque Ratio Problem Solving
_(14:50 - 35:35)_

Many exam problems omit terminal voltages and reactances entirely, providing only torque percentages (e.g., $T_{\text{st}} = 100\% T_{FL}$ and $T_{\text{max}} = 200\% T_{FL}$).

**Key Equation**:
$$\frac{T}{T_{\text{max}}} = \frac{2}{\frac{s_{mT}}{s} + \frac{s}{s_{mT}}}$$

**Workflow**:
1. From $T_{\text{st}}/T_{\text{max}} = 0.5$, substitute $s = 1$ to find $s_{mT}$:
   $$\frac{2 s_{mT}}{1 + s_{mT}^2} = 0.5 \implies s_{mT}^2 - 4 s_{mT} + 1 = 0 \implies s_{mT} \approx 0.268$$
2. From $T_{FL}/T_{\text{max}} = 0.5$, substitute $s = s_{FL}$ to find $s_{FL}$:
   $$\frac{2}{\frac{s_{mT}}{s_{FL}} + \frac{s_{FL}}{s_{mT}}} = 0.5 \implies s_{FL} \approx 0.0718$$

## External Resistance and Speed Control
_(35:36 - 50:15)_

In wound-rotor motors, adding external rotor resistance shifts $s_{mT}$ without changing peak torque.
- To achieve maximum torque at standstill ($s_{mT}' = 1$), set $R_2 + R_{\text{ext}} = X_2 \implies R_{\text{ext}} = X_2 - R_2$.
- Under a constant-torque load in the low-slip region, running slip is proportional to rotor resistance ($T \propto \frac{s V^2}{f R_2}$). Doubling $R_2$ doubles the operating slip $s$.

## Plugging Mode & Time Harmonics
_(55:30 - 71:50)_

**Plugging Mode ($s > 1$)**:
When the rotor spins backwards against the field, $P_{\text{mech}} < 0$ (absorbing mechanical power) and $P_g > 0$ (drawing electrical power). The machine acts as a pure brake, dumping all energy into rotor copper losses.

**Inverter Time Harmonics**:
A 5th time harmonic rotates backwards at $-5 N_s$. The slip relative to this harmonic field is:
$$s_5 = \frac{N_{s5} - N_r}{N_{s5}} = \frac{-5 N_s - (1-s) N_s}{-5 N_s} > 1$$
Because $s_5 > 1$, the 5th harmonic creates a parasitic braking torque (plugging operation).

## Power Flow Balance Analysis
_(71:53 - 78:04)_

A complete power flow audit verifies the fundamental ratio:
$$P_g : P_{\text{cu2}} : P_{\text{dev}} = 1 : s : (1 - s)$$

For a motor drawing 35 kW with 1 kW stator losses:
1. $P_g = 35 - 1 = 34\text{ kW}$
2. $P_{\text{cu2}} = s P_g$
3. $P_{\text{dev}} = (1-s) P_g$
4. $P_{\text{shaft}} = P_{\text{dev}} - P_{\text{rotational}}$
5. $\eta = \frac{P_{\text{shaft}}}{P_{\text{in}}}$

---

## Summary and Key Takeaways

- The developed electromagnetic torque neglecting stator impedance is $T = \frac{3}{\omega_s} \frac{V_2^2 (r_2/s)}{(r_2/s)^2 + x_2^2}$, with breakdown slip $s_{mT} = \frac{r_2}{x_2}$ and peak torque $T_{\text{max}} = \frac{3}{2 \omega_s} \frac{V_2^2}{x_2}$.
- Maximum mechanical power occurs at slip $s_{mP} = \frac{r_2}{r_2 + \sqrt{r_2^2 + x_2^2}}$, which is always lower than the breakdown torque slip $s_{mT}$.
- The normalized torque ratio $\frac{T}{T_{\text{max}}} = \frac{2}{\frac{s_{mT}}{s} + \frac{s}{s_{mT}}}$ allows direct calculation of operating and starting torque ratios without terminal voltage data.
- Maximum breakdown torque $T_{\text{max}}$ is completely independent of rotor circuit resistance $R_2$.
- Inserting external rotor resistance increases starting torque and operating slip, with maximum starting torque occurring when $R_2 + R_{\text{ext}} = X_2$.
- Under constant load torque in the low-slip region, running slip is proportional to rotor resistance and frequency, and inversely proportional to the square of voltage ($s \propto \frac{f R_2}{V^2}$).
- In braking or plugging mode ($s > 1$), the machine draws mechanical power through the shaft and electrical power from the supply, dissipating both as rotor copper heat.
- In inverter drives, the 5th time harmonic rotates backwards at $-5 N_s$, resulting in a high harmonic slip $s_5 = \frac{-5 N_s - N_r}{-5 N_s} > 1$ that produces parasitic braking.
- Complete power flow in an induction motor strictly obeys the fundamental ratio $P_g : P_{\text{cu2}} : P_{\text{dev}} = 1 : s : (1 - s)$.

---

[← Lec 141: Torque Slip Characteristics 3](Lecture_141_Torque_Slip_Characteristics_3.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 143: Torque Slip Characteristics 2 →](Lecture_143_Torque_Slip_Characteristics_2.md)
