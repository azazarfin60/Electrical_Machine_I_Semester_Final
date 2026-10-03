[← T-02: Construction & Core](T-02_Transformer_Construction_and_Core.md) | [🏠 Index](README.md) | [T-04: Equivalent Circuit →](T-04_Equivalent_Circuit.md)

---

# T-03: No-Load Operation & Phasor Diagrams

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **No-Load Operation & Phasor Diagrams** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q6(a)]
> 📋 **Appeared in:** 2017 Q6(a)

**(a) Draw the full-load phasor diagram of a single-phase transformer. [03]**

![Full-load phasor diagram of a single-phase transformer with resistance and leakage reactance](../Books/Theraja/Ch-32/diagrams/Ch-32_p21_fig29.jpg)

**Phasor diagram features:**
- $\vec{\Phi}_m$ as reference (horizontal)
- $\vec{E}_1$, $\vec{E}_2$ lagging $\Phi_m$ by 90°
- $\vec{I}_2$ lagging $\vec{V}_2$ by $\phi_2$ (load angle)
- $\vec{V}_2 = \vec{E}_2 - I_2R_2 - jI_2X_2$ (drops subtracted from induced EMF)
- $\vec{I}_0$ (no-load current) components: $I_c$ (core loss), $I_m$ (magnetizing)
- $\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$ where $I_2' = (N_2/N_1)I_2$
- $\vec{V}_1 = -\vec{E}_1 + I_1R_1 + jI_1X_1$

---

### [2018 Q1(c)]
> 📋 **Appeared in:** 2018 Q1(c)

**(c) Draw the equivalent circuit of a transformer with vector diagram for lagging pf. [02]**

#### 1. Equivalent Circuit of a Transformer
![Exact Equivalent Circuit of a Practical Transformer](diagrams/transformer_exact_equivalent_circuit.png)

#### 2. Vector (Phasor) Diagram for Lagging Power Factor ($\cos\phi_2$ lagging)
![Complete Transformer Vector Diagram for Lagging Power Factor](diagrams/transformer_phasor_lagging_pf.png)

**Governing Relations:**
- **Secondary:** $\vec{E}_2 = \vec{V}_2 + \vec{I}_2 R_2 + j\vec{I}_2 X_2 = \vec{V}_2 + \vec{I}_2 Z_2$ (where $\vec{I}_2$ lags $\vec{V}_2$ by $\phi_2$).
- **Primary:** $\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$ with $\vec{I}_2' = -\left(\frac{N_2}{N_1}\right)\vec{I}_2$, and $\vec{V}_1 = -\vec{E}_1 + \vec{I}_1 R_1 + j\vec{I}_1 X_1 = -\vec{E}_1 + \vec{I}_1 Z_1$.

---

### [2019 Q1(c)]
> 📋 **Appeared in:** 2019 Q1(c)

**(c) Why does current flow in primary when secondary is open? Explain how primary current increases as secondary load increases. [04]**

**Why current flows at no-load:**
When $V_1$ is applied, the primary winding behaves as a coil with resistance $R_1$ and inductance $L_1$. To set up the alternating core flux $\Phi_m$ (which induces $E_1 \approx V_1$ to balance applied voltage), a small magnetizing current $I_m$ must flow. Also, a small active component $I_c$ flows to supply core losses (hysteresis + eddy). Together:
$$I_0 = \sqrt{I_c^2 + I_m^2} \approx 2\text{-10\%\ of rated current}$$

**How primary current increases with secondary load:**
When a load is connected and secondary current $I_2$ flows, it creates a demagnetizing MMF $= N_2 I_2$. This tends to reduce the core flux. But $E_1 \approx V_1$ (supply voltage is fixed), so the flux must stay essentially constant. To maintain the flux, the primary must draw additional current $I_2' = I_2 \times N_2/N_1$. Total primary current:
$$I_1 = I_0 + I_2' = I_0 + \frac{N_2}{N_1}I_2$$

As load current $I_2$ increases, $I_1$ increases proportionally.

---

### [2020 Q1(c)]
> 📋 **Appeared in:** 2020 Q1(c)

**(c) Explain the working of a transformer under no-load with neat sketch. [03]**

When primary voltage $V_1$ is applied with secondary open ($I_2 = 0$):

1. Primary current $I_0$ flows (small, 2–10% of rated).
2. $I_0$ has two components:
   - **Magnetizing component $I_m$** (90° lagging from $V_1$): sets up the alternating core flux $\Phi_m$.
   - **Core-loss component $I_c$** (in phase with $V_1$): supplies hysteresis and eddy current losses.
3. Core flux $\Phi_m$ induces primary EMF $E_1 = 4.44 f N_1 \Phi_m$ (opposing $V_1$).
4. Same flux induces secondary EMF $E_2 = 4.44 f N_2 \Phi_m$.
5. Since secondary is open, $V_2 = E_2$. No output current flows.

$$I_0 = \sqrt{I_c^2 + I_m^2}, \qquad \cos\phi_0 = \frac{I_c}{I_0} = \frac{P_0}{V_1 I_0}$$

