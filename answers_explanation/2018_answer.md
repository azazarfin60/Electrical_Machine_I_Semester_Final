[← 2017 Answer](2017_answer.md) | [🏠 Index](README.md) | [2019 Answer →](2019_answer.md)

---

# ECE 2207: 2018 Semester Final: Explanation Style Answers
**RUET · ECE Dept · 2nd Year Odd Semester 2018**

> Deep tutorial-style explanations focusing on first-principles physics, "why over what", step-by-step logic, and practical engineering intuition.
> Core cross-cutting theory topics are detailed in [2018_2024_answer.md](2018_2024_answer.md).

---

## SECTION - A (Transformers: Q1 to Q4)

### Question 1

#### Q1(a): First-Principles Classification of Transformers

Transformers are categorized across multiple physical and functional axes:
1. **Voltage Transformation**:
   - *Step-up*: Secondary voltage exceeds primary ($N_2 > N_1$). Used at generating stations to minimize $I^2R$ transmission line losses.
   - *Step-down*: Secondary voltage is lower than primary ($N_2 < N_1$). Used at substations and distribution points for safe consumer utilization.
2. **Magnetic Core Geometry**:
   - *Core-Type*: Windings encircle the two vertical laminated iron limbs. Easy to insulate, preferred for high-voltage, high-power systems.
   - *Shell-Type*: Laminated core encircles and shelters the windings inside a central limb. Provides superior mechanical protection and lower leakage reactance, preferred for low-voltage, high-current applications.
3. **Number of Windings**:
   - *Two-Winding*: Electrically isolated primary and secondary coils coupled magnetically.
   - *Autotransformer*: Single continuous winding with a variable/fixed tap point; power is transferred partly conductively and partly inductively.
   - *Three-Winding (Tertiary)*: Adds a delta-connected third winding for zero-sequence harmonic suppression or substation auxiliary supply.
4. **Cooling Medium**:
   - *Dry-Type (Air-Cooled)*: Natural or forced air convection. Fire-safe, used inside hospitals, data centers, and commercial buildings.
   - *Oil-Immersed (ONAN, ONAF, OFAF)*: Immersed in mineral oil that provides both dielectric insulation and thermal convection to cooling radiators.
5. **System Application**:
   - *Power Transformer*: Sized for transmission grids (> 200 kVA); operated near 100% full-load capacity around the clock. Engineered for maximum efficiency at full load.
   - *Distribution Transformer*: Sized for end-users (< 200 kVA); energized 24/7 but loaded intermittently. Engineered for low iron loss and peak efficiency at 50–70% load.
   - *Instrument Transformers*: Current Transformers (CT) and Potential Transformers (PT) that step down high currents/voltages to standardized instrument levels (5 A, 110 V) with precise phase-angle fidelity.

---

#### Q1(b): Effect of Frequency and Flux Variations on a Transformer

#### 1. Effect of Frequency Variation (at Constant Applied Voltage $V_1$):
From the fundamental EMF relationship, $V_1 \approx E_1 = 4.44 f N_1 \Phi_m$:
$$\Phi_m \approx \frac{V_1}{4.44 f N_1} \implies B_m \propto \frac{1}{f}$$
- **If frequency increases ($f \uparrow$)**: Peak core flux density $B_m$ drops.
  - Hysteresis loss: $P_h \propto f B_m^{1.6} \propto f (f^{-1.6}) \propto f^{-0.6}$ (decreases).
  - Eddy current loss: $P_e \propto f^2 B_m^2 \propto f^2 (f^{-2}) = \text{constant}$.
  - Leakage reactance increases: $X_1 = 2\pi f L_1 \uparrow$, increasing internal voltage drops and worsening voltage regulation.
- **If frequency decreases ($f \downarrow$)**: Core flux density $B_m$ surges.
  - Operating a 50 Hz transformer at 25 Hz forces $B_m$ to double, driving the core deep into **magnetic saturation**.
  - Saturated iron causes the magnetizing current $I_m$ to explode to dangerous levels, severely overheating windings and inducing heavy 3rd harmonic waveform distortion.

