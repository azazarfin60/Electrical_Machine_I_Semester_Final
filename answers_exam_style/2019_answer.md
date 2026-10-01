[← 2018 Answer](2018_answer.md) | [🏠 Index](README.md) | [2020 Answer →](2020_answer.md)

---

# ECE 2207: 2019 Semester Final: Exam Style Answers
**RUET · ECE Dept · 2nd Year Odd Semester 2019**
**Full Marks:** 72 · **Time:** 3 Hours · **Attempt any 6 (3 from each section)**

---

## SECTION - A (Transformers: Q1 to Q4)

### Question 1

**(a) Define transformer. How is energy transferred from primary to secondary? Distinguish primary and secondary windings. [04]**

**Transformer:** A static electromagnetic device that transfers electrical energy between two or more circuits through mutual electromagnetic induction, at the same frequency but different voltage and current levels.

**Energy transfer mechanism:** AC voltage applied to the primary winding drives a current that creates an alternating magnetic flux in the iron core. By Faraday's Law, this alternating flux induces an EMF in the secondary winding. If a load is connected, current flows and energy is delivered to the load.

| Feature | Primary Winding | Secondary Winding |
|:---|:---|:---|
| Connection | Connected to AC supply | Connected to load |
| Role | Receives electrical energy | Delivers electrical energy |
| Voltage | Usually higher (step-down) or lower (step-up) | Determined by turns ratio |
| Symbol | $V_1$, $I_1$, $N_1$ | $V_2$, $I_2$, $N_2$ |

---

**(b) Derive the expression for EMF induced in a transformer winding. Show EMF per turn is same in both. [04]**

Let core flux: $\Phi(t) = \Phi_m\sin\omega t$

By Faraday's Law, primary induced EMF:
$$e_1 = -N_1\frac{d\Phi}{dt} = -N_1\omega\Phi_m\cos\omega t = N_1\omega\Phi_m\sin(\omega t - 90°)$$

Peak value: $E_{m1} = N_1\omega\Phi_m = 2\pi f N_1\Phi_m$

RMS: $\boxed{E_1 = 4.44 f N_1\Phi_m}$

Similarly: $\boxed{E_2 = 4.44 f N_2\Phi_m}$

**EMF per turn:**
$$\frac{E_1}{N_1} = 4.44 f\Phi_m = \frac{E_2}{N_2}$$

EMF per turn is $4.44f\Phi_m$ for both windings. Same for primary and secondary. *(Proved)*

---

**(c) Why does current flow in primary when secondary is open? Explain how primary current increases as secondary load increases. [04]**

**Why current flows at no-load:**
When $V_1$ is applied, the primary winding behaves as a coil with resistance $R_1$ and inductance $L_1$. To set up the alternating core flux $\Phi_m$ (which induces $E_1 \approx V_1$ to balance applied voltage), a small magnetizing current $I_m$ must flow. Also, a small active component $I_c$ flows to supply core losses (hysteresis + eddy). Together:
$$I_0 = \sqrt{I_c^2 + I_m^2} \approx 2\text{-10\%\ of rated current}$$

**How primary current increases with secondary load:**
When a load is connected and secondary current $I_2$ flows, it creates a demagnetizing MMF $= N_2 I_2$. This tends to reduce the core flux. But $E_1 \approx V_1$ (supply voltage is fixed), so the flux must stay essentially constant. To maintain the flux, the primary must draw additional current $I_2' = I_2 \times N_2/N_1$. Total primary current:
$$I_1 = I_0 + I_2' = I_0 + \frac{N_2}{N_1}I_2$$

As load current $I_2$ increases, $I_1$ increases proportionally.

---

### Question 2

**(a) Discuss OC and SC tests of a single-phase transformer. [03]**

**Open-Circuit (OC) test:**
- Performed on the low-voltage (LV) side with the high-voltage (HV) side open.
- Rated voltage is applied to the LV side.
- Voltmeter ($V_0$), ammeter ($I_0$), wattmeter ($W_0$) readings are taken.
- All power input $W_0$ = core (iron) loss, since winding current is very small.
- Determines: core loss $P_{Fe} = W_0$, magnetizing reactance $X_m$, core loss resistance $R_c$.
- Core loss is constant for all loads.

