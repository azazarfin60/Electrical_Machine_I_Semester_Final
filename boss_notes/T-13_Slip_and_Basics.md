[← T-12: Rotating Magnetic Field](T-12_Rotating_Magnetic_Field.md) | [🏠 Index](00_Index.md) | [T-14: IM Equivalent Circuit →](T-14_IM_Equivalent_Circuit.md)

---

# T-13: Slip, Synchronous Speed & Basics
> **Section:** B | **Priority:** 🔴 MUST | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-34 (Art. 34.9-34.15), VK Mehta Ch-8 (Art. 8.5-8.9), Slides L-03

## Why This Topic Matters

Slip is the single most fundamental concept in induction motor analysis. Every equation in Section B contains slip $s$. Questions on slip appear in 4 out of 7 papers, ranging from definitions (1-3 marks) to numericals (4-5 marks). The question "why can an IM never run at synchronous speed?" appeared 4 times. If you understand slip, you understand induction motors.

---

## 📝 Key Definitions

> **Slip:** "The difference between the synchronous speed $N_s$ of the rotating stator field and the actual speed $N$ of the rotor is called the slip speed. The fractional slip $s$ is defined as the ratio of slip speed to synchronous speed: $s = (N_s - N)/N_s$." — VK Mehta, Art. 8.6

> **Synchronous Speed:** "The speed at which the rotating magnetic field revolves is called the synchronous speed. For a machine with $P$ poles: $N_s = 120f/P$ r.p.m." — VK Mehta, Art. 8.3

> **Rotor Frequency:** "The frequency of the induced rotor e.m.f. and current is $f' = sf$, where $s$ is the slip and $f$ is the supply frequency." — VK Mehta, Art. 8.7

---

## Synchronous Speed

The RMF rotates at:

$$\boxed{N_s = \frac{120f}{P} \text{ rpm}}$$

| Poles ($P$) | $N_s$ at 50 Hz | $N_s$ at 60 Hz |
|:---:|:---:|:---:|
| 2 | 3000 rpm | 3600 rpm |
| 4 | 1500 rpm | 1800 rpm |
| 6 | 1000 rpm | 1200 rpm |
| 8 | 750 rpm | 900 rpm |

---

## Slip

Slip measures how much the rotor "falls behind" the rotating field.

$$\boxed{s = \frac{N_s - N}{N_s}}$$

Rearranging: $N = N_s(1-s)$

**Slip ranges:**
- At standstill ($N = 0$): $s = 1$ (100%)
- At synchronous speed ($N = N_s$): $s = 0$ (never reached)
- Normal full-load: $s = 0.02$ to $0.05$ (2% to 5%)

**Slip speed** = actual speed difference:

$$N_{\text{slip}} = N_s - N = sN_s \text{ rpm}$$

---

## Why an IM Can Never Run at Synchronous Speed

This is one of the most repeated conceptual questions. The argument is simple:

