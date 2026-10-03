[← T-17: Power Flow & Rotor Power](T-17_Power_Flow_and_Rotor_Power.md) | [🏠 Index](README.md) | [T-19: 3-Phase Starting Methods →](T-19_Starting_Methods_3-Phase_IM.md)

---

# T-18: IM Testing & Circle Diagram

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **IM Testing & Circle Diagram** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### IM-04: Blocked Rotor Test: Full Procedure and Why It's Needed

*Appears in: CT-02 Q2, 2019 Q7a, 2020 Q7c, 2021 Q8, 2024 Q7a*
>
> Note: 2024 Q7(a) is a 2-mark question that only asks for the **names** of the tests. 2023 Q7(a) was the Y-Δ starter, not a testing question.

#### What this test does

The blocked rotor test is to an induction motor what the short-circuit test is to a transformer. The rotor is physically locked, just as the secondary of a transformer is short-circuited. The result: the rotor is stationary, slip = 1, and the rotor presents its maximum impedance to the magnetic field.

This test lets us measure the series parameters of the motor equivalent circuit without needing to run the motor under full load.

#### The detailed procedure

**Setup:**
1. Identify the rotor type. For squirrel-cage: just use the motor as-is. For wound-rotor (slip-ring): short the slip rings (remove external resistance).
2. Lock the rotor shaft. Use a mechanical clamp, a brake, or a wooden block wedged between the stator housing and the shaft. The shaft must be absolutely stationary during the test.
3. Connect measuring equipment: 3-phase variac, voltmeters, ammeters (one per phase is best for balance verification), two wattmeters (for 2-wattmeter method of 3-phase power measurement).
4. Set the variac to minimum (zero output).

**Running the test:**
5. Slowly increase the variac until the ammeters read rated stator current.
6. Note: the voltage required is usually only 10–20% of rated voltage. This is because the rotor is stationary: no back-EMF opposing current. The full motor impedance is much lower than normal running.
7. Read and record: line voltage $V_{sc}$, line current $I_{sc}$ (should equal rated), total 3-phase power $P_{sc} = W_1 + W_2$.
8. **Do not keep the test running for more than 30–60 seconds.** Rated current is flowing through windings with a stationary rotor: all power is being converted to heat. The windings will overheat quickly.
9. Reduce variac to zero and disconnect supply.

![Blocked rotor test circuit connection on 3-phase induction motor](../Books/Theraja/Ch-35/diagrams/ch35_p06_fig35_09.jpg)

#### Why low voltage means negligible core loss

Core (iron) loss is approximately proportional to $V^2$ (since $B \propto V$, and $P_{\text{eddy}} \propto B^2$, $P_{\text{hyst}} \propto B^{1.6}$).

At 15% of rated voltage: core loss $\approx (0.15)^2 \times P_{Fe,\text{rated}} = 0.0225 \times P_{Fe,\text{rated}}$

Only 2.25% of rated core loss: completely negligible.

So $P_{sc}$ = stator copper loss + rotor copper loss. This is what we call full-load copper loss.

#### Parameter extraction (star connection)

Convert line values to per-phase values (divide voltages by $\sqrt{3}$ for star):

$$Z_{01} = \frac{V_{sc}/\sqrt{3}}{I_{sc}}$$

$$R_{01} = \frac{P_{sc}}{3I_{sc}^2}$$

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$

Separate stator and rotor components:
- Measure stator resistance $R_1$ separately (DC resistance × 1.3 for AC skin-effect correction).
- $R_2' = R_{01} - R_1$
- Assume equal leakage: $X_1 = X_2' = X_{01}/2$

![3-Phase Induction Motor Blocked-Rotor Test Circuit Connection (Two-Wattmeter Method)](diagrams/im_blocked_rotor_test_circuit.png)

![Per-Phase Equivalent Circuit During Blocked-Rotor Test (Simplified Series Circuit)](diagrams/im_blocked_rotor_equivalent_circuit.png)