![Transformer on no-load and its vector diagram](../Books/Theraja/Ch-32/diagrams/Ch-32_p12_fig16.jpg)

---

### [2020 Q1(d)]
> 📋 **Appeared in:** 2020 Q1(d)

**(d) Transformer: turns ratio 4:1 step-down. No-load: 10A at pf 0.2 lag. Secondary load: 200A at 0.85 pf lag. Find primary current and pf. [03]**

**Given:** $I_0 = 10$ A, $\cos\phi_0 = 0.2$, $a = 4$ (step-down), $I_2 = 200$ A, $\cos\phi_2 = 0.85$ lag.

**No-load current components:**
$$I_c = I_0\cos\phi_0 = 10 \times 0.2 = 2.0 \text{ A}$$
$$I_m = I_0\sin\phi_0 = 10 \times \sin(78.46°) = 10 \times 0.9798 = 9.798 \text{ A}$$

**Secondary current referred to primary:** $I_2' = I_2/a = 200/4 = 50$ A at $\phi_2 = 31.79°$ lag.

**Phasor addition** (taking $V_1$ as reference, lagging components negative):

| Component | In-phase (A) | Quadrature (A) |
|:---|:---:|:---:|
| $I_0$ | $+2.0$ | $-9.798$ |
| $I_2'$ | $+50 \times 0.85 = +42.5$ | $-50 \times 0.527 = -26.35$ |
| $I_1$ total | $+44.5$ | $-36.15$ |

$$I_1 = \sqrt{44.5^2 + 36.15^2} = \sqrt{1980.25 + 1306.82} = \sqrt{3287.07} = \boxed{57.33 \text{ A}}$$

$$\cos\phi_1 = \frac{44.5}{57.33} = \boxed{0.776 \text{ lagging}}$$

---

### [2021 Q2(a)]
> 📋 **Appeared in:** 2021 Q2(a)

**(a) Draw the phasor diagram of transformer considering winding resistance and leakage reactance. [04]**

![Complete phasor diagram of transformer with resistance and leakage reactance drops](../Books/Theraja/Ch-32/diagrams/Ch-32_p21_fig29.jpg)

**Phasor diagram step by step:**
> 1. **Reference:** $\vec{\Phi}_m$ horizontal (+X axis).
> 2. **Induced EMFs:** $\vec{E}_1$ and $\vec{E}_2$ pointing downward (lag $\Phi_m$ by 90°).
> 3. **Secondary terminal voltage:** $\vec{V}_2 = \vec{E}_2 - \vec{I}_2 R_2 - j\vec{I}_2 X_2$ (draw from tip of $E_2$, subtract drops).
> 4. **Secondary current:** $\vec{I}_2$ lags $\vec{V}_2$ by $\phi_2$ (load power factor angle).
> 5. **No-load current:** $\vec{I}_0 = I_c - jI_m$ (in phase with $E_1$ component and lagging component).
> 6. **Primary current:** $\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$ where $\vec{I}_2' = (N_2/N_1)\vec{I}_2$.
> 7. **Primary voltage:** $\vec{V}_1 = \vec{E}_1 + \vec{I}_1 R_1 + j\vec{I}_1 X_1$ (draw from tip of $E_1$, add drops).

The angle between $\vec{V}_1$ and $\vec{I}_1$ gives the primary power factor angle $\phi_1$.

---

### [2024 Q1(b)]
> 📋 **Appeared in:** 2024 Q1(b)

**(b) When a power transformer is excited as a manner shown in the figure, describe the induced voltage phenomena. [Marks: 04, CO: 2]**

![Transformer Excitation and Induced Voltage Phenomena](../PrevYearQuestions/diagrams/2024_q1b_transformer.png)

The figure shows a rectangular closed ferromagnetic core with two limbs. Coil1 ($N_1$ turns) sits on the left limb and is fed from a **DC source through a single-pole switch**; coil2 ($N_2$ turns) sits on the right limb and drives a resistive load $R$. Both windings are linked by the mutual flux $\Phi_{mutual}$.

**Because the source is DC, this is a switching transient, not steady-state AC.** The chain of events on closing the switch:

1. **Closing the switch** applies $v$ to coil1 and starts the primary current $i_1$ flowing.
2. **Flux builds up.** $i_1$ magnetises the core, so $\Phi_{mutual}$ rises from its residual value. Rate of change is $d\Phi/dt$ per second.
3. **Self-induction in coil1.** By Faraday's law the primary itself develops a counter-EMF opposing the applied voltage:
   $$e_1 = -N_1 \frac{d\Phi}{dt}$$
4. **Mutual induction in coil2.** The same $\Phi_{mutual}$ links all $N_2$ turns of coil2, so it too develops an EMF:
   $$e_2 = -N_2 \frac{d\Phi}{dt}$$
5. **Load current.** $e_2$ drives $i_2$ out of the upper terminal into the load $R$.
6. **Secondary reaction flux opposes $d\Phi/dt$.** By Lenz's law the secondary current creates a flux that opposes the build-up of core flux. This is exactly the m.m.f. balance that later keeps the core flux constant in a working transformer.

