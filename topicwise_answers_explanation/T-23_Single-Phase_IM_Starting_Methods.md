[← T-22: 1-Phase IM Theory (DFRT)](T-22_Single-Phase_IM_Theory_DFRT.md) | [🏠 Index](README.md) | [T-24: Single Phasing →](T-24_Single_Phasing.md)

---

# T-23: Single-Phase IM Starting Methods

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Single-Phase IM Starting Methods** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-23: Physical Principle of Starting Single-Phase Induction Motors

*Appears in: 2017 Q4(b), 2017 Q4(c), 2018 Q8(b), 2020 Q7(a), 2021 Q7(b), 2023 Q8(c)*

#### Why single-phase motors cannot self-start

As established by the Double-Field Revolving Theory, a single stator winding fed by single-phase AC creates a purely pulsating magnetic field. At standstill ($s = 1$), this decomposes into two equal and opposite rotating magnetic fields ($\Phi_f$ and $\Phi_b$) rotating at $+N_s$ and $-N_s$. 

Because both fields produce identical and opposite standstill torques ($T_f = T_b$), the net starting torque is zero:
$$T_{start} = T_f(s=1) - T_b(s=1) = 0$$

The motor hums and remains stationary unless external starting torque is introduced.

#### The auxiliary winding and phase-splitting principle

To generate starting torque, we must temporarily convert the machine into a quasi-two-phase motor:
1. **Space quadrature:** A second stator winding: called the **auxiliary (or starting) winding**: is placed in the stator slots physically displaced by **90° in space** from the main winding.
2. **Time quadrature:** The impedance of the auxiliary winding circuit is altered (using a resistor, reactor, or capacitor) so that its current $I_a$ is phase-displaced in time from the main winding current $I_m$ by an angle $\alpha$.

The developed starting torque is directly proportional to:
$$T_{start} \propto I_m I_a \sin\alpha$$

To maximize starting torque for given currents, the time phase angle must be:
$$\alpha = 90° \implies \sin(90°) = 1 \quad \text{(Quadrature Condition)}$$

When $I_a$ and $I_m$ are 90° apart in time and their physical windings are 90° apart in space, a true, forward-rotating magnetic field is established, accelerating the squirrel-cage rotor from rest.

---

### 1. Resistor Split-Phase Induction Motor

#### Operation and phasor diagram

The auxiliary winding is wound with finer wire (fewer turns, high resistance, low reactance), while the main winding has thick wire deeply embedded in slots (low resistance, high reactance).

![Split-Phase Induction Motor Circuit and Phasor Diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_13.jpeg)

- Main current $\vec{I}_m$ is highly inductive and lags applied voltage $\vec{V}$ by a large angle $\phi_m \approx 70°–80°$.
- Auxiliary current $\vec{I}_a$ is mostly resistive and lags $\vec{V}$ by a smaller angle $\phi_a \approx 30°–40°$.
- The phase angle between the two currents is $\alpha = \phi_m - \phi_a \approx 30°–40°$.
- Once the motor accelerates to approximately 75% of synchronous speed, an internal **centrifugal switch** clicks open, disconnecting the auxiliary winding to prevent overheating.

---

### 2. Capacitor-Start Induction Motor

#### Why adding a series capacitor provides massive starting torque

Instead of relying on resistance to reduce lag, a high-capacitance AC electrolytic capacitor is placed in series with the auxiliary winding.

![Capacitor-Start Induction Motor Circuit and Phasor Diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_14.jpeg)

The capacitive reactance $X_C = \frac{1}{\omega C}$ overcomes the auxiliary winding inductive reactance ($X_C > X_a$), causing the net auxiliary impedance to be capacitive.
- Main current $\vec{I}_m$ lags voltage $\vec{V}$ by $\phi_m \approx 70°–80°$.
- Auxiliary current $\vec{I}_a$ leads voltage $\vec{V}$ by angle $\phi_a$.
- By properly sizing the capacitor, the total phase angle between the currents becomes:
  $$\alpha = \phi_m + \phi_a = 90°$$
- Starting torque reaches **300% to 450% of rated full-load torque**.
- At 75% speed, the centrifugal switch disconnects the auxiliary circuit.

---

### 3. Permanent-Split Capacitor (PSC) Motor

In a PSC motor, a smaller, oil-filled paper capacitor remains permanently connected in series with the auxiliary winding; **no centrifugal switch is used**.

#### Why PSC motors run more quietly than capacitor-start motors:

1. **Continuous 2-phase operation:** Because the auxiliary winding is never disconnected, the motor operates as a balanced two-phase motor even at full running speed. The magnetic field remains nearly circular (rotating) rather than pulsating.
2. **Vibration and hum elimination:** In a capacitor-start motor running on the main winding alone, the backward field $\Phi_b$ creates a double-frequency (100 Hz / 120 Hz) pulsating torque that induces audible hum and mechanical vibration. The PSC motor largely eliminates this pulsating torque.
3. **No mechanical switch transients:** Eliminates the mechanical click, contact sparking, and current surges associated with centrifugal switches.

