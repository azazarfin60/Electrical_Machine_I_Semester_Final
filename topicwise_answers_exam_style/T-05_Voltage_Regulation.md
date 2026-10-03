[← T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) | [🏠 Index](README.md) | [T-06: OC/SC Tests & Efficiency →](T-06_OC-SC_Tests_Efficiency_and_Losses.md)

---

# T-05: Voltage Regulation

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Voltage Regulation** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2024 Q3(a)]
> 📋 **Appeared in:** 2019 Q2(b), 2024 Q3(a) (Years: 2019, 2024)

**(a) Define voltage regulation of transformer. [Marks: 02, CO: 1]**

**Voltage regulation (VR):** The change in secondary terminal voltage from no-load to full-load, expressed as a percentage of the full-load secondary terminal voltage, with the primary voltage held constant.

$$\text{VR\%} = \frac{V_{2,NL} - V_{2,FL}}{V_{2,FL}} \times 100\%$$

On open circuit $I_2 = 0$, so there are no winding drops and $V_{2,NL} = E_2$. Therefore
$$\text{VR\%} = \frac{E_2 - V_2}{V_2} \times 100\%$$

**Sign by load type:**

- **Lagging pf** (inductive): both $I_2R$ and $I_2X$ drops reduce $V_2$, so VR is positive and largest.
- **Unity pf**: only the resistive drop counts, so VR is small and positive.
- **Leading pf** (capacitive): the reactive drop boosts $V_2$ and can overcome $IR$. VR can be negative, meaning the terminal voltage rises on load. Capacitor banks exploit this.

**Physical cause.** Load current flows through the winding resistance and leakage reactance, producing an internal voltage drop. Supply voltage is fixed, so the terminal voltage must fall by that amount.

---

### [2023 Q4(c)]
> 📋 **Appeared in:** 2023 Q4(c)

**(c) A $3-\varphi$ transformer, ratio $33/6.6\text{ kV}$, $\Delta/\text{Y}$, 2-MVA has a primary resistance of $8\ \Omega$ per phase and a secondary resistance of $0.08\ \Omega$ per phase. The percentage impedance is 7%. Calculate the secondary voltage with rated primary voltage for full-load 0.75 p.f. lagging conditions. [CO1, Marks: 04]**

![Simplified series equivalent circuit used for the voltage drop calculation](diagrams/tx_step6_simplified_series_circuit.png)

**Step 1. Per-phase quantities.**
Primary is delta at 33 kV, so $V_{1,ph} = 33000\text{ V}$. Secondary is star at 6.6 kV line, so $V_{2,ph} = 6600/\sqrt{3} = 3810.5\text{ V}$. Full-load secondary current (star, line $=$ phase):
$$I_2 = \frac{2 \times 10^6}{\sqrt{3} \times 6600} = 174.95\text{ A}$$

**Step 2. Per-phase transformation ratio.**
$$K = \frac{3810.5}{33000} = 0.11547, \qquad K^2 = 0.013333$$

**Step 3. Total resistance referred to the secondary.**
$$R_{02} = R_2 + K^2 R_1 = 0.08 + 0.013333 \times 8 = 0.08 + 0.10667 = 0.1867\ \Omega$$

**Step 4. Total impedance from the 7% figure.**
$$Z_{02} = \frac{0.07 \times 3810.5}{174.95} = 1.5246\ \Omega$$

**Step 5. Leakage reactance.**
$$X_{02} = \sqrt{1.5246^2 - 0.1867^2} = \sqrt{2.3244 - 0.0348} = 1.5131\ \Omega$$

**Step 6. Voltage drop at 0.75 p.f. lagging.** $\cos\phi = 0.75$, $\sin\phi = \sqrt{1 - 0.5625} = 0.6614$:
$$\Delta V = 174.95\,(0.1867 \times 0.75 + 1.5131 \times 0.6614) = 174.95 \times 1.1409 = 199.6\text{ V per phase}$$

**Step 7. Secondary voltage on load.**
$$V_{2,ph} = 3810.5 - 199.6 = 3610.9\text{ V}, \qquad V_{2,\text{line}} = \sqrt{3} \times 3610.9 = 6254\text{ V}$$

$$\boxed{V_2 = 6254\text{ V} \approx 6.25\text{ kV (line)}, \quad \text{regulation} = 5.24\%}$$

> [!info] Percentage cross-check
> $\%R = (174.95 \times 0.1867/3810.5) \times 100 = 0.857\%$, so $\%X = \sqrt{7^2 - 0.857^2} = 6.947\%$.
> $\%\text{Reg} = 0.857 \times 0.75 + 6.947 \times 0.6614 = 5.24\%$, giving $V_2 = 6600(1 - 0.0524) = 6254\text{ V}$. Same answer.

---

### [Practice: VR Numerical from Windings]
> **Practice problem (not from a past paper)**

**(b) 3300/220V, 50Hz, 50 kVA transformer. Winding resistance: primary = $3.96\,\Omega$, secondary = $0.0176\,\Omega$. Leakage reactance: primary = $15.8\,\Omega$, secondary = $0.07\,\Omega$. Find VR at 0.8 pf lagging.**

**Turns ratio:** $a = 3300/220 = 15$

**Refer to primary:**
$$R_{01} = R_1 + a^2 R_2 = 3.96 + 225 \times 0.0176 = 3.96 + 3.96 = 7.92\,\Omega$$
$$X_{01} = X_1 + a^2 X_2 = 15.8 + 225 \times 0.07 = 15.8 + 15.75 = 31.55\,\Omega$$

**Rated primary current:**
$$I_1 = \frac{50000}{3300} = 15.15 \text{ A}$$

**VR at 0.8 pf lag ($\cos\phi = 0.8$, $\sin\phi = 0.6$):**
$$\text{VR\%} = \frac{I_1(R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100$$
$$= \frac{15.15(7.92 \times 0.8 + 31.55 \times 0.6)}{3300} \times 100$$
$$= \frac{15.15 \times 25.266}{3300} \times 100 = \boxed{11.6\%}$$

---

[← T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) | [🏠 Index](README.md) | [T-06: OC/SC Tests & Efficiency →](T-06_OC-SC_Tests_Efficiency_and_Losses.md)
