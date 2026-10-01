[← 2021 Answer](2021_answer.md) | [🏠 Index](README.md) | [2024 Answer →](2024_answer.md)

---

# ECE 2207: 2023 Semester Final: Exam Style Answers
**RUET · ECE Dept · 2nd Year Even Semester (Session 2022-23)**
**Course Code:** ECE 2207 | **Full Marks:** 60 | **Time:** 3 Hours
**Attempt any 5 questions out of 8. All questions carry equal marks (12 each).**

> **OBE Format Note:** This is the new 60-mark OBE format. Each question is 12 marks, split into sub-parts linked to specific Course Outcomes (COs).

---

## Question 1

**(a) What is transformer? With a neat schematic diagram of a 1-φ transformer, identify and explain all the variables on both sides. [06, CO1]**

**Transformer:** A static electromagnetic device that transfers electrical energy between two circuits at the same frequency but different voltage and current levels, via electromagnetic induction through a shared magnetic core.

**Schematic:**

![Schematic diagram of single-phase transformer connected to sinusoidal source on primary and load on secondary with all labeled variables](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_01.jpeg)

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

**(b) Under the assumptions of an ideal transformer, prove that $E_1 = 4.44 f N_1 \Phi_m$ and $E_2 = 4.44 f N_2 \Phi_m$. [06, CO1]**

**Assumptions:**
- Core permeability is constant (no saturation). Core reluctance is constant.
- No leakage flux. Same flux $\Phi(t)$ links all turns of both windings.

Let core flux be: $\Phi(t) = \Phi_m\sin(\omega t)$, where $\Phi_m$ = peak flux (Wb), $f$ = supply frequency (Hz), $\omega = 2\pi f$.

**For primary (N₁ turns):**

By Faraday's Law:
$$e_1(t) = -N_1\frac{d\Phi}{dt} = -N_1 \cdot \omega\Phi_m\cos\omega t = N_1\omega\Phi_m\sin(\omega t - 90°)$$

Peak value: $E_{m1} = N_1\omega\Phi_m = 2\pi f N_1\Phi_m$

RMS value (sine wave, RMS = peak/$\sqrt{2}$):
$$E_1 = \frac{E_{m1}}{\sqrt{2}} = \frac{2\pi f N_1\Phi_m}{\sqrt{2}} = \sqrt{2}\pi f N_1\Phi_m$$

Numerical constant: $\sqrt{2}\pi = 1.4142 \times 3.1416 = 4.4429 \approx 4.44$

$$\boxed{E_1 = 4.44\, f N_1 \Phi_m} \quad \textit{(Proved)}$$

**For secondary (N₂ turns):**

Same flux $\Phi(t)$ links all $N_2$ turns. By Faraday's Law:
$$e_2(t) = -N_2\frac{d\Phi}{dt} = N_2\omega\Phi_m\sin(\omega t - 90°)$$

RMS:
$$\boxed{E_2 = 4.44\, f N_2 \Phi_m} \quad \textit{(Proved)}$$

Both EMFs lag the mutual core flux by 90°.

---

## Question 2

**(a) A 100 kVA transformer, iron loss = 1 kW, full-load Cu loss = 1 kW. Distribution transformer load profile: 4h no-load, 12h half load, 8h full load. Find all-day efficiency. [06, CO1]**

**Energy output (kWh):**

| Period | Output | Hours | kWh |
|:---|:---:|:---:|:---:|
| No-load | 0 kW | 4 | 0 |
| Half load (at upf) | 50 kW | 12 | 600 |
| Full load (at upf) | 100 kW | 8 | 800 |
| **Total** | | 24 | **1400 kWh** |

**Iron loss (24 hours, constant):**
$$W_{Fe} = 1 \times 24 = 24 \text{ kWh}$$

**Copper losses:**

| Period | Cu loss | Hours | kWh |
|:---|:---:|:---:|:---:|
| No-load | 0 | 4 | 0 |
| Half load | $(0.5)^2 \times 1 = 0.25$ kW | 12 | 3 |
| Full load | $1$ kW | 8 | 8 |
| **Total Cu** | | | **11 kWh** |

