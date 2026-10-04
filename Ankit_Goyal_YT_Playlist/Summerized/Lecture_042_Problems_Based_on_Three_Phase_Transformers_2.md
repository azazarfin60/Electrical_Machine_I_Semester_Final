---
title: "Problems Based on Three Phase Transformers - 2 | L 14 | Electrical Machines | GATE 2022"
lecture: 42
topic: "Transformers"
duration: "01:10:48"
source: "https://www.youtube.com/watch?v=TvN4nAehGLg"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 041: Problems Based on Three Phase Transformers 1](Lecture_041_Problems_Based_on_Three_Phase_Transformers_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 043: Three Phase Transformer 5 →](Lecture_043_Three_Phase_Transformer_5.md)

---

# Problems Based on Three Phase Transformers - 2 | L 14 | Electrical Machines | GATE 2022

- **Source**: https://www.youtube.com/watch?v=TvN4nAehGLg
- **Duration**: 01:10:48
- **Compiled**: 2026-09-21

---

## Overview

This lecture presents comprehensive numerical problems on three-phase transformer connections and phasor relationships. It focuses on clock group identification, line-to-phase transformations, and negative sequence effects. The problems show how to calculate copper losses and efficiency across distinct winding configurations. Students also learn how to determine allowable voltage and power ratings when reconnecting three-phase windings as a single-phase transformer.

## Problem Solving Strategy

Three-phase transformer problems often look complicated at first glance, but systematic steps make them straightforward to solve:
1. Identify the connection type on both primary and secondary sides.
2. Draw the phase and line voltage phasors.
3. Apply turns ratios strictly to phase quantities.
4. Remember that primary and secondary phase voltages on corresponding limbs always lie in the exact same phase.

---

## Q1. Yd1 Clock Group Identification

**Problem**: Identify the standard clock group notation for a Star-Delta transformer where secondary terminal $b_2$ connects to $a_1$, and terminal $c_2$ connects to $b_1$.

**Solution**:
The external terminals brought out to the load are $a_2$, $b_2$, and $c_2$. The primary line phasor A ($A_1 \to A_2$) points vertically upwards to 12 o'clock. The secondary line voltage phasor ($a_1 \to a_2$) points towards the 1 o'clock mark on a standard clock face.
$V_{ab}$ lags $V_{AB}$ by $30^\circ$.
This connection represents the **Yd1** clock group.

---

## Q2. Closed-Loop Three-Phase Bank Voltage

**Problem**: Three single-phase transformers whose windings form an interconnected loop are excited by balanced voltages $V_A = V \angle 0^\circ, V_B = V \angle -120^\circ, V_C = V \angle 120^\circ$. Find the loop voltage $V$. (The loop contains fractional windings like $\frac{2}{3}V_A, -\frac{V_B}{3}$, etc.)

**Solution**:
Start at one node and traverse the loop using KVL, applying standard three-phase relationships.
$V_{loop} = V \angle 180^\circ = -V$.

---

## Q3. Phase Displacement Matching

**Problem**: Match the connection with its corresponding phase shift:
1. Normal Star - Normal Delta
2. Normal Star - Reverse Star
3. Normal Star - Reverse Delta
4. Normal Star - Normal Star

**Solution**:
- Normal Star - Normal Delta $\implies +30^\circ$ (Yd11) or $-30^\circ$ (Yd1).
- Normal Star - Reverse Star reverses winding polarity $\implies 180^\circ$.
- Normal Star - Reverse Delta reverses delta phase sequence $\implies -30^\circ$ (Yd1).
- Normal Star - Normal Star produces zero displacement $\implies 0^\circ$.

---

## Q4. Delta-Star Phase Current Ratio

**Problem**: A $33\text{ kV} / 11\text{ kV}$ star-delta transformer supplies a $10\text{ MW}$ load at unity power factor. Find the ratio of phase current in the delta winding to phase current in the star winding ($I_{ph(\Delta)} / I_{ph(Y)}$).

**Solution**:
The phase current ratio is inversely proportional to the phase voltage ratio, regardless of the load:
$$\frac{I_{ph(\Delta)}}{I_{ph(Y)}} = \frac{V_{ph(Y)}}{V_{ph(\Delta)}}$$
Calculate the respective phase voltages from the given line ratings:
- Primary star phase voltage: $V_{ph(Y)} = \frac{33}{\sqrt{3}}\text{ kV}$
- Secondary delta phase voltage: $V_{ph(\Delta)} = 11\text{ kV}$
$$\frac{I_{ph(\Delta)}}{I_{ph(Y)}} = \frac{33 / \sqrt{3}}{11} = \frac{3}{\sqrt{3}} = \sqrt{3}$$

---

## Q5. Three-Phase Efficiency Calculation

**Problem**: A 3-phase, $900\text{ kVA}, 3\text{ kV} / \sqrt{3}\text{ kV}$ delta-star transformer has $R_{HV} = 0.3\,\Omega$, $R_{LV} = 0.02\,\Omega$, and core loss $P_i = 10\text{ kW}$. Find full-load efficiency at UPF.

