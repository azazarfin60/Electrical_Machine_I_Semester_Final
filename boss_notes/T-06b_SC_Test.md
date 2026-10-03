[← T-06a: OC Test](T-06a_OC_Test.md) | [🏠 Index](00_Index.md) | [T-06c: Efficiency →](T-06c_Efficiency.md)

---

# T-06b: Short-Circuit (SC) Test
> **Section:** A | **Priority:** 🔴 MUST | **Exam Frequency:** 7/7 years
> **Sources:** Theraja Ch-32 (Art. 32.26–32.28), VK Mehta Ch-7 (Art. 7.20), Slides L-10 S18

## Why This Topic Matters

The SC test always appears together with the OC test. ALL 7 papers include an OC/SC numerical. The SC test determines the series branch parameters ($R_{01}$, $X_{01}$, $Z_{01}$) and the full-load copper loss. These parameters are then used to calculate voltage regulation and efficiency. In 2024 a new conceptual question appeared: "In performing the short circuit test of a transformer, HV side is usually short circuited — explain it." (2024 Q4(a), 2 marks)

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

**Problem:** A 50 KVA, 2200/110 V transformer when tested gave the following results:
> **O.C. test (L. V. side):** 400W, 10A, 110V
> **S.C. test (H. V. side):** 808W, 20.5A, 90V

Compute all the parameters of the equivalent circuit referred to the H. V. side.

> **Appeared:** 2024 Q2(c) — 4 marks

### Step 1: Identify Sides

- Turns ratio: $a = 2200/110 = 20$
- OC test was done on LV (110 V) side
- SC test was done on HV (2200 V) side

### Step 2: OC Test → Shunt Parameters

$$\cos\phi_0 = \frac{W_0}{V_0 I_0} = \frac{400}{110 \times 10} = 0.36364$$

$$I_w = 10 \times 0.36364 = 3.636 \text{ A}$$

$$I_m = \sqrt{10^2 - 3.636^2} = 9.3156 \text{ A}$$

Referred to LV side:

$$R_{0,LV} = \frac{110}{3.636} = \boxed{30.25\,\Omega}, \qquad X_{0,LV} = \frac{110}{9.3156} = \boxed{11.807\,\Omega}$$

Iron loss: $P_{Fe} = W_0 = 400$ W

### Step 3: Refer the Shunt Branch to HV ($\times a^2 = 400$)

$$\boxed{R_0 = 12100\,\Omega}, \qquad \boxed{X_0 = 4723\,\Omega}$$

### Step 4: SC Test → Series Parameters (already on the HV side)

$$Z_{eq} = \frac{V_{sc}}{I_{sc}} = \frac{90}{20.5} = \boxed{4.3902\,\Omega}$$

$$R_{eq} = \frac{W_{sc}}{I_{sc}^2} = \frac{808}{20.5^2} = \frac{808}{420.25} = \boxed{1.9227\,\Omega}$$

$$X_{eq} = \sqrt{4.3902^2 - 1.9227^2} = \sqrt{19.28 - 3.70} = \boxed{3.9468\,\Omega}$$

### Step 5: The Trap — scale the copper loss to full load

Rated currents: $I_{rated,HV} = 50000/2200 = 22.727$ A and $I_{rated,LV} = 50000/110 = 454.55$ A.

The S.C. test ran at only 20.5 A, not at rated current, so 808 W is **not** the full-load copper loss:

$$P_{Cu,FL} = 808 \times \left(\frac{22.727}{20.5}\right)^2 = 808 \times 1.2287 = \boxed{993\text{ W}}$$

Total loss at full load:
$$P_{loss,FL} = P_{Fe} + P_{Cu,FL} = 400 + 993 = 1393\text{ W}$$

> [!IMPORTANT] Say this out loud in the exam
> $R_{eq} = 1.9227\,\Omega$ is still correct, because it comes from the test's own $V$ and $I$. But any **loss** figure taken straight from 808 W is understated. Examiners look for the scaling.

### Step 6: Final Answer

Equivalent circuit referred to the HV side:

