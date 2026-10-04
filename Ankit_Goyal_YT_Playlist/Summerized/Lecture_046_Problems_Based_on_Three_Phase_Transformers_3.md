---
title: "Problems Based on Three Phase Transformers - 3 | L 15 | Electrical Machines | GATE 2022"
lecture: 46
topic: "Transformers"
duration: "01:06:24"
source: "https://www.youtube.com/watch?v=OCxomfN3YHE"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 045: Three Phase Transformer 7](Lecture_045_Three_Phase_Transformer_7.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 047: Parallel Operation of Transformers →](Lecture_047_Parallel_Operation_of_Transformers.md)

---

# Problems Based on Three Phase Transformers - 3 | L 15 | Electrical Machines | GATE 2022

- **Source**: https://www.youtube.com/watch?v=OCxomfN3YHE
- **Duration**: 01:06:24
- **Compiled**: 2026-09-21

---

## Overview

This lecture solves advanced problems on open-delta and Scott transformer configurations. The discussion begins with load sharing, power factor variation, and rating requirements in open-delta banks. It then analyzes the thermal derating, loss escalation, and efficiency drop when a delta-delta bank transitions to open-delta. The second half examines current transformations, neutral tapping locations, and primary line current unbalance in Scott connections supplying two-phase furnace loads.

## Contents