---

### 4. Capacitor-Start, Capacitor-Run Motor (Two-Value Capacitor)

This design combines the high starting torque of a capacitor-start motor with the high efficiency and smooth running of a PSC motor:
- **Starting:** Both the starting capacitor $C_{st}$ (large electrolytic capacitor, $\sim 200–300\,\mu\text{F}$) and running capacitor $C_{run}$ (small continuous-rated paper capacitor, $\sim 20–40\,\mu\text{F}$) operate in parallel. Total capacitance is large, giving $\alpha \approx 90°$ and huge starting torque.
- **Running:** At 75% speed, the centrifugal switch disconnects $C_{st}$, leaving $C_{run}$ permanently in circuit. This optimizes running power factor, efficiency, and quietness.

![Capacitor-Start Capacitor-Run Motor Circuit](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_16.jpeg)

---

### 5. Shaded-Pole Induction Motor

The simplest, cheapest single-phase motor. It has salient stator poles, each fitted with a copper ring (shading coil) covering about one-third of the pole face.

![Shaded-Pole Motor Construction and Action](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_17.jpeg)

#### The sweeping flux mechanism:

1. **When pole flux increases:** An induced current flows in the shading band (Lenz's Law), opposing the growth of flux in the shaded portion. Most flux is forced through the unshaded portion.
2. **When pole flux peaks:** Rate of change is zero, induced current is zero, and flux is uniformly distributed.
3. **When pole flux decreases:** The collapsing field induces current in the shading band trying to maintain the flux. Flux persists in the shaded portion while falling rapidly in the unshaded portion.

This produces a continuous **time lag** between unshaded and shaded flux, sweeping across the pole face from the **unshaded portion to the shaded portion**. The squirrel-cage rotor follows this sweeping field.

- **Starting torque:** Very low (40–60% of full load).
- **Efficiency:** Extremely poor (5–25%) because the shading band constantly dissipates $I^2 R$ heat.
- **Applications:** Small cooling fans, microwave exhaust fans, hair dryers.

---

### [2021 Q7(c)]: Worked Problem: Capacitor Calculation for Quadrature Currents

> 📋 **Appeared in:** 2021 Q7(c)

**Problem:** A 250W, 230V, 50 Hz capacitor-start motor has:
- Main winding: $\vec{Z}_m = 4.5 + j3.7\,\Omega$
- Auxiliary winding: $\vec{Z}_a = 9.5 + j3.5\,\Omega$
Find the value of the starting capacitor required to produce quadrature currents ($90°$ phase displacement) at starting.

#### Step-by-step physical solution

**Step 1: Determine main winding impedance angle:**
$$\tan\phi_m = \frac{X_m}{R_m} = \frac{3.7}{4.5} = 0.8222$$
$$\phi_m = \tan^{-1}(0.8222) \approx 39.43° \text{ (lagging)}$$

The main winding current $\vec{I}_m$ lags the supply voltage $\vec{V}$ by $39.43°$.

**Step 2: Condition for quadrature currents ($\alpha = 90°$):**
For $\vec{I}_a$ to lead $\vec{I}_m$ by $90°$, $\vec{I}_a$ must lead the supply voltage $\vec{V}$ by:
$$\phi_a = 90° - \phi_m = 90° - 39.43° = 50.57° \text{ (leading)}$$

**Step 3: Sizing the capacitive reactance $X_C$:**
With a capacitor of reactance $X_C$ connected in series with the auxiliary winding, the net auxiliary circuit impedance is:
$$\vec{Z}_{a,\text{total}} = R_a + j(X_a - X_C) = 9.5 - j(X_C - 3.5)\,\Omega$$

For $\vec{I}_a$ to lead voltage by $50.57°$, the impedance angle must be $-50.57°$:
$$\tan(50.57°) = \frac{X_C - X_a}{R_a} = \frac{X_C - 3.5}{9.5}$$

Since $\tan(50.57°) \approx 1.216$:
$$X_C - 3.5 = 1.216 \times 9.5 = 11.55\,\Omega$$
$$X_C = 11.55 + 3.5 = 15.05\,\Omega$$

**Step 4: Calculate capacitance $C$:**
$$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 15.05} = \frac{1}{4728} \approx 2.115 \times 10^{-4}\text{ F} = \boxed{211.5\,\mu\text{F}}$$

---

[← T-22: 1-Phase IM Theory (DFRT)](T-22_Single-Phase_IM_Theory_DFRT.md) | [🏠 Index](README.md) | [T-24: Single Phasing →](T-24_Single_Phasing.md)
