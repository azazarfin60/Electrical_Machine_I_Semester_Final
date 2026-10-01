[← T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) | [🏠 Index](README.md) | [T-06: OC/SC Tests & Efficiency →](T-06_OC-SC_Tests_Efficiency_and_Losses.md)

---

# T-05: Voltage Regulation

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Voltage Regulation** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Q2(b): Voltage regulation for lagging, unity, and leading loads

> 📋 **Appeared in:** 2019 Q2(b), 2023 Q3(a)

#### Physical understanding of each case

**Lagging pf load (inductive):**

The secondary current $I_2$ lags behind $V_2$. When you multiply the current by the leakage impedance drops:
- Resistive drop $I_2 R_2$: in phase with $I_2$: pulls $V_2$ down.
- Reactive drop $I_2 X_2$: 90° ahead of $I_2$: also pulls $V_2$ down (since $I_2$ already lags, the reactive drop adds to the voltage depression).

Net effect: Large voltage drop from $E_2$ to $V_2$. High VR%. The secondary voltage decreases significantly under load.

![Transformer voltage regulation phasor diagram showing impedance triangle and projection on terminal voltage](../Books/diagrams/Ch-32_p26_fig35.jpg)

**Unity pf load:**

$I_2$ is in phase with $V_2$. Reactive drop is 90° ahead of $I_2$, which means it's nearly perpendicular to $V_2$. When you add it as a phasor, it barely changes the magnitude of $V_1$: only a small trigonometric effect. VR% is positive but small.

**Leading pf load (capacitive):**

$I_2$ leads $V_2$. Now the reactive drop $jI_2 X_2$ is in a direction that actually adds voltage in phase with $E_2$. The secondary terminal voltage can actually be **higher** at full load than at no-load. VR% is negative. This is called voltage regulation improvement or boost.

![Voltage regulation phasor diagram under leading power factor conditions](../Books/diagrams/Ch-32_p26_fig36.jpg)

Capacitor banks on transmission lines exploit this exact principle: capacitive loads raise the voltage profile along the line.

---

[← T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) | [🏠 Index](README.md) | [T-06: OC/SC Tests & Efficiency →](T-06_OC-SC_Tests_Efficiency_and_Losses.md)
