[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](00_Index.md) | [T-23: 1-Phase IM Starting Methods →](T-23_1Phase_Starting_Methods.md)

---

# T-22: Double Revolving Field Theory (DFRT) & 1-Phase IM
> **Section:** B | **Priority:** 🔴 MUST | **Exam Frequency:** 7/7 years
> **Sources:** VK Mehta Ch-9 (Art. 9.1-9.4), Theraja Ch-35 (Art. 35.1), Slides L-08, L-09

## Why This Topic Matters

This question appeared in ALL 7 papers. It is the single most repeated topic in Section B. "Explain why a 1-phase IM is not self-starting using DFRT" appeared in 2017, 2018, 2019, 2020, 2021, 2023, and 2024. This is a guaranteed 5-6 mark question. Write it perfectly.

---

## 📝 Key Definitions

> **Double Revolving Field Theory (Ferraris Theorem):** "Any pulsating magnetic field can be resolved into two rotating fields, each having half the amplitude of the pulsating field. These two rotating fields revolve at synchronous speed in opposite directions." — VK Mehta, Art. 9.2

> **Single-Phase Induction Motor:** "A single-phase induction motor has one stator winding carrying single-phase AC and a squirrel-cage rotor. It produces a pulsating magnetic field, not a rotating one. It is NOT self-starting." — VK Mehta, Art. 9.1

---

## Why a 1-Phase IM is Not Self-Starting

### Step 1: Pulsating Field

A single-phase stator winding carrying AC current produces a pulsating flux:

$$\Phi = \Phi_m\sin\omega t$$

This field oscillates along one axis. It does not rotate.

### Step 2: Ferraris Decomposition (DFRT)

This pulsating field can be decomposed into two counter-rotating fields of equal magnitude:

$$\Phi = \underbrace{\frac{\Phi_m}{2}\sin(\omega t - \theta)}_{\text{Forward field } \Phi_f} + \underbrace{\frac{\Phi_m}{2}\sin(\omega t + \theta)}_{\text{Backward field } \Phi_b}$$

Both rotate at synchronous speed $N_s$: one forward, one backward.

![DFRT decomposition of pulsating flux into forward and backward components](diagrams/dfrt_pulsating_flux_split.jpeg)

### Step 3: At Standstill ($N = 0$)

For the rotor at rest:
- Forward field slip: $s_f = (N_s - 0)/N_s = 1$
- Backward field slip: $s_b = (N_s + 0)/N_s = 1$

Both fields see the same slip ($s = 1$). Both produce equal torques in opposite directions:

$$T_f = T_b \implies T_{\text{net}} = T_f - T_b = 0$$

**Zero net starting torque. The motor cannot start by itself.**

### Step 4: Once Given a Push

If the rotor is pushed to speed $N$ in the forward direction:

$$s_f = \frac{N_s - N}{N_s} = s \quad (\text{small, e.g., 0.05})$$

$$s_b = \frac{N_s + N}{N_s} = 2 - s \quad (\text{large, e.g., 1.95})$$

From the torque-slip curve:
- Forward field at small slip: $T_f$ is large (high torque, stable region)
- Backward field at slip $\approx 2$: $T_b$ is small (past the peak)

$$T_{\text{net}} = T_f - T_b > 0$$

The motor accelerates and reaches a stable running speed.

![Torque-speed characteristic showing forward, backward, and net torques](diagrams/dfrt_torque_speed.jpeg)

### Step 5: Direction is Arbitrary

If pushed backward, it runs backward. The motor does not care which direction it was started. Whatever direction it receives an initial push, it continues in that direction.

---

## Quantitative Torque Expression

$$T = T_f(s) - T_b(2-s)$$

$$T_f = \frac{k_1 s R_2}{R_2^2 + s^2X_2^2}, \qquad T_b = \frac{k_1 (2-s) R_2}{R_2^2 + (2-s)^2X_2^2}$$

At $s = 1$: $T_f = T_b$, net = 0. *(Not self-starting)*

At $s \approx 0.05$: $T_f \gg T_b$, net positive. *(Runs in forward direction)*

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Explain the principle of operation of a 1-phase IM and why it is not self-starting using DFRT.
> **Appeared:** 2017 Q4(a), 2018 Q8(a), 2019 Q8(b), 2020 Q8(c), 2021 Q7(a), 2023 Q8(a), 2024 Q8(a) — (5-6 marks)

**Full Answer:**

A single-phase IM has one stator winding carrying AC and a squirrel-cage rotor.

**The pulsating field:** AC through the stator winding creates a pulsating flux $\Phi = \Phi_m\sin\omega t$ along one axis. This is NOT a rotating field.

**Double Revolving Field Theory (Ferraris, 1885):** This pulsating field decomposes into two equal counter-rotating fields:

$$\Phi = \frac{\Phi_m}{2}\sin(\omega t - \theta) + \frac{\Phi_m}{2}\sin(\omega t + \theta)$$

Forward field $\Phi_f = \Phi_m/2$ rotates at $+N_s$. Backward field $\Phi_b = \Phi_m/2$ rotates at $-N_s$.

**At standstill ($N = 0$):** Both fields see slip = 1. Both produce equal torques:

$$T_f = T_b \implies T_{\text{net}} = 0$$

Motor cannot start itself. **Zero starting torque.**

**Once pushed to speed $N$:** Forward field slip = $s$ (small). Backward field slip = $2-s$ (large). From the torque-slip curve, $T_f \gg T_b$, so $T_{\text{net}} > 0$. The motor continues running.

**Conclusion:** A 1-phase IM is not self-starting because the forward and backward torques cancel at standstill. An auxiliary starting mechanism (capacitor, split phase, or shaded pole) is needed to create an initial asymmetry.

---

## Exam Variants

| Year | Question | Marks |
|:---|:---|:---|
| 2017 Q4(a) | 1-phase IM principle + why not self-starting | 5 |
| 2018 Q8(a) | Same (DFRT) | 6 |
| 2019 Q8(b) | Same (DFRT) | 5 |
| 2020 Q8(c) | Same (DFRT) | 5 |
| 2021 Q7(a) | Same (DFRT) | 5 |
| 2023 Q8(a) | Same (DFRT) + CO4 | 6 |
| 2024 Q8(a) | Same (DFRT) + CO4 | 6 |

---

## ⚡ Exam Tips & Common Mistakes

1. **This is a GUARANTEED question.** 7/7 years. Write it cleanly and earn full marks.
2. **Name Ferraris.** Mentioning "Ferraris theorem" shows you know the origin. Extra credit in some years.
3. **Show the math.** Write $s_f = 1$, $s_b = 1$ at standstill. Show $T_f = T_b$. Show $T_{\text{net}} = 0$.
4. **Draw the torque-speed diagram** if possible. Show $T_f$, $T_b$, and $T_{\text{net}}$ curves.
5. **Don't forget the conclusion:** "needs an auxiliary starting mechanism."

## 🔗 Related Topics

- [T-23: 1-Phase IM Starting Methods](T-23_1Phase_Starting_Methods.md) — How to solve the starting problem
- [T-12: Rotating Magnetic Field](T-12_Rotating_Magnetic_Field.md) — 3-phase creates RMF; 1-phase doesn't

---

[← T-21: Induction Generator](T-21_Induction_Generator.md) | [🏠 Index](00_Index.md) | [T-23: 1-Phase IM Starting Methods →](T-23_1Phase_Starting_Methods.md)
