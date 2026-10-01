[← T-07: 3-Phase & Open-Delta](T-07_Three-Phase_Connections_and_Open-Delta.md) | [🏠 Index](README.md) | [T-09: Vector Groups & Parallel →](T-09_Vector_Groups_and_Parallel_Operation.md)

---

# T-08: Scott (T-T) Connection

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Scott (T-T) Connection** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-08: Scott (T-T) Connection: Conversion Between 3-Phase and 2-Phase

*Appears in: 2018 Q4(a), 2018 Q4(b), 2019 Q4(b)*

#### Why phase conversion is needed

Standard electrical power generation and transmission are universally 3-phase. However, certain heavy industrial loads: such as large electric arc furnaces, induction heating equipment, and two-phase AC servomotors: require balanced two-phase power (two equal voltages displaced by 90° in time). 

Directly connecting a single-phase or two-phase load across a 3-phase line causes severe voltage unbalance, overheating nearby generators and motors. The Scott connection (invented by Charles F. Scott) provides a balanced conversion: it draws balanced 3-phase currents from the supply while delivering balanced 2-phase power to the load (or vice versa).

#### Construction and connection details

The scheme uses two single-phase transformers:
1. **Main transformer ($T_M$):**
   - The primary winding has $N_1$ turns with a center tap $D$ at exactly 50% turns ($N_1/2$).
   - Connected across two line terminals of the 3-phase supply: lines $A$ and $B$.
   - Primary voltage is the full line-to-line voltage $V_{AB} = V_L$.

2. **Teaser transformer ($T_T$):**
   - The primary winding has $N_T = \frac{\sqrt{3}}{2} N_1 \approx 0.866 N_1$ turns.
   - Connected between the center tap $D$ of the main transformer primary and the third line terminal $C$.
   - Voltage across the teaser primary is the median of the equilateral voltage triangle: $V_{DC} = \frac{\sqrt{3}}{2} V_L \approx 0.866 V_L$.

3. **Secondaries:**
   - Both main and teaser secondaries have an equal number of turns $N_2$.
   - This ensures both output phase voltages have identical magnitude: $V_{2M} = V_{2T} = V_2$.

![The Scott-T connection schematic](../SlidesByMaam/diagrams/L-11_ECE-2107_p22_fig01.jpg)

#### Mathematical proof of 90° phase displacement

In a balanced 3-phase system, the line voltages form an equilateral triangle $ABC$ with sides equal to $V_L$:
- Let line voltage $\vec{V}_{AB} = V_L \angle 0°$ (horizontal reference).
- Center tap $D$ divides $AB$ into two equal halves: $\vec{V}_{AD} = \vec{V}_{DB} = \frac{1}{2} V_L \angle 0°$.
- Vertex $C$ is at distance $V_L$ from both $A$ and $B$.

From equilateral triangle geometry, the altitude $DC$ from the midpoint $D$ to vertex $C$ is perpendicular to base $AB$:
$$\vec{V}_{DC} = \vec{V}_C - \vec{V}_D$$
$$|V_{DC}| = \sqrt{V_L^2 - \left(\frac{V_L}{2}\right)^2} = \sqrt{\frac{3}{4} V_L^2} = \frac{\sqrt{3}}{2} V_L \approx 0.866 V_L$$

Because $DC \perp AB$, the phasor $\vec{V}_{DC}$ is shifted by exactly 90° in time relative to $\vec{V}_{AB}$:
$$\vec{V}_{AB} = V_L \angle 0°$$
$$\vec{V}_{DC} = \frac{\sqrt{3}}{2} V_L \angle 90°$$

![Scott-T connection phasor diagram](../SlidesByMaam/diagrams/L-11_ECE-2107_p23_fig01.jpg)

#### Secondary induced EMFs

The secondary voltage of the main transformer is:
$$V_{2M} = V_{AB} \times \frac{N_2}{N_1} = V_L \frac{N_2}{N_1} \angle 0°$$

The secondary voltage of the teaser transformer is:
$$V_{2T} = V_{DC} \times \frac{N_2}{N_T} = \left(\frac{\sqrt{3}}{2} V_L \angle 90°\right) \times \frac{N_2}{\frac{\sqrt{3}}{2} N_1} = V_L \frac{N_2}{N_1} \angle 90°$$

Notice how the factor $\frac{\sqrt{3}}{2}$ cancels out perfectly. The two output voltages have identical magnitudes and are in exact time quadrature (90° phase shift):
$$\boxed{|V_{2M}| = |V_{2T}| \quad \text{and} \quad \vec{V}_{2T} \text{ leads } \vec{V}_{2M} \text{ by } 90°}$$

This constitutes a true, balanced 2-phase electrical supply.

---

### [2018 Q4(b)]: Worked Numerical Problem

> 📋 **Appeared in:** 2018 Q4(b)

**Problem:** Two T-connected transformers supply a 440V, 33 kVA balanced load from a 3300V balanced 3-phase supply. Find: (i) voltage and current rating of each coil, (ii) kVA rating of main and teaser.

#### Step-by-step physical solution

**Given:**
- 3-phase supply line voltage: $V_L = 3300\text{ V}$.
- 2-phase balanced load: $S_{total} = 33\text{ kVA}$, $V_2 = 440\text{ V}$.
- Power per phase in 2-phase system: $S_{phase} = 33 / 2 = 16.5\text{ kVA}$.

**1. Secondary coil ratings (identical for both transformers):**
- Secondary voltage: $V_2 = 440\text{ V}$.
- Secondary current:
  $$I_2 = \frac{S_{phase}}{V_2} = \frac{16500\text{ VA}}{440\text{ V}} = 37.5\text{ A}$$

**2. Main transformer primary coil ratings:**
- Main primary is connected across lines $A$ and $B$:
  $$V_{1,\text{main}} = V_L = 3300\text{ V}$$
- Primary current:
  $$I_{1,\text{main}} = \frac{S_{phase}}{V_{1,\text{main}}} = \frac{16500}{3300} = 5.0\text{ A}$$

**3. Teaser transformer primary coil ratings:**
- Teaser primary has $0.866 N_1$ turns and is connected from center-tap $D$ to phase $C$:
  $$V_{1,\text{teaser}} = \frac{\sqrt{3}}{2} \times 3300 = 0.866 \times 3300 = 2857.8\text{ V} \approx 2858\text{ V}$$
- Primary current (carries line current from phase $C$):
  $$I_{1,\text{teaser}} = \frac{S_{phase}}{V_{1,\text{teaser}}} = \frac{16500}{2857.8} = 5.77\text{ A}$$

**4. kVA rating of main and teaser transformers:**
$$\text{kVA}_{\text{main}} = V_{1,\text{main}} \times I_{1,\text{main}} = 3300\text{ V} \times 5.0\text{ A} = \boxed{16.5\text{ kVA}}$$
$$\text{kVA}_{\text{teaser}} = V_{1,\text{teaser}} \times I_{1,\text{teaser}} = 2857.8\text{ V} \times 5.77\text{ A} = \boxed{16.5\text{ kVA}}$$

**Conclusion:** Both transformers operate at identical apparent power ratings ($16.5\text{ kVA}$ each), perfectly sharing the total $33\text{ kVA}$ load.

---

[← T-07: 3-Phase & Open-Delta](T-07_Three-Phase_Connections_and_Open-Delta.md) | [🏠 Index](README.md) | [T-09: Vector Groups & Parallel →](T-09_Vector_Groups_and_Parallel_Operation.md)
