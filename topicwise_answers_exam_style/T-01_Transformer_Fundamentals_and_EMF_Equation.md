*(start)* | [🏠 Index](README.md) | [T-02: Construction & Core →](T-02_Transformer_Construction_and_Core.md)

---

# T-01: Transformer Fundamentals & EMF Equation

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Transformer Fundamentals & EMF Equation** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q5(a)]
> 📋 **Appeared in:** 2017 Q5(a)

**(a) What is a transformer? Write down its advantages. [04]**

A transformer is a static electromagnetic device. It transfers electrical energy from one AC circuit to another at the same frequency but different voltage and current levels. Transfer happens through mutual electromagnetic induction between two or more windings wound on a common magnetic core.

**Advantages:**
1. Voltage can be stepped up or down as needed.
2. Electrical power can be transmitted efficiently at high voltage (low current → less $I^2R$ loss).
3. No moving parts → highly reliable, low maintenance.
4. Very high efficiency (98–99% for large power transformers).
5. Electrically isolates two circuits (safety).
6. Economical: simple construction, long service life.

---

### [2017 Q5(b)]
> 📋 **Appeared in:** 2017 Q5(b)

**(b) Explain the operating principle of an ideal transformer. [04]**

**Ideal Transformer Operating Principle:**
An ideal transformer has no resistance, no leakage flux, and no core losses.

![Ideal transformer core, windings, and no-load operation](../Books/Theraja/Ch-32/diagrams/Ch-32_p07_fig13.jpg)

When AC voltage $v_1$ is applied to the primary ($N_1$ turns), an alternating current $i_0$ flows. This creates an alternating mutual flux $\Phi$ in the core.

By Faraday's Law, the alternating flux induces EMF in both windings:
$$e_1 = -N_1 \frac{d\Phi}{dt}, \qquad e_2 = -N_2 \frac{d\Phi}{dt}$$

Dividing: $\frac{e_1}{e_2} = \frac{N_1}{N_2} = \frac{1}{K}$

For an ideal transformer (no drops): $V_1 = E_1$, $V_2 = E_2$.

So: $\frac{V_1}{V_2} = \frac{N_1}{N_2}$

Since input power = output power (lossless): $V_1 I_1 = V_2 I_2$

$$\frac{I_1}{I_2} = \frac{V_2}{V_1} = \frac{N_2}{N_1}$$

---

### [2019 Q1(a)]
> 📋 **Appeared in:** 2019 Q1(a)

**(a) Define transformer. How is energy transferred from primary to secondary? Distinguish primary and secondary windings. [04]**

**Transformer:** A static electromagnetic device that transfers electrical energy between two or more circuits through mutual electromagnetic induction, at the same frequency but different voltage and current levels.

**Energy transfer mechanism:** AC voltage applied to the primary winding drives a current that creates an alternating magnetic flux in the iron core. By Faraday's Law, this alternating flux induces an EMF in the secondary winding. If a load is connected, current flows and energy is delivered to the load.

![Principle of Transformer and mutual flux](../Books/Theraja/Ch-32/diagrams/Ch-32_p02_principle.jpg)

| Feature | Primary Winding | Secondary Winding |
|:---|:---|:---|
| Connection | Connected to AC supply | Connected to load |
| Role | Receives electrical energy | Delivers electrical energy |
| Voltage | Usually higher (step-down) or lower (step-up) | Determined by turns ratio |
| Symbol | $V_1$, $I_1$, $N_1$ | $V_2$, $I_2$, $N_2$ |

---

### [2021 Q1(a)]
> 📋 **Appeared in:** 2021 Q1(a)

**(a) What are the characteristics of an ideal transformer? [03]**

An ideal transformer has the following assumptions:

