---
title: "Speed Control of Induction Motor-1 | Electrical Machines | Lec 107 | GATE/ESE Electrical Engineering"
lecture: 151
topic: "Induction Machines"
duration: "00:41:30"
source: "https://www.youtube.com/watch?v=DdEmZwgmY6c"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 150: Starting of SRIM](Lecture_150_Starting_of_SRIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 152: Speed Control of Induction Motor 2 →](Lecture_152_Speed_Control_of_Induction_Motor_2.md)

---

# Speed Control of Induction Motor-1 | Electrical Machines | Lec 107 | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=DdEmZwgmY6c
- **Duration**: 00:41:30
- **Compiled**: 2026-09-23

---

## Overview

This lecture introduces the principles of speed control in three-phase induction motors with a focus on slip control techniques. It contrasts constant torque and constant power operating regimes and classifies methods into slip control and synchronous speed control. The lecture analyzes stator voltage control and rotor resistance control, deriving operating slip formulas under constant torque and quadratic fan loads. It also explains the rotor EMF injection method, detailing the frequency matching criterion and how injected phase angles enable sub-synchronous and super-synchronous speeds.

## Contents

- [[#Drive Regimes & Classification|Drive Regimes & Classification]]
- [[#Stator Voltage Control|Stator Voltage Control]]
- [[#Rotor Resistance Control|Rotor Resistance Control]]
- [[#Rotor EMF Injection Method|Rotor EMF Injection Method]]

---

## Drive Regimes & Classification
_(00:13 - 07:07)_

**Operating Regimes**:
- **Below Base Speed (Constant Torque)**: Torque remains constant. Power increases linearly with speed ($P = T \omega \propto N$).
- **Above Base Speed (Constant Power)**: Voltage cannot exceed rated limits, so flux is weakened. Torque falls inversely with speed ($T \propto 1/N$).

**Speed Control Classification** ($N = N_s(1-s)$):
1. **Slip Control Methods** (Varies $s$, keeps $N_s$ constant):
   - Stator Voltage Control
   - Rotor Resistance Control
   - Rotor EMF Injection
2. **Synchronous Speed Control Methods** (Varies $N_s$):
   - Frequency Control ($v/f$ control)
   - Pole Changing (Applicable only to squirrel-cage motors)

## Stator Voltage Control
_(07:07 - 19:30)_

Applicable to both squirrel-cage and slip-ring motors. At low slips, torque simplifies to:
$$T \approx \frac{3}{\omega_s} \frac{s V_1^2}{R_2'}$$

- **Constant Torque Load ($T = \text{const}$)**:
  $s V_1^2 = \text{const} \implies s \propto 1/V_1^2$
  Reducing $V_1$ increases $s$ (lowers speed). However, stator current becomes $I \propto 1/V_1$. A voltage reduction causes currents to rise dangerously, leading to severe overheating ($I^2R$). Thus, speed reduction is practically limited to $10\%-15\%$ for brief periods.
- **Fan Load ($T \propto N^2$)**:
  $$ \frac{s_1 V_1^2}{s_2 V_2^2} = \left(\frac{1 - s_1}{1 - s_2}\right)^2 $$

*Note: Since voltage cannot exceed rated value, this method only provides speeds below base speed.*

## Rotor Resistance Control
_(19:34 - 29:25)_

Applicable only to slip-ring motors (wound rotor) by adding external resistance $R_E$ to the rotor circuit.

- **Constant Torque Load**:
  $$\frac{s}{R_2 + R_E} = \text{const} \implies s_2 = s_1 \left(\frac{R_2 + R_E}{R_2}\right)$$
  Adding $R_E$ increases slip, lowering speed. Rotor current remains constant ($I \approx s V_1 / (R_2 + R_E) = \text{const}$).
- **Drawbacks**:
  - The $I^2(R_2 + R_E)$ copper losses are huge. Efficiency drops proportionally with speed ($\eta \approx 1-s$).
  - Poor speed regulation (torque-speed curve becomes very flat).
  - Can only provide speeds below base speed.

## Rotor EMF Injection Method
_(29:27 - 41:18)_

An external voltage $E_i$ is injected into the rotor via slip rings.
- **Frequency Matching**: The injected voltage frequency must exactly equal the rotor slip frequency ($f_{\text{inj}} = sf$).
- **Torque Invariance**: For constant load torque, $I_2 \cos\theta_2 = \text{constant}$.
  $$\frac{s_1 E_2}{R_2^2 + (s_1 X_2)^2} = \frac{s_2 E_2 \pm E_i}{R_2^2 + (s_2 X_2)^2}$$
- **Operating Modes**:
  - **Sub-synchronous ($N < N_s$)**: $E_i$ is in phase opposition to $sE_2$ (net voltage drops, slip increases).
  - **Super-synchronous ($N > N_s$)**: $E_i$ is in phase with $sE_2$ (net voltage increases, slip becomes negative).
  Unlike previous methods, this can drive the motor *above* synchronous speed.

---

## Summary and Key Takeaways

- Motor drives run as constant torque drives below base speed with $T = \text{constant}$, and as constant power drives above base speed where torque falls as $T \propto \frac{1}{N}$.
- At low slips ($s \ll 1$), induction motor torque approximates as $T \approx \frac{3}{\omega_s} \frac{s V_1^2}{R_2'}$.
- For a constant torque load, stator voltage control requires $s V_1^2 = \text{constant}$, which causes stator current to rise inversely as $I \propto \frac{1}{V_1}$, restricting voltage control to narrow ranges and short-duty cycles.
- For fan loads under voltage control, speed obeys the ratio $\frac{s_1 V_1^2}{s_2 V_2^2} = \left(\frac{1 - s_1}{1 - s_2}\right)^2$.
- In slip ring induction motors, adding external rotor resistance $R_E$ shifts operating slip to $s_2 = s_1 \left(\frac{R_2 + R_E}{R_2}\right)$, but causes large $I^2 R$ copper losses, lowered efficiency, and degraded speed regulation.
- The rotor EMF injection method requires the injected voltage frequency to strictly equal the rotor slip frequency ($f_{\text{inj}} = s f$).
- Under rotor EMF injection with constant torque, the operating point satisfies $I_2 \cos\theta_2 = \text{constant}$, enabling sub-synchronous operation when injected in phase opposition and super-synchronous operation when injected in phase.

---

[← Lec 150: Starting of SRIM](Lecture_150_Starting_of_SRIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 152: Speed Control of Induction Motor 2 →](Lecture_152_Speed_Control_of_Induction_Motor_2.md)
