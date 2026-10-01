# ECE 2207: 2021 Semester Final: Explanation Style Answers
**RUET · ECE Dept · 2nd Year Odd Semester 2021**

> Deep tutorial-style explanations focusing on first-principles physics, "why over what", step-by-step logic, and practical engineering intuition.
> Core cross-cutting theory topics are detailed in [2018_2024_answer.md](2018_2024_answer.md).

---

## SECTION - A (Transformers: Q1 to Q4)

### Question 1

#### Q1(a): Physical Meaning of Ideal Transformer Assumptions

![Core and windings of an ideal transformer](../Books/diagrams/Ch-32_p07_fig13.jpg)

An "ideal transformer" is an idealized mathematical model that isolates the pure electromagnetic transformation mechanism from parasitic non-idealities:
1. **Zero Winding Resistance ($R_1 = R_2 = 0$)**: Coils are assumed to be wound with hypothetical perfect conductors (zero resistivity). This eliminates all $I^2R$ copper losses and internal ohmic voltage drops.
2. **Zero Leakage Flux ($\Phi_{l1} = \Phi_{l2} = 0$)**: 100% of magnetic flux is confined inside the core, linking every turn of both primary and secondary windings identically. Hence, leakage reactances are zero ($X_1 = X_2 = 0$).
3. **Infinite Core Permeability ($\mu_r \to \infty$)**: The core offers zero magnetic reluctance ($\mathcal{R} = \frac{l}{\mu A} \to 0$). Therefore, establishing full operating mutual flux $\Phi_m$ requires zero magnetizing ampere-turns: magnetizing current $I_m = 0$.
4. **Zero Core Losses ($P_h = 0, P_e = 0$)**: The core material exhibits zero hysteresis loop area and infinite electrical resistivity (zero eddy currents). The core never heats up ($I_c = 0$).
5. **Net Consequences**: No-load current is zero ($I_0 = 0$), input power equals output power at all times ($\eta = 100\%$), and voltage regulation is perfect ($0\%$, terminal voltage never drops with load).

---

#### Q1(b): Derivation of RMS EMF and EMF-per-Turn Equality