1. **Zero winding resistance:** Both primary and secondary windings have no resistance ($R_1 = R_2 = 0$). No copper losses.
2. **Zero leakage flux:** All magnetic flux is confined to the core. No flux leakage into air. Both windings link exactly the same flux.
3. **Infinite core permeability:** No magnetizing current is needed to set up the core flux ($I_m = 0$).
4. **Zero core losses:** No hysteresis or eddy current losses in the core.
5. **Constant flux:** Core flux $\Phi$ is sinusoidal and remains constant regardless of load.
6. **100% efficiency:** No losses of any kind. All input power transfers to the output.
7. **Transformation ratio:** $V_1/V_2 = N_1/N_2 = I_2/I_1 = a$

---

### [2021 Q1(c)]
> 📋 **Appeared in:** 2021 Q1(c)

**(c) 25 kVA transformer, 500/50 turns, primary on 3000V/50Hz supply. Find: full-load primary and secondary currents, secondary EMF, maximum flux in core. [04]**

**Given:** $S = 25$ kVA, $N_1 = 500$, $N_2 = 50$, $V_1 = 3000$ V, $f = 50$ Hz

**Turns ratio:**
$$a = \frac{N_1}{N_2} = \frac{500}{50} = 10$$

**Secondary EMF:**
$$E_2 = \frac{E_1}{a} = \frac{V_1}{a} = \frac{3000}{10} = \boxed{300 \text{ V}}$$

**Full-load currents:**
$$I_1 = \frac{S}{V_1} = \frac{25000}{3000} = \boxed{8.33 \text{ A}}$$

$$I_2 = \frac{S}{V_2} = \frac{25000}{300} = \boxed{83.3 \text{ A}}$$

**Maximum flux:** From $E_1 = 4.44 f N_1 \Phi_m$:
$$\Phi_m = \frac{E_1}{4.44 f N_1} = \frac{3000}{4.44 \times 50 \times 500} = \frac{3000}{111000} = \boxed{27.03 \text{ mWb}}$$

---

### [2023 Q1(a)]
> 📋 **Appeared in:** 2023 Q1(a)

**(a) What is transformer? With a neat schematic diagram of a 1-φ transformer, identify and explain all the variables on both sides. [06, CO1]**

**Transformer:** A static electromagnetic device that transfers electrical energy between two circuits at the same frequency but different voltage and current levels, via electromagnetic induction through a shared magnetic core.

**Schematic:**

![Schematic representation of a 1-phase transformer connected to a sinusoidal source on primary and load on secondary with all labeled variables](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_01.jpeg)

**Variable Identification:**

| Symbol | Name | Side |
|:---:|:---|:---:|
| $v_1(t)$, $V_1$ | Applied terminal voltage | Primary |
| $i_1(t)$, $I_1$ | Primary current | Primary |
| $N_1$ | Number of primary turns | Primary |
| $e_1(t)$, $E_1$ | Self-induced counter-EMF | Primary |
| $\Phi(t)$ | Mutual core flux (Wb) | Core |
| $\Phi_m$ | Peak mutual flux | Core |
| $N_2$ | Number of secondary turns | Secondary |
| $e_2(t)$, $E_2$ | Mutually induced EMF | Secondary |
| $v_2(t)$, $V_2$ | Secondary terminal voltage | Secondary |
| $i_2(t)$, $I_2$ | Secondary load current | Secondary |
| $Z_L = R_L + jX_L$ | Load impedance | Secondary |
| $K = N_2/N_1$ | Transformation ratio | Both |

---

### [2024 Q1(a)]
> 📋 **Appeared in:** 2024 Q1(a)

**(a) Show how the schematic representation of a 1-phase transformer connects to a sinusoidal source on the primary and a load on the secondary. Identify and label all variables on both sides. [06, CO1]**

**Schematic:**

![Schematic representation of a 1-phase transformer connected to a sinusoidal source on primary and load on secondary with all labeled variables](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_01.jpeg)

**Primary side variables:**

| Symbol | Description |
|:---:|:---|
| $v_1(t)$, $V_1$ | Instantaneous and RMS applied terminal voltage |
| $i_1(t)$, $I_1$ | Instantaneous and RMS primary current |
| $N_1$ | Number of primary turns |
| $e_1(t)$, $E_1 = 4.44fN_1\Phi_m$ | Self-induced counter-EMF (lags $\Phi$ by 90°) |

