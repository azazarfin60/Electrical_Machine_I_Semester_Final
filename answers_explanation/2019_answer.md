[← 2018 Answer](2018_answer.md) | [🏠 Index](README.md) | [2020 Answer →](2020_answer.md)

---

# ECE 2207: 2019 Semester Final: Explanation Style Answers
**RUET · ECE Dept · 2nd Year Odd Semester 2019**

> Deep tutorial-style explanations focusing on first-principles physics, "why over what", step-by-step logic, and practical engineering intuition.
> Core cross-cutting theory topics are detailed in [2018_2024_answer.md](2018_2024_answer.md).

---

## SECTION - A (Transformers: Q1 to Q4)

### Question 1

#### Q1(a): Transformer Energy Transfer and Winding Classification

![Schematic diagram of single-phase transformer connected to sinusoidal source on primary and load on secondary with all labeled variables](../Books/diagrams/VK_Mehta_Fig_7_01.jpeg)

- **Definition**: A static electromagnetic device that transfers alternating electrical energy between two or more electrically isolated circuits through mutual magnetic flux linkage, at constant frequency.
- **Energy Transfer Mechanism**: When primary voltage $v_1(t)$ is applied, it drives an alternating primary current that establishes an oscillating magnetic flux in the laminated iron core. By Faraday's Law of Induction, this core flux cuts the secondary winding, inducing secondary EMF $e_2(t)$. When an external load is connected, secondary current flows, delivering electrical power to the load across the magnetic medium without any conductive contact.
- **Distinction between Primary and Secondary**:
  - *Primary Winding*: The winding connected to the electrical source (input). It draws energy from the grid.
  - *Secondary Winding*: The winding connected to the load (output). It delivers energy to the consumer.
  *(Note: A winding is not intrinsically "primary" or "secondary" by construction—its role is defined entirely by whether it is connected to the source or load).*

---

#### Q1(b): Induced EMF Derivation and EMF per Turn Equality

