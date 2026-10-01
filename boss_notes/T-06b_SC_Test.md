[← T-06a: OC Test](T-06a_OC_Test.md) | [🏠 Index](00_Index.md) | [T-06c: Efficiency →](T-06c_Efficiency.md)

---

# T-06b: Short-Circuit (SC) Test
> **Section:** A | **Priority:** 🔴 MUST | **Exam Frequency:** 7/7 years
> **Sources:** Theraja Ch-32 (Art. 32.26–32.28), VK Mehta Ch-7 (Art. 7.20), Slides L-10 S18

## Why This Topic Matters

The SC test always appears together with the OC test. ALL 7 papers include an OC/SC numerical. The SC test determines the series branch parameters ($R_{01}$, $X_{01}$, $Z_{01}$) and the full-load copper loss. These parameters are then used to calculate voltage regulation and efficiency. In 2024, a new conceptual question appeared: "Why is the SC test done on the HV side?"

---

## 📝 Key Definitions

> **Short-Circuit (SC) Test (Impedance Test):** "The purpose of this test is to determine (i) full-load copper loss and (ii) the equivalent resistance and leakage reactance of the transformer referred to the winding in which instruments are placed. In this test, the secondary (usually the low-voltage winding) is solidly short-circuited by a thick conductor. A low voltage is applied to the primary (usually HV winding) and is carefully adjusted till full-load currents are flowing in both primary and secondary." — VK Mehta, Art. 7.20

> **Copper loss ($P_{Cu}$):** "The copper loss is the $I^2R$ loss in the windings due to resistance. At any fraction $x$ of full load: $P_{Cu} = x^2 P_{Cu,FL}$. At half load, copper loss is only one-quarter of full-load copper loss." — From Theraja Art. 32.29

---

## Test Setup and Procedure

![Short-Circuit (SC) Test Circuit Diagram](diagrams/transformer_sc_test_circuit.png)

**Connections (VK Mehta, Art. 7.20):**
1. **Short-circuit the LV winding** with a thick copper bar (very low resistance short).
2. Apply a **reduced voltage** to the **HV winding** through a variac. Start from zero and increase gradually.
3. Connect measuring instruments on the HV side:
   - Voltmeter ($V_{sc}$) across the HV winding
   - Ammeter ($I_{sc}$) in series
   - Wattmeter ($W_{sc}$)
4. Increase voltage until $I_{sc}$ reaches the **rated current** of the HV winding. Stop. Record readings.

**Why HV side?**
- The rated current on the HV side is smaller (easier to measure).
- The required voltage to circulate rated current through the short is only 5–10% of rated voltage (safe and convenient).
- If done on the LV side, the required voltage would be even smaller and harder to measure accurately.

**Readings taken:** $V_{sc}$, $I_{sc}$ (= rated current), $W_{sc}$ at rated current.

---

## Parameter Extraction

Since the applied voltage is very low (5–10% of rated), the core flux is very small. Iron losses (which depend on flux) are negligible.

**All power input = full-load copper loss:**

$$\boxed{P_{Cu,FL} = W_{sc}}$$

This copper loss is at rated current. At any other load fraction $x$:

$$P_{Cu} = x^2 \cdot P_{Cu,FL}$$

**Series impedance (referred to the HV/test side):**

$$\boxed{Z_{01} = \frac{V_{sc}}{I_{sc}}}$$

$$\boxed{R_{01} = \frac{W_{sc}}{I_{sc}^2}}$$

$$\boxed{X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}}$$

To refer to the other side, divide by $a^2$:

$$R_{02} = R_{01}/a^2, \qquad X_{02} = X_{01}/a^2, \qquad Z_{02} = Z_{01}/a^2$$

---

## Combined OC + SC Test: Complete Worked Example (PYQ 2024)

**Problem:** 20 kVA, 2000/400V transformer. OC test (HV open): 400V, 1.5A, 160W. SC test (LV short): 60V, rated I, 300W. Find: (i) equivalent circuit parameters referred to HV, (ii) efficiency at full-load 0.8 pf lag, (iii) voltage regulation.

> **Appeared:** 2024 Q3(b) — 8 marks

### Step 1: Identify Sides

- Turns ratio: $a = 2000/400 = 5$
- OC test was done on LV (400V) side
- SC test was done on HV (2000V) side

### Step 2: OC Test → Shunt Parameters

