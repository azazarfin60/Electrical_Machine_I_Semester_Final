[← T-06c: Efficiency](T-06c_Efficiency.md) | [🏠 Index](00_Index.md) | [T-07b: Open Delta →](T-07b_Open_Delta.md)

---

# T-07a: Three-Phase Transformer Connections
> **Section:** A | **Priority:** 🟡 MEDIUM | **Exam Frequency:** 2/7 years (connections) + 2/7 (Y-Y limitations)
> **Sources:** Theraja Ch-33, VK Mehta Ch-7 (Art. 7.31–7.33), Slides L-11 S03–S14

## Why This Topic Matters

Specific 3-phase connection questions appear in 2/7 papers (2018, 2024) as numericals and 2/7 papers (2021, 2023) as theory (Y-Y limitations). The real payoff is understanding context for Open-Delta (T-07b, 6/7 papers), vector groups (T-09), and parallel operation.

---

## 📝 Key Definitions

> **Three-phase transformer bank:** "Three-phase power can be transformed by using three single-phase transformers connected in a bank, or by using a single three-phase transformer. In either case, four types of connections are possible: Y-Y, Δ-Δ, Y-Δ, and Δ-Y." — VK Mehta, Art. 7.31

> **Y (Star) connection:** "In star connection, similar ends (or start ends) of the three windings are connected to a common point called the neutral. Line voltage = $\sqrt{3}$ × phase voltage. Line current = phase current." — Theraja, Ch-33

> **Δ (Delta) connection:** "In delta connection, the three windings are connected end-to-end in series to form a closed loop. Line voltage = phase voltage. Line current = $\sqrt{3}$ × phase current." — Theraja, Ch-33

---

## Four Standard Connections

| Connection | Primary | Secondary | Phase Shift | Line Voltage Ratio (turns ratio $a$) |
|:---|:---|:---|:---|:---|
| **Y-Y** | Star | Star | 0° | $a : 1$ |
| **Δ-Δ** | Delta | Delta | 0° | $a : 1$ |
| **Y-Δ** | Star | Delta | 30° lead | $\sqrt{3}a : 1$ (step-down) |
| **Δ-Y** | Delta | Star | 30° lag | $a : \sqrt{3}$ (step-up) |

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: What are the limitations of Y-Y connected transformers? How to overcome them?
> **Appeared:** 2021 Q3(a) — 3 marks, 2023 Q4(b) — 4 marks

**Full Answer:**

**Limitations:**

**1. Third harmonic voltage distortion.** The magnetizing current of a transformer is non-sinusoidal and contains third harmonics. In a Y-Y transformer without grounded neutral, third harmonic currents have no path to flow (they are zero-sequence currents that need a neutral return). As a result, third harmonic EMFs appear in the line-to-neutral voltages, causing waveform distortion and potentially dangerous overvoltages.

**2. Floating neutral problem.** Under unbalanced loads, the neutral point shifts. Different phases get different voltages. One phase may get dangerously high voltage while another gets low voltage.

**3. No phase shift.** Y-Y gives 0° phase displacement. This limits flexibility in interconnection with other transformer groups that have 30° shifts.

**Solutions:**

**(1) Connect the neutral to ground (4-wire system).** This allows zero-sequence (third harmonic) currents to flow through the ground path. Eliminates harmonic voltages in phase-to-neutral voltages.

**(2) Add a delta-connected tertiary winding.** The delta provides a closed circulating path for third harmonic currents. This suppresses harmonic voltages without requiring a grounded neutral.

**(3) Use Δ winding on at least one side (Y-Δ or Δ-Y connection).** The delta winding inherently provides a closed path for third harmonic currents, eliminating the problem.

---

### 🎯 Q2: 10 MVA, 11kV supply, through three Y-Δ transformers to a 230V load. Find kVA per transformer, voltage per coil, current per coil.
> **Appeared:** 2018 Q3(b) — 6 marks

**Full Answer:**