**Short-Circuit (SC) test:**
- Performed on the HV side with the LV side short-circuited.
- Reduced voltage applied until rated current flows.
- Voltmeter ($V_{sc}$), ammeter ($I_{sc}$), wattmeter ($W_{sc}$) readings are taken.
- Core losses are negligible at low voltage. $W_{sc}$ = full-load copper loss.
- Determines: equivalent resistance $R_{01}$, equivalent reactance $X_{01}$, leakage impedance $Z_{01}$.

---

**(b) Define voltage regulation. Find VR for unity, lagging, and leading pf. [04]**

**Voltage regulation (VR):** The change in secondary terminal voltage from no-load to full-load as a percentage of rated full-load voltage, with primary voltage held constant.

$$\text{VR\%} = \frac{V_{2,NL} - V_{2,FL}}{V_{2,FL}} \times 100\%$$

Using the approximate formula (per-unit or percentage):

**Unity pf ($\cos\phi = 1$, $\sin\phi = 0$):**
$$\text{VR\%} \approx \epsilon_r = \frac{I_2(R_{01}\cos\phi + X_{01}\sin\phi)}{V_2} \times 100 = \frac{I_2 R_{01}}{V_2} \times 100$$

**Lagging pf ($\cos\phi$ lag):**
$$\text{VR\%} = \frac{I_2(R_{01}\cos\phi + X_{01}\sin\phi)}{V_2} \times 100 \quad \text{(positive, larger than unity pf)}$$

**Leading pf ($\cos\phi$ lead):**
$$\text{VR\%} = \frac{I_2(R_{01}\cos\phi - X_{01}\sin\phi)}{V_2} \times 100 \quad \text{(can be negative: voltage rises with leading load)}$$

---

**(c) 10 kVA, 2200/220V, 60 Hz. OC (high side open): 220V, 1.5A, 153W. SC (low side shorted): 115V, rated I, 224W. Find half-load and full-load efficiencies at upf and 0.8 pf lag. [05]**

**Core loss:** $P_{Fe} = 153$ W

**Rated current (primary, HV side):** $I_1 = 10000/2200 = 4.545$ A

**Full-load Cu loss:** $P_{Cu,FL} = 224$ W

**Full load efficiency:**

At upf: $\eta = \frac{10000}{10000 + 153 + 224} = \frac{10000}{10377} = \boxed{96.37\%}$

At 0.8 pf: $\eta = \frac{8000}{8000 + 153 + 224} = \frac{8000}{8377} = \boxed{95.50\%}$

**Half-load efficiency:** Cu loss $= (0.5)^2 \times 224 = 56$ W

At upf: $\eta = \frac{5000}{5000 + 153 + 56} = \frac{5000}{5209} = \boxed{95.99\%}$

At 0.8 pf: $\eta = \frac{4000}{4000 + 153 + 56} = \frac{4000}{4209} = \boxed{95.03\%}$

---

### Question 3

**(a) What is transformer breathing? Show max efficiency when core loss = copper loss. [04]**

**Transformer breathing:** As the transformer load varies, its temperature changes. Cooling oil expands when hot and contracts when cool. In conservator-type transformers, oil level rises and falls in the conservator tank. Air is drawn in and expelled through a silica gel breather (to remove moisture). This process of inhaling/exhaling air is called transformer breathing. Moisture absorption by the insulating oil degrades it over time, which is why the breather desiccant must be regularly replaced.

**Max efficiency proof:**

Efficiency:
$$\eta = \frac{x \cdot S \cdot \cos\phi}{x \cdot S \cdot \cos\phi + P_{Fe} + x^2 P_{Cu,FL}}$$

where $x$ = fraction of full load. Differentiate w.r.t. $x$ and set to zero:

$$\frac{d\eta}{dx} = 0 \implies x^2 P_{Cu,FL} = P_{Fe}$$

$$\boxed{\text{Cu loss} = \text{Fe (core) loss}} \quad \text{at maximum efficiency}$$

The load fraction at max efficiency: $x = \sqrt{P_{Fe}/P_{Cu,FL}}$

---

**(b) "A considerable economy is achieved in core material if the middle phase winding of a 3-phase shell-type transformer is wound in the reverse direction." Justify. [04]**

In a 3-phase shell-type transformer, three single-phase cores are placed side by side. The flux in the middle limb is the vector sum of the fluxes from the two outer limbs.

For a balanced 3-phase system: $\Phi_A + \Phi_B + \Phi_C = 0$ at every instant.

If the middle phase (B) is wound in the **same** direction as A and C: the middle yoke carries the flux from both A and C passing through it. The cross-section must be larger.

