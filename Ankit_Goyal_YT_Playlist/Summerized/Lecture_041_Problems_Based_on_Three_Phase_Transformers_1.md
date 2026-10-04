---
title: "Problems Based on Three Phase Transformers - 1 | L 13 | Electrical Machines | GATE 2022"
lecture: 41
topic: "Transformers"
duration: "01:13:56"
source: "https://www.youtube.com/watch?v=03_-5LoPPrc"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 040: Three Phase Transformer 4](Lecture_040_Three_Phase_Transformer_4.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 042: Problems Based on Three Phase Transformers 2 →](Lecture_042_Problems_Based_on_Three_Phase_Transformers_2.md)

---

# Problems Based on Three Phase Transformers - 1 | L 13 | Electrical Machines | GATE 2022

- **Source**: https://www.youtube.com/watch?v=03_-5LoPPrc
- **Duration**: 01:13:56
- **Compiled**: 2026-09-21

---

## Overview

This lecture works through detailed numerical problems on three-phase transformer connections and banks. It explores polarity reversals, winding impedance transformations, and complex power balance across multi-winding systems. The problems show how to convert between line and phase quantities for star and delta banks. Students also learn how to calculate voltage regulation and determine clock group phase displacements.

## Problem Solving Strategy

Three-phase transformer problems are solved by decoupling the bank into per-phase equivalent circuits. Voltage and current ratios apply strictly across phase windings.
1. Label all winding terminals using standard dot conventions.
2. Resolve three-phase line quantities into phase quantities.
3. Apply single-phase equivalent relations across corresponding winding phases.
4. Convert calculated phase values back to line quantities.

---

## Q1. Secondary Delta Polarity Reversal

**Problem**: A normal two-winding three-phase delta-delta transformer has secondary voltages $V_{ab}, V_{bc}, V_{ca}$ of magnitude $E$. If terminals $X_1$ and $X_2$ of transformer 2 (phase bc) are accidentally interchanged, determine the net voltage inside the closed secondary delta loop.

**Solution**:
In a normal balanced delta, the sum of phase voltages is zero: $V_{ab} + V_{bc} + V_{ca} = 0$.
Interchanging the terminals of phase bc reverses its voltage phasor: $V_{bc}' = -V_{bc}$.
The net voltage becomes the sum: $V_{ab} - V_{bc} + V_{ca}$.

Using component method (with $-V_{bc}$ on the positive x-axis):
- **Horizontal**: $E\cos(0^\circ) + E\cos(60^\circ) + E\cos(60^\circ) = E + 0.5E + 0.5E = 2E$.
- **Vertical**: $E\sin(60^\circ) - E\sin(60^\circ) = 0$.

Resultant voltage $= 2E$. This massive voltage drives huge circulating currents, burning the transformer.

---

## Q2. Transformer Supplying an Induction Motor

**Problem**: A $30\text{ kW}$ induction motor operates at an efficiency of $90\%$ and a lagging power factor of $0.833$. It is fed by a three-phase $11\text{ kV} / 400\text{ V}$ delta-star transformer. Determine the phase current on the high-voltage delta side.

**Solution**:
1. Find electrical input power: $P_{\text{in}} = P_{\text{out}} / \eta = 30\text{ kW} / 0.90 = 33.33\text{ kW}$.
2. Find total apparent power: $S = P_{\text{in}} / \cos\phi = 33.33\text{ kW} / 0.833 = 40\text{ kVA}$.
3. For the HV (delta) side, phase voltage = line voltage = $11\text{ kV}$.
4. Find phase current: $S = 3 V_{ph(HV)} I_{ph(HV)} \implies I_{ph(HV)} = 40\text{ kVA} / (3 \times 11\text{ kV}) = 1.212\text{ A}$.

---

## Q3. Core Area and Turns Calculation

**Problem**: An $11,000 / 440\text{ V}$ delta-star transformer has $12\text{ V/turn}$ and $B_m = 1.2\text{ Wb/m}^2$ at $50\text{ Hz}$. Find core area and turns.

**Solution**:
1. **Core Area**: $V/\text{turn} = 4.44 f B_m A_i \implies A_i = 12 / (4.44 \times 50 \times 1.2) = 0.045\text{ m}^2 = 450\text{ cm}^2$.
2. **LV Turns (Star)**: $V_{ph(LV)} = 440 / \sqrt{3} \approx 254\text{ V}$. $N_L = 254 / 12 = 21.17 \approx 22$ turns.
3. **HV Turns (Delta)**: $V_{ph(HV)} = 11,000\text{ V}$. $N_H = N_L \times (V_{ph(HV)} / V_{ph(LV)}) = 22 \times (11,000 / (440/\sqrt{3})) \approx 952$ turns.

