[← T-17b: Blocked Rotor Test](T-17b_Blocked_Rotor_Test.md) | [🏠 Index](00_Index.md) | [T-19: Starting Methods (3-Phase) →](T-19_Starting_Methods_3Phase.md)

---

# T-18: Circle Diagram
> **Section:** B | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-35 (Art. 35.9-35.14), Slides L-07

## Why This Topic Matters

Circle diagram problems appeared in 4 out of 7 papers (2017, 2018, 2019, 2021). Each problem is worth 6-9 marks. The trend is declining (absent in 2023, 2024), but it remains in syllabus and can return. The construction is mechanical: once you know the steps, it is guaranteed marks.

---

## 📝 Key Definitions

> **Circle Diagram:** "The locus of the stator current phasor of an induction motor, as the load changes from no-load to blocked rotor, is approximately a semicircle. This semicircle, called the circle diagram, can be used to predict the performance of the motor at any load." — Theraja, Art. 35.9

---

## Data Required

You need two test results:

| Test | Measurements | What It Gives |
|:---|:---|:---|
| **No-Load** | $V_0$, $I_0$, $P_0$ (or $\cos\phi_0$) | No-load point on circle |
| **Blocked Rotor** | $V_{sc}$, $I_{sc}$, $P_{sc}$ (or $\cos\phi_{sc}$) | Short-circuit point on circle |

Both must be referred to the same (rated) voltage.

---

## Construction Steps

### Step 1: Scale BR data to full voltage

If BR test was at reduced voltage $V_{sc}$:

$$I_{sc,\text{full}} = I_{sc} \times \frac{V_{\text{rated}}}{V_{sc}}$$

Power factor stays the same: $\cos\phi_{sc} = P_{sc}/(\sqrt{3}V_{sc}I_{sc})$

### Step 2: Calculate angles

$$\phi_0 = \cos^{-1}\!\left(\frac{P_0}{\sqrt{3}V_0I_0}\right)$$

$$\phi_{sc} = \cos^{-1}(\cos\phi_{sc})$$

### Step 3: Plot points

On a graph with horizontal axis = active current (watts component) and vertical axis = reactive current:

**No-load point $O'$:**
- $O'_x = I_0\cos\phi_0$, $O'_y = I_0\sin\phi_0$

**Short-circuit point $S$:**
- $S_x = I_{sc,\text{full}}\cos\phi_{sc}$, $S_y = I_{sc,\text{full}}\sin\phi_{sc}$

### Step 4: Draw the circle

Draw a semicircle through $O'$ and $S$. The center lies on a horizontal line through $O'$.

### Step 5: Draw the power and torque lines

- **Output line:** Horizontal line from $O'$ (no-load point)
- **Torque line (air-gap line):** Connects $O'$ to a point on the $S$-line divided by the rotor/total Cu loss ratio.
- The rotor Cu loss line divides the SC intercept in the ratio of rotor Cu loss to total Cu loss at standstill.

If rotor Cu loss = stator Cu loss at standstill (equal division), the line bisects the vertical intercept.

### Step 6: Read performance

For any operating point on the circle:
- Vertical distance below power line = output power
- Vertical distance below torque line = developed torque (in sync watts)
- Power factor = $\cos$ of angle between current vector and voltage reference

![Circle diagram construction](diagrams/circle_diagram_construction.jpg)

---

## What the Circle Diagram Can Predict

| Quantity | How to Read |
|:---|:---|
| **Line current** | Length of current vector from origin to operating point |
| **Power factor** | Cosine of angle between current vector and horizontal |
| **Output power** | Vertical height above output line, times voltage scale |
| **Max output** | Longest vertical intercept below output line |
| **Max torque** | Longest vertical intercept below torque line |
| **Slip** | Ratio of rotor Cu loss segment to total air-gap segment |
| **Efficiency** | Output segment / input segment |

![Circle diagram showing maximum quantities](diagrams/circle_diagram_max_quantities.jpg)

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Circle diagram: 415V, delta, 50 Hz motor. NL: 415V, 21A, 1250W. BR: 100V, 45A, 2730W. Find line current and pf at rated output.
> **Appeared:** 2017 Q3(b), 2019 Q6(a) — (9 marks)

**Full Answer:**

**No-load data:** $V = 415$ V (delta), $I_0 = 21$ A (line), $P_0 = 1250$ W

$$\cos\phi_0 = \frac{1250}{\sqrt{3} \times 415 \times 21} = \frac{1250}{15094} = 0.0828, \quad \phi_0 = 85.25°$$

**Blocked rotor (scaled to 415V):**

$$I_{sc,\text{full}} = 45 \times 415/100 = 186.75 \text{ A}$$

$$\cos\phi_{sc} = \frac{2730}{\sqrt{3} \times 100 \times 45} = 0.35, \quad \phi_{sc} = 69.5°$$

