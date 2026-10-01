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
- The motor draws only no-load current $I_0$ (5-10% of rated current).
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

$$P_{\text{rot}} = P_0 - 3I_0^2R_1$$

where $R_1$ is the stator resistance per phase (from DC test). The term $3I_0^2R_1$ is the small stator copper loss at no-load.

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Explain the no-load and blocked rotor tests for a 3-phase IM. Determine the equivalent circuit parameters.
> **Appeared:** 2023 Q7(a), 2024 Q7(a) — (9 marks)

**Full Answer:**

**No-Load Test:**

Motor runs uncoupled at rated voltage and frequency. Since $s \approx 0$, the rotor branch is effectively open. The motor draws a small no-load current $I_0$.

**Measurements:** $V_0$ (line voltage), $I_0$ (line current), $P_0$ (3-phase power).

**Parameters found:** Shunt branch ($R_c$, $X_m$).

$$\cos\phi_0 = \frac{P_0}{\sqrt{3}V_0I_0}$$

$$I_c = I_0\cos\phi_0, \quad I_m = I_0\sin\phi_0$$

$$R_c = V_\phi/I_c, \quad X_m = V_\phi/I_m$$

Rotational losses: $P_{\text{rot}} = P_0 - 3I_0^2R_1$

**Blocked-Rotor Test:** (See [T-17b](T-17b_Blocked_Rotor_Test.md) for full details)

Rotor locked ($s = 1$). Reduced voltage applied until rated current flows. Measure $V_{sc}$, $I_{sc}$, $P_{sc}$.

$$Z_{01} = \frac{V_{sc}/\sqrt{3}}{I_{sc}}, \quad R_{01} = \frac{P_{sc}}{3I_{sc}^2}, \quad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$

$$R_2' = R_{01} - R_1, \quad X_1 = X_2' = X_{01}/2$$

**DC Test** (for $R_1$): Apply DC between two stator terminals. For star: $R_1 = R_{DC}/2$. For delta: $R_1 = 1.5R_{DC}$.

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
| 2019 Q7(a) | Describe NL test + define plugging | 4 | Plugging definition |
| 2023 Q7(a) | Explain NL + BR tests, find parameters | 9 | Blocked rotor test |
| 2024 Q7(a) | Explain NL + BR tests, find parameters | 9 | Blocked rotor test |

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
