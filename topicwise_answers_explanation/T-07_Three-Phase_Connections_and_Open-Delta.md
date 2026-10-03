[← T-06: OC/SC Tests & Efficiency](T-06_OC-SC_Tests_Efficiency_and_Losses.md) | [🏠 Index](README.md) | [T-08: Scott T-T Connection →](T-08_Scott_T-T_Connection.md)

---

# T-07: Three-Phase Connections & Open-Delta

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Three-Phase Connections & Open-Delta** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2018 Q4(c) / 2024 Q4(b)]: Open-Delta (V-V) Connection and Continuity of Supply

> 📋 **Appeared in:** 2018 Q4(c), 2019 Q3(b), 2020 Q4(b), 2021 Q3(b), 2023 Q3(a), 2024 Q4(b)

**(b) Is it possible to maintain 3-$\varphi$ power supply when one phase of a 3-$\varphi$ transformer is burned out? If 'Yes', justify the answer. If 'Not', then also justify your answer. [Marks: 04, CO: 1]**

#### The scenario & Answer: YES

You have a 3-phase Δ-Δ transformer bank with three single-phase units. One fails overnight. You cannot shut down the system. Can you continue serving the 3-phase load? Yes: using open-delta.

#### Why three-phase voltage remains balanced

Remove transformer $T_{CA}$ from the bank. Transformers $T_{AB}$ and $T_{BC}$ remain.

On the primary (supply) side: The 3-phase supply maintains $V_{AB}$ and $V_{BC}$ (two of the three line voltages). By KVL around the delta loop:
$$V_{CA} + V_{AB} + V_{BC} = 0 \implies V_{CA} = -(V_{AB} + V_{BC})$$

This voltage $V_{CA}$ is the third line voltage, and it is **automatically determined** by the other two. The 3-phase supply is balanced, so $V_{CA}$ is perfectly balanced with $V_{AB}$ and $V_{BC}$.

On the secondary (load) side: Each remaining transformer has a secondary EMF proportional to its primary voltage × turns ratio $K$. So:
$V_{ab} = K \cdot V_{AB}$, $V_{bc} = K \cdot V_{BC}$.

By KVL on the secondary side:
$$V_{ca} = -(V_{ab} + V_{bc}) = K \cdot V_{CA}$$

All three secondary line voltages are present and balanced. The load sees a balanced 3-phase supply.

#### Why capacity drops to 57.7%

**Closed-Δ (3 transformers):** Each transformer rated $S = VI$ kVA. Total = $3S$.

**Open-Δ (2 transformers):** Each transformer still handles its rated current $I$ and rated voltage $V$. Each transformer's instantaneous power output alternates. For a balanced load with unity power factor, the effective power from each transformer:

Think about it geometrically. In a balanced 3-phase system, the voltages are 120° apart. When two transformers supply a balanced load, the phase angles of their voltage-current products are not both at unity power factor: they are at $+30°$ and $-30°$ from unity:
- Transformer 1 operates at power factor $\cos 30° = \sqrt{3}/2 = 0.866$
- Transformer 2 operates at power factor $\cos 30° = 0.866$ (by symmetry)

Each delivers power: $V \times I \times 0.866 = 0.866 S$

Total open-Δ power $= 2 \times 0.866 S = \sqrt{3} S$

$$\frac{S_{\text{open}}}{S_{\text{closed}}} = \frac{\sqrt{3}S}{3S} = \frac{1}{\sqrt{3}} = 0.577 = 57.7\%$$

![V-V or open delta transformer connection schematic](../SlidesByMaam/diagrams/L-11_ECE-2107_p16_fig01.jpg)

![Phasor diagram of open delta V-V connection under balanced load](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_52.jpeg)

#### Utilization factor

Each transformer is rated $S$ kVA but works at $0.866 S$ kW useful power. The transformer's KVA product ($VI$) is at its rated value, but only $86.6\%$ of it goes to real power (the rest is reactive). So the transformer is 86.6% utilized: not 100%.

#### When to use it

1. Emergency operation when one transformer fails.
2. During maintenance (remove one transformer, keep supply going).
3. For initial low-cost installation where future load growth is expected (start with two, add third later).


---

### [2024 Q3(b)]: Designing a Three-Phase Transformer Using Three Single-Phase Units

> 📋 **Appeared in:** 2024 Q3(b)

**(b) Explain with the help of vector diagram, how three 1-$\varphi$ transformers can be used to design a 3-$\varphi$ transformer. [Marks: 04, CO: 2]**

#### 1. Concept of a Three-Phase Transformer Bank
Instead of building a single 3-phase three-limbed core unit, three identical single-phase transformers can be interconnected (banked) on both primary and secondary sides to handle three-phase power.

![The four standard three-phase transformer connections: Y-Y, delta-delta, Y-delta and delta-Y](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_51.jpeg)

#### 2. The Four Standard Winding Configurations
Three identical single-phase transformers ($T_A, T_B, T_C$), each with transformation ratio $a = N_1 / N_2$, can be interconnected in four primary/secondary arrangements:

1. **Star-Star (Y-Y) Connection:**
   - Primaries are star-connected to supply lines $A, B, C$ with neutral $N$. Secondaries are star-connected to load lines $a, b, c$ with neutral $n$.
   - Phase voltages: $V_{1,ph} = V_{1,L}/\sqrt{3}$, $V_{2,ph} = V_{2,L}/\sqrt{3}$.
   - Line current equals phase winding current: $I_L = I_{ph}$.
   - **Phase shift:** Primary and secondary line voltages are in phase ($0^\circ$ phase shift).

