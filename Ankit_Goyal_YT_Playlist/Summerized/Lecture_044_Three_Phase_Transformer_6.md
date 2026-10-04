---
title: "Electrical Machines | Lec 30 | Three Phase Transformer - 6 | GATE/ESE Electrical Engineering Lecture"
lecture: 44
topic: "Transformers"
duration: "01:00:31"
source: "https://www.youtube.com/watch?v=3V5Xq4NJVGs"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 043: Three Phase Transformer 5](Lecture_043_Three_Phase_Transformer_5.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 045: Three Phase Transformer 7 →](Lecture_045_Three_Phase_Transformer_7.md)

---

# Electrical Machines | Lec 30 | Three Phase Transformer - 6 | GATE/ESE Electrical Engineering Lecture

- **Source**: https://www.youtube.com/watch?v=3V5Xq4NJVGs
- **Duration**: 01:00:31
- **Compiled**: 2026-09-21

---

## Overview

This lecture covers the theory, construction, and phasor analysis of zigzag transformer connections. It explains why third-harmonic voltages are co-phasal and how series subtractive connections eliminate them. The discussion details the delta-zigzag star configuration, establishing the Dz0 and Dz6 vector groups. It then analyzes the star-zigzag star connection and determines its Yz1 clock group classification. Finally, the lecture compares voltage transformation ratios between zigzag connections and standard three-phase configurations.

## Contents