$$\cos\phi_0 = \frac{W_0}{V_0 I_0} = \frac{160}{400 \times 1.5} = 0.2667$$

$$I_w = 1.5 \times 0.2667 = 0.400 \text{ A}$$

$$I_\mu = 1.5 \times \sin(\cos^{-1}0.2667) = 1.5 \times 0.964 = 1.446 \text{ A}$$

Referred to LV side:

$$R_{c,LV} = \frac{400}{0.400} = 1000\,\Omega, \qquad X_{m,LV} = \frac{400}{1.446} = 276.6\,\Omega$$

Referred to HV side ($\times a^2 = 25$):

$$\boxed{R_{c,HV} = 25000\,\Omega}, \qquad \boxed{X_{m,HV} = 6915\,\Omega}$$

Iron loss: $P_{Fe} = W_0 = 160$ W

### Step 3: SC Test → Series Parameters

Rated HV current: $I_{1,rated} = 20000/2000 = 10$ A

$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{300}{100} = \boxed{3.0\,\Omega}$$

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{60}{10} = 6.0\,\Omega$$

$$X_{01} = \sqrt{6.0^2 - 3.0^2} = \sqrt{27} = \boxed{5.196\,\Omega}$$

Copper loss: $P_{Cu,FL} = W_{sc} = 300$ W

### Step 4: Efficiency at Full-Load, 0.8 pf Lag

$$\eta = \frac{S\cos\phi}{S\cos\phi + P_{Fe} + P_{Cu,FL}} = \frac{20000 \times 0.8}{16000 + 160 + 300} = \frac{16000}{16460} = \boxed{97.2\%}$$

### Step 5: Voltage Regulation at 0.8 pf Lag

