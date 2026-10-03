[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](README.md) | [T-23: 1-Phase Starting Methods →](T-23_Single-Phase_IM_Starting_Methods.md)

---

# T-22: Single-Phase IM Theory (DFRT)

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Single-Phase IM Theory (DFRT)** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### IM-03: Double-Field Revolving Theory: Why 1-Phase IM is Not Self-Starting

*Appears in: 2018 Q8a, 2019 Q8b, 2020 Q8c, 2021 Q7a, 2023 Q7c, 2024 Q6b*

#### The problem with single-phase

A 3-phase motor works because three windings, spatially displaced and phase-displaced in time, create a smoothly rotating field. Remove two phases and you have a single-phase winding that creates a pulsating (not rotating) field.

A pulsating field is different from a rotating field. It alternates back and forth along one axis. The question is: can this pulsating field still drive a rotor?

#### Ferraris' key insight (1885)

Italian physicist Galileo Ferraris showed that any pulsating magnetic field can be decomposed into two equal counter-rotating fields.

Mathematically:
$$\Phi = \Phi_m\sin\omega t$$

Can be written as:
$$\Phi = \frac{\Phi_m}{2}\cos(\omega t - \alpha) + \frac{\Phi_m}{2}\cos(\omega t + \alpha)$$

where $\alpha$ is the spatial angle. The first term rotates forward (counter-clockwise, say), the second rotates backward (clockwise). Each has magnitude $\Phi_m/2$.

At any instant, the two counter-rotating phasors add up to give the original pulsating field along the axis.

![Double revolving field theory decomposition of pulsating stator flux into forward and backward rotating vectors](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_03.jpeg)

#### Effect on the rotor: at standstill

Consider the forward-rotating field $\Phi_f = \Phi_m/2$ rotating at $+N_s$.

For the squirrel-cage rotor at rest ($N = 0$): The forward field sees slip $s_f = (N_s - 0)/N_s = 1$.

This field induces rotor currents and produces a forward torque $T_f$. This is exactly like a 3-phase motor at standstill: with the rotor field at slip 1.

Now consider the backward-rotating field $\Phi_b = \Phi_m/2$ rotating at $-N_s$.

For a stationary rotor, the backward field also sees a slip of 1 (it moves at $-N_s$ relative to the ground, and the rotor is at rest, so relative speed $= N_s$).

The backward field produces a backward torque $T_b$, equal in magnitude to $T_f$ (same slip, same rotor impedance).

**Net torque at standstill:** $T = T_f - T_b = 0$.

No starting torque. The motor just sits there.

#### Once you give it a push

Suppose you push the rotor to speed $N$ in the forward direction.

**Forward field slip:** $s_f = (N_s - N)/N_s = s$ (say $s = 0.05$ for running speed)

**Backward field slip:** The backward field rotates at $-N_s$. The rotor is at $+N$. Relative speed $= -N_s - N = -(N_s + N)$. So:
$$s_b = \frac{N_s + N}{N_s} = 1 + (1-s) = 2 - s$$

For $s = 0.05$: $s_b = 1.95$.

Now look at the torque-slip curve:
- Forward field: slip = 0.05 (well below peak, in the high-torque stable region). $T_f$ is large.
- Backward field: slip = 1.95 (past the peak, in the low-torque unstable region). $T_b$ is small.

**Net torque $= T_f - T_b > 0$**: The motor keeps accelerating and reaches a stable running speed.

**Conclusion:**
- At standstill: $T_f = T_b$, net = 0. Motor cannot start itself.
- Once running: $T_f > T_b$, net forward torque. Motor maintains speed.
- The direction of running depends on which way you push. The motor "doesn't care" which direction: it will run in whatever direction it was started.

#### Quantitative torque expression

Combining forward and backward torques:
$$T = T_f(s) - T_b(2-s)$$

where:
$$T_f(s) = \frac{k_1 s}{R_2^2 + s^2X_2^2} \cdot R_2$$

$$T_b(2-s) = \frac{k_1(2-s)}{R_2^2 + (2-s)^2X_2^2} \cdot R_2$$

At $s = 1$: these two are equal. At $s < 1$ (forward rotation): $T_f > T_b$ in typical motors.

![Torque-speed characteristic of 1-phase induction motor based on double revolving field theory](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_04.jpeg)

---

### [2024 Q6(b)]: Step-by-Step Construction and Description of 1-$\varphi$ IM Vector Diagram

> 📋 **Appeared in:** 2024 Q6(b)

**(b) Following step by step process, draw and describe the vector diagram of a 1-$\varphi$ IM. [Marks: 04, CO: 1]**

#### Step-by-Step Construction of the Vector Diagram

