[← T-12: Rotating Magnetic Field](T-12_Rotating_Magnetic_Field.md) | [🏠 Index](README.md) | [T-14: IM as Rotating Transformer →](T-14_IM_as_Rotating_Transformer.md)

---

# T-13: Slip, Synchronous Speed & Basics

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Slip, Synchronous Speed & Basics** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q1(c)]
> 📋 **Appeared in:** 2017 Q1(c)

**(c) 6-pole, 50 Hz motor, rotor driven at 1000 rpm. Find rotor voltage, frequency, slip, and torque developed. Can it run at this speed by itself? [04]**

**Given:** $P = 6$, $f = 50$ Hz, $N = 1000$ rpm

**i) Synchronous speed:**
$$N_s = \frac{120 \times 50}{6} = 1000 \text{ rpm}$$

**ii) Slip:**
$$s = \frac{N_s - N}{N_s} = \frac{1000 - 1000}{1000} = 0$$

**iii) Rotor frequency:** $f_r = sf = 0 \times 50 = 0$ Hz

**iv) Rotor voltage:** $E_{2s} = sE_2 = 0 \times E_2 = 0$ V

**v) Torque developed:** At $s = 0$, no EMF → no rotor current → **torque = 0**

**Can it run at this speed by itself?** No. At synchronous speed, slip = 0, rotor EMF = 0, rotor current = 0, torque = 0. No torque means it cannot sustain this speed against friction. An induction motor always runs at $N < N_s$.

---

### [2017 Q1(d)]
> 📋 **Appeared in:** 2017 Q1(d)

**(d) What happens if the slip of a 3-φ induction motor becomes negative? [01]**

If $N > N_s$, slip is negative ($s < 0$). The motor acts as an **induction generator**. It delivers electrical power back to the supply instead of consuming it.

---

### [2019 Q5(c)]
> 📋 **Appeared in:** 2019 Q5(c)

**(c) 4-pole, 50 Hz IM. Find: (i) synchronous speed, (ii) rotor speed at s = 4%, (iii) rotor frequency at 600 rpm. [04]**

**Given:** $P = 4$, $f = 50$ Hz

**(i) Synchronous speed:**
$$N_s = \frac{120 \times 50}{4} = \boxed{1500 \text{ rpm}}$$

**(ii) Rotor speed at $s = 4\%$:**
$$N = N_s(1 - s) = 1500(1 - 0.04) = 1500 \times 0.96 = \boxed{1440 \text{ rpm}}$$

**(iii) Rotor frequency at $N = 600$ rpm:**
$$s = \frac{N_s - N}{N_s} = \frac{1500 - 600}{1500} = \frac{900}{1500} = 0.6$$

$$f_r = sf = 0.6 \times 50 = \boxed{30 \text{ Hz}}$$

---

### [2021 Q5(a)]
> 📋 **Appeared in:** 2021 Q5(a)

**(a) For an IM, define: (i) Synchronous speed, (ii) Slip, (iii) Slip speed. [03]**

**(i) Synchronous speed ($N_s$):** The speed of the rotating magnetic field produced by the 3-phase stator winding.
$$N_s = \frac{120f}{P} \text{ rpm}$$

**(ii) Slip ($s$):** The fractional difference between synchronous speed and rotor speed. Expressed as a per-unit value or percentage.
$$s = \frac{N_s - N}{N_s}$$
Range: $s = 1$ at standstill, $s \approx 0.02$–$0.05$ at full load.

**(iii) Slip speed:** The actual speed difference between the rotating field and the rotor:
$$N_{\text{slip}} = N_s - N = s \cdot N_s \text{ rpm}$$

This is the speed at which the rotor bars cut the rotating field, determining the induced EMF magnitude.

![Induction motor working principle showing stator RMF cutting rotor conductors](../ClassNoteByRaidah/diagrams/class05_fig01_im_working_principle.jpg)

---

[← T-12: Rotating Magnetic Field](T-12_Rotating_Magnetic_Field.md) | [🏠 Index](README.md) | [T-14: IM as Rotating Transformer →](T-14_IM_as_Rotating_Transformer.md)