**Plot points** $O'$ and $S$ on the circle diagram. Draw the semicircle. Locate the operating point for rated output (29.84 kW).

Power scale: $\sqrt{3} \times 415 = 718.7$ W per ampere of active component.

**From diagram:** Line current at rated output $\approx 58$ A. Power factor $\approx 0.714$ lagging.

---

### 🎯 Q2: Circle diagram: 5.6 kW, 400V, 4-pole, 50 Hz slip-ring IM. NL: 6A, $\cos\phi_0 = 0.087$. BR: 100V, 12A, 720W. $R_1 = 0.67\,\Omega$, $R_2 = 0.185\,\Omega$. Find full-load current, slip, pf, max power.
> **Appeared:** 2018 Q7(b) — (8 marks)

**Full Answer:**

**Scale BR to full voltage:**

$I_{sc} = 12 \times 400/100 = 48$ A

$\cos\phi_{sc} = 720/(\sqrt{3} \times 100 \times 12) = 0.347$, $\phi_{sc} = 69.7°$

**No-load point:** $I_{0x} = 6 \times 0.087 = 0.52$ A, $I_{0y} = 5.98$ A

**SC point:** $I_{scx} = 48 \times 0.347 = 16.66$ A, $I_{scy} = 45.02$ A

**Rotor Cu loss line:** Total SC Cu loss at full voltage $= 720 \times (400/100)^2 = 11520$ W.

Stator Cu loss $= 3 \times 48^2 \times 0.67 = 4631$ W. Rotor Cu loss $= 11520 - 4631 = 6889$ W.

Ratio: $6889/11520 = 0.598$. The rotor Cu loss line divides the SC intercept at 59.8% from the power line.

**From diagram:** Full-load current $\approx 10.5$ A, slip $\approx 6.2\%$, pf $\approx 0.78$ lagging, max power $\approx 8.2$ kW.

---

### 🎯 Q3: Circle diagram: 14.92 kW, 400V, 6-pole. NL: 11A, pf=0.2. SC: 100V, 25A, pf=0.4. Rotor Cu = half total Cu at standstill.
> **Appeared:** 2021 Q8(c) — (6 marks)

**Full Answer:**

**No-load:** $I_{0x} = 11 \times 0.2 = 2.2$ A, $I_{0y} = 10.78$ A

**SC (scaled):** $I_{sc} = 25 \times 400/100 = 100$ A, $\cos\phi_{sc} = 0.4$

$I_{scx} = 40$ A, $I_{scy} = 91.65$ A

Plot $O'$ and $S$, draw semicircle. Since rotor Cu = stator Cu at standstill, the rotor Cu line bisects the SC intercept at 50%.

$N_s = 120 \times 50/6 = 1000$ rpm. Power scale: $\sqrt{3} \times 400 = 692.8$ W/A.

For 14.92 kW rated output, locate operating point:

**From diagram:** Line current $\approx 30$ A, slip $\approx 5\%$, efficiency $\approx 84\%$, pf $\approx 0.76$ lagging.

Maximum torque = longest vertical intercept below torque line (read from diagram in sync watts).

---

## Exam Variants

| Year | Question | Data | Marks |
|:---|:---|:---|:---|
| 2017 Q3(b) | 415V delta, 29.84 kW | NL+BR data | 9 |
| 2018 Q7(b) | 400V, 5.6 kW slip-ring | NL+BR+R1+R2 | 8 |
| 2019 Q6(a) | Same as 2017 | Same problem | 9 |
| 2021 Q8(c) | 400V, 14.92 kW, 6-pole | NL+BR, equal Cu | 6 |

---

## ⚡ Exam Tips & Common Mistakes

1. **Always scale BR data to rated voltage.** Current scales linearly with voltage: $I_{sc,\text{full}} = I_{sc} \times V_{\text{rated}}/V_{sc}$. Power factor stays the same.
2. **Choose a clear current scale.** For example: 1 cm = 5 A. Label your scale.
3. **Delta connection:** $I_{\text{phase}} = I_{\text{line}}/\sqrt{3}$. Star: $I_{\text{phase}} = I_{\text{line}}$.
4. **The power axis is horizontal.** Active current on x-axis, reactive on y-axis.
5. **The circle diagram is declining in frequency.** Absent in 2023 and 2024. But still in syllabus.
6. **Carry a protractor and compass** to the exam for this question.

## 🔗 Related Topics

- [T-17a: No-Load Test](T-17a_No_Load_Test.md) — Provides no-load point
- [T-17b: Blocked Rotor Test](T-17b_Blocked_Rotor_Test.md) — Provides SC point
- [T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) — Analytical alternative

---

[← T-17b: Blocked Rotor Test](T-17b_Blocked_Rotor_Test.md) | [🏠 Index](00_Index.md) | [T-19: Starting Methods (3-Phase) →](T-19_Starting_Methods_3Phase.md)
