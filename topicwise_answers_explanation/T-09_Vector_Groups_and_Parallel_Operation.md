# T-09: Vector Groups & Parallel Operation

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Vector Groups & Parallel Operation** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-09: Parallel Operation of Three-Phase Transformers

*Appears in: 2017 Q7(b), 2021 Q4(a), 2023 Q4(b)*

#### Why transformers are operated in parallel

In power substations, multiple smaller transformers are operated in parallel rather than using a single giant transformer:
1. **Reliability & continuity of service:** If one unit fails or undergoes scheduled maintenance, the remaining units keep power flowing to critical loads.
2. **Efficiency optimization:** During light-load hours (such as late night), one or more units can be switched off to avoid paying constant iron losses on all units.
3. **System expansion:** Substation capacity can grow incrementally with urban load growth by adding parallel units without replacing existing infrastructure.

![Parallel operation of transformers and terminal polarity](../Books/diagrams/Ch-32_p79_fig68.jpg)

#### Essential conditions for parallel operation

To connect two three-phase transformers in parallel without dangerous circulating currents or damage, five conditions must be satisfied:

1. **Identical voltage ratios (same primary and secondary ratings):**
   - If secondary voltages differ ($V_{2A} \neq V_{2B}$), a net voltage difference $\Delta V = V_{2A} - V_{2B}$ acts around the local secondary loop formed by the two paralleled windings.
   - The loop impedance is just the internal leakage impedances: $Z_{loop} = Z_{A} + Z_{B}$.
   - Circulating current:
     $$I_c = \frac{V_{2A} - V_{2B}}{Z_A + Z_B}$$
   - Because winding impedances are very small (a few ohms or less), even a 2% difference in voltage produces a massive circulating current, causing continuous overheating even at zero external load.

2. **Identical per-unit (or percentage) impedances:**
   - When supplying an external load current $I_L$, the load divides inversely as the internal impedances:
     $$\vec{I}_A = \vec{I}_L \frac{\vec{Z}_B}{\vec{Z}_A + \vec{Z}_B}, \qquad \vec{I}_B = \vec{I}_L \frac{\vec{Z}_A}{\vec{Z}_A + \vec{Z}_B}$$
   - For both transformers to share the load strictly in proportion to their rated kVA capacities ($S_A / S_B = S_{rated,A} / S_{rated,B}$), their per-unit impedances on their own ratings must be equal:
     $$Z_{pu,A} = Z_{pu,B}$$
   - If per-unit impedances differ, the unit with the smaller per-unit impedance takes a disproportionate share and overloads before the system reaches full rating.

3. **Same polarity:**
   - The instantaneous secondary voltages must oppose each other inside the loop so that net loop voltage is zero.
   - If polarity is reversed, the voltages add in phase ($\Delta V = 2V_2$), resulting in a dead short-circuit that trips protection or destroys the transformer.

4. **Same phase sequence:**
   - Both units must be connected to the busbars with the identical phase rotation (e.g., $A-B-C$). If one is reversed ($A-C-B$), line voltages match at only one phase; the other two phases produce a line-to-line short circuit across the secondary bus.

5. **Same vector group and zero relative phase displacement:**
   - Three-phase transformer connections (like Star-Delta) introduce an inherent 30° phase shift between primary and secondary line voltages. Paralleled transformers must produce secondary line voltages that are in exact time phase.

![Equivalent circuit of two transformers operating in parallel](../Books/diagrams/Ch-32_p81_fig71.jpg)

---

### [2021 Q8(b)]: Vector Groups and the Clock Notation

> 📋 **Appeared in:** 2021 Q8(b)

#### What a vector group indicates

A three-phase transformer vector group designates:
- High-voltage (HV) winding connection (uppercase letter: **Y** for Star, **D** for Delta, **Z** for Zigzag).
- Low-voltage (LV) winding connection (lowercase letter: **y**, **d**, **z**).
- Availability of a neutral terminal (**n** or **N**).
- Phase displacement between HV and LV terminals using **clock notation** (0 to 11).

![Clock position phase displacement for transformer vector groups](../SlidesByMaam/diagrams/L-11_ECE-2107_p28_fig02.jpg)

#### Decoding the clock notation

- The high-voltage line voltage phasor is taken as reference, fixed at **12 o'clock** (minute hand, 0°).
- The corresponding low-voltage line voltage phasor represents the **hour hand**.
- Each hour represents $360° / 12 = 30°$ of phase lag measured clockwise:
  - **Group 1 (0° phase shift):** Yy0, Dd0, Dz0 (Hour hand at 12 o'clock).
  - **Group 2 (180° phase shift):** Yy6, Dd6, Dz6 (Hour hand at 6 o'clock).
  - **Group 3 (-30° or 330° phase shift):** Yd1, Dy1, Yz1 (Hour hand at 1 o'clock: LV leads HV by 30° or lags by 330°).
  - **Group 4 (+30° or 30° phase shift):** Yd11, Dy11, Yz11 (Hour hand at 11 o'clock: LV leads HV by 30° or lags by 330°).

#### What "Dyn5" represents:

- **D:** High-voltage winding is connected in **Delta**.
- **y:** Low-voltage winding is connected in **Star**.
- **n:** Neutral point is brought out to a terminal on the LV star side.
- **5:** The secondary line voltage lags the primary line voltage by $5 \times 30° = 150°$ (pointing to 5 o'clock).

---

### [2019 Q3(c)]: Can Yd11 and Dy1 operate in parallel?

> 📋 **Appeared in:** 2019 Q3(c)

#### Phase angle analysis

1. **Transformer 1 (Yd11):**
   - Belongs to Group 4 (11 o'clock).
   - Low-voltage phasor points at 11 o'clock ($+30°$ or $-330°$).
   - LV line voltage leads HV line voltage by $30°$: $\angle V_{2A} = +30°$.

2. **Transformer 2 (Dy1):**
   - Belongs to Group 3 (1 o'clock).
   - Low-voltage phasor points at 1 o'clock ($-30°$ or $+330°$).
   - LV line voltage lags HV line voltage by $30°$: $\angle V_{2B} = -30°$.

#### Calculating the circulating voltage

The phase displacement between the secondary voltages of the two transformers is:
$$\Delta \theta = (+30°) - (-30°) = 60°$$

The resultant open-circuit voltage across paralleled secondary terminals is:
$$\vec{V}_{diff} = \vec{V}_{2A} - \vec{V}_{2B}$$
$$|V_{diff}| = 2 V_2 \sin\left(\frac{60°}{2}\right) = 2 V_2 \sin(30°) = 2 V_2 (0.5) = V_2$$

The net voltage driving circulating current around the local secondary loop equals **the full rated line voltage ($100\% V_2$)**!

#### Conclusion

Because the loop impedance is only the internal winding leakage impedances ($Z_A + Z_B \approx 0.08–0.10\text{ pu}$), connecting Yd11 and Dy1 in parallel would drive a circulating current equal to **10 to 12 times rated current**. 

This is equivalent to a severe symmetrical short circuit. Therefore, **direct parallel operation is impossible**.

---
