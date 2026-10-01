[← T-14: IM as Rotating Transformer](T-14_IM_as_Rotating_Transformer.md) | [🏠 Index](README.md) | [T-16: Torque Equations & Curves →](T-16_Torque_Equations_and_Characteristics.md)

---

# T-15: IM Equivalent Circuit

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **IM Equivalent Circuit** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-15: Step-by-Step Derivation of the Induction Motor Equivalent Circuit

*Appears in: 2017 Q3(a), 2020 Q5(c)*

#### The physical challenge: different frequencies on stator and rotor

In a transformer, both primary and secondary windings operate at the identical electrical frequency $f$. 
In an induction motor, however, the stator operates at supply frequency $f$, but the rotor conductors rotate at mechanical speed $N$. The relative speed between the stator rotating magnetic field ($N_s$) and the rotor ($N$) is the slip speed $sN_s$. 

Consequently, the induced rotor EMF alternates at **slip frequency**:
$$f_r = s f$$

Because electrical circuits operating at different frequencies cannot be directly joined into a single equivalent mesh, we must convert the variable-frequency rotating rotor into a mathematically equivalent stationary circuit operating at the supply frequency $f$.

#### Step 1: Stator Model and Standstill Rotor (The Transformer Analogy at $s = 1$)
At standstill (locked rotor, slip $s = 1$), the rotor is stationary, and both stator and rotor operate at the supply frequency $f$. 
* The stator primary consists of winding resistance $R_1$, leakage reactance $jX_1$, and a parallel magnetizing branch ($R_c \parallel jX_m$) carrying no-load excitation current $I_0$ ($I_c$ for core loss and $I_m$ for air-gap magnetization).
* The stator induced EMF $E_1$ couples magnetically to the rotor standstill EMF $E_2$ across the air gap via an ideal transformer of effective turns ratio $a = N_1 / N_2$.
* The rotor winding has resistance $R_2$ and standstill leakage reactance $jX_2$, short-circuited on itself.

![Step 1: Stator and rotor transformer model at standstill](diagrams/im_step1_transformer_model.png)

---

#### Step 2: Rotor Circuit at Any Running Slip $s$ (Actual Rotor Frequency $f_r = s f$)
When the rotor rotates at mechanical speed $N$, the relative speed between the stator rotating magnetic field ($N_s$) and the rotor is $(N_s - N) = s N_s$. Consequently:
1. **Rotor induced EMF:** $E_r = s E_2$
2. **Rotor frequency:** $f_r = s f$
3. **Rotor leakage reactance:** $X_r = 2\pi f_r L_2 = 2\pi (sf) L_2 = s X_2$
4. **Rotor resistance:** $R_2$ remains constant (independent of slip).

The rotor current per phase at running slip $s$ is:
$$I_2 = \frac{E_r}{Z_r} = \frac{s E_2}{\sqrt{R_2^2 + (s X_2)^2}} = \frac{s E_2}{R_2 + j s X_2}$$

![Step 2: Rotor circuit at operating slip s](diagrams/im_step2_rotor_slip_frequency.png)

---

#### Step 3: Frequency Transformation to Stator Line Frequency $f$ (Variable Resistance Model)
Because the stator operates at frequency $f$ while the rotor operates at slip frequency $s f$, they cannot be coupled directly into a unified conductive circuit. 

Dividing both the numerator and denominator of the rotor current expression by slip $s$:
$$I_2 = \frac{\frac{s E_2}{s}}{\frac{R_2 + j s X_2}{s}} = \frac{E_2}{\frac{R_2}{s} + j X_2}$$

**Physical Significance:** 
* The induced EMF is now fixed at $E_2$ at constant line frequency $f$.
* The rotor leakage reactance is fixed at its standstill value $j X_2$ at frequency $f$.
* The rotor resistance becomes a variable fictitious resistance $\frac{R_2}{s}$, which reflects the effect of mechanical rotation.
* Both stator and rotor models now operate at the same supply frequency $f$.

![Step 3: Electrically equivalent rotor circuit at line frequency f](diagrams/im_step3_frequency_transformation.png)

---

#### Step 4: Separation of Rotor Power (Copper Loss vs. Mechanical Power Output)
The total electrical power transferred across the air gap into the rotor per phase ($P_g$, air-gap power) is:
$$P_g = I_2^2 \left(\frac{R_2}{s}\right)$$

We split the variable resistance $\frac{R_2}{s}$ into two components:
$$\frac{R_2}{s} = R_2 + R_2 \left(\frac{1 - s}{s}\right) = R_2 + R_L$$

* **$R_2$ (Constant):** Actual rotor winding resistance, which accounts for the internal rotor copper loss:
  $$P_{cu} = I_2^2 R_2$$
* **$R_L = R_2 \left(\frac{1 - s}{s}\right)$ (Variable):** Fictitious electrical load resistance representing the **gross mechanical power developed** by the rotor ($P_m$):
  $$P_m = I_2^2 R_L = I_2^2 R_2 \left(\frac{1 - s}{s}\right)$$

![Step 4: Rotor circuit separating copper loss and mechanical load](diagrams/im_step4_power_separation.png)

---

#### Step 5: Referring Rotor to Stator (Complete Exact Per-Phase Equivalent Circuit)
By referring all rotor quantities across the ideal transformer to the stator side using the effective transformation ratio $a = N_1 / N_2$ (where impedances scale by $a^2$ and currents by $1/a$):
* $E_2' = a E_2 = E_1$
* $I_2' = \frac{I_2}{a}$
* $R_2' = a^2 R_2$
* $X_2' = a^2 X_2$
* $R_L' = a^2 R_L = R_2' \left(\frac{1 - s}{s}\right)$
* Total rotor branch resistance: $\frac{R_2'}{s} = R_2' + R_L'$

The ideal transformer is eliminated, resulting in the **Complete Exact Per-Phase Equivalent Circuit**:

![Step 5: Complete exact per-phase equivalent circuit of 3-phase induction motor](diagrams/im_step5_exact_equivalent_circuit.png)

---

#### Step 6: Approximate Per-Phase Equivalent Circuit (Engineering Model)
Under normal load conditions, the stator impedance drop $I_1(R_1 + jX_1)$ is negligible ($\approx 2\text{--}5\%$). Shifting the shunt magnetizing branch ($R_c \parallel jX_m$) directly across the stator supply terminals $V_1$ simplifies calculation without substantial loss of accuracy:
* Total equivalent series resistance: $R_{01} = R_1 + R_2'$
* Total equivalent series leakage reactance: $X_{01} = X_1 + X_2'$
* Load resistance: $R_L' = R_2' \left(\frac{1 - s}{s}\right)$

![Step 6: Approximate per-phase equivalent circuit](diagrams/im_step6_approximate_circuit.png)

This complete per-phase model enables exact calculation of stator current, power factor, electromagnetic torque, developed power, and efficiency across the entire speed range.

---

[← T-14: IM as Rotating Transformer](T-14_IM_as_Rotating_Transformer.md) | [🏠 Index](README.md) | [T-16: Torque Equations & Curves →](T-16_Torque_Equations_and_Characteristics.md)
