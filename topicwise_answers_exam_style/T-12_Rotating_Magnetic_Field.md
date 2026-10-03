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

![3-Phase Supply Stator connection creating rotating magnetic field](../Books/Theraja/Ch-34/diagrams/Ch-34_p09_fig11.jpg)

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
> 📋 **Appeared in:** 2024 Q5(a)

**(a) Explain how a rotating field is produced when a balanced 3-$\varphi$ induction motor is connected to a balanced 3-$\varphi$ supply. [Marks: 03, CO: 3]**

![Three-phase sinusoidal flux waveforms and spatial flux axes](../Books/Theraja/Ch-34/diagrams/Ch-34_p09_fig12_13.jpg)

**The physical picture.** Three identical stator windings are placed $120°$ apart in space. They are fed with three sinusoidal currents that are $120°$ apart in time:

$$i_1 = I_m\sin\omega t, \qquad i_2 = I_m\sin(\omega t - 120°), \qquad i_3 = I_m\sin(\omega t - 240°)$$

Each winding on its own produces a **pulsating** flux along its own axis. But the three together behave as a single field whose axis keeps moving.

**Instant by instant.**

1. At $\omega t = 0°$: phase 1 current is zero, phases 2 and 3 carry equal and opposite currents. Their resultants add along the axis of phase 1.
2. At $\omega t = 60°$: the axis of the resultant has already turned through $60°$ toward phase 2.
3. At $\omega t = 120°$: the resultant lies on the axis of phase 2.
4. Over one cycle the axis sweeps through one full pole pair and returns to its start.

![Vector diagrams of resultant 3-phase flux at four instants showing rotation](../Books/Theraja/Ch-34/diagrams/Ch-34_p10_fig14.jpg)

**The magnitude is constant.** At every instant the resultant equals

$$\boxed{\Phi_r = \frac{3}{2}\Phi_m = 1.5\,\Phi_m}$$

and it turns at $\omega = 2\pi f$, so

$$N_s = \frac{120 f}{P}\ \text{rpm}$$

**Consequences.** The field has constant magnitude, so a constant torque is available, unlike the pulsating field of a single-phase winding. The rotor is dragged round at a speed just below $N_s$ (slip $s > 0$), because at exactly $N_s$ the flux would no longer cut the rotor and no current, hence no torque, would be produced. Reversing any two supply leads reverses the phase sequence, so the field, and therefore the rotor, turns the other way.

---

### [2023 Q5(c)]
> 📋 **Appeared in:** 2023 Q5(c)

**(c) Prove that, the magnitude of resultant flux is constant and equal to $\frac{3}{2}\Phi_m$, due to any phase in an induction motor of $3-\varphi$ stator supply system with necessary figures. [CO2, Marks: 04]**

**Setup.** Three identical stator windings are spaced $120°$ apart in space. They carry currents $120°$ apart in time, so each produces a pulsating flux along its own axis:

$$\Phi_1 = \Phi_m \sin \omega t, \qquad \Phi_2 = \Phi_m \sin(\omega t - 120°), \qquad \Phi_3 = \Phi_m \sin(\omega t - 240°)$$

![Three-phase stator layout, the sinusoidal phase flux waveforms, and the phasor positions at successive instants](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_8_06.jpeg)

**Phasor method, instant by instant.** Add the three flux phasors along their own space axes at four instants.

**(i) At $\omega t = 0°$:**
$$\Phi_1 = 0, \quad \Phi_2 = \Phi_m \sin(-120°) = -0.866\Phi_m, \quad \Phi_3 = \Phi_m \sin(-240°) = +0.866\Phi_m$$

The two non-zero fluxes are $60°$ apart in space. Their resultant bisects that angle:
$$\Phi_r = 2 \times 0.866 \Phi_m \cos\frac{60°}{2} = 2 \times 0.866 \times 0.866\, \Phi_m = \frac{3}{2}\Phi_m$$

**(ii) At $\omega t = 60°$:**
$$\Phi_1 = +0.866\Phi_m, \quad \Phi_2 = -0.866\Phi_m, \quad \Phi_3 = 0$$
$$\Phi_r = 2 \times 0.866 \Phi_m \cos 30° = \frac{3}{2}\Phi_m$$

The magnitude is unchanged, but the resultant has turned through $60°$.

**(iii) At $\omega t = 120°$ and (iv) at $\omega t = 180°$:** the same arithmetic repeats, each time giving $\Phi_r = \frac{3}{2}\Phi_m$ turned a further $60°$.

**Analytical proof.** Resolve all three along a reference axis and its quadrature:
$$\Phi_x = \Phi_1 + \Phi_2 \cos 120° + \Phi_3 \cos 240° = \frac{3}{2}\Phi_m \sin\omega t$$
$$\Phi_y = \Phi_2 \sin 120° + \Phi_3 \sin 240° = \frac{3}{2}\Phi_m \cos\omega t$$
$$\therefore\ \Phi_r = \sqrt{\Phi_x^2 + \Phi_y^2} = \frac{3}{2}\Phi_m \sqrt{\sin^2\omega t + \cos^2\omega t}$$

$$\boxed{\Phi_r = \frac{3}{2}\Phi_m = 1.5\,\Phi_m \ \text{(constant), rotating at } N_s = \frac{120f}{P}}$$

The direction angle is $\tan^{-1}(\Phi_y/\Phi_x) = (90° - \omega t)$, which decreases steadily with time. So the resultant is a constant-magnitude flux rotating at a uniform angular speed $\omega$. One full electrical cycle turns it through one pole pair.

---

[← T-11: Misc Transformer Topics](T-11_Miscellaneous_Transformer_Topics.md) | [🏠 Index](README.md) | [T-13: Slip & Sync Speed →](T-13_Slip_Synchronous_Speed_and_Basics.md)