| Branch | Parameter | Value |
|:---|:---|---:|
| Shunt (excitation) | $R_0$ | $12100\,\Omega$ |
| Shunt (excitation) | $X_0$ | $4723\,\Omega$ |
| Series | $R_{eq}$ | $1.9227\,\Omega$ |
| Series | $X_{eq}$ | $3.9468\,\Omega$ |
| Series | $Z_{eq}$ | $4.3902\,\Omega$ |
| Loss | $P_{Fe}$ | $400$ W |
| Loss | $P_{Cu,FL}$ | $993$ W |

---

## Exam Variants — The OC/SC Numerical Bank

| Year | Transformer | OC Data | SC Data | Asked For |
|:---|:---|:---|:---|:---|
| 2017 Q6(c) | 500 kVA, 2300/208V | 208V, 85A, 1800W | 95V, 217.4A, 8200W | $R_{02}$, parameters |
| 2018 Q2(b) | 10 kVA, 11kV/230V | 220V, 1.5A, 200W | 120V, rated I, 300W | η at FL/HL |
| 2019 Q2(c) | 10 kVA, 2200/220V | 220V, 1.5A, 153W | 115V, rated I, 224W | η at FL/HL |
| 2020 Q2(c) | Draw circuits | — | — | Circuit diagrams |
| 2021 Q2(c) | 20 kVA, 2400/240V | — | 72V, rated I, 275W | $R_{01}$, $X_{01}$, VR |
| 2023 Q2(b) | 10 kVA, 450/120 V | 120V, 4.2A, 80W (LV) | 9.65V, 22.2A, 120W (LV shorted) | Eq. constants + η + VR |
| 2024 Q2(c) | 50 kVA, 2200/110 V | 400W, 10A, 110V (LV) | 808W, 20.5A, 90V (HV) | Eq. circuit referred to HV |

> [!IMPORTANT]
> **Memorize this procedure. It is worth 5–10 marks in EVERY exam.** The data changes but the steps are identical every time.

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Given OC and SC test data, find equivalent circuit parameters, efficiency, and voltage regulation.
> **Appeared:** 2017 Q6(c) — 5 marks, 2018 Q2(b) — 6 marks, 2019 Q2(c) — 5 marks, 2021 Q2(c) — 4 marks, 2023 Q2(b) — 4 marks, 2024 Q2(c) — 4 marks

**Full Answer:**

