---
title: "Electrical Machines | Lec 26 | Three Phase Transformer - 2 | GATE/ESE Electrical Engineering Lecture"
lecture: 38
topic: "Transformers"
duration: "00:53:20"
source: "https://www.youtube.com/watch?v=5n-ERhNlN38"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 037: Three Phase Transformer 1](Lecture_037_Three_Phase_Transformer_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 039: Three Phase Transformer 3 →](Lecture_039_Three_Phase_Transformer_3.md)

---

# Electrical Machines | Lec 26 | Three Phase Transformer - 2 | GATE/ESE Electrical Engineering Lecture

- **Source**: https://www.youtube.com/watch?v=5n-ERhNlN38
- **Duration**: 00:53:20
- **Compiled**: 2026-09-21

---

## Overview

This lecture examines three-phase transformer connections and their classification into standard phasor groups. It introduces the clock face method to determine angular displacement between primary and secondary line voltages. The discussion develops systematic rules for terminal labeling and dot conventions across delta and star windings. Detailed phasor analysis demonstrates the construction of Dd0 and Dd6 configurations. Finally, the lecture compares star and delta windings regarding required turns and conductor cross-sectional area.

## Contents

- [[#Phase Displacement and Phasor Groups|Phase Displacement and Phasor Groups]]
- [[#The Clock Method and Naming Conventions|The Clock Method and Naming Conventions]]
- [[#Phasor Construction Rules|Phasor Construction Rules]]
- [[#Comparing Star and Delta Windings|Comparing Star and Delta Windings]]

---

## Phase Displacement and Phasor Groups
_(00:13 - 18:59)_

Three-phase transformers can shift the phase angle between primary and secondary line voltages. This shift is defined as the angle by which the Low Voltage (LV) side lags the High Voltage (HV) side.

Transformers are divided into four standard phasor groups:
1. **Phasor Group 1**: $0^\circ$ displacement.
2. **Phasor Group 2**: $180^\circ$ displacement.
3. **Phasor Group 3**: $-30^\circ$ displacement (LV lags HV by $30^\circ$).
4. **Phasor Group 4**: $+30^\circ$ displacement (LV leads HV by $30^\circ$, equivalent to $330^\circ$ lag).

![Alphanumeric naming convention and phasor group definitions on the whiteboard](frames/038/frame_0018_12m06s.jpg)

### Why Connections Matter
- **Grounding**: Star ($Y$) connections provide a neutral point for grounding. Delta ($\Delta$) does not.
- **Insulation**: Star connection is preferred for high voltage because phase voltage is $V_L/\sqrt{3}$, reducing insulation cost.
- **Harmonics**: Delta connections provide a closed loop for third-harmonic currents, preventing third-harmonic voltages on lines.
- **Reliability**: A Delta-Delta bank can operate in Open-Delta ($V-V$) if one phase fails, delivering $57.7\%$ capacity.
- **Parallel Operation**: Transformers operating in parallel MUST belong to the same phasor group to avoid circulating currents.

## The Clock Method and Naming Conventions
_(08:25 - 18:59)_

Connections are named using an alphanumeric code (e.g., Yd1, Dy11, Dd0).
- **1st Letter (Uppercase)**: HV winding connection (Y or D).
- **2nd Letter (Lowercase)**: LV winding connection (y or d).
- **Number**: The phase displacement expressed as hours on a clock face (each hour = $30^\circ$ lag).

**Clock Face Rule**:
- The **HV line voltage** is the minute hand, always fixed at 12 o'clock.
- The **LV line voltage** is the hour hand.
- If LV points to **12**, phase shift is $0^\circ$ (e.g., Dd0, Yy0).
- If LV points to **6**, phase shift is $180^\circ$ (e.g., Dd6, Yy6).
- If LV points to **1**, phase shift is $30^\circ$ lag (e.g., Yd1, Dy1).
- If LV points to **11**, phase shift is $330^\circ$ lag, which is $30^\circ$ lead (e.g., Yd11, Dy11).

![Whiteboard summary of clock positions and criteria for connection selection](frames/038/frame_0023_16m28s.jpg)

## Phasor Construction Rules
_(18:59 - 49:19)_

To determine the phasor group of a given connection diagram, follow these rules:

1. **Phase Voltage Transformation Invariance**: Across any single phase limb, the induced LV phase voltage is strictly in phase with the HV phase voltage. No phase shift occurs magnetically.
   $$\frac{V_{\text{ph, HV}}}{V_{\text{ph, LV}}} = \frac{N_{\text{HV}}}{N_{\text{LV}}}$$
2. **Terminal Polarity**: Terminals with identical numerical suffixes (e.g., $A_2$ and $a_2$) or dot markings share the exact same polarity at every instant.
3. **Phasor Orientation**: Under positive sequence (A-B-C), primary phasors form a triangle/star. The arrow of each phase voltage phasor must point toward the external terminal (e.g., $A_1 \rightarrow A_2$ if $A_2$ is the line terminal).
4. **Parallel Drawing**: When drawing the secondary phasor diagram, each secondary phase voltage must be drawn strictly parallel to its corresponding primary phase voltage.
5. **Determine Shift**: Draw reference vectors from the centroid of each diagram to terminal $A_2$ (primary) and $a_2$ (secondary). Compare their angles.

### Example: Dd0 Construction
If HV connects $A_1 \rightarrow B_2$, $B_1 \rightarrow C_2$, $C_1 \rightarrow A_2$ and LV connects $a_1 \rightarrow b_2$, $b_1 \rightarrow c_2$, $c_1 \rightarrow a_2$.
- The secondary triangle points exactly the same way as the primary.
- The reference vector points to 12 o'clock on both.
- **Result**: Dd0 ($0^\circ$ shift).

![Completed Dd0 phasor diagram showing aligned vertical reference phasors](frames/038/frame_0052_40m04s.jpg)

### Example: Dd6 Construction
If LV connections are reversed ($a_2 \rightarrow b_1$, etc.):
- The secondary phasors are still drawn parallel, but the physical connections form an inverted triangle.
- The reference vector points to 12 o'clock on primary, but 6 o'clock on secondary.
- **Result**: Dd6 ($180^\circ$ shift).

![Whiteboard drawing showing Dd6 inverted secondary triangle and 180-degree shift](frames/038/frame_0063_47m08s.jpg)

## Comparing Star and Delta Windings
_(49:19 - 53:20)_

For the same three-phase power rating:

- **Turns Requirement (for identical Line Voltage)**: 
  A delta winding sees the full line voltage, while a star winding sees $V_L/\sqrt{3}$.
  Therefore, a delta winding requires **$\sqrt{3}$ times (73.2% more) turns** than a star winding.
- **Conductor Thickness (for identical Line Current)**:
  A star winding carries the full line current, while a delta winding carries $I_L/\sqrt{3}$.
  Therefore, a delta winding requires **thinner wire**, needing only **$57.7\%$ ($1/\sqrt{3}$)** of the cross-sectional area of a star winding.

*(Summary: Delta = more turns of thinner wire. Star = fewer turns of thicker wire.)*

---

## Summary and Key Takeaways

- A three-phase transformer is a phase shifting transformer because an angular displacement exists between primary and secondary line voltages.
- Phase displacement is defined as the angle by which the low-voltage winding voltage lags the high-voltage winding voltage.
- Standard alphanumeric designations use uppercase letters for high voltage, lowercase letters for low voltage, and hour numbers for phase lag in multiples of $30^\circ$.
- On a 12-hour clock face, the high-voltage phasor is fixed at 12 as the minute hand, and the low-voltage phasor serves as the hour hand.
- Phase voltages across any individual phase limb are strictly in phase and related solely by the turns ratio ($\frac{V_{\text{ph, HV}}}{V_{\text{ph, LV}}} = \frac{N_{\text{HV}}}{N_{\text{LV}}}$).
- Connecting the finish of each winding to the start of the next phase produces a Dd0 connection with $0^\circ$ phase displacement.
- Reversing secondary connections inverts the secondary delta triangle, yielding a Dd6 connection with $180^\circ$ phase displacement.
- For identical line voltage, a delta winding requires $\sqrt{3}$ times ($73.2\%$) more turns per phase than a star winding.
- For identical line current, a delta conductor requires only $57.7\%$ ($1/\sqrt{3}$) of the cross-sectional area of a star conductor.

---

[← Lec 037: Three Phase Transformer 1](Lecture_037_Three_Phase_Transformer_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 039: Three Phase Transformer 3 →](Lecture_039_Three_Phase_Transformer_3.md)
