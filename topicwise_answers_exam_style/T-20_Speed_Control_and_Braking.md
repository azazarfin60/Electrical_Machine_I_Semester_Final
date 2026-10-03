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

![Rotor rheostat circuit for speed control and starting](../Books/Theraja/Ch-35/diagrams/ch35_p28_fig35_22.jpg)

---

### [2018 Q5(a)]
> 📋 **Appeared in:** 2018 Q5(a)

**(a) Short notes on: (i) Regenerative braking (ii) Dynamic braking (iii) Plugging [03]**

![Operating modes of induction machine: Motoring, Generating, and Braking](../Books/Theraja/Ch-34/diagrams/Ch-34_p34_fig32.jpg)
![Power flow diagram during plugging (braking)](../Books/Theraja/Ch-34/diagrams/Ch-34_p32_fig27.jpg)

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


---

### [2023 Q8(a)]
> 📋 **Appeared in:** 2023 Q8(a)

**(a) Briefly explain crawling and cogging of an induction motor. Also, mention one method of speed control of an induction motor. [CO3, Marks: 03]**

#### Crawling

![Torque-speed characteristics showing the dip caused by the 7th space harmonic, which makes the motor crawl near one seventh of synchronous speed](../Books/Theraja/Ch-35/diagrams/ch35_p31_fig35_25.jpg)

A squirrel-cage motor sometimes settles down and runs stably at about **one seventh of synchronous speed** instead of accelerating to normal speed. This is called crawling.

**Cause.** The stator m.m.f. wave is not a pure sine wave. It carries odd space harmonics. The $n$th harmonic sets up its own field rotating at $N_s/n$, and so develops its own harmonic torque of magnitude about $1/n^2$ of the fundamental.

- Third harmonic: absent in a balanced 3-phase system, so no torque.
- Fifth harmonic: rotates backward at $N_s/5$, acting as a braking torque.
- Seventh harmonic: rotates **forward** at $N_s/7$ and is the troublemaker.

The 7th harmonic torque falls to zero at $N = N_s/7$. The resultant torque curve therefore has a deep dip just below $N_s/7$. If the load torque line cuts the motor curve inside that dip, the motor locks on there and crawls.

**Remedy.** Skew the rotor slots to suppress tooth-ripple harmonics.

#### Cogging (magnetic locking)

The rotor refuses to start at all, especially at reduced voltage. It happens when the number of rotor slots $S_2$ equals the number of stator slots $S_1$, or is an integral multiple of it.

**Cause.** With $S_1 = S_2$ the air-gap reluctance is lowest when the rotor teeth face the stator teeth squarely. The rotor locks into that minimum-reluctance position. If the starting torque is less than this alignment torque, the motor cannot break free.

**Remedies.**
1. Make the number of rotor slots prime to the number of stator slots.
2. **Skew the rotor slots**, so no two teeth can align over the full length.

#### One method of speed control

From $N = N_s(1 - s) = \dfrac{120f}{P}(1 - s)$, three handles exist: $f$, $P$ and $s$.

**Rotor rheostat control (slip control, for slip-ring motors).** Add external resistance through the slip rings. Extra rotor resistance increases the slip needed to carry the same torque, so the motor slows down:
$$T \propto \frac{s E_2^2 R_2}{R_2^2 + (s X_2)^2}$$

Maximum torque is unchanged, because $T_{\max} = k E_2^2/(2X_2)$ does not contain $R_2$. Only the slip at which it occurs moves, since $s_{maxT} = R_2/X_2$.

Speed control is simple and smooth and gives a high starting torque. But the extra $I_2^2R$ loss is wasted as heat, so efficiency falls as speed falls. Modern practice prefers **V/f (variable frequency) control**, which holds $V/f$ constant so the flux stays constant while frequency sets the speed.

---

[← T-19: 3-Phase Starting Methods](T-19_Starting_Methods_3-Phase_IM.md) | [🏠 Index](README.md) | [T-21: Induction Generator →](T-21_Induction_Generator.md)