$$\text{VR\%} = \frac{I_1(R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100$$

$$= \frac{10(3.0 \times 0.8 + 5.196 \times 0.6)}{2000} \times 100 = \frac{10 \times 5.518}{2000} \times 100 = \boxed{2.76\%}$$

---

## Exam Variants — The OC/SC Numerical Bank

| Year | Transformer | OC Data | SC Data | Asked For |
|:---|:---|:---|:---|:---|
| 2017 Q6(c) | 500 kVA, 2300/208V | 208V, 85A, 1800W | 95V, 217.4A, 8200W | $R_{02}$, parameters |
| 2018 Q2(b) | 10 kVA, 11kV/230V | 220V, 1.5A, 200W | 120V, rated I, 300W | η at FL/HL |
| 2019 Q2(c) | 10 kVA, 2200/220V | 220V, 1.5A, 153W | 115V, rated I, 224W | η at FL/HL |
| 2020 Q2(c) | Draw circuits | — | — | Circuit diagrams |
| 2021 Q2(c) | 20 kVA, 2400/240V | — | 72V, rated I, 275W | $R_{01}$, $X_{01}$, VR |
| 2023 Q2(b) | 2.2kV/220V | 220V, 0.8A, 80W | 12V, 10A, 40W | Eq. circuit to secondary |
| 2024 Q3(b) | 20 kVA, 2000/400V | 400V, 1.5A, 160W | 60V, rated I, 300W | Eq. circuit + η + VR |

> [!IMPORTANT]
> **Memorize this procedure. It is worth 5–10 marks in EVERY exam.** The data changes but the steps are identical every time.

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Given OC and SC test data, find equivalent circuit parameters, efficiency, and voltage regulation.
> **Appeared:** 2017 Q6(c), 2018 Q2(b), 2019 Q2(c), 2021 Q2(c), 2023 Q2(b), 2024 Q3(b) — (4–8 marks)

**Full Answer:**

The procedure is always the same 5-step method. See the [Complete Worked Example above](#combined-oc--sc-test-complete-worked-example-pyq-2024) for the full solution template (2024 data). For any other year's data, simply substitute the numbers into the same formulas:

**Step 1:** Identify which side each test was done on. OC test is usually on LV. SC test is usually on HV. Compute $a = V_1/V_2$.

**Step 2 (OC test):** $P_{Fe} = W_0$. Then $\cos\phi_0 = W_0/(V_0 I_0)$. Then $I_w = I_0\cos\phi_0$, $I_\mu = I_0\sin\phi_0$. Finally $R_c = V_0/I_w$ and $X_m = V_0/I_\mu$. To refer to other side: multiply by $a^2$.

**Step 3 (SC test):** $P_{Cu,FL} = W_{sc}$. Then $R_{01} = W_{sc}/I_{sc}^2$, $Z_{01} = V_{sc}/I_{sc}$, $X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$.

**Step 4 (Efficiency):** $\eta = xS\cos\phi / (xS\cos\phi + P_{Fe} + x^2 P_{Cu,FL})$

**Step 5 (VR):** $\text{VR\%} = I_1(R_{01}\cos\phi \pm X_{01}\sin\phi)/V_1 \times 100$

---

### 🎯 Q2: Why is the SC test performed on the HV side?
> **Appeared:** 2024 Q2(b) — new pattern

**Full Answer:**

The SC test is performed on the HV side for three reasons:

**(1) Lower current:** The rated current on the HV side is smaller than on the LV side (since $I \propto 1/V$ for the same kVA). Smaller current is easier and cheaper to supply from a variable AC source, and the ammeter can be lower-rated.

**(2) Higher impedance, easier measurement:** The HV winding has more turns, so its impedance ($R_{01}$, $X_{01}$) is larger. The short-circuit voltage $V_{sc}$ needed to force rated current through the referred impedance is larger and more easily measured. If the test were done on the LV side, $V_{sc}$ would be very small (perhaps only a few volts) and measurement accuracy would suffer.

**(3) Safety:** The voltage applied during the SC test is only 5–10% of rated HV voltage. This is a safe, low voltage. If the test were done on the LV side, even the small required voltage could be awkward to control precisely.

---

### 🎯 Q3: 2023 variant — OC: 220V, 0.8A, 80W; SC: 12V, 10A, 40W. Find equivalent circuit referred to secondary.
> **Appeared:** 2023 Q2(b) — 6 marks

**Full Answer:**

Given: 2.2 kV/220V transformer.

**OC test (done on LV = 220V side):**

$P_{Fe} = 80$ W

$\cos\phi_0 = 80/(220 \times 0.8) = 0.4545$

$I_w = 0.8 \times 0.4545 = 0.3636$ A, $I_\mu = 0.8 \times \sin(\cos^{-1}0.4545) = 0.8 \times 0.8908 = 0.7127$ A

$R_{c,LV} = 220/0.3636 = \boxed{605\,\Omega}$, $X_{m,LV} = 220/0.7127 = \boxed{308.6\,\Omega}$

(Already on the secondary/LV side since OC test was done there.)

**SC test (done on HV = 2200V side):**

$a = 2200/220 = 10$

$I_{sc} = 10$ A. $R_{01} = 40/100 = 0.4\,\Omega$, $Z_{01} = 12/10 = 1.2\,\Omega$, $X_{01} = \sqrt{1.44 - 0.16} = 1.131\,\Omega$

Referred to secondary (divide by $a^2 = 100$):

$R_{02} = 0.4/100 = \boxed{0.004\,\Omega}$, $X_{02} = 1.131/100 = \boxed{0.01131\,\Omega}$

---

## ⚡ Exam Tips & Common Mistakes

1. **SC test gives copper loss, not iron loss.** $W_{sc} = P_{Cu,FL}$. At such low voltage, core flux is negligible, so iron loss ≈ 0.
2. **The ammeter must read rated current.** If it reads something else, the copper loss must be scaled: $P_{Cu,FL} = W_{sc} \times (I_{rated}/I_{sc})^2$.
3. **Check that $R_{01} < Z_{01}$.** If $R > Z$, your calculation is wrong.
4. **Don't forget to identify which side each test was done on.** OC → usually LV. SC → usually HV. Parameters are referred to the test side. To convert, use $a^2$.
5. **Copper loss scales with $x^2$.** At half load: $P_{Cu} = 0.25 \times P_{Cu,FL}$. At 75% load: $P_{Cu} = 0.5625 \times P_{Cu,FL}$.

## 🔗 Related Topics

- [T-06a: OC Test](T-06a_OC_Test.md) — The companion test for shunt parameters
- [T-06c: Efficiency](T-06c_Efficiency.md) — Uses both $P_{Fe}$ and $P_{Cu,FL}$
- [T-05: Voltage Regulation](T-05_Voltage_Regulation.md) — Uses $R_{01}$ and $X_{01}$
- [T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) — The circuit model

---

[← T-06a: OC Test](T-06a_OC_Test.md) | [🏠 Index](00_Index.md) | [T-06c: Efficiency →](T-06c_Efficiency.md)