#### 2. Effect of Flux Variation (Supply Voltage Fluctuations):
Since $\Phi_m \propto V_1$:
- Overvoltage forces flux density above the knee of the saturation curve ($B_m > 1.6\text{–}1.8\text{ T}$).
- Hysteresis loss spikes ($\propto V^{1.6}$) and eddy loss escalates ($\propto V^2$).
- Transformer cores are operated just below saturation at rated voltage. Sustained overvoltage causes intense core hum (magnetostriction) and thermal insulation degradation.

---

#### Q1(c): Exact Equivalent Circuit and Lagging Power Factor Vector Diagram

![Exact Equivalent Circuit of a Practical Transformer](diagrams/transformer_exact_equivalent_circuit.png)
![Complete Transformer Vector Diagram for Lagging Power Factor](diagrams/transformer_phasor_lagging_pf.png)

#### Phasor Evolution for Lagging Load:
1. Horizontal reference phasor is mutual core flux $\vec{\Phi}$.
2. Both induced EMFs $\vec{E}_1, \vec{E}_2$ lag $\vec{\Phi}$ by 90° (pointing vertically downward).
3. Secondary terminal voltage $\vec{V}_2$ leads secondary current $\vec{I}_2$ by load angle $\phi_2$. By KVL: $\vec{E}_2 = \vec{V}_2 + \vec{I}_2 R_2 + j \vec{I}_2 X_2$. Adding the resistive drop parallel to $\vec{I}_2$ and inductive drop perpendicular to $\vec{I}_2$ closes the triangle at $\vec{E}_2$.
4. Primary applied voltage counterbalances back-EMF ($-\vec{E}_1$, pointing vertically upward) plus primary impedance drops: $\vec{V}_1 = -\vec{E}_1 + \vec{I}_1 R_1 + j \vec{I}_1 X_1$.
5. Primary current $\vec{I}_1$ is the vector sum of excitation current $\vec{I}_0$ and reflected load current $\vec{I}_2' = -K \vec{I}_2$.

---

#### Q1(d): SC Test Analysis and Parameter Extraction

