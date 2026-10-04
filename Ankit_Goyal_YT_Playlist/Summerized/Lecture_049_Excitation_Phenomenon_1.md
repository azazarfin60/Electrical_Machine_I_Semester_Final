---
title: "Electrical Machines | Lec 33 | Excitation Phenomenon - 1 | GATE/ESE Electrical Engineering"
lecture: 49
topic: "Transformers"
duration: "01:21:13"
source: "https://www.youtube.com/watch?v=rBRZW_8Meng"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 048: Problems based on Parallel Operation of Transformer](Lecture_048_Problems_based_on_Parallel_Operation_of_Transformer.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 050: Excitation Phenomenon 2 →](Lecture_050_Excitation_Phenomenon_2.md)

---

# Electrical Machines | Lec 33 | Excitation Phenomenon - 1 | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=rBRZW_8Meng
- **Duration**: 01:21:13
- **Compiled**: 2026-09-21

---

## Overview

This lecture examines the excitation phenomenon in transformers under non-linear magnetic core conditions. When magnetic saturation is accounted for, core flux and magnetizing current cannot be sinusoidal at the same time. A sinusoidal flux forces the magnetizing current into a sharply peaked waveform with a dominant third harmonic. Conversely, constraining the current to a sinusoid clips the core flux into a flat-topped wave, which induces dangerous spiky voltages across connected loads. Incorporating hysteresis shifts the excitation current ahead of the flux by the hysteresis angle $\beta$ to supply active core losses.

## Contents

