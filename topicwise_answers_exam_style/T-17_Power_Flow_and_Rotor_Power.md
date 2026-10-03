[← T-16: Torque Equations & Curves](T-16_Torque_Equations_and_Characteristics.md) | [🏠 Index](README.md) | [T-18: Testing & Circle Diagram →](T-18_IM_Testing_and_Circle_Diagram.md)

---

# T-17: Power Flow & Rotor Power

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Power Flow & Rotor Power** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2020 Q6(b)]
> 📋 **Appeared in:** 2020 Q6(b)

**(b) Starting from equivalent circuit, derive power equations of an induction motor. [04]**

From the equivalent circuit, per-phase power flow:

**Stator input power:**
$$P_1 = 3V_1 I_1 \cos\phi_1$$

**Stator copper loss:**
$$P_{s,Cu} = 3 I_1^2 R_1$$

**Stator iron loss:**
$$P_{Fe} = 3 V_1^2/R_c \approx 3 E_1^2/R_c$$

**Air-gap power (power transferred to rotor):**
$$P_g = P_1 - P_{s,Cu} - P_{Fe} = 3 I_2^2 \cdot \frac{R_2}{s}$$

**Rotor copper loss:**
$$P_{r,Cu} = 3 I_2^2 R_2 = s \cdot P_g$$

**Gross mechanical power:**
$$P_m = P_g - P_{r,Cu} = P_g(1-s) = 3 I_2^2 R_2 \frac{1-s}{s}$$

**Net output power:**
$$P_{out} = P_m - P_{friction+windage}$$

**Summary ratios:** $P_g : P_{r,Cu} : P_m = 1 : s : (1-s)$

![Comprehensive Power Flow diagram of an Induction Motor](../Books/Theraja/Ch-34/diagrams/Ch-34_p39_fig38.jpg)

---

### [2020 Q6(d)]
> 📋 **Appeared in:** 2020 Q6(d)

**(d) 400V, 50 Hz, 6-pole, 3-φ IM. Rotor power input = 75 kW. Rotor EMF makes 100 alternations per minute. Find: (i) slip, (ii) rotor speed, (iii) rotor Cu losses per phase, (iv) mechanical power. [04]**

**Given:** $P_g = 75$ kW, $P = 6$, $f = 50$ Hz

Rotor EMF frequency: 100 alternations per minute = 100/60 Hz $= 5/3$ Hz

**(i) Slip:**
$$f_r = sf \implies s = \frac{f_r}{f} = \frac{100/60}{50} = \frac{100}{3000} = \boxed{0.0333 = 3.33\%}$$

**(ii) Synchronous speed:**
$$N_s = \frac{120 \times 50}{6} = 1000 \text{ rpm}$$

**Rotor speed:**
$$N = N_s(1-s) = 1000(1 - 0.0333) = \boxed{966.7 \text{ rpm}}$$

**(iii) Rotor copper losses (total):**
$$P_{r,Cu} = s \times P_g = 0.0333 \times 75000 = 2500 \text{ W}$$

**Per phase:**
$$P_{r,Cu,\text{phase}} = \frac{2500}{3} = \boxed{833.3 \text{ W}}$$

**(iv) Mechanical power:**
$$P_m = (1-s)P_g = (1 - 0.0333) \times 75000 = 0.9667 \times 75000 = \boxed{72500 \text{ W} = 72.5 \text{ kW}}$$

---

### [2021 Q6(c)]
> 📋 **Appeared in:** 2021 Q6(c)

**(c) Determine the rotor efficiency of an IM. [04]**

Rotor efficiency is the ratio of mechanical power developed to the electrical power input to the rotor.

**Power input to rotor (air-gap power):**
$$P_g = 3 I_2^2 \cdot \frac{R_2}{s}$$

**Rotor copper loss:**
$$P_{Cu} = 3 I_2^2 R_2 = s P_g$$

**Mechanical power developed:**
$$P_m = P_g - P_{Cu} = P_g - sP_g = (1-s)P_g$$

**Rotor efficiency:**
$$\eta_{\text{rotor}} = \frac{P_m}{P_g} = \frac{(1-s)P_g}{P_g} = \boxed{(1-s)}$$

Or as percentage: $\eta_{\text{rotor}} = (1-s) \times 100\%$

At full load with $s = 0.04$: $\eta_{\text{rotor}} = 96\%$.

**Interpretation:** For every unit of electrical power crossing the air gap, $(1-s)$ units become mechanical power and $s$ units are lost as heat in the rotor resistance. Low slip → high rotor efficiency. This is why induction motors are designed to operate at small slip.

---

### [2021 Q8(a)]
> 📋 **Appeared in:** 2021 Q8(a)

**(a) Define synchronous watt with an example. [03]**

**Synchronous watt:** A unit of torque used in induction motor calculations. One synchronous watt is the torque that develops one watt of power at synchronous speed.

$$T \text{ (in synchronous watts)} = P_g \text{ (in watts)}$$

**Relationship:**
$$T = \frac{P_g}{\omega_s} = \frac{P_g}{2\pi N_s/60} \text{ N-m}$$

