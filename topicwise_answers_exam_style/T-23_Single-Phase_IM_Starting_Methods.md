[← T-22: 1-Phase IM Theory (DFRT)](T-22_Single-Phase_IM_Theory_DFRT.md) | [🏠 Index](README.md) | [T-24: Single Phasing →](T-24_Single_Phasing.md)

---

# T-23: Single-Phase IM Starting Methods

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Single-Phase IM Starting Methods** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q4(b)]
> 📋 **Appeared in:** 2017 Q4(b)

**(b) Why does the permanent-split capacitor motor run more quietly than the capacitor-start motor? [04]**

In a **capacitor-start motor**, the auxiliary winding and capacitor are connected only during starting. A centrifugal switch disconnects them at about 75% of synchronous speed. When this switch opens, there is a mechanical click and a small current surge. The motor then runs on the main winding only: producing a pulsating field: causing vibration and noise.

In a **permanent-split capacitor motor**, the auxiliary winding and capacitor remain connected at all times. The motor operates as a true two-phase machine (90° phase shift) during both starting and running. This produces a smoother, more nearly rotating field at all speeds. No switch is needed. No click or surge occurs. So it runs more quietly and smoothly.

---

### [2017 Q4(c)]
> 📋 **Appeared in:** 2017 Q4(c)

**(c) Explain how an auxiliary winding provides starting torque for single-phase induction motors. [04]**

A single-phase IM has a main winding (M) and an auxiliary (starting) winding (A). The two windings are placed 90° apart in space.

The auxiliary winding has either:
- Higher resistance (resistance split-phase): current in A lags less → phase difference between $I_m$ and $I_a$.
- Capacitor in series (capacitor-start): current in A leads → better phase split.

If the two currents are displaced in time (phase angle $\alpha$), they set up a rotating magnetic field. The rotating field produces a starting torque, just like in a 3-phase motor.

For maximum starting torque, the two currents should be 90° apart in time. This is achieved with a capacitor of proper value. Once the motor reaches about 75% of speed, the auxiliary winding is switched off (by centrifugal switch). The motor then runs on the main winding only.

---

### [2018 Q8(b)]
> 📋 **Appeared in:** 2018 Q8(b)

**(b) Phasor diagram of a resistor split-phase motor at max starting torque. Show: $r_a = (N_a/N_m)^2(r_m + z_m)$. [04]**

For maximum starting torque, the main and auxiliary winding currents must be 90° apart in time.

![Split-Phase Induction Motor Circuit and Phasor Diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_13.jpeg)

**Phasor relationships:**
- $\vec{I}_m$ lags $V$ by $\phi_m$
- $\vec{I}_a$ is 90° displaced from $\vec{I}_m$ for maximum starting torque
- For resistance split-phase, $\phi_a = 90° - \phi_m$

For maximum torque, auxiliary winding impedance angle $\phi_a = 90° - \phi_m$.

The auxiliary winding is designed with high resistance. From phasor geometry, for the auxiliary winding to have angle $\phi_a$:
$$z_a\sin\phi_a = z_a\cos\phi_m$$

Using the effective turns ratio and matching the voltages (EMF balance in terms of turns $N_a/N_m$):
$$r_a = \left(\frac{N_a}{N_m}\right)^2 (r_m + z_m)$$

where $r_m$ is the main winding resistance and $z_m$ is the main winding impedance. This relationship ensures that when the turns ratio is correctly chosen, the phase displacement between main and auxiliary current equals 90°.

---

### [2018 Q8(c)]
> 📋 **Appeared in:** 2018 Q8(c)

**(c) 230V, 50 Hz capacitor-start 1-φ IM. Main winding alone: 100V, 2A, 40W. Auxiliary winding alone: 80V, 1A, 50W. Find capacitance for max starting torque. [04]**

**Main winding parameters:**
$$Z_m = \frac{100}{2} = 50\,\Omega, \quad R_m = \frac{40}{2^2} = 10\,\Omega, \quad X_m = \sqrt{50^2 - 10^2} = \sqrt{2400} = 48.99\,\Omega$$

$$\phi_m = \cos^{-1}\!\left(\frac{R_m}{Z_m}\right) = \cos^{-1}(0.2) = 78.46°$$

**Auxiliary winding parameters:**
$$Z_a = \frac{80}{1} = 80\,\Omega, \quad R_a = \frac{50}{1^2} = 50\,\Omega, \quad X_a = \sqrt{80^2 - 50^2} = \sqrt{3900} = 62.45\,\Omega \text{ (inductive)}$$

