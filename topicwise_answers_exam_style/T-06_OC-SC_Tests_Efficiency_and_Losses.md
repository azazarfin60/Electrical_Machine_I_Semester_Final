[← T-05: Voltage Regulation](T-05_Voltage_Regulation.md) | [🏠 Index](README.md) | [T-07: 3-Phase & Open-Delta →](T-07_Three-Phase_Connections_and_Open-Delta.md)

---

# T-06: OC-SC Tests, Efficiency & Losses

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **OC-SC Tests, Efficiency & Losses** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2017 Q5(c)]
> 📋 **Appeared in:** 2017 Q5(c)

**(c) 25 kVA, 2000/200V transformer, iron loss = 350W, full-load Cu loss = 400W. Find efficiency. [04]**

**Full-load VA:** 25000 VA, **$P_{Fe}$** = 350 W, **$P_{Cu,FL}$** = 400 W

**At full load:**

**(i) Unity pf ($\cos\phi = 1.0$):**
$$\eta = \frac{25000 \times 1.0}{25000 \times 1.0 + 350 + 400} = \frac{25000}{25750} = \boxed{97.09\%}$$

**(ii) 0.8 lagging pf:**
$$\eta = \frac{25000 \times 0.8}{25000 \times 0.8 + 350 + 400} = \frac{20000}{20750} = \boxed{96.39\%}$$

**At half load:** Cu loss at half load $= (0.5)^2 \times 400 = 100$ W

**(i) Half load, unity pf:**
$$\eta = \frac{12500 \times 1.0}{12500 + 350 + 100} = \frac{12500}{12950} = \boxed{96.53\%}$$

**(ii) Half load, 0.8 lagging pf:**
$$\eta = \frac{12500 \times 0.8}{12500 \times 0.8 + 350 + 100} = \frac{10000}{10450} = \boxed{95.69\%}$$

---

### [2017 Q6(b)]
> 📋 **Appeared in:** 2017 Q6(b)

**(b) Short notes on: (i) Hysteresis loss (ii) Eddy current loss [04]**

**(i) Hysteresis loss:**
When the core is subjected to alternating magnetic flux, the magnetic domains in the iron reverse direction each half-cycle. Energy is spent overcoming the molecular friction during this reversal. This energy appears as heat. It is called hysteresis loss.

$$P_h = K_h f B_m^{1.6} V \text{ (Steinmetz formula)}$$

where $K_h$ = material constant, $f$ = frequency, $B_m$ = peak flux density, $V$ = core volume. Reduced by using high-grade silicon steel (low $K_h$).

**(ii) Eddy current loss:**
The alternating core flux also induces EMFs in the iron core itself. These EMFs drive circulating currents (eddy currents) within the iron. These currents cause $I^2R$ heating.

$$P_e = K_e f^2 B_m^2 t^2 V$$

where $t$ = lamination thickness. Reduced by laminating the core (thin sheets insulated from each other). Each lamination has higher resistance, so eddy currents are small.

---

### [2017 Q6(c)]
> 📋 **Appeared in:** 2017 Q6(c)

**(c) 2300/208V, 500 kVA, 50 Hz. OC test (LV side): 208V, 85A, 1800W. SC test (HV side): 95V, 217.4A, 8200W. Find $R_{02}$ and other parameters. [05]**

**OC Test (LV side = secondary, 208V):**

$$\cos\phi_0 = \frac{W_0}{V_0 I_0} = \frac{1800}{208 \times 85} = 0.1018$$

$$R_{c2} = \frac{V_0^2}{W_0} = \frac{208^2}{1800} = 24.04\,\Omega$$

$$I_m = I_0 \sin\phi_0 = 85 \times \sqrt{1 - 0.1018^2} = 84.52 \text{ A}$$

$$X_{m2} = \frac{V_0}{I_m} = \frac{208}{84.52} = 2.46\,\Omega$$

**SC Test (HV side = primary):**

Turns ratio: $a = 2300/208 = 11.06$

