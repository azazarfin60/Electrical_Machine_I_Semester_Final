[← T-01: Fundamentals & EMF](T-01_Transformer_Fundamentals_and_EMF_Equation.md) | [🏠 Index](README.md) | [T-03: No-Load & Phasors →](T-03_No-Load_Operation_and_Phasor_Diagrams.md)

---

# T-02: Transformer Construction & Core

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Transformer Construction & Core** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2019 Q3(b)]
> 📋 **Appeared in:** 2019 Q3(b)

**(b) "A considerable economy is achieved in core material if the middle phase winding of a 3-phase shell-type transformer is wound in the reverse direction." Justify. [04]**

In a 3-phase shell-type transformer, three single-phase cores are placed side by side. The flux in the middle limb is the vector sum of the fluxes from the two outer limbs.

For a balanced 3-phase system: $\Phi_A + \Phi_B + \Phi_C = 0$ at every instant.

If the middle phase (B) is wound in the **same** direction as A and C: the middle yoke carries the flux from both A and C passing through it. The cross-section must be larger.

If the middle phase (B) is wound in the **reverse** direction: effectively $\Phi_B$ is now $-\Phi_B$, which equals $\Phi_A + \Phi_C$. The flux in the middle limb equals the sum of A and C (with appropriate sign), meaning the yoke cross-section can be reduced because the net flux sharing is more symmetric and the yokes carry only the flux from adjacent limbs.

**Economy:** The two outer yokes carry only the flux from one outer phase each. Only the middle limb must carry the combined flux. With reverse winding, the mutual cancellation reduces peak yoke flux. Less core material is needed for the same performance.

![Shell-type transformer core structure and coils](../Books/Theraja/Ch-32/diagrams/Ch-32_p05_fig10.jpg)

---

### [2020 Q1(a)]
> 📋 **Appeared in:** 2020 Q1(a)

**(a) What is the purpose of laminating the core in a transformer? [02]**

The iron core sits in an alternating magnetic field. This induces EMFs in the core itself, driving circulating currents called eddy currents. These currents cause $I^2R$ heating and waste energy.

Laminating the core (cutting it into thin sheets insulated from each other) breaks the low-resistance path for eddy currents. Each lamination has high resistance across its thickness. So eddy currents are confined to each thin sheet. Since power loss $\propto t^2$ (lamination thickness), thin laminations drastically reduce eddy current losses.

![Core laminations assembled in staggered joints to reduce eddy current loss](../Books/Theraja/Ch-32/diagrams/Ch-32_p02_fig02.jpg)

Typical lamination thickness: 0.3–0.5 mm for power frequency (50/60 Hz) transformers.

---

### [Practice: Leakage Flux and Its Effect]
> **Practice problem (not from a past paper)**

**Explain leakage flux and its effect on transformer operation. Include a schematic.**

**Three types of flux:**
- $\Phi_M$ (or $\Phi_m$): Mutual flux through the iron core linking both primary and secondary windings. Transfers power.
- $\Phi_{\ell p}$ (or $\Phi_{l1}$): Primary leakage flux, linking only primary turns $N_1$, completing its path through air.
- $\Phi_{\ell s}$ (or $\Phi_{l2}$): Secondary leakage flux, linking only secondary turns $N_2$, completing its path through air.

**Schematic:**

![Schematic of transformer showing mutual flux and primary/secondary leakage fluxes](../SlidesByMaam/diagrams/L-10_ECE-2107_p04_fig01.jpg)

**Effects on operation:**

1. **Leakage reactances:** Leakage flux $\Phi_{l1} \propto I_1$ (air path, constant permeability). It induces a self-EMF lagging the current by 90°. It appears as a series reactance:
   $$X_1 = 2\pi f L_{l1}, \quad X_2 = 2\pi f L_{l2}$$
2. **Voltage equations with leakage:**
   $$V_1 = E_1 + I_1 R_1 + jI_1 X_1$$
   $$E_2 = V_2 + I_2 R_2 + jI_2 X_2$$
3. **Worsened voltage regulation:** under lagging pf load, the reactive drop $jI_2X_2$ reduces $V_2$.
4. **Fault current limiting (beneficial):** the short-circuit fault current is limited by $X_{01} = X_1 + X_2'$.

---

[← T-01: Fundamentals & EMF](T-01_Transformer_Fundamentals_and_EMF_Equation.md) | [🏠 Index](README.md) | [T-03: No-Load & Phasors →](T-03_No-Load_Operation_and_Phasor_Diagrams.md)
