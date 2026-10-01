# T-21: Induction Generator

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Induction Generator** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2018 Q5(c)]
> 📋 **Appeared in:** 2018 Q5(c)

**(c) 440V, 4-pole, 1470 rpm, 30 kW, 3-phase IM used as asynchronous generator. Rated current 40A, pf = 85%. Find: (i) capacitance per phase (Δ-connected), (ii) engine speed for 50 Hz. [04]**

**Given:** $V_L = 440$ V, $P = 4$, $N_{\text{rated}} = 1470$ rpm, $I_L = 40$ A, $\cos\phi = 0.85$

**Synchronous speed (50 Hz, 4-pole):**
$$N_s = \frac{120 \times 50}{4} = 1500 \text{ rpm}$$

**(i) Capacitance per phase (Δ-connected):**

The reactive power drawn by the motor at rated conditions (which must be supplied by capacitors when used as induction generator):

$$Q = \sqrt{3} V_L I_L \sin\phi$$

$\sin\phi = \sqrt{1 - 0.85^2} = \sqrt{1 - 0.7225} = \sqrt{0.2775} = 0.527$

$$Q = \sqrt{3} \times 440 \times 40 \times 0.527 = 1.732 \times 440 \times 40 \times 0.527 = 16082 \text{ VAR} \approx 16.08 \text{ kVAR}$$

For Δ-connected capacitors, reactive power per phase:
$$Q_{\text{phase}} = \frac{Q}{3} = \frac{16082}{3} = 5361 \text{ VAR}$$

Phase voltage for Δ-connected: $V_\text{phase} = V_L = 440$ V

$$Q_\text{phase} = \frac{V_\text{phase}^2}{X_C} \implies X_C = \frac{V^2}{Q_\text{phase}} = \frac{440^2}{5361} = \frac{193600}{5361} = 36.11\,\Omega$$

$$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 36.11} = \frac{1}{11344} = \boxed{88.2\,\mu\text{F per phase}}$$

![Self-excited induction generator with delta capacitor bank supplying isolated load](../Books/diagrams/Ch-34_p33_fig30.jpg)
![Delta capacitor bank supplying reactive power to induction generator](../Books/diagrams/Ch-34_p34_fig31.jpg)

**(ii) Engine speed for 50 Hz generation:**

The motor full-load slip: $s = \frac{N_s - N}{N_s} = \frac{1500 - 1470}{1500} = 0.02$

As an induction generator, rotor runs faster than synchronous speed. Slip is negative with same magnitude:
$$s_{\text{gen}} = -0.02$$

$$N_{\text{rotor}} = N_s(1 - s_{\text{gen}}) = 1500(1 - (-0.02)) = 1500 \times 1.02 = \boxed{1530 \text{ rpm}}$$

The engine must drive the rotor at 1530 rpm to generate at 50 Hz.

