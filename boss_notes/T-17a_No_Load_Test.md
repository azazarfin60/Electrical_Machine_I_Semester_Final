[← T-16: Power Flow](T-16_Power_Flow.md) | [🏠 Index](00_Index.md) | [T-17b: Blocked Rotor Test →](T-17b_Blocked_Rotor_Test.md)

---

# T-17a: No-Load Test (IM)
> **Section:** B | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-35 (Art. 35.3-35.5), VK Mehta Ch-8, Slides L-05

## Why This Topic Matters

The no-load test explanation appeared in 4 out of 7 papers (2019, 2021, 2023, 2024). It is always paired with the blocked rotor test. Together they are worth 4-9 marks. The no-load test provides the shunt branch parameters ($R_c$, $X_m$) and the no-load losses. This test is also an input to the circle diagram.

---

## 📝 Key Definitions

> **No-Load Test:** "The motor is run at no-load (no mechanical load on shaft) at rated voltage and frequency. Since the slip is very nearly zero, the rotor branch in the equivalent circuit is effectively an open circuit. The motor draws only a small no-load current to supply core loss and friction/windage losses." — Theraja, Art. 35.3

---

## Test Setup and Procedure

1. Connect the motor to rated 3-phase supply at rated voltage $V_0$ and rated frequency $f$.
2. Run the motor with no mechanical load on the shaft.
3. Measure: line voltage $V_0$, line current $I_0$, total 3-phase input power $P_0$.

**What happens at no-load:**
- Slip $s \approx 0$ (typically 0.001 to 0.005)
- Since $s \approx 0$: $R_2/s \to \infty$. The rotor branch is effectively open-circuited.
- The motor draws only no-load current $I_0$ (25-40% of rated current). This is much higher than a transformer's 2-5% because of the air gap.
- Input power $P_0$ covers: stator core loss + friction and windage + small stator $I^2R$ loss.

![No-load test equivalent circuit showing open rotor branch](diagrams/im_no_load_equivalent_circuit.png)

---

## Parameters from No-Load Test

**No-load power factor:**

$$\cos\phi_0 = \frac{P_0}{\sqrt{3} V_0 I_0}$$

**No-load current components:**

$$I_c = I_0\cos\phi_0 \quad \text{(core-loss component)}$$

$$I_m = I_0\sin\phi_0 \quad \text{(magnetizing component)}$$

**Shunt branch parameters (per phase):**

$$R_c = \frac{V_\phi}{I_c}, \qquad X_m = \frac{V_\phi}{I_m}$$

where $V_\phi = V_0/\sqrt{3}$ for star connection and $V_\phi = V_0$ for delta.

**Rotational losses:**

$$P_{\text{rot}} = P_0 - 3I_{0,\text{ph}}^2R_1$$

where $R_1$ is the stator resistance per phase (from DC test), and $I_{0,\text{ph}}$ is the no-load phase current ($I_0$ for star, $I_0/\sqrt{3}$ for delta). The term $3I_{0,\text{ph}}^2R_1$ is the small stator copper loss at no-load.

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

So the standard one-line answer is: **no-load test, blocked-rotor (locked-rotor) test, and the DC resistance test.**

Note the mark budget: 2 marks. Name the tests and give the one-line purpose of each. Do not write out the full derivations here; they are asked separately.

---

### 🎯 Q2: Describe the no-load test. What does plugging mean?
> **Appeared:** 2019 Q7(a) — (4 marks)

**Full Answer:**

**No-load test:** Motor runs at no-load, rated voltage and frequency. Measure $V_0$, $I_0$, $P_0$. Since $s \approx 0$, rotor branch is open. $P_0$ gives core loss + friction/windage. The no-load power factor is very low (0.1-0.2) because the current is mostly magnetizing.

Parameters: $R_c = V_\phi/I_c$ and $X_m = V_\phi/I_m$.

**Plugging:** A braking method. The phase sequence of the stator supply is reversed while the motor is running. The stator field now rotates opposite to the rotor. A braking torque opposes motion. The motor decelerates rapidly. Supply must be cut before zero speed, or the motor reverses direction.

---

## Exam Variants

| Year | Question | Marks | Paired With |
|:---|:---|:---|:---|
| 2019 Q7(a) | Describe no-load test + define plugging | 4 | Plugging definition |
| 2024 Q7(a) | Enlist the tests used for circuit model parameters | 2 | Blocked rotor test |

> Note: 2023 Q7(a) was not a testing question. It was the Y-Δ starter, which sits in [T-19](T-19_Starting_Methods_3Phase.md).

---

## ⚡ Exam Tips & Common Mistakes

1. **No-load test gives the SHUNT branch** ($R_c$, $X_m$). Blocked rotor test gives the SERIES branch ($R_{01}$, $X_{01}$).
2. **Don't forget the stator $I^2R$ correction.** $P_{\text{rot}} = P_0 - 3I_0^2R_1$, not just $P_0$.
3. **No-load power factor is very low** (0.08-0.2). The current is mostly magnetizing.
4. **For delta connection:** $V_\phi = V_0$ (line voltage = phase voltage). For star: $V_\phi = V_0/\sqrt{3}$.

## 🔗 Related Topics

- [T-17b: Blocked Rotor Test](T-17b_Blocked_Rotor_Test.md) — Always paired with NL test
- [T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) — Circuit that these tests determine
- [T-18: Circle Diagram](T-18_Circle_Diagram.md) — Uses NL + BR test data

---

[← T-16: Power Flow](T-16_Power_Flow.md) | [🏠 Index](00_Index.md) | [T-17b: Blocked Rotor Test →](T-17b_Blocked_Rotor_Test.md)