1. If rotor speed $N = N_s$, there is no relative motion between the RMF and the rotor conductors.
2. No relative motion means no flux is cut by rotor conductors.
3. No flux cutting means no induced EMF (Faraday's law).
4. No EMF means no rotor current.
5. No current means no torque.
6. No torque means the rotor cannot sustain $N_s$ against friction and windage losses.
7. The rotor slows down. Slip increases. EMF reappears. Torque is restored.

The motor settles at a speed slightly below $N_s$ where the torque exactly balances the load.

---

## Rotor Quantities at Slip $s$

At standstill ($s = 1$), rotor parameters per phase are: $E_2$, $R_2$, $X_2 = 2\pi f L_2$.

When running at slip $s$:

| Quantity | Standstill ($s=1$) | Running (slip $s$) |
|:---|:---|:---|
| Rotor EMF | $E_2$ | $sE_2$ |
| Rotor reactance | $X_2$ | $sX_2$ |
| Rotor resistance | $R_2$ | $R_2$ (unchanged) |
| Rotor impedance | $\sqrt{R_2^2 + X_2^2}$ | $\sqrt{R_2^2 + (sX_2)^2}$ |
| Rotor frequency | $f$ | $sf$ |
| Rotor current | $\frac{E_2}{\sqrt{R_2^2 + X_2^2}}$ | $\frac{sE_2}{\sqrt{R_2^2 + (sX_2)^2}}$ |

Key point: resistance $R_2$ does not change with frequency. Only reactance changes because $X = 2\pi f L$.

---

## IM as a Rotating Transformer

An IM is called a rotating transformer because:

| Aspect | Transformer | Induction Motor |
|:---|:---|:---|
| Primary | Stator winding | Stator winding |
| Secondary | Fixed secondary | Rotating rotor |
| Power transfer | Mutual flux in core | Rotating field across air gap |
| Secondary circuit | Connected to load | Short-circuited (squirrel cage) |
| Secondary frequency | Same as primary ($f$) | $sf$ (slip frequency) |

"An induction motor can be treated as a rotating transformer i.e. one in which primary winding is stationary but the secondary is free to rotate." — Theraja, Art. 34.2

---

## Worked Example (PYQ 2019)

**2019 Q5(c): 4-pole, 50 Hz IM. Find: (i) synchronous speed, (ii) rotor speed at $s = 4\%$, (iii) rotor frequency at 600 rpm.**

**(i) Synchronous speed:**

$$N_s = \frac{120 \times 50}{4} = \boxed{1500 \text{ rpm}}$$

**(ii) Rotor speed at $s = 4\%$:**

$$N = N_s(1-s) = 1500(1 - 0.04) = 1500 \times 0.96 = \boxed{1440 \text{ rpm}}$$

**(iii) Rotor frequency at $N = 600$ rpm:**

$$s = \frac{N_s - N}{N_s} = \frac{1500 - 600}{1500} = 0.6$$

$$f_r = sf = 0.6 \times 50 = \boxed{30 \text{ Hz}}$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Define synchronous speed, slip, and slip speed.
> **Appeared:** 2021 Q5(a) — (3 marks)

**Full Answer:**

**(i) Synchronous speed ($N_s$):** The speed of the rotating magnetic field produced by the 3-phase stator winding. $N_s = 120f/P$ rpm, where $f$ is supply frequency and $P$ is number of poles.

**(ii) Slip ($s$):** The fractional difference between synchronous speed and rotor speed. $s = (N_s - N)/N_s$. At standstill $s = 1$. At full load $s \approx 0.02$ to $0.05$.

**(iii) Slip speed:** The actual speed difference between the rotating field and the rotor: $N_{\text{slip}} = N_s - N = sN_s$ rpm. This is the speed at which rotor conductors cut the rotating field.

---

### 🎯 Q2: 6-pole, 50 Hz motor driven at 1000 rpm. Find rotor voltage, frequency, slip, and torque. Can it run at this speed by itself?
> **Appeared:** 2017 Q1(c) — (4 marks)

**Full Answer:**

$N_s = 120 \times 50/6 = 1000$ rpm. Rotor speed $N = 1000$ rpm.

Slip: $s = (1000 - 1000)/1000 = 0$

Rotor frequency: $f_r = sf = 0 \times 50 = 0$ Hz

Rotor voltage: $E_{2s} = sE_2 = 0$

Torque: At $s = 0$, rotor EMF = 0, rotor current = 0, so torque = 0.

**Can it run at this speed by itself?** No. At synchronous speed, slip is zero. No EMF is induced. No rotor current flows. No torque is developed. The motor cannot sustain this speed against friction. An induction motor always runs at $N < N_s$.

---

### 🎯 Q3: What happens if the slip of a 3-phase IM becomes negative?
> **Appeared:** 2017 Q1(d) — (1 mark)

**Full Answer:**

If $N > N_s$, slip is negative ($s < 0$). The motor acts as an **induction generator**. It delivers active electrical power back to the supply instead of consuming it. The machine still draws reactive power (VARs) from the supply for excitation.

---

### 🎯 Q4: Why is an IM called a rotating transformer? State advantages and disadvantages.
> **Appeared:** 2017 Q1(a), 2019 Q5(b), 2020 Q5(b) — (4 marks)

**Full Answer:**

An IM is called a rotating transformer because power transfers from the stator to the rotor by electromagnetic induction, just like a transformer. The stator is the primary. The rotor is the secondary. The key difference: the secondary (rotor) rotates.

**Advantages:**
1. Simple, strong construction (no brushes or commutator in squirrel-cage type)
2. Self-starting (unlike synchronous motor)
3. Low maintenance and long life
4. Can be totally enclosed for hazardous environments
5. Wide range of sizes and speeds available

**Disadvantages:**
1. Speed control is difficult and costly
2. Poor power factor at light loads (draws high reactive current)
3. Starting current is high (5-8 times rated)
4. Speed drops with load (not constant-speed like synchronous motor)

---

## Exam Variants

| Year | Question | Data/Type | Key Answer |
|:---|:---|:---|:---|
| 2017 Q1(a) | Why rotating transformer? | Theory | Analogy + advantages/disadvantages |
| 2017 Q1(c) | 6-pole, 50 Hz at 1000 rpm | Numerical | $s = 0$, torque = 0 |
| 2017 Q1(d) | Negative slip? | Theory | Induction generator |
| 2019 Q5(b) | Rotating transformer + adv/disadv | Theory | Same as 2017 |
| 2019 Q5(c) | 4-pole, 50 Hz IM | Numerical | $N_s = 1500$, $f_r = 30$ Hz |
| 2021 Q5(a) | Define $N_s$, $s$, slip speed | Definitions | 3 definitions |

---

## ⚡ Exam Tips & Common Mistakes

1. **Slip is dimensionless.** Express it as a decimal (0.04) or percentage (4%). State which you are using.
2. **$f_r = sf$, not $f/s$.** A common algebra error.
3. **Resistance does NOT change with frequency.** Only reactance ($X = 2\pi fL$) changes. Resistance is a property of the conductor material.
4. **"Why can't IM run at $N_s$?" needs a chain of reasoning.** Don't just say "no torque." Show the full chain: no relative motion, no EMF, no current, no torque.
5. **Negative slip = generator mode.** This is a 1-mark definition that students forget.

## 🔗 Related Topics

- [T-12: Rotating Magnetic Field](T-12_Rotating_Magnetic_Field.md) — Creates the synchronous speed
- [T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) — Uses slip to model the rotor
- [T-15a: Starting Torque](T-15a_Torque_Starting.md) — Torque at $s = 1$
- [T-16: Power Flow](T-16_Power_Flow.md) — Power division depends on slip
- [T-21: Induction Generator](T-21_Induction_Generator.md) — What happens at $s < 0$

---

[← T-12: Rotating Magnetic Field](T-12_Rotating_Magnetic_Field.md) | [🏠 Index](00_Index.md) | [T-14: IM Equivalent Circuit →](T-14_IM_Equivalent_Circuit.md)