$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{8200}{217.4^2} = 0.173\,\Omega$$

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{95}{217.4} = 0.437\,\Omega$$

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2} = \sqrt{0.437^2 - 0.173^2} = \sqrt{0.191 - 0.030} = 0.401\,\Omega$$

Referring to LV side (divide by $a^2 = 122.3$):

$$\boxed{R_{02} = \frac{R_{01}}{a^2} = \frac{0.173}{122.3} = 1.414 \times 10^{-3}\,\Omega}$$

$$X_{02} = \frac{X_{01}}{a^2} = \frac{0.401}{122.3} = 3.28 \times 10^{-3}\,\Omega$$

$$Z_{02} = \frac{Z_{01}}{a^2} = \frac{0.437}{122.3} = 3.57 \times 10^{-3}\,\Omega$$

---

### [2018 Q1(d)]
> 📋 **Appeared in:** 2018 Q1(d)

**(d) 50 Hz, 20 kVA, 11kV/230V transformer. SC test (HV side): $V = 72$ V, $I =$ rated, $W = 300$ W. Find constants and voltage regulation. [06]**

**Rated current (HV side):**
$$I_{1,\text{rated}} = \frac{\text{kVA} \times 1000}{V_{1,\text{rated}}} = \frac{20000}{11000} = 1.818 \text{ A}$$

**From SC test (HV side):**

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{72}{1.818} = 39.60\,\Omega$$

$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{300}{1.818^2} = \frac{300}{3.305} = 90.77\,\Omega$$

Wait: $R_{01}$ cannot exceed $Z_{01}$. Recheck: $I_{sc} = 1.818$ A, $R_{01} = 300/1.818^2 = 90.77\,\Omega$ and $Z_{01} = 39.60\,\Omega$. This is inconsistent. The actual rated current on the HV side:

Actually the problem states $I =$ rated. Let me recompute: Rated HV current $= 20000/11000 = 1.818$ A. With $W = 300$ W and $I = 1.818$ A:

$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{300}{(1.818)^2} = 90.8\,\Omega$$

But $Z_{01} = V_{sc}/I_{sc} = 72/1.818 = 39.6\,\Omega$. Since $R_{01} > Z_{01}$ this is impossible. The input data appears inconsistent in the original problem (a common issue with this paper). Assuming the problem intends the LV side to be shorted and values are per the HV side:

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{72}{1.818} = 39.60\,\Omega$$

$$R_{01} = \frac{P_{sc}}{I_{sc}^2} = \frac{300}{3.305} = 90.77\,\Omega$$

This is geometrically impossible. Using the problem from the same data as it appears in 2021 (same question), the rated current calculation gives:

Rated $I_{HV} = \frac{20000}{2400} = 8.33$ A (if it were a 2400V side). Let us proceed with the 2021 version (20kVA, 2400/240V):

$$I_{1,\text{rated}} = \frac{20000}{2400} = 8.33 \text{ A}, \quad V_{sc} = 72 \text{ V}, \quad W_{sc} = 275 \text{ W (2021 version)}$$

$$Z_{01} = \frac{72}{8.33} = 8.64\,\Omega, \quad R_{01} = \frac{275}{8.33^2} = \frac{275}{69.39} = 3.964\,\Omega$$

$$X_{01} = \sqrt{8.64^2 - 3.964^2} = \sqrt{74.65 - 15.71} = \sqrt{58.94} = 7.677\,\Omega$$

**Voltage regulation at 0.8 lagging pf:**
$$\epsilon_r = \frac{I_{sc}(R_{01}\cos\phi + X_{01}\sin\phi)}{V_{\text{rated}}} \times 100$$
$$= \frac{8.33(3.964 \times 0.8 + 7.677 \times 0.6)}{2400} \times 100$$
$$= \frac{8.33(3.171 + 4.606)}{2400} \times 100 = \frac{8.33 \times 7.777}{2400} \times 100$$
$$= \frac{64.78}{2400} \times 100 = \boxed{2.70\%}$$

> **Note:** The original 2018 paper has inconsistent SC test data for the stated transformer. The calculation approach above is correct: use the same formula with whatever consistent data your exam paper provides.

---