**Solution**:
1. Find phase currents.
   - Primary Delta: $I_{ph(HV)} = (900/3) / 3 = 100\text{ A}$.
   - Secondary Star: $V_{ph(LV)} = \sqrt{3}/\sqrt{3} = 1\text{ kV}$. $I_{ph(LV)} = (900/3) / 1 = 300\text{ A}$.
2. Calculate total full-load copper loss.
   - $P_{cu,fl} = 3 I_{ph(HV)}^2 R_{HV} + 3 I_{ph(LV)}^2 R_{LV} = 3(100)^2(0.3) + 3(300)^2(0.02) = 14.4\text{ kW}$.
3. Calculate efficiency.
   - $\eta = \frac{900 \times 1.0}{900 \times 1.0 + 10 + 14.4} \times 100\% = 97.36\%$.

---

## Q6. Negative-Sequence Voltage Excitation

**Problem**: The star side of a Yd transformer is excited by a negative-sequence voltage set. Determine the relationship between primary line voltage $V_{AB}$ and secondary line voltage $V_{ab}$.

**Solution**:
Under negative sequence, phases B and C swap their angular positions (A-C-B).
If the transformer was Yd11 ($+30^\circ$ lead) under positive sequence, it becomes $-30^\circ$ lag under negative sequence.
Primary line voltage $V_{AB}$ lags secondary line voltage $V_{ab}$ by $30^\circ$.

---

## Q7. Impedance Transformation Rule

**Problem**: A star-delta transformer has line voltage ratings of $110\text{ V} / 220\text{ V}$. A balanced star load with $Z_Y = 4\,\Omega/\text{phase}$ connects across the delta secondary. Find the equivalent impedance referred to the primary side.

**Solution**:
**Rule**: Before referring an impedance across a three-phase transformer, the load impedance connection must match the winding connection of that side.
1. Convert the secondary star load to delta: $Z_\Delta = 3 \times Z_Y = 12\,\Omega/\text{phase}$.
2. Calculate phase turns ratio: $\frac{N_{ph(Y)}}{N_{ph(\Delta)}} = \frac{110 / \sqrt{3}}{220} = \frac{1}{2\sqrt{3}}$.
3. Refer the impedance: $Z'_{\text{referred}} = 12 \times \left(\frac{1}{2\sqrt{3}}\right)^2 = 12 \times \frac{1}{12} = 1\,\Omega/\text{phase}$.

---

## Q8. Three-Phase to Single-Phase Reconnection

**Problem**: The windings of a $Q\text{ kVA}, V_1 / V_2\text{ V}$, 3-phase delta-connected core-type transformer are reconnected to operate as a single-phase transformer. Determine the maximum voltage and power rating of the new configuration.

**Solution**:
Two physical constraints govern the ratings:
1. Voltage rating per phase depends on dielectric insulation ($V_1$ or $V_2$).
2. Current rating per phase depends on conductor cross-sectional area ($I_1$ or $I_2$).
The original apparent power is $Q = 3 V_1 I_1 = 3 V_2 I_2$.

To maximize voltage and power without exceeding limits, connect two windings in parallel, and place that parallel pair in series with the third winding.
- Terminal voltage: $V_1 + V_1 = 2V_1$ (primary).
- Permissible line current: The series winding carries $I_1$. The parallel pair splits it ($I_1/2$). Current rating = $I_1$.
- Total apparent power: $S_{\text{hybrid}} = (2V_1) \times I_1 = 2 V_1 I_1 = \frac{2}{3}(3 V_1 I_1) = \frac{2}{3}Q$.

---

## Summary and Key Takeaways

- In balanced star-connected windings, the phase voltage lags the line voltage by $30^\circ$, giving $V_{ph} = (V_L / \sqrt{3}) \angle -30^\circ$.
- Primary and secondary phase voltages on corresponding limbs always remain in the exact same phase, with turns ratio $a = N_1 / N_2 = V_{ph1} / V_{ph2}$.
- In a closed loop formed by transformer secondary windings, the net circulating voltage equals the phasor sum of all induced phase voltages.
- The ratio of delta phase current to star phase current in a star-delta bank equals the inverse of the phase voltage ratio, $I_{ph(\Delta)} / I_{ph(Y)} = V_{ph(Y)} / V_{ph(\Delta)}$, independent of load magnitude.
- Exciting the star side of a star-delta transformer with negative-sequence voltages swaps phase sequence to $A-C-B$, causing $V_{AB}$ to lag $V_{ab}$ by $30^\circ$.
- Before referring an impedance across a three-phase transformer, the load impedance connection must match the winding connection of that side.
- Reconnecting a three-phase $Q\text{ kVA}, V_1 / V_2$ delta transformer with two windings in parallel and one in series yields a single-phase rating of $2V_1 / 2V_2$ and $\frac{2}{3}Q\text{ kVA}$.

---

[← Lec 041: Problems Based on Three Phase Transformers 1](Lecture_041_Problems_Based_on_Three_Phase_Transformers_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 043: Three Phase Transformer 5 →](Lecture_043_Three_Phase_Transformer_5.md)
