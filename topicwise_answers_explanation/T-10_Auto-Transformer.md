# T-10: Auto-Transformer

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Auto-Transformer** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Q3(b): Copper saving in auto-transformer: detailed analysis

> 📋 **Appeared in:** 2018 Q3, 2020 Q3(b)

#### Why some power doesn't need to be "transformed"

In a step-down auto-transformer ($k = V_2/V_1 < 1$):

The output voltage $V_2$ is present across the common winding (the lower section of the single winding). The series winding (top section) has voltage $V_1 - V_2$ across it.

The output current $I_2$ flows through the common winding. The series winding carries only $I_1$ (the primary current).

Power through the series winding: $P_{\text{series}} = (V_1 - V_2) \times I_1 = (1-k) \times V_1 I_1 = (1-k) S$

This is the power that must be **transformed magnetically**. The rest, $kS$, is conducted directly.

The copper needed for the windings is proportional to the VA to be handled:

**Series winding:** Handles $(1-k)$ fraction of full VA.
**Common winding:** Current $(I_2 - I_1) = I_2(1 - k)$, voltage $V_2$. VA $= V_2 \times I_2(1-k) = kS \times (1-k)/k = (1-k)S$.

Total copper in auto-transformer $\propto 2(1-k)S$. For ordinary transformer $\propto 2S$.

$$\frac{W_{auto}}{W_{ordinary}} = 1-k, \quad \text{Copper saved} = kS \times (\text{reference copper})$$

![Step-down and step-up autotransformer circuit schematics](../Books/diagrams/Ch-32_p73_fig60.jpg)

![Currents and voltages distribution in an autotransformer](../Books/diagrams/Ch-32_p74_fig61.jpg)

**When is auto-transformer best used?** When $k$ is close to 1 (small voltage step). For $k = 0.9$ (e.g., 415V/380V), copper saved is 90%. For $k = 0.5$ (220V/110V), only 50% saved: still worthwhile. For $k = 0.1$ (large ratio), only 10% saved: not economical.

---

## Induction Motor Topics