> For full derivation see [T-01: EMF Equation: $E = 4.44 f N \Phi_m$](2018_2024_answer.md#t-01-emf-equation-e--444-f-n-phi_m-full-derivation-and-intuition).

- Peak induced EMF: $E_m = \omega N \Phi_m = 2\pi f N \Phi_m$.
- RMS value: $E = \frac{2\pi f N \Phi_m}{\sqrt{2}} = \sqrt{2}\pi f N \Phi_m \approx 4.44 f N \Phi_m$.
- **Why EMF per turn is strictly equal**:
  $$\frac{E_1}{N_1} = 4.44 f \Phi_m = \frac{E_2}{N_2}$$
  Because both coils are threaded by the exact same alternating core flux $\Phi(t)$, every single loop of copper encircling the core experiences the exact same rate of change of magnetic flux ($-\frac{d\Phi}{dt}$). The voltage induced per turn is a fundamental invariant of the magnetic core.

---

#### Q1(c): Numerical: 25 kVA, 500/50 Turns, 3000V/50Hz Transformer

#### Given Data:
- Rating $S = 25\text{ kVA} = 25{,}000\text{ VA}$
- Primary turns $N_1 = 500$, Secondary turns $N_2 = 50$
- Primary voltage $V_1 = 3000\text{ V}$, Frequency $f = 50\text{ Hz}$

#### Step-by-Step Solution:
1. **Turns Ratio and Secondary EMF**:
   $$a = \frac{N_1}{N_2} = \frac{500}{50} = 10$$
   $$E_2 = \frac{E_1}{a} = \frac{3000}{10} = \mathbf{300\text{ V}}$$
2. **Full-Load Primary and Secondary Currents**:
   $$I_1 = \frac{S}{V_1} = \frac{25{,}000}{3000} = \mathbf{8.33\text{ A}}$$
   $$I_2 = \frac{S}{V_2} = \frac{25{,}000}{300} = \mathbf{83.33\text{ A}}$$
   *(Notice $I_2 = a I_1 = 10 \times 8.33 = 83.3\text{ A}$, perfectly verifying ampere-turn balance $N_1 I_1 = N_2 I_2$)*.
3. **Maximum Core Flux ($\Phi_m$)**:
   From $E_1 = 4.44 f N_1 \Phi_m$:
   $$\Phi_m = \frac{E_1}{4.44 f N_1} = \frac{3000}{4.44 \times 50 \times 500} = \frac{3000}{111{,}000} = \mathbf{0.02703\text{ Wb} = 27.03\text{ mWb}}$$

---

### Question 2

#### Q2(a): Complete Phasor Diagram of a Practical Transformer

![Complete vector diagrams of transformer](../Books/diagrams/Ch-32_p21_fig29.jpg)

#### Physical Walkthrough of Phasor Evolution:
1. **Magnetic Core Reference**: Core flux $\vec{\Phi}_m$ is drawn horizontal (0°).
2. **Induced EMFs**: Both self-induced EMF $\vec{E}_1$ and mutually induced EMF $\vec{E}_2$ lag flux by 90° (drawn vertically downward, −90°).
3. **Secondary Terminal Voltage ($\vec{V}_2$)**:
   When secondary current $\vec{I}_2$ flows at lagging angle $\phi_2$, internal winding impedance causes drops. By KVL: $\vec{E}_2 = \vec{V}_2 + \vec{I}_2 R_2 + j \vec{I}_2 X_2$.
   Graphically, start from the origin, draw $\vec{V}_2$, add $\vec{I}_2 R_2$ parallel to $\vec{I}_2$, and add $j \vec{I}_2 X_2$ leading $\vec{I}_2$ by 90° to reach $\vec{E}_2$. Thus $\vec{V}_2$ is smaller than $\vec{E}_2$.
4. **Primary Current ($\vec{I}_1$)**:
   Total primary current is the phasor sum of two components:
   $$\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$$
   - $\vec{I}_0$: No-load excitation current ($I_c$ along $-E_1$, $I_m$ along $\Phi_m$).
   - $\vec{I}_2'$: Primary balancing current ($180°$ opposite to secondary current $\vec{I}_2$, magnitude $K I_2$).
5. **Primary Applied Voltage ($\vec{V}_1$)**:
   Applied voltage must overcome both counter-EMF ($-\vec{E}_1$) and internal primary drops:
   $$\vec{V}_1 = -\vec{E}_1 + \vec{I}_1 R_1 + j \vec{I}_1 X_1$$
   Draw $-\vec{E}_1$ vertically upward (+90°), add $\vec{I}_1 R_1$ parallel to $\vec{I}_1$, and add $j \vec{I}_1 X_1$ leading $\vec{I}_1$ by 90°. The closing vector from origin is $\vec{V}_1$.

---

#### Q2(b): No-Load Test: Procedure, Circuit, and Purpose

![Open circuit or No load test schematic](../SlidesByMaam/diagrams/L-10_ECE-2107_p17_fig01.jpg)

#### Physical Rationale:
- **Why perform on LV side**: Safety and convenience. Applying rated 220 V is much safer, easier to regulate with a standard laboratory variac, and meter than several thousand volts on the HV side.
- **Why power represents strictly core loss**: Secondary winding is open ($I_2 = 0$). Primary draws only no-load current $I_0$ (typically 2–5% of rated). Primary copper loss is $I_0^2 R_1 \propto (0.03)^2 \approx 0.09\%$ of full-load copper loss—completely negligible! Hence the wattmeter reading $W_0$ captures purely core hysteresis and eddy current dissipation: $P_{Fe} = W_0$.
- **Extraction of Shunt Parameters**:
  $$\cos\phi_0 = \frac{W_0}{V_0 I_0}, \quad I_c = I_0 \cos\phi_0, \quad I_m = I_0 \sin\phi_0$$
  $$R_c = \frac{V_0}{I_c}, \qquad X_m = \frac{V_0}{I_m}$$

---

#### Q2(c): Numerical SC Test and Voltage Regulation Calculation

#### Given Data:
- Rating: $20\text{ kVA}, 2400/240\text{ V}, 50\text{ Hz}$
- SC test conducted on HV side ($2400\text{ V}$): $V_{sc} = 72\text{ V}, W_{sc} = 275\text{ W}, I_{sc} = I_{1,\text{rated}}$

#### Step-by-Step Parameter Extraction:
1. **Rated HV Current**:
   $$I_{1,\text{rated}} = \frac{20{,}000}{2400} = 8.333\text{ A}$$
2. **Series Parameters referred to HV**:
   $$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{275}{(8.333)^2} = \frac{275}{69.44} = \mathbf{3.960\,\Omega}$$
   $$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{72}{8.333} = \mathbf{8.640\,\Omega}$$
   $$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2} = \sqrt{(8.640)^2 - (3.960)^2} = \sqrt{74.65 - 15.68} = \sqrt{58.97} = \mathbf{7.679\,\Omega}$$
