[← T-19: 3-Phase Starting Methods](T-19_Starting_Methods_3-Phase_IM.md) | [🏠 Index](README.md) | [T-21: Induction Generator →](T-21_Induction_Generator.md)

---

# T-20: Speed Control & Braking

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Speed Control & Braking** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-20: Electric Braking Methods for Induction Motors

*Appears in: 2017 Q2(a), 2018 Q5(a), 2019 Q7(c), 2020 Q8(a)*

#### Why electric braking is used

Mechanical friction brakes (brake shoes/pads) suffer from severe wear, generate heat and toxic dust, and cannot be modulated smoothly. Electric braking uses the electromagnetic fields inside the machine to convert the kinetic energy of the rotating mass into electrical energy (either dissipated safely or regenerated back to the grid), bringing the motor to a swift, controlled stop.

![Operating modes of induction machine: Motoring, Generating, and Braking](../Books/diagrams/Ch-34_p34_fig32.jpg)

#### The three primary electric braking methods

**1. Regenerative Braking ($s < 0$):**
- **Physical principle:** Occurs naturally when the motor is driven by its mechanical load faster than synchronous speed ($N > N_s$).
- **Slip and torque:** The slip becomes negative ($s < 0$). The relative motion of rotor conductors through the stator flux reverses direction, which reverses the induced rotor current and developed electromagnetic torque. The machine operates as an **induction generator**.
- **Energy flow:** Kinetic energy is converted into electrical energy and pumped back into the AC supply grid.
- **Application:** Heavily used when locomotives travel downhill, in elevators lowering heavy passenger cars, and in electric vehicles during deceleration.
- **Limitation:** Can only brake down to synchronous speed $N_s$; cannot bring the motor to a complete standstill ($N=0$).

**2. Dynamic (DC Injection) Braking:**
- **Physical principle:** The 3-phase AC supply is disconnected from the stator, and a DC current is injected into two of the stator terminals.
- **Magnetic field:** The DC current creates a stationary, stationary magnetic field in space.
- **Braking action:** As the rotor continues spinning due to inertia, its conductors cut this stationary magnetic field, inducing alternating currents in the rotor bars. These currents produce a torque opposing the rotor rotation (Lenz's Law).
- **Energy flow:** All kinetic energy is dissipated as heat inside the rotor resistance.
- **Characteristics:** Very smooth, gentle deceleration with zero risk of the motor reversing direction.

**3. Plugging (Counter-Current Braking, $1 < s < 2$):**
- **Physical principle:** Any two supply leads connected to the stator are suddenly swapped while the motor is spinning at full speed.
- **Magnetic field reversal:** Reversing two phases instantaneously reverses the direction of rotation of the stator rotating magnetic field (from $+N_s$ to $-N_s$).
- **Slip during plugging:**
  $$s = \frac{-N_s - N}{-N_s} = \frac{N_s + N}{N_s} = 1 + \frac{N}{N_s} \approx 2 - s_{\text{running}}$$
  For a motor running at 4% slip ($s = 0.04$), the slip at the instant of plugging jumps to $1.96$!
- **Braking torque and severe stresses:** Because the relative speed between field and rotor is nearly $2 N_s$, massive rotor currents flow, producing powerful decelerating torque.
- **Energy dissipation:** As shown in the power flow diagram, the motor absorbs electrical power from the supply while simultaneously absorbing mechanical kinetic energy from the shaft: both are converted to heat inside the rotor windings.
- **Anti-reversal switch:** A centrifugal zero-speed switch must instantly disconnect the supply at the exact moment speed reaches zero, otherwise the motor will immediately accelerate in the reverse direction.

![Power flow diagram during plugging (braking)](../Books/diagrams/Ch-34_p32_fig27.jpg)

---

### [2017 Q2(c)]: Speed Control of Three-Phase Induction Motors

> 📋 **Appeared in:** 2017 Q2(c), 2019 Q7(c)

From the fundamental speed equation:
$$N = N_s(1 - s) = \frac{120 f}{P}(1 - s)$$

Induction motor speed can be controlled by altering three parameters:
1. **Changing synchronous speed $N_s$:**
   - **Supply frequency control ($V/f$):** The gold standard in modern industry. A Variable Frequency Drive (VFD) varies frequency $f$ to alter synchronous speed while varying applied voltage $V$ proportionally to keep air-gap flux constant ($V/f = \text{const}$). This maintains maximum available torque across the entire speed range.
   - **Pole changing:** Reconfiguring stator winding coils (Dahlander two-speed connection) to change the number of magnetic poles $P$. Provides stepped speeds (e.g., 4-pole / 8-pole).
2. **Changing slip $s$:**
   - **Stator voltage control:** Lowering stator voltage weakens the air gap flux, reducing developed torque ($T \propto V^2$). For a fixed load torque, the motor must increase its slip to maintain torque equilibrium, running slower. Very inefficient because reduced speed means high slip losses ($s P_g$).
   - **Rotor resistance control:** Applicable exclusively to wound-rotor (slip-ring) induction motors. External 3-phase rheostats are inserted into the rotor circuit through carbon brushes and slip rings.

![Rotor rheostat circuit for speed control and starting](../Books/diagrams/ch35_p28_fig35_22.jpg)

---

### [2021 Q4(c)]: Worked Numerical Problem: Rotor Resistance Speed Control

> 📋 **Appeared in:** 2021 Q4(c)

**Problem:** A 4-pole, 50 Hz slip-ring IM has $R_2 = 0.30\,\Omega/\text{phase}$ and runs at 1440 rpm at full load. Find the external resistance to be inserted per phase to lower the speed to 1320 rpm at the same load torque.

#### Step-by-step physical solution

**Step 1: Calculate synchronous speed:**
$$N_s = \frac{120 f}{P} = \frac{120 \times 50}{4} = 1500\text{ rpm}$$

**Step 2: Calculate initial slip ($s_1$):**
$$s_1 = \frac{N_s - N_1}{N_s} = \frac{1500 - 1440}{1500} = \frac{60}{1500} = 0.04 \quad (4\%)$$

**Step 3: Calculate required target slip ($s_2$):**
$$s_2 = \frac{N_s - N_2}{N_s} = \frac{1500 - 1320}{1500} = \frac{180}{1500} = 0.12 \quad (12\%)$$

**Step 4: Exploit torque-slip-resistance proportionality:**
In the normal operating region (low slip), the torque equation simplifies to:
$$T \approx \frac{k s E_2^2}{R_2}$$
$$\frac{s}{R_2} = \text{constant for constant torque}$$

Therefore:
$$\frac{s_1}{R_2} = \frac{s_2}{R_2 + R_{ext}}$$

$$\frac{0.04}{0.30} = \frac{0.12}{0.30 + R_{ext}}$$

$$\frac{0.12}{0.04} = \frac{0.30 + R_{ext}}{0.30}$$

$$3 = \frac{0.30 + R_{ext}}{0.30}$$

$$0.30 + R_{ext} = 0.90\,\Omega$$

$$R_{ext} = 0.90 - 0.30 = \boxed{0.60\,\Omega/\text{phase}}$$

**Physical insight:** To reduce speed by a factor that triples the slip (from 4% to 12%) under constant load torque, the total rotor circuit resistance must also triple (from $0.30\,\Omega$ to $0.90\,\Omega$). An external rheostat of $0.60\,\Omega/\text{phase}$ must be added.

---

[← T-19: 3-Phase Starting Methods](T-19_Starting_Methods_3-Phase_IM.md) | [🏠 Index](README.md) | [T-21: Induction Generator →](T-21_Induction_Generator.md)
