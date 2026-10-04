---
title: "Stability and Testing of Induction Machines | L 41 | Electrical Machines | GATE 2022 | Ankit Goyal"
lecture: 145
topic: "Induction Machines"
duration: "00:49:20"
source: "https://www.youtube.com/watch?v=ZEl2jJIuEhU"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 144: Stability and Testing of Induction Motor](Lecture_144_Stability_and_Testing_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 146: Circle Diagram of Induction Motor →](Lecture_146_Circle_Diagram_of_Induction_Motor.md)

---

# Stability and Testing of Induction Machines | L 41 | Electrical Machines | GATE 2022 | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=ZEl2jJIuEhU
- **Duration**: 00:49:20
- **Compiled**: 2026-09-23

---

## Overview

This lecture solves quantitative problems on the testing, equivalent circuit parameters, and operating stability of three-phase induction motors. It explains how to interpret data from no-load and blocked-rotor tests to determine efficiency, maximum developed power, and starting torque. The discussion shows how AC skin effect modifies stator resistance and how no-load rotational losses are separated from winding losses. The lecture also covers operating point stability criteria on torque-speed curves and demonstrates exact rotor resistance calculation for speed control.

## Contents

- [[#Efficiency & Power Scaling|Efficiency & Power Scaling]]
- [[#Parameter Extraction & Maximum Power|Parameter Extraction & Maximum Power]]
- [[#Starting Torque & No-Load Loss Separation|Starting Torque & No-Load Loss Separation]]
- [[#Drive Stability Criteria|Drive Stability Criteria]]
- [[#Locked-Rotor Scaling & Exact Speed Control|Locked-Rotor Scaling & Exact Speed Control]]

---

## Efficiency & Power Scaling
_(00:02 - 10:39)_

**Problem 1: Full-Load Efficiency from Test Data**
Test data isolates fixed losses from variable copper losses:
- No-Load Power ($P_0$): Core loss + Friction & Windage.
- Blocked-Rotor Power ($P_{\text{br}}$): Total copper loss at test current.

To find full-load efficiency, scale the blocked-rotor copper loss to the full-load current ($P_{\text{cu}} \propto I^2$):
$$P_{\text{cu, FL}} = P_{\text{br}} \times \left(\frac{I_{\text{FL}}}{I_{\text{br}}}\right)^2$$
Then calculate total input power $P_{\text{in}} = P_{\text{out}} + P_0 + P_{\text{cu, FL}}$, and efficiency $\eta = P_{\text{out}} / P_{\text{in}}$.

## Parameter Extraction & Maximum Power
_(10:43 - 20:04)_

**Problem 2: Parameter Extraction (Delta Stator)**
For a delta-connected stator, convert line quantities to phase quantities ($V_{\text{ph}} = V_L$, $I_{\text{ph}} = I_L/\sqrt{3}$).
From blocked-rotor test data:
$$Z_{\text{br}} = \frac{V_{\text{ph}}}{I_{\text{ph, sc}}}$$
$$R_{01} = Z_{\text{br}} \cos\phi_{\text{sc}} \quad \text{and} \quad X_{01} = Z_{\text{br}} \sin\phi_{\text{sc}}$$
Assuming equal leakage distribution: $X_1 = X'_2 = X_{01}/2$. If stator resistance is neglected, $R'_2 \approx R_{01}$.

**Maximum Mechanical Power**:
Mechanical power is maximized when the fictitious load resistance equals the internal source impedance:
$$R'_2\left(\frac{1}{s_{mp}} - 1\right) = \sqrt{R_1^2 + (X_1 + X'_2)^2}$$
Solve for $s_{mp}$, then calculate the total circuit impedance and rotor current to find the maximum power.

## Starting Torque & No-Load Loss Separation
_(20:05 - 26:16)_

**Starting Torque**:
Standstill conditions are identical to the blocked-rotor test. The starting current scales directly with applied voltage:
$$I_{\text{st}} = I_{\text{sc}} \times \left(\frac{V_{\text{rated}}}{V_{\text{sc}}}\right)$$
Calculate the three-phase input power at starting. If stator losses are neglected, all input power is air-gap power ($P_g = P_{\text{in, st}}$). Starting torque is $T_{\text{st}} = P_g / \omega_s$.

**Problem 3: Rotational Loss Separation**:
When DC stator resistance is given, AC skin effect increases it:
$$R_{\text{ac}} = 1.2 \times R_{\text{dc}}$$
Calculate no-load stator copper loss ($3 I_{\text{ph0}}^2 R_{\text{ac}}$) and subtract it from the total no-load power to isolate rotational losses ($P_{\text{rotational}}$).

## Drive Stability Criteria
_(27:17 - 30:24)_

**Problem 4: Graphical Stability**
An operating point is stable if:
$$\frac{dT_L}{d\omega} > \frac{dT_m}{d\omega}$$
Graphically, evaluate the slopes of the motor and load torque curves at their intersections. If any positive speed disturbance creates a net decelerating torque ($T_L > T_m$), the operating point is stable.

## Locked-Rotor Scaling & Exact Speed Control
_(30:24 - 45:30)_

**Problem 5: Frequency/Voltage Scaling on Locked-Rotor**
Under blocked-rotor conditions, leakage reactance dominates resistance ($X_{\text{br}} \gg R_{\text{br}}$). Thus, impedance scales proportionally with frequency:
$$X_{\text{br}} \propto f$$
If supply frequency increases, reactance increases, causing the locked-rotor current to decrease even if voltage increases slightly.

**Problem 6: Exact Rotor Resistance for Speed Control**
When stator impedance is known from test data, the exact torque equation must be used to find the required external rotor resistance to change speed at constant torque:
$$T = \frac{3}{\omega_s} \times \frac{V_1^2 \left(R'_2 / s\right)}{\left(R_1 + \frac{R'_2}{s}\right)^2 + X_{\text{eq}}^2}$$
Equating the torque expressions for the initial and final slips produces a quadratic equation in terms of the total rotor resistance $R'_{\text{total}}$. The required external resistance is $R_{\text{ext}} = R'_{\text{total}} - R'_2$.

---

## Summary and Key Takeaways

- No-load test input power $P_0$ represents core loss plus mechanical friction and windage when stator copper loss is neglected.
- Blocked-rotor test power $P_{\text{br}}$ represents total copper losses at standstill, scaling with the square of current as $P_{\text{cu}} \propto I^2$.
- Measured DC stator resistance must be converted to AC resistance using the skin effect factor $R_{\text{ac}} = k \cdot R_{\text{dc}}$.
- Stator copper loss cannot be ignored at no-load when computing rotational losses precisely, because $I_0$ reaches $30\%$ to $35\%$ of rated current.
- Maximum mechanical power develops when the fictitious mechanical load resistance matches the source impedance: $R'_2\left(\frac{1}{s}-1\right) \approx X_{01}$.
- Starting torque equals total active input power at standstill divided by synchronous speed: $T_{\text{st}} = \frac{P_{\text{in, st}}}{\omega_s}$ when stator losses are neglected.
- When power factor is omitted in blocked-rotor data, series leakage reactance dominates resistance ($X_{\text{br}} \gg R_{\text{br}}$) and scales proportionally with supply frequency.
- An operating point on a torque-speed characteristic is stable if and only if $\frac{dT_L}{d\omega} > \frac{dT_m}{d\omega}$.
- Exact calculation of external rotor resistance for speed control at constant torque requires solving a quadratic equation that accounts for stator impedance.

---

[← Lec 144: Stability and Testing of Induction Motor](Lecture_144_Stability_and_Testing_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 146: Circle Diagram of Induction Motor →](Lecture_146_Circle_Diagram_of_Induction_Motor.md)
