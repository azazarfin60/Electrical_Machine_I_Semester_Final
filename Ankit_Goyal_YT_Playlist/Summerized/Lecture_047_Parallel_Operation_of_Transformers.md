---
title: "Parallel Operation of Transformers | Electrical Machines | Lec 32 | GATE/ESE (EE, ECE) | Ankit Goyal"
lecture: 47
topic: "Transformers"
duration: "01:20:36"
source: "https://www.youtube.com/watch?v=oqgDQt9G2fo"
compiled: "2026-09-21"
tags:
  - electrical-machines
  - gate
---

[← Lec 046: Problems Based on Three Phase Transformers 3](Lecture_046_Problems_Based_on_Three_Phase_Transformers_3.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 048: Problems based on Parallel Operation of Transformer →](Lecture_048_Problems_based_on_Parallel_Operation_of_Transformer.md)

---

# Parallel Operation of Transformers | Electrical Machines | Lec 32 | GATE/ESE (EE, ECE) | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=oqgDQt9G2fo
- **Duration**: 01:20:36
- **Compiled**: 2026-09-21

---

## Overview

This lecture establishes the theory and practice of operating transformers in parallel. It presents the technical and economic reasons for parallel operation, including increased current capacity, higher reliability, and reduced standby unit costs. The lecture derives both necessary conditions to prevent circulating currents and desirable conditions to optimize load sharing. It develops analytical methods to compute branch currents, apparent power distribution, and the maximum permissible load without overloading either unit.

## Contents

