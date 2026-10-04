---
title: "Electrical Machines | Lec 34 | Excitation Phenomenon - 2 | GATE/ESE Electrical Engineering"
lecture: 50
topic: "Transformers"
duration: "00:57:03"
source: "https://www.youtube.com/watch?v=jEL_42aqTmk"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 049: Excitation Phenomenon 1](Lecture_049_Excitation_Phenomenon_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 051: Excitation Phenomenon 3 →](Lecture_051_Excitation_Phenomenon_3.md)

---

# Electrical Machines | Lec 34 | Excitation Phenomenon - 2 | GATE/ESE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=jEL_42aqTmk
- **Duration**: 00:57:03
- **Compiled**: 2026-09-21

---

## Overview

This lecture investigates harmonic behavior and excitation phenomena in three-phase transformers. It establishes symmetrical sequence properties across all odd harmonic orders using Fourier series expansions. The discussion then analyzes how star and delta winding topologies handle zero-sequence triplen harmonics. Finally, it links winding connections to core flux distortion and terminal waveform quality.

## Contents

- [[#Review of Core Excitation Rule|Review of Core Excitation Rule]]
- [[#Harmonic Sequence Classification|Harmonic Sequence Classification]]
- [[#Behavior of Triplen Harmonics in Star Connection|Behavior of Triplen Harmonics in Star Connection]]
- [[#Behavior of Triplen Harmonics in Delta Connection|Behavior of Triplen Harmonics in Delta Connection]]
- [[#Summary Matrix: 3rd Harmonics vs Connections|Summary Matrix: 3rd Harmonics vs Connections]]

---

## Review of Core Excitation Rule
_(00:13 - 05:17)_

**The Core Rule**: Magnetic core saturation strictly requires the third harmonic to exist either in the magnetizing current or the magnetic flux. It cannot vanish from both. 
- **Desired Operation**: Allow the 3rd harmonic to flow freely in the magnetizing current. This ensures core flux remains sinusoidal, keeping the induced secondary voltage clean and sinusoidal.
- **Undesired Operation**: Block the 3rd harmonic current. The core flux becomes flat-topped, inducing a spiky, highly distorted secondary voltage.

## Harmonic Sequence Classification
_(05:17 - 20:37)_

In a balanced three-phase system ($v_a, v_b, v_c$), odd harmonics resolve into three distinct symmetrical sequences:

| Group Formula | Harmonic Orders | Sequence Type | Phase Rotation |
| :--- | :--- | :--- | :--- |
| $3k$ (odd $k$) | 3, 9, 15, 21 | Zero sequence | Co-phasal ($0^\circ$ displacement) |
| $6k - 1$ | 5, 11, 17, 23 | Negative sequence | $A-C-B$ rotation |
| $6k + 1$ | 7, 13, 19, 25 | Positive sequence | $A-B-C$ rotation |

**Properties of Triplen (3rd) Harmonics**:
- The 3rd harmonic is the lowest order odd harmonic, thus the most dominant in magnitude.
- Triplen harmonics are **co-phasal** (zero sequence). They have $0^\circ$ relative phase shift: 
  $v_{a3}(t) = v_{b3}(t) = v_{c3}(t) = V_{m3} \sin(3\omega t)$.
- Their sum is non-zero: $v_{a3} + v_{b3} + v_{c3} = 3 V_{m3} \sin(3\omega t)$.

## Behavior of Triplen Harmonics in Star Connection
_(20:46 - 34:54)_

**Voltages**:
Line voltage is the difference of phase voltages ($v_{ab} = v_{an} - v_{bn}$). Because 3rd harmonics are identical in all phases, they cancel out completely:
$v_{ab3} = v_{an3} - v_{bn3} = V_{m3}\sin(3\omega t) - V_{m3}\sin(3\omega t) = 0$.
- *Conclusion*: **Line voltages in Star never contain 3rd harmonics ($V_{L3} = 0$).**

**Currents**:
By KCL at the neutral point: $i_n = i_a + i_b + i_c$.
- **Ungrounded Star (3-wire)**: $i_n$ must be 0. Thus, $3 i_{a3} = 0 \implies i_{a3} = 0$. 3rd harmonic currents *cannot* flow. (This forces flat-topped flux).
- **Grounded Star (4-wire)**: The neutral wire provides a return path. $i_{n3} = 3 i_{a3}$. 3rd harmonic currents flow freely. (This allows sinusoidal flux).

## Behavior of Triplen Harmonics in Delta Connection
_(34:57 - 54:49)_

**Voltages**:
- **Open Delta**: KVL around an open delta loop sums the phase EMFs. The fundamental, 5th, and 7th sum to zero. The 3rd harmonics add directly. A voltmeter across the open corner reads $V_{\text{voltmeter}} \approx 3 E_{3,\text{rms}}$.
- **Closed Delta**: The net 3rd harmonic EMF drives a circulating 3rd harmonic current ($I_3$) inside the closed mesh. This current flows until its internal impedance drop ($I_3 Z_3$) cancels the induced EMF ($E_3$). Thus, terminal phase voltage $V_{\text{ph3}} = E_3 - I_3 Z_3 = 0$.

**Currents**:
By KCL at a delta node to find line current: $I_{A3} = I_{AB3} - I_{CA3}$.
Since the circulating 3rd harmonic currents are identical ($I_{AB3} = I_{CA3}$):
$I_{A3} = 0$.
- *Conclusion*: **3rd harmonic currents circulate in the Delta loop but cannot enter the line ($I_{L3} = 0$).** (The circulating current allows the core flux to remain sinusoidal).

## Summary Matrix: 3rd Harmonics vs Connections
_(54:54 - 56:55)_

| Parameter (3rd Harmonic) | Star (Y) | Delta ($\Delta$) |
| :--- | :--- | :--- |
| **Phase Voltage ($V_{ph3}$)** | Can exist (peaky if ungrounded) | Zero (canceled by internal loop drop) |
| **Line Voltage ($V_{L3}$)** | Zero (canceled by phase subtraction) | Zero ($V_L = V_{ph} = 0$) |
| **Phase Current ($I_{ph3}$)** | Exists only if neutral is grounded | Circulates in closed loop |
| **Line Current ($I_{L3}$)** | Exists only if neutral is grounded | Zero (trapped in loop by KCL) |

**Golden Rule for Three-Phase Banks**:
Any connection that provides a closed path for 3rd harmonic currents (Delta loop or grounded-neutral Star) allows the core flux and terminal voltages to remain sinusoidal. An isolated neutral Star (without a Delta) blocks 3rd harmonic currents, forcing peaky, distorted phase voltages.

---

## Summary and Key Takeaways

- Odd harmonic orders in balanced three-phase systems divide into three sequence groups: triplen harmonics ($3k$) are zero-sequence, $6k-1$ harmonics are negative-sequence, and $6k+1$ harmonics are positive-sequence.
- Triplen harmonic components ($3^{\text{rd}}, 9^{\text{th}}, 15^{\text{th}}$) are co-phasal and have identical instantaneous values across all three phases.
- Star connections eliminate all triplen harmonics from line voltages ($V_{L3} = 0$) because phase subtraction cancels identical co-phasal quantities.
- Star phase windings carry third-harmonic currents only when the neutral terminal connects to ground.
- The neutral conductor of a balanced grounded star system carries three times the third-harmonic phase current ($i_n = 3 I_{m3}\sin 3\omega t$).
- An ideal voltmeter across an open corner of a delta winding measures the sum of co-phasal triplen EMFs ($V_{\text{rms}} \approx 3 E_3$).
- In a closed delta winding, third-harmonic currents circulate freely inside the mesh but cannot enter external line conductors ($I_{L3} = 0$).
- Circulating delta currents produce an internal impedance drop that cancels the induced third-harmonic EMF at the terminals ($V_{AB3} = 0$).

---

[← Lec 049: Excitation Phenomenon 1](Lecture_049_Excitation_Phenomenon_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 051: Excitation Phenomenon 3 →](Lecture_051_Excitation_Phenomenon_3.md)
