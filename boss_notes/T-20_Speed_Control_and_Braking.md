[← T-19: Starting Methods](T-19_Starting_Methods_3Phase.md) | [🏠 Index](00_Index.md) | [T-21: Induction Generator →](T-21_Induction_Generator.md)

---

# T-20: Speed Control & Braking
> **Section:** B | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-34-35, Slides L-07

## Why This Topic Matters

Speed control and braking questions appeared in 4 out of 7 papers. Plugging was defined in 4 papers (2017, 2018, 2019, 2020). Speed control methods appeared in 2017, 2019, 2023. The rotor resistance speed control numerical appeared in 2021. These are short, definition-heavy questions worth 2-4 marks each.

---

## 📝 Key Definitions

> **Plugging:** "A braking method in which the phase sequence of the stator supply is reversed while the motor is running. The stator field now rotates opposite to the rotor, producing a braking torque. The motor decelerates rapidly. The supply must be disconnected before zero speed, otherwise the motor reverses direction." — Theraja, Art. 34.44

> **Pull-out Torque:** "The maximum torque a motor can develop at any operating speed. Also called breakdown torque. If the load torque exceeds pull-out torque, the motor stalls." — Theraja, Art. 34.24

---

## Speed Control Methods

From $N = N_s(1-s)$ and $N_s = 120f/P$:

$$N = \frac{120f}{P}(1-s)$$

Speed can be changed by varying $f$, $P$, or $s$.

### 1. Stator Voltage Control
Reduce supply voltage $V \to$ reduced torque $\to$ higher slip $\to$ lower speed.

Simple but inefficient. Torque drops as $V^2$. Only suitable for fan/pump loads (torque $\propto N^2$).

### 2. Supply Frequency Control (V/f)
Change $f$ to change $N_s$. Must change $V$ proportionally to maintain constant flux ($V/f$ = constant).

Wide, smooth speed range. Used in Variable Frequency Drives (VFDs). Best modern method.

### 3. Pole Changing
Switch winding configurations to change $P$. Gives discrete speed steps.

Example: $P = 4 \to N_s = 1500$ rpm; $P = 8 \to N_s = 750$ rpm. Only for squirrel-cage motors.

### 4. Rotor Resistance Control (Slip-Ring Only)
Add external resistance $R_{ext}$ in rotor circuit through slip rings. Higher $R_2 \to$ higher slip at same torque $\to$ lower speed.

Disadvantage: Power $= sP_g$ wasted as heat in external resistors. Efficiency drops.

---

## Electric Braking Methods

### Regenerative Braking
Motor driven above $N_s$ ($s < 0$). Acts as induction generator. Feeds power back to supply. Energy-efficient. Only above synchronous speed.

### Dynamic Braking (DC Injection)
Stator disconnected from AC. DC current fed to stator. Creates stationary field. Rotating rotor cuts this field. Braking currents induced. Energy dissipated as heat.

### Plugging (Counter-Current)
Reverse two stator supply leads while running. Stator field reverses direction. Braking torque opposes motion. Very rapid deceleration. Must disconnect just before zero speed, otherwise the motor reverses. At the instant of plugging $s \approx 2$, decreasing to $s = 1$ at standstill.

![Torque-speed curve showing all three operating modes](diagrams/torque_speed_complete_curve.jpg)

---

## Worked Example (PYQ 2021)

**2021 Q4(c): 4-pole, 50 Hz slip-ring IM. $R_2 = 0.30\,\Omega$/phase, runs at 1440 rpm full load. Find external resistance to lower speed to 1320 rpm at same torque.**

$N_s = 120 \times 50/4 = 1500$ rpm

**Full-load slip:** $s_1 = (1500 - 1440)/1500 = 0.04$

**New slip:** $s_2 = (1500 - 1320)/1500 = 0.12$

**Constant torque condition (low-slip approximation):**

$$\frac{s_1}{R_2} = \frac{s_2}{R_2 + R_{ext}}$$

