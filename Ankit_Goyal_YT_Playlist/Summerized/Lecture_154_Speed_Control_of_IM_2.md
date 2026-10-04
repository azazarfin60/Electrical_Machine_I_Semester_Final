---
title: "Speed Control of IM - 2 | L 45 | Electrical Machines | GATE 2022 | Ankit Goyal"
lecture: 154
topic: "Induction Machines"
duration: "00:45:46"
source: "https://www.youtube.com/watch?v=N7RmYwEDxh0"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 153: Speed Control of IM 1](Lecture_153_Speed_Control_of_IM_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 155: Braking of Induction Motor →](Lecture_155_Braking_of_Induction_Motor.md)

---

# Speed Control of IM - 2 | L 45 | Electrical Machines | GATE 2022 | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=N7RmYwEDxh0
- **Duration**: 00:45:46
- **Compiled**: 2026-09-23

---

## Overview

This lecture solves quantitative problems across multiple induction motor speed control techniques. It begins with frequency variation under fixed voltage and analyzes rotor EMF injection for sub-synchronous and super-synchronous operation. The discussion details stator voltage control penalties, evaluating rotor ohmic loss increase and power factor degradation under constant torque loads. It concludes with frequency shifts in breakdown torque, cumulative cascade set speed calculations, and autotransformer starting current quadratic scaling.

## Contents

- [[#V/f Flux Scaling & EMF Injection Constraints|V/f Flux Scaling & EMF Injection Constraints]]
- [[#Rotor Resistance & Stator Voltage Control Variations|Rotor Resistance & Stator Voltage Control Variations]]
- [[#V/f Torque Shifts and Cascade Slip Relations|V/f Torque Shifts and Cascade Slip Relations]]
- [[#Autotransformer Current Scaling|Autotransformer Current Scaling]]

---

## V/f Flux Scaling & EMF Injection Constraints
_(00:00 - 14:56)_

- **Flux Scaling**: Air gap flux density scales directly with the terminal voltage-to-frequency ratio ($B_m \propto V/f$). If supply frequency is reduced without lowering the applied voltage, the core becomes heavily saturated, severely increasing magnetizing current.
- **Rotor EMF Injection**: To maintain constant torque, the condition $I_2 \cos \theta_2 = \text{constant}$ must be satisfied. Setting up the equation before and after injection yields a quadratic in slip $s$:
  $$\frac{s_1 E_2 R_2}{R_2^2 + (s_1 X_2)^2} = \frac{s E_2 \pm E_i}{R_2^2 + (s X_2)^2}$$
  The two roots represent **sub-synchronous** ($s > 0$) and **super-synchronous** ($s < 0$) operating modes. The injected frequency must strictly match the rotor slip frequency ($f_{\text{injected}} = sf$).

## Rotor Resistance & Stator Voltage Control Variations
_(10:00 - 24:55)_

- **Rotor Resistance**: Under constant torque, $s / R_{\text{rotor}} = \text{constant}$. Adding resistance increases slip and reduces speed.
- **Stator Voltage Control**: Under constant torque, slip is inversely proportional to voltage squared: $s_2 = s_1 (V_1/V_2)^2$.
  - **Penalty 1 (Heating)**: Air gap power $P_g$ remains constant, but since $P_{cu} = s P_g$, rotor copper losses increase directly with the higher slip.
  - **Penalty 2 (Power Factor)**: The rotor impedance phase angle is $\tan \phi = s X_2 / R_2$. As slip increases, the impedance becomes more inductive, worsening the power factor.

## V/f Torque Shifts and Cascade Slip Relations
_(24:58 - 34:52)_

- **Frequency Shifts**: Rotor leakage reactance scales with frequency ($X_2 \propto f$). Therefore, the slip for maximum torque scales inversely with frequency: $s_{mT} = R_2/X_2 \propto 1/f$. When supply frequency drops, the speed at which maximum torque occurs shifts significantly.
- **Constant V/f Invariant**: In the stable low-slip region, for a constant torque load, the absolute slip speed difference remains invariant across all frequencies: $N_s - N_r = \text{constant}$.
- **Cascade Slips**: In a cumulative cascade set, the mechanical speeds match. Using $N_1 = N_2$ yields:
  $$\frac{1 - s_1}{P_1} = \frac{s_1(1 - s_2)}{P_2}$$
  If the final rotor frequency $f_2'$ is known, we use $f_2' = s_1 s_2 f$.

## Autotransformer Current Scaling
_(34:57 - 45:36)_

For an autotransformer starter with tapping ratio $x$:
- The voltage applied to the motor is $x V_{\text{rated}}$.
- The starting current **at the motor terminals** scales linearly: $I_{\text{motor}} = x I_{\text{direct}}$.
- By power balance across the ideal transformer, the starting current drawn **from the main supply** scales quadratically: $I_{\text{line}} = x^2 I_{\text{direct}}$.

---

## Summary and Key Takeaways

- Air gap flux density scales directly with the terminal voltage-to-frequency ratio $B_m \propto V/f$, causing core saturation if supply frequency is reduced without lowering applied voltage.
- Under constant load torque, rotor EMF injection maintains constant air gap power, enforcing $I_2 \cos \theta_2 = \text{constant}$ and yielding two operating slips corresponding to sub-synchronous and super-synchronous motoring.
- In the low-slip linear region, rotor resistance control maintains constant torque by preserving the ratio $s / R_{\text{rotor}} = \text{constant}$.
- Stator voltage control at constant torque forces operating slip to scale inversely with voltage squared according to $s \propto 1/V^2$.
- Rotor ohmic copper loss increases in direct proportion to operating slip under constant torque: $P_{cu} = s P_g$.
- Slip for maximum torque scales inversely with frequency ($s_{mT} \propto 1/f$), causing peak torque speed to shift when supply frequency changes.
- In a cumulative cascaded set, mechanical speeds match according to $(1 - s_1)/P_1 = (s_1 - s_1 s_2)/P_2$ with auxiliary rotor frequency given by $f_2' = s_1 s_2 f$.
- In constant $V/f$ drives driving constant torque loads, the absolute slip speed difference remains invariant across frequencies: $N_s - N_r = \text{constant}$.
- Autotransformer starting reduces motor terminal current by tapping ratio $x$, while the current drawn from the supply scales by $x^2$.

---

[← Lec 153: Speed Control of IM 1](Lecture_153_Speed_Control_of_IM_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 155: Braking of Induction Motor →](Lecture_155_Braking_of_Induction_Motor.md)