**Total losses** $= 24 + 11 = 35$ kWh

**Total input** $= 1400 + 35 = 1435$ kWh

$$\boxed{\eta_{\text{all-day}} = \frac{1400}{1435} \times 100 = 97.56\%}$$

---

**(b) OC test (secondary open): 220V, 0.8A, 80W. SC test (primary short): 12V, 10A, 40W. Transformer rated 2.2kV/220V. Find the equivalent circuit parameters referred to the secondary. [06, CO1]**

**From OC test (secondary/LV side):**

![Open circuit or No load test schematic](../SlidesByMaam/diagrams/L-10_ECE-2107_p17_fig01.jpg)

$$\cos\phi_0 = \frac{W_0}{V_0 I_0} = \frac{80}{220 \times 0.8} = \frac{80}{176} = 0.4545$$

$$I_c = I_0\cos\phi_0 = 0.8 \times 0.4545 = 0.364 \text{ A}$$

$$I_m = I_0\sin\phi_0 = 0.8 \times \sqrt{1 - 0.4545^2} = 0.8 \times 0.8909 = 0.713 \text{ A}$$

Referred to secondary:
$$R_{c2} = \frac{V_0}{I_c} = \frac{220}{0.364} = \boxed{604.4\,\Omega}$$

$$X_{m2} = \frac{V_0}{I_m} = \frac{220}{0.713} = \boxed{308.6\,\Omega}$$

**From SC test (primary/HV side shorted):**

![Short circuit test schematic](../SlidesByMaam/diagrams/L-10_ECE-2107_p18_fig01.jpg)

Turns ratio: $a = 2200/220 = 10$

Rated secondary current: $I_2 = $ rated → from SC test, $I_{sc} = 10$ A on secondary.

$$R_{02,sec} = \frac{W_{sc}}{I_{sc}^2} = \frac{40}{10^2} = \boxed{0.4\,\Omega}$$

$$Z_{02} = \frac{V_{sc}}{I_{sc}} = \frac{12}{10} = 1.2\,\Omega$$

$$X_{02} = \sqrt{Z_{02}^2 - R_{02}^2} = \sqrt{1.44 - 0.16} = \sqrt{1.28} = \boxed{1.131\,\Omega}$$

**Equivalent circuit referred to secondary:**
- Series: $R_{02} = 0.4\,\Omega$, $X_{02} = 1.131\,\Omega$
- Shunt: $R_{c2} = 604.4\,\Omega$, $X_{m2} = 308.6\,\Omega$

---

## Question 3

**(a) What is voltage regulation? Derive the expression for VR with neat phasor diagrams for lagging, unity, and leading pf loads. [08, CO1]**

**Voltage Regulation (VR):** The change in secondary terminal voltage from no-load to full-load, as a percentage of the rated full-load secondary voltage, with primary voltage held constant.

$$\text{VR\%} = \frac{V_{2,NL} - V_{2,FL}}{V_{2,FL}} \times 100\%$$

**Derivation (approximate formula):**

From the equivalent circuit, secondary terminal voltage referred to primary:
$$V_1 = V_2' + I_2'R_{01}\cos\phi_2 + I_2'X_{01}\sin\phi_2 + j(\ldots) \approx V_2' + I_2'(R_{01}\cos\phi_2 \pm X_{01}\sin\phi_2)$$

where $+$ for lagging, $-$ for leading.

No-load voltage: $V_{2,NL} \approx V_1/a = V_2'$

Full-load voltage: $V_{2,FL} = V_2'$

Using phasor:
$$\text{VR\%} \approx \frac{I_2(R_{01}\cos\phi + X_{01}\sin\phi)}{V_{2,\text{rated}}} \times 100 \quad \text{(lagging, positive)}$$

