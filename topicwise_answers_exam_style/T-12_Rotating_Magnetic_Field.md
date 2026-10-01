[← T-11: Misc Transformer Topics](T-11_Miscellaneous_Transformer_Topics.md) | [🏠 Index](README.md) | [T-13: Slip & Sync Speed →](T-13_Slip_Synchronous_Speed_and_Basics.md)

---

# T-12: Rotating Magnetic Field

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Rotating Magnetic Field** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2019 Q5(a)]
> 📋 **Appeared in:** 2019 Q5(a)

**(a) What is an electrical machine? Describe the principle of operation of a 3-φ induction motor. [04]**

**Electrical machine:** A device that converts electrical energy to mechanical energy (motor) or mechanical energy to electrical energy (generator), using the principles of electromagnetic induction.

**3-φ IM operating principle:**
1. Three-phase balanced AC supply to stator creates a RMF of magnitude $1.5\Phi_m$ at synchronous speed $N_s = 120f/P$ rpm.
2. The RMF sweeps across stationary rotor bars. Relative motion induces EMF in rotor bars (Faraday's Law).
3. Induced EMF drives rotor current through short-circuited rotor bars.
4. Rotor current in the stator field produces Lorentz force (torque).
5. Rotor spins in the direction of RMF (Lenz's Law: to reduce relative motion).
6. Motor always runs at $N < N_s$ (slip $s > 0$), otherwise torque = 0.

![3-Phase Supply Stator connection creating rotating magnetic field](../Books/diagrams/Ch-34_p09_fig11.jpg)

---

### [2021 Q5(c)]
> 📋 **Appeared in:** 2021 Q5(c)

**(c) Show that 2-phase supply produces a rotating magnetic field at synchronous speed. [05]**

![Two-phase rotating magnetic field phasor vectors and space rotation](../ClassNoteByRaidah/diagrams/class04_fig02_twophase_rmf_phasors.jpg)

**Setup:** Two windings placed 90° apart in space. A balanced 2-phase supply:
$$i_a = I_m\sin\omega t, \qquad i_b = I_m\sin(\omega t - 90°) = -I_m\cos\omega t$$

Each winding produces a pulsating flux along its axis:
$$\Phi_a = \Phi_m\sin\omega t \quad \text{(along X-axis)}$$
$$\Phi_b = \Phi_m\sin(\omega t - 90°) = -\Phi_m\cos\omega t \quad \text{(along Y-axis)}$$

**Resultant flux:**

X-component: $\Phi_x = \Phi_a = \Phi_m\sin\omega t$

Y-component: $\Phi_y = \Phi_b = -\Phi_m\cos\omega t$

**Magnitude:**
$$\Phi_r = \sqrt{\Phi_x^2 + \Phi_y^2} = \sqrt{\Phi_m^2\sin^2\omega t + \Phi_m^2\cos^2\omega t} = \Phi_m = \text{constant}$$

**Space angle:**
$$\theta = \tan^{-1}\!\left(\frac{\Phi_y}{\Phi_x}\right) = \tan^{-1}\!\left(\frac{-\cos\omega t}{\sin\omega t}\right) = \omega t - 90°$$

$$\frac{d\theta}{dt} = \omega = 2\pi f \implies N_s = \frac{120f}{P} \text{ rpm}$$

**Conclusion:** The 2-phase supply produces a rotating field of constant magnitude $\Phi_m$ (not $1.5\Phi_m$ as in 3-phase), rotating at synchronous speed $N_s$. *(Proved)*

Note: Magnitude is $\Phi_m$ (not $1.5\Phi_m$) because 2-phase has only 2 phases, not 3.

---

### [2024 Q5(a)]
> 📋 **Appeared in:** 2017 Q1(b), 2018 Q6(b), 2024 Q5(a) (Years: 2017, 2018, 2024)

**(a) A 3-phase IM is connected to a balanced 3-phase supply. Prove that the resultant flux produced by the stator currents is constant in magnitude ($= 1.5\Phi_m$) and rotates at synchronous speed. [08, CO2]**

![Three-phase sinusoidal flux waveforms and spatial flux axes](../Books/diagrams/Ch-34_p09_fig12_13.jpg)
![Vector diagrams of resultant 3-phase flux at four instants showing rotation](../Books/diagrams/Ch-34_p10_fig14.jpg)

**Setup:** Stator windings 120° apart in space. Balanced 3-phase supply:
$$\Phi_R = \Phi_m\sin\omega t, \quad \Phi_Y = \Phi_m\sin(\omega t - 120°), \quad \Phi_B = \Phi_m\sin(\omega t + 120°)$$

**Resolve into X (horizontal) and Y (vertical) components:**

Take R-phase axis as +X. Y-phase axis is at 120° from X. B-phase axis is at 240° from X.

**X-component:**
$$\Phi_x = \Phi_R(1) + \Phi_Y\cos 120° + \Phi_B\cos 240°$$
$$= \Phi_m\sin\omega t + \Phi_m\sin(\omega t - 120°)(-\tfrac{1}{2}) + \Phi_m\sin(\omega t + 120°)(-\tfrac{1}{2})$$

Using $\sin(A-B) + \sin(A+B) = 2\sin A\cos B$:
$$= \Phi_m\sin\omega t - \frac{1}{2}\Phi_m \cdot 2\sin\omega t\cos 120° = \Phi_m\sin\omega t - \frac{1}{2}\Phi_m \cdot 2\sin\omega t \cdot (-\frac{1}{2})$$
$$= \Phi_m\sin\omega t + \frac{1}{2}\Phi_m\sin\omega t = \frac{3}{2}\Phi_m\sin\omega t$$

**Y-component:**
$$\Phi_y = \Phi_Y\sin 120° + \Phi_B\sin 240°$$
$$= \Phi_m\sin(\omega t - 120°)\cdot\frac{\sqrt{3}}{2} + \Phi_m\sin(\omega t + 120°)\cdot(-\frac{\sqrt{3}}{2})$$
$$= \frac{\sqrt{3}}{2}\Phi_m[\sin(\omega t - 120°) - \sin(\omega t + 120°)]$$

Using $\sin(A-B) - \sin(A+B) = -2\cos A\sin B$:
$$= \frac{\sqrt{3}}{2}\Phi_m \cdot (-2\cos\omega t\sin 120°) = \frac{\sqrt{3}}{2}\Phi_m \cdot (-2\cos\omega t \cdot \frac{\sqrt{3}}{2}) = -\frac{3}{2}\Phi_m\cos\omega t$$

**Magnitude:**
$$\Phi_r = \sqrt{\Phi_x^2 + \Phi_y^2} = \sqrt{\left(\frac{3}{2}\Phi_m\right)^2(\sin^2\omega t + \cos^2\omega t)} = \boxed{\frac{3}{2}\Phi_m = 1.5\Phi_m = \text{constant}}$$

**Space angle:**
$$\theta = \tan^{-1}\!\left(\frac{\Phi_y}{\Phi_x}\right) = \tan^{-1}\!\left(\frac{-\cos\omega t}{\sin\omega t}\right) = \omega t - 90°$$

$$\frac{d\theta}{dt} = \omega = 2\pi f \implies N_s = \frac{120f}{P} \text{ rpm}$$

**Conclusion:** Resultant flux = $1.5\Phi_m$ (constant magnitude), rotating at synchronous speed $N_s$. *(Proved)*

---

[← T-11: Misc Transformer Topics](T-11_Miscellaneous_Transformer_Topics.md) | [🏠 Index](README.md) | [T-13: Slip & Sync Speed →](T-13_Slip_Synchronous_Speed_and_Basics.md)