### [2018 Q2(a)]
> 📋 **Appeared in:** 2018 Q2(a)

**(a) Define all-day efficiency of a transformer. [01]**

All-day efficiency is the ratio of total energy output (in kWh) to total energy input (in kWh) over a 24-hour period.

$$\eta_{\text{all-day}} = \frac{\text{Total kWh output in 24 hours}}{\text{Total kWh input in 24 hours}} \times 100\%$$

It accounts for the fact that a distribution transformer runs at partial load for most of the day. Iron losses run continuously (24 hours), but copper losses vary with load.

---

### [2018 Q2(b)]
> 📋 **Appeared in:** 2018 Q2(b)

**(b) 10 kVA, 11kV/230V, 50 Hz. OC test (HV open): 220V, 1.5A, 200W. SC test (LS short): 120V, rated I, 300W. Find efficiency at half-load and full-load at upf and 0.8 pf lag. [06]**

**From OC test:** $P_{Fe} = 200$ W (core loss, constant for all loads)

**From SC test:** Full-load Cu loss $P_{Cu,FL} = 300$ W

**At full load:**

**(i) Unity pf:**
$$\eta_{FL,1} = \frac{10000 \times 1.0}{10000 + 200 + 300} = \frac{10000}{10500} = \boxed{95.24\%}$$

**(ii) 0.8 pf lagging:**
$$\eta_{FL,0.8} = \frac{10000 \times 0.8}{10000 \times 0.8 + 200 + 300} = \frac{8000}{8500} = \boxed{94.12\%}$$

**At half load:** Cu loss at half load $= (0.5)^2 \times 300 = 75$ W

**(i) Unity pf:**
$$\eta_{HL,1} = \frac{5000 \times 1.0}{5000 + 200 + 75} = \frac{5000}{5275} = \boxed{94.79\%}$$

**(ii) 0.8 pf lagging:**
$$\eta_{HL,0.8} = \frac{5000 \times 0.8}{5000 \times 0.8 + 200 + 75} = \frac{4000}{4275} = \boxed{93.57\%}$$

---

### [2018 Q2(c)]
> 📋 **Appeared in:** 2018 Q2(c)

**(c) 100 kVA transformer. Core loss = 200W, Cu loss = 500W. Load profile: 2hr at 5/4 load; 6hr at full load; 8hr at half load; 4hr at 1/4 load; 4hr at no load. Find all-day efficiency. [05]**

**Energy output (kWh):**

| Condition | Load | Hours | kWh Output |
|:---|:---:|:---:|:---:|
| 5/4 load (125%) | 125 kW | 2 | 250 |
| Full load | 100 kW | 6 | 600 |
| Half load | 50 kW | 8 | 400 |
| 1/4 load | 25 kW | 4 | 100 |
| No load | 0 | 4 | 0 |
| **Total** | | **24** | **1350 kWh** |

**Iron losses (run 24 hours):**
$$P_{Fe} \times 24 = 200 \times 24 = 4800 \text{ Wh} = 4.8 \text{ kWh}$$

**Copper losses:**

| Condition | Cu loss | Hours | kWh |
|:---|:---:|:---:|:---:|
| 5/4 load | $(5/4)^2 \times 500 = 781.25$ W | 2 | 1.5625 |
| Full load | $500$ W | 6 | 3.0 |
| Half load | $(0.5)^2 \times 500 = 125$ W | 8 | 1.0 |
| 1/4 load | $(0.25)^2 \times 500 = 31.25$ W | 4 | 0.125 |
| No load | 0 | 4 | 0 |
| **Total Cu** | | | **5.6875 kWh** |

**Total losses** $= 4.8 + 5.6875 = 10.4875$ kWh

**Total input** $= 1350 + 10.4875 = 1360.49$ kWh

$$\boxed{\eta_{\text{all-day}} = \frac{1350}{1360.49} \times 100 = 99.23\%}$$

---

### [2019 Q2(a)]
> 📋 **Appeared in:** 2019 Q2(a)

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

### [2019 Q2(c)]
> 📋 **Appeared in:** 2019 Q2(c)

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

