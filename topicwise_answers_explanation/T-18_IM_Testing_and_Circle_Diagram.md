[← T-17: Power Flow & Rotor Power](T-17_Power_Flow_and_Rotor_Power.md) | [🏠 Index](README.md) | [T-19: 3-Phase Starting Methods →](T-19_Starting_Methods_3-Phase_IM.md)

---

# T-18: IM Testing & Circle Diagram

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **IM Testing & Circle Diagram** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### IM-04: Blocked Rotor Test: Full Procedure and Why It's Needed

*Appears in: CT-02 Q2, 2019 Q7a, 2020 Q7c, 2021 Q8, 2023 Q7a, 2024 Q7a*

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

![Blocked rotor test circuit connection on 3-phase induction motor](../Books/diagrams/ch35_p06_fig35_09.jpg)

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

![Induction motor circle diagram construction and torque line](../Books/diagrams/ch35_p08_fig35_11.jpg)


---

*Source questions:* [PrevYearQuestions](../PrevYearQuestions/README.md) (all years)

---

### Q7: Blocked rotor test 2024: emphasis on what the parameters mean physically

> 📋 **Appeared in:** 2024 Q7

#### What each parameter tells you

**$R_{01}$** (total series resistance referred to stator):
This represents all copper losses in both windings per unit current squared. If you multiply by the rated current squared and by 3 (three phases), you get the full-load copper loss in watts. This goes directly into efficiency calculation.

**$X_{01}$** (total series leakage reactance):
This is the reactance that limits current during a short circuit. During a fault: $I_{fault} = V/(Z_{01}) = V/\sqrt{R_{01}^2 + X_{01}^2}$. A motor with high $X_{01}$ (high leakage reactance) will have lower fault current: safer.

**$R_2'$ vs $R_1$:**
Separating rotor from stator resistance tells you where copper losses are concentrated. If $R_2' > R_1$, the rotor has higher resistance: perhaps by design (to improve starting torque, at the cost of running efficiency).

**$X_1 = X_2'$:**
The assumption that stator and rotor leakage reactance are equal is an approximation. For exact analysis, they can be separated by running the blocked rotor test at different frequencies (reducing frequency reduces $X$ effects and helps isolate $R$).

---

[← T-17: Power Flow & Rotor Power](T-17_Power_Flow_and_Rotor_Power.md) | [🏠 Index](README.md) | [T-19: 3-Phase Starting Methods →](T-19_Starting_Methods_3-Phase_IM.md)
