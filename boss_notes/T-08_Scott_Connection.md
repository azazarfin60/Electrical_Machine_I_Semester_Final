[← T-07b: Open Delta](T-07b_Open_Delta.md) | [🏠 Index](00_Index.md) | [T-09: Vector Groups →](T-09_Vector_Groups.md)

---

# T-08: Scott (T-T) Connection
> **Section:** A | **Priority:** 🟡 MEDIUM | **Exam Frequency:** 1/7 years (Scott) · 2/7 years (T-connection)
> **Sources:** Theraja Ch-33 (Art. 33.10), VK Mehta Ch-7 (Art. 7.37), Slides L-11 S20–S24

## Why This Topic Matters

**Scott** and the **T-connection** are different topics and are easy to confuse. Scott proper appeared in only **1 of 7** papers (2018 Q4(a), 4 marks, "Explain Scott connections with the help of necessary diagrams"). The **T-connection** — two transformers in T supplying a balanced 3-φ load from a 3-φ supply — is a separate question and appeared **twice**: 2018 Q4(b) and again verbatim in 2024 Q4(c) (440 V, 33 kVA from 3300 V). Do not tag a T-connection numerical to Scott.

---

## 📝 Key Definitions

> **Scott (T-T) connection:** "The Scott connection is a means of converting a 3-phase supply to a 2-phase supply, or vice versa, using two single-phase transformers. One transformer is called the 'main' (or 'T') transformer and the other is called the 'teaser' transformer. The teaser primary has $\sqrt{3}/2$ (= 86.6%) of the main transformer primary turns." — VK Mehta, Art. 7.37

---

## How the Scott Connection Works

![Scott (T-T) connection schematic showing main and teaser transformers](diagrams/scott_connection_schematic.jpg)

**Main transformer:** Primary connected between phases A and B (full line voltage $V_{AB}$). Secondary provides one phase of the 2-phase output.

**Teaser transformer:** Primary connected from the midpoint (M) of the main transformer primary to phase C. The voltage from M to C:

$$V_{MC} = \frac{\sqrt{3}}{2} \times V_L$$

This is the height of the equilateral voltage triangle. The teaser primary needs $\frac{\sqrt{3}}{2} = 86.6\%$ of the main transformer turns.

**Why the outputs are 90° apart:**

![Scott connection phasor diagram showing 90° separation](diagrams/scott_connection_phasor.jpg)

$V_{AB}$ is a line voltage. $V_{MC}$ is perpendicular to $V_{AB}$ in the phasor diagram (midpoint M bisects AB, so MC is the perpendicular bisector). The two secondary voltages inherit this 90° separation. Result: balanced 2-phase output.

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Explain the Scott connection with necessary diagrams.
> **Appeared:** 2018 Q4(a) — 4 marks

**Full Answer:**

The Scott (T-T) connection converts 3-phase power to 2-phase power using two single-phase transformers.

**Two transformers required:**

**(1) Main transformer:** Standard transformer. Primary connected between two phases (e.g., A and B). Full line voltage $V_{AB}$ appears across its primary.

**(2) Teaser transformer:** Primary connected from the midpoint (M) of the main transformer primary to the third phase (C). Its primary has $\sqrt{3}/2 = 86.6\%$ of the main transformer's turns, because the voltage from midpoint M to C is $V_{MC} = (\sqrt{3}/2) V_L$ (the height of the equilateral voltage triangle).

**Why 90° separation:** In a balanced 3-phase system, the voltage from the midpoint of one line voltage to the third phase is always perpendicular to that line voltage. $V_{AB}$ is horizontal in the phasor diagram, $V_{MC}$ is vertical. The two secondaries inherit this 90° separation, producing a balanced 2-phase output.

**Applications:** Electric arc furnace power supplies, powering 2-phase induction motors, converting 2-phase to 3-phase (reverse operation is possible because transformers are reciprocal devices).

---

### 🎯 Q2: Can you convert 3-phase to 2-phase or vice versa? If yes, explain.
> **Appeared:** 2019 Q4(b) — 4 marks

**Full Answer:**

Yes. This is done using the **Scott (T-T) connection.**

Two single-phase transformers are needed:

**(1) Main transformer:** Primary connected between two phases of the 3-phase supply (e.g., lines A and B). Secondary provides one phase of the 2-phase output.

**(2) Teaser transformer:** Primary connected from the mid-point of the main transformer primary to the third line (C). The teaser primary has $\sqrt{3}/2$ (86.6%) of the main transformer's turns. Secondary provides the second phase of the 2-phase output, exactly 90° displaced from the first.

