---
title: "Electrical Machines | Lec 108 | Speed Control of Induction Motor-2 | GATE/ESE Electrical Engineering"
lecture: 152
topic: "Induction Machines"
duration: "00:43:42"
source: "https://www.youtube.com/watch?v=zF5WSpRLA_Q"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 151: Speed Control of Induction Motor 1](Lecture_151_Speed_Control_of_Induction_Motor_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 153: Speed Control of IM 1 →](Lecture_153_Speed_Control_of_IM_1.md)

---

# Electrical Machines | Lec 108 | Speed Control of Induction Motor-2 | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=zF5WSpRLA_Q
- **Duration**: 00:43:42
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines synchronous speed control methods for three-phase induction motors. It focuses on variable frequency control below and above base speed using power electronic inverters. The lecture details the torque-speed characteristics under constant $V/f$ control, drive capability regions, and low-frequency voltage boost. It also covers discrete speed adjustment through consequent pole changing in squirrel cage machines. Finally, it analyzes slip power recovery through cumulative and differential cascading of induction and synchronous machines.

## Contents

- [[#Constant V/f Control (Below Base Speed)|Constant V/f Control (Below Base Speed)]]
- [[#Field Weakening (Above Base Speed)|Field Weakening (Above Base Speed)]]
- [[#Low Frequency Voltage Boost|Low Frequency Voltage Boost]]
- [[#Pole Changing Method|Pole Changing Method]]
- [[#Cascading & Slip Power Recovery|Cascading & Slip Power Recovery]]

---

## Constant V/f Control (Below Base Speed)
_(00:12 - 09:45)_

To control speed below the rated base speed, supply frequency is reduced. However, flux is proportional to $V/f$. If $V$ is kept constant while $f$ drops, the core will saturate. 
> [!success] V/f Control
> To prevent saturation, voltage must be reduced proportionally with frequency, maintaining a constant $V/f$ ratio.

**Torque Characteristics**:
- **Maximum Torque**: $T_{\max} \propto (V/f)^2$. Since $V/f$ is constant, the maximum breakdown torque remains **constant**.
- **Starting Torque**: $T_{st} \propto (V/f)^2 \cdot (1/f)$. Since $V/f$ is constant, starting torque increases as frequency decreases ($T_{st} \propto 1/f$).
- **Slip Speed**: For a constant load torque, the absolute slip speed in rpm ($N_s - N_r$) remains **constant** across all frequencies.

## Field Weakening (Above Base Speed)
_(09:47 - 19:20)_

To run above base speed, supply frequency is increased beyond rated frequency. However, terminal voltage cannot be increased beyond rated voltage to avoid insulation failure.
- **Voltage**: Remains constant at $V_{\text{rated}}$.
- **Flux**: Drops ($\Phi \propto V_{\text{rated}}/f \propto 1/f$).
- **Maximum Torque**: $T_{\max} \propto V_{\text{rated}}^2 / f^2 \propto 1/f^2$.
- **Starting Torque**: $T_{st} \propto 1/f^3$.

The motor operates in the **Constant Power Region**, where torque capability falls hyperbolically with speed, while power capability remains capped at the rated value.

## Low Frequency Voltage Boost
_(19:20 - 24:04)_

At very low supply frequencies, the stator leakage reactance $X_1$ drops near zero, and the stator resistance $R_1$ dominates the impedance drop.
Because of the significant $I_1 R_1$ drop, the induced air gap EMF $E_1$ becomes much less than $V_1$.
Thus, $E_1/f$ drops, causing a loss of core flux and torque capability.
> [!info] Voltage Boost
> To compensate for the $I_1R_1$ drop, an additional voltage offset (boost) must be added at low frequencies so that $V_1 = I_1R_1 + kf$. This maintains $E_1/f$ constant.

## Pole Changing Method
_(24:05 - 28:43)_

Applicable *only* to squirrel cage induction motors (as squirrel cages automatically adapt to any number of stator poles). 
By switching stator coil connections from series-aiding to series-opposing, the number of magnetic poles can be doubled (from $P$ to $2P$) using the principle of **consequent poles**.
This allows discrete speed control, effectively halving the synchronous speed.

## Cascading & Slip Power Recovery
_(28:43 - 43:31)_

The electrical power transferred across the air gap into the rotor is $P_g$. It splits into mechanical power $(1-s)P_g$ and electrical power $sP_g$.
Instead of wasting $sP_g$ as heat in rotor resistance, it can be recovered.

**Cascaded Induction Motors**:
Two motors mechanically coupled on the same shaft. Motor 1 (must be a slip-ring motor) is fed from the mains. Its slip rings feed the stator of Motor 2 at slip frequency $f_2 = s_1 f_1$.
- **Cumulative Cascading**: Both stators produce torque in the same direction. The set runs at a speed equivalent to $(P_1 + P_2)$ poles:
  $$N_{\text{set}} = \frac{120 f_1}{P_1 + P_2}$$
- **Differential Cascading**: Motor 2's phase sequence is reversed, opposing Motor 1. The set runs at a speed equivalent to $|P_1 - P_2|$ poles:
  $$N_{\text{set}} = \frac{120 f_1}{|P_1 - P_2|}$$

If cascaded with a **synchronous machine**, the entire set locks to the strict synchronous speed defined by the synchronous machine's poles.

---

## Summary and Key Takeaways

- Below base speed ($f < f_{\text{rated}}$), maintaining a constant ratio of terminal voltage to frequency ($V/f = \text{constant}$) keeps air gap core flux constant and prevents magnetic saturation.
- Under constant $V/f$ control below base speed, maximum breakdown torque remains constant ($T_{\max} = \text{constant}$), while starting torque increases inversely with frequency ($T_{st} \propto 1/f$).
- For any constant torque mechanical load operating below base speed under constant $V/f$ control, the slip speed remains constant: $N_s - N_r = \text{constant}$.
- Above base speed ($f > f_{\text{rated}}$), terminal voltage is clamped at rated voltage to protect winding insulation, so the motor enters the field-weakening constant power region where $T_{\max} \propto 1/f^2$.
- At low stator frequencies, the series stator resistance drop $I_1 R_1$ can no longer be neglected, requiring an intentional voltage boost to keep air gap induced EMF $E_1/f$ constant.
- The pole changing method alters synchronous speed by switching stator coil polarities in a 2:1 ratio using consequent poles, and this technique applies exclusively to squirrel cage induction motors.
- The total power crossing the air gap divides into mechanical power $(1 - s) P_g$ and rotor electrical power $s P_g$, which can be recovered rather than wasted as heat.
- Two mechanically coupled induction motors operating in cumulative cascading run at a set synchronous speed corresponding to total effective poles: $N_{\text{set}} = \frac{120 f_1}{P_1 + P_2}$.
- When cascaded in differential mode with reversed phase sequence, the set synchronous speed corresponds to the pole difference: $N_{\text{set}} = \frac{120 f_1}{|P_1 - P_2|}$.

---

[← Lec 151: Speed Control of Induction Motor 1](Lecture_151_Speed_Control_of_Induction_Motor_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 153: Speed Control of IM 1 →](Lecture_153_Speed_Control_of_IM_1.md)
