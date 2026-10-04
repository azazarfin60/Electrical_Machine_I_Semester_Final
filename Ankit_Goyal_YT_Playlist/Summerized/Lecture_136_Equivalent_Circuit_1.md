---
title: "Equivalent Circuit - 1 | Electrical Machines | Lec 98 | GATE/ESE (EE, ECE) | Ankit Goyal"
lecture: 136
topic: "Induction Machines"
duration: "00:44:11"
source: "https://www.youtube.com/watch?v=DyAQgR3A1fY"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 135: Rotating Magnetic Field](Lecture_135_Rotating_Magnetic_Field.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 137: Equivalent Circuit 2 →](Lecture_137_Equivalent_Circuit_2.md)

---

# Equivalent Circuit - 1 | Electrical Machines | Lec 98 | GATE/ESE (EE, ECE) | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=DyAQgR3A1fY
- **Duration**: 00:44:11
- **Compiled**: 2026-09-23

---

## Overview

This lecture establishes the equivalent circuit and power flow equations of three-phase induction machines. It begins by examining space-phasor diagrams under both motoring and generating regimes. The lecture shows how rotor electrical parameters vary with slip. Then it develops the transformed rotor circuit operating at constant stator line frequency. Finally, it analyzes the division of air-gap power into copper losses and gross mechanical power.

## Contents