- [[#Motivation for Parallel Operation|Motivation for Parallel Operation]]
- [[#Necessary Conditions for Parallel Operation|Necessary Conditions for Parallel Operation]]
- [[#Desirable Conditions for Parallel Operation|Desirable Conditions for Parallel Operation]]
- [[#Current and Power Sharing Principles|Current and Power Sharing Principles]]
- [[#Base Conversion and Maximum Loading Strategy|Base Conversion and Maximum Loading Strategy]]

---

## Motivation for Parallel Operation
_(00:12 - 10:51)_

Transformers are operated in parallel to:
1. **Increase Capacity**: Total capacity equals the sum of individual capacities ($S_{\text{total}} = V I_{\text{total}}^*$).
2. **Improve Reliability**: If one unit fails, the others continue supplying load, preventing total blackout.
3. **Optimize Efficiency (Demand Switching)**: Transformers can be switched on or off to match load variations, saving core losses during light load periods.
4. **Reduce Standby Cost**: A system of four 25 MVA units only needs one 25 MVA spare, whereas a 100 MVA unit needs a 100 MVA spare.
5. **Improve Voltage Regulation**: Parallel impedance is lower ($Z_{\text{eq}} = Z_1 \parallel Z_2$), reducing internal voltage drops.

## Necessary Conditions for Parallel Operation
_(10:54 - 23:40)_

Failing to meet these conditions creates destructive circulating currents or short circuits:

1. **Equal Voltage Ratios ($a_1 = a_2$)**: Unequal secondary voltages drive a continuous circulating current $I_c = \frac{V_1/a_1 - V_1/a_2}{Z_1 + Z_2}$ in the local loop, which overloads one unit and increases total $I^2R$ copper loss.
2. **Identical Polarity**: Connecting dotted to undotted terminals adds the secondary voltages (loop voltage $= 2V_1/a$), causing an immediate and catastrophic short-circuit current.
3. **Same Phase Sequence (3-Phase Only)**: Both must be $RYB$ or $RBY$.
4. **Same Phasor Group (3-Phase Only)**: Zero phase shift between their secondary voltages. For example, a $Y\text{-}y$ ($0^\circ$) cannot operate in parallel with a $Y\text{-}d$ ($30^\circ$).

## Desirable Conditions for Parallel Operation
_(23:41 - 28:28)_

Failing to meet these won't prevent operation, but reduces optimal utilization:

1. **Proportional Load Sharing**: $\frac{S_1}{S_2} = \frac{S_{1, \text{rated}}}{S_{2, \text{rated}}}$.
   - Condition: Per-unit impedances on their *own respective bases* must be equal ($Z_{1, pu} = Z_{2, pu}$).
2. **Identical X/R Ratios**: Both should have the same phase angle $\theta = \tan^{-1}(X/R)$.
   - Consequence: Both operate at the load power factor. Apparent powers add algebraically ($S_{\text{total}} = |S_1| + |S_2|$), maximizing total usable capacity.

## Current and Power Sharing Principles
_(28:31 - 49:59)_

Using nodal analysis, branch currents can be resolved into two components:
1. **Load Current Division**: $I_{1, \text{load}} = I_L \left(\frac{Z_2}{Z_1 + Z_2}\right)$.
2. **Circulating Current**: $I_c = \frac{V_1/a_1 - V_1/a_2}{Z_1 + Z_2}$.

When voltage ratios are equal ($I_c = 0$), load sharing relies entirely on current division. In terms of complex power ($S_1 = V_L I_1^*$):
$$
S_1 = S_L \left(\frac{Z_2}{Z_1 + Z_2}\right)^* \quad \text{and} \quad S_2 = S_L \left(\frac{Z_1}{Z_1 + Z_2}\right)^*
$$
*Note the conjugate on the impedance division factor.*

**Sign Convention**:
- Lagging Load: $S_L = P + jQ$ (positive angle).
- Leading Load: $S_L = P - jQ$ (negative angle).

The apparent power magnitude ratio is inversely proportional to ohmic impedance magnitudes:
$$ \left|\frac{S_1}{S_2}\right| = \left|\frac{Z_2}{Z_1}\right| $$

## Base Conversion and Maximum Loading Strategy
_(50:01 - 01:20:28)_

**Per-Unit Base Conversion**:
To calculate actual load sharing, per-unit impedances must be referred to a common base kVA:
$$Z_{\text{pu, new}} = Z_{\text{pu, old}} \left(\frac{S_{\text{new}}}{S_{\text{old}}}\right)$$

**Determining Maximum Permissible Load**:
To find the maximum load a parallel bank can supply without overloading any unit:
1. **Identify the Limiting Unit**: Compare $Z_{\text{pu}}$ of both transformers on their *own rating base*. The unit with the smaller $Z_{\text{pu}}$ takes more relative load and will overload first.
2. **Fix Output**: Set the limiting unit to its full rated capacity ($S_2 = S_{2, \text{rated}} \angle 0^\circ$).
3. **Compute Other Output**: Calculate the other unit's load using $S_1 = S_2 \left(\frac{Z_2}{Z_1}\right)^*$.
4. **Vector Sum**: Add $S_1$ and $S_2$ using phasor addition (law of cosines) to find total maximum capacity.

---

## Summary and Key Takeaways

- Parallel connection of transformers increases total current and power capacity while reducing equivalent series impedance and improving voltage regulation.
- Equal voltage ratios and identical polarities are necessary conditions for single-phase parallel operation to prevent circulating currents.
- Three-phase parallel operation additionally requires identical phase sequence and matching phasor groups to avoid phase angle differences across secondary windings.
- Circulating current between parallel transformers is given by $I_c = (V_1/a_1 - V_1/a_2)/(Z_1 + Z_2)$, which overloads one unit and increases total copper loss.
- When voltage ratios are equal, complex power divides according to $S_1 = S_L [Z_2 / (Z_1 + Z_2)]^*$ and $S_2 = S_L [Z_1 / (Z_1 + Z_2)]^*$.
- Load sharing is strictly proportional to rated kVA if and only if per-unit impedances on each transformer's own rating base are equal: $Z_{1,pu} = Z_{2,pu}$.
- Identical $X/R$ ratios ensure both transformers operate at the load power factor, allowing their apparent powers to add algebraically to maximize total capacity.
- The maximum load without overloading either unit is determined by setting the transformer with lower per-unit impedance on its own base to rated capacity and calculating total power by phasor sum.

---

[← Lec 046: Problems Based on Three Phase Transformers 3](Lecture_046_Problems_Based_on_Three_Phase_Transformers_3.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 048: Problems based on Parallel Operation of Transformer →](Lecture_048_Problems_based_on_Parallel_Operation_of_Transformer.md)