3. **Voltage Regulation at Full Load, 0.8 PF Lagging ($\cos\phi = 0.8, \sin\phi = 0.6$)**:
   $$\Delta V_1 = I_1 (R_{01}\cos\phi + X_{01}\sin\phi) = 8.333 \times (3.960 \times 0.8 + 7.679 \times 0.6)$$
   $$\Delta V_1 = 8.333 \times (3.168 + 4.607) = 8.333 \times 7.775 = 64.79\text{ V}$$
   $$\text{VR\%} = \frac{\Delta V_1}{V_1} \times 100\% = \frac{64.79}{2400} \times 100\% = \mathbf{2.70\%}$$

---

### Question 3

#### Q3(a): Limitations of Y-Y Transformers and the Third Harmonic Problem

#### Why Third Harmonics Exist:
Ferromagnetic cores have non-linear $B-H$ saturation characteristics. To produce a sinusoidal flux wave $\Phi(t)$, the required magnetizing current cannot be sinusoidal—it must contain a pronounced 3rd harmonic component (~30–40% of fundamental at 150 Hz).

#### The Y-Y Trap:
In a 3-phase system, third harmonic currents are zero-sequence: they are completely in phase in all three lines. In an ungrounded 3-wire star (Y-Y) connection, all three line currents must sum to zero at the neutral ($i_a + i_b + i_c = 0$). Since third harmonics want to flow in the same direction simultaneously, they find **no return path** and are completely blocked!
- **Consequence**: Since 3rd harmonic magnetizing currents cannot flow, the core flux is forced to become non-sinusoidal (flat-topped).
- A flat-topped flux wave induces sharply peaked EMFs in each phase winding ($e = -N \frac{d\Phi}{dt}$). The phase-to-neutral voltages become severely distorted, containing large 3rd harmonic voltage components that overstress winding insulation and produce floating neutral instability.

#### Engineering Solutions:
1. **Grounded Neutral (4-Wire System)**: Provides an external return wire through earth for the zero-sequence 3rd harmonic currents, restoring sinusoidal core flux.
2. **Tertiary Delta Winding**: Adding a small auxiliary delta-connected third winding. The closed delta loop allows 3rd harmonic currents to circulate freely locally, trapping the harmonics inside the transformer and keeping phase voltages pure sine waves.
3. **Delta-Star (Δ-Y) Connection**: The delta primary allows 3rd harmonic currents to circulate freely within the delta loop.

---

#### Q3(b): Open-Delta (V-V) Operation When One Transformer is Damaged

