[← T-07a: 3-Phase Connections](T-07a_3Phase_Connections.md) | [🏠 Index](00_Index.md) | [T-08: Scott Connection →](T-08_Scott_Connection.md)

---

# T-07b: Open-Delta (V-V) Connection
> **Section:** A | **Priority:** 🔴 MUST | **Exam Frequency:** 7/7 years
> **Sources:** Theraja Ch-33 (Art. 33.8), VK Mehta Ch-7 (Art. 7.36), Slides L-11 S15–S18

## Why This Topic Matters

Open-Delta appeared in all 7 papers (2017, 2018, 2019, 2020, 2021, 2023, 2024). It ties with OC/SC test as the most repeated question in the entire exam. The question is almost always the same: "One transformer in a Δ-Δ bank fails. Show that 3-phase power can still be supplied. Prove the capacity reduces to 57.7%." This is a guaranteed 4-8 marks.

---

## 📝 Key Definitions

> **Open-Delta (V-V) connection:** "If one of the transformers in a Δ-Δ bank is damaged or removed, the remaining two transformers continue to supply 3-phase power. This is known as open-delta or V-V connection. The total kVA capacity reduces to $\sqrt{3}/3 = 57.7\%$ of the original closed-delta capacity." — VK Mehta, Art. 7.36

> **Utilization factor:** "In open-delta, each transformer operates at a power factor of $\cos 30° = 0.866$, not at unity. The utilization of each transformer is only $\sqrt{3}/2 = 86.6\%$ of its rated capacity." — VK Mehta

---

## Why 3-Phase Power Still Works

Start with three transformers in Δ-Δ: $T_{AB}$, $T_{BC}$, $T_{CA}$. Suppose $T_{CA}$ fails and is removed.

**On the primary side:** The 3-phase supply maintains all three line voltages. By KVL in the delta loop: $V_{CA} = -(V_{AB} + V_{BC})$. This voltage exists at the open terminals even without $T_{CA}$.

**On the secondary side:** $T_{AB}$ produces $V_{ab} = K \cdot V_{AB}$. $T_{BC}$ produces $V_{bc} = K \cdot V_{BC}$. By KVL: $V_{ca} = -(V_{ab} + V_{bc}) = K \cdot V_{CA}$. All three secondary line voltages are present and balanced.

**Result:** Balanced 3-phase power is delivered using only two transformers.

---

## The 57.7% Capacity Proof

Let each single-phase transformer be rated $S = VI$ (voltage $V$, current $I$).

**Closed Δ (3 transformers):** $S_{\text{closed}} = 3S$

**Open Δ (2 transformers):** Each transformer still operates at its rated $V$ and $I$. But for a balanced load, each transformer operates at $\cos 30°$ (not unity). The proof:

In open delta, the two remaining transformers must handle the full line current. The angle between each transformer's voltage and the current it carries is not 0° but ±30°.

$$S_{\text{open}} = 2 \times V \times I \times \cos 30° = 2VI \times \frac{\sqrt{3}}{2} = \sqrt{3} \times VI = \sqrt{3}S$$

$$\frac{S_{\text{open}}}{S_{\text{closed}}} = \frac{\sqrt{3}S}{3S} = \frac{1}{\sqrt{3}} = \boxed{0.577 = 57.7\%}$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: One transformer in a Δ-Δ bank is damaged. Show that 3-phase power can still be supplied and prove the capacity reduces to 57.7%.
> **Appeared:** 2023 Q3(a) — 4 marks, 2024 Q4(b) — 4 marks (plus 2017 Q7(a), 2018 Q3(c), 2019 Q4(a), 2020 Q4(b), 2021 Q3(b) in earlier papers)

**Full Answer:**

**Part 1: Why 3-phase power still reaches the load**

Consider three transformers $T_{AB}$, $T_{BC}$, $T_{CA}$ in Δ-Δ. Suppose $T_{CA}$ fails and is removed.

On the primary side: The 3-phase supply maintains $V_{AB}$ and $V_{BC}$. By KVL in the delta loop: $V_{CA} = -(V_{AB} + V_{BC})$. Even without $T_{CA}$, this voltage is present at the open terminals because it is imposed by the supply.

On the secondary side: $T_{AB}$ produces $V_{ab} = K \cdot V_{AB}$. $T_{BC}$ produces $V_{bc} = K \cdot V_{BC}$. By KVL: $V_{ca} = -(V_{ab} + V_{bc}) = K \cdot V_{CA}$. All three secondary line voltages exist and are balanced.