**For maximum starting torque:** starting torque is proportional to $I_m I_a \sin\alpha$, where $\alpha$ is the angle between the two currents. Adding $X_C$ changes $|I_a|$ as well as $\alpha$, so forcing $\alpha = 90°$ does **not** give the largest product.

Maximising $I_a \sin\alpha$ gives the auxiliary branch angle:
$$\phi_a = \frac{90° - \phi_m}{2} = \frac{90° - 78.46°}{2} = 5.77° \text{ leading}$$

The auxiliary branch must be net capacitive, so:
$$\tan\phi_a = \frac{X_C - X_a}{R_a} \implies X_C = X_a + R_a\tan\phi_a = X_a + \frac{R_a R_m}{Z_m + X_m}$$

$$X_C = 62.45 + \frac{50 \times 10}{50 + 48.99} = 62.45 + \frac{500}{98.99} = 62.45 + 5.05 = 67.50\,\Omega$$

$$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 67.50} = \boxed{47.1\,\mu\text{F}}$$

---

---

### [2019 Q6(b)]
> 📋 **Appeared in:** 2019 Q6(b)

**(b) Prove: $X_c = X_a + \frac{r_a r_m}{Z_m + X_m}$ for a capacitor split-phase motor. [04]**

For maximum starting torque, $I_m$ and $I_a$ must be 90° apart.

Taking main winding current as reference:
- Main winding: $Z_m = r_m + jX_m$, so $I_m = V/Z_m$ (lagging by $\phi_m$)
- Auxiliary winding + capacitor: $Z_a = r_a + j(X_a - X_c)$, so $I_a$ leads or lags depending on $X_c$

For 90° between $I_m$ and $I_a$: the imaginary part of $Z_a$ must satisfy a specific condition.

Using phasor geometry, when the angle between $I_m$ and $I_a = 90°$:
$$X_c = X_a + \frac{r_a r_m}{X_m + Z_m}$$

*(Derivation requires equating the phase angle condition from the phasor diagram.)*

---

### [2020 Q7(a)]
> 📋 **Appeared in:** 2020 Q7(a)

**(a) Describe any one method for making single-phase IM self-starting. [03]**

**Capacitor-start method:**

A single-phase IM has a main winding (M) and an auxiliary (starting) winding (A) placed 90° apart in space. A capacitor is connected in series with the auxiliary winding.

The capacitor advances the phase of the auxiliary winding current. If the capacitor value is chosen correctly, the auxiliary current leads the main current by nearly 90° in time. This 90° time-phase shift between $I_m$ and $I_a$, combined with the 90° space separation of the windings, produces a rotating magnetic field. This RMF develops a starting torque.

Once the motor reaches about 75% of synchronous speed, a centrifugal switch opens and disconnects the auxiliary winding. The motor continues to run on the main winding alone.

**Starting torque:** $\approx 200$–400% of full-load torque.

![Capacitor-Start Induction Motor Circuit and Phasor Diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_14.jpeg)

---

### [2021 Q7(b)]
> 📋 **Appeared in:** 2021 Q7(b)

**(b) How does a capacitor-start-and-run single-phase IM operate? [04]**

![Capacitor-Start Capacitor-Run Motor Circuit](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_16.jpeg)

A capacitor-start-and-run (or two-value capacitor) motor has:
- Main winding (M): always connected to supply.
- Auxiliary winding (A): permanently connected, with two capacitors:
  - **Starting capacitor $C_{st}$** (large value): in circuit during starting only.
  - **Running capacitor $C_{run}$** (small value): remains in circuit during running.

**Starting operation:**
$C_{st}$ (in parallel with $C_{run}$) provides large phase advance. The combined capacitance gives nearly 90° phase split between $I_m$ and $I_a$. High starting torque (150–300% of FL torque). Better than a simple capacitor-start motor.

**Running operation:**
After reaching ~75% of $N_s$, a centrifugal switch opens and disconnects $C_{st}$. The motor runs with $C_{run}$ in circuit. $C_{run}$ is optimized for running conditions: it maintains better efficiency, power factor, and quieter operation than using no capacitor or the larger $C_{st}$.

**Advantages:** High starting torque + good running performance. Quieter than capacitor-start (auxiliary winding stays on). Better power factor than split-phase.

---

### [2021 Q7(c)]
> 📋 **Appeared in:** 2021 Q7(c)

**(c) 250W, 230V, 50 Hz capacitor-start motor. Main winding: $Z_m = (4.5 + j3.7)\,\Omega$. Auxiliary winding: $Z_a = (9.5 + j3.5)\,\Omega$. Find starting capacitor for quadrature currents. [04]**

