---
title: "Electrical Machines | Lec 35 | Excitation Phenomenon - 3 | GATE/ESE Electrical Engineering"
lecture: 51
topic: "Transformers"
duration: "01:10:18"
source: "https://www.youtube.com/watch?v=gqVpwEHk3nA"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 050: Excitation Phenomenon 2](Lecture_050_Excitation_Phenomenon_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 052: Switching Transients →](Lecture_052_Switching_Transients.md)

---

# Electrical Machines | Lec 35 | Excitation Phenomenon - 3 | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=gqVpwEHk3nA
- **Duration**: 01:10:18
- **Compiled**: 2026-09-21

---

## Overview

This lecture analyzes harmonic excitation phenomena and zero-sequence flux behavior in three-phase transformers. It links core geometry to the circulation paths of third-harmonic flux. The discussion establishes the mechanism of the oscillating neutral in ungrounded star-star systems. It also details the harmonic trapping behavior of delta windings and tertiary stabilization circuits.

## Contents

- [[#Ungrounded Star-Star Connection & The Oscillating Neutral|Ungrounded Star-Star Connection & The Oscillating Neutral]]
- [[#Impact of Core Geometry on Triplen Flux|Impact of Core Geometry on Triplen Flux]]
- [[#Grounded Star-Star Connection & Communication Interference|Grounded Star-Star Connection & Communication Interference]]
- [[#Delta Windings: Harmonic Confinement|Delta Windings: Harmonic Confinement]]
- [[#Tertiary Delta Winding|Tertiary Delta Winding]]
- [[#Harmonic Voltage Calculation Rule|Harmonic Voltage Calculation Rule]]

---

## Ungrounded Star-Star Connection & The Oscillating Neutral
_(14:54 - 36:14)_

In an ungrounded star-star transformer, triplen harmonic currents cannot flow ($I_3 = 0$). This forces a flat-topped flux and peaky induced phase voltages.

**Voltage Amplification**:
Taking the derivative of flux amplifies voltage distortion by harmonic order $n$. A 20% 3rd-harmonic flux becomes a 60% 3rd-harmonic voltage:
$\frac{E_n}{E_1} = n \left(\frac{\Phi_n}{\Phi_1}\right)$

**The Oscillating Neutral**:
Because phase voltages contain massive 3rd-harmonic components ($v_{an3} = v_{bn3} = v_{cn3} = V_{m3} \cos 3\omega t$), the physical neutral potential $N'$ is no longer at the geometric center $N$.
- The effective neutral $N'$ rotates around the stationary fundamental neutral $N$ in a circle of radius $V_3$ at triple angular speed ($3\omega$).
- Line voltages remain perfectly balanced and sinusoidal ($V_{L3} = 0$), but phase voltages fluctuate wildly.
- *Consequence*: You cannot connect single-phase loads (phase-to-neutral) to an ungrounded star-star transformer; the voltage fluctuations will damage equipment.

## Impact of Core Geometry on Triplen Flux
_(06:10 - 14:54, 36:14 - 42:21)_

Because 3rd harmonic fluxes ($\Phi_{a3}, \Phi_{b3}, \Phi_{c3}$) are zero-sequence, they flow in the same direction simultaneously. Their ability to exist depends on the core providing a return path:
- **3-Phase Bank (3 Single-Phase Units)**: Each phase has an independent closed iron path. Triplen flux establishes easily $\implies$ huge voltage distortion.
- **5-Limb Core**: The two outer limbs provide a low-reluctance return path for zero-sequence flux. Triplen flux establishes easily $\implies$ huge voltage distortion.
- **3-Limb Core**: At the top yoke, the three co-phasal fluxes meet ($3\Phi_3$). There is no iron return path. The flux must leak through the surrounding oil, air, and steel tank walls.
  - *Result*: The high reluctance of air/oil suppresses $\Phi_3$. Voltage distortion is minimal.
  - *Drawback*: The flux penetrating the steel tank induces eddy currents, causing tank heating. (Mitigated by using non-magnetic/conductive aluminum tanks).

## Grounded Star-Star Connection & Communication Interference
_(42:24 - 47:33)_

Grounding the neutral provides a path for 3rd harmonic currents ($i_n = 3i_{a3}$).
- **Benefit**: The magnetizing current becomes peaky, meaning the flux and induced voltages become perfectly sinusoidal. The oscillating neutral is eliminated.
- **Drawback**: The 3rd harmonic currents flow out along all three transmission lines in phase. Their magnetic fields add up ($3\Phi_3 \neq 0$) and induce 150 Hz noise voltages in adjacent parallel telephone/communication lines. This creates severe electromagnetic interference (EMI).

## Delta Windings: Harmonic Confinement
_(47:33 - 59:40)_

Any connection with a Delta winding ($\Delta-Y, Y-\Delta, \Delta-\Delta$) provides a closed internal loop for zero-sequence voltages.
- The induced 3rd harmonic EMFs drive a circulating 3rd harmonic current around the Delta loop ($I_3 = E_3 / Z_3$).
- This circulating current cancels the 3rd harmonic core flux, restoring sinusoidal flux and sinusoidal phase voltages.
- **Harmonic Trapping**: By KCL at the delta nodes ($I_{L3} = I_{A3} - I_{B3} = 0$), the 3rd harmonic currents remain entirely trapped *inside* the delta mesh. They never enter the transmission lines.
- *Conclusion*: Delta connections eliminate both the oscillating neutral AND communication line interference.

## Tertiary Delta Winding
_(59:40 - 66:27)_

When a Star-Star connection is required for transmission reasons (e.g., grounding), a third winding connected in Delta is added on the same core, creating a 3-winding transformer ($Y-Y-\Delta$).
**Functions of the Tertiary Delta**:
1. Circulates 3rd harmonic currents internally to suppress the oscillating neutral and prevent telephone interference.
2. Interconnects a third voltage level.
3. Provides a connection point for reactive power compensation (capacitor banks/synchronous condensers).
4. Supplies substation auxiliary loads (fans, lighting).

## Harmonic Voltage Calculation Rule
_(66:27 - 70:10)_

For numerical exam problems:
- **Star Connection**: Include 3rd harmonics in phase voltages ($V_{ph} = \sqrt{V_1^2 + V_3^2 + \dots}$). Exclude 3rd harmonics from line voltages ($V_L = \sqrt{3}\sqrt{V_1^2 + V_5^2 + \dots}$). The ratio $V_L/V_{ph}$ will be less than $\sqrt{3}$.
- **Delta Connection**: 3rd harmonics are cancelled by the internal impedance drop. Exclude 3rd harmonics from *both* phase and line voltages ($V_{ph} = V_L$).

---

## Summary and Key Takeaways

- In three-phase transformers, third-harmonic components are co-phasal zero-sequence quantities with identical phase angles across all three phases.
- Differentiating flux magnifies voltage distortion by the harmonic order: $E_n / E_1 = n (\Phi_n / \Phi_1)$, raising the third-harmonic induced voltage distortion by a factor of three.
- In ungrounded star-star systems, the effective neutral $N'$ rotates around the stationary fundamental circumcenter $N$ in a circle of radius $V_3$ at triple angular speed $3\omega$.
- Three-phase banks and five-limb cores provide low-reluctance iron paths that sustain high third-harmonic flux $\Phi_3$ and peaky phase voltages.
- Three-limb cores lack an iron return path for zero-sequence flux, forcing third-harmonic flux into the surrounding oil, air, and tank walls.
- Grounding the neutral in star-star systems allows third-harmonic currents to flow through transmission lines, which causes electromagnetic interference in parallel communication circuits.
- Delta windings form closed meshes where zero-sequence EMFs drive circulating currents $I_3 = E_3 / Z_3$ that cancel core harmonic flux and suppress the oscillating neutral.
- Third-harmonic currents trapped within delta meshes cannot enter external lines ($I_{L3} = 0$), completely eliminating communication line noise.
- Delta tertiary windings in three-winding transformers ($Y-Y-\Delta$) stabilize the neutral potential, improve station power factor, and allow single-phase phase-to-neutral loading.

---

[← Lec 050: Excitation Phenomenon 2](Lecture_050_Excitation_Phenomenon_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 052: Switching Transients →](Lecture_052_Switching_Transients.md)