If the middle phase (B) is wound in the **reverse** direction: effectively $\Phi_B$ is now $-\Phi_B$, which equals $\Phi_A + \Phi_C$. The flux in the middle limb equals the sum of A and C (with appropriate sign), meaning the yoke cross-section can be reduced because the net flux sharing is more symmetric and the yokes carry only the flux from adjacent limbs.

**Economy:** The two outer yokes carry only the flux from one outer phase each. Only the middle limb must carry the combined flux. With reverse winding, the mutual cancellation reduces peak yoke flux. Less core material is needed for the same performance.

---

**(c) Yd11 in parallel with Dy1: possible? [04]**

**Vector group numbers:** Each unit represents a 30° phase shift (clock notation: 12 = 0°, 11 = 330° = −30°, 1 = 30°).

- Yd11: Phase displacement = 11 × 30° = 330° (= −30°): secondary lags primary by 30°.
- Dy1: Phase displacement = 1 × 30° = 30°: secondary leads primary by 30°.

The difference in secondary voltage phase angles: $330° - 30° = 300°$ (or equivalently $60°$ lag). This is a 60° phase displacement between their secondary voltages.

Two transformers can only be paralleled if their secondary voltages are exactly in phase (same vector group number). A 60° difference means a large circulating current would flow even at no load.

**Direct parallel: not possible** due to the 60° phase displacement.

**Possible workaround:** Yes, it is possible if a phase-shifting transformer or external connection rearrangement shifts one transformer's output by 60° to match the other. In practice, rearranging the external secondary connections (changing the bus-bar connections) can sometimes compensate for a 30° difference: but a 60° difference is generally not bridgeable by simple reconnection.

**Conclusion:** Direct parallel operation is **not possible** without modification.

---

### Question 4

**(a) Define single phasing of a 3-phase Δ-Δ transformer. Show secondary voltages remain balanced when one phase is damaged. [04]**

**Single phasing of a 3-phase transformer:** One of the three single-phase units in the bank fails or is disconnected. The remaining two units continue to supply the 3-phase load.

**For a Δ-Δ transformer with one phase damaged:**

Let transformers T_AB, T_BC, T_CA form the bank. If T_CA fails, we have open-Δ (T_AB and T_BC remain).