Three-phase balanced power is delivered by just two transformers. This configuration is called the **open-delta (V-V) connection**.

**Part 2: Capacity reduces to 57.7%**

Let each single-phase transformer be rated $S = VI$ kVA.

Closed-Δ total: $S_{\text{closed}} = 3 \times VI = 3S$

Open-Δ: Each transformer operates at rated $V$ and $I$. But for a balanced 3-phase load at unity pf, each transformer operates at effective power factor $\cos 30° = \sqrt{3}/2$ (due to the 30° phase displacement between transformer voltage and line current in the open configuration).

$$S_{\text{open}} = 2 \times VI \times \cos 30° = 2VI \times \frac{\sqrt{3}}{2} = \sqrt{3} \times VI = \sqrt{3}S$$

$$\text{Ratio} = \frac{S_{\text{open}}}{S_{\text{closed}}} = \frac{\sqrt{3}S}{3S} = \frac{1}{\sqrt{3}} = 0.577 = \boxed{57.7\%}$$

**Utilization factor** per transformer: $\sqrt{3}/2 = 86.6\%$ (each transformer delivers only 86.6% of its rated capacity).

---

### 🎯 Q2: Two 25 kVA transformers in Open-Δ: find maximum load without overloading, and load when third transformer closes the delta.
> **Appeared:** 2020 Q4(c) — 4 marks

**Full Answer:**

**(i) Open-Δ capacity:**

$$S_{\text{open}} = \sqrt{3} \times S_{\text{each}} = \sqrt{3} \times 25 = \boxed{43.3 \text{ kVA}}$$

Check: Each transformer handles 25 kVA. Two transformers at $\cos 30°$: $2 \times 25 \times 0.866 = 43.3$ kVA. ✓

**(ii) Closed-Δ capacity (third transformer added):**

$$S_{\text{closed}} = 3 \times S_{\text{each}} = 3 \times 25 = \boxed{75 \text{ kVA}}$$

Ratio: $43.3/75 = 0.577$ (confirms 57.7%).

### 🎯 Q3: Prove that closed-Δ kVA is $\sqrt{3}$ times higher than open-Δ kVA.
> **Appeared:** 2023 Q4(b) — 3 marks

**Full Answer:**

Let each single-phase transformer be rated at winding voltage $V$ and winding current $I$.

**Closed $\Delta$-Δ (three transformers).** In delta, $V_L = V_{ph} = V$ and $I_L = \sqrt{3} I_{ph} = \sqrt{3} I$:
$$S_{\Delta} = \sqrt{3}\, V_L I_L = \sqrt{3} \times V \times \sqrt{3} I = 3 V I$$

This is simply three times the rating of one transformer, as expected.

**Open $\Delta$ (V-V, two transformers).** Each winding sits directly in a line, so the line current cannot exceed the winding rating: $I_L = I$, $V_L = V$:
$$S_{V} = \sqrt{3}\, V_L I_L = \sqrt{3}\, V I$$

**Ratio.**
$$\frac{S_{\Delta}}{S_{V}} = \frac{3 V I}{\sqrt{3} V I} = \frac{3}{\sqrt{3}} = \sqrt{3}$$

$$\boxed{S_{\Delta} = \sqrt{3}\, S_{V} \qquad \text{or} \qquad S_{V} = 0.577\, S_{\Delta}}$$

**Numerical feel:** three 10 kVA units in $\Delta$-$\Delta$ give 30 kVA. Remove one and the two left give $\sqrt{3} \times 10 = 17.32$ kVA, which is $57.7\%$ of 30 kVA. Each of the two is then loaded to $17.32/2 = 8.66$ kVA, that is $86.6\%$ of its own 10 kVA.

---

---

## ⚡ Exam Tips & Common Mistakes

1. **Don't write $2S$ for Open-Δ capacity.** The capacity is $\sqrt{3}S$, not $2S$.
2. **The 57.7% is the ratio to the CLOSED delta capacity.** $\sqrt{3}S / 3S = 57.7\%$.
3. **KVL argument is essential.** Examiners want you to show WHY the third voltage still exists.
4. **This is an emergency configuration.** Not designed for permanent use.

## 🔗 Related Topics

- [T-07a: 3-Phase Connections](T-07a_3Phase_Connections.md) — The closed Δ-Δ configuration
- [T-09: Vector Groups](T-09_Vector_Groups.md) — Phase shifts in connections

---

[← T-07a: 3-Phase Connections](T-07a_3Phase_Connections.md) | [🏠 Index](00_Index.md) | [T-08: Scott Connection →](T-08_Scott_Connection.md)
