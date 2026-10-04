---
title: "Electrical Machines | Lec 99 | Equivalent Circuit - 2 | GATE Electrical Engineering"
lecture: 137
topic: "Induction Machines"
duration: "00:40:59"
source: "https://www.youtube.com/watch?v=K2QQi9ab4RE"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 136: Equivalent Circuit 1](Lecture_136_Equivalent_Circuit_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 138: Losses and Efficiency of Induction Machines →](Lecture_138_Losses_and_Efficiency_of_Induction_Machines.md)

---

# Electrical Machines | Lec 99 | Equivalent Circuit - 2 | GATE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=K2QQi9ab4RE
- **Duration**: 00:40:59
- **Compiled**: 2026-09-23

---

## Overview

This lecture completes the equivalent circuit modeling and power analysis of three-phase induction motors. It develops the stator equivalent circuit using effective turns and analyzes the high magnetizing current caused by the air gap. The lecture resolves the difference between the two rotor equivalent circuits through observer frames of reference. Finally, it constructs the complete stator-referred equivalent circuit, details the power flow cascade, and categorizes motor losses and efficiency.

## Contents

- [[#Effective Turns and Stator Circuit|Effective Turns and Stator Circuit]]
- [[#The Magnetizing Branch ($X_m$ and $R_c$)|The Magnetizing Branch ($X_m$ and $R_c$)]]
- [[#Frame of Reference in Circuit Transformation|Frame of Reference in Circuit Transformation]]
- [[#Complete Equivalent Circuit & Resistance Splitting|Complete Equivalent Circuit & Resistance Splitting]]
- [[#Comprehensive Power Flow|Comprehensive Power Flow]]
- [[#Classification of Losses and Efficiency|Classification of Losses and Efficiency]]

---

## Effective Turns and Stator Circuit
_(00:13 - 06:30)_

The induction machine acts like a transformer, but its windings are distributed rather than concentrated.
- **Transformation Ratio ($a$)**: Must use *effective* turns, accounting for winding factors ($K_w = K_p K_d$).
  $a = \frac{E_1}{E_2} = \frac{N_1 K_{w1}}{N_2 K_{w2}} = \frac{N_{e1}}{N_{e2}}$
- **MMF Balance**: MMF balance between stator and rotor must also use effective turns:
  $N_{e1} I_1 = N_{e2} I_2 + \text{MMF}_0$

## The Magnetizing Branch ($X_m$ and $R_c$)
_(06:30 - 11:11)_

The stator equivalent circuit includes $R_1$, $X_1$, and a parallel shunt branch:
- **Core-loss component ($I_w$)**: Flows through $R_c$, supplying stator iron losses.
- **Magnetizing component ($I_\mu$)**: Flows through $X_m$, establishing the air-gap flux.

**The Air-Gap Effect**: 
Unlike a static transformer, flux must cross a physical air gap. Because air has high reluctance, an induction motor draws a very large magnetizing current ($25\%$ to $40\%$ of rated current). Therefore, $I_\mu \gg I_w$, which implies $X_m \ll R_c$. In many calculations, the large $R_c$ is ignored, leaving only $X_m$.

## Frame of Reference in Circuit Transformation
_(11:11 - 28:42)_

In the previous lecture, dividing the rotor circuit by $s$ transformed the frequency from $sf$ to $f$. While the current and phase angle remained identical, the real power changed from $I_2^2 R_2$ to $I_2^2 (R_2/s)$. Why?

It depends on the observer's frame of reference:
1. **Rotor Frame ($f_r = sf$)**: To an observer on the rotor, the rotor is stationary. There is no mechanical motion observed. Thus, the only real power seen is the ohmic heating ($P_{cu} = I_2^2 R_2$).
2. **Stator Frame ($f_r = f$)**: To an observer on the stator, the rotor is spinning at $N_r$. The observer sees both ohmic heating AND mechanical power generation. Thus, the total power seen is the full air-gap power ($P_{\text{ag}} = I_2^2 (R_2/s) = P_{cu} + P_m$).

**Note on Rotor Core Loss**: Under normal running conditions, rotor slip frequency ($sf$) is very small (1-2 Hz). Thus, rotor hysteresis and eddy current losses are negligible and omitted from the equivalent circuit.

## Complete Equivalent Circuit & Resistance Splitting
_(28:42 - 34:19)_

By referring the transformed rotor circuit to the stator using $a = N_{e1}/N_{e2}$:
- $R_2' = a^2 R_2$
- $X_2' = a^2 X_2$
- $I_2' = I_2 / a$

We split the total rotor resistance $R_2'/s$ into two physical parts to model the power components separately:
$\frac{R_2'}{s} = R_2' + R_2'\left(\frac{1-s}{s}\right)$
1. **$R_2'$**: The physical winding resistance, which models actual copper loss ($P_{cu}$).
2. **$R_2'\left(\frac{1-s}{s}\right)$**: A fictitious load resistance, which models the gross electromechanical power developed ($P_m$).

## Comprehensive Power Flow
_(28:42 - 34:19)_

Power cascades through the machine as follows:
1. **Input Power**: $P_{\text{in}} = \sqrt{3} V_L I_L \cos\theta$
2. **Stator Losses**: Subtract Stator Copper ($3 I_1^2 R_1$) and Stator Core losses.
3. **Air-Gap Power**: $P_{\text{ag}} = P_{\text{in}} - P_{cu1} - P_{core1} = 3(I_2')^2 \left(\frac{R_2'}{s}\right)$
4. **Rotor Copper Loss**: $P_{cu2} = s P_{\text{ag}}$
5. **Gross Mechanical Power**: $P_m = P_{\text{ag}} - P_{cu2} = (1-s)P_{\text{ag}}$
6. **Shaft Output Power**: $P_{\text{shaft}} = P_m - P_{fw}$ (Friction & Windage)

> [!important] Rule: Do Not Merge Rotational Losses
> In DC machines, core loss and friction loss are lumped as "rotational loss". In induction machines, stator core loss happens on the stationary stator before the air gap, while friction/windage happens on the spinning rotor after mechanical conversion. They must NEVER be combined.

## Classification of Losses and Efficiency
_(34:19 - 40:52)_

- **Fixed Losses**: Stator core loss, bearing friction, brush friction (SRIM only), windage loss.
- **Variable Losses**: Stator copper loss, rotor copper loss.
- **Maximum Efficiency Condition**: Occurs when Variable Losses = Fixed Losses.

**Windage Comparison**: A Slip Ring Induction Motor (SRIM) has a bulkier wound rotor and larger air gap than a Squirrel Cage Motor, leading to greater aerodynamic shear. Thus, SRIMs suffer from higher windage losses.

---

## Summary and Key Takeaways

- Induced EMF in stator and rotor windings depends on effective turns, yielding the transformation ratio $a = E_1 / E_2 = N_{e1} / N_{e2} = (N_1 K_{w1}) / (N_2 K_{w2})$.
- MMF balancing between stator and rotor requires effective turns rather than raw turn counts: $N_{e1} I_1 = N_{e2} I_2 + \text{MMF}_0$.
- The presence of an air gap drastically increases magnetizing current to $25\% \text{–} 40\%$ of rated current, making $X_m \ll R_c$ so $R_c$ is often omitted in shunt calculations.
- Transforming the rotor loop from frequency $s f$ to line frequency $f$ shifts the observer frame of reference from the spinning rotor to the stationary stator.
- In the rotor reference frame, relative speed is zero so only rotor copper loss $I_2^2 R_2$ appears, while in the stator frame, rotor rotation is observed so total air-gap power $I_2^2 (R_2/s)$ appears.
- Rotor core losses are neglected during normal running conditions because rotor slip frequency $s f$ is very small ($0.5\text{–}2\text{ Hz}$).
- Splitting rotor resistance as $R_2'/s = R_2' + R_2'(1-s)/s$ isolates physical ohmic loss from the fictitious electromechanical load resistance $R_L'$.
- Core loss on the stationary stator and friction loss on the spinning rotor occur at different physical locations and must never be merged into a single rotational loss.
- Maximum efficiency occurs when variable losses equal fixed losses: $P_{\text{variable}} = P_{\text{fixed}}$, with brush contact drop excluded from the condition.

---

[← Lec 136: Equivalent Circuit 1](Lecture_136_Equivalent_Circuit_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 138: Losses and Efficiency of Induction Machines →](Lecture_138_Losses_and_Efficiency_of_Induction_Machines.md)