**Why it works:** The two primary voltages are 90° apart geometrically in the phasor diagram. The line-to-midpoint voltage ($V_{MC}$) is perpendicular to the line-to-line voltage ($V_{AB}$) in a balanced 3-phase system. This 90° separation transfers to the two secondary voltages, giving a balanced 2-phase output.

**Reverse (2-phase to 3-phase):** Connect the two-phase supply to the secondaries. The 3-phase supply comes from the primaries. The same transformation works in reverse because transformers are reciprocal devices.

---

### 🎯 Q3: Two T-connected transformers supply 440V, 33 kVA balanced load from 3300V 3-phase. Find ratings.
> **Appeared:** 2018 Q4(b) — 4 marks, **repeated verbatim as 2024 Q4(c) — 4 marks**

**Full Answer:**

The exam asks for two T-connected transformers supplying a balanced 3-phase load from a 3-phase supply (T-T connection):
Given: Supply $V_{1L} = 3300\text{ V}$ (3-phase). Load: $V_{2L} = 440\text{ V}$, $S = 33\text{ kVA}$ (3-phase balanced).

**Step 1: Primary and secondary line currents**

$$I_{1L} = \frac{S}{\sqrt{3} V_{1L}} = \frac{33000}{\sqrt{3} \times 3300} = \frac{10}{\sqrt{3}} = \boxed{5.77\text{ A}}$$

$$I_{2L} = \frac{S}{\sqrt{3} V_{2L}} = \frac{33000}{\sqrt{3} \times 440} = \boxed{43.30\text{ A}}$$

**Step 2: Main transformer ratings**
- The main transformer primary is connected across lines A and B:
  $$V_{1,\text{main}} = V_{1L} = 3300\text{ V}$$
- The primary carries full line current $I_{1L} = 5.77\text{ A}$.
- Main transformer secondary voltage: $V_{2,\text{main}} = V_{2L} = 440\text{ V}$ carrying $I_{2L} = 43.30\text{ A}$.
- Operating rating of Main transformer:
  $$\text{Rating}_{\text{main}} = 3300\text{ V} \times 5.77\text{ A} = \boxed{19.05\text{ kVA}}$$

**Step 3: Teaser transformer ratings**
- The teaser transformer primary is connected from the midpoint of AB to line C:
  $$V_{1,\text{teaser}} = \frac{\sqrt{3}}{2} V_{1L} = 0.866 \times 3300 = \boxed{2858\text{ V}}$$
- The teaser primary carries line current $I_{1L} = 5.77\text{ A}$.
- Teaser secondary voltage: $V_{2,\text{teaser}} = \frac{\sqrt{3}}{2} V_{2L} = 0.866 \times 440 = 381\text{ V}$ carrying $I_{2L} = 43.30\text{ A}$.
- Operating rating of Teaser transformer:
  $$\text{Rating}_{\text{teaser}} = 2858\text{ V} \times 5.77\text{ A} = \boxed{16.50\text{ kVA}}$$

**Step 4: Total installed capacity**
- Combined operating capacity: $19.05 + 16.50 = 35.55\text{ kVA}$.
- In practice, two identical interchangeable transformers are used. Each must be sized for the larger rating ($19.05\text{ kVA}$):
  $$\text{Total installed capacity} = 2 \times 19.05 = \boxed{38.10\text{ kVA}}$$
- Ratio of installed capacity to load: $38.10 / 33 = 1.155$ (giving the classic **15.5% oversize** of the T-T connection).

> [!WARNING] Common Exam Trap: Why Main is 19.05 kVA, Not 16.5 kVA
> Do not divide total power simply as $33/2 = 16.5\text{ kVA}$ for the main transformer. 
> The teaser current ($5.77\text{ A}$) enters the neutral tap of the main primary and splits equally ($2.885\text{ A}$ each way) in quadrature with the main load current ($5.0\text{ A}$). 
> Phasor addition in each half of the main winding: $\sqrt{5.0^2 + 2.885^2} = 5.77\text{ A}$. 
> Thus the main winding carries full line current $5.77\text{ A}$, making its required rating $3300 \times 5.77 = 19.05\text{ kVA}$.

---

## ⚡ Exam Tips & Common Mistakes

1. **Teaser has $\sqrt{3}/2$ = 86.6% turns, not 50%.** This is the most common error.
2. **Both transformers have the same kVA rating.** The teaser has fewer turns but higher current.
3. **The 90° comes from geometry, not from any special winding.**

## 🔗 Related Topics

- [T-07a: 3-Phase Connections](T-07a_3Phase_Connections.md) — Standard 3-phase configurations
- [T-10: Auto-Transformer](T-10_Auto_Transformer.md) — Another special transformer type

---

[← T-07b: Open Delta](T-07b_Open_Delta.md) | [🏠 Index](00_Index.md) | [T-09: Vector Groups →](T-09_Vector_Groups.md)
