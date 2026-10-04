---
title: "Problems based on Voltage Regulation of Transformer | L 9 | Electrical Machines | GATE 2022"
lecture: 28
topic: "Transformers"
duration: "01:12:14"
source: "https://www.youtube.com/watch?v=6T2k7FLsffw"
compiled: "2026-09-20"
tags:
  - electrical-machines
  - gate
---

[← Lec 027: Voltage Regulation](Lecture_027_Voltage_Regulation.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 029: Important Concepts in Electrical Machines 1 →](Lecture_029_Important_Concepts_in_Electrical_Machines_1.md)

---

# Problems based on Voltage Regulation of Transformer | L 9 | Electrical Machines | GATE 2022

- **Source**: https://www.youtube.com/watch?v=6T2k7FLsffw
- **Duration**: 01:12:14
- **Compiled**: 2026-09-20

---

## Overview

This lecture works through comprehensive numerical problems on transformer voltage regulation, efficiency, and tap setting determination. It connects open-circuit and short-circuit test data to internal equivalent circuit parameters in both physical and per-unit systems. Through worked examples, the lecture demonstrates how tap-changing transformers compensate for internal leakage drops and transmission line impedance. It also analyzes fractional load effects and examines the condition required for zero voltage regulation.

## Contents

- [[#Problem 1: Efficiency and Regulation from PU Test Data|Problem 1: Efficiency and Regulation from PU Test Data]]
- [[#Problem 2 & 4: Tap Setting for Feeder Drop Compensation|Problem 2 & 4: Tap Setting for Feeder Drop Compensation]]
- [[#Problem 3 & 6: Primary Voltage from Regulation|Problem 3 & 6: Primary Voltage from Regulation]]
- [[#Problem 5: Zero Voltage Regulation Condition|Problem 5: Zero Voltage Regulation Condition]]
- [[#Problem 7: Comprehensive 3-Phase Parameter Extraction|Problem 7: Comprehensive 3-Phase Parameter Extraction]]
- [[#Conceptual Questions|Conceptual Questions]]

---

## Problem 1: Efficiency and Regulation from PU Test Data
_(00:07 - 11:05)_

> [!example] Problem 1
> Test 1: $V = 1.0\text{ pu}$, $I = 0.06\text{ pu}$, $\cos\phi = 0.2$
> Test 2: $V = 0.08\text{ pu}$, $I = 1.0\text{ pu}$, $\cos\phi = 0.3$
> Find full-load efficiency and voltage regulation at UPF and 0.8 lagging PF.

- **Test Identification**:
  - Test 1 has rated voltage ($V=1.0\text{ pu}$) and low current $\implies$ **Open-Circuit Test**. $P_i = 1.0 \times 0.06 \times 0.2 = 0.012\text{ pu}$.
  - Test 2 has rated current ($I=1.0\text{ pu}$) and low voltage $\implies$ **Short-Circuit Test**. $P_{cu,fl} = 0.08 \times 1.0 \times 0.3 = 0.024\text{ pu}$.
  - Equivalent impedance: $Z_{\text{pu}} = 0.08\text{ pu}$, $\cos\theta = 0.3 \implies \theta = 72.54^\circ$.
- **Efficiency Results ($x=1$)**:
  - UPF ($\cos\phi=1$): $\eta = \frac{1 \times 1}{1 + 0.012 + 0.024} = 96.525\%$
  - 0.8 Lagging ($\cos\phi=0.8$): $\eta = \frac{0.8}{0.8 + 0.012 + 0.024} = 95.693\%$
- **Voltage Regulation Results ($VR = x Z_{\text{pu}} \cos(\theta \mp \phi)$)**:
  - UPF ($\phi = 0^\circ$): $VR = 0.08 \times \cos(72.54^\circ) = 2.4\%$
  - 0.8 Lagging ($\phi = 36.87^\circ$): $VR = 0.08 \times \cos(72.54^\circ - 36.87^\circ) = 6.498\%$

![Digital whiteboard showing test data identification and per-unit loss formulas](frames/028/frame_0016_05m02s.jpg)

## Problem 2 & 4: Tap Setting for Feeder Drop Compensation
_(11:09 - 33:20)_

> [!example] Problem 2
> $11\text{ kV} / 433\text{ V}$, $\Delta\text{-Y}$ transformer. Load is $12\text{ kVA}$, $400\text{ V}$ at 0.8 lag.
> Feeder impedance: $0.6 + j1\,\Omega/\text{ph}$.
> $Z_{LV} = 0.3 + j1\,\Omega/\text{ph}$, $Z_{HV} = 400 + j1600\,\Omega/\text{ph}$.
> Find tap setting on primary to maintain $400\text{ V}$ at load.

- **Approach (Per-Phase Referral)**:
  - Turns ratio (phase voltages): $a = V_{1,ph}/V_{2,ph} = 11000 / (400/\sqrt{3}) = 47.63$.
  - Refer $Z_{HV}$ to LV: $Z_1' = Z_{HV} / a^2 = 0.2066 + j0.8264\,\Omega$.
  - Total impedance $Z_{\text{eq}} = Z_1' + Z_{LV} + Z_{\text{line}} = 1.1066 + j2.8264\,\Omega/\text{ph}$.
  - Load Current: $I_L = 12000 / (\sqrt{3} \times 400) = 17.32\text{ A}$, angle $-36.87^\circ$.
  - KVL on LV side: $\bar{V}_2 = V_{\text{load,ph}} + \bar{I}_L Z_{\text{eq}} \implies V_2 = 277.03\text{ V}$ (phase).
- **Result**: Line voltage required = $\sqrt{3} \times 277.03 = 479.82\text{ V}$.
  - Required boost: $\frac{479.82}{433} = 1.108\text{ pu} \implies \text{Tap Setting} = +10.8\%$.

*(Problem 4 uses the per-unit scalar drop formula $VR = x(R_{\text{pu}} \cos\phi + X_{\text{pu}} \sin\phi)$ to calculate the tap directly by setting $V_1 = V_{\text{load,pu}}(1 + VR)$).*

## Problem 3 & 6: Primary Voltage from Regulation
_(33:34 - 38:37, 49:46 - 54:41)_

> [!example] Problem 3
> $100\text{ kVA}$, $6600/330\text{ V}$. SC Test (HV): $100\text{ V}, 10\text{ A}, 436\text{ W}$. Find HV applied voltage for full load at 0.8 lag to maintain $330\text{ V}$ on LV.

- **Parameter Extraction**: $Z_{sc} = 100/10 = 10\,\Omega$, $R_{sc} = 436/10^2 = 4.36\,\Omega$, $X_{sc} = 9.0\,\Omega$.
- **Scalar Voltage Drop**: $\Delta V = I_{fl}(R \cos\phi + X \sin\phi) = 15.15(4.36(0.8) + 9.0(0.6)) = 134.66\text{ V}$.
- **Result**: $V_1 = V_2' + \Delta V = 6600 + 134.66 = 6734.66\text{ V}$.

*(Problem 6 applies this principle using given percentage VR for a distribution transformer).*

## Problem 5: Zero Voltage Regulation Condition
_(43:14 - 49:46)_

> [!example] Problem 5
> $R_{\text{eq}} = 0.5\,\Omega$, $X_{\text{eq}} = 0.8\,\Omega$. Find load PF for zero VR.

- **Condition**: $VR = 0 \implies R \cos\phi - X \sin\phi = 0 \implies \tan\phi = R/X$.
- **Calculation**: $\tan\phi = 0.5 / 0.8 \implies \cos\phi = \frac{X}{Z} = \frac{0.8}{\sqrt{0.5^2 + 0.8^2}} = 0.848$ (leading).
- **Result**: Zero VR always requires a **leading** power factor to provide a capacitive voltage rise cancelling the resistive drop.

## Problem 7: Comprehensive 3-Phase Parameter Extraction
_(54:41 - 66:23)_

> [!example] Problem 7
> $50\text{ kVA}$, $6.6/0.4\text{ kV}$.
> OC (LV): $400\text{ V}, 4.21\text{ A}, 520\text{ W}$
> SC (HV): $340\text{ V}, 4.35\text{ A}, 610\text{ W}$
> Find PU parameters, full load VR (0.8 lag), and max efficiency load.

- **Base Values**: $S_{\text{base}} = 50\text{ kVA}$, $V_{\text{base,LV}} = 400\text{ V}$, $V_{\text{base,HV}} = 6600\text{ V}$.
- **PU Conversion**:
  - $I_{\text{base,LV}} = 72.17\text{ A}$, $I_{\text{base,HV}} = 4.37\text{ A}$.
  - OC Test (PU): $V = 1.0$, $I = 0.0583$, $P = 0.0104$.
  - SC Test (PU): $V = 0.0515$, $I = 0.9945 \approx 1.0$, $P = 0.0122$.
- **Results**:
  - Shunt: $I_w = 0.0104\text{ pu} \implies R_c = 96.15\text{ pu}$; $I_\mu = 0.0574\text{ pu} \implies X_m = 17.42\text{ pu}$.
  - Series: $R_{\text{eq}} = 0.0122\text{ pu}$, $X_{\text{eq}} = 0.050\text{ pu}$.
  - $VR$ (0.8 lag) = $0.0122(0.8) + 0.05(0.6) = 3.976\%$.
  - Max Efficiency = $\sqrt{0.0104 / 0.0122} \times 50\text{ kVA} = 46.16\text{ kVA}$.

![Whiteboard showing derivation of shunt, series parameters, and efficiency](frames/028/frame_0166_64m32s.jpg)

## Conceptual Questions
_(66:23 - 72:06)_

> [!example] Ideal Transformer Metrics
> Assertion: Both efficiency and voltage regulation of an ideal transformer are 100%.

- **Reasoning**: An ideal transformer has no losses ($\eta = 100\%$). It also has zero internal impedance ($Z = 0$), so no voltage drop occurs under load ($V_{NL} = V_{FL}$). Thus, VR is **0%**, not 100%. Assertion is False.

---

## Summary and Key Takeaways

- Open-circuit test data at rated voltage gives the core loss $P_i$, while short-circuit test data at rated current gives the full-load copper loss $P_{cu,fl}$.
- Voltage regulation can be evaluated using $VR = x(R_{\text{pu}} \cos\phi \pm X_{\text{pu}} \sin\phi)$ or the equivalent form $VR = x Z_{\text{pu}} \cos(\theta \mp \phi)$.
- The loading fraction $x = S_{\text{actual}} / S_{\text{rated}}$ scales the voltage regulation directly with load current.
- For three-phase transformers, the turns ratio must always be evaluated using per-phase voltages rather than line-to-line voltages.
- Tap changer settings adjust the primary winding turns ratio to boost voltage and maintain rated voltage at distant load terminals.
- Converting all test measurements to per-unit values eliminates the need to track three-phase star or delta connection factors.
- Zero voltage regulation occurs at a leading power factor when $\tan\phi = R/X$, which corresponds to $\cos\phi = X/Z$.
- An ideal transformer has $100\%$ efficiency and $0\%$ voltage regulation because it possesses zero internal impedance and zero losses.

---

[← Lec 027: Voltage Regulation](Lecture_027_Voltage_Regulation.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 029: Important Concepts in Electrical Machines 1 →](Lecture_029_Important_Concepts_in_Electrical_Machines_1.md)
