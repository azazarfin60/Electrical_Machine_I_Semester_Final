---
title: "Electrical Machines | Lec 36 | Switching Transients | GATE/ESE Electrical Engineering"
lecture: 52
topic: "Transformers"
duration: "00:45:21"
source: "https://www.youtube.com/watch?v=ZCa9PWbW3MQ"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 051: Excitation Phenomenon 3](Lecture_051_Excitation_Phenomenon_3.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 053: Problems based on Harmonics and Inrush Current →](Lecture_053_Problems_based_on_Harmonics_and_Inrush_Current.md)

---

# Electrical Machines | Lec 36 | Switching Transients | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=ZCa9PWbW3MQ
- **Duration**: 00:45:21
- **Compiled**: 2026-09-21

---

## Overview

This lecture examines switching transients and the physics of magnetizing inrush current in power transformers. It derives the mathematical equation of core flux following sudden energization. The discussion highlights how core saturation and switching angles govern peak transient fluxes. It also analyzes protective relay coordination methods using harmonic restraint.

## Contents

- [[#Core Flux Equation and Transient Offset|Core Flux Equation and Transient Offset]]
- [[#The Flux Doubling Effect|The Flux Doubling Effect]]
- [[#Magnetizing Inrush Current|Magnetizing Inrush Current]]
- [[#Switching Angle Optimization|Switching Angle Optimization]]
- [[#Harmonic Restraint Differential Protection|Harmonic Restraint Differential Protection]]

---

## Core Flux Equation and Transient Offset
_(00:13 - 12:49)_

When an unloaded transformer is suddenly connected to a sinusoidal AC source $v(t) = V_m \sin(\omega t)$ at some switching instant $t = t_0$, the core flux cannot change instantaneously. 
By integrating Faraday's law ($v = N \frac{d\phi}{dt}$), the resulting core flux is a superposition of a steady-state AC term and a transient DC offset:
$$\phi(t) = \underbrace{-\Phi_m \cos(\omega t)}_{\text{AC Steady State}} + \underbrace{\Phi_m \cos(\omega t_0) \pm \phi_r}_{\text{Transient DC Offset}}$$
- **$\Phi_m$**: Rated peak steady-state flux.
- **$\phi_r$**: Residual (remnant) flux left in the core from previous operation.
- **$\omega t_0$**: The switching angle (the phase angle of the voltage at the exact moment the switch is closed).

Because practical transformers contain electrical resistance ($R$) in the windings and core losses, the transient DC offset is not permanent. It decays exponentially with a time constant $\tau = L/R$:
$$\phi_{\text{trans}}(t) = \left[ \Phi_m \cos(\omega t_0) \pm \phi_r \right] e^{-t/\tau}$$

## The Flux Doubling Effect
_(12:52 - 17:52)_

**Worst-Case Switching (Zero Voltage)**:
If the switch is closed exactly when the supply voltage crosses zero ($\omega t_0 = 0$, meaning $v(0) = 0$), the transient term becomes maximum:
$\phi_{\text{trans}} = \Phi_m \cos(0) = \Phi_m$
The total flux equation (ignoring residual flux) becomes:
$\phi(t) = \Phi_m(1 - \cos\omega t)$
- The entire waveform is shifted into the positive region.
- At $\omega t = \pi$ (one half-cycle later), the flux reaches exactly twice its normal peak value: **$\phi_{\text{peak}} = 2\Phi_m$**.
- This phenomenon is called **Flux Doubling**. If residual flux is present in the same direction, the peak climbs even higher to $2\Phi_m + \phi_r$.

## Magnetizing Inrush Current
_(17:55 - 22:49, 27:59 - 39:59)_

Normal steady-state operation occurs near the knee of the B-H curve, drawing a very small magnetizing current (3% to 5% of full-load current).
- During flux doubling ($2\Phi_m$), the core is driven deep into extreme magnetic saturation (operating almost like an air core).
- To establish this doubled flux, the transformer draws an enormous surge of current called **Magnetizing Inrush Current**.
- Peak inrush current can reach **5 to 10 times the rated full-load current**.

**Properties of Inrush Current**:
1. **Unidirectional**: Because the flux oscillates entirely in the positive region, the inrush current consists of sharp, positive, unidirectional pulses.
2. **Breaks Half-Wave Symmetry**: Because the positive and negative half-cycles are not identical, Fourier analysis dictates that the waveform contains **even harmonics**.
3. **2nd Harmonic Dominance**: The **second harmonic** ($2\omega$) is the most dominant harmonic component in magnetizing inrush current.
4. **Mechanical Stress**: Because electromagnetic forces scale with the square of the current ($F \propto i^2$), inrush current generates massive repulsive forces (up to 100x normal) between windings, requiring heavy mechanical bracing.

## Switching Angle Optimization
_(22:58 - 27:56)_

To avoid switching transients entirely, the DC offset term must be zero:
$\phi_{\text{trans}} = \Phi_m \cos(\omega t_0) = 0 \implies \omega t_0 = 90^\circ \ (\pi/2)$
- **Transient-Free Switching**: If the transformer is energized exactly at the **peak of the supply voltage** ($v = V_m$), no transient offset occurs. The flux immediately tracks its normal steady-state trajectory.
- In practice, poles close randomly, meaning the switching angle usually lies somewhere between $0$ and $90^\circ$, causing an intermediate level of inrush current.

## Harmonic Restraint Differential Protection
_(39:59 - 45:13)_

Transformers use differential protection relays to detect internal faults ($I_{\text{diff}} = |I_1 - I_2|$).
- **The Problem**: During energization, $I_2 = 0$ but $I_1 = I_{\text{inrush}}$, which is massive. The relay sees this as an internal fault and will incorrectly trip the circuit breaker (maloperation).
- **The Solution**: Use a **Harmonic-Restraint Differential Relay**.
- **How it works**: Genuine short circuits are almost pure fundamental frequency ($50$ Hz). Inrush current is rich in the 2nd harmonic ($100$ Hz). The relay contains a restraining coil tuned to the 2nd harmonic. If high 2nd harmonic content is detected, the relay blocks the tripping signal, recognizing the event as a transient inrush rather than a fault.

---

## Summary and Key Takeaways

- Sudden transformer energization induces an AC switching transient consisting of an alternating steady-state component and a unidirectional DC flux offset: $\phi(t) = -\Phi_m \cos(\omega t) + \Phi_m \cos(\omega t_0) \pm \phi_r$.
- Switching on at the instant of zero voltage ($\omega t_0 = 0$) causes flux doubling, where peak core flux reaches twice steady-state amplitude: $\phi_{\max} = 2\Phi_m$.
- Pre-existing remnant flux pushes peak core flux even higher to $\phi_{\max} = 2\Phi_m + \phi_r$.
- Switching on at peak supply voltage ($\omega t_0 = \pi/2$) eliminates the transient DC offset completely, producing a transient-free response.
- Severe core saturation during flux doubling produces magnetizing inrush currents of $5$ to $10$ times rated full-load current.
- Unidirectional flux offsets break half-wave symmetry, making the second harmonic ($2^{\text{nd}}$ harmonic) the most dominant harmonic in inrush current.
- Large inrush currents produce repulsive electromagnetic forces scaling with current squared ($F \propto i^2$), requiring heavy winding bracing.
- Circuit resistance and core losses provide natural damping, causing the DC flux offset and inrush current to decay exponentially with time constant $\tau = L/R$.
- Harmonic-restraint differential relays use second-harmonic current in their restraining coils to block false tripping during inrush while maintaining sensitivity to genuine faults.

---

[← Lec 051: Excitation Phenomenon 3](Lecture_051_Excitation_Phenomenon_3.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 053: Problems based on Harmonics and Inrush Current →](Lecture_053_Problems_based_on_Harmonics_and_Inrush_Current.md)
