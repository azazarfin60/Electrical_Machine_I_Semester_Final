[← T-06: OC/SC Tests & Efficiency](T-06_OC-SC_Tests_Efficiency_and_Losses.md) | [🏠 Index](README.md) | [T-08: Scott T-T Connection →](T-08_Scott_T-T_Connection.md)

---

# T-07: Three-Phase Connections & Open-Delta

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Three-Phase Connections & Open-Delta** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2018 Q3(a)]
> 📋 **Appeared in:** 2018 Q3(a)

**(a) Describe the four-wire delta-connected transformer. [03]**

A four-wire delta connection is used for 3-phase distribution where a neutral is needed. Three single-phase transformers connect in a delta (Δ) configuration on the secondary. A center-tap is taken from one of the secondary windings, which forms the neutral (4th wire).

The result is: three-phase secondary voltages available (e.g., 240V line-to-line) and single-phase voltages from line to neutral (half-phase voltage = 120V). This allows serving both 3-phase loads (motors) and single-phase loads (lighting) from the same transformer bank. The neutral provides the return path for single-phase currents.

---

### [2018 Q3(b)]
> 📋 **Appeared in:** 2018 Q3(b)

**(b) 10 MVA, 11kV supply, through three Y-Δ transformers to a 230V load. Find kVA per transformer, voltage per coil, current per coil. [06]**

**3-phase system, 10 MVA total:**

**kVA per transformer:**
$$S_{\text{each}} = \frac{10000}{3} = \boxed{3333.3 \text{ kVA}}$$

**Primary (Y-connected, 11kV line):**
$$V_{1,\text{coil}} = \frac{V_{1,\text{line}}}{\sqrt{3}} = \frac{11000}{\sqrt{3}} = \boxed{6351 \text{ V}}$$

$$I_{1,\text{coil}} = \frac{S_{\text{each}} \times 1000}{V_{1,\text{coil}}} = \frac{3333300}{6351} = \boxed{524.8 \text{ A}}$$

**Secondary (Δ-connected, 230V line):**
$$V_{2,\text{coil}} = V_{2,\text{line}} = \boxed{230 \text{ V}}$$

$$I_{2,\text{coil}} = \frac{S_{\text{each}} \times 1000}{V_{2,\text{coil}}} = \frac{3333300}{230} = \boxed{14492 \text{ A}}$$

(Line current on secondary $= \sqrt{3} \times 14492.75 = 25102\text{ A}$ total)

---

### [2018 Q4(c)]
> 📋 **Appeared in:** 2018 Q4(c)

**(c) Advantages of transformer bank. Line voltage ratios for 10:1 turns ratio connections. [04]**

**Advantages of transformer bank:**
1. Flexibility: can connect/disconnect one transformer at a time for maintenance.
2. Can use open-Δ (57.7% capacity) if one transformer fails: no complete outage.
3. Can be built up in stages as load grows.

**Line voltage ratios (turns ratio $a = 10:1$, so $N_1:N_2 = 10:1$):**

| Connection | Turns Ratio | Line Voltage Ratio |
|:---:|:---:|:---:|
| Y-Y | 10:1 | 10:1 |
| Δ-Δ | 10:1 | 10:1 |
| Δ-Y | 10:1 | $10:\sqrt{3}$ = 5.77:1 (step-up on secondary) |
| Y-Δ | 10:1 | $\sqrt{3} \times 10:1$ = 17.32:1 |
| Open-Δ | 10:1 | 10:1 (same as Δ-Δ but 57.7% capacity) |

---

## SECTION - B (Induction Motors: Q5 to Q8)

---

### [2020 Q4(c)]
> 📋 **Appeared in:** 2020 Q4(c)

**(c) Two 25 kVA transformers in open-Δ, supply 220V balanced 3-phase load. [04]**

**(i) Total load without overloading:**

Open-Δ rating $= \sqrt{3} \times 25 = 43.3$ kVA.

Check: Each transformer handles 25 kVA. Two transformers in open-Δ: $2 \times 25 \times \cos 30° = 2 \times 25 \times 0.866 = 43.3$ kVA.

$$\boxed{\text{Load without overloading} = 43.3 \text{ kVA}}$$

**(ii) When third 25 kVA transformer closes the Δ:**

Closed-Δ rating $= 3 \times 25 = 75$ kVA.

$$\boxed{\text{Total load with closed-Δ} = 75 \text{ kVA}}$$

---

## SECTION - B (Induction Motors: Q5 to Q8)

---

### [2021 Q3(a)]
> 📋 **Appeared in:** 2021 Q3(a)

**(a) Limitations of Y-Y connected transformer. How to overcome them? [03]**

