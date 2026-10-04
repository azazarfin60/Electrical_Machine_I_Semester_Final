---
title: "Problems based on Harmonics and Inrush Current | L 17 | Electrical Machines | GATE 2022"
lecture: 53
topic: "Transformers"
duration: "00:33:36"
source: "https://www.youtube.com/watch?v=hwvRhuCKuEE"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 052: Switching Transients](Lecture_052_Switching_Transients.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 131: Induction Machines Introduction →](Lecture_131_Induction_Machines_Introduction.md)

---

# Problems based on Harmonics and Inrush Current | L 17 | Electrical Machines | GATE 2022

- **Source**: https://www.youtube.com/watch?v=hwvRhuCKuEE
- **Duration**: 00:33:36
- **Compiled**: 2026-09-21

---

## Overview

This lecture solves key problems on harmonic distortion and switching inrush transients in power transformers. It examines how non-linear magnetic saturation distorts exciting currents and shapes core flux waveforms. The session investigates magnetic flux return paths in three-limb cores and circulating currents in delta windings. It also determines the exact switching instant needed to avoid transient inrush currents and analyzes multi-winding transients.

## Contents

- [[#RMS Calculation of Exciting Current with Harmonics|RMS Calculation of Exciting Current with Harmonics]]
- [[#Triplen Flux Paths and Core Geometry|Triplen Flux Paths and Core Geometry]]
- [[#Star-Delta Switching Problem (No-Load)|Star-Delta Switching Problem (No-Load)]]
- [[#Switching Angle Optimization for Minimum Inrush|Switching Angle Optimization for Minimum Inrush]]
- [[#Multi-Winding Transient Initial Conditions|Multi-Winding Transient Initial Conditions]]
- [[#Mitigation of Harmonics|Mitigation of Harmonics]]
- [[#Open Delta Corner Voltage|Open Delta Corner Voltage]]

---

## RMS Calculation of Exciting Current with Harmonics
_(00:03 - 05:20)_

Because harmonic currents are orthogonal over a fundamental period, the total RMS current is the root sum of squares of individual harmonic RMS values:
$I_{\text{rms}} = \sqrt{I_1^2 + I_3^2 + I_5^2 + I_7^2 + \dots}$

> [!example] Problem
> Under normal saturated conditions, a transformer has 3rd, 5th, and 7th harmonics of 30%, 15%, and 5% of fundamental respectively. Find the total RMS exciting current.
> **Solution**:
> $I_{\text{rms}} = \sqrt{I_1^2 + (0.30 I_1)^2 + (0.15 I_1)^2 + (0.05 I_1)^2}$
> $I_{\text{rms}} = I_1 \sqrt{1 + 0.09 + 0.0225 + 0.0025} = I_1 \sqrt{1.115} \approx 1.056 I_1$
> Harmonics increase the total RMS current drawn by the core by roughly 6%.

## Triplen Flux Paths and Core Geometry
_(05:20 - 09:57)_

Triplen (3rd) harmonics are zero-sequence and thus strictly in-phase across all three phases ($3 \times 120^\circ = 360^\circ \equiv 0^\circ$).
- In a **3-limb core**, the three co-phasal fluxes meet at the top yoke. Since their sum is not zero ($\sum \phi_3 = 3\Phi_{3m}$), they cannot return through the iron limbs.
- The flux must leak through the high-reluctance transformer oil, structural steel, and tank walls. This suppresses the 3rd harmonic flux magnitude but causes eddy current heating in the tank walls.

## Star-Delta Switching Problem (No-Load)
_(10:01 - 15:17)_

> [!example] Problem
> A star-delta transformer is fed from a balanced 3-phase supply at no load.
> **Case 1**: Switch $S_1$ (Star Neutral) and Switch $S_2$ (Delta Mesh) are both OPEN.
> - **Result**: With neutral open, 3rd harmonic current cannot flow in the primary. With delta open, it cannot circulate in the secondary. Magnetizing current is purely sinusoidal, forcing the core flux to be **flat-topped**.
> 
> **Case 2**: Switch $S_1$ is OPEN, Switch $S_2$ is CLOSED.
> - **Result**: The closed delta mesh provides a path for 3rd harmonic currents driven by the induced 3rd harmonic EMFs. Since it's at no-load, secondary line currents are zero, so fundamental currents cannot flow. The only current circulating in the delta winding is a **pure 3rd harmonic sinusoid**.

## Switching Angle Optimization for Minimum Inrush
_(15:17 - 18:40)_

The core flux following a sudden switching transient is:
$\phi(t) = -\Phi_m \cos(\omega t) + \Phi_m \cos(\omega t_0)$
- **Maximum Inrush (Worst Case)**: Switch closed at zero voltage ($\omega t_0 = 0$). Transient offset is $\Phi_m$, causing flux to double to $2\Phi_m$.
- **Minimum Inrush (Ideal Case)**: Switch closed at maximum voltage ($\omega t_0 = 90^\circ$). Transient offset $\Phi_m \cos(90^\circ) = 0$. The core immediately enters steady-state, drawing no inrush current.

## Multi-Winding Transient Initial Conditions
_(18:40 - 25:36)_

> [!example] Problem
> A transformer has 3 identical windings ($N_1=N_2=N_3$). Primary is fed by a switch opening at $t=0$. Secondary 1 connects to a $10\,\Omega$ resistor. Secondary 2 connects to a $15\,\mu\text{F}$ capacitor charged to $5\,\text{V}$ (dotted terminal negative). Find $V_P(0^+)$ and $I_R(0^+)$.
> **Solution**:
> - Capacitor voltage cannot jump. $v_C(0^+) = v_C(0^-) = 5\,\text{V}$.
> - The charged capacitor acts as a voltage source, placing $-5\,\text{V}$ on its dotted terminal.
> - By turns ratio (1:1:1) and dot convention, all dotted terminals are at $-5\,\text{V}$.
> - Primary voltage: $V_P(0^+t) = -5\,\text{V}$.
> - Resistor current: $I_R(0^+) = \frac{-5\,\text{V}}{10\,\Omega} = -0.5\,\text{A}$.

## Mitigation of Harmonics
_(25:36 - 30:47)_

Magnetic saturation is the primary cause of harmonics, resulting in higher core/copper losses and communication interference.
Methods to reduce/mitigate harmonics:
1. **Adding tuned LC filters**: Can selectively block/trap specific harmonic frequencies.
2. **Delta connections**: Provides an internal closed loop for 3rd harmonic currents to circulate, preventing them from entering transmission lines.
3. *Note*: Adding a pure resistor does NOT selectively remove harmonics; it just wastes fundamental power.

## Open Delta Corner Voltage
_(30:47 - 33:34)_

If a delta winding is broken open at one corner terminal:
- Fundamental voltages sum to zero ($v_{1a} + v_{1b} + v_{1c} = 0$).
- 3rd harmonic voltages are in-phase and add directly ($v_{3a} + v_{3b} + v_{3c} = 3 E_{3m} \sin 3\omega t$).
- A voltmeter placed across the open corner will measure exactly **three times the 3rd harmonic phase voltage** ($V_{\text{open}} = 3 E_3$).

---

## Summary and Key Takeaways

- Saturated exciting current has an orthogonal RMS value given by $I_{\text{rms}} = \sqrt{I_1^2 + I_3^2 + I_5^2 + \dots}$.
- Third-harmonic fluxes in three-phase cores are in phase, forcing them to return through air, oil, and tank walls.
- Blocking third-harmonic currents in star and delta windings makes the core flux waveform flat-topped.
- In an unloaded star-delta transformer, only third-harmonic current circulates inside the closed delta mesh.
- Odd half-wave symmetry eliminates even harmonics, making the third harmonic dominant in magnetizing current.
- Switching at peak voltage ($\omega t_0 = 90^\circ$) eliminates transient DC flux and prevents switching inrush current.
- Switching at voltage zero triggers the doubling effect, driving core flux up to $2\Phi_m$.
- A voltmeter across a broken delta corner measures three times the third-harmonic phase voltage, $V_{\text{open}} = 3 E_3$.

---

[← Lec 052: Switching Transients](Lecture_052_Switching_Transients.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 131: Induction Machines Introduction →](Lecture_131_Induction_Machines_Introduction.md)