- [[#Air-Gap Flux and Torque Equation|Air-Gap Flux and Torque Equation]]
- [[#Rotor Equivalent Circuit (Slip Dependent)|Rotor Equivalent Circuit (Slip Dependent)]]
- [[#The Transformed Rotor Circuit|The Transformed Rotor Circuit]]
- [[#Power Flow and Air-Gap Power ($P_{\text{ag}}$)|Power Flow and Air-Gap Power ($P_{\text{ag}}$)]]
- [[#Torque Formulations and Shaft Power|Torque Formulations and Shaft Power]]

---

## Air-Gap Flux and Torque Equation
_(00:14 - 13:11)_

The stator and rotor flux waves combine to form the **resultant mutual air-gap flux** $\vec{\Phi}_r = \vec{\Phi}_1 + \vec{\Phi}_2$. This mutual flux induces EMF in both windings.

The electromagnetic torque is developed as the rotor flux tries to align with the stator flux (or resultant flux).
- **Torque Equation**: $T_e \propto \Phi_r \Phi_2 \cos\theta_2$
  where $\theta_2 = \tan^{-1}(X_2/R_2)$ is the rotor impedance angle.
- **Maximum Torque per Ampere**: Achieved when $\theta_2 \to 0$ ($\cos\theta_2 \to 1$). This requires negligible rotor leakage reactance ($X_2 \ll R_2$).
- **Generator Mode**: Driven above synchronous speed ($s < 0$), the rotor current physically reverses. The electromagnetic torque now opposes the direction of prime mover rotation.

## Rotor Equivalent Circuit (Slip Dependent)
_(13:15 - 18:47)_

At standstill ($s=1$), the rotor frequency equals line frequency ($f_r = f$). The rotor acts exactly like a shorted transformer secondary:
- Induced EMF: $E_2 = 4.44 f N_{ph2} K_{w2} \Phi_m$
- Leakage Reactance: $X_2 = 2\pi f L_2$
- Resistance: $R_2$

Under running conditions, the rotor slips and its electrical frequency drops to $f_r = s f$:
- Running EMF: $E_{2r} = s E_2$
- Running Reactance: $X_{2r} = s X_2$
- Resistance: $R_2$ (Constant, independent of frequency)
- Rotor Current: $I_2 = \frac{s E_2}{\sqrt{R_2^2 + (s X_2)^2}}$

## The Transformed Rotor Circuit
_(18:51 - 27:34)_

Analyzing a circuit where voltage and reactance vary with speed is difficult. We transform it by dividing both the numerator and denominator of the current equation by slip $s$:

$$I_2 = \frac{E_2}{\sqrt{(R_2/s)^2 + X_2^2}}$$

**Physical Meaning of the Transformation**:
We have replaced the variable-frequency rotor circuit with an equivalent constant-frequency ($f$) circuit. 
- The EMF is fixed at standstill value $E_2$.
- The reactance is fixed at standstill value $X_2$.
- The resistance becomes a slip-dependent variable resistor: **$R_2 / s$**.
This transformed circuit can now be directly coupled to the stator equivalent circuit.

## Power Flow and Air-Gap Power ($P_{\text{ag}}$)
_(27:34 - 39:37)_

**Air-Gap Power ($P_{\text{ag}}$)** is the real electromagnetic power crossing the air gap from the stator into the rotor. In the transformed circuit, all real power is absorbed by the variable resistor $R_2 / s$:
$$P_{\text{ag}} = I_2^2 \left(\frac{R_2}{s}\right)$$

We can split this total resistance into two physical components:
$$\frac{R_2}{s} = R_2 + R_2 \left(\frac{1-s}{s}\right)$$

Multiplying by $I_2^2$ reveals the fundamental power split:
1. **Rotor Copper Loss ($P_{cu}$)**: The heat dissipated in the actual physical resistance.
   $P_{cu} = I_2^2 R_2 = s P_{\text{ag}}$
2. **Gross Mechanical Power ($P_m$)**: The power converted into mechanical rotation.
   $P_m = I_2^2 R_2 \left(\frac{1-s}{s}\right) = (1-s) P_{\text{ag}}$

> [!success] The 1 : s : (1-s) Rule
> The division of rotor power is fixed by the slip:
> **$P_{\text{ag}} : P_{cu} : P_m = 1 : s : (1-s)$**

## Torque Formulations and Shaft Power
_(39:37 - 44:04)_

**Developed Torque ($T_d$)**:
Torque is mechanical power divided by mechanical angular speed ($\omega_r = \frac{2\pi N_r}{60}$).
$$T_d = \frac{P_m}{\omega_r}$$
Since $P_m = (1-s)P_{\text{ag}}$ and $\omega_r = (1-s)\omega_s$, the $(1-s)$ terms cancel:
$$T_d = \frac{P_{\text{ag}}}{\omega_s}$$
*Note: Always use total 3-phase power when calculating torque ($P_{\text{ag}} = 3 I_2^2 \frac{R_2}{s}$).*

**Shaft Power and Net Torque**:
Not all developed power reaches the load. Friction and windage losses ($P_{fw}$) consume some of it.
- **Shaft Power**: $P_{sh} = P_m - P_{fw}$
- **Shaft Torque (Load Torque)**: $T_{sh} = \frac{P_{sh}}{\omega_r}$
- **Loss Torque**: $T_{loss} = \frac{P_{fw}}{\omega_r}$

---

## Summary and Key Takeaways

- The air-gap flux is the space-phasor resultant $\vec{\Phi}_r = \vec{\Phi}_1 + \vec{\Phi}_2$, which induces EMF in both stator and rotor windings.
- Electromagnetic torque develops as the rotor flux tries to catch the stator flux, yielding $T_e \propto \Phi_r \Phi_2 \cos\theta_2$.
- Maximum torque per ampere requires minimizing the rotor impedance angle $\theta_2$, meaning rotor leakage reactance should be negligible compared to resistance.
- Under running conditions at slip $s$, rotor frequency is $f_r = s f$, induced EMF is $E_{2r} = s E_2$, and leakage reactance is $X_{2r} = s X_2$.
- Dividing rotor loop equations by slip $s$ yields a transformed circuit with constant standstill EMF $E_2$, reactance $X_2$, and effective variable resistance $R_2 / s$.
- Total real air-gap power transferred across the gap equals active power absorbed by the effective resistance: $P_{\text{ag}} = I_2^2 (R_2 / s)$.
- Air-gap power divides into rotor ohmic loss and gross electromechanical developed power according to $P_{\text{ag}} : P_{cu} : P_m = 1 : s : (1-s)$.
- Developed torque can be computed as $T_d = P_m / \omega_r = P_{\text{ag}} / \omega_s$, using total three-phase power.
- Shaft torque delivered to the mechanical load is $T_{sh} = (P_m - P_{fw}) / \omega_r$, where friction and windage losses reduce net torque by $T_{loss}$.

---

[← Lec 135: Rotating Magnetic Field](Lecture_135_Rotating_Magnetic_Field.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 137: Equivalent Circuit 2 →](Lecture_137_Equivalent_Circuit_2.md)
