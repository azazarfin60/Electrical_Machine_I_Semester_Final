[← T-17a: No-Load Test](T-17a_No_Load_Test.md) | [🏠 Index](00_Index.md) | [T-18: Circle Diagram →](T-18_Circle_Diagram.md)

---

# T-17b: Blocked Rotor Test
> **Section:** B | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-35 (Art. 35.6-35.8), VK Mehta Ch-8, Slides L-05

## Why This Topic Matters

The blocked rotor test is always tested together with the no-load test. The pair appeared in 4 out of 7 papers. The blocked rotor test determines the series impedance ($R_{01}$, $X_{01}$) of the equivalent circuit. A standalone SC test numerical (given $V_{sc}$, $I_{sc}$, $P_{sc}$, find $R_2'$, $X_1$, $X_2'$) is a likely 4-mark variant.

2024 asked only for the **names** of the tests (2 marks), not the derivations. Do not over-write here. When the paper asks for parameters, the working is given below.

---

## 📝 Key Definitions

> **Blocked Rotor Test (Locked Rotor Test):** "The rotor is held stationary (locked) so that it cannot rotate. A reduced voltage (10-15% of rated) is applied to the stator so that rated full-load current flows. Since the voltage is low, core losses are negligible and the input power is essentially the full-load copper loss." — Theraja, Art. 35.6

---

## Test Setup and Procedure

1. Lock the rotor mechanically so it cannot rotate ($s = 1$).
2. Apply reduced voltage to the stator until rated full-load current flows.
3. Measure: line voltage $V_{sc}$, line current $I_{sc}$, total 3-phase input power $P_{sc}$.

**What happens at blocked rotor:**
- $s = 1$, so $R_2/s = R_2$ (small value). The rotor branch draws heavy current.
- At low voltage (10-15% of rated), the shunt branch current is negligible.
- All input power is copper loss: $P_{sc} = P_{Cu,s} + P_{Cu,r}$.

![Blocked rotor test equivalent circuit](diagrams/im_blocked_rotor_equivalent_circuit.png)

---

## Parameters from Blocked Rotor Test

**Equivalent impedance referred to stator (per phase):**

$$Z_{01} = \frac{V_{sc,\phi}}{I_{sc,\phi}} = \frac{V_{sc}/\sqrt{3}}{I_{sc}} \quad \text{(for star connection)}$$

$$R_{01} = \frac{P_{sc}}{3I_{sc,\phi}^2} = \frac{P_{sc}}{3I_{sc}^2} \quad \text{(for star connection)}$$

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$

**Separating stator and rotor parameters:**

$$R_2' = R_{01} - R_1$$

where $R_1$ is from the DC resistance test.

$$X_1 = X_2' = \frac{X_{01}}{2}$$

(Assuming equal leakage reactances on stator and rotor sides.)

---

## DC Resistance Test (for $R_1$)

Apply DC voltage between two stator terminals. Measure $V_{DC}$ and $I_{DC}$.

$$R_{DC} = V_{DC}/I_{DC}$$

For **star** connection: $R_1 = R_{DC}/2$ (two phases in series)

For **delta** connection: $R_1 = 1.5 \times R_{DC}$ (parallel-series combination)

---

## Worked Example

> **Practice problem (not from a past paper)**

**Star-connected IM, SC test: $V = 75$ V, $I = 38$ A, $P = 4$ kW. $R_1 = 0.5\,\Omega$/phase. Find $R_2'$, $X_1$, $X_2'$.**

**Per-phase voltage:** $V_{sc,\phi} = 75/\sqrt{3} = 43.30$ V

$$Z_{01} = \frac{43.30}{38} = \boxed{1.140\,\Omega}$$

$$R_{01} = \frac{4000}{3 \times 38^2} = \frac{4000}{4332} = \boxed{0.923\,\Omega}$$

$$X_{01} = \sqrt{1.140^2 - 0.923^2} = \sqrt{1.300 - 0.852} = \sqrt{0.448} = \boxed{0.669\,\Omega}$$

$$R_2' = R_{01} - R_1 = 0.923 - 0.5 = \boxed{0.423\,\Omega}$$

$$X_1 = X_2' = X_{01}/2 = 0.669/2 = \boxed{0.335\,\Omega}$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Enlist the test's name used for determining circuit model parameters of an IM.
> **Appeared:** 2024 Q7(a) — 2 marks

