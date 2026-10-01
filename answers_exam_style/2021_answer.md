[← 2020 Answer](2020_answer.md) | [🏠 Index](README.md) | [2023 Answer →](2023_answer.md)

---

# ECE 2207: 2021 Semester Final: Exam Style Answers
**RUET · ECE Dept · 2nd Year Odd Semester 2021**
**Full Marks:** 72 · **Time:** 3 Hours · **Attempt any 6 (3 from each section)**

---

## SECTION - A (Transformers: Q1 to Q4)

### Question 1

**(a) What are the characteristics of an ideal transformer? [03]**

![Core and windings of an ideal transformer](../Books/diagrams/Ch-32_p07_fig13.jpg)

An ideal transformer has the following assumptions:

1. **Zero winding resistance:** Both primary and secondary windings have no resistance ($R_1 = R_2 = 0$). No copper losses.
2. **Zero leakage flux:** All magnetic flux is confined to the core. No flux leakage into air. Both windings link exactly the same flux.
3. **Infinite core permeability:** No magnetizing current is needed to set up the core flux ($I_m = 0$).
4. **Zero core losses:** No hysteresis or eddy current losses in the core.
5. **Constant flux:** Core flux $\Phi$ is sinusoidal and remains constant regardless of load.
6. **100% efficiency:** No losses of any kind. All input power transfers to the output.
7. **Transformation ratio:** $V_1/V_2 = N_1/N_2 = I_2/I_1 = a$

---

**(b) Derive the equation for RMS EMF induced in both primary and secondary windings. Show EMF/turn is the same in both. [05]**

Let core flux: $\Phi(t) = \Phi_m\sin(\omega t)$. Same flux links all turns of both windings (no leakage).

**Primary induced EMF:**

By Faraday's Law:
$$e_1(t) = -N_1\frac{d\Phi}{dt} = -N_1\omega\Phi_m\cos(\omega t) = N_1\omega\Phi_m\sin\!\left(\omega t - 90°\right)$$

Peak value: $E_{m1} = N_1\omega\Phi_m = 2\pi f N_1\Phi_m$

RMS value:
$$E_1 = \frac{E_{m1}}{\sqrt{2}} = \frac{2\pi f N_1\Phi_m}{\sqrt{2}} = \sqrt{2}\pi f N_1\Phi_m$$

Since $\sqrt{2}\pi = 4.44$:
$$\boxed{E_1 = 4.44 f N_1 \Phi_m}$$

**Secondary induced EMF:** Same $\Phi(t)$ links all $N_2$ secondary turns:

$$e_2(t) = -N_2\frac{d\Phi}{dt} = N_2\omega\Phi_m\sin(\omega t - 90°)$$

RMS:
$$\boxed{E_2 = 4.44 f N_2 \Phi_m}$$

**EMF per turn:**
$$\frac{E_1}{N_1} = 4.44 f \Phi_m = \frac{E_2}{N_2}$$

EMF per turn $= 4.44f\Phi_m$ for both windings. *(Proved)*

---

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

### Question 2

**(a) Draw the phasor diagram of transformer considering winding resistance and leakage reactance. [04]**

![Complete vector diagrams of transformer](../Books/diagrams/Ch-32_p21_fig29.jpg)
> 1. **Reference:** $\vec{\Phi}_m$ horizontal (+X axis).
> 2. **Induced EMFs:** $\vec{E}_1$ and $\vec{E}_2$ pointing downward (lag $\Phi_m$ by 90°).
> 3. **Secondary terminal voltage:** $\vec{V}_2 = \vec{E}_2 - \vec{I}_2 R_2 - j\vec{I}_2 X_2$ (draw from tip of $E_2$, subtract drops).
> 4. **Secondary current:** $\vec{I}_2$ lags $\vec{V}_2$ by $\phi_2$ (load power factor angle).
> 5. **No-load current:** $\vec{I}_0 = I_c - jI_m$ (in phase with $E_1$ component and lagging component).
> 6. **Primary current:** $\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$ where $\vec{I}_2' = (N_2/N_1)\vec{I}_2$.
> 7. **Primary voltage:** $\vec{V}_1 = \vec{E}_1 + \vec{I}_1 R_1 + j\vec{I}_1 X_1$ (draw from tip of $E_1$, add drops).

