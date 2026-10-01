[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](README.md) | [T-23: 1-Phase Starting Methods →](T-23_Single-Phase_IM_Starting_Methods.md)

---

# T-22: Single-Phase IM Theory (DFRT)

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Single-Phase IM Theory (DFRT)** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2024 Q8(a)]
> 📋 **Appeared in:** 2017 Q4(a), 2018 Q8(a), 2019 Q8(b), 2020 Q8(c), 2021 Q7(a), 2023 Q8(a), 2024 Q8(a) (Years: 2017, 2018, 2019, 2020, 2021, 2023, 2024)

**(a) Explain the principle of operation of a 1-phase induction motor and why it is not self-starting (with double revolving field theory). [06, CO4]**

A single-phase induction motor has:
- One stator winding (main winding) carrying single-phase AC.
- A squirrel-cage rotor.

**Why it is not self-starting:**

A single-phase AC current creates a pulsating magnetic flux, not a rotating one:
$$\Phi = \Phi_m\sin\omega t$$

By the **double revolving field theory (Ferraris theorem):**

This pulsating field decomposes into two counter-rotating RMFs of equal magnitude $\Phi_m/2$:

$$\Phi = \underbrace{\frac{\Phi_m}{2}\sin(\omega t - \theta)}_{\text{Forward field}} + \underbrace{\frac{\Phi_m}{2}\sin(\omega t + \theta)}_{\text{Backward field}}$$

![Resolution of Alternating Flux into Two Oppositely Rotating Fluxes](../Books/diagrams/VK_Mehta_Fig_9_03.jpeg)

Each produces a torque on the squirrel-cage rotor:
- Forward field produces $T_f$ (positive)
- Backward field produces $T_b$ (negative)

**At standstill ($N = 0$):** Both fields see the same slip ($s = 1$). So $T_f = T_b$ and net torque $= 0$.

**When running (pushed to forward speed $N$):**
- Slip for forward field: $s_f = (N_s - N)/N_s$ (small)
- Slip for backward field: $s_b = (N_s + N)/N_s = 2 - s_f$ (close to 2)
- $T_f > T_b$ → motor continues running in the pushed direction.

![Torque-Speed Characteristic Under Double-Field Revolving Theory showing zero net starting torque](../Books/diagrams/VK_Mehta_Fig_9_04.jpeg)

**Conclusion:** Zero starting torque → not self-starting. The motor needs a starting mechanism.

---

[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](README.md) | [T-23: 1-Phase Starting Methods →](T-23_Single-Phase_IM_Starting_Methods.md)