**Secondary side variables:**

| Symbol | Description |
|:---:|:---|
| $N_2$ | Number of secondary turns |
| $e_2(t)$, $E_2 = 4.44fN_2\Phi_m$ | Mutually induced EMF |
| $v_2(t)$, $V_2$ | Secondary terminal voltage |
| $i_2(t)$, $I_2$ | Secondary load current |
| $Z_L = R_L + jX_L$ | Load impedance |

**Core variables:**

| Symbol | Description |
|:---:|:---|
| $\Phi(t) = \Phi_m\sin\omega t$ | Mutual core flux |
| $\Phi_m$ | Peak mutual flux (Wb) |
| $f$ | Supply frequency (Hz) |
| $K = N_2/N_1 = E_2/E_1$ | Transformation ratio |

---

### [2024 Q4(a)]
> 📋 **Appeared in:** 2019 Q1(b), 2021 Q1(b), 2023 Q1(b), 2024 Q4(a) (Years: 2019, 2021, 2023, 2024)

**(a) Under assumptions of constant permeability and no leakage flux, derive the transformer EMF equation. [06, CO1]**

**Assumptions:**
- Constant core permeability → constant reluctance → $\Phi \propto I_1$ (linear magnetic circuit).
- Zero leakage flux → same flux $\Phi(t)$ links all $N_1$ primary and $N_2$ secondary turns.

Let: $\Phi(t) = \Phi_m\sin(2\pi ft)$

**Primary EMF:**
$$e_1(t) = -N_1\frac{d\Phi}{dt} = -N_1 \cdot 2\pi f\Phi_m\cos(2\pi ft) = N_1(2\pi f)\Phi_m\sin(2\pi ft - 90°)$$

Peak: $E_{m1} = 2\pi f N_1\Phi_m$

RMS: $E_1 = \frac{2\pi f N_1\Phi_m}{\sqrt{2}} = \sqrt{2}\pi f N_1\Phi_m = 4.44 f N_1\Phi_m$

**Secondary EMF:**
$$\boxed{E_1 = 4.44 f N_1\Phi_m, \qquad E_2 = 4.44 f N_2\Phi_m}$$

**Alternative (form factor method):**

In quarter-cycle ($T/4 = 1/4f$), flux rises from $0$ to $\Phi_m$:
$$\text{Avg EMF per turn} = \frac{\Phi_m}{1/(4f)} = 4f\Phi_m$$

Form factor of sine wave: $K_f = \text{RMS}/\text{Avg} = \pi/(2\sqrt{2}) = 1.11$

RMS EMF per turn $= 1.11 \times 4f\Phi_m = 4.44f\Phi_m$

Multiply by turns: $E_1 = 4.44fN_1\Phi_m$, $E_2 = 4.44fN_2\Phi_m$ ✓

---

### [2024 Q4(b)]
> 📋 **Appeared in:** 2024 Q4(b)

**(b) 50 Hz, 6.6 kV/400V transformer. Cross-section = 25 cm². Max flux density = 1.2 T. Find number of turns on each side. [03, CO1]**

**Peak flux:**
$$\Phi_m = B_m \times A = 1.2 \times 25 \times 10^{-4} = 3 \times 10^{-3} \text{ Wb} = 3 \text{ mWb}$$

**Primary turns ($E_1 = V_1 = 6600$ V):**
$$N_1 = \frac{E_1}{4.44 f \Phi_m} = \frac{6600}{4.44 \times 50 \times 3 \times 10^{-3}} = \frac{6600}{0.666} = \boxed{9910 \text{ turns}}$$

**Secondary turns ($E_2 = V_2 = 400$ V):**
$$N_2 = \frac{E_2}{4.44 f \Phi_m} = \frac{400}{0.666} = \boxed{600 \text{ turns}}$$

**Check:** $N_1/N_2 = 9910/600 = 16.52 \approx 6600/400 = 16.5$ ✓

---

*(start)* | [🏠 Index](README.md) | [T-02: Construction & Core →](T-02_Transformer_Construction_and_Core.md)