$$\frac{0.04}{0.30} = \frac{0.12}{0.30 + R_{ext}}$$

$$0.30 + R_{ext} = \frac{0.12 \times 0.30}{0.04} = 0.90\,\Omega$$

$$R_{ext} = 0.90 - 0.30 = \boxed{0.60\,\Omega/\text{phase}}$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Define plugging and pull-out torque.
> **Appeared:** 2017 Q2(a) — (2 marks)

**Full Answer:**

**Plugging:** A braking method. The phase sequence of stator supply is reversed while the motor runs. A braking torque opposes rotation. Motor decelerates rapidly. Supply must be cut just before zero speed, otherwise the motor reverses. Slip is $s \approx 2$ when initiated at rated speed, and drops to $s = 1$ at standstill ($1 < s \le 2$).

**Pull-out torque:** The maximum torque a motor can develop. Also called breakdown torque ($T_{\max}$). If load exceeds this, the motor stalls.

---

### 🎯 Q2: Short notes on regenerative braking, dynamic braking, and plugging.
> **Appeared:** 2018 Q5(a) — (3 marks)

**Full Answer:**

**(i) Regenerative braking:** Motor speed exceeds $N_s$ ($s < 0$). Machine acts as generator. Power fed back to supply. Smooth, efficient. Used in cranes (lowering loads) and electric trains.

**(ii) Dynamic braking:** Stator disconnected from AC supply. DC fed to stator winding. Stationary magnetic field created. Rotating rotor cuts this field and braking currents are induced. Energy dissipated as heat in rotor.

**(iii) Plugging:** Two stator leads swapped while running. Stator field reverses. Braking torque opposes motion. Very rapid stop. Must disconnect just before zero speed, otherwise the motor reverses. Slip ranges from $s \approx 2$ down to $s = 1$ at standstill.

---

### 🎯 Q3: Mention speed control methods and discuss any one.
> **Appeared:** 2017 Q2(c) — (4 marks)

**Full Answer:**

Speed control methods: (1) Stator voltage control, (2) Supply frequency control (V/f), (3) Pole changing, (4) Rotor resistance control.

**Rotor resistance control:** For slip-ring motors only. External resistance added through slip rings. From $T \propto sV^2/R_{\text{total}}$ (at low slip), for constant torque: $s \propto R_{\text{total}}$. Higher resistance = higher slip = lower speed.

Disadvantage: Power $sP_g$ wasted as heat. Efficiency drops. Used where step-speed control and high starting torque are needed (cranes, hoists).

---

### 🎯 Q4: Rotor resistance numerical for speed reduction.
> **Appeared:** 2021 Q4(c) — (4 marks)

**Full Answer:**

