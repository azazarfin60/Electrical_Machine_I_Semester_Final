

[← T-09: Vector Groups & Parallel](T-09_Vector_Groups_and_Parallel_Operation.md) | [🏠 Index](README.md) | [T-11: Misc Transformer Topics →](T-11_Miscellaneous_Transformer_Topics.md)

---

# T-10: Auto-Transformer

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Auto-Transformer** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2020 Q2(a)]
> 📋 **Appeared in:** 2020 Q2(a)

**(a) Compare two-winding transformer and auto-transformer. [03]**

| Feature | Two-Winding Transformer | Auto-Transformer |
|:---|:---|:---|
| Windings | Two separate windings | Single winding with a tap |
| Isolation | Primary and secondary are electrically isolated | No galvanic isolation |
| Copper used | More | Less (copper used = $(1-k)$ of ordinary; saving = $k$ fraction) |
| Efficiency | Slightly lower | Higher (part of power conducted directly) |
| Size/Weight | Larger | Smaller and lighter |
| Cost | Higher | Lower |
| Voltage ratio | Any ratio practical | Better for close ratios ($k \approx 1$) |
| Short-circuit current | Limited by leakage | Higher (less impedance) |
| Application | Power transmission, isolation needed | Starters, lab variacs, close-ratio power |

![Auto-transformer connections (Step-down and Step-up)](../Books/Theraja/Ch-32/diagrams/Ch-32_p73_fig60.jpg)

---

### [2020 Q2(b)]
> 📋 **Appeared in:** 2020 Q2(b), 2020 Q3(b) (Years: 2020)

**(b) Prove: copper saved in auto-transformer = $(1-k)$ times that in ordinary transformer. [04]**

![Auto-transformer winding currents and copper distribution](../Books/Theraja/Ch-32/diagrams/Ch-32_p74_fig61.jpg)

For a two-winding transformer of rating $VA$, secondary voltage $V_2$, secondary current $I_2$:
- Total copper used $\propto$ total conductor volume $\propto N_1 I_1 + N_2 I_2$
- Since $N_1 I_1 = N_2 I_2 = S/V$ (approximate for ideal): copper $\propto 2 \cdot N \cdot I \propto$ total ampere-turns.

For an auto-transformer with $k = V_2/V_1$ (step-down, $k < 1$):

The common winding (shared section) carries current $(I_2 - I_1)$.
The series winding carries current $I_1$.

Copper in auto-transformer:
$$W_{auto} \propto N_1 I_1 + N_2(I_2 - I_1)$$

$$= N_1 I_1 + N_2 I_2 - N_2 I_1 = N_1 I_1(1 + \frac{N_2}{N_1}) - N_2 I_1$$

Since $N_1 I_1 = N_2 I_2$ (approximately):
$$W_{auto} \propto N_2(I_2 - I_1) + N_1 I_1 = \text{ampere-turns of common section + series section}$$

Ratio of copper used:
$$\frac{W_{auto}}{W_{ordinary}} = 1 - k$$

Therefore:
$$\text{Copper saved} = W_{ordinary} - W_{auto} = W_{ordinary} - (1-k) W_{ordinary} = \boxed{k \cdot W_{ordinary}}$$

Or equivalently: copper in auto-transformer is $(1-k)$ fraction of ordinary transformer copper. *(Proved)*

---

### [2020 Q4(a)]
> 📋 **Appeared in:** 2020 Q4(a)

**(a) Fields of application of auto-transformer. [03]**

1. **Starting of induction motors:** Reduced-voltage starting (auto-transformer starter).
2. **Laboratory variacs:** Variable voltage AC supplies for testing.
3. **Power transmission inter-ties:** Close-voltage-ratio interconnections between two power systems (e.g., 400kV/345kV).
4. **Railway traction:** 25kV/12.5kV boosters along the track.
5. **Voltage stabilizers:** Automatic voltage regulators for small consumers.
6. **Fluorescent lamp ballasts and dimmers:** Voltage adjustment.


---

### [2023 Q2(c)]
> 📋 **Appeared in:** 2020 Q2(b), 2023 Q2(c) (Years: 2020, 2023)

**(c) Prove that less copper is used in auto-transformer than in an ordinary transformer. [CO2, Marks: 03]**

![Auto-transformer winding currents: the common section carries the difference of primary and secondary currents](../Books/Theraja/Ch-32/diagrams/Ch-32_p74_fig61.jpg)

**Basis.** The weight of copper in a winding is proportional to (number of turns) $\times$ (current it carries), since turns fix the length and current fixes the cross-section:
$$W \propto N I$$

**Two-winding transformer.** It has two separate windings:
$$W_o \propto N_1 I_1 + N_2 I_2$$

**Auto-transformer (step-down, $N_1$ total turns, tapped at $N_2$).** It has one winding in two sections:
- Series section $AB$: $(N_1 - N_2)$ turns carrying $I_1$
- Common section $BC$: $N_2$ turns carrying $(I_2 - I_1)$

$$W_a \propto (N_1 - N_2) I_1 + N_2 (I_2 - I_1)$$

**Take the ratio.**
$$\frac{W_a}{W_o} = \frac{(N_1 - N_2)I_1 + N_2(I_2 - I_1)}{N_1 I_1 + N_2 I_2} = \frac{N_1 I_1 + N_2 I_2 - 2 N_2 I_1}{N_1 I_1 + N_2 I_2}$$

Now use the m.m.f. balance $N_1 I_1 = N_2 I_2$. The denominator becomes $2 N_1 I_1$ and the numerator becomes $2N_1 I_1 - 2 N_2 I_1$:
$$\frac{W_a}{W_o} = \frac{2 I_1 (N_1 - N_2)}{2 N_1 I_1} = 1 - \frac{N_2}{N_1} = 1 - K$$

$$\boxed{W_a = (1 - K)\,W_o \qquad \text{Saving of copper} = K \, W_o}$$

Since $0 < K < 1$ always, $W_a < W_o$. So an auto-transformer always uses less copper. The saving grows as $K \to 1$. For $K = 0.9$ the saving is 90%.

---

[← T-09: Vector Groups & Parallel](T-09_Vector_Groups_and_Parallel_Operation.md) | [🏠 Index](README.md) | [T-11: Misc Transformer Topics →](T-11_Miscellaneous_Transformer_Topics.md)