Given: Total $S = 10$ MVA = 10000 kVA. Primary: Y-connected at 11 kV line. Secondary: Δ-connected at 230V line.

**kVA per transformer:** Each transformer handles one-third:

$$S_{\text{each}} = \frac{10000}{3} = \boxed{3333.3 \text{ kVA}}$$

**Primary (Y-connected, 11kV line):**

In Y connection: $V_{\text{phase}} = V_{\text{line}}/\sqrt{3}$ and $I_{\text{phase}} = I_{\text{line}}$.

$$V_{1,\text{coil}} = \frac{11000}{\sqrt{3}} = \boxed{6351 \text{ V}}$$

$$I_{1,\text{coil}} = I_{1,\text{line}} = \frac{S_{\text{each}} \times 1000}{V_{1,\text{coil}}} = \frac{3333300}{6351} = \boxed{524.8 \text{ A}}$$

**Secondary (Δ-connected, 230V line):**

In Δ connection: $V_{\text{phase}} = V_{\text{line}}$ and $I_{\text{phase}} = I_{\text{line}}/\sqrt{3}$.

$$V_{2,\text{coil}} = V_{2,\text{line}} = \boxed{230 \text{ V}}$$

$$I_{2,\text{coil}} = \frac{S_{\text{each}} \times 1000}{V_{2,\text{coil}}} = \frac{3333300}{230} = \boxed{14492 \text{ A}}$$

Line current on secondary: $I_{2,\text{line}} = \sqrt{3} \times 14492 = 25095$ A.

---

### 🎯 Q3: Advantages of a transformer bank. Line voltage ratios for 10:1 turns ratio in different connections.
> **Appeared:** 2018 Q4(c) — 4 marks

**Full Answer:**

**Advantages of transformer bank (3 single-phase transformers instead of one 3-phase transformer):**
1. **Flexibility in maintenance:** Can disconnect/replace one transformer at a time without complete shutdown.
2. **Emergency operation:** If one transformer fails, the remaining two can operate in open-Δ (V-V) at 57.7% capacity. No complete outage.
3. **Expandability:** Can build up the bank in stages as load grows.
4. **Transportation:** Three smaller transformers are easier to transport than one large 3-phase unit.

**Line voltage ratios (turns ratio per phase = $a = 10:1$):**

| Connection | Phase ratio | Line Voltage Ratio |
|:---:|:---:|:---:|
| Y-Y | 10:1 | 10:1 |
| Δ-Δ | 10:1 | 10:1 |
| Δ-Y | 10:1 | $10:\sqrt{3}$ = 5.77:1 (step-up on secondary) |
| Y-Δ | 10:1 | $\sqrt{3} \times 10:1$ = 17.32:1 |
| Open-Δ | 10:1 | 10:1 (same as Δ-Δ but 57.7% capacity) |

---

## ⚡ Exam Tips & Common Mistakes

1. **Y: $V_{\text{phase}} = V_{\text{line}}/\sqrt{3}$, $I_{\text{phase}} = I_{\text{line}}$.** Δ: $V_{\text{phase}} = V_{\text{line}}$, $I_{\text{phase}} = I_{\text{line}}/\sqrt{3}$.
2. **Y-Δ and Δ-Y introduce a 30° phase shift.** Critical for parallel operation (must match vector groups).
3. **Each transformer in a bank handles $S_{\text{total}}/3$.**

## 🔗 Related Topics

- [T-07b: Open Delta](T-07b_Open_Delta.md) — What happens when one Δ-Δ transformer fails
- [T-09: Vector Groups](T-09_Vector_Groups.md) — Phase shifts from different connections
- [T-08: Scott Connection](T-08_Scott_Connection.md) — 3-phase to 2-phase conversion

---

[← T-06c: Efficiency](T-06c_Efficiency.md) | [🏠 Index](00_Index.md) | [T-07b: Open Delta →](T-07b_Open_Delta.md)
