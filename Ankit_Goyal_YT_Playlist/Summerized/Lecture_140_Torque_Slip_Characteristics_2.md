---
title: "Electrical Machines | Lec 101 | Torque Slip Characteristics -2 | GATE Electrical Engineering"
lecture: 140
topic: "Induction Machines"
duration: "00:50:20"
source: "https://www.youtube.com/watch?v=aBFWdvuxu7c"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 139: Torque Slip Characteristics 1](Lecture_139_Torque_Slip_Characteristics_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 141: Torque Slip Characteristics 3 →](Lecture_141_Torque_Slip_Characteristics_3.md)

---

# Electrical Machines | Lec 101 | Torque Slip Characteristics -2 | GATE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=aBFWdvuxu7c
- **Duration**: 00:50:20
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines torque-slip and torque-speed relationships in three-phase induction machines. It establishes the maximum torque condition using the Maximum Power Transfer Theorem applied across the rotor resistance branch. The discussion demonstrates why maximum breakdown torque is independent of rotor resistance while the breakdown slip varies proportionally with resistance. It details starting torque behavior across different rotor slot geometries and determines the required external rotor resistance to achieve maximum torque at standstill. Finally, the lecture develops normalized torque ratio expressions relating operating torque, starting torque, full-load torque, and maximum breakdown torque.

## Contents

