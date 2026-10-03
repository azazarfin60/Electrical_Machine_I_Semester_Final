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

**(a) Show that the rms value of the induced emf in the whole of primary winding is $E_1 = 4.44\, f N_1 B_m A$. [CO1, Marks: 03]**

Let the core flux be sinusoidal: $\Phi(t) = \Phi_m \sin \omega t$, $\omega = 2\pi f$, with $\Phi_m = B_m A$.

![Sinusoidal core flux wave over one cycle, showing the quarter cycle in which flux rises from zero to its peak](../Books/Theraja/Ch-32/diagrams/Ch-32_p08_fig14.jpg)

**Step 1. Faraday's law over all $N_1$ turns.** The same mutual flux links every primary turn:
$$e_1 = -N_1 \frac{d\Phi}{dt} = -N_1 \omega \Phi_m \cos \omega t$$

**Step 2. Peak value.** $E_{m1} = N_1 \omega \Phi_m = 2\pi f N_1 \Phi_m$

**Step 3. Convert to rms.** For a sine wave, rms $=$ peak$/\sqrt{2}$:
$$E_1 = \frac{2\pi f N_1 \Phi_m}{\sqrt{2}} = \sqrt{2}\,\pi f N_1 \Phi_m = 4.44\, f N_1 \Phi_m$$

**Step 4. Replace $\Phi_m$ by $B_m A$.**
$$\boxed{E_1 = 4.44\, f N_1 B_m A \ \text{volt}}$$

**Alternative route (average-value method).** In a quarter cycle $T/4 = 1/4f$ the flux goes from $0$ to $\Phi_m$, so the average emf per turn is $4f\Phi_m$. The sine-wave form factor is 1.11, giving $E_1 = 1.11 \times 4fN_1\Phi_m = 4.44fN_1\Phi_m$.

The same argument on the secondary gives $E_2 = 4.44 f N_2 B_m A$. Also note $e_1$ lags $\Phi$ by $90°$.

---

### [2023 Q1(b)]
> 📋 **Appeared in:** 2023 Q1(b)

**(b) Briefly describe the effect of variation of load on core flux and primary current of a transformer. [CO1, Marks: 03]**

![Action of a transformer on load, showing the magnetic balance of the primary and secondary m.m.f. in the core](../Books/Theraja/Ch-32/diagrams/Ch-32_p15_fig17.jpg)

**1. Core flux stays practically constant at every load.** From the emf equation, $V_1 \approx E_1 = 4.44 f N_1 \Phi_m$. Both $V_1$ and $f$ are fixed by the supply, so $\Phi_m \approx V_1/(4.44 f N_1) = \text{constant}$. A transformer is a **constant-flux machine**.

**2. The m.m.f. balance is what keeps it constant.** When $I_2$ flows, its m.m.f. $N_2 I_2$ opposes the core flux by Lenz's law. The flux dips slightly, $E_1$ dips, and the primary at once draws an extra current $I_2' = (N_2/N_1) I_2$ to cancel the secondary m.m.f. The net core m.m.f. returns to $N_1 I_0$, so the flux is restored.

**3. Primary current rises almost in step with the load.** $\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$. $I_0$ is small and fixed; $I_2'$ is proportional to load. So $I_1$ grows nearly linearly from $I_0$ at no load to rated value at full load, and the primary power factor improves from a very poor $\cos\phi_0$ toward the load power factor.

| Quantity | Behaviour with load |
|:---|:---|
| Core flux $\Phi_m$ | Constant |
| Iron loss $P_{Fe}$ | Constant (depends on $\Phi_m$ and $f$ only) |
| Primary current $I_1$ | Rises with load |
| Copper loss $P_{Cu}$ | Rises as $I_1^2$ |

---

### [2023 Q1(c)]
> 📋 **Appeared in:** 2023 Q1(c)

**(c) Define voltage transformation ratio. A transformer has a primary winding of 800 turns and a secondary winding of 200 turns. When the load current on the secondary is 80 A at 0.8 P.F. lagging, the primary current is 25 A at 0.707 P.F. lagging. Determine the no-load current of the transformer and its phase with respect to the voltage. [CO3, Marks: 04]**

