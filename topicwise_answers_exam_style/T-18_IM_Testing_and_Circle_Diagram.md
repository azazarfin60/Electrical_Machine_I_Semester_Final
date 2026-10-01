[← T-17: Power Flow & Rotor Power](T-17_Power_Flow_and_Rotor_Power.md) | [🏠 Index](README.md) | [T-19: 3-Phase Starting Methods →](T-19_Starting_Methods_3-Phase_IM.md)

---

# T-18: IM Testing & Circle Diagram

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **IM Testing & Circle Diagram** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q3(b)]
> 📋 **Appeared in:** 2017 Q3(b), 2019 Q6(a) (Years: 2017, 2019)

**(b) Circle diagram problem: 415V, 29.84 kW, 50 Hz, delta-connected motor. No-load: 415V, 21A, 1250W. Locked rotor: 100V, 45A, 2730W. [09]**

**Step 1: No-load data (referred to full voltage):**

Line voltage $V = 415$ V (delta), so phase voltage $= 415$ V.

No-load current per phase: $I_0 = 21/\sqrt{3} = 12.12$ A (line to phase for delta: $I_{\text{phase}} = I_{\text{line}}/\sqrt{3}$)

No-load input power $W_0 = 1250$ W
$$\cos\phi_0 = \frac{W_0}{\sqrt{3} V I_0} = \frac{1250}{\sqrt{3} \times 415 \times 21} = \frac{1250}{15094} = 0.0828$$

No-load phase: $\phi_0 = \cos^{-1}(0.0828) = 85.25°$

**Step 2: Blocked rotor data (referred to full voltage):**

At 100V, $I_{sc} = 45$ A, $W_{sc} = 2730$ W.

Scale to full voltage (415V):
$$I_{sc,\text{full}} = 45 \times \frac{415}{100} = 186.75 \text{ A}$$

$$\cos\phi_{sc} = \frac{W_{sc}}{\sqrt{3} \times 100 \times 45} = \frac{2730}{7794} = 0.35$$

$\phi_{sc} = \cos^{-1}(0.35) = 69.5°$

**Step 3: Diameter of circle:**

Total rotor copper loss = stator copper loss (given: equal at standstill). So rotor copper loss line bisects the short-circuit point.

**Step 4: Rated output:**

Rated output $= 29.84$ kW. Use circle diagram scale to read off line current and power factor at this output.

$$P_{\text{output}} = \sqrt{3} \times 415 \times I_L \times \cos\phi \implies \text{read from diagram}$$

**(i) Line current at rated output:** Read from circle diagram ≈ 58 A
**(ii) Power factor at rated output:** ≈ 0.714 lagging

**Maximum torque:**
$$T_{\max} = \frac{3}{2\pi N_s} \times \frac{E_2^2}{2X_2}$$
Read from circle diagram: the maximum torque line is the longest vertical intercept below the no-load line.

![Construction of Circle Diagram for Induction Motor](../Books/diagrams/ch35_p06_fig35_09.jpg)

---

### [2018 Q7(b)]
> 📋 **Appeared in:** 2018 Q7(b)

**(b) Circle diagram for 5.6 kW, 400V, 3-φ, 4-pole, 50 Hz slip-ring IM. No-load: 400V, 6A, $\cos\phi_0 = 0.087$. Blocked rotor: 100V, 12A, 720W. Stator turns/rotor turns $= 2.62$. $R_{1} = 0.67\,\Omega/\text{phase}$, $R_2 = 0.185\,\Omega/\text{phase}$. Find: (i) full load current, (ii) slip, (iii) pf, (iv) max power. [08]**

**Scale to full voltage (Blocked rotor data):**

$$I_{sc} = 12 \times \frac{400}{100} = 48 \text{ A (at full voltage)}$$

$$\cos\phi_{sc} = \frac{720}{\sqrt{3} \times 100 \times 12} = \frac{720}{2078.5} = 0.347, \quad \phi_{sc} = 69.7°$$

**No-load point:**
$I_0 = 6$ A, $\cos\phi_0 = 0.087$, $\phi_0 = 85°$

$I_{0x} = 6\cos\phi_0 = 6 \times 0.087 = 0.52$ A (horizontal)
$I_{0y} = 6\sin\phi_0 = 6 \times 0.9962 = 5.98$ A (vertical)

**Short-circuit point:**
$I_{scx} = 48\cos\phi_{sc} = 48 \times 0.347 = 16.66$ A
$I_{scy} = 48\sin\phi_{sc} = 48 \times 0.938 = 45.02$ A

**Rotor copper loss line:**

Total SC copper loss $= 720 \times (400/100)^2 = 720 \times 16 = 11520$ W at full voltage.