- [[#Problem 1: Open-Delta Rating and Line Currents|Problem 1: Open-Delta Rating and Line Currents]]
- [[#Problem 2: Efficiency and Loss Impact in V-V|Problem 2: Efficiency and Loss Impact in V-V]]
- [[#Problem 3: Capacity Derating and Overloading in V-V|Problem 3: Capacity Derating and Overloading in V-V]]
- [[#Problem 4: Current Distribution under Delta-Delta, Star-Delta, and V-V|Problem 4: Current Distribution under Delta-Delta, Star-Delta, and V-V]]
- [[#Problem 5: Scott Connection Neutral Tap Location|Problem 5: Scott Connection Neutral Tap Location]]
- [[#Problem 6: Scott Connection with Balanced and Unbalanced Furnace Loads|Problem 6: Scott Connection with Balanced and Unbalanced Furnace Loads]]
- [[#Problem 7: Primary Currents with Unequal Furnace Loads|Problem 7: Primary Currents with Unequal Furnace Loads]]

---

## Problem 1: Open-Delta Rating and Line Currents
_(05:22 - 20:08)_

> [!example] Problem 1
> Four 25 kW, three-phase, 400 V induction motors are supplied by transformers connected in open delta from an 11 kV line. At full load, each motor has an efficiency of 95% and operates at 0.866 lagging power factor.
> Determine the kVA rating of each of the two transformers, their turns ratio, the line currents, and operating power factors.

- **Load**: $P_{in} = \frac{4 \times 25}{0.95} = 105.263\text{ kW}$.
- **Apparent Power**: $S_{in} = \frac{105.263}{0.866} = 121.55\text{ kVA}$.
- **Unit Rating**: $S_{\text{1-ph}} = \frac{S_{in}}{\sqrt{3}} = 70.18\text{ kVA}$.
- **Turns Ratio**: $a = \frac{11000}{400} = 27.5$.
- **Line Currents**: $I_{HV} = \frac{121.55 \times 10^3}{\sqrt{3} \times 11000} = 6.38\text{ A}$, $I_{LV} = \frac{121.55 \times 10^3}{\sqrt{3} \times 400} = 175.44\text{ A}$.
- **Power Factors**:
  - $\phi = 30^\circ$ (for $0.866$ lag).
  - $T_1$: $\cos(30^\circ + 30^\circ) = 0.5$ lag.
  - $T_2$: $\cos(30^\circ - 30^\circ) = 1.0$ (UPF).
- **Real Power Sharing**: $P_1 = 70.177 \times 0.5 = 35.088\text{ kW}$, $P_2 = 70.177 \times 1.0 = 70.177\text{ kW}$.

## Problem 2: Efficiency and Loss Impact in V-V
_(20:08 - 29:36)_

> [!example] Problem 2
> Three identical single-phase transformers in delta-delta supply a balanced three-phase load. One is removed. Total load kVA remains unchanged. Core loss is 0.01 pu, ohmic loss is 0.02 pu at rated load. Determine the increase in losses, decrease in efficiency, and derating for the same temperature rise.

- **Initial $\Delta\text{-}\Delta$**: $S_{\text{load}} = 3\text{ pu}$. Losses $= 3(0.01 + 0.02) = 0.09\text{ pu}$. $\eta = \frac{3}{3.09} = 97.087\%$.
- **V-V (Same Load)**: Phase current becomes $\sqrt{3} I_{ph}$. Copper loss per unit becomes $3 \times 0.02 = 0.06\text{ pu}$.
  - Total losses $= 2(0.01) + 2(0.06) = 0.14\text{ pu}$.
  - Increase in losses $= \frac{0.14 - 0.09}{0.09} = 55.55\%$.
  - New efficiency $= \frac{3}{3.14} = 95.54\%$. Decrease $= 1.54\%$.
- **Derating (Same Temp Rise)**: Current must remain $I_{ph}$. Output $S_{VV} = \sqrt{3} V_{ph} I_{ph} = \frac{1}{\sqrt{3}} S_{\Delta\Delta} \approx 0.577 S_{\Delta\Delta}$. Capacity reduction $= 42.3\%$.

## Problem 3: Capacity Derating and Overloading in V-V
_(29:41 - 34:59)_

> [!example] Problem 3
> A 400 kVA load at 0.7 lag is supplied by three 200 kVA single-phase transformers in delta-delta. One is removed.
> Calculate load carried by each, percentage overloading, safe rating, rating ratio, and percentage increase in load.

- **Load per transformer**: $\frac{400}{\sqrt{3}} = 230.94\text{ kVA}$.
- **Overloading**: $\frac{230.94}{200} = 115.47\%$ ($15.47\%$ overloaded).
- **Safe V-V Rating**: $\sqrt{3} \times 200 = 346.41\text{ kVA}$.
- **Rating Ratio**: $\frac{346.41}{600} = 0.577$.
- **Increase in Load**: Originally carried $\frac{400}{3} = 133.33\text{ kVA}$. New load is $230.94\text{ kVA}$. Increase $= \frac{230.94 - 133.33}{133.33} = 73.2\%$.

## Problem 4: Current Distribution under Delta-Delta, Star-Delta, and V-V
_(34:59 - 46:07)_

> [!example] Problem 4
> A lighting load of $I$ is supplied. Determine current distributions for (1) $\Delta\text{-}\Delta$, (2) $Y\text{-}\Delta$, (3) $V\text{-}V$.

1. **$\Delta\text{-}\Delta$**: Secondary $I_{L2} = \sqrt{3} I$. Primary phase $I_{ph1} = \frac{I}{a}$. Primary line $I_{L1} = \frac{\sqrt{3} I}{a}$.
2. **$Y\text{-}\Delta$**: Secondary $I_{ph2} = I$. Primary phase $I_{ph1} = \frac{I}{a}$. Primary line $I_{L1} = \frac{I}{a}$.
3. **$V\text{-}V$**: Line current equals phase current ($I_{L2} = I_{ph2} = I$). Primary line current $I_{L1} = \frac{I}{a}$.

## Problem 5: Scott Connection Neutral Tap Location
_(46:13 - 51:07)_

> [!example] Problem 5
> A Scott-connected transformer is fed from a 6600 V two-phase network and supplies a 500 V three-phase four-wire system. Two-phase side has 500 turns. Find primary turns ($N_1$) and neutral tap position.

- **Main Turns ($N_1$)**: $N_1 = 500 \times \frac{500}{6600} = 37.88 \approx 38\text{ turns}$.
- **Neutral Tap**: Located on the teaser primary at one-third of the teaser turns from the base junction D.
  - $N_{ND} = \frac{1}{3} (0.866 N_1) \approx 0.288 N_1$.
  - $N_{AN} = \frac{2}{3} (0.866 N_1) \approx 0.577 N_1$.

## Problem 6: Scott Connection with Balanced and Unbalanced Furnace Loads
_(51:12 - 56:03)_

> [!example] Problem 6
> Two 200 kW single-phase furnaces at 100 V are supplied via a Scott connection from an 11,000 V three-phase line. Leading phase (teaser) operates at UPF. Lagging phase (main) operates at 0.8 lag. Find primary line currents.

- **Turns Ratio**: $\frac{N_1}{N_2} = \frac{11000}{100} = 110$.
- **Secondary Currents**:
  - Teaser: $I_a = \frac{200,000}{100 \times 1.0} = 2000 \angle 90^\circ\text{ A}$.
  - Main: $I_b = \frac{200,000}{100 \times 0.8} = 2500 \angle -36.87^\circ\text{ A}$.
- **Reflected Primary Currents**:
  - $I_A = \frac{2000 \angle 90^\circ}{0.866 \times 110} = 21.0 \angle 90^\circ\text{ A}$.
  - $I_{BC} = \frac{2500 \angle -36.87^\circ}{110} = 22.73 \angle -36.87^\circ\text{ A}$.
- **Line Currents**:
  - $I_B = I_{BC} - \frac{I_A}{2} = (18.18 - j13.64) - j10.5 = 18.18 - j24.14 = 30.22 \angle -53.8^\circ\text{ A}$.
  - $I_C = -I_{BC} - \frac{I_A}{2} = -18.18 + j3.14 = 18.45 \angle 170.22^\circ\text{ A}$.

## Problem 7: Primary Currents with Unequal Furnace Loads
_(56:03 - 66:17)_

> [!example] Problem 7
> Two furnaces at 110 V take 500 kW and 800 kW respectively, both at 0.71 lagging pf. The supply is 6600 V three-phase. Find primary line currents.

- **Turns Ratio**: $\frac{N_1}{N_2} = \frac{6600}{110} = 60$. Power factor angle $\phi = \cos^{-1}(0.71) \approx 45^\circ$.
- **Secondary Currents**:
  - Teaser (500 kW): $I_a = \frac{500,000}{110 \times 0.71} = 6402\text{ A}$. Phase $= 90^\circ - 45^\circ = 45^\circ$.
  - Main (800 kW): $I_b = \frac{800,000}{110 \times 0.71} = 10243.2\text{ A}$. Phase $= 0^\circ - 45^\circ = -45^\circ$.
- **Reflected Primary Currents**:
  - $I_A = \frac{6402 \angle 45^\circ}{60 \times 0.866} = 123.21 \angle 45^\circ\text{ A}$.
  - $I_{BC} = \frac{10243.2 \angle -45^\circ}{60} = 170.72 \angle -45^\circ\text{ A}$.
- **Line Currents $I_B, I_C$**:
  - $I_A/2 = 61.61 \angle 45^\circ = 43.56 + j43.56\text{ A}$.
  - $I_{BC} = 170.72 \angle -45^\circ = 120.72 - j120.72\text{ A}$.
  - $I_B = I_{BC} - I_A/2 = 77.16 - j164.28 = 181.50 \angle -64.84^\circ\text{ A}$.
  - $I_C = -I_{BC} - I_A/2 = -164.28 + j77.16 = 181.50 \angle 154.84^\circ\text{ A}$.
- **Conclusion**: Unequal loads on the two-phase side cause unbalanced line currents ($I_A \neq I_B = I_C$) on the primary three-phase side.

---

## Summary and Key Takeaways

- An open-delta bank delivers a maximum apparent power of $S_{VV} = \sqrt{3} V_{ph} I_{ph}$, which is $57.7\%$ of a full delta-delta bank rating.
- The two transformers in an open-delta bank operate at unequal power factors given by $\cos(30^\circ + \phi)$ and $\cos(30^\circ - \phi)$.
- Supplying the original three-phase load after removing one transformer increases phase currents by $\sqrt{3}$ and increases total losses by $55.55\%$.
- Operating an open-delta bank at the same temperature rise as a delta-delta bank requires derating the load capacity by $42.3\%$.
- In open-delta banks, the line currents and phase currents are identical because no closed delta loop exists.
- In a Scott connection, the teaser transformer requires $0.866 N_1$ primary turns when the main transformer has $N_1$ turns.
- The primary neutral tap on a Scott connection is located at one-third of the teaser winding turns ($0.288 N_1$) from the junction point.
- Unequal single-phase loads or differing load power factors on the two-phase side cause unbalanced line currents on the primary three-phase side.

---

[← Lec 045: Three Phase Transformer 7](Lecture_045_Three_Phase_Transformer_7.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 047: Parallel Operation of Transformers →](Lecture_047_Parallel_Operation_of_Transformers.md)