**Full Answer:**

Two laboratory tests give the equivalent circuit parameters, plus a third low-current test to split the series branch:

| Test | Full name | What is measured | Parameters obtained |
|:---|:---|:---|:---|
| **No-load test** | Running-light test | $V_0, I_0, P_0$ at rated voltage, shaft uncoupled | Shunt branch $R_c$, $X_m$; friction and windage loss |
| **Blocked rotor test** | Locked-rotor test (short-circuit test, equivalent test) | $V_{sc}, I_{sc}, P_{sc}$ at reduced voltage, rotor held | Series branch $Z_{01}, R_{01}, X_{01}$ |
| **DC test** | Winding resistance (ohmic) test | $V_{DC}, I_{DC}$ between stator terminals | $R_1$, hence $R_2' = R_{01} - R_1$ |

One-line answer: **no-load test, blocked-rotor (locked-rotor) test, and the DC resistance test.**

For the 2-mark version, that is enough. The derivations below are worth their own question if the paper asks for the parameters.

**Full derivations, for reference.**

*No-load test.* Motor runs uncoupled at rated voltage and frequency. Since $s \approx 0$, the rotor branch is effectively open.
$$\cos\phi_0 = \frac{P_0}{\sqrt{3}V_0I_0}, \qquad I_c = I_0\cos\phi_0, \quad I_m = I_0\sin\phi_0$$
$$R_c = V_\phi/I_c, \quad X_m = V_\phi/I_m, \qquad P_{\text{rot}} = P_0 - 3I_0^2R_1$$

*Blocked-rotor test.* Rotor locked ($s = 1$). Reduced voltage applied until rated current flows. At low voltage core loss is negligible, so input power = full-load copper loss.
$$Z_{01} = \frac{V_{sc}/\sqrt{3}}{I_{sc}}, \quad R_{01} = \frac{P_{sc}}{3I_{sc}^2}, \quad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$
$$R_2' = R_{01} - R_1, \quad X_1 = X_2' = X_{01}/2$$

*DC test* for $R_1$: apply DC between two stator terminals. Star: $R_1 = R_{DC}/2$. Delta: $R_1 = 1.5R_{DC}$.

---

### 🎯 Q2: SC test numerical: $V = 75$ V, $I = 38$ A, $P = 4$ kW, $R_1 = 0.5\,\Omega$. Find $R_2'$, $X_1$, $X_2'$.
> **Practice problem (not from a past paper)**

**Full Answer:**

See [Worked Example](#worked-example) above. Results: $R_2' = 0.423\,\Omega$, $X_1 = X_2' = 0.335\,\Omega$.

---

## Exam Variants

| Year | Question | Marks | Type |
|:---|:---|:---|:---|
| 2019 Q7(a) | Describe blocked rotor test | 4 | Theory |
| 2024 Q7(a) | Enlist the tests used for circuit model parameters | 2 | Names only |
| Practice (no past paper) | SC test numerical | — | Numerical |

> Note: 2023 Q7(a) was not a testing question. It was the Y-Δ starter, which sits in [T-19](T-19_Starting_Methods_3Phase.md).

---

## ⚡ Exam Tips & Common Mistakes

1. **Don't forget $\sqrt{3}$.** For star connection: $V_\phi = V_L/\sqrt{3}$. For delta: $V_\phi = V_L$.
2. **$R_{01}$ includes BOTH stator and rotor resistance.** $R_2' = R_{01} - R_1$.
3. **The assumption $X_1 = X_2'$** is standard unless told otherwise. State it explicitly.
4. **Blocked rotor test is analogous to SC test of transformer.** Same formulas, same logic.
5. **Power formula uses LINE current:** $R_{01} = P_{sc}/(3I_{sc}^2)$ where $I_{sc}$ is the LINE current (which equals phase current for star).

## 🔗 Related Topics

- [T-17a: No-Load Test](T-17a_No_Load_Test.md) — Always paired
- [T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) — The circuit being determined
- [T-18: Circle Diagram](T-18_Circle_Diagram.md) — Uses BR test data as input

---

[← T-17a: No-Load Test](T-17a_No_Load_Test.md) | [🏠 Index](00_Index.md) | [T-18: Circle Diagram →](T-18_Circle_Diagram.md)
