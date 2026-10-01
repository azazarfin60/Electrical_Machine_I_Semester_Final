[← T-09: Vector Groups](T-09_Vector_Groups.md) | [🏠 Index](00_Index.md) | [T-11: Miscellaneous →](T-11_Miscellaneous_Transformer.md)

---

# T-10: Auto-Transformer
> **Section:** A | **Priority:** 🟡 MEDIUM | **Exam Frequency:** 3/7 years
> **Sources:** Theraja Ch-32 (Art. 32.37–32.40), VK Mehta Ch-7 (Art. 7.25–7.27), Slides L-11 S32

## Why This Topic Matters

The auto-transformer appeared in 3/7 papers (2020 three times). When it appears, it carries 3-4 marks per sub-question. The three standard question types are: (1) compare with 2-winding transformer, (2) prove copper saving = $(1-K)$, (3) list applications. The 2020 paper devoted 10 marks to auto-transformers alone.

---

## 📝 Key Definitions

> **Auto-transformer:** "An auto-transformer is a transformer with one winding only, part of the winding being common to both primary and secondary. Obviously, in an auto-transformer, the primary and secondary are not electrically isolated from each other as is the case with a 2-winding transformer. However, its theory and operation are similar to those of a two-winding transformer." — VK Mehta, Art. 7.25

> **Transformation ratio ($K$):** "$K = V_2/V_1 = N_2/N_1$. For step-down: $K < 1$. The closer $K$ is to 1, the greater the copper saving." — VK Mehta

---

## How an Auto-Transformer Works

![Auto-transformer step-down and step-up connections](diagrams/auto_transformer_connections.jpg)

In a regular 2-winding transformer, primary and secondary are electrically isolated. In an auto-transformer, there is **no isolation**. The secondary is part of the primary winding.

**Step-down auto-transformer:** The full winding ($N_1$ turns) connects to the supply. A tap at $N_2$ turns provides the output. Current in the common section is $(I_2 - I_1)$, which is smaller than $I_2$.

---

## Comparison with Two-Winding Transformer

| Feature | Two-Winding | Auto-Transformer |
|:---|:---|:---|
| Windings | Two separate, isolated | Single winding with tap |
| Electrical isolation | Yes | No |
| Copper required | More | Less (saving = $1-K$) |
| Efficiency | Slightly lower | Higher (direct conduction) |
| Size and weight | Larger | Smaller, lighter |
| Cost | Higher | Lower |
| Voltage ratio | Any ratio practical | Best for close ratios ($K \approx 1$) |
| Short-circuit current | Limited by leakage | Higher (less impedance) |

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Compare two-winding transformer and auto-transformer.
> **Appeared:** 2020 Q2(a) — 3 marks

**Full Answer:**

| Feature | Two-Winding Transformer | Auto-Transformer |
|:---|:---|:---|
| **Construction** | Two separate, electrically isolated windings wound on a common core | Single winding with a tapping point, part common to both primary and secondary |
| **Electrical isolation** | Complete galvanic isolation between primary and secondary | No isolation. Primary and secondary are electrically connected. A fault on one side affects the other. |
| **Copper requirement** | Higher. Both windings need full copper for their respective currents. | Lower. Copper saving = $(1-K)$ fraction. For close ratios ($K \approx 1$), the saving is huge. |
| **Efficiency** | Slightly lower. All power transfers magnetically. | Higher. Part of the power transfers by direct electrical conduction (not through the magnetic field), reducing losses. |
| **Size and weight** | Larger (more copper, more core) | Smaller and lighter for the same VA rating |
| **Cost** | Higher | Lower |
| **Suitable voltage ratio** | Any ratio, including very high step-up/step-down | Best for close ratios ($K > 0.5$). At extreme ratios, the lack of isolation becomes a safety concern. |
| **Short-circuit current** | Limited by leakage impedance | Higher than a 2-winding transformer (less leakage). Protection must be more robust. |
| **Applications** | Power transmission (isolation needed), distribution | Motor starting (reduced voltage), variacs, inter-ties between close-voltage power systems |

