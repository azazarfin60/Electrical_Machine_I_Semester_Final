---
title: "Torque Slip Characteristics - 1 | Electrical Machines | Lec 100 | GATE & ESE (EE, ECE) | Ankit Goyal"
lecture: 139
topic: "Induction Machines"
duration: "00:40:00"
source: "https://www.youtube.com/watch?v=OdA19ldXm7E"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 138: Losses and Efficiency of Induction Machines](Lecture_138_Losses_and_Efficiency_of_Induction_Machines.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 140: Torque Slip Characteristics 2 →](Lecture_140_Torque_Slip_Characteristics_2.md)

---

# Torque Slip Characteristics - 1 | Electrical Machines | Lec 100 | GATE & ESE (EE, ECE) | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=OdA19ldXm7E
- **Duration**: 00:40:00
- **Compiled**: 2026-09-23

---

## Overview

This lecture establishes the complete analytical and graphical treatment of torque-slip characteristics for three-phase induction machines. The stator circuit is reduced to a Thévenin equivalent network to derive closed-form expressions for rotor current, air gap power, and developed electromagnetic torque. The complete torque-speed characteristic is mapped across motoring, generating, and braking regimes. Standard engineering approximations are then developed for both low-slip linear operation and high-slip starting conditions.

## Contents

- [[#Thévenin Equivalent Circuit|Thévenin Equivalent Circuit]]
- [[#The General Torque Equation|The General Torque Equation]]
- [[#The Three Operating Regimes|The Three Operating Regimes]]
- [[#Approximate Torque Equations (Standard)|Approximate Torque Equations (Standard)]]
- [[#Linear and Starting Approximations|Linear and Starting Approximations]]

---

## Thévenin Equivalent Circuit
_(05:14 - 10:07)_

To evaluate rotor current and developed torque analytically, the stator network is reduced to a Thévenin equivalent circuit across the magnetizing branch. Assuming stator resistance is small compared to stator reactance ($R_1 \ll x_1 + X_m$), the parameters simplify to:

1. **Thévenin Voltage**: $V_{th} \approx V_1 \left(\frac{X_m}{x_1 + X_m}\right)$
2. **Thévenin Impedance**: 
   - $R_{th} \approx R_1 \left(\frac{X_m}{x_1 + X_m}\right)$
   - $X_{th} \approx x_1 \left(\frac{X_m}{x_1 + X_m}\right)$

The scaling factor $\frac{X_m}{x_1 + X_m}$ is typically between 0.90 and 0.97.

## The General Torque Equation
_(10:12 - 14:48)_

Using the Thévenin circuit, the rotor current $I_2'$ is determined. Substituting $I_2'$ into the air gap power equation $P_G = 3 (I_2')^2 (r_2'/s)$ and dividing by synchronous speed $\omega_s$ yields the exact general torque equation:

> [!success] General Developed Torque Equation
> $$T_{\text{dev}} = \frac{3}{\omega_s} \frac{V_{th}^2 \left(\frac{r_2'}{s}\right)}{\left(R_{th} + \frac{r_2'}{s}\right)^2 + (X_{th} + x_2')^2}$$

*Use this formula when stator parameters ($R_1, x_1$) are explicitly provided.*

## The Three Operating Regimes
_(15:04 - 26:24)_

Plotting developed torque against rotor speed (or slip) maps the entire machine capability:

1. **Motoring Mode ($0 < s < 1$)**: $N_r$ is between $0$ and $N_s$. Torque acts in the direction of rotation.
2. **Generating Mode ($s < 0$)**: $N_r > N_s$. The prime mover drives the rotor faster than the synchronous field. Torque opposes rotation, delivering active power to the grid. The machine still relies on the grid for reactive magnetizing power.
3. **Braking/Plugging Mode ($s > 1$)**: $N_r < 0$. Achieved by swapping two stator phases to reverse the field rotation. The rotor spins opposite to the field, producing massive counter-torque that rapidly brakes the load.

## Approximate Torque Equations (Standard)
_(26:26 - 31:42)_

In many practical exam problems, stator impedance ($R_1$ and $x_1$) is omitted or ignored. Under this assumption ($R_1 \to 0, x_1 \to 0$), the Thévenin parameters simplify to $V_{th} = V_1$, $R_{th} = 0$, and $X_{th} = 0$.

> [!success] Approximate Developed Torque Equation
> $$T_{\text{dev}} \approx \frac{3}{\omega_s} \frac{V_1^2 \left(\frac{r_2'}{s}\right)}{\left(\frac{r_2'}{s}\right)^2 + (x_2')^2}$$

This formula emphasizes a critical relationship: **$T_{\text{dev}} \propto V_1^2$**. A drop in supply voltage causes a severe reduction in developed torque. (Always assume a Delta connection for the stator unless specified otherwise, to maximize phase voltage $V_1$).

## Linear and Starting Approximations
_(31:47 - 39:52)_

### Low-Slip Linear Region ($0 < s \le s_{mT}$)
Near synchronous speed, slip $s$ is tiny. The resistance term dominates leakage reactance: $\frac{r_2'}{s} \gg x_2'$. 
The approximate torque equation further reduces:
$$T_{\text{dev}} \approx \frac{3}{\omega_s} \frac{V_1^2}{r_2'} s$$
In this operating region, **$T_{\text{dev}} \propto s$**. The torque-slip curve is a straight line.

### Starting Torque ($s = 1$)
At standstill, slip $s = 1$. The rotor leakage reactance usually dominates winding resistance ($r_2' \ll x_2'$). The approximate torque equation yields:
$$T_{\text{st}} \approx \frac{3}{\omega_s} \frac{V_1^2 r_2'}{(x_2')^2}$$
This shows the fundamental law: **$T_{\text{st}} \propto r_2'$**. High rotor resistance is required for high starting torque (which is why slip-ring motors use external rheostats).

---

## Summary and Key Takeaways

- Developed electromagnetic torque is obtained by dividing three-phase air gap power by synchronous angular velocity: $T_{\text{dev}} = P_G / \omega_s$.
- Thévenin reduction of the stator network yields $V_{th} \approx V_1 [X_m / (x_1 + X_m)]$, $R_{th} \approx R_1 [X_m / (x_1 + X_m)]$, and $X_{th} \approx x_1 [X_m / (x_1 + X_m)]$.
- The exact general torque formula is $T_{\text{dev}} = \frac{3}{\omega_s} \frac{V_{th}^2 (r_2'/s)}{(R_{th} + r_2'/s)^2 + (X_{th} + x_2')^2}$.
- An induction machine operates in motoring mode for $0 < s < 1$, generating mode for $s < 0$, and braking (plugging) mode for $s > 1$.
- Plugging is initiated by swapping two stator supply phases, making the stator field rotate opposite to the rotor and yielding slips between $1 < s \le 2$.
- Neglecting stator impedance ($R_1 = 0, x_1 = 0$) simplifies the torque equation to $T_{\text{dev}} = \frac{3}{\omega_s} \frac{V_1^2 (r_2'/s)}{(r_2'/s)^2 + (x_2')^2}$, showing $T_{\text{dev}} \propto V_1^2$.
- In the low-slip region ($0 \le s \le s_{mT}$), $r_2'/s \gg x_2'$, resulting in a linear torque-slip relationship: $T_{\text{dev}} \approx \frac{3}{\omega_s} \frac{V_1^2}{r_2'} s$.
- Starting torque ($s = 1$) is directly proportional to rotor circuit resistance: $T_{\text{st}} \propto r_2'$.

---

[← Lec 138: Losses and Efficiency of Induction Machines](Lecture_138_Losses_and_Efficiency_of_Induction_Machines.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 140: Torque Slip Characteristics 2 →](Lecture_140_Torque_Slip_Characteristics_2.md)