> For comprehensive capacity and utilization proof see [T-04: Open-Delta Connection: Why 57.7% and When to Use It](2018_2024_answer.md#t-04-open-delta-connection-why-577-and-when-to-use-it).

- **Why it works**: By Kirchhoff's Voltage Law, the sum of line voltages in a closed loop is zero: $\vec{V}_{ab} + \vec{V}_{bc} + \vec{V}_{ca} = 0$. Even when transformer $CA$ is physically removed, the line voltages across the load terminals remain intact: $\vec{V}_{ca} = -(\vec{V}_{ab} + \vec{V}_{bc})$. The load continues to receive balanced 3-phase power.
- **Capacity**: Reduces to $\frac{\sqrt{3} V I}{3 V I} = \frac{1}{\sqrt{3}} = \mathbf{57.7\%}$ of original closed-delta bank capacity.

---

#### Q3(c): Complete Torque-Speed Characteristic of an Induction Motor

![Torque-Speed characteristics](../Books/diagrams/Chapman_Ch07_p202_torque_speed_r2_comp.jpg)

The induction machine operates in three distinct operational regions depending on rotor speed $N$ and slip $s = \frac{N_s - N}{N_s}$:
1. **Motoring Region ($0 < N < N_s$, $0 < s < 1$)**:
   Normal operation. Stator field rotates faster than rotor. Electromagnetic torque is positive, dragging the rotor forward in the direction of field rotation.
   - At $N = 0$ ($s = 1$): Motor produces starting torque $T_{st}$.
   - At $N = N_{mT}$ ($s = s_{mT} = R_2/X_2$): Motor develops breakdown (pull-out) torque $T_{\max}$.
   - Near synchronous speed ($s \approx 0.02\text{–}0.05$): Normal operating stable linear zone.
   - At synchronous speed $N = N_s$ ($s = 0$): Relative motion ceases $\implies$ no induced EMF $\implies$ torque drops to zero.
2. **Generating Region ($N > N_s$, $s < 0$)**:
   Rotor is driven mechanically faster than synchronous speed by an external prime mover (e.g., wind turbine). Slip becomes negative. Induced rotor current reverses direction, creating negative torque that opposes rotation. The machine converts mechanical power into electrical power fed back to the AC grid.
3. **Plugging / Braking Region ($N < 0$, $s > 1$)**:
   Two stator supply leads are swapped while running, suddenly reversing the direction of stator RMF rotation. The rotor is now spinning opposite to the field ($N < 0 \implies s = \frac{N_s - (-N)}{N_s} > 1$). The machine develops strong counter-torque that rapidly decelerates the rotor to a dead stop (used for rapid emergency braking).

---

### Question 4

#### Q4(a): Conditions for Parallel Operation of 3-Phase Transformers

Connecting two 3-phase transformers in parallel requires strict adherence to five fundamental rules:
1. **Identical Voltage Ratios**: Prevents continuous circulating currents between transformers at no load.
2. **Identical Polarity**: Prevents dead short-circuits.
3. **Same Phase Sequence**: Reversing phase sequence (e.g., A-B-C vs A-C-B) creates line-to-line short circuits with full line voltage across pairs of terminals.
4. **Zero Relative Phase Displacement (Same Vector Group)**: Both units must belong to compatible clock groups (e.g., both Dyn11 or both Yyn0). A 30° phase shift between secondary line voltages causes massive circulating currents driven by $\Delta V = 2 V \sin(15°) \approx 0.52 V_{\text{rated}}$.
5. **Equal Per-Unit Impedances ($Z_{pu}$)**: Ensures that external load divides strictly in proportion to their kVA ratings without overloading either unit.

---

#### Q4(b): Physical Methods for Generating Magnetic Fields

1. **Permanent Magnets**: Arise from uncancelled microscopic electron spins and orbital angular momenta in ferromagnetic materials (NdFeB, Alnico) aligned within magnetic domains. Produces constant DC flux with zero power dissipation.
2. **DC Electromagnets**: DC current flowing through wire coils generates steady magnetic fields via Ampere's Law ($\nabla \times \vec{H} = \vec{J}$). Used in DC machine stator poles and synchronous rotor exciters.
3. **Pulsating AC Electromagnets**: Single-phase alternating current through a coil sets up a field whose magnitude oscillates sinusoidally along a fixed spatial axis. Used in transformer cores.
4. **Rotating Magnetic Field (Polyphase Stator)**: Balanced polyphase AC currents distributed in spatial windings create a smoothly revolving field of constant amplitude. Three-phase windings yield $1.5\Phi_m$ rotating at synchronous speed, forming the operating foundation of all AC induction and synchronous motors.

---

#### Q4(c): Speed Control of Slip-Ring IM by Adding Rotor Resistance

#### Given Data:
- Poles $P = 4$, Frequency $f = 50\text{ Hz} \implies N_s = \frac{120 \times 50}{4} = 1500\text{ rpm}$
- Rotor resistance $R_2 = 0.30\,\Omega/\text{phase}$
- Initial operating point: $N_1 = 1440\text{ rpm} \implies s_1 = \frac{1500 - 1440}{1500} = 0.04$
- Target operating point: $N_2 = 1320\text{ rpm} \implies s_2 = \frac{1500 - 1320}{1500} = 0.12$
- Condition: Load torque remains strictly constant ($T_1 = T_2$).

#### Physical Principle and Solution:
In the normal operating stable zone (small slip), rotor leakage reactance is negligible compared to rotor resistance ($s X_2 \ll R_2$). The torque equation simplifies to:
$$T \approx \frac{k s E_2^2}{R_{\text{total}}}$$
For constant torque at constant applied voltage:
$$\frac{s_1}{R_2} = \frac{s_2}{R_2 + R_{\text{ext}}}$$
$$\frac{0.04}{0.30} = \frac{0.12}{0.30 + R_{\text{ext}}}$$
$$0.30 + R_{\text{ext}} = \frac{0.12 \times 0.30}{0.04} = 3 \times 0.30 = 0.90\,\Omega$$
$$R_{\text{ext}} = 0.90 - 0.30 = \mathbf{0.60\,\Omega/\text{phase}}$$

*Physical Insight:* To develop the same electromagnetic torque at a lower speed (higher slip), the rotor current must be maintained at its original value. Since induced rotor EMF increases proportionally with slip ($E_{2s} = s E_2$), total rotor circuit resistance must be increased in the exact same proportion to keep $I_2 \approx \frac{s E_2}{R_{\text{total}}}$ constant.

---

## SECTION - B (Induction Motors: Q5 to Q8)

### Question 5

#### Q5(a): Definitions of Synchronous Speed, Slip, and Slip Speed

1. **Synchronous Speed ($N_s$)**: The rotational speed of the magnetic field produced by the balanced 3-phase stator currents inside the air gap. It depends solely on supply frequency $f$ and stator pole pairs $P$:
   $$N_s = \frac{120 f}{P}\text{ rpm}, \qquad \omega_s = \frac{4\pi f}{P}\text{ rad/s}$$
2. **Slip Speed ($N_{\text{slip}}$)**: The relative physical speed between the rotating magnetic field and the actual mechanical rotor:
   $$N_{\text{slip}} = N_s - N\text{ rpm}$$
   *Physical Meaning:* This relative motion is what causes the rotor bars to cut magnetic flux lines, inducing voltage and current by Faraday's Law. Without slip speed, induced rotor voltage would be zero.
3. **Slip ($s$)**: The normalized fractional ratio of slip speed to synchronous speed:
   $$s = \frac{N_s - N}{N_s}$$
   - Standstill: $N = 0 \implies s = 1.0$.
   - Synchronous speed: $N = N_s \implies s = 0$.
   - Normal full-load motoring: $s \approx 0.02\text{ to }0.05$.

---

#### Q5(b): Starting Torque Derivation and Maximum Starting Torque Condition

Starting torque is obtained by evaluating the torque equation at standstill ($s = 1$):
$$T_{st} = \frac{k (1) E_2^2 R_2}{R_2^2 + (1)^2 X_2^2} = \frac{k E_2^2 R_2}{R_2^2 + X_2^2}$$
To find the rotor resistance that maximizes starting torque, differentiate $T_{st}$ with respect to $R_2$ and set to zero:
$$\frac{dT_{st}}{dR_2} = k E_2^2 \left[ \frac{(R_2^2 + X_2^2)(1) - R_2(2 R_2)}{(R_2^2 + X_2^2)^2} \right] = 0$$
$$R_2^2 + X_2^2 - 2 R_2^2 = 0 \implies R_2^2 = X_2^2 \implies \mathbf{R_2 = X_2}$$

Substituting $R_2 = X_2$ into the starting torque expression:
$$T_{st,\max} = \frac{k E_2^2 X_2}{X_2^2 + X_2^2} = \boxed{\frac{k E_2^2}{2 X_2}}$$
Notice that $T_{st,\max}$ equals the absolute maximum running breakdown torque $T_{\max}$! In slip-ring (wound-rotor) induction motors, external resistance is inserted so that total rotor resistance equals standstill reactance ($R_2 + R_{\text{ext}} = X_2$), allowing the motor to start with maximum possible torque while drawing minimal starting current.

---

#### Q5(c): Rotating Magnetic Field Produced by a 2-Phase Supply

![Resultant 3-phase flux](../Books/diagrams/Ch-34_p10_fig14.jpg)

#### Setup:
Consider two stator windings placed 90° apart in space (Phase A along X-axis, Phase B along Y-axis), energized by balanced 2-phase currents 90° apart in time:
$$i_a(t) = I_m \sin\omega t, \qquad i_b(t) = I_m \sin(\omega t - 90°) = -I_m \cos\omega t$$

#### Spatial Flux Components:
- Flux along X-axis: $\Phi_x = \Phi_m \sin\omega t$
- Flux along Y-axis: $\Phi_y = -\Phi_m \cos\omega t$

#### Resultant Vector:
- **Magnitude**:
  $$\Phi_r = \sqrt{\Phi_x^2 + \Phi_y^2} = \sqrt{\Phi_m^2 \sin^2\omega t + \Phi_m^2 \cos^2\omega t} = \mathbf{\Phi_m = \text{constant}}$$
- **Spatial Angle**:
  $$\theta = \tan^{-1}\left(\frac{\Phi_y}{\Phi_x}\right) = \tan^{-1}\left(\frac{-\cos\omega t}{\sin\omega t}\right) = \omega t - 90°$$
  $$\frac{d\theta}{dt} = \omega = 2\pi f \implies N_s = \frac{120 f}{P}\text{ rpm}$$

**Comparison with 3-Phase**:
- 2-Phase produces constant flux magnitude of $\Phi_m$.
- 3-Phase produces constant flux magnitude of $1.5\Phi_m$ (50% larger flux from the same peak phase flux).

---

### Question 6

#### Q6(a): Effect of Supply Frequency Increase on Torque and Speed

When supply frequency jumps from $f_1$ to $f_2 > f_1$ with terminal voltage $V$ held constant:
1. **Synchronous Speed**: $N_s = \frac{120 f}{P}$ increases in direct proportion to $f$.
2. **Magnetic Flux Attenuation**: Core flux is $\Phi_m \propto \frac{V}{f}$. With $V$ constant and $f$ higher, core flux weakens significantly.
3. **Leakage Reactance**: Standstill reactance $X_2 = 2\pi f L_2$ increases proportionally with $f$.
4. **Catastrophic Drop in Breakdown Torque**:
   $$T_{\max} = \frac{k E_2^2}{2 X_2} \propto \frac{1}{\omega_s} \frac{(V/f)^2}{2 (2\pi f L_2)} \propto \frac{V^2}{f^3}$$
   Maximum torque collapses inversely with the **cube of frequency ($1/f^3$)**! A 20% frequency increase slashes maximum torque capability by over 42%.
5. **Why V/f Control is Mandatory**: To vary motor speed without sacrificing torque capability, variable frequency drives always adjust voltage and frequency simultaneously such that the ratio $V/f$ remains strictly constant.

---

#### Q6(b): Increase in Copper Loss when Line Voltage Drops to 90%

#### Given:
- Motor drives a constant-torque load ($T = \text{constant}$, independent of speed).
- Terminal voltage drops to $V_2 = 0.9 V_1$.

#### Physical Analysis:
In the normal low-slip operating range, torque is proportional to slip and voltage squared:
$$T \approx K \frac{s V^2}{R_2}$$
Since the load demands the exact same torque $T$:
$$s_1 V_1^2 = s_2 V_2^2 \implies s_2 = s_1 \left(\frac{V_1}{V_2}\right)^2 = s_1 \left(\frac{1}{0.9}\right)^2 = \frac{s_1}{0.81} \approx 1.2346\, s_1$$
Operating slip must increase by 23.46% to compensate for the weaker magnetic field.

Now consider rotor copper loss:
$$P_{r,Cu} = s P_g$$
Because load torque $T$ and synchronous speed $\omega_s$ are constant, air-gap power $P_g = T \omega_s$ remains constant.
Therefore, rotor copper loss is directly proportional to slip:
$$\frac{P_{Cu,\text{new}}}{P_{Cu,\text{old}}} = \frac{s_2}{s_1} = 1.2346$$
$$\text{Percentage Increase in Cu Loss} = (1.2346 - 1) \times 100\% = \mathbf{23.46\%}$$

*Physical Warning:* Operating an induction motor under undervoltage conditions causes it to draw substantially higher current and generate 23.5% more heat in its windings, frequently tripping thermal overload relays.

---

#### Q6(c): Rotor Efficiency Derivation

- Air gap input power: $P_g = 3 I_2^2 \frac{R_2}{s}$
- Rotor ohmic loss: $P_{r,Cu} = 3 I_2^2 R_2 = s P_g$
- Developed mechanical power: $P_m = P_g - P_{r,Cu} = (1-s) P_g$
- Rotor efficiency:
  $$\eta_{\text{rotor}} = \frac{P_m}{P_g} = \frac{(1-s) P_g}{P_g} = \boxed{1 - s}$$

---

### Question 7

#### Q7(a): Double-Field Revolving Theory of 1-Phase IM

![Resolution of alternating flux into two oppositely rotating fields](../Books/diagrams/VK_Mehta_Fig_9_03.jpeg)
![Torque-speed characteristic under double-field revolving theory showing zero starting torque](../Books/diagrams/VK_Mehta_Fig_9_04.jpeg)

> See full details in [IM-03: Single-Phase Induction Motor: Double Revolving Field Theory](2018_2024_answer.md#im-03-single-phase-induction-motor-double-revolving-field-theory).

- Forward field rotates at $+N_s$ with slip $s_f = s$.
- Backward field rotates at $-N_s$ with slip $s_b = 2 - s$.
- At standstill ($s = 1$), forward torque equals backward torque ($T_f = T_b$), yielding zero net starting torque.

---

#### Q7(b): Operation of Capacitor-Start-and-Run (Two-Value) Induction Motor

- **Starting**: Large electrolytic capacitor ($C_{st}$) in parallel with run capacitor ($C_{run}$) forces auxiliary current to lead main current by 90°, producing a balanced two-phase rotating field with high starting torque (200–350% FL).
- **Running**: Centrifugal switch disconnects $C_{st}$ at 75% speed. Small AC continuous-duty capacitor ($C_{run}$) remains in series with auxiliary winding, maintaining a clean rotating field under running conditions. This maximizes efficiency, achieves near-unity power factor (0.95), and eliminates acoustic vibration.

---

#### Q7(c): Calculation of Starting Capacitor for Quadrature Current

#### Given Data:
- Supply: $230\text{ V}, 50\text{ Hz}$
- Main winding impedance: $Z_m = 4.5 + j3.7\,\Omega$
- Auxiliary winding impedance: $Z_a = 9.5 + j3.5\,\Omega$

#### Condition for Quadrature Currents:
Auxiliary current $\vec{I}_a$ must lead main winding current $\vec{I}_m$ by exactly 90° in time:
1. **Main Winding Phase Angle**:
   $$\phi_m = \tan^{-1}\left(\frac{X_m}{R_m}\right) = \tan^{-1}\left(\frac{3.7}{4.5}\right) = \tan^{-1}(0.8222) = 39.43°\text{ lagging}$$
2. **Required Auxiliary Branch Phase Angle**:
   For $\vec{I}_a$ to lead $\vec{I}_m$ by 90°, $\vec{I}_a$ must lead the terminal voltage by:
   $$\phi_a = 90° - \phi_m = 90° - 39.43° = 50.57°\text{ leading}$$
3. **Net Auxiliary Reactance with Series Capacitor $X_C$**:
   Total auxiliary branch impedance is $Z_{\text{total},a} = R_a + j(X_a - X_C) = 9.5 - j(X_C - 3.5)$.
   For the branch to have a leading angle of $50.57°$:
   $$\tan(50.57°) = \frac{X_C - X_a}{R_a} = \frac{X_C - 3.5}{9.5}$$
   $$\tan(50.57°) = 1.2160$$
   $$X_C - 3.5 = 1.2160 \times 9.5 = 11.552\,\Omega$$
   $$X_C = 11.552 + 3.5 = \mathbf{15.052\,\Omega}$$
4. **Capacitance Value**:
   $$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 15.052} = \frac{1}{4728.7} = 2.1147 \times 10^{-4}\text{ F} = \mathbf{211.5\,\mu\text{F}}$$

---

### Question 8

#### Q8(a): Synchronous Watt Definition and Practical Meaning

#### Definition:
A **synchronous watt** is a convenient unit of torque used in AC motor analysis. It is defined as the torque which, at synchronous speed, develops one watt of mechanical power:
$$T \text{ (in synchronous watts)} = P_g \text{ (air-gap power in watts)}$$

#### Physical Meaning:
Electromagnetic torque in mechanical units (N-m) is:
$$T = \frac{P_g}{\omega_s} = \frac{P_g}{\frac{2\pi N_s}{60}}$$
Since synchronous speed $\omega_s$ is constant for a given motor, torque is directly proportional to air-gap power $P_g$. Expressing torque directly in "synchronous watts" saves engineers from repeatedly multiplying and dividing by $\frac{2\pi N_s}{60}$ in induction motor power flow and circle diagram calculations.

**Example**:
If a 4-pole, 50 Hz motor ($N_s = 1500\text{ rpm} \implies \omega_s = 157.08\text{ rad/s}$) has an air-gap power of $P_g = 5000\text{ W}$:
- Torque in synchronous watts $= \mathbf{5000\text{ sync watts}}$.
- Torque in conventional SI units $= \frac{5000}{157.08} = \mathbf{31.83\text{ N-m}}$.

---

#### Q8(b): Meaning of Vector Group and "Dyn5" Representation

#### What Vector Group Tells an Engineer:
1. **Primary Winding Connection**: Uppercase letter (D = Delta, Y = Star).
2. **Secondary Winding Connection**: Lowercase letter (d = Delta, y = Star).
3. **Neutral Conductor Availability**: Letter 'n' indicates neutral is brought out.
4. **Phase Displacement (Clock Position)**: An integer $0\text{–}11$ indicating the angular phase displacement of secondary line voltage relative to primary line voltage. Each clock hour represents $30°$ lagging (12 o'clock = 0°, 1 o'clock = 30° lag, 5 o'clock = 150° lag).

#### Physical Decoding of "Dyn5":
- **D**: Primary winding is connected in **Delta**.
- **y**: Secondary winding is connected in **Star**.
- **n**: Secondary **neutral** terminal is brought out externally for 4-wire supply.
- **5**: Secondary line voltage lags primary line voltage by $5 \times 30° = \mathbf{150°}$ (pointing to 5 o'clock on the phasor dial).

---

#### Q8(c): Induction Motor Circle Diagram Analysis

![Construction of Circle Diagram](../Books/diagrams/ch35_p06_fig35_09.jpg)

#### First-Principles Theory of the Circle Diagram:
As the mechanical load on an induction motor varies from no-load to standstill, the equivalent circuit impedance traces a circular locus in the complex current plane (Heyland circle).
- **Data Required**:
  1. No-Load Test ($V_0, I_0, \cos\phi_0$): Defines the origin $O'$ of the circle locus.
  2. Blocked-Rotor / SC Test scaled to rated voltage ($I_{sc}, \cos\phi_{sc}$): Defines the short-circuit point $S$.
  3. Stator Resistance $R_1$: Splits the vertical line representing standstill losses into stator copper loss and rotor copper loss.
- **Graphical Extraction at Rated Output (14.92 kW)**:
  - Vertical distance from the output line represents mechanical power output.
  - At the point corresponding to $14.92\text{ kW}$, reading the vector from origin $O$ to that operating point yields:
    - **Line Current $I_1$**: Length of the phasor vector $\approx 30\text{ A}$.
    - **Operating Power Factor $\cos\phi_1$**: Cosine of the angle between voltage axis and current phasor $\approx 0.76\text{ lagging}$.
    - **Slip $s$**: Ratio of vertical intercept of rotor Cu loss to air-gap power $\approx 5\%$.
    - **Efficiency $\eta$**: Ratio of output power to total input power $\approx 84\%$.
  - **Maximum Torque**: Maximum vertical distance from the circle circumference to the torque line.

---

*Source:* [PrevYearQuestions/2021.md](../PrevYearQuestions/2021.md)
*Writing guideline:* [writing_guideline.md](../.agents/rules/writing_style.md)