![Y-Y transformer connection schematic](../SlidesByMaam/diagrams/L-11_ECE-2107_p07_fig01.jpg)

**Limitations:**

1. **Third harmonic voltages:** The magnetizing current of a transformer is non-sinusoidal: it contains third harmonics. In a Y-Y transformer, the neutral point is not usually connected. Third harmonic currents have no path to flow (they are zero-sequence). As a result, third harmonic EMFs appear in the line-to-neutral voltages, causing waveform distortion.

2. **Voltage unbalance:** Under unbalanced loads, the neutral point shifts. This causes unequal voltage distribution among phases.

3. **No phase shift:** Y-Y gives 0° phase displacement. This limits flexibility in interconnection with other transformer groups.

**How to overcome:**

1. **Connect the neutral to ground (4-wire system):** Allows zero-sequence (third harmonic) currents to flow. Eliminates harmonic voltages in phase-to-neutral voltages.

2. **Add a delta-connected tertiary winding:** The delta provides a closed circulating path for third harmonic currents. This suppresses harmonic voltages without requiring a grounded neutral.

3. **Use Δ winding on at least one side (Y-Δ or Δ-Y connection):** Inherently eliminates third harmonic voltage problems.

---

### [2023 Q3(a)]
> 📋 **Appeared in:** 2023 Q3(a), 2024 Q4(b) (Years: 2023, 2024)

**(a) Is it possible to continue $3-\varphi$ power supply when one phase is burn out? If "yes" then explain one method. [CO1, Marks: 04]**

**Yes, it is possible.** The method is the **open-delta (V-V) connection**.

![Open-delta (V-V) connection circuit with two transformers, and the phasor diagram showing that the third line voltage is still produced](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_52.jpeg)

**How it works.** Start from a $\Delta$–$\Delta$ bank of three single-phase transformers. If one unit burns out, disconnect and remove it. The remaining two are left connected in a "V" shape on both sides.

The two healthy transformers still produce two line voltages directly. The third line voltage appears across the open corner, because in a balanced 3-phase system the three line voltages sum to zero:
$$\vec{V}_{CA} = -(\vec{V}_{AB} + \vec{V}_{BC})$$

So the load still sees three balanced line voltages, $120°$ apart. Supply continues without interruption.

**Capacity.** Let $V$ and $I$ be the rated winding voltage and current of one transformer.

Closed $\Delta$–$\Delta$ bank:
$$S_{\Delta\Delta} = 3 V I$$

In open delta the line current is limited to the winding current of one transformer, so $I_L = I$ and $V_L = V$:
$$S_{VV} = \sqrt{3}\, V_L I_L = \sqrt{3}\, V I$$

$$\frac{S_{VV}}{S_{\Delta\Delta}} = \frac{\sqrt{3} V I}{3 V I} = \frac{1}{\sqrt{3}} = 0.577$$

$$\boxed{\text{Open-delta capacity} = 57.7\%\ \text{of the original } \Delta\text{--}\Delta \text{ bank}}$$

The two surviving units are each loaded to
$$\frac{\sqrt{3} V I}{2 V I} = \frac{\sqrt{3}}{2} = 86.6\%\ \text{of their own rating}$$

**Limitations.** The two transformers work at unequal power factors, $\cos(30° - \phi)$ and $\cos(30° + \phi)$. Secondary voltages fall slightly out of balance on load. It is an emergency or light-load arrangement only.

---

### [2023 Q3(c)]
> 📋 **Appeared in:** 2021 Q3(a), 2023 Q3(c) (Years: 2021, 2023)

**(c) Mention the limitations of a Y-Y connected transformer. [CO1, Marks: 02]**

![The four standard three-phase transformer connections: Y-Y, delta-delta, Y-delta and delta-Y](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_51.jpeg)

1. **Third-harmonic trouble.** The magnetising current needs a third-harmonic component. In Y-Y with isolated neutrals there is no closed path for it, so the flux wave is distorted and a large third-harmonic voltage (up to about 5 times normal) appears in each phase voltage.

2. **Neutral shifting on unbalanced load.** With an unbalanced or single-phase load and no neutral wire, the star point moves. Phase voltages become unequal, so some loads see over-voltage and others see under-voltage.

3. **Needs a neutral or a tertiary winding.** Both faults above are cured only by solidly earthing the neutrals or by adding a third delta (tertiary) winding. That adds cost.

4. **No emergency open-delta operation.** If one unit fails, a Y-Y bank cannot run as open delta. Supply is lost.

5. **Insulation cost.** Each winding must be insulated for $V_L/\sqrt{3}$, which is an advantage, but surge and harmonic stresses offset it.