#### The five things this test gives you

1. **Full-load copper losses** → Calculate efficiency at any load.
2. **Series impedance** $R_{01}$, $X_{01}$ → Complete the equivalent circuit.
3. **Starting current at rated voltage:**
   $$I_{start} = I_{sc} \times \frac{V_{\text{rated}}}{V_{sc}}$$
   This lets you check if DOL starting is safe or if a starter is needed.
4. **Starting torque:**
   $$T_{start} \propto \frac{I_{start}^2 \cdot R_2'}{N_s}$$
5. **Circle diagram construction:** The short-circuit current magnitude ($I_{sc,\text{full voltage}}$) and power factor ($\cos\phi_{sc}$) define the circle diagram's short-circuit point.

![Induction motor circle diagram construction and torque line](../Books/Theraja/Ch-35/diagrams/ch35_p08_fig35_11.jpg)


---

*Source questions:* [PrevYearQuestions](../PrevYearQuestions/README.md) (all years)

---

### [2024 Q7(a)]: Tests for Determining Equivalent Circuit Model Parameters of an Induction Motor

> 📋 **Appeared in:** 2024 Q7(a)

**(a) Enlist the test's name used for determining circuit model parameters of an IM. [Marks: 02, CO: 1]**

#### Complete List of Tests and Parameters Determined

To determine all five parameters of the per-phase equivalent circuit ($R_1, X_1, R_2', X_2', R_c, X_m$) of a three-phase induction motor, three standard laboratory tests are performed:

1. **No-Load Test (Running Light Test):**
   - **Procedure:** Rated balanced line voltage at rated frequency is applied to the stator with the motor running uncoupled from any mechanical load ($s \approx 0$).
   - **Measurements:** No-load line voltage ($V_0$), no-load line current ($I_0$), and active input power ($W_0$).
   - **Parameters Determined:**
     - Shunt core-loss resistance ($R_c$ or $R_0$) and magnetizing reactance ($X_m$ or $X_0$).
     - Constant rotational losses: core iron loss ($P_{Fe}$) and mechanical friction & windage loss ($P_{fw}$).

2. **Blocked-Rotor Test (Locked-Rotor Test):**
   - **Procedure:** The rotor is mechanically clamped/locked to prevent rotation ($N = 0$, slip $s = 1$). A reduced, variable voltage at rated frequency is applied to the stator and adjusted until rated full-load stator current circulates.
   - **Measurements:** Blocked-rotor voltage ($V_{BR}$), rated current ($I_{BR}$), and power input ($W_{BR}$).
   - **Parameters Determined:**
     - Equivalent series resistance referred to stator: $R_{01} = R_1 + R_2' = W_{BR} / (3 I_{BR,ph}^2)$.
     - Equivalent series leakage reactance referred to stator: $X_{01} = X_1 + X_2' = \sqrt{Z_{BR}^2 - R_{01}^2}$.
     - Total full-load copper loss ($P_{Cu,FL}$).

3. **Stator DC Resistance Test:**
   - **Procedure:** A direct current (DC) source is applied across pairs of stator terminals using a Kelvin bridge or DC voltmeter-ammeter method to measure DC winding resistance.
   - **Correction:** Multiplied by an empirical AC skin-effect factor ($R_{1,AC} \approx 1.2\text{–}1.25 \times R_{1,DC}$) and temperature-corrected to operating temperature ($75^\circ\text{C}$).
   - **Parameter Determined:**
     - Stator winding resistance per phase ($R_1$).
     - Enables separating rotor resistance from total equivalent resistance: $R_2' = R_{01} - R_1$. (Reactance is typically split as $X_1 = X_2' = 0.5 X_{01}$ or per NEMA design classes).

---

[← T-17: Power Flow & Rotor Power](T-17_Power_Flow_and_Rotor_Power.md) | [🏠 Index](README.md) | [T-19: 3-Phase Starting Methods →](T-19_Starting_Methods_3-Phase_IM.md)
