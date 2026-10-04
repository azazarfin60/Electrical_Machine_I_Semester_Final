---
title: "Problems based on Parallel Operation of Transformer | L 16 | Electrical Machines | GATE 2022"
lecture: 48
topic: "Transformers"
duration: "01:04:18"
source: "https://www.youtube.com/watch?v=7f8Er86vHCM"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 047: Parallel Operation of Transformers](Lecture_047_Parallel_Operation_of_Transformers.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 049: Excitation Phenomenon 1 →](Lecture_049_Excitation_Phenomenon_1.md)

---

# Problems based on Parallel Operation of Transformer | L 16 | Electrical Machines | GATE 2022

- **Source**: https://www.youtube.com/watch?v=7f8Er86vHCM
- **Duration**: 01:04:18
- **Compiled**: 2026-09-21

---

## Overview

This problem-solving session works through representative examination problems on the parallel operation of transformers and alternators. It covers numerical methods for calculating complex power sharing, evaluating nodal equations with specified load impedances, and determining maximum permissible loading without exceeding ratings. The lecture also addresses conceptual questions on phasor groups, series-parallel configurations, and impedance modification for balanced load sharing.

## Contents

- [[#Problem 1: Load Sharing with Equal Turns Ratios|Problem 1: Load Sharing with Equal Turns Ratios]]
- [[#Problem 2: Base Conversion and Complex Power Sharing|Problem 2: Base Conversion and Complex Power Sharing]]
- [[#Problem 3: Nodal Analysis with Specified Load Impedance|Problem 3: Nodal Analysis with Specified Load Impedance]]
- [[#Problem 4: Maximum Permissible Loading|Problem 4: Maximum Permissible Loading]]
- [[#Problem 5: Series-Parallel Transformer Network|Problem 5: Series-Parallel Transformer Network]]
- [[#Problem 6: Parallel Alternators and Power Factor|Problem 6: Parallel Alternators and Power Factor]]
- [[#Problem 7: Delta-Star Switching Fault|Problem 7: Delta-Star Switching Fault]]
- [[#Problem 8: Series Reactance for Equal Load Sharing|Problem 8: Series Reactance for Equal Load Sharing]]

---

## Problem 1: Load Sharing with Equal Turns Ratios
_(04:55 - 10:52)_

> [!example] Problem 1
> Two single-phase transformers with equal turns ratios have secondary reactances $Z_A = j3.2\,\Omega$ and $Z_B = j19.2\,\Omega$. They operate in parallel to supply a 100 kW load at 0.8 power factor lagging. Determine the real power delivered by each transformer.

- **Load**: $S_L = \frac{100}{0.8} \angle \cos^{-1}(0.8) = 125\angle +36.87^\circ\text{ kVA}$.
- **Sharing Formula**: $S_A = S_L \left(\frac{Z_B}{Z_A + Z_B}\right)^*$.
- $S_A = 125\angle 36.87^\circ \left(\frac{j19.2}{j22.4}\right)^* = 125 \times \frac{6}{7} \angle 36.87^\circ = \frac{750}{7} \angle 36.87^\circ\text{ kVA}$.
- **Real Power A**: $P_A = |S_A| \cos(36.87^\circ) = \frac{750}{7} \times 0.8 = \frac{600}{7} \approx 85.71\text{ kW}$.
- **Real Power B**: $P_B = 100 - 85.71 = 14.29\text{ kW}$.

## Problem 2: Base Conversion and Complex Power Sharing
_(11:00 - 21:05)_

> [!example] Problem 2
> A 600 kVA transformer ($0.012 + j0.054\text{ pu}$) operates in parallel with a 300 kVA transformer ($0.014 + j0.048\text{ pu}$). They supply an 800 kVA load at 0.8 pf lagging. Calculate load shared by each.

- **Base Conversion**: Convert 300 kVA impedance to 600 kVA base.
  - $Z_B = (0.014 + j0.048) \times \left(\frac{600}{300}\right) = 0.028 + j0.096\text{ pu}$.
- **Total Impedance**: $Z_A + Z_B = 0.040 + j0.150\text{ pu}$.
- **Load Sharing**: $S_A = S_L \left(\frac{Z_B}{Z_A + Z_B}\right)^*$.
  - $\left(\frac{0.028 + j0.096}{0.040 + j0.150}\right)^* = 0.6443 \angle +1.33^\circ$.
  - $S_A = 800\angle 36.87^\circ \times 0.6443\angle 1.33^\circ = 485.71 \angle 39.20^\circ\text{ kVA}$.
  - $S_B = S_L - S_A = 800\angle 36.87^\circ - 485.71\angle 39.20^\circ = 315.32 \angle 33.24^\circ\text{ kVA}$.

## Problem 3: Nodal Analysis with Specified Load Impedance
_(26:33 - 31:47)_

> [!example] Problem 3
> Two transformers A and B supply a load $Z_L = 44 + j18.6\,\Omega$.
> - A: $E_A = 600\text{ V}$, $Z_A = 1.8 + j5.6\,\Omega$.
> - B: $E_B = 610\text{ V}$, $Z_B = 1.8 + j7.4\,\Omega$.
> Calculate terminal voltage and branch currents.

- **Nodal Equation**: $\frac{V - 600}{1.8 + j5.6} + \frac{V - 610}{1.8 + j7.4} + \frac{V}{44 + j18.6} = 0$.
- **Admittances**: $Y_A = 0.0520 - j0.1617$, $Y_B = 0.0310 - j0.1276$, $Y_L = 0.0193 - j0.0081$.
- **Total Admittance**: $Y_{\text{total}} = 0.3145 \angle -71.02^\circ$.
- **Injection Current**: $I_{\text{inj}} = 600 Y_A + 610 Y_B = 181.89 \angle -74.00^\circ\text{ A}$.
- **Terminal Voltage**: $V = I_{\text{inj}} / Y_{\text{total}} = 578.29 \angle -2.98^\circ\text{ V}$.
- **Branch Currents**:
  - $I_A = \frac{600\angle 0^\circ - V}{Z_A} = 6.39 \angle -19.00^\circ\text{ A}$.
  - $I_B = \frac{610\angle 0^\circ - V}{Z_B} = 5.81 \angle -23.56^\circ\text{ A}$.

## Problem 4: Maximum Permissible Loading
_(36:58 - 47:37)_

> [!example] Problem 4
> Transformer A (1000 kVA, $0.02 + j0.07\text{ pu}$) and Transformer B (500 kVA, $0.025 + j0.0875\text{ pu}$). Determine largest UPF load without overloading.

- **Overloading Principle**: The unit with the *lower* per-unit impedance on its own base overloads first.
  - $|Z_{A, pu}| = \sqrt{0.02^2 + 0.07^2} = 0.0728\text{ pu}$.
  - $|Z_{B, pu}| = \sqrt{0.025^2 + 0.0875^2} = 0.0910\text{ pu}$.
  - A overloads first. Set $S_A = 1000 \angle 0^\circ\text{ kVA}$.
- **Base Conversion**: Convert B to 1000 kVA base: $Z_B = (0.025 + j0.0875) \times \frac{1000}{500} = 0.05 + j0.175\text{ pu}$.
- **Power Sharing**: $S_B = S_A \left(\frac{Z_A}{Z_B}\right)^* = 1000 \left(\frac{0.02 + j0.07}{0.05 + j0.175}\right)^*$.
  - Notice $Z_B = 2.5 Z_A$. Thus, $\frac{Z_A}{Z_B} = \frac{1}{2.5} = 0.4$.
  - $S_B = 1000 \times 0.4 = 400 \angle 0^\circ\text{ kVA}$.
- **Max Load**: $S_{\text{max}} = 1000 + 400 = 1400\text{ kVA}$.

## Problem 5: Series-Parallel Transformer Network
_(41:57 - 47:37)_

> [!example] Problem 5
> Two identical 200/200 V transformers A and B have primaries in series across 200 V. Secondary $S_A$ is directly across the 200 V source. Find open-circuit voltage of $S_B$.

- Secondary $A$ is forced to 200 V. Thus, primary $A$ has 200 V across it.
- KVL on primary loop: $V_A + V_B = 200\text{ V} \implies 200 + V_B = 200 \implies V_B = 0\text{ V}$.
- Induced voltage on secondary $B$: $V_{SB} = 0\text{ V}$.

## Problem 6: Parallel Alternators and Power Factor
_(47:39 - 52:42)_

> [!example] Problem 6
> Two alternators supply: Load 1 (250 kW, 0.95 lag), Load 2 (100 kW, 0.8 lead). Alternator 1 supplies 200 kW, 0.9 lag. Find Alternator 2 power factor.

- **Active Power Balance**: $P_{\text{total}} = 250 + 100 = 350\text{ kW}$. $P_{G2} = 350 - 200 = 150\text{ kW}$.
- **Reactive Power Balance**:
  - $Q_{L1} = 250 \tan(\cos^{-1} 0.95) = +82.17\text{ kVAR}$.
  - $Q_{L2} = -100 \tan(\cos^{-1} 0.8) = -75.00\text{ kVAR}$.
  - $Q_{\text{total}} = 82.17 - 75.00 = +7.17\text{ kVAR}$.
  - $Q_{G1} = 200 \tan(\cos^{-1} 0.9) = +96.86\text{ kVAR}$.
  - $Q_{G2} = 7.17 - 96.86 = -89.69\text{ kVAR}$.
- **Alternator 2 PF**: $S_{G2} = \sqrt{150^2 + (-89.69)^2} = 174.77\text{ kVA}$. $\text{pf}_2 = 150 / 174.77 = 0.858\text{ leading}$.

## Problem 7: Delta-Star Switching Fault
_(52:43 - 59:19)_

> [!example] Problem 7
> An 11kV/415V $\Delta\text{-}Y$ transformer has its primary terminals B and C shorted. 11kV is applied across A and B. Find secondary line voltage $V_{AC}$.

- $V_{BC} = 0$. $V_{AB} = 11000\angle 0^\circ$. KVL inside delta: $V_{AB} + V_{BC} + V_{CA} = 0 \implies V_{CA} = -11000 = 11000\angle 180^\circ$.
- Secondary phase voltage magnitude $= \frac{415}{\sqrt{3}} \approx 240\text{ V}$.
- Phase voltages: $V_{an} = 240\angle 0^\circ$, $V_{cn} = 240\angle 180^\circ$.
- $V_{AC} = V_{an} - V_{cn} = 240 - (-240) = 480\text{ V}$.

## Problem 8: Series Reactance for Equal Load Sharing
_(59:21 - 01:04:09)_

> [!example] Problem 8
> Transformers A and B have equal no-load EMFs. $Z_A = 0.4 + j2.2\,\Omega$, $Z_B = 0.6 + j1.6\,\Omega$. Find series reactance $X$ with B for equal current sharing.

- Current is equally shared when impedance magnitudes are equal: $|Z_A| = |Z_B + jX|$.
- $0.4^2 + 2.2^2 = 0.6^2 + (1.6 + X)^2$.
- $5.00 = 0.36 + (1.6 + X)^2 \implies (1.6 + X)^2 = 4.64$.
- $1.6 + X = \sqrt{4.64} \approx 2.154 \implies X = 0.554\,\Omega$.

---

## Summary and Key Takeaways

- For parallel transformers with equal turns ratios, complex power is shared according to $S_A = S_L [Z_B / (Z_A + Z_B)]^*$, where impedances must be in ohms or per-unit on a common base.
- When load impedance is given in ohms rather than complex power, nodal analysis yields a linear equation for the terminal voltage $V = I_{\text{inj}} / Y_{\text{total}}$.
- The maximum load without overloading either transformer is found by identifying the unit with lower per-unit impedance on its own base and fixing it at rated capacity.
- In series-parallel transformer circuits, fixing the secondary voltage of one unit directly across the supply forces zero net voltage across the remaining series primary winding.
- In parallel alternator systems, individual operating power factors are determined through independent active and reactive power balance equations: $\sum P_G = \sum P_L$ and $\sum Q_G = \sum Q_L$.
- Three-phase transformers can operate in parallel only if they belong to the same phasor group with matching phase displacement.
- Load current is shared equally in magnitude between two parallel units with identical no-load EMFs when their total branch impedance magnitudes are equal: $|Z_A| = |Z_B + jX|$.

---

[← Lec 047: Parallel Operation of Transformers](Lecture_047_Parallel_Operation_of_Transformers.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 049: Excitation Phenomenon 1 →](Lecture_049_Excitation_Phenomenon_1.md)