2. **Delta-Delta ($\Delta$-$\Delta$) Connection:**
   - Primaries and secondaries are connected in closed loops.
   - Winding voltages equal full line voltages: $V_{1,ph} = V_{1,L}$, $V_{2,ph} = V_{2,L}$.
   - Line currents are $\sqrt{3}$ times phase winding currents: $I_L = \sqrt{3} I_{ph}$ and lag phase currents by $30^\circ$.
   - **Phase shift:** $0^\circ$ between primary and secondary line voltages.

3. **Star-Delta (Y-$\Delta$) Connection:**
   - Primary in star ($V_{1,ph} = V_{1,L}/\sqrt{3}$); secondary in delta ($V_{2,ph} = V_{2,L}$).
   - Overall voltage transformation ratio:
     $$\frac{V_{1,L}}{V_{2,L}} = \frac{\sqrt{3} V_{1,ph}}{V_{2,ph}} = \sqrt{3} a$$
   - **Vector diagram phase shift:** Secondary line voltage lags (or leads) primary line voltage by $30^\circ$ (clock group Yd1 or Yd11).

4. **Delta-Star ($\Delta$-Y) Connection:**
   - Primary in delta ($V_{1,ph} = V_{1,L}$); secondary in star ($V_{2,L} = \sqrt{3} V_{2,ph}$).
   - Overall voltage transformation ratio:
     $$\frac{V_{1,L}}{V_{2,L}} = \frac{V_{1,ph}}{\sqrt{3} V_{2,ph}} = \frac{a}{\sqrt{3}}$$
   - **Vector diagram phase shift:** Secondary line voltage leads (or lags) primary line voltage by $30^\circ$ (clock group Dy11 or Dy1). Extensively used for step-up generation and 4-wire secondary distribution.

#### 3. Summary of Vector Relationships

| Connection | Primary Line Voltage | Secondary Line Voltage | Line Voltage Ratio ($V_{1,L}/V_{2,L}$) | Phase Shift ($\theta_{L2} - \theta_{L1}$) |
|:---|:---:|:---:|:---:|:---:|
| **Y - Y** | $\sqrt{3} V_{1,ph}$ | $\sqrt{3} V_{2,ph}$ | $a$ | $0^\circ$ |
| **$\Delta$ - $\Delta$** | $V_{1,ph}$ | $V_{2,ph}$ | $a$ | $0^\circ$ |
| **Y - $\Delta$** | $\sqrt{3} V_{1,ph}$ | $V_{2,ph}$ | $\sqrt{3} a$ | $\pm 30^\circ$ |
| **$\Delta$ - Y** | $V_{1,ph}$ | $\sqrt{3} V_{2,ph}$ | $a / \sqrt{3}$ | $\pm 30^\circ$ |

#### 4. Engineering Trade-offs: Single 3-$\varphi$ Unit vs. Bank of Three 1-$\varphi$ Units
- **Transportation and Weight:** For very large ratings (e.g., hundreds of MVA), three single-phase units are significantly easier to transport over bridges and mountainous roads than one massive 3-phase unit.
- **Spare Unit Economy:** A substation requires only one single-phase spare unit (33% capital reserve) instead of an entire duplicate three-phase transformer (100% reserve).
- **Service Continuity:** If one unit in a $\Delta$-$\Delta$ bank burns out, the bank can immediately operate in **Open-Delta (V-V)** at $57.7\%$ capacity without interrupting power supply.

---

### Q3(a): Limitations of Y-Y transformer: the third harmonic problem

> 📋 **Appeared in:** 2021 Q3(a)

#### Why third harmonics exist in transformer cores

Transformer cores are made of ferromagnetic material. The B-H curve of iron is non-linear (it saturates). This means the magnetizing current needed to produce a sinusoidal flux is not itself sinusoidal: it contains third, fifth, and higher harmonics.

In particular, to produce a sinusoidal core flux at 50 Hz, the magnetizing current must be rich in third harmonics (150 Hz components). This is just the physics of ferromagnetic magnetization.

#### How Y-Y connection blocks third harmonics

In a balanced 3-phase system, third harmonic currents are "zero-sequence": all three phases have the same phase angle at the third harmonic frequency. They want to flow in or out of all three phases simultaneously.

In a Y-Y connected transformer without a grounded neutral: zero-sequence currents have no return path. They cannot flow. The third harmonic magnetizing currents are suppressed.

**Consequence:** Since the magnetizing current can only be sinusoidal (no third harmonics allowed), the core flux is no longer sinusoidal. The flux becomes "peaked" (its waveform becomes distorted: similar to a square wave peak). A peaked flux induces a peaked (distorted) EMF in the windings.

The phase-to-neutral voltage (line-to-neutral voltage) contains third harmonic components. The line-to-line voltages are unaffected (third harmonics cancel in line-to-line differences), but the neutral point "floats" and the neutral voltage contains harmonics.

#### Solutions

1. **Ground the neutral (4-wire Y-Yn):** Third harmonic currents flow through the grounded neutral. Flux remains sinusoidal. No harmonic voltages.

2. **Delta-connected tertiary:** Add a delta-connected third winding. The closed delta provides a circulating path for third harmonic currents. Suppresses harmonic voltages without needing a grounded neutral. Very commonly used in large power transformers.

3. **Avoid Y-Y altogether:** Use Y-Δ or Δ-Y. The delta side always provides a path for third harmonic circulation.

![Three phase transformer core configurations and winding connections](../SlidesByMaam/diagrams/L-11_ECE-2107_p07_fig01.jpg)

---

[← T-06: OC/SC Tests & Efficiency](T-06_OC-SC_Tests_Efficiency_and_Losses.md) | [🏠 Index](README.md) | [T-08: Scott T-T Connection →](T-08_Scott_T-T_Connection.md)
