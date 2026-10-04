---
title: "Electrical Machines | Lec 103 | Stability & Testing of Induction Motor | GATE Electrical Engineering"
lecture: 144
topic: "Induction Machines"
duration: "00:55:29"
source: "https://www.youtube.com/watch?ePsBUg-DBSs"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 143: Torque Slip Characteristics 2](Lecture_143_Torque_Slip_Characteristics_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 145: Stability and Testing of Induction Machines →](Lecture_145_Stability_and_Testing_of_Induction_Machines.md)

---

# Electrical Machines | Lec 103 | Stability & Testing of Induction Motor | GATE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=ePsBUg-DBSs
- **Duration**: 00:55:29
- **Compiled**: 2026-09-23

---

## Overview

This lecture establishes the operating point stability criteria and experimental testing procedures for three-phase induction motors. It begins by examining the mechanical dynamic equation of motion to derive physical and derivative stability conditions on torque-speed axes. The presentation then maps transformer open-circuit and short-circuit tests to induction motor no-load and blocked-rotor tests. It demonstrates how to determine equivalent circuit branch parameters, separate core loss from mechanical friction and windage, analyze non-rated operating conditions, and predict Direct-On-Line starting currents from test data.

## Contents

- [[#Operating Point Stability Criteria|Operating Point Stability Criteria]]
- [[#No-Load Test Principle & Measurements|No-Load Test Principle & Measurements]]
- [[#Separation of No-Load Losses|Separation of No-Load Losses]]
- [[#Blocked Rotor Test Principle & Equivalent Circuit|Blocked Rotor Test Principle & Equivalent Circuit]]
- [[#Direct-On-Line (DOL) Starting Relations|Direct-On-Line (DOL) Starting Relations]]

---

## Operating Point Stability Criteria
_(00:13 - 20:38)_

**Mechanical Dynamic Equation**:
$$J \frac{d\omega}{dt} = T_m - T_L$$
Steady-state equilibrium occurs when motor torque matches load torque ($T_m = T_L$). 
An operating point is stable if a perturbation creates a restoring net torque that returns the system to equilibrium.

**Derivative Stability Criterion**:
When torque is plotted on the vertical ($Y$) axis and speed on the horizontal ($X$) axis:
> [!success] Stability Condition
> $$\frac{dT_L}{d\omega} > \frac{dT_m}{d\omega} \implies \text{Stable}$$
If this slope condition is met, any speed increase ($\Delta \omega > 0$) causes load torque to exceed motor torque ($T_L > T_m$), producing deceleration that drives the speed back down.

*(Note: When speed is on the Y-axis and torque on the X-axis, the visual slope rule flips. The safest method is to mentally perturb speed upward and verify whether $T_L > T_m$ horizontally to pull it back).*

## No-Load Test Principle & Measurements
_(20:38 - 31:49)_

The no-load test is the induction motor equivalent of a transformer open-circuit test. 
- The motor runs uncoupled at rated voltage and frequency. 
- Because $N \approx N_s$, slip $s \approx 0$. 
- The fictitious mechanical load resistance $R'_2(1/s - 1) \to \infty$. The rotor branch draws negligible current.

**Calculations from No-Load Test**:
1. Measure line voltage $V_{nl}$, line current $I_{nl}$, and total active power $P_{nl}$.
2. Convert to per-phase values: $Z_{nl} = V_{ph} / I_{ph}$.
3. Measure stator DC resistance $R_{dc}$, apply skin effect factor: $R_1 \approx (1.2 \text{ to } 1.3) R_{dc}$.
4. The no-load reactance is the sum of stator leakage and magnetizing reactances:
   $$X_{nl} = \sqrt{Z_{nl}^2 - R_1^2} = X_1 + X_m$$

## Separation of No-Load Losses
_(31:52 - 36:54)_

The no-load active power input $P_{nl}$ contains stator copper loss, core loss, and friction/windage loss:
$$P_{\text{rot}} = P_{nl} - 3 I_{nl}^2 R_1 = P_{\text{core}} + P_{f+w}$$

To separate $P_{\text{core}}$ from $P_{f+w}$:
- Run the no-load test at varying voltages down to the stalling point (at rated frequency).
- Since $P_{\text{core}} \propto V^2$ and $P_{f+w}$ is constant (since speed $\approx N_s$ is constant), plot $P_{\text{rot}}$ versus $V$ (or $V^2$).
- The y-intercept (at $V=0$) gives the purely mechanical friction and windage loss $P_{f+w}$.

**Parametric Effects on No-Load**:
- **Under-Voltage ($V \downarrow, f$ rated)**: Flux decreases, magnetizing current drops, power factor improves, speed and $P_{f+w}$ stay roughly constant.
- **Under-Frequency ($V$ rated, $f \downarrow$)**: Flux ($V/f$) increases heavily, driving the core into deep saturation. Magnetizing current spikes, power factor collapses, and speed drops (lowering $P_{f+w}$).

## Blocked Rotor Test Principle & Equivalent Circuit
_(42:18 - 55:21)_

The blocked rotor test is the induction motor equivalent of a transformer short-circuit test.
- The rotor is mechanically locked ($N = 0, s = 1$).
- The fictitious mechanical load resistance $R'_2(1/s - 1)$ becomes zero (short circuit).
- Reduced voltage $V_{br}$ is applied to circulate rated current.
- Because $V_{br} \ll V_{\text{rated}}$, core flux is tiny. Magnetizing branch and core losses are neglected.

**Calculations from Blocked Rotor Test**:
1. Total equivalent resistance: $R_{01} = \frac{P_{br}}{3 I_{br,ph}^2}$.
2. Rotor resistance: $R'_2 = R_{01} - R_1$.
3. Total leakage reactance: $X_{01} = \sqrt{Z_{br}^2 - R_{01}^2}$.
4. Assuming equal distribution: $X_1 = X'_2 = X_{01}/2$.
5. Magnetizing reactance (from no-load): $X_m = X_{nl} - X_1$.

## Direct-On-Line (DOL) Starting Relations
_(48:21 - 55:21)_

When a motor starts Direct-On-Line at full voltage, it is physically in the blocked-rotor state ($s=1$), but at rated voltage. The starting short-circuit current scales directly from the blocked-rotor test measurements via the voltage ratio:

> [!success] DOL Starting Current
> $$I_{sc} = I_{br} \times \left(\frac{V_{\text{rated}}}{V_{br}}\right)$$

---

## Summary and Key Takeaways

- The mechanical dynamic equation of motion is $J \frac{d\omega}{dt} = T_m - T_L$, where equilibrium steady-state operation occurs at $T_m = T_L$.
- On a torque (vertical) versus speed (horizontal) plot, an operating point is stable if $\frac{dT_L}{d\omega} > \frac{dT_m}{d\omega}$, ensuring that any speed disturbance produces a restoring torque.
- When speed is plotted on the vertical axis, stability is determined by introducing a vertical test shift and verifying that net torque opposes the perturbation.
- The no-load test runs uncoupled at $s \approx 0$, which open-circuits the mechanical load resistance $R'_2\left(\frac{1}{s}-1\right)$ and yields the no-load reactance $X_{nl} = X_1 + X_m$.
- Stator winding resistance $R_1$ is determined using a DC voltmeter-ammeter measurement and multiplied by an AC skin-effect factor of $1.2$ to $1.3$.
- Friction and windage loss $P_{f+w}$ is separated from stator core loss by extrapolating the rotational loss curve against applied voltage down to $V = 0$.
- In the blocked rotor test, the rotor is clamped at standstill ($s = 1$), which reduces the circuit to series resistance $R_{01}$ and leakage reactance $X_{01} = 2 X_1 = 2 X'_2$.
- The magnetizing reactance is obtained by combining results from both tests: $X_m = X_{nl} - X_1$.
- Direct-On-Line full-voltage starting current is directly proportional to blocked-rotor test current through the voltage ratio $I_{sc} = I_{br} \left(\frac{V_{\text{rated}}}{V_{br}}\right)$.

---

[← Lec 143: Torque Slip Characteristics 2](Lecture_143_Torque_Slip_Characteristics_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 145: Stability and Testing of Induction Machines →](Lecture_145_Stability_and_Testing_of_Induction_Machines.md)
