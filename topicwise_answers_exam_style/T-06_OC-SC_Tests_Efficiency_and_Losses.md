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

$$\boxed{\eta_{\text{commercial}} = \frac{500}{584} \times 100 = 85.62\%}$$

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

**(a) A 100 kVA transformer, iron loss = 1 kW, full-load Cu loss = 1 kW. Distribution transformer load profile: 4h no-load, 12h half load, 8h full load. Find all-day efficiency. [06, CO1]**

**Energy output (kWh):**

| Period | Output | Hours | kWh |
|:---|:---:|:---:|:---:|
| No-load | 0 kW | 4 | 0 |
| Half load (at upf) | 50 kW | 12 | 600 |
| Full load (at upf) | 100 kW | 8 | 800 |
| **Total** | | 24 | **1400 kWh** |

**Iron loss (24 hours, constant):**
$$W_{Fe} = 1 \times 24 = 24 \text{ kWh}$$

**Copper losses:**

| Period | Cu loss | Hours | kWh |
|:---|:---:|:---:|:---:|
| No-load | 0 | 4 | 0 |
| Half load | $(0.5)^2 \times 1 = 0.25$ kW | 12 | 3 |
| Full load | $1$ kW | 8 | 8 |
| **Total Cu** | | | **11 kWh** |

**Total losses** $= 24 + 11 = 35$ kWh

**Total input** $= 1400 + 35 = 1435$ kWh

$$\boxed{\eta_{\text{all-day}} = \frac{1400}{1435} \times 100 = 97.56\%}$$

---

### [2023 Q2(b)]
> 📋 **Appeared in:** 2023 Q2(b)

**(b) OC test (secondary open): 220V, 0.8A, 80W. SC test (primary short): 12V, 10A, 40W. Transformer rated 2.2kV/220V. Find the equivalent circuit parameters referred to the secondary. [06, CO1]**

**From OC test (secondary/LV side):**

$$\cos\phi_0 = \frac{W_0}{V_0 I_0} = \frac{80}{220 \times 0.8} = \frac{80}{176} = 0.4545$$

$$I_c = I_0\cos\phi_0 = 0.8 \times 0.4545 = 0.364 \text{ A}$$

$$I_m = I_0\sin\phi_0 = 0.8 \times \sqrt{1 - 0.4545^2} = 0.8 \times 0.8909 = 0.713 \text{ A}$$

Referred to secondary:
$$R_{c2} = \frac{V_0}{I_c} = \frac{220}{0.364} = \boxed{604.4\,\Omega}$$

$$X_{m2} = \frac{V_0}{I_m} = \frac{220}{0.713} = \boxed{308.6\,\Omega}$$

**From SC test (primary/HV side shorted):**

Turns ratio: $a = 2200/220 = 10$

Rated secondary current: $I_2 = $ rated → from SC test, $I_{sc} = 10$ A on secondary.

$$R_{02,sec} = \frac{W_{sc}}{I_{sc}^2} = \frac{40}{10^2} = \boxed{0.4\,\Omega}$$

$$Z_{02} = \frac{V_{sc}}{I_{sc}} = \frac{12}{10} = 1.2\,\Omega$$

$$X_{02} = \sqrt{Z_{02}^2 - R_{02}^2} = \sqrt{1.44 - 0.16} = \sqrt{1.28} = \boxed{1.131\,\Omega}$$

**Equivalent circuit referred to secondary:**
- Series: $R_{02} = 0.4\,\Omega$, $X_{02} = 1.131\,\Omega$
- Shunt: $R_{c2} = 604.4\,\Omega$, $X_{m2} = 308.6\,\Omega$

---

### [2024 Q3(a)]
> 📋 **Appeared in:** 2024 Q3(a)

**(a) Why are OC and SC tests preferred to direct load test for finding efficiency and voltage regulation of a transformer? [04, CO1]**

**Direct load test problems:**
1. Requires a full-rated load (resistive, inductive, or capacitive): difficult to arrange and expensive for large transformers.
2. The load must absorb the full kVA during the test.
3. Full losses must be supplied continuously. For a 500 kVA transformer, maintaining a full test for hours is costly and wasteful.
4. The test gives results only at one load condition.

**OC and SC test advantages:**
1. **Low power consumption:** OC test uses rated voltage but only no-load current (~2-10% of rated). SC test uses only ~5% of rated voltage. Power consumed is only the losses: orders of magnitude smaller.
2. **Economical:** No large load needed.
3. **Accurate:** Direct measurement of losses (core loss from OC, copper loss from SC). No estimation.
4. **Multiple results:** Using these parameters, efficiency and VR can be calculated for any load and any power factor without repeating the test.
5. **Safe:** No thermal stress from full-load currents sustained for long.

---

### [2024 Q3(b)]
> 📋 **Appeared in:** 2024 Q3(b)

**(b) 20 kVA, 2000/400V, OC test (HV open): 400V, 1.5A, 160W. SC test (LV short): 60V, rated I, 300W. Find: (i) parameters of equivalent circuit referred to HV side, (ii) efficiency and VR at full-load 0.8 pf lag. [08, CO1]**

**Turns ratio:** $a = 2000/400 = 5$

**Rated HV current:** $I_{1,\text{rated}} = 20000/2000 = 10$ A

**OC test (LV side = secondary, 400V):**

$$\cos\phi_0 = \frac{W_0}{V_0 I_0} = \frac{160}{400 \times 1.5} = \frac{160}{600} = 0.2667$$

$$I_c = 1.5 \times 0.2667 = 0.400 \text{ A}, \quad I_m = 1.5\sin(\cos^{-1}0.2667) = 1.5 \times 0.9638 = 1.446 \text{ A}$$

Referred to HV side ($\times a^2 = 25$):
$$R_{c1} = \frac{V_{0,HV}^2}{W_0} = \frac{2000^2}{160} = 25000\,\Omega$$

$$X_{m1} = \frac{V_{0,HV}}{I_{m,HV}} = \frac{2000}{1.446/5} = \frac{2000}{0.289} = 6920\,\Omega$$

(Or: $R_{c1} = a^2 R_{c,LV} = 25 \times (400^2/160) = 25 \times 1000 = 25000\,\Omega$ ✓)

**SC test (HV side):**

$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{300}{10^2} = 3.0\,\Omega$$

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{60}{10} = 6.0\,\Omega$$

$$X_{01} = \sqrt{6.0^2 - 3.0^2} = \sqrt{36 - 9} = \sqrt{27} = 5.196\,\Omega$$

**Equivalent circuit parameters (referred to HV):**
- Shunt: $R_{c1} = 25000\,\Omega$, $X_{m1} = 6920\,\Omega$
- Series: $R_{01} = 3.0\,\Omega$, $X_{01} = 5.196\,\Omega$

**Efficiency at full load, 0.8 pf lag:**

$$\eta = \frac{S\cos\phi}{S\cos\phi + P_{Fe} + P_{Cu,FL}} = \frac{20000 \times 0.8}{16000 + 160 + 300} = \frac{16000}{16460} = \boxed{97.20\%}$$

**Voltage regulation at full load, 0.8 pf lag:**

$$\text{VR\%} = \frac{I_1(R_{01}\cos\phi + X_{01}\sin\phi)}{V_1} \times 100$$

$$= \frac{10(3.0 \times 0.8 + 5.196 \times 0.6)}{2000} \times 100 = \frac{10(2.4 + 3.118)}{2000} \times 100$$

$$= \frac{10 \times 5.518}{2000} \times 100 = \frac{55.18}{2000} \times 100 = \boxed{2.76\%}$$

