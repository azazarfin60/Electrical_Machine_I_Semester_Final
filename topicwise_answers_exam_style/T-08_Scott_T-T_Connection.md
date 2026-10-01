[← T-07: 3-Phase & Open-Delta](T-07_Three-Phase_Connections_and_Open-Delta.md) | [🏠 Index](README.md) | [T-09: Vector Groups & Parallel →](T-09_Vector_Groups_and_Parallel_Operation.md)

---

# T-08: Scott (T-T) Connection

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Scott (T-T) Connection** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2018 Q4(a)]
> 📋 **Appeared in:** 2018 Q4(a)

**(a) Explain Scott connection with necessary diagrams. [04]**

The Scott (or T-T) connection converts a 3-phase supply into a 2-phase supply (or vice versa) using two single-phase transformers.

**Two transformers required:**
1. **Main transformer (Teaser):** Standard transformer. Primary connected between two phases (e.g., A and B). It provides the horizontal component of the 2-phase voltage.

2. **Teaser transformer:** Primary has $\sqrt{3}/2$ of main transformer turns (86.6% of main turns). It is connected from the midpoint of the main transformer primary to the third phase (C). It provides the vertical component.

The two secondary voltages are equal in magnitude and 90° apart in time: giving a balanced 2-phase output.

![The Scott-T connection schematic](../SlidesByMaam/diagrams/L-11_ECE-2107_p22_fig01.jpg)
![Scott-T connection phasor diagram](../SlidesByMaam/diagrams/L-11_ECE-2107_p23_fig01.jpg)

**Application:** Used in electric arc furnace power supplies and to power 2-phase induction motors. Also used to convert 2-phase power to 3-phase.

---

### [2018 Q4(b)]
> 📋 **Appeared in:** 2018 Q4(b)

**(b) Two T-connected transformers supply a 440V, 33 kVA balanced load from a 3300V balanced 3-phase supply. Find: (i) voltage and current rating of each coil, (ii) kVA rating of main and teaser. [04]**

**Supply:** $V_L = 3300$ V (3-phase), Load: 440V, 33 kVA (2-phase)

**Secondary voltages (2-phase, equal):**
$$V_{2,\text{each}} = 440 \text{ V per phase}$$

**Secondary current:**
$$I_{2} = \frac{S/2}{V_{2}} = \frac{33000/2}{440} = \frac{16500}{440} = 37.5 \text{ A per phase}$$

**Primary voltage of main transformer:** Connected across A-B: $V_{AB} = V_L = 3300$ V

$$V_{1,\text{main}} = 3300 \text{ V}, \qquad I_{1,\text{main}} = \frac{S/2}{V_{1,\text{main}}} = \frac{16500}{3300} = 5 \text{ A}$$

**Primary voltage of teaser:** Connected from midpoint of AB to C. Length from midpoint of AB to C in an equilateral triangle:
$$V_{1,\text{teaser}} = \frac{\sqrt{3}}{2} \times V_L = 0.866 \times 3300 = 2858 \text{ V}$$

$$I_{1,\text{teaser}} = \frac{S/2}{V_{1,\text{teaser}}} = \frac{16500}{2858} = 5.77 \text{ A}$$

**kVA ratings:**
$$\text{Main transformer kVA} = V_{1,\text{main}} \times I_{1,\text{main}} = 3300 \times 5 = \boxed{16.5 \text{ kVA}}$$

$$\text{Teaser transformer kVA} = V_{1,\text{teaser}} \times I_{1,\text{teaser}} = 2858 \times 5.77 = \boxed{16.5 \text{ kVA}}$$

Both transformers have the same kVA rating. Total = 33 kVA ✓

---

### [2019 Q4(b)]
> 📋 **Appeared in:** 2019 Q4(b)

**(b) Convert 3-phase to 2-phase or vice versa? If yes, explain. [04]**

Yes. This is done using the **Scott (T-T) connection**.

**Principle:** Two single-phase transformers are used.

1. **Main transformer:** Primary connected between two phases of the 3-phase supply (e.g., lines A and B). Secondary provides one phase of the 2-phase output.

2. **Teaser transformer:** Primary connected from the mid-point of the main transformer primary to the third line (C). The teaser primary has $\sqrt{3}/2$ (86.6%) of the main transformer's turns. Secondary provides the second phase of the 2-phase output, exactly 90° displaced from the first.

**Why it works:** The two primary voltages are 90° apart geometrically in the phasor diagram (the line-to-midpoint voltage is perpendicular to the line-to-line voltage in a balanced 3-phase system). This 90° separation transfers to the two secondary voltages, giving a balanced 2-phase output.

**Reverse (2-phase to 3-phase):** Connect the two-phase supply to the secondaries and the 3-phase supply comes from the primaries: the same transformation works in reverse because transformers are reciprocal devices.

---

[← T-07: 3-Phase & Open-Delta](T-07_Three-Phase_Connections_and_Open-Delta.md) | [🏠 Index](README.md) | [T-09: Vector Groups & Parallel →](T-09_Vector_Groups_and_Parallel_Operation.md)