In short-circuit test calculations, series impedance parameters are extracted:
- Total series impedance: $Z_{01} = \frac{V_{sc}}{I_{sc}}$
- Total series resistance: $R_{01} = \frac{W_{sc}}{I_{sc}^2}$
- Total leakage reactance: $X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$
- Voltage Regulation at power factor $\cos\phi$:
  $$\text{VR\%} = \frac{I_1 (R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100\%$$

*(Note on 2018 Paper Data: The numerical values stated on the original 11kV question sheet contain a typographical mismatch where $W_{sc}/I_{sc}^2 > V_{sc}/I_{sc}$, which is physically impossible. Solving with the standard corrected 20 kVA benchmark yields $Z_{01} = 8.64\,\Omega, R_{01} = 3.96\,\Omega, X_{01} = 7.68\,\Omega$, and full-load voltage regulation of $\mathbf{2.70\%}$ at 0.8 lagging pf).*

---

### Question 2

#### Q2(a): Definition and Significance of All-Day Efficiency

> See full background in [T-03: Efficiency and All-Day Efficiency](2018_2024_answer.md#t-03-efficiency-and-all-day-efficiency).

All-day efficiency (or operational energy efficiency) is defined as:
$$\eta_{\text{all-day}} = \frac{\text{Total Energy Output in 24 Hours (kWh)}}{\text{Total Energy Input in 24 Hours (kWh)}} \times 100\%$$
Because iron loss occurs 24 hours a day while copper loss depends on the square of instantaneous load current ($x^2$), this metric dictates the design of distribution transformers, ensuring iron loss is minimized even if full-load copper loss is slightly higher.

---

#### Q2(b): 10 kVA Transformer Efficiency at Half and Full Load

#### Given Data:
- Rating $S = 10\text{ kVA} = 10{,}000\text{ VA}$
- Core loss $P_{Fe} = 200\text{ W}$ (from OC test, constant)
- Full-load copper loss $P_{Cu,FL} = 300\text{ W}$ (from SC test)

#### 1. Full-Load Performance ($x = 1.0$):
- **At Unity Power Factor ($\cos\phi = 1.0$)**:
  $$P_{\text{out}} = 10{,}000 \times 1.0 = 10{,}000\text{ W}$$
  $$P_{\text{loss}} = 200 + 300 = 500\text{ W} \implies \eta = \frac{10{,}000}{10{,}500} \times 100\% = \mathbf{95.24\%}$$
- **At 0.8 Lagging Power Factor ($\cos\phi = 0.8$)**:
  $$P_{\text{out}} = 10{,}000 \times 0.8 = 8{,}000\text{ W}$$
  $$P_{\text{loss}} = 500\text{ W} \implies \eta = \frac{8{,}000}{8{,}500} \times 100\% = \mathbf{94.12\%}$$

#### 2. Half-Load Performance ($x = 0.5$):
- Half-load copper loss: $P_{Cu} = x^2 P_{Cu,FL} = (0.5)^2 \times 300 = 0.25 \times 300 = 75\text{ W}$.
- Total losses at half-load: $P_{\text{loss}} = 200 + 75 = 275\text{ W}$.
- **At Unity Power Factor**:
  $$P_{\text{out}} = 0.5 \times 10{,}000 \times 1.0 = 5{,}000\text{ W} \implies \eta = \frac{5{,}000}{5{,}275} \times 100\% = \mathbf{94.79\%}$$
- **At 0.8 Lagging Power Factor**:
  $$P_{\text{out}} = 0.5 \times 10{,}000 \times 0.8 = 4{,}000\text{ W} \implies \eta = \frac{4{,}000}{4{,}275} \times 100\% = \mathbf{93.57\%}$$

---

#### Q2(c): 100 kVA Transformer All-Day Efficiency With 5-Step Load Profile

#### Given Data:
- Rating $S = 100\text{ kVA}$, Iron loss $P_{Fe} = 200\text{ W} = 0.20\text{ kW}$, Full-load copper loss $P_{Cu,FL} = 500\text{ W} = 0.50\text{ kW}$
- 24-Hour Load Cycle:
  1. 2 hours at $5/4$ load ($x = 1.25$): $P_{\text{out}} = 1.25 \times 100 = 125\text{ kW}$
  2. 6 hours at full load ($x = 1.0$): $P_{\text{out}} = 100\text{ kW}$
  3. 8 hours at half load ($x = 0.5$): $P_{\text{out}} = 50\text{ kW}$
  4. 4 hours at quarter load ($x = 0.25$): $P_{\text{out}} = 25\text{ kW}$
  5. 4 hours at no load ($x = 0$): $P_{\text{out}} = 0\text{ kW}$

#### Step-by-Step Energy Balance:
1. **Total Output Energy ($W_{\text{out}}$)**:
   $$W_{\text{out}} = (125 \times 2) + (100 \times 6) + (50 \times 8) + (25 \times 4) + 0 = 250 + 600 + 400 + 100 = \mathbf{1350\text{ kWh}}$$
2. **Total Iron Loss Energy (Continuous 24 Hours)**:
   $$W_{Fe} = 0.20\text{ kW} \times 24\text{ h} = \mathbf{4.80\text{ kWh}}$$
3. **Total Copper Loss Energy ($W_{Cu} = \sum x_i^2 P_{Cu,FL} t_i$)**:
   - Step 1: $(1.25)^2 \times 0.50\text{ kW} \times 2\text{ h} = 1.5625 \times 0.50 \times 2 = 1.5625\text{ kWh}$
   - Step 2: $(1.0)^2 \times 0.50\text{ kW} \times 6\text{ h} = 3.0000\text{ kWh}$
   - Step 3: $(0.5)^2 \times 0.50\text{ kW} \times 8\text{ h} = 0.25 \times 0.50 \times 8 = 1.0000\text{ kWh}$
   - Step 4: $(0.25)^2 \times 0.50\text{ kW} \times 4\text{ h} = 0.0625 \times 0.50 \times 4 = 0.1250\text{ kWh}$
   - Step 5: $0\text{ kWh}$
   $$W_{Cu} = 1.5625 + 3.0000 + 1.0000 + 0.1250 = \mathbf{5.6875\text{ kWh}}$$
4. **All-Day Efficiency**:
   $$W_{\text{loss}} = W_{Fe} + W_{Cu} = 4.80 + 5.6875 = 10.4875\text{ kWh}$$
   $$W_{\text{in}} = 1350 + 10.4875 = 1360.4875\text{ kWh}$$
   $$\eta_{\text{all-day}} = \frac{1350}{1360.4875} \times 100\% = \mathbf{99.23\%}$$

---

### Question 3

#### Q3(a): Four-Wire Delta-Connected Secondary (High-Leg Delta)

In distribution systems serving both heavy 3-phase power loads and single-phase domestic loads, three single-phase transformers have their secondaries connected in delta ($\Delta$), and the center-tap of **one** phase winding is grounded to provide a 4th neutral wire:
- **Two 120 V Lighting Legs**: The two lines adjacent to the center-tapped winding provide standard 120 V line-to-neutral single-phase power for ordinary appliances.
- **Three-Phase Power**: Line-to-line voltage across all three main phases remains 240 V 3-phase for industrial motor drives.
- **The "High-Leg" Warning**: The third line (opposite the center tap) has a line-to-neutral voltage of $\frac{\sqrt{3}}{2} \times 240 = 208\text{ V}$. It is color-coded orange ("wild leg") and must never be connected to standard 120 V single-phase branch circuits.

---

#### Q3(b): 10 MVA, 11kV/230V 3-Phase Bank Parameter Breakdown

#### Given Data:
- Total bank capacity: $S_{\text{total}} = 10\text{ MVA} = 10{,}000\text{ kVA}$
- Primary: Star-connected, Line voltage $V_{1,L} = 11{,}000\text{ V}$
- Secondary: Delta-connected, Line voltage $V_{2,L} = 230\text{ V}$

#### 1. Rating Per Transformer:
$$S_{\text{each}} = \frac{S_{\text{total}}}{3} = \frac{10{,}000}{3} = \mathbf{3333.3\text{ kVA} \approx 3.33\text{ MVA}}$$

#### 2. Primary Side (Star Connection):
- Voltage per primary coil (phase voltage):
  $$V_{1,\text{coil}} = \frac{V_{1,L}}{\sqrt{3}} = \frac{11{,}000}{\sqrt{3}} = \mathbf{6350.85\text{ V} \approx 6351\text{ V}}$$
- Current per primary coil:
  $$I_{1,\text{coil}} = \frac{S_{\text{each}}}{V_{1,\text{coil}}} = \frac{3{,}333{,}333\text{ VA}}{6350.85\text{ V}} = \mathbf{524.86\text{ A}}$$

#### 3. Secondary Side (Delta Connection):
- Voltage per secondary coil:
  $$V_{2,\text{coil}} = V_{2,L} = \mathbf{230\text{ V}}$$
- Current per secondary coil (phase current):
  $$I_{2,\text{coil}} = \frac{S_{\text{each}}}{V_{2,\text{coil}}} = \frac{3{,}333{,}333\text{ VA}}{230\text{ V}} = \mathbf{14{,}492.75\text{ A}}$$
  *(Secondary external line current is $I_{2,L} = \sqrt{3} \times 14{,}492.75 = 25{,}095\text{ A}$)*.

---

#### Q3(c): Open-Delta (V-V) Capacity Proof

> See detailed proof and vector diagram in [T-04: Open-Delta Connection: Why 57.7% and When to Use It](2018_2024_answer.md#t-04-open-delta-connection-why-577-and-when-to-use-it).

- Closed delta bank of 3 single-phase units: $S_{\Delta} = 3 V I$.
- Open delta bank with 2 units: $S_{V} = \sqrt{3} V I$.
- Capacity ratio:
  $$\frac{S_{V}}{S_{\Delta}} = \frac{\sqrt{3} V I}{3 V I} = \frac{1}{\sqrt{3}} = \mathbf{0.577 = 57.7\%}$$

---

### Question 4

#### Q4(a): Scott (T-T) Connection for 3-Phase to 2-Phase Transformation

![Scott Connection Wiring Diagram](../Books/diagrams/VK_Mehta_Fig_7_53.jpeg)

- **Main Transformer**: Primary connected between lines A and B ($V_{AB}$), center-tapped at $D$.
- **Teaser Transformer**: Primary connected between line C and center-tap $D$. Its turns are tapped at $\frac{\sqrt{3}}{2} \approx 86.6\%$ of the main transformer turns.
- **Physical Reason for 86.6%**: The line-to-midpoint voltage in an equilateral voltage triangle is $V_{CD} = \frac{\sqrt{3}}{2} V_{AB}$. Tapping at 86.6% turns ensures that the induced volts-per-turn in both transformers are strictly identical.
- **Output**: Because $\vec{V}_{CD}$ is perpendicular to $\vec{V}_{AB}$, the secondary windings produce two equal voltages displaced by 90° in time, supplying a perfectly balanced 2-phase load.

---

#### Q4(b): Numerical Scott Connection (3300V to 440V, 33 kVA Load)

#### Given Data:
- 3-Phase Line Voltage: $V_{1,L} = 3300\text{ V}$
- 2-Phase Load: $S_{\text{load}} = 33\text{ kVA}, V_2 = 440\text{ V}$ balanced across two phases.

#### 1. Secondary Quantities:
- Apparent power per phase: $S_2 = \frac{33{,}000}{2} = 16{,}500\text{ VA}$
- Secondary voltage per phase: $V_{2,\text{main}} = V_{2,\text{teaser}} = \mathbf{440\text{ V}}$
- Secondary current per phase:
  $$I_{2,\text{main}} = I_{2,\text{teaser}} = \frac{16{,}500}{440} = \mathbf{37.50\text{ A}}$$

#### 2. Primary Quantities:
- **Main Transformer Primary**:
  - Voltage: $V_{1,\text{main}} = V_{AB} = \mathbf{3300\text{ V}}$
  - Current: $I_{1,\text{main}} = \frac{16{,}500}{3300} = \mathbf{5.00\text{ A}}$
  - kVA Rating: $3300\text{ V} \times 5\text{ A} = \mathbf{16.50\text{ kVA}}$
- **Teaser Transformer Primary**:
  - Voltage: $V_{1,\text{teaser}} = \frac{\sqrt{3}}{2} \times 3300 = 0.8660 \times 3300 = \mathbf{2857.9\text{ V} \approx 2858\text{ V}}$
  - Current: Line current from phase C is $I_C = \frac{16{,}500}{2858} = \mathbf{5.77\text{ A}}$
  - kVA Rating: $2858\text{ V} \times 5.77\text{ A} = \mathbf{16.50\text{ kVA}}$

---

#### Q4(c): Transformer Banks and Voltage Ratios for 10:1 Turns Ratio

- **Advantages of 3-Phase Transformer Banks**:
  1. *Reliability and Service Continuity*: If one unit burns out, the remaining two maintain 3-phase service via open-delta (57.7% capacity).
  2. *Modularity and Transport*: Three smaller single-phase units are drastically easier to transport into remote mountainous or underground substations than one massive 3-phase tank.
  3. *Spare Strategy*: Only one single-phase spare unit needs to be stocked rather than an entire 3-phase spare transformer.
- **Line Voltage Ratios ($N_1 : N_2 = 10 : 1$ per phase)**:
  - **Y-Y**: $\frac{V_{1,L}}{V_{2,L}} = \frac{\sqrt{3} V_{1,\phi}}{\sqrt{3} V_{2,\phi}} = \frac{N_1}{N_2} = \mathbf{10 : 1}$
  - **Δ-Δ**: $\frac{V_{1,L}}{V_{2,L}} = \frac{V_{1,\phi}}{V_{2,\phi}} = \frac{N_1}{N_2} = \mathbf{10 : 1}$
  - **Δ-Y**: $\frac{V_{1,L}}{V_{2,L}} = \frac{V_{1,\phi}}{\sqrt{3} V_{2,\phi}} = \frac{10}{\sqrt{3}} : 1 = \mathbf{5.77 : 1}$ (voltage stepped up on secondary)
  - **Y-Δ**: $\frac{V_{1,L}}{V_{2,L}} = \frac{\sqrt{3} V_{1,\phi}}{V_{2,\phi}} = 10\sqrt{3} : 1 = \mathbf{17.32 : 1}$ (voltage stepped down further)

---

## SECTION - B (Induction Motors: Q5 to Q8)

### Question 5

#### Q5(a): Electrical Braking Techniques in Induction Motors

1. **Regenerative Braking**: Occurs when an external mechanical load drives the motor shaft faster than synchronous speed ($N > N_s$). Slip becomes negative ($s < 0$), reversing the direction of electromagnetic torque. The machine operates as an induction generator, feeding kinetic energy back into the power lines as electrical power. Highly efficient, used on downhill electric train runs and elevator descents.
2. **Dynamic (DC Rheostatic) Braking**: The stator is disconnected from the 3-phase AC supply and immediately connected to a DC excitation voltage. The DC current sets up a stationary, non-rotating magnetic field in the air gap. As the rotor continues to spin, its conductors cut this stationary field, inducing heavy currents that dissipate rotational kinetic energy as heat in external rotor resistors, bringing the motor smoothly to rest.
3. **Plugging (Counter-Current Braking)**: Two stator power leads are swapped while running, abruptly reversing the rotation of the stator RMF. Slip spikes to $s = 2 - s_f > 1$. The motor develops massive reverse torque opposing shaft rotation. To avoid accelerating in the reverse direction, a centrifugal zero-speed switch cuts power the moment speed reaches zero.

---

#### Q5(b): Air-Gap Power Proof: $P_m = (1-s)P_2$

> See full derivation and tree diagram in [IM-01: Air-Gap Power Ratios](2018_2024_answer.md#im-01-air-gap-power-ratios-p_g--p_rcu--p_m--1--s--1-s).

- Total air-gap power transferred into rotor: $P_2 = 3 I_2^2 \frac{R_2}{s}$.
- Rotor copper loss: $P_{r,Cu} = 3 I_2^2 R_2 = s P_2$.
- Mechanical power developed internally:
  $$P_m = P_2 - P_{r,Cu} = P_2 - s P_2 = \mathbf{(1-s)P_2}$$
- Rotor efficiency: $\eta_{\text{rotor}} = \frac{P_m}{P_2} = \mathbf{1 - s}$.

---

#### Q5(c): Self-Excited Induction Generator (Capacitance and Engine Speed)

![Self-excited induction generator circuit with terminal capacitors](../Books/diagrams/Ch-34_p34_fig31.jpg)
![Induction generator torque-slip curve in generating region (slip < 0)](../Books/diagrams/Ch-34_p33_fig30.jpg)

#### Given Data:
- Rating: $440\text{ V}, 4\text{-Pole}, 50\text{ Hz}, 30\text{ kW}, I_L = 40\text{ A}, \cos\phi = 0.85$
- Motoring speed: $N = 1470\text{ rpm}$
- Synchronous speed: $N_s = \frac{120 \times 50}{4} = 1500\text{ rpm}$

#### 1. Terminal Capacitance Per Phase (Delta Connected):
An induction generator cannot self-excite without external reactive VARs to build and sustain air-gap flux:
- Reactive power required:
  $$\sin\phi = \sqrt{1 - (0.85)^2} = 0.5268$$
  $$Q = \sqrt{3} V_L I_L \sin\phi = \sqrt{3} \times 440 \times 40 \times 0.5268 = 16{,}060\text{ VAR}$$
- Per-phase VAR for Delta capacitors:
  $$Q_\phi = \frac{Q}{3} = \frac{16{,}060}{3} = 5353.3\text{ VAR}$$
- Capacitive reactance per phase ($V_\phi = V_L = 440\text{ V}$):
  $$X_C = \frac{V_L^2}{Q_\phi} = \frac{440^2}{5353.3} = \frac{193{,}600}{5353.3} = 36.16\,\Omega$$
- Capacitance:
  $$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 36.16} = \mathbf{88.0\,\mu\text{F per phase}}$$

#### 2. Engine Speed for 50 Hz Output:
- Motor slip: $s_m = \frac{1500 - 1470}{1500} = 0.02$.
- In generating mode, slip is negative: $s_{\text{gen}} = -0.02$.
- The driving engine must rotate the rotor above synchronous speed:
  $$N_{\text{engine}} = N_s (1 - s_{\text{gen}}) = 1500 \times (1 - (-0.02)) = 1500 \times 1.02 = \mathbf{1530\text{ rpm}}$$

---

### Question 6

#### Q6(a): Single-Phasing in 3-Phase Induction Motors

![Single-phasing delta motor](../Books/diagrams/ch35_p53_fig35_58.jpg)

- **What Happens at Standstill (Attempting to Start)**:
  If one supply line is broken before starting, the motor receives only single-phase power. It develops zero starting torque ($T_{st} = 0$). The motor will not rotate, drawing extreme locked-rotor current and humming loudly until thermal fuses blow.
- **What Happens While Running**:
  If one line opens while running, the motor continues to spin due to rotational momentum, but the magnetic field collapses into an unbalanced pulsating field.
  - Current in the remaining two active lines increases by $\approx \sqrt{3} \times I_{\text{rated}} \approx 173\%$.
  - Rotor slip increases, causing rotor speed to dip.
  - The healthy phase windings overheat rapidly; without negative-sequence or thermal overload protection, the stator windings will burn out within minutes.

---

#### Q6(b): Proof: Resultant Flux of 3-Phase Induction Motor is Constant ($1.5\Phi_m$)

![Resultant 3-phase flux](../Books/diagrams/Ch-34_p10_fig14.jpg)

$$\Phi_R = \Phi_m \sin\omega t, \quad \Phi_Y = \Phi_m \sin(\omega t - 120°), \quad \Phi_B = \Phi_m \sin(\omega t + 120°)$$
Resolving along orthogonal spatial axes:
$$\Phi_x = \frac{3}{2}\Phi_m \sin\omega t, \qquad \Phi_y = -\frac{3}{2}\Phi_m \cos\omega t$$
$$\Phi_r = \sqrt{\Phi_x^2 + \Phi_y^2} = \frac{3}{2}\Phi_m \sqrt{\sin^2\omega t + \cos^2\omega t} = \mathbf{1.5\Phi_m = \text{constant}}$$

---

#### Q6(c): 6-Pole, 240V IM Numerical Calculation

#### Given Data:
- Poles $P = 6, f = 50\text{ Hz} \implies N_s = 1000\text{ rpm}, \omega_s = 104.72\text{ rad/s}$
- Star connection: $V_{1,\phi} = \frac{240}{\sqrt{3}} = 138.56\text{ V}$
- Turns ratio $N_1/N_2 = 1.8 \implies E_2 = \frac{138.56}{1.8} = 76.98\text{ V/phase}$
- Rotor parameters: $R_2 = 0.12\,\Omega, X_2 = 0.85\,\Omega$, full-load slip $s_f = 0.04$.

#### 1. Full-Load Developed Torque:
$$k = \frac{3}{\omega_s} = \frac{3}{104.72} = 0.028648\text{ N-m}\cdot\text{s/W}$$
$$T_{FL} = \frac{k s_f E_2^2 R_2}{R_2^2 + s_f^2 X_2^2} = \frac{0.028648 \times 0.04 \times (76.98)^2 \times 0.12}{(0.12)^2 + (0.04 \times 0.85)^2} = \frac{0.8146}{0.0144 + 0.001156} = \frac{0.8146}{0.01556} = \mathbf{52.35\text{ N-m}}$$

#### 2. Maximum Torque:
$$T_{\max} = \frac{k E_2^2}{2 X_2} = \frac{0.028648 \times 5925.9}{2 \times 0.85} = \frac{169.76}{1.70} = \mathbf{99.86\text{ N-m}}$$

#### 3. Speed at Maximum Torque:
$$s_{mT} = \frac{R_2}{X_2} = \frac{0.12}{0.85} = 0.1412 \implies N_{mT} = 1000 \times (1 - 0.1412) = \mathbf{858.8\text{ rpm}}$$

---

### Question 7

#### Q7(a): Star-Delta Starter Operation and Trade-Offs

![Star-delta starter connections](../Books/diagrams/ch35_p23_fig35_21.jpg)

- **Mechanism**:
  - *Starting (Star)*: Phase voltage is reduced to $V_\phi = \frac{V_L}{\sqrt{3}}$. Line starting current is reduced to $I_{st,\text{star}} = \frac{1}{3} I_{st,\text{delta}}$, and starting torque drops to $T_{st,\text{star}} = \frac{1}{3} T_{st,\text{delta}}$.
  - *Running (Delta)*: Once the motor reaches ~80% speed, a timer or centrifugal switch snaps the contacts to Delta, restoring full rated line voltage across each phase winding.
- **Limitation**: The $67\%$ reduction in starting torque makes it unsuitable for high-inertia or heavy loaded starting (e.g., loaded crushers, positive displacement pumps).

---

#### Q7(b): Circle Diagram Graphical Analysis (5.6 kW Slip-Ring IM)

![Construction of Circle Diagram](../Books/diagrams/ch35_p06_fig35_09.jpg)

- **Scaled SC Current at Rated 400 V**: $I_{sc} = 12 \times \frac{400}{100} = 48\text{ A}$.
- **Loss Separation**: Stator copper loss is calculated from measured $R_1$, dividing the vertical short-circuit line into stator Cu loss and rotor Cu loss segments.
- **Reading at Rated Output (5.6 kW)**:
  - Full-load line current $\approx \mathbf{10.5\text{ A}}$
  - Full-load operating slip $\approx \mathbf{6.2\%}$
  - Full-load power factor $\approx \mathbf{0.78\text{ lagging}}$
  - Maximum mechanical power output $\approx \mathbf{8.2\text{ kW}}$

---

### Question 8

#### Q8(a): Double-Field Revolving Theory of Single-Phase IM

> See comprehensive derivation in [IM-03: Single-Phase Induction Motor: Double Revolving Field Theory](2018_2024_answer.md#im-03-single-phase-induction-motor-double-revolving-field-theory).

- Forward field $\Phi_f = \Phi_m/2$ at $+N_s$ with slip $s_f = s$.
- Backward field $\Phi_b = \Phi_m/2$ at $-N_s$ with slip $s_b = 2 - s$.
- At standstill ($s = 1$), torques cancel exactly ($T_f = T_b \implies T_{\text{net}} = 0$).

---

#### Q8(b): Resistor Split-Phase Motor Starting Condition

![Split-Phase Induction Motor Circuit and Phasor Diagram](../Books/diagrams/VK_Mehta_Fig_9_13.jpeg)

In a resistance split-phase motor, the auxiliary winding is wound with finer wire (high resistance, low reactance), while the main winding has thick wire (low resistance, high reactance).
- For maximum starting torque, the two currents must be in temporal quadrature ($\phi_m - \phi_a = 90°$).
- Matching the winding impedance angles and effective turns ratio ($N_a/N_m$) yields the optimum auxiliary resistance design formula:
  $$\boxed{r_a = \left(\frac{N_a}{N_m}\right)^2 (r_m + z_m)}$$

---

#### Q8(c): Capacitor Calculation for Maximum Starting Torque

#### Given Data:
- Main winding: $V = 100\text{ V}, I = 2\text{ A}, P = 40\text{ W} \implies Z_m = \frac{100}{2} = 50\,\Omega, R_m = \frac{40}{2^2} = 10\,\Omega, X_m = \sqrt{50^2 - 10^2} = 48.99\,\Omega$
  $$\phi_m = \cos^{-1}\left(\frac{10}{50}\right) = 78.46°\text{ lagging}$$
- Auxiliary winding: $V = 80\text{ V}, I = 1\text{ A}, P = 50\text{ W} \implies Z_a = 80\,\Omega, R_a = \frac{50}{1^2} = 50\,\Omega, X_a = \sqrt{80^2 - 50^2} = 62.45\,\Omega$

#### Condition for 90° Quadrature:
For auxiliary current to lead main current by 90°, it must lead the supply voltage by:
$$\phi_a = 90° - 78.46° = 11.54°\text{ leading}$$
$$\tan(11.54°) = \frac{X_C - X_a}{R_a} = \frac{X_C - 62.45}{50} = 0.20416$$
$$X_C - 62.45 = 50 \times 0.20416 = 10.21\,\Omega$$
$$X_C = 62.45 + 10.21 = \mathbf{72.66\,\Omega}$$
$$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 72.66} = \frac{1}{22{,}826.9} = \mathbf{43.8\,\mu\text{F}}$$

---

*Source:* [PrevYearQuestions/2018.md](../PrevYearQuestions/2018.md)

---

[← 2017 Answer](2017_answer.md) | [🏠 Index](README.md) | [2019 Answer →](2019_answer.md)