**Ratio to state at the end:** $E_2/E_1 = N_2/N_1$, and both induced EMFs lag the flux by $90°$.

---

### [2024 Q1(c)]
> 📋 **Appeared in:** 2024 Q1(c)

**(c) Find the magnetizing and iron-loss components of no-load current. [Marks: 04, CO: 2]**

The no-load current $I_0$ resolves into $I_w$ (working / iron-loss component, in phase with $V_1$) and $I_m$ (magnetizing component, lagging $V_1$ by 90°):
$$I_0 = \sqrt{I_w^2 + I_m^2}, \qquad I_w = I_0 \cos\phi_0, \qquad I_m = I_0 \sin\phi_0$$

**(i) 2,200/200 V transformer, $I_0 = 0.6$ A, 400 W absorbed.**
$$\cos\phi_0 = \frac{400}{2200 \times 0.6} = 0.30303$$
$$I_w = 0.6 \times 0.30303 = \boxed{0.182\text{ A}}, \qquad I_m = \sqrt{0.6^2 - 0.1818^2} = \boxed{0.572\text{ A}}$$

**(ii) 2,200/250 V transformer, 0.5 A at 0.3 pf on open circuit.**
$$I_w = 0.5 \times 0.3 = \boxed{0.15\text{ A}}, \qquad I_m = \sqrt{0.5^2 - 0.15^2} = \boxed{0.477\text{ A}}$$

> [!NOTE] Label clearly which is which
> The paper asks for magnetizing first in part (i) and "magnetizing and working" in part (ii). Both parts need the same pair, so state which value is $I_m$ and which is $I_w$ every time.

---

### [2024 Q2(a)]
> 📋 **Appeared in:** 2024 Q2(a)

**(a) "The magnetizing current of power transformer is not fully sinusoidal" — justify it. [Marks: 02, CO: 1]**

**Justification.** The core flux $\Phi_m$ is forced to be nearly sinusoidal because it is linked to a sinusoidal applied voltage through the emf equation $V_1 \approx 4.44 f N_1 \Phi_m$. The magnetizing current $I_m$ is whatever current the core needs to sustain that flux.

**A saturating core is a non-linear element.** Its flux-current relation $\Phi = f(I_m)$ is not linear, so the current that produces a sinusoidal flux must itself be **peaked and distorted**, with a third-harmonic component. The sharper the saturation knee, the more pronounced the peak.

**Where the harmonic goes.** Three-phase core-type transformers are built so the third-harmonic magnetizing currents circulate in the delta of the three limbs, which suppresses third-harmonic voltages in the phase windings. Star-connected windings without a delta path cannot carry them, and the third-harmonic flux then appears as a third-harmonic voltage. That is the standard reason a power transformer uses a delta tertiary.

---

### [2024 Q2(b)]
> 📋 **Appeared in:** 2024 Q2(b)

**(b) Draw and explain the phasor diagram of a power transformer, when the transformer is loaded with "R-L" load. [Marks: 04, CO: 1]**

![Phasor diagram of transformer on inductive lagging load](../Books/Theraja/Ch-32/diagrams/Ch-32_p15_fig18.jpg)

For an R-L load the secondary current lags the secondary terminal voltage by
$$\phi_2 = \tan^{-1}\frac{X_L}{R_L}$$

**Step 1.** Draw the mutual flux $\vec{\Phi}_m$ along the horizontal axis as reference.

**Step 2.** Draw $\vec{E}_1$ and $\vec{E}_2$ vertically downward. Both lag $\vec{\Phi}_m$ by $90°$ because an induced emf lags the flux that produces it.

**Step 3.** With no winding drops (ideal transformer): $\vec{V}_2 = \vec{E}_2$ (downward) and $\vec{V}_1 = -\vec{E}_1$ (upward).

**Step 4.** The load is R-L, so $\vec{I}_2$ lags $\vec{V}_2$ by $\phi_2$. Draw it clockwise from $\vec{E}_2$.

**Step 5.** For an ideal transformer $I_0 = 0$, so the ampere-turn balance $N_1\vec{I}_1 = -N_2\vec{I}_2$ gives $\vec{I}_1 = -(N_2/N_1)\vec{I}_2$, that is $\vec{I}_1$ points $180°$ opposite to $\vec{I}_2$.

**Step 6.** The angle between $\vec{V}_1$ (upward) and $\vec{I}_1$ equals $\phi_2$. **An ideal transformer reflects the load power factor to the primary: $\phi_1 = \phi_2$.**

**Phasor summary:**

| Phasor | Angle from $\vec{\Phi}_m$ |
|:---:|:---:|
| $\vec{\Phi}_m$ | $0°$ |
| $\vec{E}_1, \vec{E}_2, \vec{V}_2$ | $-90°$ |
| $\vec{V}_1$ | $+90°$ |
| $\vec{I}_2$ | $-90° - \phi_2$ |
| $\vec{I}_1$ | $+90° - \phi_2$ |

---

[← T-02: Construction & Core](T-02_Transformer_Construction_and_Core.md) | [🏠 Index](README.md) | [T-04: Equivalent Circuit →](T-04_Equivalent_Circuit.md)
