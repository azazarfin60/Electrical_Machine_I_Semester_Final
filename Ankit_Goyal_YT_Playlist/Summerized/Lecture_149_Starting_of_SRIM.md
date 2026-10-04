---
title: "Electrical Machines | Lec 106 | Starting of SRIM | GATE/ESE Electrical Engineering"
lecture: 149
topic: "Induction Machines"
duration: "00:29:30"
source: "https://www.youtube.com/watch?v=vro0fzqEfzk"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 148: Starting of SCIM](Lecture_148_Starting_of_SCIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 150: Starting of SRIM →](Lecture_150_Starting_of_SRIM.md)

---

# Electrical Machines | Lec 106 | Starting of SRIM | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=vro0fzqEfzk
- **Duration**: 00:29:30
- **Compiled**: 2026-09-23

---

## Overview

This lecture establishes the theory, mathematical derivation, and practical design of rotor resistance starters for slip-ring induction motors. It explains how inserting external resistance through slip rings restricts starting inrush currents while developing high starting torque. The discussion shows how progressive resistance switching bounds the rotor current between specified maximum and minimum limits. It proves that the switching slips and resistance sections form geometric progressions and provides a structured five-step design algorithm.

## Contents

- [[#Rotor Resistance Starting Principle|Rotor Resistance Starting Principle]]
- [[#Bounded Current Oscillation & Switching Slips|Bounded Current Oscillation & Switching Slips]]
- [[#Geometric Progression & Design Algorithm|Geometric Progression & Design Algorithm]]
- [[#Numerical Example|Numerical Example]]

---

## Rotor Resistance Starting Principle
_(00:12 - 09:49)_

Slip-ring induction motors (SRIM) allow physical access to the rotor windings. Adding external resistance:
1. Reduces excessive starting current by increasing total impedance.
2. Increases starting torque, allowing the motor to start against heavy loads.

**Stepped Resistance Switching**:
As the motor accelerates, slip $s$ decreases, naturally increasing the effective internal rotor resistance $r_2/s$. To keep the current and torque within design bounds, external resistance is progressively cut out in discrete steps. 

For an $n$-section starter, there are $n+1$ contact studs.
- **Stud 1 (Standstill)**: All external sections $R_1, \dots, R_n$ are in series with $r_2$. Total resistance is $R_1'$.
- **Stud $n+1$ (Running)**: All external sections are bypassed. Total resistance is just $r_2$.

## Bounded Current Oscillation & Switching Slips
_(09:49 - 15:35)_

The rotor current traces a periodic sawtooth profile, oscillating between an upper limit $I_{\max}$ and a lower limit $I_{\min}$.
- The motor accelerates, slip falls from $s_1$ to $s_2$, and current drops to $I_{\min}$.
- At $I_{\min}$, the contact arm moves to the next stud, instantly cutting out a resistance section.
- Rotor speed cannot change instantly (inertia), so slip remains $s_2$. The sudden drop in resistance causes current to shoot back up to $I_{\max}$.

Because all peak currents $I_{\max}$ are identical and all trough currents $I_{\min}$ are identical, the ratios of consecutive slips are constant.
$$\frac{s_2}{s_1} = \frac{s_3}{s_2} = \dots = \frac{s_m}{s_n} = \alpha$$

> [!success] Switching Slips
> The switching slips form a Geometric Progression (GP) with a common ratio $\alpha < 1$.
> Since $s_1 = 1$ at standstill, the minimum operating slip on the final stud is $s_m = \alpha^n$.
> Thus, the stepping ratio is $\alpha = s_m^{1/n}$.

## Geometric Progression & Design Algorithm
_(15:35 - 23:23)_

The total remaining circuit resistances at each stud also form a GP:
$$R_k' = \alpha^{k-1} R_1'$$
Where $R_1' = r_2/s_m$.

The individual resistance sections $R_k$ cut out at each step (where $R_k = R_k' - R_{k+1}'$) also form a GP:
$$R_k = \alpha^{k-1} R_1$$

**Five-Step Starter Design Algorithm**:
1. Find the common ratio: $\alpha = s_m^{1/n}$
2. Calculate total initial circuit resistance: $R_1' = r_2 / s_m$
3. Compute the first external resistance section: $R_1 = R_1'(1 - \alpha)$
4. Compute subsequent sections: $R_2 = \alpha R_1, \dots, R_n = \alpha^{n-1} R_1$
5. Total external resistance per phase: $R_{\text{ext}} = R_1' - r_2$

## Numerical Example
_(23:23 - 29:22)_

**Problem**: SRIM with $r_2 = 0.03\ \Omega/\text{phase}$, $6$-stud starter ($n=5$). $s_{\text{fl}} = 0.02$. Current oscillates between $I_{\text{fl}}$ and $2 I_{\text{fl}}$. Find resistance sections.

**Solution**:
Neglecting leakage reactance, $I \approx s V_1 / r_2$. 
On the final stud, $I_{\max} = s_m V_1 / r_2$.
$\frac{I_{\max}}{I_{\text{fl}}} = \frac{s_m}{s_{\text{fl}}} = 2 \implies s_m = 2(0.02) = 0.04$.

1. $\alpha = s_m^{1/5} = (0.04)^{0.2} \approx 0.5253$
2. $R_1' = 0.03 / 0.04 = 0.75\ \Omega$
3. $R_1 = 0.75(1 - 0.5253) \approx 0.356\ \Omega$
4. $R_2 = \alpha R_1 \approx 0.187\ \Omega$
   $R_3 = \alpha R_2 \approx 0.098\ \Omega$
   $R_4 = \alpha R_3 \approx 0.052\ \Omega$
   $R_5 = \alpha R_4 \approx 0.027\ \Omega$

---

## Summary and Key Takeaways

- External rotor resistance can be inserted into slip-ring induction motors via slip rings to increase starting torque and limit starting current.
- As the rotor accelerates, slip drops and effective internal impedance $R_2/s$ naturally rises, enabling progressive removal of external resistance steps.
- Rotor current is maintained within designed operational bounds oscillating between $I_{\max}$ and $I_{\min}$.
- Consecutive switching slips form a geometric progression with common ratio $\alpha = s_m^{1/n}$, where $s_m$ is the minimum operating slip and $n$ is the number of resistance sections.
- An $n$-section rotor resistance starter requires exactly $n+1$ contact studs per rotor phase.
- Total remaining circuit resistances on consecutive studs follow the geometric progression $R_k' = \alpha^{k-1} R_1'$, with $R_1' = \frac{r_2}{s_m}$.
- Individual resistance sections connected between adjacent studs satisfy $R_k = \alpha^{k-1} R_1$, where the first section is $R_1 = R_1'(1 - \alpha)$.
- When designing starter sections, the minimum operating slip $s_m$ must be calculated from operating current bounds and should not be assumed equal to full-load slip.

---

[← Lec 148: Starting of SCIM](Lecture_148_Starting_of_SCIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 150: Starting of SRIM →](Lecture_150_Starting_of_SRIM.md)