**Definition.** The voltage transformation ratio $K$ is the ratio of secondary to primary induced emf, which equals the turns ratio:
$$K = \frac{E_2}{E_1} = \frac{N_2}{N_1} = \frac{I_1}{I_2}$$

![Voltage transformation ratio of an ideal transformer on no load](../Books/Theraja/Ch-32/diagrams/Ch-32_p09_fig15.jpg)

**Given:** $N_1 = 800$, $N_2 = 200$, $I_2 = 80\text{ A}$ at $\cos\phi_2 = 0.8$ lag, $I_1 = 25\text{ A}$ at $\cos\phi_1 = 0.707$ lag.

**Step 1. Ratio and referred load component of primary current.**
$$K = \frac{200}{800} = 0.25$$
$$I_2' = K I_2 = 0.25 \times 80 = 20\text{ A}$$

**Step 2. Resolve both currents with $V_1$ as reference.** $\phi_2 = 36.87°$ ($\sin\phi_2 = 0.6$), $\phi_1 = 45°$ ($\sin\phi_1 = 0.707$):
$$\vec{I}_2' = 20\angle{-36.87°} = (16 - j12)\text{ A}, \qquad \vec{I}_1 = 25\angle{-45°} = (17.68 - j17.68)\text{ A}$$

**Step 3. Use $\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$.**
$$\vec{I}_0 = (17.68 - 16) + j(-17.68 + 12) = (1.675 - j5.680)\text{ A}$$

**Step 4. Magnitude and phase.**
$$I_0 = \sqrt{1.675^2 + 5.680^2} = 5.92\text{ A}, \qquad \phi_0 = \tan^{-1}\frac{5.680}{1.675} = 73.6° \text{ lagging}$$

$$\boxed{I_0 = 5.92\text{ A, lagging } V_1 \text{ by } 73.6° \quad (\cos\phi_0 = 0.283)}$$

---

### [2024 Q1(a)]
> 📋 **Appeared in:** 2024 Q1(a)

**(a) Enlist some practical applications of transformer. [Marks: 02, CO: 1]**

1. **Step-up in generating stations:** raise generator voltage to a high value for economical transmission (lower $I^2R$ loss).
2. **Step-down in receiving substations:** reduce the transmission voltage to distribution levels for consumer use.
3. **Interconnecting two systems of different voltages** (e.g. 400 kV with 345 kV) using auto-transformers.
4. **Voltage matching for instruments:** potential transformer for voltmeters, current transformer for ammeters and relays. They also give electrical isolation.
5. **Furnace and welding supplies:** arc-furnace and spot-welding transformers give the large low-voltage, high-current supply needed.
6. **Frequency/voltage control:** variacs in laboratories, and stabilizers for sensitive equipment.

---

### [Practice: Number of Turns from the EMF Equation]
> **Practice problem (not from a past paper)**

**50 Hz, 6.6 kV/400 V transformer. Cross-section = 25 cm². Max flux density = 1.2 T. Find the number of turns on each side.**

**Peak flux:**
$$\Phi_m = B_m A = 1.2 \times 25 \times 10^{-4} = 3 \times 10^{-3} \text{ Wb} = 3 \text{ mWb}$$

**Primary turns ($E_1 = V_1 = 6600$ V):**
$$N_1 = \frac{E_1}{4.44 f \Phi_m} = \frac{6600}{4.44 \times 50 \times 3 \times 10^{-3}} = \frac{6600}{0.666} = \boxed{9910 \text{ turns}}$$

**Secondary turns ($E_2 = V_2 = 400$ V):**
$$N_2 = \frac{E_2}{4.44 f \Phi_m} = \frac{400}{0.666} = \boxed{600 \text{ turns}}$$

**Check:** $N_1/N_2 = 9910/600 = 16.52 \approx 6600/400 = 16.5$ ✓

---

*(start)* | [🏠 Index](README.md) | [T-02: Construction & Core →](T-02_Transformer_Construction_and_Core.md)
