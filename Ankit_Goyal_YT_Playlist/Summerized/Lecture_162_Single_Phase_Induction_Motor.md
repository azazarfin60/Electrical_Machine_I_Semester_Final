---
title: "Single Phase Induction Motor | L 48 | Electrical Machines | GATE 2022 | Ankit Goyal"
lecture: 162
topic: "Induction Machines"
duration: "00:49:06"
source: "https://www.youtube.com/watch?v=cOLfgO5qF9U"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 161: Single Phase Induction Motor 2](Lecture_161_Single_Phase_Induction_Motor_2.md) | [🏠 Index](00_yt_study_guide.md)

---

# Single Phase Induction Motor | L 48 | Electrical Machines | GATE 2022 | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=cOLfgO5qF9U
- **Duration**: 00:49:06
- **Compiled**: 2026-09-23

---

## Overview

This lecture solves representative GATE and ESE numerical problems on single-phase induction motors. It covers equivalent circuit analysis at no-load and full-load slip, input impedance calculations, and power factor determination. The discussion analyzes the double revolving field theory, rotor frequency ratios, and air-gap flux asymmetry. Finally, it demonstrates exact methods to determine rotor rotation direction and derives capacitance criteria for both space-time quadrature and maximum starting torque.

## Contents

- [[#Equivalent Circuit & Numerical Analysis|Equivalent Circuit & Numerical Analysis]]
- [[#Direction of Rotation Application|Direction of Rotation Application]]
- [[#Capacitance Optimization Problems|Capacitance Optimization Problems]]

---

## Equivalent Circuit & Numerical Analysis
_(00:00 - 06:53, 32:03 - 41:59)_

**No-Load Approximation ($s \approx 0$)**:
At no-load, the forward slip is nearly zero. The forward rotor branch resistance $\frac{R_2'}{2s} \to \infty$, acting as an open circuit. Only the forward magnetizing branch $j\frac{X_m}{2}$ carries current. The backward slip $s_b \approx 2$, so the backward rotor branch resistance is $\frac{R_2'}{4}$, which is very small. This effectively shorts out the backward magnetizing branch. Thus, the motor draws a large lagging magnetizing current, leading to a very poor no-load power factor (e.g., $\text{pf} \approx 0.1\text{ lagging}$).

**Full-Load Operation ($s = 0.05$ to $0.1$)**:
Under load, both the forward parallel branch $Z_f$ and the backward parallel branch $Z_b$ must be evaluated using their respective slips $s$ and $2-s$. The total input impedance is $Z_{\text{in}} = (R_1 + jX_1) + Z_f + Z_b$. Because $Z_f \gg Z_b$ during forward running, the forward air-gap flux is much larger than the backward flux.
- **Rotor Frequency Ratio**: The ratio of the frequencies of the induced rotor currents is exactly the ratio of the slips: $\frac{f_f}{f_b} = \frac{s}{2-s}$.

## Direction of Rotation Application
_(11:36 - 21:29)_

The "Leading-to-Lagging Rule" is applied to practical circuit values:
1. Calculate the phase angle of the main current: $\theta_m = \tan^{-1}(X_m/R_m)$ lagging.
2. Calculate the phase angle of the auxiliary current: $\theta_a$ (could be lagging for split-phase, or leading for capacitor-start).
3. Identify which current leads the other in time.
4. The motor rotates from the spatial axis of the leading-current winding toward the spatial axis of the lagging-current winding.

If $\theta_m \approx \theta_a$ (e.g., both around $85^\circ$), the phase difference $\alpha = |\theta_m - \theta_a|$ is very small ($< 10^\circ$). The starting torque, being proportional to $\sin\alpha$, will be practically zero and the motor will fail to start.

## Capacitance Optimization Problems
_(21:31 - 27:06, 42:03 - 49:01)_

Numerical problems highlight the difference between the two capacitor sizing criteria:

1. **For Pure Rotating Magnetic Field (Quadrature)**:
   Requires $\phi_m + \phi_a = 90^\circ$.
   Formula: $X_c = X_a + R_a\left(\frac{R_m}{X_m}\right)$

2. **For Maximum Starting Torque**:
   Requires optimizing the product $I_a \sin(\phi_m + \phi_a)$.
   Formula: $\phi_a = \frac{90^\circ - \phi_m}{2}$.
   Using $\tan\phi_a = \frac{X_c - X_a}{R_a}$, we solve for the required $X_c$.

The capacitance value required for maximum starting torque is generally lower than the value required for perfect quadrature.

---

## Summary and Key Takeaways

- At no-load synchronous speed ($s \approx 0$), the forward rotor branch resistance $\frac{R_2'}{2s}$ becomes an open circuit, causing the forward branch to draw purely magnetizing reactive current.
- The no-load power factor of a single-phase induction motor is very low and lagging ($\text{pf} \approx 0.1\text{ lagging}$) due to the large magnetizing branch requirement.
- In double revolving field theory, a single-phase pulsating MMF decomposes into two counter-rotating fields, each of magnitude $\frac{F_m}{2}$, rotating at synchronous speed $\pm N_s$.
- Physical rotor rotation always proceeds from the space axis of the leading current winding toward the space axis of the lagging current winding along the shortest spatial displacement.
- In split-phase motors, a minimum phase difference $\alpha \ge 20^\circ \text{ to } 30^\circ$ is essential to produce sufficient starting torque; angular differences under $10^\circ$ produce negligible torque.
- The forward-to-backward rotor current frequency ratio is $\frac{f_f}{f_b} = \frac{s_f}{2 - s_f}$, which also governs the ratio of induced rotor EMFs.
- Series capacitance required for pure $90^\circ$ time-phase displacement is $X_c = X_a + R_a \left(\frac{R_m}{X_m}\right)$.
- Series capacitance required for maximum starting torque is governed by the distinct condition $\phi_a = \frac{90^\circ - \phi_m}{2}$.
- Two-value capacitor motors retain a run capacitor under continuous operation, maintaining balanced two-phase running conditions with high efficiency and power factor.

---

[← Lec 161: Single Phase Induction Motor 2](Lecture_161_Single_Phase_Induction_Motor_2.md) | [🏠 Index](00_yt_study_guide.md)
