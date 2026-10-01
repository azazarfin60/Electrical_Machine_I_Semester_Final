# T-13: Slip, Synchronous Speed & Basics

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Slip, Synchronous Speed & Basics** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Question 1(c): 6-pole, 50 Hz motor driven at 1000 rpm

> 📋 **Appeared in:** 2017 Q1(c)

#### Understanding the question

The question asks what happens when the motor runs at exactly 1000 rpm. This requires thinking carefully about what makes an induction motor different from a synchronous motor.

**Step 1: Find synchronous speed.**

For a 6-pole motor on a 50 Hz supply:
$$N_s = \frac{120f}{P} = \frac{120 \times 50}{6} = 1000 \text{ rpm}$$

**Step 2: Calculate slip.**

Slip is defined as the fractional speed difference between the rotating field and the rotor:
$$s = \frac{N_s - N}{N_s} = \frac{1000 - 1000}{1000} = 0$$

**Step 3: Rotor frequency.**

The rotor EMF frequency equals $sf$:
$$f_r = sf = 0 \times 50 = 0 \text{ Hz}$$

This means the rotor EMF alternates at zero frequency: it is a **DC** quantity. An alternating field cannot induce a DC EMF. The rotor EMF is effectively zero.

**Step 4: Rotor voltage.**

$$E_{2s} = sE_2 = 0 \times E_2 = 0 \text{ V}$$

No voltage is induced in the rotor.

**Step 5: Rotor current and torque.**

With zero rotor voltage, no rotor current flows. With zero current, the Lorentz force ($F = BIl$) is zero. No force means no electromagnetic torque.

**Step 6: Can it sustain this speed?**

No. Without electromagnetic torque, the only forces acting on the rotor are friction (windage, bearing drag). These decelerate the rotor. As soon as the rotor slows even slightly below 1000 rpm, slip becomes positive, rotor EMF appears, rotor current flows, torque develops, and the motor tries to recover. But it can never actually reach or sustain 1000 rpm because at that exact speed the torque is zero.

In practice, an induction motor under load runs at 940–980 rpm (for a 1000 rpm synchronous speed), always slightly below $N_s$.

![Induction machine motoring (Nr < Ns) vs generating (Nr > Ns) operational modes](../ClassNoteByRaidah/diagrams/class12_fig02_motor_vs_generator.jpg)

**The negative slip case:** If an external engine drives the rotor above 1000 rpm, slip becomes negative, the machine acts as an induction generator and feeds power back to the grid. This is used in wind turbines.


---