$$\text{VR\%} \approx \frac{I_2(R_{01}\cos\phi - X_{01}\sin\phi)}{V_{2,\text{rated}}} \times 100 \quad \text{(leading, can be negative)}$$

**Phasor diagrams:**

![Complete vector diagrams of transformer](../Books/Theraja/Ch-32/diagrams/Ch-32_p21_fig29.jpg)
> 
> **Lagging pf:** $V_2$ reference. $I_2$ lags $V_2$ by $\phi$. $V_1 = V_2 + I_2R_{01}\angle0° + I_2X_{01}\angle90°$. $|V_1| > |V_2|$. VR > 0.
>
> **Unity pf:** $I_2$ in phase with $V_2$. Drop is only $I_2R_{01}$ (purely resistive). $|V_1|$ slightly greater. VR > 0 but small.
>
> **Leading pf:** $I_2$ leads $V_2$ by $\phi$. Reactive drop partially cancels resistive drop. $|V_1|$ may be less than $|V_2|$. VR can be negative (secondary voltage rises with load).

---

**(b) 3300/220V, 50Hz, 50 kVA transformer. Winding resistance: primary = $3.96\,\Omega$, secondary = $0.0176\,\Omega$. Leakage reactance: primary = $15.8\,\Omega$, secondary = $0.07\,\Omega$. Find VR at 0.8 pf lagging. [04, CO1]**

**Turns ratio:** $a = 3300/220 = 15$

**Refer to primary:**
$$R_{01} = R_1 + a^2 R_2 = 3.96 + 225 \times 0.0176 = 3.96 + 3.96 = 7.92\,\Omega$$

$$X_{01} = X_1 + a^2 X_2 = 15.8 + 225 \times 0.07 = 15.8 + 15.75 = 31.55\,\Omega$$

**Rated primary current:**
$$I_1 = \frac{50000}{3300} = 15.15 \text{ A}$$

