[← T-19: 3-Phase Starting Methods](T-19_Starting_Methods_3-Phase_IM.md) | [🏠 Index](README.md) | [T-21: Induction Generator →](T-21_Induction_Generator.md)

---

# T-20: Speed Control & Braking

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Speed Control & Braking** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q2(a)]
> 📋 **Appeared in:** 2017 Q2(a)

**(a) Define: (i) Plugging (ii) Pull-out torque [02]**

**Plugging:** A braking method. The phase sequence of stator supply is reversed while the motor is running. The motor develops a torque opposing rotation. The motor decelerates and stops quickly. The supply must be cut off at zero speed or the motor reverses direction.

**Pull-out torque:** The maximum torque a motor can develop at any operating speed. Also called breakdown torque or maximum torque ($T_{\max}$). If the load torque exceeds this, the motor stalls.

---

### [2017 Q2(c)]
> 📋 **Appeared in:** 2017 Q2(c)

**(c) Mention speed control methods and discuss any one. [04]**

Speed control methods for a 3-phase induction motor:
1. Stator voltage control
2. Supply frequency control (V/f control)
3. Pole changing
4. Rotor resistance control (slip-ring motors only)

**Rotor resistance control:**

For a slip-ring induction motor, external resistance is added to the rotor circuit through slip rings. From the torque equation, slip $s$ increases when $R_2$ increases (to maintain the same torque). Since $N = N_s(1 - s)$, higher slip means lower speed.

Disadvantage: Power $= s \times P_{\text{air gap}}$ is wasted in the external resistors. Efficiency drops. Used where step-speed control and good starting torque are needed (e.g., cranes, hoists).

![Rotor rheostat circuit for speed control and starting](../Books/diagrams/ch35_p28_fig35_22.jpg)

---

### [2018 Q5(a)]
> 📋 **Appeared in:** 2018 Q5(a)

**(a) Short notes on: (i) Regenerative braking (ii) Dynamic braking (iii) Plugging [03]**

![Operating modes of induction machine: Motoring, Generating, and Braking](../Books/diagrams/Ch-34_p34_fig32.jpg)
![Power flow diagram during plugging (braking)](../Books/diagrams/Ch-34_p32_fig27.jpg)

**(i) Regenerative braking:** The motor speed exceeds synchronous speed ($N > N_s$), making slip negative. The machine acts as an induction generator, feeding power back to the supply. Smooth, energy-efficient, but only possible above synchronous speed. Used in cranes (lowering heavy loads) and electric trains on downhill sections.

**(ii) Dynamic braking:** The stator is disconnected from the AC supply. A DC current is then fed into the stator winding. This creates a stationary magnetic field. The rotating rotor cuts the stationary field and induces braking currents. The motor comes to a controlled stop. Energy is dissipated as heat in the rotor circuit.

**(iii) Plugging:** Also called counter-current braking. The phase sequence of the stator supply is reversed while the motor is running. The stator field rotates opposite to rotor direction. A braking torque is produced. The motor decelerates rapidly. The supply must be disconnected before zero speed, otherwise the motor reverses direction.

---

### [2019 Q7(c)]
> 📋 **Appeared in:** 2019 Q7(c)

**(c) Define braking of IM. How can speed be controlled? [04]**

**Braking of IM:** Applying a decelerating torque to bring the motor to rest (or to control speed during deceleration). Three methods: plugging, dynamic braking, regenerative braking.

**Speed control methods:**

1. **Stator voltage control:** Reduce supply voltage → reduce torque → speed drops. Simple but poor efficiency. Used for fan/pump loads.

2. **Supply frequency control (V/f control):** Change both $V$ and $f$ proportionally. Synchronous speed $N_s = 120f/P$ changes. Wide, smooth speed range. Used in VFDs.

3. **Pole changing:** Switch between winding configurations to change the number of poles ($P$). Gives discrete speed steps ($N_s = 120f/P$). Only for squirrel-cage motors.

4. **Rotor resistance control:** Add external resistance in rotor (slip-ring motors). Higher slip = lower speed. Simple but lossy.

5. **Slip energy recovery:** Feed slip power back to supply (Kramer system) instead of dissipating. Efficient but complex.

---

### [2020 Q8(a)]
> 📋 **Appeared in:** 2020 Q8(a)

**(a) Define: (i) Plugging, (ii) Slip. [02]**

**(i) Plugging:** An electric braking method. The phase sequence of the stator supply is reversed while the motor is running. The motor develops a torque opposing its current direction of rotation. The motor decelerates rapidly. The supply must be disconnected when speed reaches zero, otherwise the motor reverses.

**(ii) Slip:** The fractional difference between synchronous speed and rotor speed:
$$s = \frac{N_s - N}{N_s}$$

At standstill: $s = 1$. At synchronous speed: $s = 0$ (never reached in practice). Normal full-load: $s = 0.02$–$0.05$ (2–5%).

---

### [2021 Q4(c)]
> 📋 **Appeared in:** 2021 Q4(c)

**(c) 4-pole, 50 Hz slip-ring IM. $R_2 = 0.30\,\Omega/\text{phase}$, runs at 1440 rpm full load. Find external resistance to lower speed to 1320 rpm at same torque. [04]**

**Given:** $P = 4$, $f = 50$ Hz, $R_2 = 0.30\,\Omega$, $N_1 = 1440$ rpm (full load)

$$N_s = \frac{120 \times 50}{4} = 1500 \text{ rpm}$$

**Full-load slip:**
$$s_1 = \frac{1500 - 1440}{1500} = \frac{60}{1500} = 0.04$$

**New slip at 1320 rpm:**
$$s_2 = \frac{1500 - 1320}{1500} = \frac{180}{1500} = 0.12$$

**Condition for same torque at both operating points:**

From the torque equation, at constant torque (and ignoring the $s^2 X_2^2$ term for small slip, or using the proportionality at low slip):

$$T \propto \frac{sE_2^2 R_{\text{total}}}{R_{\text{total}}^2} = \frac{sE_2^2}{R_{\text{total}}}$$

For constant torque: $\frac{s_1}{R_2} = \frac{s_2}{R_2 + R_{ext}}$

$$\frac{0.04}{0.30} = \frac{0.12}{0.30 + R_{ext}}$$

$$0.30 + R_{ext} = \frac{0.12 \times 0.30}{0.04} = \frac{0.036}{0.04} = 0.90\,\Omega$$

$$R_{ext} = 0.90 - 0.30 = \boxed{0.60\,\Omega/\text{phase}}$$

---

## SECTION - B (Induction Motors: Q5 to Q8)

---

[← T-19: 3-Phase Starting Methods](T-19_Starting_Methods_3-Phase_IM.md) | [🏠 Index](README.md) | [T-21: Induction Generator →](T-21_Induction_Generator.md)