### [2019 Q3(a)]
> 📋 **Appeared in:** 2019 Q3(a)

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

### [2019 Q4(c)]
> 📋 **Appeared in:** 2019 Q4(c)

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

**Commercial efficiency** is output watts over input watts at rated load (Theraja Art. 32.32). At full load the losses are 3 kW iron plus 3 kW copper:

$$\boxed{\eta_{\text{commercial}} = \frac{100}{100 + 3 + 3} \times 100 = 94.34\%}$$

The 24-hour energy ratio is the **all-day efficiency**, a different quantity:

$$\eta_{\text{all-day}} = \frac{500}{584} \times 100 = 85.62\%$$

---

## SECTION - B (Induction Motors: Q5 to Q8)

---

### [2020 Q2(c)]
> 📋 **Appeared in:** 2020 Q2(c)

**(c) Draw circuit diagrams for OC and SC tests on a single-phase transformer. [02]**

**1. Open-Circuit (OC) / No-Load Test:**
- **Connections:** LV winding connected to rated supply voltage ($V_1$) via Voltmeter ($V$), Ammeter ($A$), and LPF Wattmeter ($W$). HV winding is left **open-circuited**.
- **Yields:** Core loss ($W_0 \approx P_{core}$) and shunt branch parameters ($R_0, X_0$).

![Open-Circuit (OC) Test Circuit Diagram](diagrams/transformer_oc_test_circuit.png)

**2. Short-Circuit (SC) / Impedance Test:**
- **Connections:** LV winding is **solidly short-circuited** with a thick conductor strip. Reduced AC voltage ($5\text{--}10\%$ rated) is applied to HV winding via a Variac until rated current ($I_{sc}$) circulates.
- **Yields:** Full-load copper loss ($W_{sc} \approx P_{cu}$) and equivalent series impedance ($R_{01}, X_{01}, Z_{01}$).

![Short-Circuit (SC) Test Circuit Diagram](diagrams/transformer_sc_test_circuit.png)

---

### [2020 Q2(d)]
> 📋 **Appeared in:** 2020 Q2(d)

**(d) No-load test: Primary = 220V, Secondary = 110V, $I_0 = 0.5$ A, Power = 30W. Find: (i) magnetizing current, (ii) loss component, (iii) iron loss. [03]**

*(Same as Q1(d) above: identical data and method.)*

$$P_{Fe} = 30 \text{ W}, \quad I_c = 0.136 \text{ A}, \quad I_m = 0.481 \text{ A}$$

---

### [2021 Q2(b)]
> 📋 **Appeared in:** 2021 Q2(b)

**(b) Explain the procedure of the no-load test of a transformer. Why is this test performed? [04]**

**Procedure:**
1. Keep secondary (HV) side open-circuited.
2. Apply rated voltage to the primary (LV) side via a variac.
3. Connect measuring instruments on the primary side: voltmeter ($V_0$), ammeter ($I_0$), wattmeter ($W_0$).
4. Record readings when supply reaches rated value: $V_0 = V_{\text{rated}}$, $I_0$, $W_0$.

**Calculations:**

Core loss: $P_{Fe} = W_0$ (constant, independent of load)

$$\cos\phi_0 = \frac{W_0}{V_0 I_0}, \quad I_c = I_0\cos\phi_0, \quad I_m = I_0\sin\phi_0$$

$$R_c = \frac{V_0}{I_c}, \quad X_m = \frac{V_0}{I_m}$$

Turns ratio check: $a = V_1/V_2$ (measure both voltages)

**Why this test is performed:**
1. To measure core (iron) losses: constant at all loads.
2. To determine shunt branch parameters ($R_c$ and $X_m$) of the equivalent circuit.
3. To verify the turns ratio.
4. To calculate no-load current and power factor.

The test is economical: rated voltage is applied but rated current does not flow (only 2–10%). Power consumption during the test is low.

---

### [2021 Q2(c)]
> 📋 **Appeared in:** 2021 Q2(c)

**(c) 20 kVA, 2400/240V, 50 Hz transformer. SC test (HV side): $V = 72$ V, $W = 275$ W, $I =$ rated. Find constants referred to HV side and voltage regulation at 0.8 pf lag. [04]**

