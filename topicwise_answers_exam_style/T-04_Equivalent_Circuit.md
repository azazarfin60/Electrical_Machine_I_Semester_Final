[← T-03: No-Load & Phasors](T-03_No-Load_Operation_and_Phasor_Diagrams.md) | [🏠 Index](README.md) | [T-05: Voltage Regulation →](T-05_Voltage_Regulation.md)

---

# T-04: Equivalent Circuit

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Equivalent Circuit** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q8(c)]
> 📋 **Appeared in:** 2017 Q8(c)

**(c) 200/400V step-up transformer, parameters referred to LV side: $R_{eq} = 0.15\,\Omega$, $X_{eq} = 0.37\,\Omega$, $R_c = 600\,\Omega$, $X_m = 300\,\Omega$. Load: 10A at 0.8 pf lag (secondary). Find: (i) primary current, (ii) secondary terminal voltage. [05]**

**Given:** Turns ratio $a = N_1/N_2 = 200/400 = 0.5$ (step-up), all parameters on LV (primary) side:
$R_{eq} = 0.15\,\Omega, \quad X_{eq} = 0.37\,\Omega, \quad R_c = 600\,\Omega, \quad X_m = 300\,\Omega$

Secondary load: $I_2 = 10\text{ A}$ at $\cos\phi_2 = 0.8\text{ lag}$ ($\sin\phi_2 = 0.6$).

**Load current referred to primary side:**
$$I_2' = \frac{I_2}{a} = \frac{10}{0.5} = 20\text{ A}$$

**Taking applied primary voltage as reference:**
The rating specifies applied primary voltage $V_1 = 200\text{ V}$, so $\vec{V}_1 = 200\angle 0°\text{ V}$.
$$\vec{I}_2' = 20\angle -36.87° = 20(0.8 - j0.6) = (16 - j12)\text{ A}$$

**(i) Primary current (including magnetizing branch):**
$$I_c = \frac{V_1}{R_c} = \frac{200}{600} = 0.333\text{ A (in phase with }V_1)$$
$$I_m = \frac{V_1}{X_m} = \frac{200}{300} = 0.667\text{ A (lagging }V_1\text{ by 90°)}$$

No-load excitation current:
$$\vec{I}_0 = I_c - jI_m = (0.333 - j0.667)\text{ A}$$

Total primary input current:
$$\vec{I}_1 = \vec{I}_0 + \vec{I}_2' = (0.333 - j0.667) + (16 - j12) = (16.333 - j12.667)\text{ A}$$
$$|I_1| = \sqrt{16.333^2 + 12.667^2} = \sqrt{266.77 + 160.45} = \sqrt{427.22} \approx \boxed{20.67\text{ A}}$$
$$\text{Primary pf} = \frac{16.333}{20.67} = 0.79\text{ lag}$$

**(ii) Secondary terminal voltage:**
The series impedance drop referred to the primary side at $\cos\phi_2 = 0.8\text{ lag}$:
$$\Delta V_1 = I_2'(R_{eq}\cos\phi_2 + X_{eq}\sin\phi_2) = 20(0.15 \times 0.8 + 0.37 \times 0.6) = 20(0.12 + 0.222) = 6.84\text{ V}$$

Referred secondary terminal voltage:
$$V_2' = V_1 - \Delta V_1 = 200 - 6.84 = 193.16\text{ V}$$

