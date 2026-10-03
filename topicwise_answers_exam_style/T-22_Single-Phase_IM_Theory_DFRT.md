[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](README.md) | [T-23: 1-Phase Starting Methods →](T-23_Single-Phase_IM_Starting_Methods.md)

---

# T-22: Single-Phase IM Theory (DFRT)

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Single-Phase IM Theory (DFRT)** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2023 Q7(c)]
> 📋 **Appeared in:** 2023 Q7(c)

**(c) Explain the double field revolving theory for the operation of $1-\varphi$ induction motor. [CO1, Marks: 03]**

**Statement.** Any alternating (pulsating) flux can be resolved into two rotating fluxes of equal magnitude, each half the peak of the pulsating flux, revolving in opposite directions at synchronous speed.

![Resolution of an alternating pulsating flux into two equal flux components rotating in opposite directions](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_03.jpeg)

**Mathematical form.** The single stator winding produces
$$\Phi = \Phi_m \cos\omega t$$

Write it as the sum of two counter-rotating vectors of magnitude $\Phi_m/2$:
$$\Phi = \underbrace{\frac{\Phi_m}{2}\angle{+\omega t}}_{\text{forward field } \Phi_f} + \underbrace{\frac{\Phi_m}{2}\angle{-\omega t}}_{\text{backward field } \Phi_b}$$

Their components across the winding axis always cancel. Their components along the axis always add to $\Phi_m \cos\omega t$. So the two rotating fields are an exact equivalent of the one pulsating field.

**Torque production.**

![Torque-speed curves of the forward field and the backward field, and the resultant curve showing zero net starting torque](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_04.jpeg)

Let the rotor turn at speed $N$. The two fields see different slips:
$$s_f = \frac{N_s - N}{N_s} = s \qquad \text{(forward field)}$$
$$s_b = \frac{N_s - (-N)}{N_s} = 2 - s \qquad \text{(backward field)}$$

Each field produces its own torque. The forward torque $T_f$ is positive, the backward torque $T_b$ is negative, and the net torque is
$$T = T_f - T_b$$

**At standstill ($N = 0$, $s = 1$):** both fields see the same slip of 1. So $T_f = T_b$ and
$$T_{st} = 0$$

$$\boxed{\text{A 1-}\varphi \text{ induction motor has zero starting torque and is not self-starting.}}$$

**Once it is turning:** suppose the rotor is pushed forward. Then $s < 1$ for the forward field and $2 - s > 1$ for the backward field. The forward torque grows and the backward torque shrinks. The net torque is positive and the motor runs up to near $N_s$. It keeps running in whichever direction it was started.

So a single-phase induction motor will run on its own but will not start on its own.

---

### [2024 Q6(b)]
> 📋 **Appeared in:** 2024 Q6(b)

**(b) Following step by step process, draw and describe the vector diagram of a 1-$\varphi$ IM. [Marks: 04, CO: 1]**

**Take the supply voltage $\vec{V}$ as the reference**, drawn horizontally to the right.

**Step 1 — Main winding.** $\vec{I}_m$ lags $\vec{V}$ by $\phi_m = \tan^{-1}(X_m/R_m)$, because the main winding is inductive. Draw $\vec{I}_m$ below $\vec{V}$ by that angle.

**Step 2 — Split the pulsating field into two counter-rotating fields.** By DFRT the field $\Phi_m \cos\omega t$ is equivalent to:
- a forward field of magnitude $\Phi_m/2$ rotating at $+N_s$
- a backward field of magnitude $\Phi_m/2$ rotating at $-N_s$

**Step 3 — Slips seen by the two fields.** For a rotor running forwards at speed $N$:
$$s_f = \frac{N_s - N}{N_s} = s, \qquad s_b = \frac{N_s + N}{N_s} = 2 - s$$

**Step 4 — Currents and torques.** Each field induces its own rotor current and hence its own torque. Both use the standard 3-$\varphi$ torque formula $T \propto \dfrac{sE_2^2 R_2}{R_2^2 + (sX_2)^2}$:
- forward: evaluate at $s_f = s$, which is small, so $T_f$ is large and in the forward direction
- backward: evaluate at $s_b = 2 - s$, which is well above 1 and therefore above $s_{maxT} = R_2/X_2$, so the backward torque is small and opposes rotation

**Step 5 — Net torque.** $T_{net} = T_f - T_b$ (shown as two opposite arrows).

**Step 6 — Starting point.** At $s = 1$: $s_f = s_b = 1$, so $T_f = T_b$ and
$$\boxed{T_{net} = 0 \text{ at standstill: the motor is not self-starting}}$$

**Step 7 — Running point.** As $N$ rises, $s_f$ falls towards 0 while $s_b$ rises towards 2, so $T_f$ grows and $T_b$ shrinks. The net torque becomes positive and the motor continues to run in the direction it was pushed.

![Torque-speed curves of the forward field and the backward field, and the resultant curve showing zero net starting torque](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_04.jpeg)

**Conclusion.** The backward field is the reason a 1-$\varphi$ motor cannot start itself, and the reason it runs at slightly lower speed and worse power factor than the forward field alone would give.
### [2024 Q8(a)]
> 📋 **Appeared in:** 2017 Q4(a), 2018 Q8(a), 2019 Q8(b), 2020 Q8(c), 2021 Q7(a), 2024 Q8(a) (Years: 2017, 2018, 2019, 2020, 2021, 2024)

**(a) Explain the principle of operation of a 1-phase induction motor and why it is not self-starting (with double revolving field theory). [Marks: 02, CO: 1]**

A single-phase induction motor has:
- One stator winding (main winding) carrying single-phase AC.
- A squirrel-cage rotor.

**Why it is not self-starting:**

A single-phase AC current creates a pulsating magnetic flux, not a rotating one:
$$\Phi = \Phi_m\sin\omega t$$

By the **double revolving field theory (Ferraris theorem):**

This pulsating field decomposes into two counter-rotating RMFs of equal magnitude $\Phi_m/2$:

$$\Phi = \underbrace{\frac{\Phi_m}{2}\sin(\omega t - \theta)}_{\text{Forward field}} + \underbrace{\frac{\Phi_m}{2}\sin(\omega t + \theta)}_{\text{Backward field}}$$

![Resolution of Alternating Flux into Two Oppositely Rotating Fluxes](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_03.jpeg)

Each produces a torque on the squirrel-cage rotor:
- Forward field produces $T_f$ (positive)
- Backward field produces $T_b$ (negative)

**At standstill ($N = 0$):** Both fields see the same slip ($s = 1$). So $T_f = T_b$ and net torque $= 0$.

**When running (pushed to forward speed $N$):**
- Slip for forward field: $s_f = (N_s - N)/N_s$ (small)
- Slip for backward field: $s_b = (N_s + N)/N_s = 2 - s_f$ (close to 2)
- $T_f > T_b$ → motor continues running in the pushed direction.

![Torque-Speed Characteristic Under Double-Field Revolving Theory showing zero net starting torque](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_04.jpeg)

**Conclusion:** Zero starting torque → not self-starting. The motor needs a starting mechanism.

---

[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](README.md) | [T-23: 1-Phase Starting Methods →](T-23_Single-Phase_IM_Starting_Methods.md)