So if $P_g = 1000$ W (1 synchronous watt) and $N_s = 1500$ rpm:
$$T = \frac{1000}{2\pi \times 1500/60} = \frac{1000}{157.08} = 6.37 \text{ N-m}$$

**Example:** A motor has air-gap power $P_g = 5000$ W. If synchronous speed is 1000 rpm ($\omega_s = 104.7$ rad/s):
$$T = \frac{5000}{104.7} = 47.75 \text{ N-m}$$

Expressing the torque as 5000 synchronous watts captures both the power and speed dependence in one quantity.

---

### [2023 Q6(a)]
> 📋 **Appeared in:** 2018 Q5(b), 2023 Q6(a) (Years: 2018, 2023)

**(a) Define synchronous watt. Derive an expression of rotor efficiency of a $3-\varphi$ induction motor. [CO2, Marks: 04]**

**Synchronous watt.** One synchronous watt is that torque which, acting at synchronous speed, would develop a power of one watt. Torque expressed in synchronous watts is numerically equal to the rotor input power:
$$T_g \ (\text{in synchronous watts}) = P_2 \ (\text{in watts})$$
$$T_g \ (\text{N-m}) = \frac{\text{torque in synchronous watts}}{2\pi N_s / 60} = \frac{P_2}{\omega_s}$$

It is a handy unit because torque and rotor input are then the same number.

**Rotor efficiency.**

![Block diagram of induction motor power stages: stator input, rotor input across the air gap, mechanical power developed, and rotor output](../Books/Theraja/Ch-34/diagrams/Ch-34_p38_power_stages_block.jpg)

Let $P_2$ be the rotor input (power crossing the air gap), $P_{cu2}$ the rotor copper loss and $P_m$ the gross mechanical power developed.

**Step 1. Rotor copper loss in terms of slip.** The rotor emf per phase when running is $sE_2$, and the rotor current is $I_{2r}$:
$$P_{cu2} = 3 I_{2r}^2 R_2 = 3 (s E_2) I_{2r} \cos\phi_2$$

The rotor input is the product of the standstill emf and the in-phase current:
$$P_2 = 3 E_2 I_{2r} \cos\phi_2$$

Dividing:
$$\boxed{P_{cu2} = s P_2}$$

**Step 2. Mechanical power developed.** By energy balance,
$$P_m = P_2 - P_{cu2} = P_2 - s P_2 = (1 - s) P_2$$

**Step 3. Power ratio.**
$$P_2 : P_m : P_{cu2} = 1 : (1 - s) : s$$

**Step 4. Rotor efficiency.**
$$\eta_{\text{rotor}} = \frac{P_m}{P_2} = \frac{(1-s)P_2}{P_2} = 1 - s$$

Since $s = (N_s - N)/N_s$, we also have $1 - s = N/N_s$:

$$\boxed{\eta_{\text{rotor}} = 1 - s = \frac{N}{N_s}}$$

> [!example] Quick use
> At 4% slip the rotor efficiency is 96%. The remaining 4% of the air-gap power is lost as rotor copper loss. This is why an induction motor cannot be run at large slip for long.

---

### [Practice: Rotor Efficiency Summary]
> **Practice problem (not from a past paper)**

**(c) What is rotor efficiency? Show that rotor efficiency = $(1-s)$.**

**Rotor efficiency:** Ratio of mechanical power developed to electrical power input to the rotor (air-gap power).

$$\eta_{\text{rotor}} = \frac{P_m}{P_g} = \frac{(1-s)P_g}{P_g} = \boxed{(1-s)}$$

From the power ratio $P_g : P_{r,Cu} : P_m = 1 : s : (1-s)$:
- Of each unit of air-gap power, fraction $s$ is wasted as rotor copper heat.
- Fraction $(1-s)$ becomes mechanical work.

At $s = 0.04$ (full load, typical): $\eta_{\text{rotor}} = 96\%$. High rotor efficiency is achievable at low slip. Motors are designed to run at small slip for this reason.

---

### [2024 Q5(b)]
> 📋 **Appeared in:** 2024 Q5(b)

**(b) Define slip. Prove that an induction motor cannot run at synchronous speed. [Marks: 03, CO: 3]**

The full treatment of this question is in [T-13: Slip, Synchronous Speed & Basics](T-13_Slip_Synchronous_Speed_and_Basics.md), which files it jointly under 2023 Q5(b) and 2024 Q5(b). In power-flow terms the proof is one line:

| Slip | Rotor emf | Rotor current | Air-gap power | Torque |
|:---:|:---:|:---:|:---:|:---:|
| $s = 0$ | $sE_2 = 0$ | $I_{2r} = 0$ | $P_g = 0$ | $T = 0$ |

Zero slip means zero relative motion between the rotating field and the rotor. Nothing is induced, no current flows, the air-gap power is zero and so is the torque. Since friction and windage always need torque, the rotor must fall back below synchronous speed.

$$\boxed{N < N_s \text{ always} \implies \text{the induction motor is asynchronous}}$$

---

[← T-16: Torque Equations & Curves](T-16_Torque_Equations_and_Characteristics.md) | [🏠 Index](README.md) | [T-18: Testing & Circle Diagram →](T-18_IM_Testing_and_Circle_Diagram.md)
