---
title: "Torque Slip Characteristics - 2 | L 40 | Electrical Machines | GATE 2022 | Ankit Sir"
lecture: 143
topic: "Induction Machines"
duration: "00:49:06"
source: "https://www.youtube.com/watch?v=VxAbdLzfr1E"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 142: Torque Slip Characteristics 1](Lecture_142_Torque_Slip_Characteristics_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 144: Stability and Testing of Induction Motor →](Lecture_144_Stability_and_Testing_of_Induction_Motor.md)

---

# Torque Slip Characteristics - 2 | L 40 | Electrical Machines | GATE 2022 | Ankit Sir

- **Source**: https://www.youtube.com/watch?v=VxAbdLzfr1E
- **Duration**: 00:49:06
- **Compiled**: 2026-09-23

---

## Overview

This lecture solves fourteen comprehensive numerical problems on the torque-slip characteristics and performance of 3-phase induction motors. It focuses on analytical methods for evaluating operating slip, starting torque ratios, and breakdown conditions under varied operating constraints. The discussion details the influence of rotor resistance insertion, frequency and voltage variations, and stator leakage impedance. Through step-by-step solutions, it demonstrates how normalized torque equations provide quick, exact solutions for competitive examinations.

## Contents

- [[#Torque Ratios and Stator Leakage|Torque Ratios and Stator Leakage]]
- [[#Starting Current and Torque Multipliers|Starting Current and Torque Multipliers]]
- [[#External Resistance and Speed Control|External Resistance and Speed Control]]
- [[#Frequency and Voltage Scaling|Frequency and Voltage Scaling]]
- [[#Power Flow and Gross Torque Verification|Power Flow and Gross Torque Verification]]
- [[#Frequency for Max Starting Torque|Frequency for Max Starting Torque]]

---

## Torque Ratios and Stator Leakage
_(00:01 - 07:33)_

**Problem 1: Torque Ratios**
When stator impedance is neglected, the torque ratio formula simplifies problem solving.
For a motor with $R_2 = 0.1\,\Omega, X_2 = 0.92\,\Omega$, breakdown slip is $s_{mT} = R_2/X_2 = 0.1087$. 
At $s_{FL} = 0.03$:
$$\frac{T_{FL}}{T_{\text{max}}} = \frac{2}{\frac{s_{mT}}{s_{FL}} + \frac{s_{FL}}{s_{mT}}} = \frac{2}{3.623 + 0.276} \approx 0.513$$

**Problem 2: Including Stator Leakage**
If stator resistance is zero ($r_1 = 0$) but stator leakage reactance $x_1$ is given, simply replace $x_2'$ with the total leakage $x_1 + x_2'$:
$$T_{\text{max}} = \frac{3}{2 \omega_s} \frac{V_1^2}{x_1 + x_2'}$$

## Starting Current and Torque Multipliers
_(07:33 - 10:25)_

**Problem 3**
Starting torque can be computed from the starting current multiplier. Since $T \propto I_2^2 R_2 / s$:
$$\frac{T_{\text{st}}}{T_{FL}} = \left(\frac{I_{\text{st}}}{I_{FL}}\right)^2 s_{FL}$$
If $I_{\text{st}} = 5 I_{FL}$ and $s_{FL} = 0.05$:
$$\frac{T_{\text{st}}}{T_{FL}} = (5)^2 (0.05) = 1.25$$

## External Resistance and Speed Control
_(10:25 - 15:02)_

**Problem 4**
To force a motor to develop its rated full-load torque at a much higher slip (e.g., changing operating slip from $s_1=0.03$ to $s_2=0.20$), external resistance is added.
In the low-slip linear region, $T \propto s / R_{2,\text{total}}$. For constant torque:
$$\frac{s_1}{R_2} = \frac{s_2}{R_2 + r_{\text{ext}}}$$
$$1 + \frac{r_{\text{ext}}}{R_2} = \frac{0.20}{0.03} \implies r_{\text{ext}} \approx 5.67 R_2$$

## Frequency and Voltage Scaling
_(15:09 - 24:53)_

**Problem 5**
When both frequency $f$ and voltage $V$ change:
- $s_{mT} \propto 1/f$
- $T_{\text{max}} \propto (V/f)^2$
If frequency halves ($f_2 = 0.5 f_1$) and voltage drops to $0.75 V_1$:
Breakdown slip doubles ($s_{mT2} = 2 s_{mT1}$), and maximum torque scales by $(0.75 / 0.5)^2 = 2.25$.

**Problem 7: Finding $s_{mT}$ from Percentages**
If $T_{\text{st}} = 1.5 T_{FL}$ and $T_{\text{max}} = 2.0 T_{FL}$, then $T_{\text{st}} / T_{\text{max}} = 0.75$.
Using $\frac{2 s_{mT}}{s_{mT}^2 + 1} = 0.75 \implies 3s_{mT}^2 - 8s_{mT} + 3 = 0$.
The roots are $0.451$ and $2.215$. The stable motoring root is $s_{mT} = 0.451$.

## Power Flow and Gross Torque Verification
_(25:00 - 29:47)_

**Problem 8**
Developed gross electromagnetic torque can be evaluated using two identical expressions. Because $P_{\text{dev}} = (1 - s) P_g$ and $\omega_r = (1 - s) \omega_s$:
$$T_{\text{dev}} = \frac{P_g}{\omega_s} = \frac{P_{\text{dev}}}{\omega_r}$$
This allows calculating torque directly from air-gap power without finding rotor speed.

## Frequency for Max Starting Torque
_(34:37 - 39:30)_

**Problem 11 & 12**
- **Conceptual Trap**: $T_{\text{max}}$ is independent of $R_2$. The *speed* at which $T_{\text{max}}$ occurs depends on $R_2$.
- **Tuning for Start**: To get maximum torque right at standstill ($s=1$), we need $s_{mT} = 1 \implies X_2(f) = R_2$. 
If a 50 Hz motor has $X_2 = 2 R_2$, we must halve the frequency to 25 Hz so that the new reactance equals $R_2$.

---

## Summary and Key Takeaways

- When stator impedance is neglected, the torque ratio satisfies $\frac{T}{T_{\text{max}}} = \frac{2}{\frac{s_{mT}}{s} + \frac{s}{s_{mT}}}$, where breakdown slip is $s_{mT} = \frac{R_2}{X_2}$.
- If stator resistance is zero but stator leakage reactance is present, breakdown torque is $T_{\text{max}} = \frac{3}{2 \omega_s} \frac{V_1^2}{x_1 + x_2'}$.
- The ratio of starting torque to full-load torque relates directly to starting current by $\frac{T_{\text{st}}}{T_{FL}} = \left(\frac{I_{\text{st}}}{I_{FL}}\right)^2 s_{FL}$.
- Maintaining constant full-load torque at higher slip requires added rotor resistance scaling as $\frac{s_1}{R_2} = \frac{s_2}{R_2 + r_{\text{ext}}}$.
- Breakdown slip scales inversely with supply frequency ($s_{mT} \propto 1/f$), while maximum torque scales with the square of the voltage-to-frequency ratio ($T_{\text{max}} \propto (V/f)^2$).
- Gross developed electromagnetic torque can be evaluated using either air-gap power or developed mechanical power: $T_{\text{dev}} = \frac{P_g}{\omega_s} = \frac{P_{\text{dev}}}{\omega_r}$.
- Maximum breakdown torque magnitude is independent of rotor resistance, but the rotor speed at which maximum torque occurs depends directly on rotor resistance.
- For maximum torque to occur right at standstill ($s = 1$), the supply frequency must be adjusted until standstill reactance matches rotor resistance ($X_2(f) = R_2$).

---

[← Lec 142: Torque Slip Characteristics 1](Lecture_142_Torque_Slip_Characteristics_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 144: Stability and Testing of Induction Motor →](Lecture_144_Stability_and_Testing_of_Induction_Motor.md)