> For complete mathematical derivation see [T-01: EMF Equation: $E = 4.44 f N \Phi_m$](2018_2024_answer.md#t-01-emf-equation-e--444-f-n-phi_m-full-derivation-and-intuition).

- Peak induced EMF: $E_m = \omega N \Phi_m = 2\pi f N \Phi_m$.
- RMS induced EMF: $E = \frac{E_m}{\sqrt{2}} = \sqrt{2}\pi f N \Phi_m \approx 4.44 f N \Phi_m$.
- **Why EMF per turn is strictly equal**:
  $$\frac{E_1}{N_1} = 4.44 f \Phi_m = \frac{E_2}{N_2}$$
  Because every individual turn of wire on both coils encircles the exact same shared magnetic core flux $\Phi(t)$, each turn experiences the identical instantaneous rate of change of flux ($-\frac{d\Phi}{dt}$). Hence, volts-per-turn is an invariant geometric and magnetic property of the core.

---

#### Q1(c): Why Does Primary Current Increase With Secondary Load?

#### The Fundamental Principle: MMF Balance and Flux Invariance
An AC transformer core maintains its mutual operating flux $\Phi_m$ essentially constant from no-load to full-load, governed by the applied supply voltage:
$$\Phi_m \approx \frac{V_1}{4.44 f N_1}$$

1. **At No-Load ($I_2 = 0$)**:
   The primary draws only the small no-load current $I_0$ (2–5% of rated). The primary MMF ($N_1 I_0$) provides the magnetic force needed to establish and maintain $\Phi_m$ in the core.
2. **When Secondary Load Current Flows ($I_2 > 0$)**:
   The load current flowing through $N_2$ turns creates a secondary MMF:
   $$\vec{F}_2 = N_2 \vec{I}_2$$
   By Lenz's Law, this secondary MMF directly opposes and demagnetizes the core flux $\Phi_m$.
3. **Primary Self-Regulating Action**:
   The moment $\Phi_m$ tends to drop, the primary counter-EMF $E_1 = 4.44 f N_1 \Phi_m$ decreases slightly. Because $V_1$ is maintained constant by the grid, the net driving voltage $(V_1 - E_1)$ increases, immediately pulling an additional compensating current $\vec{I}_2'$ from the supply.
4. **Restoring MMF Equilibrium**:
   The primary draws balancing current $\vec{I}_2'$ such that its MMF cancels the secondary demagnetizing MMF completely:
   $$N_1 \vec{I}_2' + N_2 \vec{I}_2 = 0 \implies \vec{I}_2' = -\frac{N_2}{N_1}\vec{I}_2$$
   Total primary current is the phasor sum:
   $$\vec{I}_1 = \vec{I}_0 + \vec{I}_2' = \vec{I}_0 + \frac{N_2}{N_1}\vec{I}_2$$
   As secondary load current $I_2$ rises, the primary automatically draws a proportionally larger reflected current from the supply to maintain constant core flux and conserve energy.

---

### Question 2

#### Q2(a): Open-Circuit and Short-Circuit Tests

![Open circuit or No load test schematic](../SlidesByMaam/diagrams/L-10_ECE-2107_p17_fig01.jpg)
![Short circuit test schematic](../SlidesByMaam/diagrams/L-10_ECE-2107_p18_fig01.jpg)

- **Open-Circuit Test (Conducted on LV side, HV open)**:
  Rated voltage is applied to the LV winding. Because $I_2 = 0$, primary draws only no-load current $I_0$ (negligible copper loss). The wattmeter reading $W_0$ measures **purely core loss** ($P_{Fe} = P_h + P_e$). Extracts shunt parameters:
  $$\cos\phi_0 = \frac{W_0}{V_0 I_0}, \quad R_c = \frac{V_0}{I_0 \cos\phi_0}, \quad X_m = \frac{V_0}{I_0 \sin\phi_0}$$
- **Short-Circuit Test (Conducted on HV side, LV shorted)**:
  A tiny voltage (~5–10% rated) is applied to circulate rated current. Because voltage is low, core flux is negligible ($\Phi \propto V_{sc}$), making core loss practically zero. The wattmeter reading $W_{sc}$ measures **purely full-load copper loss** ($P_{Cu,FL}$). Extracts series parameters:
  $$Z_{01} = \frac{V_{sc}}{I_{sc}}, \quad R_{01} = \frac{W_{sc}}{I_{sc}^2}, \quad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$

---

#### Q2(b): Voltage Regulation for Lagging, Unity, and Leading Loads

![Complete vector diagrams of transformer](../Books/diagrams/Ch-32_p21_fig29.jpg)

$$\text{VR\%} \approx \frac{I_2 (R_{02}\cos\phi_2 \pm X_{02}\sin\phi_2)}{V_{2,\text{rated}}} \times 100\%$$

- **Lagging PF Load (Inductive)**: Current lags voltage. The reactive drop $j I_2 X_{02}$ points forward in phase with the resistive drop, subtracting from terminal voltage. $\Delta V$ is large and positive, causing substantial voltage drop (**VR is positive and maximum**).
- **Unity PF Load (Pure Resistive)**: $\sin\phi_2 = 0$. The reactive drop is in quadrature with $V_2$, causing primarily a small phase shift rather than a magnitude drop. $\Delta V \approx I_2 R_{02}$ (**VR is positive but small**).
- **Leading PF Load (Capacitive)**: Current leads voltage. The reactive drop $j I_2 X_{02}$ rotates backward, opposing the resistive drop. If $X_{02}\sin\phi_2 > R_{02}\cos\phi_2$, secondary terminal voltage rises above no-load EMF ($V_2 > E_2$). $\Delta V$ is negative (**negative VR / voltage rise**).

---

#### Q2(c): Numerical Efficiency Calculation (10 kVA, 2200/220V)

#### Given Data:
- Rating $S = 10\text{ kVA} = 10{,}000\text{ VA}$
- OC Test: $P_{Fe} = 153\text{ W}$ (constant at all loads)
- SC Test: Full-load copper loss $P_{Cu,FL} = 224\text{ W}$

#### 1. Full-Load Efficiency ($x = 1.0$):
- **At Unity Power Factor ($\cos\phi = 1.0$)**:
  $$P_{\text{out}} = 10{,}000 \times 1.0 = 10{,}000\text{ W}$$
  $$P_{\text{loss}} = P_{Fe} + P_{Cu,FL} = 153 + 224 = 377\text{ W}$$
  $$\eta = \frac{10{,}000}{10{,}000 + 377} \times 100\% = \frac{10{,}000}{10{,}377} \times 100\% = \mathbf{96.37\%}$$
- **At 0.8 PF Lagging ($\cos\phi = 0.8$)**:
  $$P_{\text{out}} = 10{,}000 \times 0.8 = 8{,}000\text{ W}$$
  $$P_{\text{loss}} = 377\text{ W}$$
  $$\eta = \frac{8{,}000}{8{,}000 + 377} \times 100\% = \frac{8{,}000}{8{,}377} \times 100\% = \mathbf{95.50\%}$$

#### 2. Half-Load Efficiency ($x = 0.5$):
- Copper loss at half-load: $P_{Cu} = x^2 P_{Cu,FL} = (0.5)^2 \times 224 = 0.25 \times 224 = 56\text{ W}$.
- Total losses at half-load: $P_{\text{loss}} = 153 + 56 = 209\text{ W}$.
- **At Unity Power Factor ($\cos\phi = 1.0$)**:
  $$P_{\text{out}} = 0.5 \times 10{,}000 \times 1.0 = 5{,}000\text{ W}$$
  $$\eta = \frac{5{,}000}{5{,}000 + 209} \times 100\% = \frac{5{,}000}{5{,}209} \times 100\% = \mathbf{95.99\%}$$
- **At 0.8 PF Lagging ($\cos\phi = 0.8$)**:
  $$P_{\text{out}} = 0.5 \times 10{,}000 \times 0.8 = 4{,}000\text{ W}$$
  $$\eta = \frac{4{,}000}{4{,}000 + 209} \times 100\% = \frac{4{,}000}{4{,}209} \times 100\% = \mathbf{95.03\%}$$

---

### Question 3

#### Q3(a): Transformer Breathing and Maximum Efficiency Proof

#### Transformer Breathing:
As transformer electrical load fluctuates, winding and core losses heat up the insulating oil. The dielectric oil expands as its temperature rises and contracts as it cools. In conservator-tank transformers, this volume change forces air to be expelled into the atmosphere when hot and sucked into the conservator when cool. This cyclic inhalation and exhalation of air is called **transformer breathing**.
- To prevent humid atmospheric air from contaminating the oil, the air passes through a **silica gel breather**. Dehydrated silica gel crystals absorb atmospheric moisture (turning from deep blue to pale pink), preserving the dielectric insulation strength of the oil.

#### Mathematical Proof of Maximum Efficiency Condition:
Efficiency at load fraction $x$ and power factor $\cos\phi$:
$$\eta = \frac{x S \cos\phi}{x S \cos\phi + P_{Fe} + x^2 P_{Cu,FL}} = \frac{S \cos\phi}{S \cos\phi + \frac{P_{Fe}}{x} + x P_{Cu,FL}}$$
To maximize $\eta$, minimize the denominator $D(x) = S\cos\phi + \frac{P_{Fe}}{x} + x P_{Cu,FL}$:
$$\frac{d D(x)}{dx} = -\frac{P_{Fe}}{x^2} + P_{Cu,FL} = 0$$
$$\frac{P_{Fe}}{x^2} = P_{Cu,FL} \implies \boxed{x^2 P_{Cu,FL} = P_{Fe}}$$
**Maximum efficiency occurs when variable copper loss equals constant iron loss.**
The load fraction for peak efficiency is $x = \sqrt{\frac{P_{Fe}}{P_{Cu,FL}}}$.

---

#### Q3(b): Economy of Reversed Middle-Phase Winding in 3-Phase Shell Transformers

In a 3-phase shell-type transformer, three single-phase frames are built side by side.
- For a balanced 3-phase supply, the instantaneous sum of phase fluxes is zero: $\Phi_A + \Phi_B + \Phi_C = 0$.
- **If all three coils are wound in the same direction**:
  The flux in the common yoke separating limbs A and B is the vector difference $\vec{\Phi}_{\text{yoke}} = \vec{\Phi}_A - \vec{\Phi}_B$.
  Since $\vec{\Phi}_A$ and $\vec{\Phi}_B$ are 120° apart, $|\vec{\Phi}_A - \vec{\Phi}_B| = \sqrt{3}\Phi_m \approx 1.732\Phi_m$.
  The yoke steel cross-section must be sized for $1.732\Phi_m$, demanding a massive iron core.
- **If the middle phase (B) winding is wound in reverse**:
  The effective flux of phase B is negated ($-\vec{\Phi}_B$). The yoke flux becomes:
  $$\vec{\Phi}_{\text{yoke}} = \vec{\Phi}_A - (-\vec{\Phi}_B) = \vec{\Phi}_A + \vec{\Phi}_B = -\vec{\Phi}_C$$
  The magnitude of the resultant flux in the yoke is now simply $|\vec{\Phi}_C| = \mathbf{\Phi_m}$!
- **Core Economy**: Reversing the middle coil reduces peak yoke flux from $1.732\Phi_m$ down to $1.0\Phi_m$, allowing a **42.3% reduction in the cross-sectional area of the common yokes**, saving substantial laminated steel and reducing core weight.

---

#### Q3(c): Paralleling Yd11 With Dy1: Feasibility Analysis

- **Yd11 Vector Group**: Star primary, Delta secondary. Secondary line voltage leads primary line voltage by $11 \times 30° = 330° \equiv -30°$ (secondary lags by 30°).
- **Dy1 Vector Group**: Delta primary, Star secondary. Secondary line voltage lags primary line voltage by $1 \times 30° = 30°$ (or points to 1 o'clock, $+30°$ phase displacement).
- **Phase Angle Difference**:
  $$\Delta \theta = (+30°) - (-30°) = \mathbf{60°}$$
- **Consequence of Direct Connection**:
  Connecting the secondary terminals together forces an internal circulating voltage:
  $$\Delta V = 2 V_2 \sin\left(\frac{60°}{2}\right) = 2 V_2 \sin(30°) = V_2$$
  The circulating voltage driving current between the two transformers is equal to **100% of rated secondary voltage**! This represents a dead short-circuit across internal winding impedances, causing catastrophic overcurrent.
- **Conclusion**: Direct parallel operation is **physically impossible**.

---

### Question 4

#### Q4(a): Single Phasing of Δ-Δ Transformer and Open-Delta Voltages

> See full proof in [T-04: Open-Delta Connection: Why 57.7% and When to Use It](2018_2024_answer.md#t-04-open-delta-connection-why-577-and-when-to-use-it).

- When one transformer in a $\Delta$-$\Delta$ bank fails and is removed, the remaining two operate in an **Open-Delta (V-V)** connection.
- By KVL around the secondary terminals: $\vec{V}_{ab} + \vec{V}_{bc} + \vec{V}_{ca} = 0 \implies \vec{V}_{ca} = -(\vec{V}_{ab} + \vec{V}_{bc})$. Even without a third transformer, the line voltage across the open terminals is automatically synthesized with correct magnitude and 120° phase angle.
- The remaining bank delivers balanced 3-phase power at $\frac{1}{\sqrt{3}} = \mathbf{57.7\%}$ of original closed-delta bank capacity.

---

#### Q4(b): Scott (T-T) Connection for 3-Phase to 2-Phase Conversion

#### Working Principle:
The Scott connection uses two single-phase transformers to interconnect 3-phase and 2-phase AC systems:
1. **Main Transformer**:
   Connected directly across lines $A$ and $B$ of the 3-phase supply. Its primary has $N_1$ turns and center-tap $D$. The voltage across it is $V_{AB}$.
2. **Teaser Transformer**:
   Connected between the remaining phase line $C$ and the neutral center-tap $D$ of the main transformer.
   - Geometrically, in an equilateral triangle of line voltages, the altitude from line $C$ to the midpoint of $AB$ is:
     $$V_{CD} = \frac{\sqrt{3}}{2} V_{AB} \approx 0.866 V_{AB}$$
   - Therefore, to induce the same volts-per-turn as the main transformer, the teaser primary winding is wound with exactly:
     $$N_{\text{teaser}} = \frac{\sqrt{3}}{2} N_1 \approx 0.866 N_1 \text{ turns}$$
3. **Phase Quadrature**:
   In balanced 3-phase geometry, altitude phasor $\vec{V}_{CD}$ is perpendicular (90° out of phase) to base phasor $\vec{V}_{AB}$. This 90° temporal relationship transforms into two balanced, equal-magnitude secondary voltages displaced by exactly 90°, creating a pure 2-phase supply.
4. **Reversible**: Because transformers are reciprocal, energizing the secondaries from a 2-phase source produces balanced 3-phase power at the primary terminals.

---

#### Q4(c): Commercial / All-Day Efficiency Problem

#### Given Data:
- Rating $S = 100\text{ kVA}$. Full-load losses $= 6\text{ kW}$ split equally:
  - Iron loss $P_{Fe} = 3\text{ kW}$ (constant 24 hours)
  - Full-load copper loss $P_{Cu,FL} = 3\text{ kW}$
- Daily Operating Schedule:
  - Full load ($x = 1.0$) for 3 hours
  - Half load ($x = 0.5$) for 4 hours
  - No load ($x = 0$) for remaining 17 hours

#### Step-by-Step Energy Balance:
1. **Energy Output (assuming unity power factor)**:
   $$W_{\text{out}} = (1.0 \times 100\text{ kW} \times 3\text{ h}) + (0.5 \times 100\text{ kW} \times 4\text{ h}) + 0 = 300 + 200 = \mathbf{500\text{ kWh}}$$
2. **Iron Loss Energy (continuous 24 hours)**:
   $$W_{Fe} = 3\text{ kW} \times 24\text{ h} = \mathbf{72\text{ kWh}}$$
3. **Copper Loss Energy**:
   - Full-load period (3 h): $1.0^2 \times 3\text{ kW} \times 3\text{ h} = 9\text{ kWh}$
   - Half-load period (4 h): $(0.5)^2 \times 3\text{ kW} \times 4\text{ h} = 0.25 \times 3 \times 4 = 3\text{ kWh}$
   - No-load period (17 h): $0\text{ kWh}$
   $$W_{Cu} = 9 + 3 + 0 = \mathbf{12\text{ kWh}}$$
4. **Total Energy Input & Commercial Efficiency**:
   $$W_{\text{loss}} = W_{Fe} + W_{Cu} = 72 + 12 = 84\text{ kWh}$$
   $$W_{\text{in}} = W_{\text{out}} + W_{\text{loss}} = 500 + 84 = 584\text{ kWh}$$
   $$\eta_{\text{commercial}} = \frac{500}{584} \times 100\% = \mathbf{85.62\%}$$

---

## SECTION - B (Induction Motors: Q5 to Q8)

### Question 5

#### Q5(a): Operating Principle of a 3-Phase Induction Motor

1. **RMF Generation**: Balanced 3-phase currents in distributed stator windings create a constant-magnitude magnetic field ($1.5\Phi_m$) rotating at synchronous speed $N_s = \frac{120f}{P}$.
2. **Induced Rotor Currents**: As the stator field sweeps past the stationary rotor conductors, flux lines are cut at relative speed $N_s - N$. By Faraday's Law, an alternating EMF is induced in the rotor bars: $e_{2s} = s E_2$. Because rotor conductors form a closed circuit, strong circulating rotor currents flow.
3. **Torque Generation**: Rotor current-carrying bars reside within the stator magnetic field, experiencing a Lorentz force ($\vec{F} = I \vec{L} \times \vec{B}$) that produces rotational torque.
4. **Lenz's Law Compliance**: The rotor accelerates in the direction of the rotating field to minimize relative motion. It must always run at a speed $N$ strictly less than $N_s$ ($s > 0$). If $N$ were ever to reach $N_s$, relative cutting of flux would cease, induced EMF would vanish, rotor current would drop to zero, and torque would collapse.

---

#### Q5(b): Why Induction Motor is Called a Rotating Transformer

![Induction motor as a generalized rotating transformer showing stator primary, air gap, and short-circuited rotor secondary](../Books/diagrams/Ch-34_p58_fig45.jpg)

- **The Analogy**:
  - The stator acts as the transformer primary, receiving AC power from the grid.
  - The rotor acts as a short-circuited secondary, receiving power entirely through electromagnetic induction across the air gap.
  - At standstill ($s = 1$), rotor frequency equals stator frequency ($f_r = f$), and the machine is an exact physical transformer with an air gap.
  - When running ($s < 1$), the secondary rotates mechanically, converting electrical energy into mechanical power while throttling secondary electrical frequency down to $f_r = s f$.
- **Practical Trade-offs**:
  - *Advantages*: Rugged, brushless, no commutator, self-starting, explosion-proof, minimal maintenance.
  - *Disadvantages*: Low power factor at light loads, difficult speed control, high starting inrush current (5–8 $\times I_{\text{rated}}$).

---

#### Q5(c): Numerical: 4-Pole, 50 Hz Induction Motor

#### Given Data: $P = 4, f = 50\text{ Hz}$
1. **Synchronous Speed**:
   $$N_s = \frac{120 f}{P} = \frac{120 \times 50}{4} = \mathbf{1500\text{ rpm}}$$
2. **Rotor Speed at $s = 4\% = 0.04$**:
   $$N = N_s (1 - s) = 1500 \times (1 - 0.04) = 1500 \times 0.96 = \mathbf{1440\text{ rpm}}$$
3. **Rotor Frequency at $N = 600\text{ rpm}$**:
   $$s = \frac{N_s - N}{N_s} = \frac{1500 - 600}{1500} = \frac{900}{1500} = 0.60$$
   $$f_r = s f = 0.60 \times 50 = \mathbf{30\text{ Hz}}$$

---

### Question 6

#### Q6(a): Circle Diagram Analysis (415V, 29.84 kW Delta IM)

![Construction of Circle Diagram](../Books/diagrams/ch35_p06_fig35_09.jpg)

#### Test Data Scaling:
- **No-Load Test ($V_L = 415\text{ V}, I_0 = 21\text{ A}, W_0 = 1250\text{ W}$)**:
  $$\cos\phi_0 = \frac{W_0}{\sqrt{3} V_L I_0} = \frac{1250}{\sqrt{3} \times 415 \times 21} = \frac{1250}{15{,}094} = 0.0828 \implies \phi_0 = 85.25°$$
  Active component: $I_{0w} = I_0 \cos\phi_0 = 1.74\text{ A}$
  Magnetizing component: $I_{0m} = I_0 \sin\phi_0 = 20.93\text{ A}$
- **Blocked-Rotor Test scaled to rated 415 V ($V_{sc} = 100\text{ V}, I_{sc,\text{test}} = 45\text{ A}, W_{sc,\text{test}} = 2730\text{ W}$)**:
  $$I_{sc} = 45 \times \frac{415}{100} = 186.75\text{ A}$$
  $$\cos\phi_{sc} = \frac{W_{sc}}{\sqrt{3} V_{sc} I_{sc,\text{test}}} = \frac{2730}{\sqrt{3} \times 100 \times 45} = 0.3503 \implies \phi_{sc} = 69.5°$$
- **Graphical Extraction at Rated Output ($29.84\text{ kW}$)**:
  Plotting no-load point $O'$ and short-circuit point $S$ on the complex plane defines the Heyland circle locus. Reading the vector at the height representing $29.84\text{ kW}$ output:
  - **Full-load Line Current**: $\approx \mathbf{58\text{ A}}$
  - **Full-load Power Factor**: $\approx \mathbf{0.71\text{ lagging}}$
  - **Maximum Torque**: Vertical distance from circle peak to torque line yields $T_{\max} \approx 2.5 \times T_{\text{rated}}$.

---

#### Q6(b): Condition for Quadrature Currents in Capacitor Split-Phase Motor

To develop maximum starting torque, auxiliary winding current $\vec{I}_a$ and main winding current $\vec{I}_m$ must be 90° apart:
- Main winding impedance: $\vec{Z}_m = r_m + j X_m = Z_m \angle \phi_m$, where $\tan\phi_m = \frac{X_m}{r_m}$.
- Auxiliary circuit with series capacitor $X_c$: $\vec{Z}_a = r_a + j(X_a - X_c) = Z_a \angle -\phi_a$, where $\tan\phi_a = \frac{X_c - X_a}{r_a}$.
- For quadrature phase angle: $\phi_m + \phi_a = 90° \implies \phi_a = 90° - \phi_m$.
- Taking tangent on both sides:
  $$\tan\phi_a = \tan(90° - \phi_m) = \cot\phi_m = \frac{r_m}{X_m}$$
- Equating expressions for $\tan\phi_a$:
  $$\frac{X_c - X_a}{r_a} = \frac{r_m}{X_m} \implies X_c = X_a + \frac{r_a r_m}{X_m}$$
- When core impedance and mutual coupling effects are included in the exact formulation, this generalizes to:
  $$\boxed{X_c = X_a + \frac{r_a r_m}{Z_m + X_m}}$$

---

### Question 7

#### Q7(a): Induction Motor Plugging and Standard Tests

![3-Phase Induction Motor Blocked-Rotor Test Circuit Connection (Two-Wattmeter Method)](diagrams/im_blocked_rotor_test_circuit.png)
![3-Phase Induction Motor No-Load Test Connection and Loss Separation Curves](../SlidesByMaam/diagrams/L-05_ECE-2107_p04_fig01.jpg)

- **Plugging**: An electric braking method where two stator phases are swapped while running. This suddenly reverses the RMF rotation direction. Operating slip becomes $s = \frac{N_s - (-N)}{N_s} > 1$. The motor develops massive reverse torque, bringing the shaft to a rapid halt. A zero-speed switch disconnects power at zero speed to prevent reverse rotation.
- **Blocked Rotor Test ($s = 1.0$)**: Clamped shaft, low voltage (~15%) applied. Core loss is negligible ($\propto V^2$). Input power yields series equivalent resistance $R_{01}$ and reactance $X_{01}$.
- **No-Load Test ($s \approx 0$)**: Motor runs uncoupled at rated voltage. Rotor branch acts as open circuit. Wattmeter measures core and mechanical rotational losses, yielding shunt parameters $R_c$ and $X_m$.

---

#### Q7(b): Direct-On-Line (DOL) Starting Effects and Mitigation

- **Severe Drawbacks for Large Motors (> 25 kW)**:
  1. *Huge Inrush Current*: Draws 6 to 8 times full-load rated current at very low power factor (0.2 lag), causing voltage sag on the supply network that disrupts adjacent equipment.
  2. *Mechanical Shock*: High starting torque surge creates mechanical stress on couplings, gearboxes, and driven machinery.
  3. *Thermal Stress*: Prolonged acceleration draws high $I^2R$ heat that degrades insulation life.
- **Mitigation Methods**:
  1. *Star-Delta Starter*: Starts in Star ($V_\phi = V_L/\sqrt{3}$), reducing starting current and torque to $1/3$ of DOL values before switching to Delta.
  2. *Autotransformer Starter*: Provides voltage taps (50%, 65%, 80%) to tailor starting torque and current.
  3. *Solid-State Soft Starter*: Uses thyristors to smoothly ramp up terminal voltage without current spikes.
  4. *Variable Frequency Drive (VFD)*: Provides full torque at rated current by controlling frequency and voltage together.

---

#### Q7(c): Braking and Speed Control Methods

- **Braking Methods**:
  1. *Plugging*: Reversing stator phase sequence (fastest, high energy dissipation).
  2. *Dynamic (DC Rheostatic) Braking*: Stator is disconnected from AC supply and connected to DC source, creating a stationary magnetic field. Rotating rotor dissipates kinetic energy as heat in external resistors.
  3. *Regenerative Braking*: Rotor is driven faster than synchronous speed ($N > N_s, s < 0$), converting kinetic energy into electrical power returned to the grid.
- **Speed Control Methods**:
  1. *V/f Control (Variable Frequency Drives)*: Smooth, efficient speed variation across a wide range by keeping $V/f$ constant.
  2. *Pole Changing*: Switching stator winding configurations to obtain multiple synchronous speeds (e.g., 4-pole / 8-pole).
  3. *Rotor Resistance Control (Wound Rotor)*: Adding external resistance via slip rings; reduces speed by increasing slip (lossy).

---

### Question 8

#### Q8(a): Pull-Out Torque and Maximum Starting Torque Derivation

- **Pull-Out (Breakdown) Torque ($T_{\max}$)**: The peak electromagnetic torque an induction motor can generate. If load torque exceeds pull-out torque, the motor abruptly stalls.
- **Derivation of Maximum Starting Torque**:
  At standstill ($s = 1$):
  $$T_{st} = \frac{k E_2^2 R_2}{R_2^2 + X_2^2}$$
  Differentiating with respect to $R_2$ and setting to zero:
  $$\frac{d T_{st}}{d R_2} = k E_2^2 \left[\frac{(R_2^2 + X_2^2) - 2 R_2^2}{(R_2^2 + X_2^2)^2}\right] = 0 \implies R_2^2 = X_2^2 \implies \mathbf{R_2 = X_2}$$
  Substituting $R_2 = X_2$:
  $$T_{st,\max} = \frac{k E_2^2 X_2}{X_2^2 + X_2^2} = \boxed{\frac{k E_2^2}{2 X_2}}$$
  Thus, maximum starting torque equals breakdown torque $T_{\max}$.

---

#### Q8(b): Why Single-Phase Induction Motors Are Not Self-Starting

> See full proof in [IM-03: Single-Phase Induction Motor: Double Revolving Field Theory](2018_2024_answer.md#im-03-single-phase-induction-motor-double-revolving-field-theory).

- A single stator winding produces a pulsating stationary magnetic field $\Phi(t) = \Phi_m \sin\omega t$.
- By double revolving field theory, this decomposes into two equal and opposite rotating fields: forward field ($\Phi_f = \Phi_m/2$ at $+N_s$) and backward field ($\Phi_b = \Phi_m/2$ at $-N_s$).
- At standstill ($N = 0$), both forward and backward slips are $1.0$ ($s_f = s_b = 1.0$). The torques developed are identical in magnitude and opposite in direction ($T_f = T_b$).
- Resultant starting torque is strictly **zero ($T_{\text{net}} = 0$)**.

---

#### Q8(c): Numerical Problem: Torque Ratio and Speed at Max Torque

#### Given Data:
- Poles $P = 8, f = 50\text{ Hz} \implies N_s = \frac{120 \times 50}{8} = 750\text{ rpm}$
- Standstill rotor parameters: $R_2 = 0.001\,\Omega, X_2 = 0.005\,\Omega$
- Full-load slip $s_f = 2\% = 0.02$

#### 1. Slip and Speed at Maximum Torque:
- Slip at max torque:
  $$s_{mT} = \frac{R_2}{X_2} = \frac{0.001}{0.005} = \mathbf{0.20 \quad (20\% \text{ slip})}$$
- Speed at maximum torque:
  $$N_{mT} = N_s (1 - s_{mT}) = 750 \times (1 - 0.20) = \mathbf{600\text{ rpm}}$$

#### 2. Ratio of Maximum Torque to Full-Load Torque ($T_{\max}/T_{FL}$):
Using the standard torque ratio formula with $a = s_{mT} = 0.20$ and $s = 0.02$:
$$\frac{T_{FL}}{T_{\max}} = \frac{2 a s}{a^2 + s^2} = \frac{2 \times 0.20 \times 0.02}{(0.20)^2 + (0.02)^2} = \frac{0.008}{0.040 + 0.0004} = \frac{0.008}{0.0404} \approx 0.1980$$
Inverting to find the ratio:
$$\frac{T_{\max}}{T_{FL}} = \frac{1}{0.1980} = \mathbf{5.05}$$

---

*Source:* [PrevYearQuestions/2019.md](../PrevYearQuestions/2019.md)

---

[← 2018 Answer](2018_answer.md) | [🏠 Index](README.md) | [2020 Answer →](2020_answer.md)
