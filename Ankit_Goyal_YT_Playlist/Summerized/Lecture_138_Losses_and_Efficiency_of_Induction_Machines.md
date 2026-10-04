---
title: "Losses and Efficiency of Induction Machines | L 38 | Electrical Machines | GATE 2022 | Ankit Sir"
lecture: 138
topic: "Induction Machines"
duration: "01:16:06"
source: "https://www.youtube.com/watch?v=pa30V1ocJvk"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 137: Equivalent Circuit 2](Lecture_137_Equivalent_Circuit_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 139: Torque Slip Characteristics 1 →](Lecture_139_Torque_Slip_Characteristics_1.md)

---

# Losses and Efficiency of Induction Machines | L 38 | Electrical Machines | GATE 2022 | Ankit Sir

- **Source**: https://www.youtube.com/watch?v=pa30V1ocJvk
- **Duration**: 01:16:06
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines quantitative problem-solving methods for losses, power flow, and efficiency in three-phase induction machines. The discussion develops the complete power flow model from stator input through the air gap to the mechanical shaft. It presents worked numerical problems covering rotor EMF cycle rates, slip-ring contact gear losses, network analysis using both approximate and exact T-equivalent circuits, and constant-torque response under voltage and frequency disturbances. Through systematic derivations, the lecture establishes how operating slip governs torque generation, internal electrical losses, and overall machine efficiency.

## Contents

