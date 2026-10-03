[← T-14: IM as Rotating Transformer](T-14_IM_as_Rotating_Transformer.md) | [🏠 Index](README.md) | [T-16: Torque Equations & Curves →](T-16_Torque_Equations_and_Characteristics.md)

---

# T-15: IM Equivalent Circuit

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **IM Equivalent Circuit** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q3(a) / 2020 Q5(c)]
> 📋 **Appeared in:** 2017 Q3(a), 2020 Q5(c) (Years: 2017, 2020)
> - **2017 Q3(a)**: *"Draw the step-by-step equivalent circuit of a 3-φ induction motor. [03]"*
> - **2020 Q5(c)**: *"How can the equivalent circuit model of an induction motor be obtained? [06]"*

**1. Stator Model and Standstill Rotor ($s=1$):**
At standstill, the motor acts like a transformer. Stator has $R_1, X_1$ and shunt branch $R_c, X_m$. Rotor has $R_2$ and $X_2$ at frequency $f$.
![Step 1: Stator and rotor transformer model](diagrams/im_step1_transformer_model.png)

**2. Rotor at Running Slip $s$:**
Rotor frequency is $sf$, induced EMF is $sE_2$, and reactance is $sX_2$.
$$I_2 = \frac{sE_2}{R_2 + jsX_2}$$
![Step 2: Rotor circuit at slip s](diagrams/im_step2_rotor_slip_frequency.png)

**3. Frequency Transformation:**
Divide the current equation by $s$ to refer the rotor to stator frequency $f$:
$$I_2 = \frac{E_2}{R_2/s + jX_2}$$
The rotor resistance is modeled as a variable resistance $R_2/s$.
![Step 3: Frequency transformation](diagrams/im_step3_frequency_transformation.png)

**4. Power Separation:**
Split $R_2/s$ into actual copper loss and mechanical load components:
$$\frac{R_2}{s} = R_2 + R_2\left(\frac{1-s}{s}\right)$$
$R_2$ causes heat ($P_{cu}$), and $R_L = R_2(1-s)/s$ represents gross mechanical power ($P_m$).
![Step 4: Power separation](diagrams/im_step4_power_separation.png)

**5. Exact Equivalent Circuit (Referred to Stator):**
Refer rotor parameters to stator using turns ratio $a = N_1/N_2$:
$$R_2' = a^2R_2, \quad X_2' = a^2X_2, \quad R_L' = R_2'\left(\frac{1-s}{s}\right)$$
![Step 5: Exact Equivalent Circuit](diagrams/im_step5_exact_equivalent_circuit.png)

**6. Approximate Equivalent Circuit:**
Since stator voltage drop is small, the shunt branch can be shifted to the input terminals.
![Step 6: Approximate per-phase equivalent circuit](diagrams/im_step6_approximate_circuit.png)

---

![Approximate per-phase equivalent circuit of a three-phase induction motor referred to the stator, with the exciting branch at the input terminals and the rotor branch shown as R2'/s](diagrams/im_step6_approximate_circuit.png)

---

### [2023 Q6(b)]
> 📋 **Appeared in:** 2023 Q6(b)

**(b) Draw the equivalent circuit of an induction motor as a generalized transformer. [CO1, Marks: 03]**

![Induction motor represented as a generalized transformer, stator acting as the primary and the short-circuited rotor as the secondary](diagrams/im_step1_transformer_model.png)

An induction motor is a transformer whose secondary is free to rotate and is short-circuited on itself.

| Transformer | Induction motor |
|:---|:---|
| Primary winding | Stator winding |
| Secondary winding | Rotor winding |
| Secondary load impedance | Mechanical load on the shaft |
| Secondary open ($I_2 = 0$) | Rotor at synchronous speed ($s = 0$) |
| Secondary shorted | Rotor at standstill ($s = 1$) |

**The one difference.** In a transformer both windings see the same frequency. In an induction motor the rotor sees slip frequency $f_2 = s f$. So the rotor quantities become
$$E_{2r} = s E_2, \qquad X_{2r} = s X_2, \qquad R_2 \text{ unchanged}$$
$$I_{2r} = \frac{s E_2}{\sqrt{R_2^2 + (s X_2)^2}}$$

**Removing the frequency difference.** Divide numerator and denominator by $s$:
$$I_{2r} = \frac{E_2}{\sqrt{(R_2/s)^2 + X_2^2}}$$

The current is unchanged, but now every quantity is at supply frequency. The rotating machine has become an ordinary static transformer with its secondary resistance changed from $R_2$ to $R_2/s$.

![Exact per-phase equivalent circuit of the induction motor referred to the stator, in standard transformer form](diagrams/im_step5_exact_equivalent_circuit.png)

Splitting the rotor resistance shows where the power goes:
$$\frac{R_2}{s} = \underbrace{R_2}_{\text{rotor copper loss}} + \underbrace{R_2\left(\frac{1-s}{s}\right)}_{\text{gross mechanical power}}$$

---

### [2023 Q5(a)]
> 📋 **Appeared in:** 2023 Q5(a)

**(a) Draw the electrical equivalent circuit of an induction motor. Also draw the complete torque-speed curve of a 3-phase induction motor. [CO3, Marks: 03]**

**Equivalent circuit (per phase, referred to the stator).**

| Element | Meaning |
|:---|:---|
| $R_1, X_1$ | Stator resistance and leakage reactance |
| $R_0, X_0$ | Core loss resistance and magnetising reactance |
| $R_2', X_2'$ | Rotor resistance and standstill reactance, referred to stator |
| $R_2'/s$ | Rotor branch resistance under running conditions |
| $R_2'\left(\dfrac{1-s}{s}\right)$ | Fictitious resistance that carries the mechanical power |

The whole slip dependence sits in the single term $R_2'/s$. Splitting it as
$$\frac{R_2'}{s} = R_2' + R_2'\left(\frac{1-s}{s}\right)$$
separates the rotor copper loss from the gross mechanical power.

**Complete torque-speed curve.**

![Complete torque-speed characteristic of a three-phase induction machine covering the braking, motoring and generating regions](../Books/Theraja/Ch-34/diagrams/Ch-34_p34_fig32.jpg)

![Torque-speed characteristic under load showing locked-rotor torque, pull-up torque, breakdown torque and the full-load operating point](../Books/Theraja/Ch-34/diagrams/Ch-34_p29_fig22.jpg)

| Region | Speed | Slip | Machine action |
|:---|:---|:---|:---|
| Braking (plugging) | $-N_s < N < 0$ | $1 < s < 2$ | Brake |
| Motoring | $0 < N < N_s$ | $0 < s < 1$ | Motor |
| Generating | $N > N_s$ | $s < 0$ | Induction generator |

Key points on the motoring part: starting torque at $s = 1$, breakdown (maximum) torque at $s = s_{maxT} = R_2/X_2$, then a steep, nearly straight stable run from $T_{max}$ down to zero torque at $N_s$.

---

[← T-14: IM as Rotating Transformer](T-14_IM_as_Rotating_Transformer.md) | [🏠 Index](README.md) | [T-16: Torque Equations & Curves →](T-16_Torque_Equations_and_Characteristics.md)