**For quadrature currents:** $I_m$ and $I_a$ must be 90° apart in time.

**Main winding angle:**
$$\phi_m = \tan^{-1}\!\left(\frac{3.7}{4.5}\right) = \tan^{-1}(0.822) = 39.43° \text{ lagging}$$

**For $I_a$ to be 90° ahead of $I_m$:** $I_a$ must lead voltage by $(90° - 39.43°) = 50.57°$.

So the auxiliary + capacitor circuit must have total angle = $+50.57°$ leading.

Auxiliary winding without capacitor: $\phi_a = \tan^{-1}(3.5/9.5) = 20.22°$ lagging.

With capacitor in series, net reactance:
$$X_{\text{net}} = X_C - X_a = X_C - 3.5$$

For leading angle of $50.57°$:
$$\tan(50.57°) = \cot(39.43°) = \frac{R_m}{X_m} = \frac{4.5}{3.7} = 1.2162$$

$$\frac{X_C - 3.5}{9.5} = 1.2162 \implies X_C - 3.5 = 1.2162 \times 9.5 = 11.554\,\Omega$$

$$X_C = 11.554 + 3.5 = 15.054\,\Omega$$

$$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 15.054} = \frac{1}{4729.4} = \boxed{211.4\,\mu\text{F}}$$

*(Note: If using intermediate rounded $\tan 50.57° \approx 1.213$: $X_C = 15.02\,\Omega$, and $C = \frac{1}{2\pi \times 50 \times 15.02} = \frac{1}{4718.7} \approx 211.9\,\mu\text{F}$.)*

---

### [2023 Q8(b)]
> 📋 **Appeared in:** 2023 Q8(b)

**(b) Describe any two methods of making a 1-phase IM self-starting. [Marks: 04, CO: 3]**

**Method 1: Capacitor-Start Motor:**

An auxiliary (starting) winding is placed 90° apart in space from the main winding. A capacitor is connected in series with the auxiliary winding. The capacitor advances the phase of auxiliary winding current. With the right capacitor value, the auxiliary current $I_a$ leads the main current $I_m$ by nearly 90° in time.

The 90° time-phase split + 90° space-phase split produces a rotating magnetic field. This generates a starting torque.

Once the motor reaches ~75% of synchronous speed, a centrifugal switch disconnects the auxiliary winding + capacitor. The motor continues on the main winding.

**Starting torque:** 200-400% of full-load torque.

**Advantages:** High starting torque, relatively quiet.

**Disadvantages:** Centrifugal switch is a wear component. Capacitor adds cost.

---

**Method 2: Shaded-Pole Motor:**

A short-circuited copper band (shading band) is placed around a portion of each stator pole face.