- [[#Non-Linear Magnetization and Saturation|Non-Linear Magnetization and Saturation]]
- [[#Fourier Analysis and Half-Wave Symmetry|Fourier Analysis and Half-Wave Symmetry]]
- [[#Effect of Hysteresis and Dynamic B-H Loop|Effect of Hysteresis and Dynamic B-H Loop]]
- [[#The Duality: Flat-Topped Flux vs. Peaky Current|The Duality: Flat-Topped Flux vs. Peaky Current]]
- [[#Harmonic Amplification in Induced EMF|Harmonic Amplification in Induced EMF]]

---

## Non-Linear Magnetization and Saturation
_(00:13 - 14:42)_

Practical ferromagnetic cores are non-linear. The $\Phi-i$ characteristic dictates that flux $\Phi$ and magnetizing current $I_\mu$ cannot simultaneously be sinusoidal (unless operating in an air-core/linear region).

**Case 1: Sinusoidal Flux**
If the applied voltage is sinusoidal, core flux is sinusoidal ($\phi(t) = \Phi_m \sin \omega t$).
To maintain this sinusoidal flux near the saturation knee, a disproportionately large magnetizing current is required. This forces $I_\mu(t)$ into a **sharply peaked** (peaky) waveform, symmetric about its peak at $\omega t = 90^\circ$.

## Fourier Analysis and Half-Wave Symmetry
_(14:52 - 37:42)_

The peaky $I_\mu(t)$ waveform is periodic and non-sinusoidal. It possesses **half-wave symmetry**:
$$f\left(t \pm \frac{T}{2}\right) = -f(t)$$
*Consequence*: It contains **zero DC component** and **zero even harmonics**. It consists only of odd harmonics ($n=1, 3, 5, 7, \dots$).

The Fourier series for the peaky magnetizing current is:
$$i_\mu(t) = I_{m1} \sin(\omega t) - I_{m3} \sin(3\omega t) + I_{m5} \sin(5\omega t) - \dots$$

**Role of the Third Harmonic ($I_{m3}$)**:
- It is the most dominant harmonic (largest amplitude after the fundamental).
- The negative sign ($-I_{m3}$) is crucial: at $\omega t = 90^\circ$, $-I_{m3} \sin(270^\circ) = +I_{m3}$.
- It adds constructively to the fundamental peak ($I_{m1} + I_{m3}$), creating the sharp crest.

## Effect of Hysteresis and Dynamic B-H Loop
_(37:45 - 58:26)_

When hysteresis is included, the relationship between flux and current traces a hysteresis loop. The total no-load current is $\vec{I}_0 = \vec{I}_\mu + \vec{I}_w$.
- **Phase Lead**: $I_0(t)$ crosses zero *before* $\phi(t)$ crosses zero. $I_0$ leads $\Phi$ by the **hysteresis angle** $\beta$.
- **Active Power**: This phase shift occurs because the core requires active power (supplied by in-phase current $I_h$) to overcome hysteresis losses.
- **Dynamic B-H Loop**: Under AC excitation, eddy currents oppose the main flux, requiring more source current. This broadens the static hysteresis loop into a dynamic B-H loop, whose total area represents total core loss ($P_h + P_e$). Projection from this dynamic loop gives the total core loss current $I_w$.

## The Duality: Flat-Topped Flux vs. Peaky Current
_(58:26 - 68:02)_

**Case 2: Sinusoidal Magnetizing Current**
If the magnetizing current is forced to be sinusoidal (e.g., via a current source), the resulting core flux is clipped by saturation, creating a **flat-topped** (trapezoidal) waveform.

The Fourier series for the flat-topped flux is:
$$\phi(t) = \Phi_{m1} \sin(\omega t) + \Phi_{m3} \sin(3\omega t) + \dots$$
- The positive sign ($+\Phi_{m3}$) subtracts from the peak at $\omega t = 90^\circ$: $+\Phi_{m3} \sin(270^\circ) = -\Phi_{m3}$, causing the flattening of the crest.

> [!info] Mutual Exclusivity
> In a saturable core, $\Phi$ and $I_\mu$ cannot both be sinusoidal. Exactly one must contain a dominant third harmonic.

## Harmonic Amplification in Induced EMF
_(68:11 - 81:07)_

If the core flux is flat-topped, the induced EMF $e(t) = -N \frac{d\phi}{dt}$ becomes heavily distorted.
Differentiating the flux series:
$$e(t) = -N\omega \left[ \Phi_{m1} \cos(\omega t) + 3\Phi_{m3} \cos(3\omega t) + 5\Phi_{m5} \cos(5\omega t) + \dots \right]$$

**Harmonic Amplification Rule**:
The proportion of the $n$-th harmonic in the induced voltage is multiplied by its harmonic order $n$:
$$\frac{E_n}{E_1} = n \left(\frac{\Phi_n}{\Phi_1}\right)$$
A 10% third-harmonic flux distortion becomes a 30% third-harmonic voltage distortion.

**Practical Consequence**:
The resulting EMF waveform is narrow and **spiky** (zero voltage during the flat flux plateau, sharp spikes during flux transitions). While a flat-topped flux reduces core losses (lower $B_m$), the spiky induced voltage is catastrophic for connected loads (motor overheating, insulation stress). Thus, power systems strictly operate with **sinusoidal flux** and tolerate the peaky magnetizing current.

---

## Summary and Key Takeaways

- Magnetic saturation makes core flux $\Phi$ and magnetizing current $I_\mu$ mutually exclusive sinusoids in ferromagnetic cores.
- A sinusoidal core flux produces a peaky magnetizing current waveform containing odd harmonics dominated by the third harmonic: $i_\mu(t) = I_{m1}\sin(\omega t) - I_{m3}\sin(3\omega t) + \dots$.
- Because $I_\mu(t)$ satisfies half-wave symmetry $x(t + T/2) = -x(t)$, DC bias and all even harmonics are identically zero.
- Core hysteresis shifts total excitation current $I_0$ ahead of flux by the hysteresis angle $\beta$, where in-phase component $I_h$ delivers active hysteresis loss power and quadrature component $I_\mu$ supplies reactive field power.
- Expanding the static B-H curve into a wider dynamic B-H loop incorporates eddy current losses and yields the full core loss current $I_w = I_h + I_e$.
- A sinusoidal magnetizing current produces a flat-topped flux waveform described by $\phi(t) = \Phi_{m1}\sin(\omega t) + \Phi_{m3}\sin(3\omega t) + \dots$, where the positive third-harmonic sign depresses the crest at $90^\circ$.
- Time differentiation $e = -N d\phi/dt$ multiplies each $n$-th harmonic in flat-topped flux by order $n$, producing a spiky induced EMF that causes severe heating and torque pulsations in connected loads.
- Power systems strictly enforce sinusoidal flux operation because harmonic currents remain confined to transformer windings without entering load circuits.

---

[← Lec 048: Problems based on Parallel Operation of Transformer](Lecture_048_Problems_based_on_Parallel_Operation_of_Transformer.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 050: Excitation Phenomenon 2 →](Lecture_050_Excitation_Phenomenon_2.md)