Unlike a polyphase induction motor which produces a single steadily rotating magnetic field, a single-phase induction motor with a single stator winding establishes a pulsating stationary magnetic field $\Phi(t) = \Phi_m \cos\omega t$. 

In accordance with the **Double-Field Revolving Theory (DFRT)**, this pulsating field is resolved into two rotating vectors:
$$\Phi_f = \frac{\Phi_m}{2}\angle +\omega t \quad \text{(Forward rotating field at } +N_s\text{)}$$
$$\Phi_b = \frac{\Phi_m}{2}\angle -\omega t \quad \text{(Backward rotating field at } -N_s\text{)}$$

![Resolution of an alternating pulsating flux into two equal flux components rotating in opposite directions](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_03.jpeg)

#### Step-by-Step Process:

1. **Step 1: Reference Axis & Flux Resolution:**
   - Draw horizontal reference axis representing the physical winding axis.
   - At time $t = 0$, both forward vector $\vec{\Phi}_f$ and backward vector $\vec{\Phi}_b$ coincide along the positive horizontal axis, each having a constant magnitude of $\Phi_m / 2$.
   - At any time $t$, $\vec{\Phi}_f$ has rotated by an electrical angle $+\theta = +\omega t$ counter-clockwise, while $\vec{\Phi}_b$ has rotated by $-\theta = -\omega t$ clockwise.
   - The vertical quadrature components $(\frac{\Phi_m}{2}\sin\omega t - \frac{\Phi_m}{2}\sin\omega t)$ identically cancel to zero at every instant.
   - The horizontal components add arithmetically: $2 \times (\frac{\Phi_m}{2}\cos\omega t) = \Phi_m \cos\omega t$, perfectly reproducing the pulsating stator flux.

2. **Step 2: Slip Seen by the Two Rotating Fields:**
   - When the rotor runs at speed $N$ rpm in the forward direction:
     - **Forward Slip ($s_f$):** $s_f = \frac{N_s - N}{N_s} = s$
     - **Backward Slip ($s_b$):** Relative speed between backward field (turning at $-N_s$) and forward rotor (turning at $+N$) is $N_s - (-N) = N_s + N$. Thus:
       $$s_b = \frac{N_s + N}{N_s} = \frac{N_s + N_s(1 - s)}{N_s} = 2 - s$$

3. **Step 3: Induced Rotor EMFs and Currents:**
   - Each field independently cuts the squirrel-cage rotor bars and induces rotor currents:
     - Forward rotor current: $I_{2f} = \frac{s E_2}{\sqrt{R_2^2 + (s X_2)^2}}$
     - Backward rotor current: $I_{2b} = \frac{(2 - s) E_2}{\sqrt{R_2^2 + (2 - s)^2 X_2^2}}$

4. **Step 4: Developed Torques:**
   - Each field develops torque in its own direction of rotation:
     $$T_f = k \frac{s E_2^2 R_2}{R_2^2 + s^2 X_2^2} \quad \text{(Forward driving torque)}$$
     $$T_b = k \frac{(2 - s) E_2^2 R_2}{R_2^2 + (2 - s)^2 X_2^2} \quad \text{(Opposing backward torque)}$$
   - The resultant electromagnetic torque acting on the shaft is the algebraic difference:
     $$T_{\text{net}} = T_f - T_b$$

5. **Step 5: Standstill Condition ($N = 0 \implies s = 1$):**
   - At rest, $s_f = 1$ and $s_b = 2 - 1 = 1$.
   - Both forward and backward fields see identical slip ($s=1$), identical rotor impedance, and induce identical currents.
   - Therefore, $T_f = T_b \implies T_{\text{net}} = 0$.
   - **Conclusion:** The vector diagram rigorously demonstrates that a single-phase induction motor develops **zero starting torque** and is inherently not self-starting.

6. **Step 6: Running Condition ($N > 0 \implies s \ll 1$):**
   - Once given an initial mechanical push in the forward direction, $s \approx 0.03\text{–}0.05$.
   - Forward slip is tiny ($s_f = 0.04$), placing the forward operating point in the high-torque, predominantly resistive region ($T_f$ is large).
   - Backward slip is large ($s_b = 1.96$), placing the backward operating point far past the breakdown knee where high rotor inductive reactance suppresses current and power factor ($T_b$ is very small).
   - Consequently, $T_f \gg T_b$, yielding a strong positive net torque $T_{\text{net}} > 0$ that accelerates the motor to normal running speed.

![Torque-speed curves of the forward field and the backward field, with the resultant curve showing zero net torque at standstill](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_04.jpeg)

---

[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](README.md) | [T-23: 1-Phase Starting Methods →](T-23_Single-Phase_IM_Starting_Methods.md)
