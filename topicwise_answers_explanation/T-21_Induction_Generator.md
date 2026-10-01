# T-21: Induction Generator

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Induction Generator** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Q5(c): Induction generator: capacitance and engine speed

> 📋 **Appeared in:** 2018 Q5(c)

#### Why an induction machine can generate

At slip $s < 0$ (rotor spinning faster than synchronous speed), the torque reverses direction. Instead of the stator driving the rotor, an external engine drives the rotor above $N_s$. The machine now converts mechanical power to electrical power, feeding it back to the supply (or, with capacitors, to an isolated load).

#### Reactive power must be supplied externally

An induction generator still needs reactive (magnetizing) current to maintain its magnetic field. In grid-connected mode, the grid supplies reactive power. In islanded mode (no grid), capacitors must supply the reactive power.

![Self-excited induction generator circuit with terminal capacitors](../Books/diagrams/Ch-34_p34_fig31.jpg)

The capacitor bank must supply exactly the reactive power that the motor would have drawn at the same operating point.

**Capacitance calculation:**

At rated motor conditions: reactive power $Q = \sqrt{3} V_L I_L \sin\phi$

For Δ-connected capacitors: each capacitor sees line voltage $V_L$.

$Q_C = 3 V_L^2/X_C$ (per-phase capacitors in delta, $Q_C$ total for 3-phase)

$X_C = 3V_L^2/Q$ → $C = 1/(2\pi f X_C)$

#### Engine speed calculation

Full-load slip as motor: $s_{motor} = (N_s - N_{FL})/N_s$. As generator, the rotor must run above $N_s$ by the same magnitude of slip:

$s_{gen} = -s_{motor}$

$N_{gen} = N_s(1 - s_{gen}) = N_s(1 + s_{motor})$

![Induction generator torque-slip curve in generating region (slip < 0)](../Books/diagrams/Ch-34_p33_fig30.jpg)

---