- [[#Maximum Torque via MPTT|Maximum Torque via MPTT]]
- [[#Effect of Rotor Resistance|Effect of Rotor Resistance]]
- [[#Starting Heavy Loads & Slot Geometry|Starting Heavy Loads & Slot Geometry]]
- [[#Required Resistance for Max Starting Torque|Required Resistance for Max Starting Torque]]
- [[#Torque Ratio Equations|Torque Ratio Equations]]

---

## Maximum Torque via MPTT
_(06:07 - 21:07)_

Instead of differentiating the torque equation, we use the Maximum Power Transfer Theorem (MPTT). Developed torque is proportional to air gap power ($P_G$), which is the power absorbed by the variable resistor $r_2'/s$ in the Thévenin circuit. 

Maximum power transfers when this load resistance equals the magnitude of the source impedance:
$$\frac{r_2'}{s_{mT}} = |Z_{\text{source}}| = \sqrt{R_{th}^2 + (X_{th} + x_2')^2}$$

Solving for breakdown slip $s_{mT}$:
$$s_{mT} = \frac{r_2'}{\sqrt{R_{th}^2 + (X_{th} + x_2')^2}}$$

**Approximate Formulas ($R_1 = 0, x_1 = 0$):**
- Breakdown Slip: $s_{mT} \approx \frac{r_2'}{x_2'}$
- Maximum Torque: $T_{\text{max}} \approx \frac{3}{2 \omega_s} \frac{V_1^2}{x_2'}$

## Effect of Rotor Resistance
_(21:08 - 28:35)_

From the approximate formulas, we derive a fundamental rule for induction machines:
1. **$T_{\text{max}}$ is independent of rotor resistance $r_2'$**. Changing rotor resistance does not alter the peak torque magnitude.
2. **Breakdown slip $s_{mT}$ is directly proportional to $r_2'$**. Increasing rotor resistance shifts the peak torque toward higher slips (lower speeds).

## Starting Heavy Loads & Slot Geometry
_(28:35 - 39:57)_

At starting ($s = 1$), the torque is:
$$T_{\text{st}} \approx \frac{3}{\omega_s} \frac{V_1^2 r_2'}{(x_2')^2}$$
Starting torque is directly proportional to rotor resistance. Heavy loads (trains, cranes) require high breakaway torque, dictating high rotor resistance at startup.

**Leakage Reactance & Slot Geometry**:
$T_{\text{st}}$ is inversely proportional to the square of leakage reactance $x_2'$. 
- **Closed Slots**: Highest leakage flux $\implies$ Highest $x_2'$ $\implies$ Lowest $T_{\text{st}}$
- **Semi-Open Slots**: Moderate $x_2'$ $\implies$ Moderate $T_{\text{st}}$
- **Open Slots**: Lowest leakage flux $\implies$ Lowest $x_2'$ $\implies$ Highest $T_{\text{st}}$

## Required Resistance for Max Starting Torque
_(33:34 - 39:57)_

To make the motor develop its maximum breakdown torque right at standstill, we need $s_{mT} = 1$.
Using the approximate relation $s_{mT} = (r_2 + R_{\text{ext}}) / x_2 = 1$:
> [!success] Required External Resistance
> **$R_{\text{ext}} = x_2 - r_2$**
*(Note: This is only physically possible in Slip-Ring / Wound Rotor machines, not Squirrel Cage machines).*

## Torque Ratio Equations
_(39:58 - 50:14)_

When stator impedance is neglected, we can normalize developed torque at any slip $s$ against $T_{\text{max}}$:

> [!success] Ratio of Torque to Maximum Torque
> $$ \frac{T}{T_{\text{max}}} = \frac{2}{\dfrac{s_{mT}}{s} + \dfrac{s}{s_{mT}}} $$

*(Warning: Never use this equation to compare two arbitrary slips $s_1$ and $s_2$. It only works when comparing a generic slip $s$ directly to $s_{mT}$).*

**Derived Ratios**:
- **Full Load Ratio**: $\frac{T_{FL}}{T_{\text{max}}} = \frac{2}{\dfrac{s_{mT}}{s_{FL}} + \dfrac{s_{FL}}{s_{mT}}}$
- **Starting Ratio**: $\frac{T_{\text{st}}}{T_{\text{max}}} = \frac{2}{s_{mT} + \dfrac{1}{s_{mT}}}$
- **Starting to Full-Load Ratio**: $\frac{T_{\text{st}}}{T_{FL}} = \frac{\dfrac{s_{mT}}{s_{FL}} + \dfrac{s_{FL}}{s_{mT}}}{s_{mT} + \dfrac{1}{s_{mT}}}$

**Current-Based Ratio**:
Because air-gap power is $3(I_2')^2 (r_2'/s)$, the starting-to-full-load torque ratio can be rewritten using line currents:
> [!success] Current-Based Torque Ratio
> $$ \frac{T_{\text{st}}}{T_{FL}} = \left(\frac{I_{\text{st}}}{I_{FL}}\right)^2 s_{FL} $$
*(This is heavily used when analyzing motor starters).*

---

## Summary and Key Takeaways

- Maximum mechanical power transfer occurs when rotor branch resistance satisfies $r_2'/s_{mT} = \sqrt{R_{th}^2 + (X_{th} + x_2')^2}$.
- Neglecting stator impedance simplifies the breakdown slip expression to $s_{mT} \approx r_2'/x_2'$, proving that breakdown slip is directly proportional to rotor circuit resistance.
- Peak breakdown torque is given approximately by $T_{\text{max}} \approx \frac{3}{2 \omega_s} \frac{V_1^2}{x_2'}$, which is independent of rotor resistance $r_2'$.
- Adding external resistance $R_{\text{ext}}$ shifts the torque-speed peak toward lower speeds without altering the value of maximum torque.
- Closed rotor slots have the highest leakage reactance and yield the lowest starting torque, whereas open slots minimize leakage reactance and provide maximum starting torque.
- To achieve maximum torque at starting ($s=1$), external resistance equal to $R_{\text{ext}} = x_2 - r_2$ must be inserted in slip-ring rotor circuits.
- The developed torque normalized to maximum torque is given by $\frac{T}{T_{\text{max}}} = \frac{2}{\dfrac{s_{mT}}{s} + \dfrac{s}{s_{mT}}}$.
- The ratio of starting torque to full-load torque can be calculated from current as $\frac{T_{\text{st}}}{T_{FL}} = \left(\frac{I_{\text{st}}}{I_{FL}}\right)^2 s_{FL}$.

---

[← Lec 139: Torque Slip Characteristics 1](Lecture_139_Torque_Slip_Characteristics_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 141: Torque Slip Characteristics 3 →](Lecture_141_Torque_Slip_Characteristics_3.md)