See [Worked Example](#worked-example-pyq-2021) above. Result: $R_{ext} = 0.60\,\Omega$/phase.

---

### 🎯 Q5: Define braking of IM. How can speed be controlled?
> **Appeared:** 2019 Q7(c) — (4 marks)

**Full Answer:**

**Braking:** Applying a decelerating torque to bring the motor to rest or control speed. Three methods: plugging, dynamic braking, regenerative braking.

**Speed control methods:**
1. **Stator voltage control:** Reduce $V$, torque drops, speed drops. Simple but poor efficiency.
2. **V/f control:** Change both $V$ and $f$ proportionally. Wide smooth range. VFDs.
3. **Pole changing:** Switch winding configuration. Discrete speed steps. Squirrel-cage only.
4. **Rotor resistance:** Add external $R$ (slip-ring). Higher slip = lower speed. Lossy.
5. **Slip energy recovery:** Feed slip power back to supply instead of wasting. Efficient but complex.

### 🎯 Q6: Briefly explain crawling and cogging of an induction motor. Also, mention one method of speed control of an induction motor.
> **Appeared:** 2023 Q8(a) — 3 marks

**Full Answer:**

#### Crawling

![Torque-speed characteristics showing the dip caused by the 7th space harmonic, which makes the motor crawl near one seventh of synchronous speed](../Books/Theraja/Ch-35/diagrams/ch35_p31_fig35_25.jpg)

A squirrel-cage motor sometimes settles down and runs stably at about **one seventh of synchronous speed** instead of accelerating to normal speed.

**Cause.** The stator m.m.f. wave is not a pure sine wave. It carries odd space harmonics. The $n$th harmonic sets up its own field rotating at $N_s/n$, and so develops its own harmonic torque of magnitude about $1/n^2$ of the fundamental. The third harmonic is absent in a balanced 3-phase system. The fifth rotates backward at $N_s/5$ and acts as braking torque. The **seventh rotates forward** at $N_s/7$ and is the troublemaker.

The 7th harmonic torque falls to zero at $N = N_s/7$, so the resultant torque curve has a deep dip just below $N_s/7$. If the load torque line cuts the motor curve inside that dip, the motor locks on there and crawls.

**Remedy.** Skew the rotor slots to suppress tooth-ripple harmonics.

#### Cogging (magnetic locking)

The rotor refuses to start at all, especially at reduced voltage. It happens when the number of rotor slots $S_2$ equals the number of stator slots $S_1$, or is an integral multiple of it.

**Cause.** With $S_1 = S_2$ the air-gap reluctance is lowest when the rotor teeth face the stator teeth squarely. The rotor locks into that minimum-reluctance position. If the starting torque is less than this alignment torque, the motor cannot break free.

**Remedies.** (1) Make the number of rotor slots prime to the number of stator slots. (2) **Skew the rotor slots**, so no two teeth can align over the full length.

#### One method of speed control

From $N = N_s(1 - s) = \dfrac{120f}{P}(1 - s)$, three handles exist: $f$, $P$ and $s$.

**Rotor rheostat control (slip control, for slip-ring motors).** Add external resistance through the slip rings. Extra rotor resistance increases the slip needed to carry the same torque, so the motor slows down. Maximum torque is unchanged, because $T_{\max} = kE_2^2/(2X_2)$ does not contain $R_2$. Only the slip at which it occurs moves, since $s_{maxT} = R_2/X_2$. It is simple and smooth and gives a high starting torque, but the extra $I_2^2R$ loss is wasted as heat. Modern practice prefers **V/f control**, which holds $V/f$ constant.

---

---

## Exam Variants

| Year | Question | Marks | Focus |
|:---|:---|:---|:---|
| 2017 Q2(a) | Define plugging + pull-out torque | 2 | Definitions |
| 2017 Q2(c) | Speed control methods + discuss one | 4 | Theory |
| 2018 Q5(a) | Three types of braking | 3 | Short notes |
| 2019 Q7(c) | Define braking + speed control | 4 | Theory |
| 2020 Q8(a) | Define plugging + slip | 2 | Definitions |
| 2021 Q4(c) | Rotor resistance numerical | 4 | Numerical |

---

## ⚡ Exam Tips & Common Mistakes

1. **Plugging appears in almost every paper.** Memorize a 3-sentence definition.
2. **Rotor resistance method ONLY works for slip-ring motors.** Squirrel-cage has no access to rotor.
3. **In the speed control numerical:** The key equation is $s_1/R_2 = s_2/(R_2 + R_{ext})$ for constant torque.
4. **Don't confuse regenerative braking with plugging.** Regenerative = above $N_s$, power flows back. Plugging = phase reversal, no power recovery.

## 🔗 Related Topics

- [T-15c: Torque-Speed Curves](T-15c_Torque_Speed_Curves.md) — Braking regions on the curve
- [T-19: Starting Methods](T-19_Starting_Methods_3Phase.md) — Related to starting current
- [T-21: Induction Generator](T-21_Induction_Generator.md) — Regenerative braking = generator mode

---

[← T-19: Starting Methods](T-19_Starting_Methods_3Phase.md) | [🏠 Index](00_Index.md) | [T-21: Induction Generator →](T-21_Induction_Generator.md)
