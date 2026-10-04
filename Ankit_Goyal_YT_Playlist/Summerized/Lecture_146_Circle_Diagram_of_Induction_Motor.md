---
title: "Circle Diagram of Induction Motor | Electrical Machines | Lec 104 | GATE/ESE (EE, ECE) | Ankit Goyal"
lecture: 146
topic: "Induction Machines"
duration: "01:03:26"
source: "https://www.youtube.com/watch?v=vMY-IizxLFM"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 145: Stability and Testing of Induction Machines](Lecture_145_Stability_and_Testing_of_Induction_Machines.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 147: Starting of SCIM →](Lecture_147_Starting_of_SCIM.md)

---

# Circle Diagram of Induction Motor | Electrical Machines | Lec 104 | GATE/ESE (EE, ECE) | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=vMY-IizxLFM
- **Duration**: 01:03:26
- **Compiled**: 2026-09-23

---

## Overview

This lecture explains the geometric derivation and construction of the circle diagram for three-phase induction machines. It demonstrates how no-load and blocked-rotor test measurements define the semicircular locus of stator current. The discussion breaks down total input power into output shaft power, copper losses, and constant rotational losses. It establishes the power line and torque line to graphically determine motor efficiency, operating slip, and pull-out torque.

## Contents

- [[#Semicircular Locus Derivation|Semicircular Locus Derivation]]
- [[#Origin Shift & No-Load Current|Origin Shift & No-Load Current]]
- [[#Power Line & Torque Line Construction|Power Line & Torque Line Construction]]
- [[#Operating Point Analysis (Power, Slip, Efficiency)|Operating Point Analysis (Power, Slip, Efficiency)]]
- [[#Maximum Output Computations|Maximum Output Computations]]

---

## Semicircular Locus Derivation
_(00:13 - 12:52)_

The rotor equation $I_2 = \frac{E_2}{R_2/s + jX_2}$ can be algebraically transformed into a vector equation demonstrating that $I_2$ forms a right angle with a voltage-dependent term.
Because the angle is constant at $90^\circ$ over a fixed hypotenuse, the locus of rotor current (and subsequently the load component of stator current $I'_1$) is a semicircle.

> [!success] Circle Diameter
> The diameter of the operating semicircle lies on the horizontal axis and has a magnitude of:
> $$\text{Diameter} = \frac{V_1}{X_1 + X'_2}$$

## Origin Shift & No-Load Current
_(12:57 - 28:05)_

The true stator current is $I_1 = I_0 + I'_1$.
- The no-load current $I_0$ (measured from the no-load test) defines a fixed point $Q$.
- The semicircle is drawn starting from $Q$, with its diameter extending horizontally to the right.
- The vertical projection of $I_0$ accounts for fixed core losses and friction/windage losses ($P_{\text{core}} + P_{\text{fw}}$). This creates a constant loss baseline extending horizontally below $Q$.

## Power Line & Torque Line Construction
_(28:05 - 45:37)_

**Power Line ($QB$)**:
- Point $B$ on the circle represents the standstill condition ($s=1$), found via the blocked-rotor test ($I_{\text{sc}}$ and $\phi_{\text{sc}}$).
- The chord connecting $Q$ (no-load) to $B$ (standstill) is the **Power Line**. 
- The total vertical drop from $B$ to the horizontal reference line represents total copper loss at standstill ($P_{\text{cu, sc}}$).

**Torque Line ($QE$)**:
- The standstill copper loss vertical line is divided at point $E$ in the ratio of rotor-to-stator resistance:
  $$\frac{BE}{ED} = \frac{R'_2}{R_1} = \frac{P_{\text{cu, rotor}}}{P_{\text{cu, stator}}}$$
- The chord connecting $Q$ to $E$ is the **Torque Line**.

## Operating Point Analysis (Power, Slip, Efficiency)
_(45:37 - 63:14)_

For any general operating load point $F$ on the circle, drop a vertical line down to the horizontal baseline. The segments represent:
- **$FH$**: Distance from circle to Power Line = Shaft output power ($P_{\text{out}}$).
- **$HK$**: Distance from Power Line to Torque Line = Rotor copper loss.
- **$KG$**: Distance from Torque Line to Reference Line = Stator copper loss.
- **$GM$**: Distance from Reference Line to Baseline = Fixed rotational & core losses.

By aggregating these segments:
- **$FK$**: Total vertical distance from circle to Torque Line = Air-gap power ($P_g \propto \text{Torque } T$).
- **$FM$**: Total vertical distance from circle to Baseline = Total electrical input power ($P_{\text{in}}$).

**Calculations directly from the graph**:
- **Slip**: $s = \frac{\text{Rotor Cu Loss}}{\text{Air-Gap Power}} = \frac{HK}{FK}$
- **Efficiency**: $\eta = \frac{\text{Output Power}}{\text{Input Power}} = \frac{FH}{FM}$

## Maximum Output Computations
_(56:42 - 63:14)_

- **Maximum Output Power**: Draw a perpendicular from the center of the semicircle to the **Power Line ($QB$)**, extend it to the circle boundary. The vertical drop from that boundary point to the Power Line gives $P_{\text{max}}$.
- **Maximum Torque (Breakdown Torque)**: Draw a perpendicular from the center to the **Torque Line ($QE$)**, extend it to the circle boundary. The vertical drop from that boundary point to the Torque Line gives $T_{\text{max}}$.

---

## Summary and Key Takeaways

- The rotor current locus forms a semicircle with diameter equal to $\frac{V_1}{X_{01}}$ lying on a horizontal reference line shifted by no-load current $I_0$.
- In the circle diagram, vertical distances from any operating point represent real power while horizontal distances represent reactive power.
- Semicircle construction requires only no-load and blocked-rotor test data to fix the origin, the chord $QB$, and the diameter endpoint.
- Line $QB$ represents the power line because the vertical segment from the circle down to $QB$ equals mechanical shaft output power $P_{\text{out}}$.
- Line $QE$ represents the torque line because the vertical segment from the circle down to $QE$ equals air-gap power $P_g$.
- Operating slip is measured directly as the ratio of rotor copper loss to air-gap power: $s = \frac{HK}{FK}$.
- Operating motor efficiency is given by the ratio of shaft output vertical segment to total input vertical segment: $\eta = \frac{FH}{FM}$.
- Maximum output power and maximum electromagnetic torque occur at the intersection points of perpendiculars drawn from the semicircle center to the power line and torque line.

---

[← Lec 145: Stability and Testing of Induction Machines](Lecture_145_Stability_and_Testing_of_Induction_Machines.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 147: Starting of SCIM →](Lecture_147_Starting_of_SCIM.md)