The procedure is always the same 5-step method. See the [Complete Worked Example above](#combined-oc--sc-test-complete-worked-example-pyq-2024) for the full solution template using the 2024 data. For any other year's data, substitute the numbers into the same formulas. **Note:** 2023 Q2(b) also asks for efficiency and voltage regulation, so add those two final steps.

**Step 1:** Identify which side each test was done on. OC test is usually on LV. SC test is usually on HV. Compute $a = V_1/V_2$.

**Step 2 (OC test):** $P_{Fe} = W_0$. Then $\cos\phi_0 = W_0/(V_0 I_0)$. Then $I_w = I_0\cos\phi_0$, $I_\mu = I_0\sin\phi_0$. Finally $R_c = V_0/I_w$ and $X_m = V_0/I_\mu$. To refer to other side: multiply by $a^2$.

**Step 3 (SC test):** $P_{Cu,FL} = W_{sc}$. Then $R_{01} = W_{sc}/I_{sc}^2$, $Z_{01} = V_{sc}/I_{sc}$, $X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$.

**Step 4 (Efficiency):** $\eta = xS\cos\phi / (xS\cos\phi + P_{Fe} + x^2 P_{Cu,FL})$

**Step 5 (VR):** $\text{VR\%} = I_1(R_{01}\cos\phi \pm X_{01}\sin\phi)/V_1 \times 100$

---

### 🎯 Q2: In performing the short circuit test of a transformer, HV side is usually short circuited — explain it.
> **Appeared:** 2024 Q4(a) — 2 marks

**Full Answer:**

**Read the question carefully: it asks why the *other* winding is short-circuited during the SC test, and why the instruments are placed on the HV winding.**

**Why short-circuit the secondary:** a transformer cannot be tested on open circuit at reduced voltage and still give useful results. With the secondary shorted, the rated current is limited by the transformer's own small leakage impedance instead of being blocked, so only 5–10% of rated voltage is needed to circulate full-load current. With the secondary open, almost no current would flow at a safe voltage.

**Why put the instruments on the HV side:**

1. **Lower current.** Rated current is much smaller on the HV winding, so the ammeter and the wattmeter current coil carry far less current.
2. **Larger, more readable voltage.** $V_{sc}$ is 5–10% of a high rated voltage, easier to measure accurately than a few volts on the LV side.
3. **Higher referred impedance.** The HV side impedance is $a^2$ times the LV side, giving a better signal-to-error ratio.

**Why short-circuiting is safe.** The core flux at 5–10% of rated voltage is only a few percent of normal, so the iron loss is negligible and the core cannot saturate. All the wattmeter reading is copper loss.

---

### 🎯 Q3: 2023 variant — 10-kVA, 450/120 V transformer, OC on LV and SC on LV-shorted side. Compute equivalent circuit constants, efficiency and voltage regulation at 0.8 pf lag.
> **Appeared:** 2023 Q2(b) — 4 marks

**Full Answer:**

Given: **O.C. test** $V_1 = 120$ V, $I_1 = 4.2$ A, $W_1 = 80$ W (read on the LV side).
**S.C. test** $V_1 = 9.65$ V, $I_1 = 22.2$ A, $W_1 = 120$ W (LV winding short circuited).

**Which side is which.** Rated HV current $= 10000/450 = 22.2$ A and rated LV current $= 10000/120 = 83.3$ A. The S.C. reading of 22.2 A is therefore the HV (450 V, primary) side. The O.C. test is on the LV (120 V) side.

**(i) Equivalent circuit constants**

O.C. test (shunt branch, LV side):
$$\cos\phi_0 = \frac{80}{120 \times 4.2} = 0.159, \qquad I_w = 0.667\text{ A}, \qquad I_\mu = 4.147\text{ A}$$
$$R_0' = \frac{120}{0.667} = 180\ \Omega, \qquad X_0' = \frac{120}{4.147} = 28.9\ \Omega$$

Refer to the primary with $a = 450/120 = 3.75$, $a^2 = 14.06$:
$$R_0 = 180 \times 14.06 = \boxed{2525\ \Omega}, \qquad X_0 = 28.9 \times 14.06 = \boxed{406\ \Omega}$$
Iron loss $P_i = 80$ W.

S.C. test (series branch, referred to primary):
$$Z_{01} = \frac{9.65}{22.2} = \boxed{0.435\ \Omega}, \qquad R_{01} = \frac{120}{22.2^2} = \boxed{0.243\ \Omega}, \qquad X_{01} = \sqrt{0.435^2 - 0.243^2} = \boxed{0.361\ \Omega}$$
Full-load copper loss $P_{Cu} = 120$ W.

**(ii) Efficiency and voltage regulation at 0.8 pf lag**

$$\text{Output} = 10000 \times 0.8 = 8000\text{ W}, \qquad \eta = \frac{8000}{8000 + 80 + 120} = \boxed{97.56\%}$$

$$\text{Drop} = 22.2\,(0.243 \times 0.8 + 0.361 \times 0.6) = 22.2 \times 0.4112 = 9.13\text{ V}, \qquad \%\text{Reg} = \frac{9.13}{450} \times 100 = \boxed{2.03\%}$$

---

### 🎯 Q4: 2024 variant — 50 kVA, 2200/110 V. OC on LV (400 W, 10 A, 110 V), SC on HV (808 W, 20.5 A, 90 V). All equivalent circuit parameters referred to the HV side.
> **Appeared:** 2024 Q2(c) — 4 marks

**Full Answer:**

See [the complete worked example above](#combined-oc--sc-test-complete-worked-example-pyq-2024). Summary:

$$R_0 = 12100\ \Omega, \quad X_0 = 4723\ \Omega, \quad R_{eq} = 1.9227\ \Omega, \quad X_{eq} = 3.9468\ \Omega$$

And the mark-winning step, the copper-loss scaling:
$$P_{Cu,FL} = 808 \times \left(\frac{22.727}{20.5}\right)^2 = \boxed{993\text{ W}} \quad \text{(not 808 W)}$$

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