**Rated HV current:**
$$I_1 = \frac{20000}{2400} = 8.33 \text{ A}$$

**From SC test (HV side):**
$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{275}{8.33^2} = \frac{275}{69.39} = 3.964\,\Omega$$

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{72}{8.33} = 8.643\,\Omega$$

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2} = \sqrt{8.643^2 - 3.964^2} = \sqrt{74.70 - 15.71} = \sqrt{58.99} = 7.681\,\Omega$$

**Voltage regulation at 0.8 pf lag ($\cos\phi = 0.8$, $\sin\phi = 0.6$):**
$$\text{VR\%} = \frac{I_1(R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100$$

$$= \frac{8.33(3.964 \times 0.8 + 7.681 \times 0.6)}{2400} \times 100$$

$$= \frac{8.33(3.171 + 4.609)}{2400} \times 100 = \frac{8.33 \times 7.780}{2400} \times 100$$

$$= \frac{64.81}{2400} \times 100 = \boxed{2.70\%}$$

---

### [2023 Q2(a)]
> 📋 **Appeared in:** 2023 Q2(a)

**(a) Define power transformer. Prove that, the efficiency of a transformer will be maximum when copper loss is equal to iron loss. [CO2, Marks: 03]**

**Power transformer.** A large, high-rating static transformer used in generating stations and transmission substations to step voltage up or down at bulk power levels. It runs near full load for most of the day, is designed for the highest possible full-load efficiency, and is usually oil-immersed with forced cooling.

![Transformer efficiency curve against load, peaking where copper loss equals iron loss](../Books/Theraja/Ch-32/diagrams/Ch-32_p56_fig56.jpg)

**Proof.** Let the secondary carry current $I_2$ at terminal voltage $V_2$ and power factor $\cos\phi$. Let $P_i$ be the iron loss and $R_{02}$ the total resistance referred to the secondary.

$$\eta = \frac{V_2 I_2 \cos\phi}{V_2 I_2 \cos\phi + P_i + I_2^2 R_{02}}$$

Divide numerator and denominator by $I_2$:
$$\eta = \frac{V_2 \cos\phi}{V_2 \cos\phi + \dfrac{P_i}{I_2} + I_2 R_{02}}$$

$V_2$ and $\cos\phi$ are held constant, so $\eta$ is maximum when the denominator is minimum:
$$\frac{d}{dI_2}\left(\frac{P_i}{I_2} + I_2 R_{02}\right) = 0 \implies -\frac{P_i}{I_2^2} + R_{02} = 0$$
$$\therefore\ I_2^2 R_{02} = P_i$$

$$\boxed{\text{Copper loss} = \text{Iron loss at maximum efficiency}}$$

The second derivative is $2P_i/I_2^3 > 0$, so this is a true minimum of the loss term and a maximum of $\eta$.

**Load at which it happens.** If $P_{Cu,FL}$ is the full-load copper loss, the load fraction $x$ for maximum efficiency is $x = \sqrt{P_i/P_{Cu,FL}}$.

---

### [2023 Q2(b)]
> 📋 **Appeared in:** 2023 Q2(b)

**(b) The corrected instrument readings obtained from open and short-circuit tests on 10-kVA, 450/120 V, 50-Hz transformer are: [CO3, Marks: 04]**
> **O.C. test:** $V_1 = 120\text{ V}; \ I_1 = 4.2\text{ A}; \ W_1 = 80\text{ W}$ (read on the low voltage side).
> **S.C. test:** $V_1 = 9.65\text{ V}; \ I_1 = 22.2\text{ A}; \ W_1 = 120\text{ W}$ (with low-voltage winding short circuited).
>
> Compute **(i)** equivalent circuit constants, **(ii)** efficiency and voltage regulation for an 80% lagging p.f. load.

**Which side is which.** Rated HV current $= 10000/450 = 22.2\text{ A}$ and rated LV current $= 10000/120 = 83.3\text{ A}$. The S.C. reading of 22.2 A is therefore the HV (450 V, primary) side. The O.C. test is on the LV (120 V) side.

![Open-circuit test circuit: low voltage winding energised at rated voltage with wattmeter, ammeter and voltmeter, high voltage winding left open](diagrams/transformer_oc_test_circuit.png)

![Short-circuit test circuit: reduced voltage applied to the high voltage winding with the low voltage winding shorted, wattmeter reading full-load copper loss](diagrams/transformer_sc_test_circuit.png)

#### (i) Equivalent circuit constants

**From the O.C. test (shunt branch, LV side):**
$$\cos\phi_0 = \frac{80}{120 \times 4.2} = 0.159, \qquad \sin\phi_0 = 0.987$$
$$I_w = 4.2 \times 0.159 = 0.667\text{ A}, \qquad I_\mu = 4.2 \times 0.987 = 4.147\text{ A}$$
$$R_0' = \frac{120}{0.667} = 180\ \Omega, \qquad X_0' = \frac{120}{4.147} = 28.9\ \Omega \quad \text{(LV side)}$$

Refer to the primary with $a = 450/120 = 3.75$, so $a^2 = 14.06$:
$$\boxed{R_0 = 180 \times 14.06 = 2531\ \Omega \approx 2525\ \Omega, \qquad X_0 = 28.9 \times 14.06 = 407\ \Omega \approx 406\ \Omega}$$

Iron loss $P_i = 80\text{ W}$.

**From the S.C. test (series branch, referred to primary):**
$$Z_{01} = \frac{9.65}{22.2} = 0.435\ \Omega$$
$$R_{01} = \frac{120}{22.2^2} = \frac{120}{492.8} = 0.243\ \Omega$$
$$X_{01} = \sqrt{0.435^2 - 0.243^2} = \sqrt{0.1892 - 0.0590} = 0.361\ \Omega$$

$$\boxed{R_{01} = 0.243\ \Omega, \quad X_{01} = 0.361\ \Omega, \quad Z_{01} = 0.435\ \Omega}$$

Full-load copper loss $P_{Cu} = 120\text{ W}$.

![Approximate equivalent circuit referred to the primary, with the exciting branch at the input terminals and R01, X01 in series](diagrams/tx_step5_approximate_referred_to_primary.png)

#### (ii) Efficiency and voltage regulation at 80% lagging p.f.

**Efficiency (full load):**
$$\text{Output} = 10000 \times 0.8 = 8000\text{ W}, \qquad \text{Total loss} = 80 + 120 = 200\text{ W}$$
$$\eta = \frac{8000}{8000 + 200} \times 100\%$$

$$\boxed{\eta = 97.56\%}$$

**Voltage regulation.** Full-load primary current $I_1 = 10000/450 = 22.2$ A, $\cos\phi = 0.8$, $\sin\phi = 0.6$:
$$\text{Drop} = 22.2\,(0.243 \times 0.8 + 0.361 \times 0.6) = 22.2 \times 0.4112 = 9.13\text{ V}$$
$$\%\text{Reg} = \frac{9.13}{450} \times 100\%$$

$$\boxed{\text{Voltage regulation} = 2.03\% \ \text{(lagging, so it is a voltage drop)}}$$

> [!info] Cross-check
> Working on the LV side instead gives $R_{02} = 0.0173\ \Omega$, $X_{02} = 0.0256\ \Omega$, $I_2 = 83.3\text{ A}$, drop $= 2.43\text{ V}$ out of 120 V, which is the same 2.03%.

---

### [2023 Q3(b)]
> 📋 **Appeared in:** 2023 Q3(b)

**(b) Define all day efficiency of a transformer. A 100-kVA lighting transformer has a full-load loss of 3 kW, the losses being equally divided between iron and copper. During a day, the transformer operates on full load for 3 hours, one-half load for 4 hours, the output being negligible for the remainder of the day. Calculate the all day efficiency. [CO3, Marks: 04]**

**Definition.** All-day (or energy) efficiency is the ratio of energy output in kWh to energy input in kWh over 24 hours:
$$\eta_{\text{all-day}} = \frac{\text{kWh output in 24 h}}{\text{kWh output} + \text{kWh iron loss} + \text{kWh copper loss}}$$

It is used for distribution transformers, which stay energised all day but are loaded only part of the day. The iron loss then runs for 24 hours while the copper loss runs only while loaded.

![Transformer losses plotted against load, showing constant iron loss and load-dependent copper loss](../Books/Theraja/Ch-32/diagrams/Ch-32_p54_losses_vs_load.jpg)

**Given:** 100 kVA, full-load loss $= 3\text{ kW}$ shared equally, so $P_{Fe} = P_{Cu,FL} = 1.5\text{ kW}$. A lighting load is treated as unity power factor, so 100 kVA gives 100 kW.

**Step 1. Energy output in 24 h.**

| Period | Load | Output (kW) | Hours | kWh |
|:---|:---|---:|---:|---:|
| Full load | 100% | 100 | 3 | 300 |
| Half load | 50% | 50 | 4 | 200 |
| Rest | negligible | 0 | 17 | 0 |
| **Total** | | | **24** | **500** |

$$\text{Output} = 300 + 200 = 500\text{ kWh}$$

**Step 2. Iron loss for the full 24 hours.** The transformer stays energised, so
$$\text{kWh}_{Fe} = 1.5 \times 24 = 36\text{ kWh}$$

**Step 3. Copper loss, which follows the square of load.**
$$\text{kWh}_{Cu} = \underbrace{1.5 \times 3}_{\text{full load}} + \underbrace{1.5 (0.5)^2 \times 4}_{\text{half load}} = 4.5 + 0.375 \times 4 = 4.5 + 1.5 = 6\text{ kWh}$$

**Step 4. All-day efficiency.**
$$\eta_{\text{all-day}} = \frac{500}{500 + 36 + 6} = \frac{500}{542}$$

$$\boxed{\eta_{\text{all-day}} = 92.25\%}$$

> [!info] Why it is so much lower than full-load efficiency
> At full load, $\eta = 100/(100+1.5+1.5) = 97.1\%$. Over the day the 36 kWh of iron loss dominates, because the transformer is magnetised for 24 hours but delivers useful output for only 7 of them.

---

### [2024 Q2(c)]
> 📋 **Appeared in:** 2024 Q2(c)

**(c) A 50 KVA, 2200/110 V transformer when tested gave the following results: [Marks: 04, CO: 2]**
> **O.C. test (L. V. side):** 400W, 10A, 110V
> **S.C. test (H. V. side):** 808W, 20.5A, 90V
>
> Compute all the parameters of the equivalent circuit referred to the H. V. side.

Ratio $a = 2200/110 = 20$.

**O.C. test (excitation branch, LV side):**
$$\cos\phi_0 = \frac{400}{110 \times 10} = 0.36364$$
$$I_w = 10 \times 0.36364 = 3.636\text{ A}, \qquad I_m = \sqrt{10^2 - 3.636^2} = 9.3156\text{ A}$$
$$R_0(\text{LV}) = \frac{110}{3.636} = 30.25\ \Omega, \qquad X_0(\text{LV}) = \frac{110}{9.3156} = 11.807\ \Omega$$
Iron loss $= 400\text{ W}$

**Referred to HV ($\times a^2 = 400$):**
$$\boxed{R_0(\text{HV}) = 12100\ \Omega, \qquad X_0(\text{HV}) = 4723\ \Omega}$$

**S.C. test (series branch, HV side):**
$$Z_{eq}(\text{HV}) = \frac{90}{20.5} = 4.3902\ \Omega$$
$$R_{eq}(\text{HV}) = \frac{808}{20.5^2} = \frac{808}{420.25} = 1.9227\ \Omega$$
$$X_{eq}(\text{HV}) = \sqrt{4.3902^2 - 1.9227^2} = 3.9468\ \Omega$$

Rated currents: $I_{\text{rated}}(\text{HV}) = 50000/2200 = 22.727$ A; $I_{\text{rated}}(\text{LV}) = 50000/110 = 454.55$ A.

> [!IMPORTANT] The trap in this question
> The S.C. reading is **20.5 A**, but rated HV current is **22.73 A**. So the full-load copper loss must be scaled:
> $$P_{cu,FL} = 808 \times \left(\frac{22.727}{20.5}\right)^2 = 808 \times 1.2287 = \boxed{993\text{ W}}$$
> $R_{eq}$ is still correct at 1.9227 $\Omega$, because it comes from the test's own $V$ and $I$. But any loss figure taken straight from 808 W is understated. Total loss at full load $= 400 + 993 = 1393$ W.

---

### [2024 Q3(c)]
> 📋 **Appeared in:** 2024 Q3(c)

**(c) In no-load test of single-phase transformer, the following test data were obtained: [Marks: 04, CO: 2]**
> Resistance of primary winding $= 0.6\ \Omega$; Primary voltage: 220 V; Secondary voltage: 110 V; Primary current: 0.5 A; Power input: 30 W
>
> Find: **(i)** turn ratio, **(ii)** magnetizing component of no-load current, **(iii)** working (or loss) component, **(iv)** iron loss.

**(i) Turn ratio**
$$a = \frac{V_1}{V_2} = \frac{220}{110} = \boxed{2}$$

**(ii) Magnetizing component of $I_0$**

The working component first (it is the one used to find $I_m$):
$$\cos\phi_0 = \frac{W_0}{V_1 I_0} = \frac{30}{220 \times 0.5} = \frac{30}{110} = 0.2727, \qquad \phi_0 = 74.17°$$
$$I_m = I_0 \sin\phi_0 = 0.5 \times 0.9621 = \boxed{0.481\text{ A}}$$

**(iii) Working (loss) component**
$$I_w = I_0 \cos\phi_0 = 0.5 \times 0.2727 = \boxed{0.1364\text{ A}}$$

**(iv) Iron loss**

The wattmeter reads power **input**, which is iron loss plus the small primary copper loss:
$$P_{core} = W_0 - I_0^2 R_1 = 30 - (0.5^2 \times 0.6) = 30 - 0.15 = \boxed{29.85\text{ W}}$$

> [!NOTE] The intended answer for (iv)
> The paper supplies $R_1 = 0.6\ \Omega$ precisely so that the answer is **29.85 W**, not the usual approximation 30 W. State 29.85 W as the answer and add that 30 W is the usual approximation.

Optional shunt branch: $R_0 = 220/0.13636 = 1613.3\ \Omega$, $X_0 = 220/0.48105 = 457.3\ \Omega$.

---

### [2024 Q4(a)]
> 📋 **Appeared in:** 2024 Q4(a)

**(a) In performing the short circuit test of a transformers, HV side is usually short circuited — explain it. [Marks: 02, CO: 2]**

**Read the question carefully: it asks why the *other* winding is short-circuited during the SC test, and why the instruments are placed on the HV winding.**

A transformer cannot be tested on open circuit at reduced voltage and still give useful results. In the SC test the secondary (LV) winding is **short-circuited** so that:
1. The rated current is limited by the transformer's own small leakage impedance instead of being blocked. With the secondary open, almost no current could be made to flow at a safe voltage.
2. The test then only has to raise the applied voltage to about 5-10% of rated to circulate full-load current.

**Why the instruments go on the HV side:**
1. **Lower current.** Rated current is much smaller on the HV winding, so the ammeter and the wattmeter current coil carry far less current.
2. **Larger, more readable voltage.** $V_{sc}$ is 5-10% of a high rated voltage, easier to measure accurately than a few volts on the LV side.
3. **Higher referred impedance.** The HV side impedance is $a^2$ times the LV side, giving a better signal-to-error ratio.

**Why short-circuiting is safe.** The core flux at 5-10% of rated voltage is only a few percent of normal, so the iron loss is negligible and the core cannot saturate. All the wattmeter reading is copper loss.

---

[← T-05: Voltage Regulation](T-05_Voltage_Regulation.md) | [🏠 Index](README.md) | [T-07: 3-Phase & Open-Delta →](T-07_Three-Phase_Connections_and_Open-Delta.md)
