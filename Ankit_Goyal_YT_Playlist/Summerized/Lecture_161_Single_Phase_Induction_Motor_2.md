---
title: "Electrical Machines | Lec 113 | Single Phase Induction Motor-2 | GATE/ESE Electrical Engineering"
lecture: 161
topic: "Induction Machines"
duration: "00:49:18"
source: "https://www.youtube.com/watch?v=68N1xTckLjU"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 160: Single Phase Induction Motor 1](Lecture_160_Single_Phase_Induction_Motor_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 162: Single Phase Induction Motor →](Lecture_162_Single_Phase_Induction_Motor.md)

---

# Electrical Machines | Lec 113 | Single Phase Induction Motor-2 | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=68N1xTckLjU
- **Duration**: 00:49:18
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines starting methods and performance optimization for single-phase induction motors. It explains how phase-splitting creates an asymmetric pair of forward and backward revolving magnetic fields to produce starting torque. The discussion analyzes resistance split-phase motors, capacitor-start motors, permanent-split capacitor motors, and two-value capacitor motors. Mathematical conditions are derived for creating a pure rotating magnetic field and for maximizing starting torque. Finally, analytical and shortcut techniques are established to determine the direction of rotor rotation.

## Contents

- [[#Resistance Split-Phase Motors|Resistance Split-Phase Motors]]
- [[#Capacitor Motors and Operating Conditions|Capacitor Motors and Operating Conditions]]
- [[#Direction of Rotation|Direction of Rotation]]

---

## Resistance Split-Phase Motors
_(00:13 - 17:15)_

To make a single-phase induction motor self-starting, a second **auxiliary winding** is added in space quadrature ($90^\circ$ electrical) to the **main winding**. 
- **Main Winding**: Deep slots, thick wire. Low resistance ($R_m$), high reactance ($X_m$). Current $I_m$ lags $V_1$ by a large angle $\phi_m$.
- **Auxiliary Winding**: Shallow slots, thin wire. High resistance ($R_a$), low reactance ($X_a$). Current $I_a$ lags $V_1$ by a small angle $\phi_a$.
- **Starting**: The difference in impedance ratios creates a phase difference $\alpha = \phi_m - \phi_a \approx 20^\circ-30^\circ$ between the two currents. This phase difference causes the forward revolving field $B_f$ to become stronger than the backward revolving field $B_b$, generating a net positive starting torque.
- **Running**: A centrifugal switch opens at $75\%-80\%$ of synchronous speed, disconnecting the auxiliary winding. The motor then runs as a pure single-phase motor.

## Capacitor Motors and Operating Conditions
_(17:15 - 39:40)_

To increase starting torque and eliminate the backward rotating field entirely, a capacitor is placed in series with the auxiliary winding. This makes the auxiliary branch capacitive, so $I_a$ *leads* $V_1$ while $I_m$ *lags* $V_1$.
- **Capacitor-Start**: Centrifugal switch disconnects the capacitor and auxiliary winding at $75\%-80\%$ speed.
- **Permanent-Split Capacitor (Capacitor-Run)**: No switch. Capacitor stays in circuit, providing balanced two-phase running, high efficiency, and quiet operation (no pulsating torque).
- **Two-Value Capacitor (Capacitor-Start Capacitor-Run)**: Uses a large short-time starting capacitor $C_s$ (switched out) in parallel with a smaller continuous running capacitor $C_r$ to optimize both starting torque and running performance.

**Optimizing the Capacitor**:
1. **Condition for Pure Rotating Magnetic Field (No Backward Field)**:
   The two currents must be in exact time quadrature ($\phi_m + \phi_a = 90^\circ$).
   Required capacitive reactance: $X_c = X_a + R_a \left(\frac{R_m}{X_m}\right)$
2. **Condition for Maximum Starting Torque**:
   Starting torque $T_{\text{start}} \propto I_m I_a \sin(\phi_m + \phi_a)$. Because increasing $X_c$ alters both the angle $\phi_a$ and the current magnitude $I_a$, maximum torque occurs when:
   $$\phi_a = \frac{90^\circ - \phi_m}{2}$$

## Direction of Rotation
_(39:40 - 49:10)_

The direction of rotor rotation is identical to the direction of the rotating magnetic field.
- **The Shortcut Rule**: Trace the shortest physical path along the stator periphery from the axis of the **leading current winding** to the axis of the **lagging current winding**. The physical direction of this trace (e.g., clockwise) is the direction of rotation.
- **Reversal**: To reverse the direction of rotation, reverse the terminal connections of **either** the main winding or the auxiliary winding (but not both).

---

## Summary and Key Takeaways

- Standstill single-phase motors lack starting torque because equal and opposite forward and backward rotating magnetic fields cancel each other.
- Resistance split-phase motors use an auxiliary winding with high resistance and low reactance to create an initial phase difference $\alpha \approx 20^\circ \text{ to } 30^\circ$.
- A centrifugal switch opens at approximately $75\%\text{--}80\%$ of synchronous speed, disconnecting the auxiliary circuit in split-phase and capacitor-start motors.
- Pure time quadrature ($\alpha = 90^\circ$) eliminates the backward revolving field and requires series capacitive reactance $X_c = X_a + R_a (R_m / X_m)$.
- Maximum starting torque requires a different condition: $\phi_a = (90^\circ - \phi_m) / 2$, which accounts for variations in both auxiliary current magnitude and phase angle.
- Permanent-split capacitor motors omit the centrifugal switch to maintain balanced two-phase operation, lower acoustic noise, and improved running power factor.
- Two-value capacitor motors use a large electrolytic start capacitor ($C_s$) in parallel with a smaller continuous-duty run capacitor ($C_r$) to achieve high starting torque and smooth running.
- In space, the rotor rotates from the axis of the leading current winding toward the axis of the lagging current winding along the shortest angle.
- Reversing the terminal connections of either the main winding or the auxiliary winding reverses the direction of rotor rotation.

---

[← Lec 160: Single Phase Induction Motor 1](Lecture_160_Single_Phase_Induction_Motor_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 162: Single Phase Induction Motor →](Lecture_162_Single_Phase_Induction_Motor.md)