The angle between $\vec{V}_1$ and $\vec{I}_1$ gives the primary power factor angle $\phi_1$.

---

**(b) Explain the procedure of the no-load test of a transformer. Why is this test performed? [04]**

**Procedure:**
1. Keep secondary (HV) side open-circuited.
2. Apply rated voltage to the primary (LV) side via a variac.
3. Connect measuring instruments on the primary side: voltmeter ($V_0$), ammeter ($I_0$), wattmeter ($W_0$).
4. Record readings when supply reaches rated value: $V_0 = V_{\text{rated}}$, $I_0$, $W_0$.

**Calculations:**

Core loss: $P_{Fe} = W_0$ (constant, independent of load)

$$\cos\phi_0 = \frac{W_0}{V_0 I_0}, \quad I_c = I_0\cos\phi_0, \quad I_m = I_0\sin\phi_0$$

$$R_c = \frac{V_0}{I_c}, \quad X_m = \frac{V_0}{I_m}$$

Turns ratio check: $a = V_1/V_2$ (measure both voltages)

**Why this test is performed:**
1. To measure core (iron) losses: constant at all loads.
2. To determine shunt branch parameters ($R_c$ and $X_m$) of the equivalent circuit.
3. To verify the turns ratio.
4. To calculate no-load current and power factor.

The test is economical: rated voltage is applied but rated current does not flow (only 2–10%). Power consumption during the test is low.

---

**(c) 20 kVA, 2400/240V, 50 Hz transformer. SC test (HV side): $V = 72$ V, $W = 275$ W, $I =$ rated. Find constants referred to HV side and voltage regulation at 0.8 pf lag. [04]**

**Rated HV current:**
$$I_1 = \frac{20000}{2400} = 8.33 \text{ A}$$

**From SC test (HV side):**
$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{275}{8.33^2} = \frac{275}{69.39} = 3.964\,\Omega$$

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{72}{8.33} = 8.643\,\Omega$$

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2} = \sqrt{8.643^2 - 3.964^2} = \sqrt{74.70 - 15.71} = \sqrt{58.99} = 7.681\,\Omega$$