**VR at 0.8 pf lag ($\cos\phi = 0.8$, $\sin\phi = 0.6$):**
$$\text{VR\%} = \frac{I_1(R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100$$

$$= \frac{15.15(7.92 \times 0.8 + 31.55 \times 0.6)}{3300} \times 100$$

$$= \frac{15.15(6.336 + 18.93)}{3300} \times 100 = \frac{15.15 \times 25.266}{3300} \times 100$$

$$= \frac{382.78}{3300} \times 100 = \boxed{11.6\%}$$

---

## Question 4

**(a) Explain what happens to a 3-phase Δ-Δ transformer bank when one transformer is damaged. Show 3-phase power can still be served. Also prove the capacity reduces to 57.7%. [08, CO1]**

**Event:** One transformer (say $T_{CA}$) in the Δ-Δ bank fails.

**Why 3-phase power still reaches the load:**

The primary and secondary delta loops still have two active transformers: $T_{AB}$ and $T_{BC}$.

On the primary delta: The 3-phase supply maintains $V_{AB}$ and $V_{BC}$. KVL in the delta loop demands $V_{CA} = -(V_{AB} + V_{BC})$. Even without $T_{CA}$, this voltage is present at the open terminal.

On the secondary delta: $T_{AB}$ produces $V_{ab} = K\cdot V_{AB}$. $T_{BC}$ produces $V_{bc} = K\cdot V_{BC}$. By KVL: $V_{ca} = -(V_{ab} + V_{bc}) = K\cdot V_{CA}$. All three secondary line voltages exist and are balanced.

**Three-phase balanced power is delivered by two transformers.** This configuration is called the open-delta (V-V) connection.

**Capacity proof:**

Let each single transformer be rated $S = VI$ kVA.

In closed-Δ (3 transformers): Total $= 3S$ kVA.

In open-Δ (2 transformers):
Each transformer still carries rated current $I$ at rated voltage $V$.
For a balanced 3-phase unity pf load, each transformer operates at power factor $\cos 30° = \sqrt{3}/2$.

$$S_{\text{open}} = 2 \times V \times I \times \cos 30° = 2VI \times \frac{\sqrt{3}}{2} = \sqrt{3}VI = \sqrt{3}S$$

$$\frac{S_{\text{open}}}{S_{\text{closed}}} = \frac{\sqrt{3}S}{3S} = \frac{1}{\sqrt{3}} = 0.577 = \boxed{57.7\%}$$

**Utilization factor of each transformer** in open-Δ: The transformer is rated $S = VI$ kVA but works at power factor $\cos 30° = 0.866$, delivering only $0.866 S$ kW. So the utilization is 86.6% instead of 100%.

---

**(b) Conditions for parallel operation. [04, CO1]**

1. Same voltage ratio (same primary/secondary rated voltages).
2. Same per-unit impedance (for proportional load sharing).
3. Same polarity (same instantaneous phase relationship at terminals).
4. Same phase sequence (3-phase transformers only).
5. Same vector group: zero phase angle between secondary voltages.

---

## Question 5

**(a) For a 3-phase induction motor, derive the torque expression and show that the torque-slip relationship is: $T = \frac{ksE_2^2 R_2}{R_2^2 + s^2X_2^2}$ where $k = \frac{3}{2\pi n_s}$. [08, CO2]**

**At running slip $s$, per-phase rotor quantities:**

- Rotor induced EMF: $E_{2s} = sE_2$
- Rotor reactance: $X_{2s} = sX_2$
- Rotor current: $I_2 = \frac{sE_2}{\sqrt{R_2^2 + s^2X_2^2}}$
- Rotor power factor: $\cos\phi_2 = \frac{R_2}{\sqrt{R_2^2 + s^2X_2^2}}$

**Air-gap power (power transferred to rotor):**

$$P_g = 3 E_{2s} I_2 \cos\phi_2 = 3 \cdot sE_2 \cdot \frac{sE_2}{\sqrt{R_2^2 + s^2X_2^2}} \cdot \frac{R_2}{\sqrt{R_2^2 + s^2X_2^2}}$$

$$P_g = \frac{3s^2E_2^2 R_2}{R_2^2 + s^2X_2^2}$$

Alternatively, using the equivalent circuit representation $R_2/s$:

$$P_g = 3 I_2^2 \cdot \frac{R_2}{s} = 3 \cdot \frac{s^2E_2^2}{R_2^2 + s^2X_2^2} \cdot \frac{R_2}{s} = \frac{3sE_2^2 R_2}{R_2^2 + s^2X_2^2}$$

**Torque from air-gap power:**

Synchronous speed in rps: $n_s = N_s/60$. Angular synchronous speed: $\omega_s = 2\pi n_s$.

$$T = \frac{P_g}{\omega_s} = \frac{P_g}{2\pi n_s} = \frac{3sE_2^2 R_2}{(R_2^2 + s^2X_2^2) \cdot 2\pi n_s}$$

$$\boxed{T = \frac{ksE_2^2 R_2}{R_2^2 + s^2X_2^2}, \qquad k = \frac{3}{2\pi n_s}}$$

*(Derived)*

---

**(b) 8-pole, 50 Hz, 3-phase IM. Full-load slip = 2.5%. $R_2 = 0.4\,\Omega$, $X_2 = 2.0\,\Omega$ (standstill). Find: slip and speed at maximum torque, ratio $T_{\max}/T_{FL}$. [04, CO2]**

$$N_s = \frac{120 \times 50}{8} = 750 \text{ rpm}$$

**Slip at max torque:**
$$s_{mT} = \frac{R_2}{X_2} = \frac{0.4}{2.0} = \boxed{0.2}$$

**Speed at max torque:**
$$N_{mT} = N_s(1 - s_{mT}) = 750(1 - 0.2) = \boxed{600 \text{ rpm}}$$

**Torque ratio:** Using $a = s_{mT} = 0.2$, $s_f = 0.025$:

$$\frac{T_f}{T_{\max}} = \frac{2as_f}{a^2 + s_f^2} = \frac{2 \times 0.2 \times 0.025}{0.04 + 0.000625} = \frac{0.010}{0.040625} = 0.246$$

$$\boxed{\frac{T_{\max}}{T_f} = \frac{1}{0.246} = 4.07}$$

---

## Question 6

**(a) For a 3-phase IM, derive: $P_g : P_{r,Cu} : P_m = 1 : s : (1-s)$. Draw the complete power flow diagram. [06, CO2]**

**From equivalent circuit, rotor quantities:**

Rotor current: $I_2 = \frac{sE_2}{\sqrt{R_2^2 + s^2X_2^2}}$

Air-gap power:
$$P_g = 3 I_2^2 \cdot \frac{R_2}{s}$$

Rotor copper loss:
$$P_{r,Cu} = 3 I_2^2 R_2 = s \cdot \left(3 I_2^2 \frac{R_2}{s}\right) = s \cdot P_g$$

Mechanical power:
$$P_m = P_g - P_{r,Cu} = P_g - sP_g = (1-s)P_g$$

Therefore:
$$\boxed{P_g : P_{r,Cu} : P_m = 1 : s : (1-s)}$$

**Power flow diagram:**

![Induction motor power flow diagram showing air-gap, copper, and mechanical stages](../Books/Theraja/Ch-34/diagrams/Ch-34_p39_fig38.jpg)

---

**(b) How can we improve the poor power factor of an induction motor at light loads? [03, CO2]**

At light load, the motor draws mostly magnetizing current (reactive). The working (active) component is small. So the power factor is very low.

**Methods to improve power factor:**

1. **Avoid running at no-load or very light load:** Switch off motors that are idling.
2. **Capacitor banks:** Connect shunt capacitors at the motor terminals. Reactive current from capacitors offsets the lagging reactive current of the motor.
3. **Use appropriately sized motor:** An oversized motor at light load has low pf. Match motor size to load requirement.
4. **Synchronous condenser:** A synchronous motor running at no-load (overexcited) supplies reactive power to the system.
5. **Variable frequency drive (VFD):** Reduces voltage at light load, which reduces flux and reduces magnetizing current. Improves efficiency and pf at light loads.

---

**(c) What is rotor efficiency? Show that rotor efficiency = $(1-s)$. [03, CO2]**

**Rotor efficiency:** Ratio of mechanical power developed to electrical power input to the rotor (air-gap power).

$$\eta_{\text{rotor}} = \frac{P_m}{P_g} = \frac{(1-s)P_g}{P_g} = \boxed{(1-s)}$$

From the power ratio $P_g : P_{r,Cu} : P_m = 1 : s : (1-s)$:
- Of each unit of air-gap power, fraction $s$ is wasted as rotor copper heat.
- Fraction $(1-s)$ becomes mechanical work.

At $s = 0.04$ (full load, typical): $\eta_{\text{rotor}} = 96\%$. High rotor efficiency is achievable at low slip. Motors are designed to run at small slip for this reason.

---

## Question 7

**(a) Explain the no-load and blocked rotor tests of a 3-phase induction motor. [08, CO3]**

**No-Load Test:**
Motor runs uncoupled at rated voltage and frequency. Since slip $s \approx 0$, the rotor branch is effectively an open circuit. The motor draws a small no-load current $I_0$ to supply core loss and friction/windage loss.
- **Measurements:** $V_0$ (line voltage), $I_0$ (line current), $P_0$ (3-phase power).
- **Parameters found:** Shunt branch ($R_c$, $X_m$).
$$R_c = \frac{V_\phi}{I_c}, \quad X_m = \frac{V_\phi}{I_m} \quad \text{where } I_c = I_0 \cos\phi_0, I_m = I_0 \sin\phi_0$$

**Blocked-Rotor Test:**
Rotor is mechanically blocked ($s = 1$). A reduced voltage (10-15% of rated) is applied to circulate rated full-load current. At such low voltage, core loss is negligible. Input power equals full-load copper loss.
- **Measurements:** $V_{sc}$ (line voltage), $I_{sc}$ (line current), $P_{sc}$ (3-phase power).
- **Parameters found:** Equivalent series resistance and reactance ($R_{01}, X_{01}$).
$$Z_{01} = \frac{V_{sc}/\sqrt{3}}{I_{sc}}, \quad R_{01} = \frac{P_{sc}}{3 I_{sc}^2}, \quad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$
Assuming $X_1 = X_2' = X_{01}/2$.

**DC Test (for $R_2'$):**
Measure stator resistance $R_1$ using a DC source. Then rotor resistance referred to stator is $R_2' = R_{01} - R_1$.

![Complete Equivalent Circuit](diagrams/im_step5_exact_equivalent_circuit.png)

---

**(b) A 3-phase star-connected IM, SC test gives: $V = 75$ V, $I = 38$ A, $P = 4$ kW. Stator resistance per phase = $0.5\,\Omega$. Find: $R_2'$, $X_1$, $X_2'$. [04, CO3]**

**From SC test (star-connected, 3-phase):**

Per-phase voltage: $V_{sc,\phi} = 75/\sqrt{3} = 43.30$ V

$$Z_{01} = \frac{V_{sc,\phi}}{I_{sc}} = \frac{43.30}{38} = 1.140\,\Omega$$

$$R_{01} = \frac{P_{sc}}{3I_{sc}^2} = \frac{4000}{3 \times 38^2} = \frac{4000}{4332} = 0.923\,\Omega$$

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2} = \sqrt{1.140^2 - 0.923^2} = \sqrt{1.300 - 0.852} = \sqrt{0.448} = 0.669\,\Omega$$

$$R_2' = R_{01} - R_1 = 0.923 - 0.5 = \boxed{0.423\,\Omega}$$

$$X_1 = X_2' = \frac{X_{01}}{2} = \frac{0.669}{2} = \boxed{0.335\,\Omega}$$

---

## Question 8

**(a) Explain the principle of operation of a 1-phase induction motor using the double revolving field theory. [06, CO4]**

A single-phase stator with alternating current $i = I_m\sin\omega t$ creates a pulsating magnetic flux along one fixed axis:
$$\Phi = \Phi_m\sin\omega t$$

**Double revolving field theory (Ferraris theorem):**

This pulsating flux is mathematically equivalent to two equal halves rotating in opposite directions:

$$\Phi = \frac{\Phi_m}{2}\sin(\omega t - \theta) + \frac{\Phi_m}{2}\sin(\omega t + \theta)$$

- **Forward field ($\Phi_f$):** Magnitude $\Phi_m/2$, rotates at $+N_s$ rpm (forward).
- **Backward field ($\Phi_b$):** Magnitude $\Phi_m/2$, rotates at $-N_s$ rpm (backward).

Each rotating field interacts with the squirrel-cage rotor, producing an induction torque just like in a 3-phase motor.

**At standstill ($s = 1$):**

For forward field: slip $s_f = 1$
For backward field: slip $s_b = (2 - s) = (2 - 1) = 1$

Both fields produce equal and opposite torques:
$$T_f(s=1) = T_b(s=1)$$

Net torque $= T_f - T_b = 0$. **Motor cannot self-start.**

**When running (pushed to speed $N$):**

Forward slip: $s_f = (N_s - N)/N_s = s$ (small)
Backward slip: $s_b = (N_s + N)/N_s = 2 - s$ (nearly 2)

For small $s$: $T_f$ is in the stable high-torque region, $T_b$ is in the low-torque high-slip region.

$$T_f > T_b \implies \text{Net forward torque} > 0$$

Motor continues to run. The direction of running is determined by the initial push.

---

**(b) Describe any two methods of making a 1-phase IM self-starting. [06, CO4]**

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

*Source:* [PrevYearQuestions/2023.md](../PrevYearQuestions/2023.md)

---

[← 2021 Answer](2021_answer.md) | [🏠 Index](README.md) | [2024 Answer →](2024_answer.md)