- [[#Rotor Frequency from Cycle Rates|Rotor Frequency from Cycle Rates]]
- [[#The Core Power Equations|The Core Power Equations]]
- [[#Wound Rotor External Losses|Wound Rotor External Losses]]
- [[#Disturbance Analysis (Voltage and Frequency Drops)|Disturbance Analysis (Voltage and Frequency Drops)]]
- [[#Equivalent Circuit Numerical Methods|Equivalent Circuit Numerical Methods]]

---

## Rotor Frequency from Cycle Rates
_(00:02 - 05:36)_

Exam problems often provide the rotor EMF oscillation rate instead of direct rotor frequency.
- If the rotor EMF completes $n$ cycles per minute, the rotor frequency is: $f_r = \frac{n}{60} \text{ Hz}$.
- The operating slip is then found by: $s = \frac{f_r}{f}$.

> [!example] Problem
> A 6-pole, 50 Hz motor's rotor EMF makes 90 cycles per minute. Find slip.
> **Solution**: $f_r = 90 / 60 = 1.5 \text{ Hz}$. Slip $s = 1.5 / 50 = 0.03$.

## The Core Power Equations
_(05:40 - 10:01, 31:49 - 41:39)_

To solve induction machine problems quickly, master the power cascade and torque relationships:
1. **Air Gap Power**: $P_G = T_{\text{dev}} \omega_s = \frac{P_{\text{rcu}}}{s} = \frac{P_{\text{dev}}}{1-s}$
2. **Gross Developed Power**: $P_{\text{dev}} = T_{\text{dev}} \omega_r = P_G(1-s)$
3. **Net Shaft Power**: $P_{\text{sh}} = T_{\text{sh}} \omega_r = P_{\text{dev}} - P_{\text{mech (friction/windage)}}$
4. **Efficiency**: $\eta = \frac{P_{\text{sh}}}{P_{\text{in}}} = \frac{P_{\text{sh}}}{P_G + P_{\text{stator losses}}}$

> [!important] Rule
> Never mix up $T_{\text{dev}}$ and $T_{\text{sh}}$. $T_{\text{dev}}$ uses $\omega_s$ (with $P_G$) or $\omega_r$ (with $P_{\text{dev}}$). $T_{\text{sh}}$ is the useful output load torque and must use $\omega_r$ with $P_{\text{sh}}$.

## Wound Rotor External Losses
_(26:26 - 31:48)_

In slip-ring induction motors, total rotor copper loss ($sP_G$) includes both internal winding heating and external contact losses.
- $P_{\text{rcu, total}} = P_{\text{gear (external)}} + P_{\text{winding (internal)}}$
- To find the true internal rotor resistance $R_2$, use only the internal loss: $P_{\text{winding}} = 3 (I_r)^2 R_2$.

## Disturbance Analysis (Voltage and Frequency Drops)
_(41:39 - 52:03)_

For a motor driving a constant-torque load, electromagnetic torque $T_{\text{dev}}$ remains constant. 
In the low-slip linear region, $T_{\text{dev}} \propto \frac{s V^2}{f}$.
- **Equilibrium Condition**: $\frac{s_1 V_1^2}{f_1} = \frac{s_2 V_2^2}{f_2} \implies s_2 = s_1 \left(\frac{f_2}{f_1}\right) \left(\frac{V_1}{V_2}\right)^2$

> [!warning] Critical Trap
> When calculating the new mechanical speed $N_{r2} = N_{s2}(1 - s_2)$, you MUST use the updated synchronous speed $N_{s2} = \frac{120 f_2}{P}$ based on the new disturbed frequency $f_2$. Do not use the old $N_{s1}$.

## Equivalent Circuit Numerical Methods
_(17:04 - 26:25, 57:10 - 76:01)_

When calculating motor performance from circuit parameters:
1. **Approximate Circuit**: Moves the magnetizing branch to the input terminals.
   - Total series impedance: $Z_t = (R_1 + R_2'/s) + j(X_1 + X_2')$.
   - Rotor current: $I_2' = V_{\text{ph}} / |Z_t|$.
   - Valid for quick calculations but underestimates voltage drop across stator leakage.
2. **Exact T-Equivalent Circuit**: Keeps the magnetizing branch between stator and rotor branches.
   - Calculate total parallel impedance: $Z_p = jX_m \parallel (R_2'/s + jX_2')$.
   - Add stator impedance: $Z_{\text{eq}} = Z_1 + Z_p$.
   - Find stator current: $I_1 = V_{\text{ph}} / Z_{\text{eq}}$.
   - Use current division to find $I_2' = I_1 \times \frac{jX_m}{(R_2'/s + jX_2') + jX_m}$.

Once $I_2'$ is found by either method, standard power flow applies: $P_G = 3 (I_2')^2 (R_2'/s)$.

---

## Summary and Key Takeaways

- The rotor EMF oscillation rate $n$ in cycles per minute gives the rotor frequency as $f_r = n / 60\text{ Hz}$, which establishes operating slip via $s = f_r / f$.
- Air gap power $P_G$ links electromagnetic developed torque $T_{\text{dev}}$ and synchronous speed through $P_G = T_{\text{dev}} \omega_s$, while gross developed mechanical power satisfies $P_{\text{dev}} = T_{\text{dev}} \omega_r = (1 - s) P_G$.
- Rotor copper loss is strictly proportional to slip according to $P_{\text{rcu}} = s P_G = [s / (1 - s)] P_{\text{dev}}$.
- In slip-ring induction motors, total rotor electrical loss separates into internal winding copper loss $3 I_r^2 R_2$ and external contact loss in the short-circuiting gear.
- In the normal low-slip operating region, electromagnetic torque satisfies $T_{\text{dev}} \propto s V^2 / f$, requiring operating slip to scale as $s_2 = s_1 (f_2 / f_1) (V_1 / V_2)^2$ under constant developed torque.
- Disturbance calculations for rotor speed must use the updated synchronous speed $N_{s2} = 120 f_2 / P$ in the relation $N_{r2} = N_{s2}(1 - s_2)$.
- Stator core loss in induction machines occurs almost entirely in the stator laminations because slip frequency in the rotor core is very low during normal operation.
- In the exact T-equivalent circuit, total input impedance $Z_{\text{eq}} = Z_1 + (j X_m \parallel Z_2')$ determines stator current, after which current division yields the rotor branch current $I_2'$ for air gap power evaluation.

---

[← Lec 137: Equivalent Circuit 2](Lecture_137_Equivalent_Circuit_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 139: Torque Slip Characteristics 1 →](Lecture_139_Torque_Slip_Characteristics_1.md)