When alternating flux through the pole increases, the shading band opposes the change (Lenz's Law). Flux in the shaded portion lags behind flux in the unshaded portion. This creates a phase difference between the two portions of each pole.

The non-uniform, time-shifted flux produces a weak rotating effect across the pole face. This gives a small starting torque, and the motor starts rotating from the unshaded to the shaded portion of the pole.

**Advantages:** Extremely simple, no switches or capacitors. Very reliable. Cheap.

**Disadvantages:** Very low starting torque (typically 40-50% of FL). Low efficiency (copper band always dissipates energy). Low power factor. Small sizes only (fans, small appliances).

---

---

### [Practice: Two Common 1-Phase Motor Types]
> **Practice problem (not from a past paper)**

**Describe two types of single-phase induction motors commonly used in practice.**

**Type 1: Capacitor-Start, Capacitor-Run Motor (Two-Value Capacitor Motor):**

This motor has:
- Main winding (M): always in circuit.
- Auxiliary winding (A): permanently in circuit.
- Starting capacitor $C_s$: in circuit only during starting (switched out by centrifugal switch after ~75% speed).
- Running capacitor $C_r$: permanently in circuit.

**Starting:** $C_s + C_r$ (combined large capacitance) gives nearly 90° phase split between $I_m$ and $I_a$. High starting torque (200-350% of FL).

**Running:** $C_s$ disconnected. $C_r$ (smaller value) is optimized for running. Better running efficiency, power factor, and quieter operation compared to single capacitor motors.

**Applications:** Refrigerator compressors, pumps, air conditioners, power tools.

---

**Type 2: Shaded-Pole Motor:**

![Shaded-Pole Motor Construction and Action](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_17.jpeg)

This is the simplest single-phase induction motor. It has:
- Salient poles (projecting poles like a DC machine).
- A short-circuited copper band (shading ring) placed around a portion of each pole face.

**Operating principle:**

The alternating flux in each pole induces a current in the shading ring. By Lenz's Law, this current opposes the flux change in the shaded portion. The flux in the shaded portion lags behind the flux in the unshaded portion in time, though they are in the same physical space. This time lag produces a sweeping effect from unshaded to shaded portion, like a weak rotating field. This gives a small, unidirectional starting torque.

The rotor (squirrel-cage) follows this sweeping field from unshaded → shaded, and keeps running.

**Characteristics:**
- Very low starting torque (40-60% of FL)
- Very low efficiency (copper ring always dissipates heat)
- Very simple and reliable: no capacitors, no switches, no auxiliary winding
- Only for small sizes (fans, relays, small appliances)
- Fixed rotation direction (cannot be reversed without mechanical modification)

**Applications:** Small cooling fans, hair dryers, small exhaust fans, record turntables, display motors.

---


---

### [2023 Q8(c)]
> 📋 **Appeared in:** 2023 Q8(c)

**(c) How is a single phase induction motor is made self-starting? Describe two methods of making a single phase induction motor self-starting. [CO3, Marks: 04]**

**The core idea.** A single winding gives a pulsating field, which splits into two equal and opposite rotating fields, so the starting torque is zero. To get a starting torque, the field at standstill must be made to **rotate**, not pulsate.

That needs two conditions together:
1. **Two windings displaced in space**, ideally by $90°$ electrical.
2. **Their currents displaced in time**, ideally by $90°$.

A main winding plus an auxiliary (starting) winding, fed through a phase-splitting element, produces an unbalanced two-phase supply. That gives a rotating field and a real starting torque. The auxiliary winding is then cut out by a **centrifugal switch** at about 75% of full speed.

![Main and auxiliary stator windings displaced in space on a single-phase induction motor](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_07.jpeg)

#### Method 1: Split-phase (resistance-start) motor

![Split-phase induction motor circuit with main winding, high-resistance starting winding and centrifugal switch, together with its phasor diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_13.jpeg)

**Construction.** The starting winding is wound with fewer turns of thin wire, so it has **high resistance and low reactance**. The main winding has many turns of thick wire, so it has **low resistance and high reactance**. Both are across the same supply, and a centrifugal switch is in series with the starting winding.

**Working.**
- $I_s$ in the high-resistance starting winding is nearly in phase with $V$.
- $I_m$ in the highly inductive main winding lags $V$ by a large angle.
- The phase split is about $25°$ to $30°$, which is enough to produce a rotating field.

$$\alpha \approx 25°\text{--}30°, \qquad T_{st} \approx 1.5\text{ to } 2 \times T_{FL}$$

At about 75% of full speed the centrifugal switch opens and the motor carries on with the main winding alone.

**Uses.** Fans, blowers, small grinders, office machinery. Cheap, but low starting torque.

#### Method 2: Capacitor-start motor

![Capacitor-start induction motor circuit with a capacitor in series with the starting winding, together with its phasor diagram](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_14.jpeg)

**Construction.** A **capacitor** is put in series with the starting winding, along with the centrifugal switch. An electrolytic capacitor is used because it is needed only for a few seconds.

**Working.** The capacitive branch makes $I_s$ **lead** the supply voltage, while $I_m$ still lags it. So the phase split is far larger:
$$\alpha \approx 80°\text{--}90°$$

With the split close to the ideal $90°$, the field at standstill is almost a true two-phase rotating field:
$$T_{st} \approx 3\text{ to } 4.5 \times T_{FL}$$

**Uses.** Compressors, pumps, refrigerators, air conditioners, conveyors. Anywhere a high starting torque is needed.

#### Comparison

| Feature | Split-phase | Capacitor-start |
|:---|:---|:---|
| Phase-splitting element | High-resistance winding | Series capacitor |
| Phase split $\alpha$ | $25°$–$30°$ | $80°$–$90°$ |
| Starting torque | $1.5$–$2\, T_{FL}$ | $3$–$4.5\, T_{FL}$ |
| Starting current | High | Moderate |
| Cost | Low | Higher |
| Typical use | Fans, blowers | Compressors, pumps |

> [!success] Other methods worth naming
> Capacitor-start capacitor-run (two capacitors, better running power factor), permanent-split capacitor, and shaded-pole (a copper shading ring gives a weak sweeping field, used in tiny fans).

---

[← T-22: 1-Phase IM Theory (DFRT)](T-22_Single-Phase_IM_Theory_DFRT.md) | [🏠 Index](README.md) | [T-24: Single Phasing →](T-24_Single_Phasing.md)
