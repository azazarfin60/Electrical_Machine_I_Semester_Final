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

(Line current on secondary $= \sqrt{3} \times 14492 = 25095$ A total)

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

### [2023 Q4(a)]
> 📋 **Appeared in:** 2017 Q7(a), 2018 Q3(c), 2019 Q4(a), 2020 Q4(b), 2021 Q3(b), 2023 Q4(a) (Years: 2017, 2018, 2019, 2020, 2021, 2023)

**(a) Explain what happens to a 3-phase Δ-Δ transformer bank when one transformer is damaged. Show 3-phase power can still be served. Also prove the capacity reduces to 57.7%. [08, CO1]**

![The open-Delta (or V-V) connection schematic](../SlidesByMaam/diagrams/L-11_ECE-2107_p16_fig01.jpg)
![Open-Delta (V-V) Connection Circuit and Phasor Diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_52.jpeg)

**Event:** One transformer (say $T_{CA}$) in the Δ-Δ bank fails.

**Why 3-phase power still reaches the load:**

The primary and secondary delta loops still have two active transformers: $T_{AB}$ and $T_{BC}$.

On the primary delta: The 3-phase supply maintains $V_{AB}$ and $V_{BC}$. KVL in the delta loop demands $V_{CA} = -(V_{AB} + V_{BC})$. Even without $T_{CA}$, this voltage is present at the open terminal.

On the secondary delta: $T_{AB}$ produces $V_{ab} = K\cdot V_{AB}$. $T_{BC}$ produces $V_{bc} = K\cdot V_{BC}$. By KVL: $V_{ca} = -(V_{ab} + V_{bc}) = K\cdot V_{CA}$. All three secondary line voltages exist and are balanced.

**Three-phase balanced power is delivered by two transformers.** This configuration is called the open-delta (V-V) connection.

**Capacity proof:**

Let each single transformer be rated $S = VI$ kVA.

In closed-Δ (3 transformers): Total $= 3S$ kVA.

In open-Δ (2 transformers):
Each transformer still carries rated current $I$ at rated voltage $V$.
For a balanced 3-phase unity pf load, each transformer operates at power factor $\cos 30° = \sqrt{3}/2$.

$$S_{\text{open}} = 2 \times V \times I \times \cos 30° = 2VI \times \frac{\sqrt{3}}{2} = \sqrt{3}VI = \sqrt{3}S$$

$$\frac{S_{\text{open}}}{S_{\text{closed}}} = \frac{\sqrt{3}S}{3S} = \frac{1}{\sqrt{3}} = 0.577 = \boxed{57.7\%}$$

**Utilization factor of each transformer** in open-Δ: The transformer is rated $S = VI$ kVA but works at power factor $\cos 30° = 0.866$, delivering only $0.866 S$ kW. So the utilization is 86.6% instead of 100%.

---

[← T-06: OC/SC Tests & Efficiency](T-06_OC-SC_Tests_Efficiency_and_Losses.md) | [🏠 Index](README.md) | [T-08: Scott T-T Connection →](T-08_Scott_T-T_Connection.md)