Stator Cu loss per phase: $I_{sc}^2 R_1/3 = 48^2 \times 0.67/3$ (three-phase, dividing for one transformer of the equivalent): actually stator Cu loss $= 3 I_{sc}^2 R_1 = 3 \times 48^2 \times 0.67 = 3 \times 2304 \times 0.67 = 4631$ W

Rotor Cu loss = Total SC Cu loss − Stator Cu loss $= 11520 − 4631 = 6889$ W.

Ratio of rotor to total Cu loss $= 6889/11520 = 0.598$. The rotor copper loss line divides the SC line at this ratio from the power base line.

**From circle diagram (reading):**

Rated output $= 5.6$ kW.

**(i) Full load line current:** ≈ 10.5 A

**(ii) Full load slip:** $s \approx 0.062$ (6.2%)

**(iii) Full load power factor:** $\approx 0.78$ lagging

**(iv) Maximum power:** Longest intercept below the output line ≈ 8.2 kW (estimated from circle diagram geometry).

![Circle diagram for induction motor showing operating point and output line](../Books/diagrams/ch35_p08_fig35_11.jpg)

---

### [2019 Q7(a)]
> 📋 **Appeared in:** 2019 Q7(a)

**(a) Define plugging. Describe blocked rotor test and no-load test. [04]**

**Plugging:** A braking method for induction motors. The phase sequence of the stator supply is reversed while the motor is running. The stator field now rotates opposite to the rotor. The motor develops a torque opposing motion. The motor decelerates rapidly. Supply is cut before the motor reverses.

**Blocked rotor test:** Rotor locked ($N = 0$, $s = 1$). Reduced voltage applied until rated current flows. Measure $V_{sc}$, $I_{sc}$, $P_{sc}$. Determines: $R_{01} = P_{sc}/(3I_{sc}^2)$, $Z_{01} = V_{sc}/(\sqrt{3}I_{sc})$, $X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$. Gives copper losses and equivalent circuit series parameters.

**No-load test:** Motor runs at no-load (no shaft load). Rated voltage applied. Measure $V_0$, $I_0$, $P_0$. The no-load power $P_0$ = stator iron loss + friction and windage loss + small stator copper loss. Determines shunt branch parameters ($R_c$, $X_m$) and friction/windage losses.

![No-load test circuit and separation of losses](../Books/diagrams/ch35_p03_fig35_07_08.jpg)

---

### [2021 Q8(c)]
> 📋 **Appeared in:** 2021 Q8(c)

**(c) Circle diagram: 3-φ, 14.92 kW, 400V, 6-pole IM. No-load: 400V, 11A, pf = 0.2. SC: 100V, 25A, pf = 0.4. Rotor Cu loss at standstill = half total Cu loss. Find from diagram: (i) line current, slip, efficiency, pf at full load; (ii) max torque. [06]**

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

![Circle diagram showing Maximum Quantities and torque line](../Books/diagrams/ch35_p08_fig35_10.jpg)

---

---

### [2023 Q7(b)]
> 📋 **Appeared in:** 2023 Q7(b)

**(b) A 3-phase star-connected IM, SC test gives: $V = 75$ V, $I = 38$ A, $P = 4$ kW. Stator resistance per phase = $0.5\,\Omega$. Find: $R_2'$, $X_1$, $X_2'$. [04, CO3]**

**From SC test (star-connected, 3-phase):**

Per-phase voltage: $V_{sc,\phi} = 75/\sqrt{3} = 43.30$ V

$$Z_{01} = \frac{V_{sc,\phi}}{I_{sc}} = \frac{43.30}{38} = 1.140\,\Omega$$

$$R_{01} = \frac{P_{sc}}{3I_{sc}^2} = \frac{4000}{3 \times 38^2} = \frac{4000}{4332} = 0.923\,\Omega$$

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2} = \sqrt{1.140^2 - 0.923^2} = \sqrt{1.300 - 0.852} = \sqrt{0.448} = 0.669\,\Omega$$

$$R_2' = R_{01} - R_1 = 0.923 - 0.5 = \boxed{0.423\,\Omega}$$

$$X_1 = X_2' = \frac{X_{01}}{2} = \frac{0.669}{2} = \boxed{0.335\,\Omega}$$

---

### [2024 Q7(a)]
> 📋 **Appeared in:** 2023 Q7(a), 2024 Q7(a) (Years: 2023, 2024)

**(a) Explain the no-load and blocked rotor tests for a 3-phase IM. From these tests, determine the equivalent circuit parameters. [09, CO3]**

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

[← T-17: Power Flow & Rotor Power](T-17_Power_Flow_and_Rotor_Power.md) | [🏠 Index](README.md) | [T-19: 3-Phase Starting Methods →](T-19_Starting_Methods_3-Phase_IM.md)