Actual secondary terminal voltage ($K = N_2/N_1 = 1/a = 2$):
$$V_2 = \frac{V_2'}{a} = 2 \times 193.16 = \boxed{386.3\text{ V}}$$

*(Note: On load, secondary terminal voltage drops to 386.3 V, about 13.7 V below the 400 V no-load rating. Setting $V_2 = 400\text{ V}$ would incorrectly assume an over-rated primary supply of 206.9 V).*

---

### [2020 Q1(b)]
> 📋 **Appeared in:** 2020 Q1(b)

**(b) Derive the equivalent circuit of a single-phase two-winding transformer. [04]**

**Step 1: Ideal transformer with no losses, no leakage:**
$$\frac{V_1}{V_2} = \frac{N_1}{N_2} = a, \qquad I_1 = \frac{I_2}{a}$$

**Step 2: Add core loss and magnetizing current (shunt branch):**
Primary draws no-load current $I_0 = I_c + jI_m$ even at no load.
- $I_c$ in phase with $V_1$: represented by $R_c = V_1/I_c$ in shunt.
- $I_m$ lags $V_1$ by 90°: represented by $X_m = V_1/I_m$ in shunt.

**Step 3: Add primary winding resistance and leakage reactance:**
Series elements $R_1$ and $jX_1$ on the primary side.

**Step 4: Refer secondary to primary:**
Replace $R_2$, $jX_2$ with $a^2 R_2 = R_2'$, $ja^2 X_2 = jX_2'$ on the primary side.

**Step 5: Final approximate equivalent circuit (shunt branch at input):**

$$V_1 \to [R_1 + jX_1 + R_2' + jX_2'] \to E_1$$

Shunt branch ($R_c \| jX_m$) connected across $V_1$.

For simplicity, combine series elements:
$$R_{01} = R_1 + R_2', \quad X_{01} = X_1 + X_2'$$

![Approximate equivalent circuit of transformer referred to primary](../Books/Theraja/Ch-32/diagrams/Ch-32_p29_fig40.jpg)

---

### [2020 Q3(c)]
> 📋 **Appeared in:** 2020 Q3(c)

**(c) Step-by-step equivalent circuit of a transformer referred to primary side. [05]**

**1. Ideal Transformer Core Model:**
Start with an ideal core (zero winding resistance, zero leakage flux, infinite permeability, zero core loss).
$$E_1 = aE_2, \quad I_1 = I_2/a \quad \text{where } a = N_1/N_2$$
![Step 1: Ideal Transformer Model](diagrams/tx_step1_ideal_transformer.png)

**2. Winding Resistances and Leakage Reactances:**
Add practical winding series resistance ($R_1, R_2$) and leakage reactance ($X_1, X_2$) on both sides.
$$V_1 = E_1 + I_1(R_1 + jX_1), \quad E_2 = V_2 + I_2(R_2 + jX_2)$$
![Step 2: Practical Windings with Resistance and Leakage Reactance](diagrams/tx_step2_winding_resistance_leakage.png)

**3. Core Excitation Shunt Branch:**
Add a parallel branch across $E_1$ to model core iron loss ($R_c$) and magnetizing reactance ($X_m$). The total no-load current is $I_0 = I_c + I_m$.
![Step 3: Complete Circuit Model with Physical Core Shunt Branch](diagrams/tx_step3_excitation_shunt_branch.png)

**4. Transferring Secondary to Primary (Exact Equivalent Circuit):**
To eliminate the ideal transformer, transfer secondary parameters to the primary using $a^2$:
$$R_2' = a^2R_2, \quad X_2' = a^2X_2, \quad V_2' = aV_2, \quad I_2' = I_2/a$$
![Step 4: Exact Equivalent Circuit](diagrams/tx_step4_exact_referred_to_primary.png)

**5. Approximate Equivalent Circuit:**
Since $I_0$ is small and the primary voltage drop $I_0(R_1+jX_1)$ is negligible, move the shunt branch to the primary terminals. The series impedances combine to $R_{01} = R_1 + R_2'$ and $X_{01} = X_1 + X_2'$.
![Step 5: Approximate Equivalent Circuit](diagrams/tx_step5_approximate_referred_to_primary.png)

---

### [Practice: Equivalent Circuit Referred to the Primary Side]
> **Practice problem (not from a past paper)**

**Obtain the equivalent circuit of a transformer referred to the primary side.**

**Referring secondary to primary:**
Replace all secondary quantities with primary-referred (primed) values:
$$R_2' = a^2 R_2, \quad X_2' = a^2 X_2, \quad E_2' = aE_2 = E_1, \quad Z_L' = a^2 Z_L$$

**Final equivalent circuit referred to primary:**
Series branch: $R_{01} = R_1 + R_2'$, $X_{01} = X_1 + X_2'$ (total series impedance).
Shunt branch: $R_c \| jX_m$ (at the primary terminals in the approximate circuit).

![Exact and approximate equivalent circuit referred to primary](../Books/Theraja/Ch-32/diagrams/Ch-32_p29_fig40.jpg)

In the approximate equivalent circuit the shunt branch is moved to the primary input terminals (before $R_1$, $X_1$). This simplifies calculation without significant error for most power transformers.

---

[← T-03: No-Load & Phasors](T-03_No-Load_Operation_and_Phasor_Diagrams.md) | [🏠 Index](README.md) | [T-05: Voltage Regulation →](T-05_Voltage_Regulation.md)