In the primary Δ: voltage $V_{CA} = V_{AB} + V_{BC}$ (by Kirchhoff's voltage law around the delta loop, even with T_CA removed, the primary line voltages are fixed by the 3-phase supply). So $V_{AB}$ and $V_{BC}$ are determined by supply. $V_{CA} = -(V_{AB} + V_{BC})$: the voltage still exists across the open terminals.

On the secondary side: $V_{ab} = K \cdot V_{AB}$, $V_{bc} = K \cdot V_{BC}$. Since supply is balanced, $V_{AB}$ and $V_{BC}$ are balanced. The open secondary terminal for phase CA maintains voltage $V_{ca} = K \cdot V_{CA}$ (because the delta loop closes through the other two transformer EMFs).

**Result:** All three secondary line voltages remain balanced at the rated value, even with one transformer removed. *(Shown)*

**Trade-off:** Only 57.7% of the original bank's kVA capacity remains available.

---

**(b) Convert 3-phase to 2-phase or vice versa? If yes, explain. [04]**

Yes. This is done using the **Scott (T-T) connection**.

**Principle:** Two single-phase transformers are used.

1. **Main transformer:** Primary connected between two phases of the 3-phase supply (e.g., lines A and B). Secondary provides one phase of the 2-phase output.

2. **Teaser transformer:** Primary connected from the mid-point of the main transformer primary to the third line (C). The teaser primary has $\sqrt{3}/2$ (86.6%) of the main transformer's turns. Secondary provides the second phase of the 2-phase output, exactly 90° displaced from the first.

**Why it works:** The two primary voltages are 90° apart geometrically in the phasor diagram (the line-to-midpoint voltage is perpendicular to the line-to-line voltage in a balanced 3-phase system). This 90° separation transfers to the two secondary voltages, giving a balanced 2-phase output.

**Reverse (2-phase to 3-phase):** Connect the two-phase supply to the secondaries and the 3-phase supply comes from the primaries: the same transformation works in reverse because transformers are reciprocal devices.

---

**(c) 100 kVA transformer, full-load loss = 6 kW, half iron and half copper. Full load for 3 hr, half load for 4 hr. Find commercial efficiency. [04]**

**Given:** Total full-load loss $= 6$ kW → $P_{Fe} = 3$ kW, $P_{Cu,FL} = 3$ kW (equal split)

**Energy output:**

| Period | Load | Hours | kWh |
|:---|:---:|:---:|:---:|
| Full load | 100 kW | 3 | 300 |
| Half load | 50 kW | 4 | 200 |
| Remaining (no load) | 0 | 17 | 0 |
| **Total** | | 24 | **500 kWh** |

**Iron loss energy (24 hours):** $3 \times 24 = 72$ kWh

**Copper loss energy:**

| Period | Cu loss | Hours | kWh |
|:---|:---:|:---:|:---:|
| Full load | $3000$ W | 3 | 9.0 |
| Half load | $(0.5)^2 \times 3000 = 750$ W | 4 | 3.0 |
| No load | 0 | 17 | 0 |
| **Total Cu** | | | **12 kWh** |

**Total losses** $= 72 + 12 = 84$ kWh

**Total input** $= 500 + 84 = 584$ kWh

$$\boxed{\eta_{\text{commercial}} = \frac{500}{584} \times 100 = 85.62\%}$$

---

## SECTION - B (Induction Motors: Q5 to Q8)

### Question 5

**(a) What is an electrical machine? Describe the principle of operation of a 3-φ induction motor. [04]**

**Electrical machine:** A device that converts electrical energy to mechanical energy (motor) or mechanical energy to electrical energy (generator), using the principles of electromagnetic induction.

**3-φ IM operating principle:**
1. Three-phase balanced AC supply to stator creates a RMF of magnitude $1.5\Phi_m$ at synchronous speed $N_s = 120f/P$ rpm.
2. The RMF sweeps across stationary rotor bars. Relative motion induces EMF in rotor bars (Faraday's Law).
3. Induced EMF drives rotor current through short-circuited rotor bars.
4. Rotor current in the stator field produces Lorentz force (torque).
5. Rotor spins in the direction of RMF (Lenz's Law: to reduce relative motion).
6. Motor always runs at $N < N_s$ (slip $s > 0$), otherwise torque = 0.

---

**(b) Why is an IM called a rotating transformer? Advantages and disadvantages. [04]**

![Induction motor as a generalized rotating transformer showing stator primary, air gap, and short-circuited rotor secondary](../Books/diagrams/Ch-34_p58_fig45.jpg)

**Rotating transformer analogy:**

| Aspect | Transformer | Induction Motor |
|:---|:---|:---|
| Primary | Primary winding (stator) | Stator winding |
| Secondary | Secondary winding (rotor) | Rotor bars |
| Power transfer | Via mutual flux in core | Via rotating field in air gap |
| Secondary | Fixed (static) | Rotating |
| Secondary current | Load current | Rotor current (produces torque) |

The IM is called a rotating transformer because power transfers from stator to rotor by electromagnetic induction, just like in a transformer. The main difference: the rotor rotates.

**Advantages:**
- Simple, strong construction (no commutator, no brushes in squirrel-cage type)
- Self-starting
- Low maintenance and long life
- Can be used in hazardous environments (totally enclosed)
- Wide speed and size range available

**Disadvantages:**
- Speed control is difficult and costly
- Poor power factor at light loads (draws reactive current)
- Starting current is high (6–8 times rated)
- Speed drops with load (not constant-speed like synchronous motor)

---

**(c) 4-pole, 50 Hz IM. Find: (i) synchronous speed, (ii) rotor speed at s = 4%, (iii) rotor frequency at 600 rpm. [04]**

**Given:** $P = 4$, $f = 50$ Hz

**(i) Synchronous speed:**
$$N_s = \frac{120 \times 50}{4} = \boxed{1500 \text{ rpm}}$$

**(ii) Rotor speed at $s = 4\%$:**
$$N = N_s(1 - s) = 1500(1 - 0.04) = 1500 \times 0.96 = \boxed{1440 \text{ rpm}}$$

**(iii) Rotor frequency at $N = 600$ rpm:**
$$s = \frac{N_s - N}{N_s} = \frac{1500 - 600}{1500} = \frac{900}{1500} = 0.6$$

$$f_r = sf = 0.6 \times 50 = \boxed{30 \text{ Hz}}$$

---

### Question 6

**(a) 415V, 29.84 kW, 50 Hz delta-connected motor. No-load: 415V, 21A, 1250W. Locked rotor: 100V, 45A, 2730W. Circle diagram: line current, pf at rated output, max torque. [08]**

![Construction of Circle Diagram](../Books/diagrams/ch35_p06_fig35_09.jpg)

**No-load point (referred to line values):**
$$\cos\phi_0 = \frac{W_0}{\sqrt{3} V_L I_0} = \frac{1250}{\sqrt{3} \times 415 \times 21} = \frac{1250}{15092} = 0.0828, \quad \phi_0 = 85.25°$$

No-load components:
$I_{0x} = 21 \times 0.0828 = 1.74$ A (active)
$I_{0y} = 21 \times \sin(85.25°) = 21 \times 0.9966 = 20.93$ A (reactive)

**Short-circuit point (at full voltage):**
$$I_{sc} = 45 \times \frac{415}{100} = 186.75 \text{ A}$$

$$\cos\phi_{sc} = \frac{W_{sc}}{\sqrt{3} \times V_{sc} \times I_{sc,\text{test}}} = \frac{2730}{\sqrt{3} \times 100 \times 45} = \frac{2730}{7794} = 0.3503, \quad \phi_{sc} = 69.5°$$

$I_{scx} = 186.75 \times 0.3503 = 65.44$ A
$I_{scy} = 186.75 \times \sin(69.5°) = 186.75 \times 0.9367 = 174.94$ A

**Diameter of circle:**

The short-circuit current $I_{sc}$ defines the diameter. The no-load current $I_0$ defines the no-load point.

**Stator and rotor copper loss line:** Stator and rotor Cu losses are equal at standstill (given). So the torque line bisects the vertical intercept at the SC point.

**From circle diagram at rated output (29.84 kW):**

Input power at rated output (using circle diagram reading):
Output kW line drawn at height corresponding to 29.84 kW.

**(i) Line current at rated output:** ≈ 58 A (read from circle diagram)

**(ii) Power factor at rated output:** ≈ 0.71 lagging

**(iii) Maximum torque (from circle diagram):**

Maximum torque corresponds to the longest vertical intercept between the upper semi-circle and the torque line.

$$T_{\max} \approx \frac{\sqrt{3} \times 415 \times I_{\text{max torque}}}{2\pi N_s} \approx \text{read from diagram}$$

---

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

### Question 7

**(a) Define plugging. Describe blocked rotor test and no-load test. [04]**

![3-Phase Induction Motor Blocked-Rotor Test Circuit Connection (Two-Wattmeter Method)](diagrams/im_blocked_rotor_test_circuit.png)

![3-Phase Induction Motor No-Load Test Connection and Loss Separation Curves](../SlidesByMaam/diagrams/L-05_ECE-2107_p04_fig01.jpg)

**Plugging:** A braking method for induction motors. The phase sequence of the stator supply is reversed while the motor is running. The stator field now rotates opposite to the rotor. The motor develops a torque opposing motion. The motor decelerates rapidly. Supply is cut before the motor reverses.

**Blocked rotor test:** Rotor locked ($N = 0$, $s = 1$). Reduced voltage applied until rated current flows. Measure $V_{sc}$, $I_{sc}$, $P_{sc}$. Determines: $R_{01} = P_{sc}/(3I_{sc}^2)$, $Z_{01} = V_{sc}/(\sqrt{3}I_{sc})$, $X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$. Gives copper losses and equivalent circuit series parameters.

**No-load test:** Motor runs at no-load (no shaft load). Rated voltage applied. Measure $V_0$, $I_0$, $P_0$. The no-load power $P_0$ = stator iron loss + friction and windage loss + small stator copper loss. Determines shunt branch parameters ($R_c$, $X_m$) and friction/windage losses.

---

**(b) Effects of direct-line starting of IM > 25 kW. How to minimize? [04]**

**Effects of direct-on-line (DOL) starting:**
1. Starting current surge $= 5$–8 times rated current. This causes voltage dips in the supply that affect other loads.
2. High mechanical stress on motor shaft, couplings, and driven equipment due to high starting torque surges.
3. Thermal stress on windings: repeated DOL starting can overheat the motor.
4. For motors > 25 kW, the utility supply authority often prohibits DOL starting due to supply disturbances.

**How to minimize:**
1. **Star-delta starter:** Reduces starting voltage to $V_L/\sqrt{3}$. Starting current and torque reduce to 1/3 of DOL values.
2. **Auto-transformer starter:** Reduced voltage via tapped autotransformer. Provides better torque-current ratio than Y-Δ.
3. **Rotor resistance (slip-ring motor):** Insert external resistance in rotor circuit to improve starting torque with reduced current.
4. **Soft starter (electronic):** Thyristor-based gradual voltage ramp-up. Smooth starting, no current surge.
5. **Variable frequency drive (VFD):** Controls both voltage and frequency. Best control, most expensive.

---

**(c) Define braking of IM. How can speed be controlled? [04]**

**Braking of IM:** Applying a decelerating torque to bring the motor to rest (or to control speed during deceleration). Three methods: plugging, dynamic braking, regenerative braking.

**Speed control methods:**

1. **Stator voltage control:** Reduce supply voltage → reduce torque → speed drops. Simple but poor efficiency. Used for fan/pump loads.

2. **Supply frequency control (V/f control):** Change both $V$ and $f$ proportionally. Synchronous speed $N_s = 120f/P$ changes. Wide, smooth speed range. Used in VFDs.

3. **Pole changing:** Switch between winding configurations to change the number of poles ($P$). Gives discrete speed steps ($N_s = 120f/P$). Only for squirrel-cage motors.

4. **Rotor resistance control:** Add external resistance in rotor (slip-ring motors). Higher slip = lower speed. Simple but lossy.

5. **Slip energy recovery:** Feed slip power back to supply (Kramer system) instead of dissipating. Efficient but complex.

---

### Question 8

**(a) What is pull-out torque? Derive the equation for maximum starting torque of a 3-φ IM. [05]**

**Pull-out torque:** The maximum torque a 3-phase IM can develop while running. Also called breakdown torque or $T_{\max}$. If the mechanical load torque exceeds pull-out torque, the motor stalls.

**Maximum starting torque derivation:**

Starting torque is the torque at $s = 1$ (standstill):
$$T_{st} = \frac{k E_2^2 R_2}{R_2^2 + X_2^2}$$

To find $R_2$ for maximum starting torque, differentiate w.r.t. $R_2$ and set to zero:
$$\frac{d T_{st}}{dR_2} = \frac{(R_2^2 + X_2^2) - R_2(2R_2)}{(R_2^2 + X_2^2)^2} = 0$$

$$R_2^2 + X_2^2 - 2R_2^2 = 0 \implies R_2 = X_2$$

For maximum starting torque, rotor resistance must equal standstill rotor reactance.

Substituting $R_2 = X_2$:
$$T_{st,\max} = \frac{kE_2^2 X_2}{X_2^2 + X_2^2} = \boxed{\frac{kE_2^2}{2X_2}}$$

Note: $T_{st,\max} = T_{\max}$ (when $R_2 = X_2$, starting torque equals the maximum running torque). *(Derived)*

---

**(b) Explain why a 1-φ IM is not self-starting using double field revolving theory. [03]**

A single-phase stator creates a **pulsating** flux, not rotating. By the double-field revolving theory, this pulsating flux resolves into:
- Forward RMF: magnitude $\Phi_m/2$, speed $+N_s$
- Backward RMF: magnitude $\Phi_m/2$, speed $-N_s$

At standstill ($s = 1$ for forward, $s = 2 - 1 = 1$ effective for backward):
- Forward torque $T_f$ = backward torque $T_b$ (both equal and opposite)
- Net torque $= T_f - T_b = 0$

So the single-phase IM develops no net starting torque and cannot start by itself.

---

**(c) 8-pole, 50 Hz IM. $s_{FL} = 2\%$, $R_2 = 0.001\,\Omega$, $X_2 = 0.005\,\Omega$. Find: (i) $T_{\max}/T_{FL}$ ratio, (ii) speed at max torque. [04]**

$$N_s = \frac{120 \times 50}{8} = 750 \text{ rpm}$$

$$s_{mT} = \frac{R_2}{X_2} = \frac{0.001}{0.005} = 0.2$$

Using $a = s_{mT} = 0.2$, $s_f = 0.02$:
$$\frac{T_f}{T_{\max}} = \frac{2as_f}{a^2 + s_f^2} = \frac{2 \times 0.2 \times 0.02}{0.04 + 0.0004} = \frac{0.008}{0.0404} = 0.1980$$

$$\frac{T_{\max}}{T_f} = \frac{1}{0.1980} = \boxed{5.05}$$

**Speed at max torque:**
$$N_{mT} = 750(1 - 0.2) = \boxed{600 \text{ rpm}}$$

---

*Source:* [PrevYearQuestions/2019.md](../PrevYearQuestions/2019.md)

---

[← 2018 Answer](2018_answer.md) | [🏠 Index](README.md) | [2020 Answer →](2020_answer.md)
