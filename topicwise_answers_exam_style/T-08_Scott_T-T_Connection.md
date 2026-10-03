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
1. **Main transformer:** Standard transformer. Primary connected between two phases (e.g., A and B). It provides the horizontal component of the 2-phase voltage.

2. **Teaser transformer:** Primary has $\sqrt{3}/2$ of main transformer turns (86.6% of main turns). It is connected from the midpoint of the main transformer primary to the third phase (C). It provides the vertical component.

The two secondary voltages are equal in magnitude and 90° apart in time: giving a balanced 2-phase output.

![The Scott-T connection schematic](../SlidesByMaam/diagrams/L-11_ECE-2107_p22_fig01.jpg)
![Scott-T connection phasor diagram](../SlidesByMaam/diagrams/L-11_ECE-2107_p23_fig01.jpg)

**Application:** Used in electric arc furnace power supplies and to power 2-phase induction motors. Also used to convert 2-phase power to 3-phase.

---

### [2018 Q4(b)]
> 📋 **Appeared in:** 2018 Q4(b)

**(b) Two T-connected transformers supply a 440V, 33 kVA balanced load from a 3300V balanced 3-phase supply. Find: (i) voltage and current rating of each coil, (ii) kVA rating of main and teaser. [04]**

> 💡 *Note: This exact problem was repeated in [2024 Q4(c)](#2024-q4c) below. The standard 3-φ to 3-φ T-T solution is presented here.*

**Step 1: System line currents:**
- Primary line current:
  $$I_{1L} = \frac{S}{\sqrt{3} V_{1L}} = \frac{33000}{\sqrt{3} \times 3300} = \mathbf{5.77\text{ A}}$$
- Secondary line current:
  $$I_{2L} = \frac{S}{\sqrt{3} V_{2L}} = \frac{33000}{\sqrt{3} \times 440} = \mathbf{43.30\text{ A}}$$

#### (i) Voltage and current rating of each coil:
- **Main Transformer ($T_1$):**
  - Primary coil: $V_{1,\text{main}} = V_{1L} = \mathbf{3300\text{ V}}, \quad I_{1,\text{main}} = I_{1L} = \mathbf{5.77\text{ A}}$
  - Secondary coil: $V_{2,\text{main}} = V_{2L} = \mathbf{440\text{ V}}, \quad I_{2,\text{main}} = I_{2L} = \mathbf{43.30\text{ A}}$
- **Teaser Transformer ($T_2$):**
  - Primary coil: $V_{1,\text{teaser}} = \frac{\sqrt{3}}{2} \times 3300 = \mathbf{2858\text{ V}}, \quad I_{1,\text{teaser}} = I_{1L} = \mathbf{5.77\text{ A}}$
  - Secondary coil: $V_{2,\text{teaser}} = \frac{\sqrt{3}}{2} \times 440 = \mathbf{381\text{ V}}, \quad I_{2,\text{teaser}} = I_{2L} = \mathbf{43.30\text{ A}}$

#### (ii) kVA rating of main and teaser transformer:
- **Operating ratings:**
  $$\text{kVA}_{\text{main}} = \frac{3300 \times 5.7735}{1000} = \boxed{\mathbf{19.05\text{ kVA}}}$$
  $$\text{kVA}_{\text{teaser}} = \frac{2857.9 \times 5.7735}{1000} = \boxed{\mathbf{16.50\text{ kVA}}}$$
- **Commercial interchangeable rating:** Both units sized for $\mathbf{19.05\text{ kVA}}$ each (total $38.10\text{ kVA}$, representing 15.5% oversize).
- *(Alternative 2-phase load interpretation: $I_2 = 37.5\text{ A}$, nominal rating $= 16.5\text{ kVA}$ each).*

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

### [2024 Q4(c)]
> 📋 **Appeared in:** 2018 Q4(b), 2024 Q4(c) (Years: 2018, 2024)

**(c) Two T-connected transformers are used to supply a 440 V, 33 KVA balanced load from a balanced 3-$\varphi$ supply of 3300 V. Calculate — [Marks: 04, CO: 2]**
> **(i)** voltage and current rating of each coil.
> **(ii)** KVA rating of the main and teaser transformer.

**Topology.** T1 primary sits across lines A–B (full 3300 V); T1 secondary across load lines a–b (full 440 V). T2 primary connects between line C and the 50% midpoint M of T1 primary ($V = \frac{\sqrt{3}}{2} \times 3300 = 2858\text{ V}$). T2 secondary connects between load line c and the 50% midpoint M of T1 secondary ($V = \frac{\sqrt{3}}{2} \times 440 = 381\text{ V}$).

![The Scott-T connection schematic](../SlidesByMaam/diagrams/L-11_ECE-2107_p22_fig01.jpg)

**Step 1: System line currents:**
$$I_{2L} = \frac{33000}{\sqrt{3} \times 440} = \frac{33000}{762.10} = \boxed{43.30\text{ A}}$$
$$I_{1L} = \frac{33000}{\sqrt{3} \times 3300} = \frac{10}{\sqrt{3}} = \boxed{5.77\text{ A}}$$

#### (i) Voltage and current rating of each coil

**Main transformer (T1):**
$$\text{Primary coil: } 3300\text{ V}, \qquad 5.77\text{ A}$$
$$\text{Secondary coil: } 440\text{ V}, \qquad 43.30\text{ A}$$

**Teaser transformer (T2):**
$$\text{Primary coil: } \frac{\sqrt{3}}{2} \times 3300 = \mathbf{2858\text{ V}}, \qquad \mathbf{5.77\text{ A}}$$
$$\text{Secondary coil: } \frac{\sqrt{3}}{2} \times 440 = \mathbf{381\text{ V}}, \qquad \mathbf{43.30\text{ A}}$$

#### (ii) kVA rating of the main and teaser transformer

**Operating (calculated) ratings:**
$$\text{kVA}_{\text{main}} = \frac{3300 \times 5.7735}{1000} = \frac{440 \times 43.301}{1000} = \boxed{\mathbf{19.05\text{ kVA}}}$$
$$\text{kVA}_{\text{teaser}} = \frac{2857.9 \times 5.7735}{1000} = \frac{381.05 \times 43.301}{1000} = \boxed{\mathbf{16.50\text{ kVA}}}$$

Notice that $\text{kVA}_{\text{teaser}} = \frac{\sqrt{3}}{2}\,\text{kVA}_{\text{main}} = 0.866 \times 19.05 = 16.50\text{ kVA}$.

> [!IMPORTANT] Commercial identical units sanity check (15.5 % oversize)
> If two identical interchangeable transformers are used, both are sized for the larger requirement of **19.05 kVA** each (with an 86.6% tap provided on the teaser):
> $$\text{Total installed} = 19.05 + 19.05 = \mathbf{38.10\text{ kVA}}$$
> $$\frac{38.10}{33} = \frac{2}{\sqrt{3}} = \mathbf{1.155} \quad (\mathbf{15.5\% \text{ oversize}})$$
> Mentioning this is the mark-winning observation.
---

[← T-07: 3-Phase & Open-Delta](T-07_Three-Phase_Connections_and_Open-Delta.md) | [🏠 Index](README.md) | [T-09: Vector Groups & Parallel →](T-09_Vector_Groups_and_Parallel_Operation.md)