---

### 🎯 Q2: Prove: copper saved in auto-transformer = $(1-K)$ times that of an ordinary transformer.
> **Appeared:** 2020 Q2(b), 2020 Q3(b) — 4 marks

**Full Answer:**

![Auto-transformer winding currents](diagrams/auto_transformer_currents.jpg)

**For a two-winding transformer** of rated $S = VI$: copper is proportional to total ampere-turns in both windings.

$$W_{\text{2-winding}} \propto N_1 I_1 + N_2 I_2$$

Since $N_1 I_1 = N_2 I_2$ (approximately):

$$W_{\text{2-winding}} \propto 2 N_1 I_1$$

**For an auto-transformer** with step-down ratio $K = N_2/N_1 < 1$:

- Series section ($N_1 - N_2$ turns) carries current $I_1$
- Common section ($N_2$ turns) carries current $(I_2 - I_1)$

Copper in auto-transformer:

$$W_{\text{auto}} \propto (N_1 - N_2) I_1 + N_2 (I_2 - I_1)$$

Since $N_1 I_1 = N_2 I_2$: we can write $N_2 I_2 = N_1 I_1$

$$W_{\text{auto}} \propto N_1 I_1 - N_2 I_1 + N_2 I_2 - N_2 I_1 = N_1 I_1 - 2N_2 I_1 + N_1 I_1 = 2I_1(N_1 - N_2)$$

**Ratio:**

$$\frac{W_{\text{auto}}}{W_{\text{2-winding}}} = \frac{2I_1(N_1 - N_2)}{2N_1 I_1} = 1 - \frac{N_2}{N_1} = 1 - K$$

Therefore: **Copper in auto-transformer = $(1-K)$ × copper in ordinary transformer.**

$$\boxed{\text{Copper saving} = K \times W_{\text{ordinary}}}$$

**Example:** For $K = 0.9$ (10% step-down): auto-transformer uses only $(1-0.9) = 10\%$ of the copper. Saves 90%. For $K = 0.5$ (50% step-down): saves only 50%.

---

### 🎯 Q3: Fields of application of auto-transformer.
> **Appeared:** 2020 Q4(a) — 3 marks

**Full Answer:**

1. **Starting of induction motors (auto-transformer starter):** Provides reduced voltage during starting to limit starting current, then switches to full voltage at running speed.
2. **Laboratory variacs (variable AC supply):** A continuously variable auto-transformer provides any voltage from 0 to rated (and often above rated) for testing.
3. **Power transmission inter-ties:** Close-voltage-ratio interconnections between two power systems (e.g., 400 kV / 345 kV). The small voltage difference means large copper savings.
4. **Railway traction:** Voltage boosters along the track (25 kV / 12.5 kV).
5. **Voltage stabilizers:** Automatic voltage regulators for consumer supply.
6. **Fluorescent lamp ballasts and dimmers:** Voltage adjustment for lighting circuits.

---

## ⚡ Exam Tips & Common Mistakes

1. **No electrical isolation.** This is the main disadvantage.
2. **Copper saving = $K$, not $(1-K)$.** The auto-transformer USES $(1-K)$ fraction of copper. It SAVES $K$ fraction.
3. **Best for close ratios.** When $K \approx 1$, savings are enormous.

## 🔗 Related Topics

- [T-01: Fundamentals](T-01_Transformer_Fundamentals.md) — Basic transformer principle
- [T-11: Miscellaneous](T-11_Miscellaneous_Transformer.md) — Other special transformer topics

---

[← T-09: Vector Groups](T-09_Vector_Groups.md) | [🏠 Index](00_Index.md) | [T-11: Miscellaneous →](T-11_Miscellaneous_Transformer.md)