**Voltage regulation at 0.8 pf lag ($\cos\phi = 0.8$, $\sin\phi = 0.6$):**
$$\text{VR\%} = \frac{I_1(R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100$$

$$= \frac{8.33(3.964 \times 0.8 + 7.681 \times 0.6)}{2400} \times 100$$

$$= \frac{8.33(3.171 + 4.609)}{2400} \times 100 = \frac{8.33 \times 7.780}{2400} \times 100$$

$$= \frac{64.81}{2400} \times 100 = \boxed{2.70\%}$$

---

### Question 3

**(a) Limitations of Y-Y connected transformer. How to overcome them? [03]**

**Limitations:**

1. **Third harmonic voltages:** The magnetizing current of a transformer is non-sinusoidal: it contains third harmonics. In a Y-Y transformer, the neutral point is not usually connected. Third harmonic currents have no path to flow (they are zero-sequence). As a result, third harmonic EMFs appear in the line-to-neutral voltages, causing waveform distortion.

2. **Voltage unbalance:** Under unbalanced loads, the neutral point shifts. This causes unequal voltage distribution among phases.

3. **No phase shift:** Y-Y gives 0° phase displacement. This limits flexibility in interconnection with other transformer groups.

**How to overcome:**

1. **Connect the neutral to ground (4-wire system):** Allows zero-sequence (third harmonic) currents to flow. Eliminates harmonic voltages in phase-to-neutral voltages.

2. **Add a delta-connected tertiary winding:** The delta provides a closed circulating path for third harmonic currents. This suppresses harmonic voltages without requiring a grounded neutral.

3. **Use Δ winding on at least one side (Y-Δ or Δ-Y connection):** Inherently eliminates third harmonic voltage problems.

---

**(b) Is it possible to continue 3-phase power if one transformer is damaged? Justify and describe one technique. [06]**

**Yes: it is possible** using the **open-delta (V-V) connection**.

**Justification:**

In a Δ-Δ bank of three single-phase transformers, if one fails, the remaining two can be reconnected in open-delta. Three-phase voltages remain balanced. Load can be served, but at only 57.7% of the original bank capacity.

**How it works:**

Let transformers $T_{AB}$, $T_{BC}$, $T_{CA}$ form the bank. Remove $T_{CA}$.

**Primary side:** The three line voltages are fixed by the 3-phase supply. Even with $T_{CA}$ open, $V_{AB}$ and $V_{BC}$ still exist. By KVL around the delta loop: $V_{CA} = -(V_{AB} + V_{BC})$: so the voltage across the open $T_{CA}$ position is also defined. But no transformer carries this voltage.

**Secondary side:** $T_{AB}$ produces secondary voltage $V_{ab} = K\cdot V_{AB}$. $T_{BC}$ produces $V_{bc} = K\cdot V_{BC}$. By KVL: $V_{ca} = -(V_{ab} + V_{bc}) = K\cdot V_{CA}$. All three secondary voltages exist and are balanced.

**Capacity reduction:**

Each remaining transformer operates at rated voltage and rated current, but the load power factor for each differs from the closed-delta case. Net 3-phase output:
$$S_{open-\Delta} = \sqrt{3} \times S_{\text{single transformer}} = 0.577 \times 3S_{\text{single}} = 57.7\% \text{ of closed-Δ}$$

**Practical importance:** Used during maintenance (one transformer removed for repair) without interrupting supply.

---

**(c) Draw the complete torque-speed curve of an induction motor. [03]**

![Torque-Speed characteristics](../Books/diagrams/Chapman_Ch07_p202_torque_speed_r2_comp.jpg)
> - At $N = 0$ (s = 1): Starting torque $T_{st}$ (positive, typically 1.5-2x full-load torque).
> - Torque increases as speed increases from 0, reaching maximum $T_{\max}$ (pull-out torque) at speed $N_{mT} = N_s(1 - R_2/X_2)$.
> - After $T_{\max}$, torque decreases rapidly as speed approaches $N_s$.
> - At $N = N_s$ (s = 0): Torque = 0.
> - Beyond $N_s$ (s < 0, negative slip): Machine acts as induction generator: negative torque (braking).
> - At $N < 0$ (plugging region, s > 1): Torque is positive but motor is in plugging mode.
> 
> Mark: Full-load operating point at about 95-98% of $N_s$, $T_{\max}$ at $N_{mT}$, starting torque at $N = 0$.

---

### Question 4

**(a) Conditions for parallel operation of two 3-phase transformers. [04]**

1. **Same voltage ratio:** Primary and secondary rated voltages must be equal. Otherwise a circulating current flows in the secondary loop even at no load.

2. **Same per-unit (or percentage) impedance:** Ensures load sharing is proportional to rated kVA. If impedances differ, the transformer with lower impedance takes a disproportionate share and may overload.

3. **Same polarity:** Corresponding terminals must have the same instantaneous polarity. For 3-phase, this means the same phase sequence of secondary voltages.

4. **Same phase sequence:** Both transformers must be connected to the same phase sequence (A-B-C). A reversed sequence causes a voltage difference and large circulating currents.

5. **Same vector group (zero phase displacement):** Both transformers must have the same vector group or have zero phase angle between their secondary voltages. A 30° phase difference (e.g., Yy0 with Yd11) causes very large circulating currents.

---

**(b) What methods can be used for generating magnetic field? [04]**

Magnetic fields can be generated by several methods:

1. **Permanent magnets:** Iron, alnico, neodymium magnets produce static fields. Used in BLDC motors, PMSMs, speakers.

2. **DC electromagnets:** DC current through a coil wound on an iron core creates a constant magnetic field. Used in synchronous motors, DC machines, relays.

3. **AC electromagnets:** Alternating current through a coil creates a pulsating magnetic field. Used in transformer cores, AC contactors.

4. **Rotating magnetic field (3-phase windings):** Three-phase AC currents in three spatially displaced windings create a continuously rotating field of constant magnitude. Used in 3-phase induction and synchronous motors.

5. **Rotating magnetic field (2-phase):** Two-phase currents (90° apart) in windings 90° apart in space produce a rotating field. Less common, used in some servo systems.

6. **Single-phase with auxiliary winding:** Capacitor or resistance creates phase split, giving a rotating field. Used in single-phase induction motors.

---

**(c) 4-pole, 50 Hz slip-ring IM. $R_2 = 0.30\,\Omega/\text{phase}$, runs at 1440 rpm full load. Find external resistance to lower speed to 1320 rpm at same torque. [04]**

**Given:** $P = 4$, $f = 50$ Hz, $R_2 = 0.30\,\Omega$, $N_1 = 1440$ rpm (full load)

$$N_s = \frac{120 \times 50}{4} = 1500 \text{ rpm}$$

**Full-load slip:**
$$s_1 = \frac{1500 - 1440}{1500} = \frac{60}{1500} = 0.04$$

**New slip at 1320 rpm:**
$$s_2 = \frac{1500 - 1320}{1500} = \frac{180}{1500} = 0.12$$

**Condition for same torque at both operating points:**

From the torque equation, at constant torque (and ignoring the $s^2 X_2^2$ term for small slip, or using the proportionality at low slip):

$$T \propto \frac{sE_2^2 R_{\text{total}}}{R_{\text{total}}^2} = \frac{sE_2^2}{R_{\text{total}}}$$

For constant torque: $\frac{s_1}{R_2} = \frac{s_2}{R_2 + R_{ext}}$

$$\frac{0.04}{0.30} = \frac{0.12}{0.30 + R_{ext}}$$

$$0.30 + R_{ext} = \frac{0.12 \times 0.30}{0.04} = \frac{0.036}{0.04} = 0.90\,\Omega$$

$$R_{ext} = 0.90 - 0.30 = \boxed{0.60\,\Omega/\text{phase}}$$

---

## SECTION - B (Induction Motors: Q5 to Q8)

### Question 5

**(a) For an IM, define: (i) Synchronous speed, (ii) Slip, (iii) Slip speed. [03]**

**(i) Synchronous speed ($N_s$):** The speed of the rotating magnetic field produced by the 3-phase stator winding.
$$N_s = \frac{120f}{P} \text{ rpm}$$

**(ii) Slip ($s$):** The fractional difference between synchronous speed and rotor speed. Expressed as a per-unit value or percentage.
$$s = \frac{N_s - N}{N_s}$$
Range: $s = 1$ at standstill, $s \approx 0.02$–$0.05$ at full load.

**(iii) Slip speed:** The actual speed difference between the rotating field and the rotor:
$$N_{\text{slip}} = N_s - N = s \cdot N_s \text{ rpm}$$

This is the speed at which the rotor bars cut the rotating field, determining the induced EMF magnitude.

---

**(b) Determine the starting torque of an IM. [04]**

Starting torque is the torque developed when the rotor is at standstill ($s = 1$).

From the general torque equation at $s = 1$:

$$T_{st} = \frac{k \cdot 1 \cdot E_2^2 R_2}{R_2^2 + (1)^2 X_2^2} = \frac{kE_2^2 R_2}{R_2^2 + X_2^2}$$

where $k = \frac{3}{2\pi N_s}$ and $E_2$ is standstill rotor EMF per phase.

**Effect of rotor resistance on starting torque:**

To find the rotor resistance $R_2$ that maximizes starting torque:
$$\frac{dT_{st}}{dR_2} = 0 \implies R_2^2 + X_2^2 - 2R_2^2 = 0 \implies R_2 = X_2$$

**Maximum starting torque** (at $R_2 = X_2$):
$$T_{st,\max} = \frac{kE_2^2 X_2}{X_2^2 + X_2^2} = \boxed{\frac{kE_2^2}{2X_2}}$$

This equals $T_{\max}$: the maximum running torque. In wound-rotor motors, external resistance is added to achieve $R_{\text{total}} = X_2$ for maximum starting torque.

---

**(c) Show that 2-phase supply produces a rotating magnetic field at synchronous speed. [05]**

**Setup:** Two windings placed 90° apart in space. A balanced 2-phase supply:
$$i_a = I_m\sin\omega t, \qquad i_b = I_m\sin(\omega t - 90°) = -I_m\cos\omega t$$

Each winding produces a pulsating flux along its axis:
$$\Phi_a = \Phi_m\sin\omega t \quad \text{(along X-axis)}$$
$$\Phi_b = \Phi_m\sin(\omega t - 90°) = -\Phi_m\cos\omega t \quad \text{(along Y-axis)}$$

**Resultant flux:**

X-component: $\Phi_x = \Phi_a = \Phi_m\sin\omega t$

Y-component: $\Phi_y = \Phi_b = -\Phi_m\cos\omega t$

**Magnitude:**
$$\Phi_r = \sqrt{\Phi_x^2 + \Phi_y^2} = \sqrt{\Phi_m^2\sin^2\omega t + \Phi_m^2\cos^2\omega t} = \Phi_m = \text{constant}$$

**Space angle:**
$$\theta = \tan^{-1}\!\left(\frac{\Phi_y}{\Phi_x}\right) = \tan^{-1}\!\left(\frac{-\cos\omega t}{\sin\omega t}\right) = \omega t - 90°$$

$$\frac{d\theta}{dt} = \omega = 2\pi f \implies N_s = \frac{120f}{P} \text{ rpm}$$

**Conclusion:** The 2-phase supply produces a rotating field of constant magnitude $\Phi_m$ (not $1.5\Phi_m$ as in 3-phase), rotating at synchronous speed $N_s$. *(Proved)*

Note: Magnitude is $\Phi_m$ (not $1.5\Phi_m$) because 2-phase has only 2 phases, not 3.

---

### Question 6

**(a) What happens to torque and speed of an IM if supply frequency increases suddenly? [04]**

From the key equations:

$$N_s = \frac{120f}{P}, \qquad T_{\max} = \frac{kE_2^2}{2X_2} = \frac{k(KV)^2}{2(2\pi f L_2)}$$

If supply frequency $f$ increases suddenly (with voltage $V$ unchanged):

1. **Synchronous speed $N_s$ increases** (directly proportional to $f$). The rotor cannot instantly follow, so slip increases momentarily.

2. **Standstill rotor reactance $X_2 = 2\pi f L_2$ increases** proportionally with $f$.

3. **Maximum torque $T_{\max} \propto V^2/f^2$ decreases** (since $X_2 \propto f$, and $V$ is constant). Significant torque reduction.

4. **Full-load slip at the new frequency:** Since the motor must develop the same load torque, and $T_{\max}$ has decreased, the operating slip increases (motor operates closer to pull-out torque: less stable).

5. **Speed changes:** The new synchronous speed is higher, but the rotor catches up partially. Final rotor speed may be higher or lower depending on the magnitude of the frequency change and the load torque.

**Summary:** Higher frequency → higher $N_s$, lower $T_{\max}$, potential instability if $T_{\max}$ drops below load torque. This is why VFDs must change $V$ and $f$ together (constant V/f ratio) to maintain constant flux and constant torque capability.

---

**(b) Motor driving full-load torque (independent of speed). Line voltage drops to 90%. Find increase in Cu losses. [04]**

$T_{\max} \propto V^2$. If voltage drops to $0.9V$:

New $T_{\max} = (0.9)^2 T_{\max,original} = 0.81\, T_{\max,original}$

Since the load torque is constant (independent of speed), and $T \propto \frac{sE_2^2 R_2}{R_2^2 + s^2 X_2^2}$:

For small slip (low-slip approximation): $T \approx \frac{kE_2^2 s}{R_2} \propto \frac{sV^2}{R_2}$

At full load, torque is constant:
$$T = k_1 \frac{s_1 V_1^2}{R_2} = k_1 \frac{s_2 V_2^2}{R_2}$$

$$s_1 V_1^2 = s_2 V_2^2 \implies s_2 = s_1 \left(\frac{V_1}{V_2}\right)^2 = s_1 \times \left(\frac{1}{0.9}\right)^2 = s_1 \times 1.2346$$

**Rotor copper loss:** $P_{Cu} = s \times P_g$, and $P_g = T \cdot \omega_s$ (constant since $T$ and $\omega_s$ are constant).

$$\frac{P_{Cu,\text{new}}}{P_{Cu,\text{old}}} = \frac{s_2}{s_1} = 1.2346$$

**Increase in Cu losses:**
$$\Delta P_{Cu} = (1.2346 - 1) \times 100\% = \boxed{23.46\%}$$

Cu losses increase by about 23.5% when voltage drops to 90% of rated, for constant-torque load.

---

**(c) Determine the rotor efficiency of an IM. [04]**

Rotor efficiency is the ratio of mechanical power developed to the electrical power input to the rotor.

**Power input to rotor (air-gap power):**
$$P_g = 3 I_2^2 \cdot \frac{R_2}{s}$$

**Rotor copper loss:**
$$P_{Cu} = 3 I_2^2 R_2 = s P_g$$

**Mechanical power developed:**
$$P_m = P_g - P_{Cu} = P_g - sP_g = (1-s)P_g$$

**Rotor efficiency:**
$$\eta_{\text{rotor}} = \frac{P_m}{P_g} = \frac{(1-s)P_g}{P_g} = \boxed{(1-s)}$$

Or as percentage: $\eta_{\text{rotor}} = (1-s) \times 100\%$

At full load with $s = 0.04$: $\eta_{\text{rotor}} = 96\%$.

**Interpretation:** For every unit of electrical power crossing the air gap, $(1-s)$ units become mechanical power and $s$ units are lost as heat in the rotor resistance. Low slip → high rotor efficiency. This is why induction motors are designed to operate at small slip.

---

### Question 7

**(a) Explain the double-field revolving theory of single-phase IM. [04]**

![Resolution of alternating flux into two oppositely rotating fields](../Books/diagrams/VK_Mehta_Fig_9_03.jpeg)

A single-phase stator current $i = I_m\sin\omega t$ creates a pulsating flux:
$$\Phi = \Phi_m\sin\omega t$$

**Decomposition into two rotating fields:**

Using the trigonometric identity:
$$\Phi_m\sin\omega t = \frac{\Phi_m}{2}\cos(\theta - \omega t) + \frac{\Phi_m}{2}\cos(\theta + \omega t)$$

At any angle $\theta$, the pulsating field equals:
- **Forward field ($\Phi_f$):** Magnitude $\Phi_m/2$, rotates in the +ve direction at $+\omega$ rad/s.
- **Backward field ($\Phi_b$):** Magnitude $\Phi_m/2$, rotates in the −ve direction at $-\omega$ rad/s.

**At standstill ($N = 0$):**
- Slip for forward field: $s_f = 1$
- Slip for backward field: $s_b = 1$
- Forward torque $T_f$ = backward torque $T_b$
- Net torque = 0. **No self-starting.**

**At speed $N$ (given a push forward):**
- $s_f = (N_s - N)/N_s = s$ (small, < 1)
- $s_b = (N_s + N)/N_s = (2-s)$ (close to 2, large)
- $T_f > T_b$ (forward torque dominates)
- Motor continues to accelerate and maintains running.

![Torque-speed characteristic under double-field revolving theory showing zero starting torque](../Books/diagrams/VK_Mehta_Fig_9_04.jpeg)

---

**(b) How does a capacitor-start-and-run single-phase IM operate? [04]**

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
$$\tan(50.57°) = \frac{X_C - 3.5}{9.5} = 1.213$$

$$X_C - 3.5 = 1.213 \times 9.5 = 11.52$$

$$X_C = 11.52 + 3.5 = 15.02\,\Omega$$

$$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 15.02} = \frac{1}{4722} = \boxed{211.8\,\mu\text{F}}$$

---

### Question 8

**(a) Define synchronous watt with an example. [03]**

**Synchronous watt:** A unit of torque used in induction motor calculations. One synchronous watt is the torque that develops one watt of power at synchronous speed.

$$T \text{ (in synchronous watts)} = P_g \text{ (in watts)}$$

**Relationship:**
$$T = \frac{P_g}{\omega_s} = \frac{P_g}{2\pi N_s/60} \text{ N-m}$$

So if $P_g = 1000$ W (1 synchronous watt) and $N_s = 1500$ rpm:
$$T = \frac{1000}{2\pi \times 1500/60} = \frac{1000}{157.08} = 6.37 \text{ N-m}$$

**Example:** A motor has air-gap power $P_g = 5000$ W. If synchronous speed is 1000 rpm ($\omega_s = 104.7$ rad/s):
$$T = \frac{5000}{104.7} = 47.75 \text{ N-m}$$

Expressing the torque as 5000 synchronous watts captures both the power and speed dependence in one quantity.

---

**(b) What does vector group of a transformer indicate? What does "Dyn5" represent? [03]**

**Vector group:** A standardized notation that tells you:
1. The connection of the primary winding (uppercase letter: Y, D, or Z).
2. The connection of the secondary winding (lowercase letter: y, d, or z).
3. Whether a neutral is available (letter n).
4. The phase displacement between primary and secondary voltages (clock notation: number × 30°).

**"Dyn5" means:**
- **D** → Primary winding connected in Delta (Δ)
- **y** → Secondary winding connected in Star (Y)
- **n** → Neutral conductor available on the secondary side
- **5** → Phase displacement = 5 × 30° = 150° (secondary voltage lags primary voltage by 150°)

In clock notation: 12 = 0°, 1 = 30°, 5 = 150°. So Dyn5 means the secondary star voltage phasor points to "5 o'clock" relative to the primary delta voltage phasor at "12 o'clock."

---

**(c) Circle diagram: 3-φ, 14.92 kW, 400V, 6-pole IM. No-load: 400V, 11A, pf = 0.2. SC: 100V, 25A, pf = 0.4. Rotor Cu loss at standstill = half total Cu loss. Find from diagram: (i) line current, slip, efficiency, pf at full load; (ii) max torque. [06]**

![Construction of Circle Diagram](../Books/diagrams/ch35_p06_fig35_09.jpg)

**No-load data:**
$I_0 = 11$ A, $\cos\phi_0 = 0.2$, $\phi_0 = 78.46°$

$I_{0x} = 11 \times 0.2 = 2.2$ A, $I_{0y} = 11 \times \sin(78.46°) = 11 \times 0.9798 = 10.78$ A

**Short-circuit data (referred to full voltage 400V):**
$$I_{sc} = 25 \times \frac{400}{100} = 100 \text{ A}$$
$\cos\phi_{sc} = 0.4$, $\phi_{sc} = 66.42°$
$I_{scx} = 100 \times 0.4 = 40$ A, $I_{scy} = 100 \times 0.917 = 91.65$ A

**Circle diagram construction:**
- Plot no-load point $O'$ at $(I_{0x}, I_{0y}) = (2.2, 10.78)$ A.
- Plot short-circuit point $S$ at $(I_{scx}, I_{scy}) = (40, 91.65)$ A.
- Draw the circle through $O'$ and $S$.
- The power base line is horizontal (active component axis).
- Since rotor Cu loss = stator Cu loss at standstill: the rotor Cu line divides the SC intercept equally (at 50%).

**At rated output 14.92 kW:**

Input power at rated output (from circle diagram):

$N_s = \frac{120 \times 50}{6} = 1000$ rpm

Scale: power scale depends on voltage scale. Using $\sqrt{3} \times 400 = 692.8$ V per unit current.

Power per amp of active component $= \sqrt{3} \times 400 = 692.8$ W/A.

For 14.92 kW output, find the point on the circle where the vertical height above the output line equals the output power.

**(i) From circle diagram (estimated):**

- Full load line current: ≈ 30 A
- Full load slip: ≈ 5%
- Full load efficiency: ≈ 84%
- Full load power factor: ≈ 0.76 lagging

**(ii) Maximum torque:**
Maximum torque corresponds to the longest vertical distance from the circle to the torque line (line from $O'$ to the point where rotor Cu loss line meets the base line).

$T_{\max}$ in synchronous watts $\approx$ read from circle diagram.

---

*Source:* [PrevYearQuestions/2021.md](../PrevYearQuestions/2021.md)

---

[← 2020 Answer](2020_answer.md) | [🏠 Index](README.md) | [2023 Answer →](2023_answer.md)