> [!success] Exam line
> Y-Y is rarely used in practice. $\Delta$-Y, Y-$\Delta$ and $\Delta$-$\Delta$ are preferred.

---

### [2023 Q4(b)]
> 📋 **Appeared in:** 2023 Q4(b)

**(b) Prove that closed-$\Delta$ kVA is $\sqrt{3}$ times higher than that open-$\Delta$ kVA. [CO1, Marks: 03]**

Let each single-phase transformer be rated at winding voltage $V$ and winding current $I$.

**Closed $\Delta$–$\Delta$ (three transformers).**

In delta, $V_L = V_{ph} = V$ and $I_L = \sqrt{3} I_{ph} = \sqrt{3} I$. So
$$S_{\Delta} = \sqrt{3}\, V_L I_L = \sqrt{3} \times V \times \sqrt{3} I = 3 V I$$

This is simply three times the rating of one transformer, as expected.

**Open $\Delta$ (V-V, two transformers).**

Here each winding sits directly in a line, so the line current cannot exceed the winding rating:
$$I_L = I, \qquad V_L = V$$
$$S_{V} = \sqrt{3}\, V_L I_L = \sqrt{3}\, V I$$

**Ratio.**
$$\frac{S_{\Delta}}{S_{V}} = \frac{3 V I}{\sqrt{3} V I} = \frac{3}{\sqrt{3}} = \sqrt{3}$$

$$\boxed{S_{\Delta} = \sqrt{3}\, S_{V} \qquad \text{or} \qquad S_{V} = 0.577\, S_{\Delta}}$$

![Open-delta (V-V) bank of two transformers with its phasor diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_52.jpeg)

> [!example] Numerical feel
> Three 10 kVA units in $\Delta$-$\Delta$ give 30 kVA. Remove one and the two left give $\sqrt{3} \times 10 = 17.32$ kVA, which is $57.7\%$ of 30 kVA. Each of the two is then loaded to $17.32/2 = 8.66$ kVA, that is $86.6\%$ of its own 10 kVA.

---

### [2024 Q3(b)]
> 📋 **Appeared in:** 2024 Q3(b)

**(b) Explain with the help of vector diagram, how three 1-$\varphi$ transformers can be used to design a 3-$\varphi$ transformer. [Marks: 04, CO: 2]**

A three-phase transformer cannot always be bought as a single unit. Three single-phase transformers can be banked to do the same job.

**1. Y-Y (star-star) connection.** Put all three primaries in star and all three secondaries in star. Each primary phase winding takes $V_L/\sqrt{3}$ and each secondary takes $V_L/\sqrt{3}$. The phase shift is $0°$.

**2. $\Delta$-$\Delta$ (delta-delta) connection.** Put both windings in delta. Each winding takes the full $V_L$. The phase shift is also $0°$.

![The four standard three-phase transformer connections: Y-Y, delta-delta, Y-delta and delta-Y](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_51.jpeg)

**3. Mixed connections (Y-$\Delta$ and $\Delta$-Y).** One side star, the other delta. The phase shift is $30°$.

**Vector-diagram facts to state:**

- For a **star** connection the line voltage leads the phase voltage by $30°$: $V_L = \sqrt{3} V_{ph}$. Line current equals phase current.
- For a **delta** connection the phase voltage equals the line voltage, and the line current lags the phase current by $30°$: $I_L = \sqrt{3} I_{ph}$.
- Adding a phase shift of $30°$ on one winding alone gives the clock-notation numbers 1 or 11.

| Connection | $V_{ph}/V_L$ | $I_L/I_{ph}$ | Phase shift |
|:---|:---:|:---:|:---:|
| Y-Y | $1/\sqrt{3}$ | 1 | $0°$ |
| $\Delta$-$\Delta$ | 1 | $\sqrt{3}$ | $0°$ |
| Y-$\Delta$ | $V_{1,ph} = V_{1,L}/\sqrt3$, $V_{2,ph} = V_{2,L}$ | $\sqrt{3}$ on secondary | $30°$ |
| $\Delta$-Y | $V_{ph} = V_L$ | 1 on secondary | $30°$ |

**When to bank three single-phase transformers:** for large ratings, for easy transport and erection (a 3-phase unit must be shipped as one piece), and for maintenance, since one unit can be taken out and the remaining two can run in open-delta at 57.7% capacity.

---

[← T-06: OC/SC Tests & Efficiency](T-06_OC-SC_Tests_Efficiency_and_Losses.md) | [🏠 Index](README.md) | [T-08: Scott T-T Connection →](T-08_Scott_T-T_Connection.md)