---

## Q4. Three Single-Phase Units Interconnected

**Problem**: Three single-phase transformers with unity turns ratio ($N_1/N_2 = 1$) are connected. Primary is delta-connected to line voltage $V$. Secondary windings are connected as shown (see video/diagrams). Find $V_{A2C2}$.

**Solution**:
Primary is delta, so phase voltage = $V$.
Phase voltages are $V \angle 0^\circ, V \angle -120^\circ, V \angle 120^\circ$.
Secondary induced voltages equal primary since $N_1/N_2 = 1$.
Applying KVL across the specific secondary interconnection:
$V_{A2C2} = V_{A2} - V_{C2} = V \angle -120^\circ + V \angle 120^\circ - V \angle 0^\circ = -2V$.
Magnitude = $2V$.

---

## Q5. Per-Unit to Ohmic Impedance on Delta Side

**Problem**: A $500\text{ kVA}$, $11 / 0.43\text{ kV}$ delta-star transformer has copper losses of $2.5\text{ kW}$ (HV) and $2.0\text{ kW}$ (LV). Leakage reactance is $0.06\text{ p.u.}$ Find equivalent ohmic resistance and reactance referred to the delta side.

**Solution**:
1. Total copper loss $= 4.5\text{ kW}$.
2. Per-unit resistance $R_{pu} = P_{cu(fl)} / S_{base} = 4.5\text{ kW} / 500\text{ kVA} = 0.009\text{ p.u.}$
3. Delta side (HV) base impedance: $Z_{base(HV)} = 3(V_{L(HV)})^2 / S_{3\phi} = 3(11\text{ kV})^2 / 500\text{ kVA} = 726\Omega$.
4. Ohmic values: $R = 0.009 \times 726 = 6.534\Omega$, $X = 0.06 \times 726 = 43.56\Omega$.

---

## Q6. Complex Power in Three-Winding Transformer

**Problem**: A $200\text{ kVA}$, $33\text{ kV} / 11\text{ kV} / 400\text{ V}$ transformer supplies $150\text{ kVA}$ at $0.8$ pf lag (secondary) and $50\text{ kVA}$ at $0.9$ pf lag (tertiary). Magnetizing current is $4\%$ of rated, iron loss is $1\text{ kW}$. Find total primary current.

**Solution**:
Use complex power: $S_{\text{source}} = S_{\text{sec}} + S_{\text{tert}} + S_{\text{mag}} + P_{\text{iron}}$.
- $S_{\text{sec}} = 150 \angle 36.87^\circ = 120 + j90\text{ kVA}$.
- $S_{\text{tert}} = 50 \angle 25.84^\circ = 45 + j21.79\text{ kVA}$.
- $S_{\text{mag}} = +j(0.04 \times 200) = +j8\text{ kVA}$.
- $P_{\text{iron}} = 1\text{ kW}$.
Total $S_{\text{source}} = (120+45+1) + j(90+21.79+8) = 166 + j119.79 = 204.71\text{ kVA} \angle 35.8^\circ$.
Primary Line Current $I_{L} = S / (\sqrt{3} V_L) = 204.71\text{ kVA} / (\sqrt{3} \times 33\text{ kV}) = 3.581\text{ A}$.

---

## Summary and Key Takeaways

- Reversing one phase winding in a delta secondary creates a net circulating voltage of $2 E$ across the open corner, where $E$ is the phase voltage magnitude.
- In three-phase induction motor problems, input active power equals shaft mechanical power divided by efficiency: $P_{\text{in}} = P_{\text{out}} / \eta$.
- Core cross-sectional area relates directly to the induced EMF per turn through the relation $A_i = (E_{ph} / N_{ph}) / (4.44 f B_m)$.
- Per-unit series resistance of a transformer equals total full-load copper loss divided by the base apparent power: $R_{pu} = P_{cu,fl} / S_{\text{base}}$.
- Three-winding transformer analysis simplifies by applying complex power balance, where the source delivers $\vec{S}_{\text{source}} = \vec{S}_{\text{sec}} + \vec{S}_{\text{tert}} + \vec{S}_{\text{loss}}$.
- Maximum voltage regulation for any power factor occurs when the load impedance angle equals the transformer impedance angle, giving $\text{VR}_{\max} = Z_{pu}$.
- Nameplate voltage ratings for three-phase banks always specify line-to-line voltages, requiring a factor of $\sqrt{3}$ conversion for star-connected windings.

---

[← Lec 040: Three Phase Transformer 4](Lecture_040_Three_Phase_Transformer_4.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 042: Problems Based on Three Phase Transformers 2 →](Lecture_042_Problems_Based_on_Three_Phase_Transformers_2.md)
