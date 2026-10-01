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
| Copper used | More | Less (saving = $1 - k$ fraction) |
| Efficiency | Slightly lower | Higher (part of power conducted directly) |
| Size/Weight | Larger | Smaller and lighter |
| Cost | Higher | Lower |
| Voltage ratio | Any ratio practical | Better for close ratios ($k \approx 1$) |
| Short-circuit current | Limited by leakage | Higher (less impedance) |
| Application | Power transmission, isolation needed | Starters, lab variacs, close-ratio power |

![Auto-transformer connections (Step-down and Step-up)](../Books/diagrams/Ch-32_p73_fig60.jpg)

---

### [2020 Q2(b)]
> 📋 **Appeared in:** 2020 Q2(b), 2020 Q3(b) (Years: 2020)

**(b) Prove: copper saved in auto-transformer = $(1-k)$ times that in ordinary transformer. [04]**

![Auto-transformer winding currents and copper distribution](../Books/diagrams/Ch-32_p74_fig61.jpg)

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