- [[#Motivation: Third-Harmonic Cancellation|Motivation: Third-Harmonic Cancellation]]
- [[#Delta-Zigzag Star Configuration|Delta-Zigzag Star Configuration]]
- [[#Phasor Construction for Delta-Zigzag Star|Phasor Construction for Delta-Zigzag Star]]
- [[#Voltage Ratios in Delta-Zigzag Star|Voltage Ratios in Delta-Zigzag Star]]
- [[#Star-Zigzag Star Connection|Star-Zigzag Star Connection]]

---

## Motivation: Third-Harmonic Cancellation
_(00:12 - 09:39)_

The primary purpose of a zigzag connection is to eliminate third-harmonic voltages.
Third-harmonic voltages have frequencies $3\omega$. Their phase shifts are multiplied by 3:
- $V_{A3} = V_{m3} \sin(3\omega t)$
- $V_{B3} = V_{m3} \sin(3(\omega t - 120^\circ)) = V_{m3} \sin(3\omega t - 360^\circ) = V_{m3} \sin(3\omega t)$
- $V_{C3} = V_{m3} \sin(3(\omega t + 120^\circ)) = V_{m3} \sin(3\omega t + 360^\circ) = V_{m3} \sin(3\omega t)$

Third-harmonic voltages are identical in magnitude and time phase. They are **co-phasal**.
Because they are identical, subtracting one phase voltage from another eliminates them: $V_{A3} - V_{B3} = 0$.

**Zigzag Principle**: Connect two half-windings from different phases in series with subtractive polarity. This cancels third harmonics while preserving the fundamental component.
Subtractive polarity means connecting like terminals together (dotted to dotted, or undotted to undotted).

## Delta-Zigzag Star Configuration
_(09:50 - 15:00)_

Primary is delta-connected. Secondary phase windings are divided into two equal halves (each with $N_S/2$ turns).
**Parity Convention**:
- Dotted terminals: Even numbers ($2, 4$)
- Undotted terminals: Odd numbers ($1, 3$)

**Undotted-to-Undotted Subtractive Polarity**:
1. Neutral: Connect $A_2, B_2, C_2$.
2. Interconnects: $A_1 \to B_3$, $B_1 \to C_3$, $C_1 \to A_3$.
3. Lines: $A_4, B_4, C_4$.

![Wiring diagram of delta-zigzag star with neutral at A2, B2, C2](frames/044/frame_0015_12m31s.jpg)

## Phasor Construction for Delta-Zigzag Star
_(15:01 - 30:27)_

**Phasor Rules**:
- From neutral $A_2$ to $A_1$ is Even $\to$ Odd. Reverses primary orientation ($1 \to 2$).
- From $B_3$ to $B_4$ is Odd $\to$ Even. Keeps primary orientation.

**Dz0 Configuration**:
- Neutral at $A_2, B_2, C_2$ (even terminals).
- Connections: $A_1 \to B_3$, etc.
- Phasor sum gives $A_4, B_4, C_4$ identical in direction to primary line voltages.
- Result: $0^\circ$ phase shift $\implies \text{Dz0}$.

**Dz6 Configuration**:
- Neutral at $A_1, B_1, C_1$ (odd terminals).
- Connections: $A_2 \to B_4$, etc.
- Phasor sum gives $180^\circ$ reversal.
- Result: $180^\circ$ phase shift $\implies \text{Dz6}$.

## Voltage Ratios in Delta-Zigzag Star
_(30:56 - 41:58)_

Secondary phase voltage is the vector sum of two half-windings separated by $60^\circ$:
$$V_{ph(\text{secondary})} = \sqrt{\left(\frac{V_1}{2x}\right)^2 + \left(\frac{V_1}{2x}\right)^2 + 2\left(\frac{V_1}{2x}\right)^2 \cos 60^\circ} = \frac{\sqrt{3}}{2} V_1 \left(\frac{N_S}{N_P}\right)$$
where $x = N_P / N_S$.
Secondary line voltage: $V_{LS} = \sqrt{3} V_{ph(\text{sec})} = \frac{3}{2} V_{LP} \left(\frac{N_S}{N_P}\right)$.
Line voltage ratio:
$$\frac{V_{LP}}{V_{LS}} = \frac{2}{3} \left(\frac{N_P}{N_S}\right) \approx 0.667 \left(\frac{N_P}{N_S}\right)$$

Compared to delta-star, the delta-zigzag yields $86.6\%$ ($\sqrt{3}/2$) of the secondary phase voltage for identical turns.

## Star-Zigzag Star Connection
_(41:58 - 57:46)_

Primary is star. Secondary is zigzag.
**Yz1 Classification**:
- Secondary phase voltage is the sum of two phasors displaced by $120^\circ$.
- $V_{an} = V_{C2C1} + V_{A3A4} = \frac{V}{2}\left(\frac{N_S}{N_P}\right)\angle -60^\circ + \frac{V}{2}\left(\frac{N_S}{N_P}\right)\angle 0^\circ = \frac{\sqrt{3}}{2} V\left(\frac{N_S}{N_P}\right)\angle -30^\circ$.
- Secondary phase lags primary phase by $30^\circ$ $\implies \text{Yz1}$.

Line Voltage Ratio:
$$\frac{V_{LP}}{V_{LS}} = \frac{\sqrt{3} V_{ph,p}}{\sqrt{3} V_{ph,s}} = \frac{\sqrt{3} V}{\frac{3}{2} V \left(\frac{N_S}{N_P}\right)} = \frac{2}{\sqrt{3}}\left(\frac{N_P}{N_S}\right) \approx 1.155\left(\frac{N_P}{N_S}\right)$$
Secondary line voltage is $86.6\%$ of standard star-star.

---

## Summary and Key Takeaways

- Third-harmonic voltages in a balanced three-phase system have identical phase angles, making them co-phasal.
- Connecting two half-windings from different phases in series with subtractive polarity cancels co-phasal third-harmonic voltages completely.
- In delta-zigzag star, undotted-to-undotted interconnections with neutral at even terminals produce the $\text{Dz0}$ vector group with $0^\circ$ phase shift.
- In delta-zigzag star, dotted-to-dotted interconnections with neutral at undotted terminals produce the $\text{Dz6}$ vector group with $180^\circ$ phase shift.
- The line voltage ratio for delta-zigzag star is $\frac{V_{LP}}{V_{LS}} = \frac{2}{3}\left(\frac{N_P}{N_S}\right)$, giving a secondary voltage $86.6\%$ of that in standard delta-star.
- Star-zigzag star with neutral at $A_2, B_2, C_2$ produces the $\text{Yz1}$ vector group, where secondary voltage lags primary voltage by $30^\circ$.
- The line voltage ratio for star-zigzag star is $\frac{V_{LP}}{V_{LS}} = \frac{2}{\sqrt{3}}\left(\frac{N_P}{N_S}\right) \approx 1.155\left(\frac{N_P}{N_S}\right)$.
- To produce the same secondary output voltage as standard connections, a zigzag secondary requires $15.5\%$ more copper turns.

---

[← Lec 043: Three Phase Transformer 5](Lecture_043_Three_Phase_Transformer_5.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 045: Three Phase Transformer 7 →](Lecture_045_Three_Phase_Transformer_7.md)
