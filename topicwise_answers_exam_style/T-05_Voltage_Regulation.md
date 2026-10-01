# T-05: Voltage Regulation

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Voltage Regulation** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2023 Q3(a)]
> 📋 **Appeared in:** 2019 Q2(b), 2023 Q3(a) (Years: 2019, 2023)

**(a) What is voltage regulation? Derive the expression for VR with neat phasor diagrams for lagging, unity, and leading pf loads. [08, CO1]**

**Voltage Regulation (VR):** The change in secondary terminal voltage from no-load to full-load, as a percentage of the rated full-load secondary voltage, with primary voltage held constant.

$$\text{VR\%} = \frac{V_{2,NL} - V_{2,FL}}{V_{2,FL}} \times 100\%$$

**Derivation (approximate formula):**

From the equivalent circuit, secondary terminal voltage referred to primary:
$$V_1 = V_2' + I_2'R_{01}\cos\phi_2 + I_2'X_{01}\sin\phi_2 + j(\ldots) \approx V_2' + I_2'(R_{01}\cos\phi_2 \pm X_{01}\sin\phi_2)$$

where $+$ for lagging, $-$ for leading.

No-load voltage: $V_{2,NL} \approx V_1/a = V_2'$

Full-load voltage: $V_{2,FL} = V_2'$

Using phasor:
$$\text{VR\%} \approx \frac{I_2(R_{01}\cos\phi + X_{01}\sin\phi)}{V_{2,\text{rated}}} \times 100 \quad \text{(lagging, positive)}$$

$$\text{VR\%} \approx \frac{I_2(R_{01}\cos\phi - X_{01}\sin\phi)}{V_{2,\text{rated}}} \times 100 \quad \text{(leading, can be negative)}$$

**Phasor diagrams for Voltage Regulation:**

![Phasor diagram for approximate voltage drop derivation on lagging load](../Books/diagrams/Ch-32_p26_fig35.jpg)
![Voltage drop phasor diagrams at (a) Unity power factor and (b) Leading power factor](../Books/diagrams/Ch-32_p26_fig36.jpg)

- **Lagging pf:** $V_2$ reference. $I_2$ lags $V_2$ by $\phi$. $V_1' = V_2 + I_2R_{02}\cos\phi + I_2X_{02}\sin\phi$. Here $|V_1'| > |V_2|$, so VR > 0.
- **Unity pf:** $I_2$ in phase with $V_2$. Drop is primarily $I_2R_{02}$. Small positive VR.
- **Leading pf:** $I_2$ leads $V_2$ by $\phi$. Reactive drop subtracts from resistive drop: $I_2R_{02}\cos\phi - I_2X_{02}\sin\phi$. Terminal voltage can rise with load (negative VR).

---

### [2023 Q3(b)]
> 📋 **Appeared in:** 2023 Q3(b)

**(b) 3300/220V, 50Hz, 50 kVA transformer. Winding resistance: primary = $3.96\,\Omega$, secondary = $0.0176\,\Omega$. Leakage reactance: primary = $15.8\,\Omega$, secondary = $0.07\,\Omega$. Find VR at 0.8 pf lagging. [04, CO1]**

**Turns ratio:** $a = 3300/220 = 15$

**Refer to primary:**
$$R_{01} = R_1 + a^2 R_2 = 3.96 + 225 \times 0.0176 = 3.96 + 3.96 = 7.92\,\Omega$$

$$X_{01} = X_1 + a^2 X_2 = 15.8 + 225 \times 0.07 = 15.8 + 15.75 = 31.55\,\Omega$$

**Rated primary current:**
$$I_1 = \frac{50000}{3300} = 15.15 \text{ A}$$

**VR at 0.8 pf lag ($\cos\phi = 0.8$, $\sin\phi = 0.6$):**
$$\text{VR\%} = \frac{I_1(R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100$$

$$= \frac{15.15(7.92 \times 0.8 + 31.55 \times 0.6)}{3300} \times 100$$

$$= \frac{15.15(6.336 + 18.93)}{3300} \times 100 = \frac{15.15 \times 25.266}{3300} \times 100$$

$$= \frac{382.78}{3300} \times 100 = \boxed{11.6\%}$$

