[← T-06b: SC Test](T-06b_SC_Test.md) | [🏠 Index](00_Index.md) | [T-07a: 3-Phase Connections →](T-07a_3Phase_Connections.md)

---

# T-06c: Transformer Efficiency
> **Section:** A | **Priority:** 🟠 HIGH | **Exam Frequency:** 5/7 years
> **Sources:** Theraja Ch-32 (Art. 32.29–32.34), VK Mehta Ch-7 (Art. 7.22–7.24), Slides L-10 S19

## Why This Topic Matters

Efficiency calculations appeared in 5/7 papers (2017, 2018, 2019, 2023, 2024). The question types include: (1) calculate efficiency at full-load and half-load for different power factors, (2) prove the condition for maximum efficiency, and (3) calculate all-day efficiency with a load schedule. All-day efficiency appeared in 3/7 papers (2018, 2019, 2023). These are pure formula-plugging questions. Free marks.

---

## 📝 Key Definitions

> **Transformer efficiency ($\eta$):** "The efficiency of a transformer is defined as the ratio of output power to input power. Since input = output + losses: $\eta = \text{Output}/(\text{Output} + \text{Losses})$." — VK Mehta, Art. 7.22

> **All-day efficiency ($\eta_{\text{all-day}}$):** "The all-day efficiency (or energy efficiency) is defined as the ratio of total energy output (kWh) to total energy input (kWh) over a 24-hour period. It is of particular importance for distribution transformers which remain connected to the supply round the clock but deliver varying loads throughout the day." — VK Mehta, Art. 7.24

> **Maximum efficiency condition:** "Efficiency of a transformer is maximum when copper loss equals iron loss, i.e., variable loss = constant loss. This condition yields the load fraction $x = \sqrt{P_{Fe}/P_{Cu,FL}}$." — VK Mehta, Art. 7.23

---

## The Efficiency Formula

A transformer has exactly two types of losses:

1. **Iron loss ($P_{Fe}$):** Constant at all loads. Measured from OC test.
2. **Copper loss ($P_{Cu}$):** Proportional to load current squared. At fraction $x$ of full load: $P_{Cu} = x^2 P_{Cu,FL}$.

$$\boxed{\eta = \frac{x \cdot S \cdot \cos\phi}{x \cdot S \cdot \cos\phi + P_{Fe} + x^2 P_{Cu,FL}} \times 100\%}$$

where:
- $x$ = fraction of full load (1 = full load, 0.5 = half load)
- $S$ = rated VA (in watts, not kVA!)
- $\cos\phi$ = load power factor
- $P_{Fe}$ = iron loss (from OC test)
- $P_{Cu,FL}$ = full-load copper loss (from SC test)

---

## Condition for Maximum Efficiency

Differentiate $\eta$ with respect to $x$ and set to zero:

$$\frac{d\eta}{dx} = 0 \implies x^2 P_{Cu,FL} = P_{Fe}$$

$$\boxed{\text{At maximum efficiency: Copper loss = Iron loss}}$$

$$x_{\text{max}\,\eta} = \sqrt{\frac{P_{Fe}}{P_{Cu,FL}}}$$

> [!TIP]
> If $P_{Fe} = P_{Cu,FL}$, maximum efficiency is at full load ($x = 1$). If $P_{Fe} < P_{Cu,FL}$ (typical for distribution transformers), maximum efficiency occurs at partial load. Distribution transformers are designed this way because they spend most hours below full load.

---

## All-Day (Energy) Efficiency

$$\boxed{\eta_{\text{all-day}} = \frac{\text{Total kWh output}}{\text{Total kWh output} + \text{Total kWh losses}} \times 100\%}$$

**Procedure:**

1. **Energy output:** For each load period, $\text{kWh} = x \cdot S \cdot \cos\phi \times \text{hours}$
2. **Iron loss energy:** $P_{Fe} \times 24$ kWh (runs 24 hours, always!)
3. **Copper loss energy:** For each period, $x_i^2 \times P_{Cu,FL} \times t_i$ hours
4. Sum everything and divide.

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Prove that maximum efficiency occurs when copper loss = iron loss.
> **Appeared:** 2019 Q3(a) — 4 marks, 2023 Q2(a) — 3 marks

**Full Answer:**

**Derivation:**

Transformer efficiency: $\eta = \frac{P_{out}}{P_{out} + P_{Fe} + P_{Cu}}$

At fraction $x$ of full load: $P_{out} = xS\cos\phi$, $P_{Cu} = x^2 P_{Cu,FL}$, $P_{Fe}$ is constant.

$$\eta = \frac{xS\cos\phi}{xS\cos\phi + P_{Fe} + x^2 P_{Cu,FL}}$$

Let $A = S\cos\phi$ (constant for fixed pf). Then:

$$\eta = \frac{xA}{xA + P_{Fe} + x^2 P_{Cu,FL}}$$

For maximum $\eta$, set $d\eta/dx = 0$. Using the quotient rule:

$$\frac{d\eta}{dx} = \frac{A(xA + P_{Fe} + x^2 P_{Cu,FL}) - xA(A + 2x P_{Cu,FL})}{(xA + P_{Fe} + x^2 P_{Cu,FL})^2} = 0$$

Numerator must be zero:

$$A(xA + P_{Fe} + x^2 P_{Cu,FL}) - xA(A + 2x P_{Cu,FL}) = 0$$

$$xA^2 + AP_{Fe} + Ax^2 P_{Cu,FL} - xA^2 - 2Ax^2 P_{Cu,FL} = 0$$

$$AP_{Fe} - Ax^2 P_{Cu,FL} = 0$$

$$\boxed{P_{Fe} = x^2 P_{Cu,FL}}$$

That is: **iron loss = copper loss at the operating load.**

The load fraction for maximum efficiency:

$$x = \sqrt{\frac{P_{Fe}}{P_{Cu,FL}}}$$

For example, if $P_{Fe} = 350$ W and $P_{Cu,FL} = 400$ W:

$$x = \sqrt{350/400} = \sqrt{0.875} = 0.935$$

Maximum efficiency occurs at 93.5% of full load.

---

### 🎯 Q2: 25 kVA transformer, iron loss = 350 W, full-load Cu loss = 400 W. Find efficiency at FL and HL, at upf and 0.8 pf lag.
> **Appeared:** 2017 Q5(c) — 4 marks

**Full Answer:**

Given: $S = 25$ kVA = 25000 W, $P_{Fe} = 350$ W, $P_{Cu,FL} = 400$ W.

| Condition | $x$ | Output (W) | $P_{Fe}$ (W) | $P_{Cu} = x^2 \times 400$ (W) | Input (W) | $\eta$ |
|:---|:---:|---:|---:|---:|---:|:---|
| FL, upf | 1.0 | 25000 | 350 | 400 | 25750 | $25000/25750 = \boxed{97.1\%}$ |
| FL, 0.8 lag | 1.0 | 20000 | 350 | 400 | 20750 | $20000/20750 = \boxed{96.4\%}$ |
| HL, upf | 0.5 | 12500 | 350 | 100 | 12950 | $12500/12950 = \boxed{96.5\%}$ |
| HL, 0.8 lag | 0.5 | 10000 | 350 | 100 | 10450 | $10000/10450 = \boxed{95.7\%}$ |

**Why is efficiency lower at 0.8 pf?** The losses (350 + 400 W) stay the same. But the output drops (multiplied by 0.8). So losses take a bigger fraction of the input.

**Why is HL efficiency less than FL at same pf?** At half load, the iron loss (350 W) is proportionally larger compared to the output (12.5 kW) than at full load (25 kW). Maximum efficiency occurs at $x = \sqrt{350/400} = 0.935$ (93.5% of full load), which is close to FL.

---

### 🎯 Q3: A 100-kVA lighting transformer has a full-load loss of 3 kW, the losses being equally divided between iron and copper. During a day, the transformer operates on full load for 3 hours, one-half load for 4 hours, the output being negligible for the remainder of the day. Calculate the all-day efficiency.
> **Appeared:** 2023 Q3(b) — 4 marks

**Full Answer:**

Given: $S = 100$ kVA, full-load loss $= 3$ kW shared equally, so $P_{Fe} = P_{Cu,FL} = 1.5$ kW. A lighting load is taken at unity power factor, so 100 kVA gives 100 kW.

**Definition to quote:** "The all-day efficiency (or energy efficiency) is defined as the ratio of total energy output (kWh) to total energy input (kWh) over a 24-hour period." — VK Mehta, Art. 7.24

**Energy output:**

| Period | Load | Output (kW) | Hours | kWh |
|:---|:---|---:|---:|---:|
| Full load | 100% | 100 | 3 | 300 |
| Half load | 50% | 50 | 4 | 200 |
| Rest | negligible | 0 | 17 | 0 |
| **Total** | | | **24** | **500** |

**Iron loss energy** (runs the full 24 hours, the transformer stays energised):
$$1.5 \times 24 = \boxed{36\text{ kWh}}$$

**Copper loss energy** (follows the square of load, and is zero when the load is zero):
$$1.5 \times 3 + (0.5)^2 \times 1.5 \times 4 = 4.5 + 1.5 = \boxed{6\text{ kWh}}$$

**Total losses** $= 36 + 6 = 42$ kWh

$$\eta_{\text{all-day}} = \frac{500}{500 + 42} = \frac{500}{542} = \boxed{92.25\%}$$

**Why it is so much lower than full-load efficiency.** At full load, $\eta = 100/(100+1.5+1.5) = 97.1\%$. Over the day the 36 kWh of iron loss dominates, because the transformer is magnetised for 24 hours but delivers useful output for only 7 of them. This is exactly why a lighting transformer is designed with a low iron loss.

---

### 🎯 Q3b: Define power transformer. Prove that efficiency is maximum when copper loss equals iron loss.
> **Appeared:** 2023 Q2(a) — 3 marks

**Full Answer:**

**Power transformer.** A large, high-rating static transformer used in generating stations and transmission substations to step voltage up or down at bulk power levels. It runs near full load for most of the day, is designed for the highest possible full-load efficiency, and is usually oil-immersed with forced cooling.

**Proof.** Let the secondary carry current $I_2$ at terminal voltage $V_2$ and power factor $\cos\phi$. Let $P_i$ be the iron loss and $R_{02}$ the total resistance referred to the secondary.

$$\eta = \frac{V_2 I_2 \cos\phi}{V_2 I_2 \cos\phi + P_i + I_2^2 R_{02}} = \frac{V_2 \cos\phi}{V_2 \cos\phi + \dfrac{P_i}{I_2} + I_2 R_{02}}$$

$V_2$ and $\cos\phi$ are held constant, so $\eta$ is maximum when the denominator is minimum:
$$\frac{d}{dI_2}\left(\frac{P_i}{I_2} + I_2 R_{02}\right) = 0 \implies -\frac{P_i}{I_2^2} + R_{02} = 0 \implies I_2^2 R_{02} = P_i$$

$$\boxed{\text{Copper loss} = \text{Iron loss at maximum efficiency}}$$

The second derivative is $2P_i/I_2^3 > 0$, so this is a true minimum of the loss term and a maximum of $\eta$. Load fraction at maximum efficiency: $x = \sqrt{P_i/P_{Cu,FL}}$.

---

### 🎯 Q4: Define all-day efficiency.
> **Appeared:** 2018 Q2(a) — 1 mark

**Full Answer:**

"All-day efficiency (or energy efficiency) is defined as the ratio of total energy output (kWh) to total energy input (kWh) over a 24-hour period." — VK Mehta, Art. 7.24

$$\eta_{\text{all-day}} = \frac{\text{Total kWh output in 24h}}{\text{Total kWh input in 24h}} \times 100 = \frac{\text{Total kWh output}}{\text{Total kWh output} + \text{Total kWh losses}} \times 100$$

It is important for distribution transformers that remain connected to the supply 24 hours a day but supply varying loads. The iron loss accumulates over all 24 hours regardless of load, while copper loss varies with the load profile.

---

## ⚡ Exam Tips & Common Mistakes

1. **Iron loss runs 24 hours.** Even during no-load periods. This is the single most common error in all-day efficiency calculations.
2. **Copper loss scales with $x^2$, not $x$.** At half load: $P_{Cu} = 0.25 P_{Cu,FL}$, not $0.5 P_{Cu,FL}$.
3. **Use watts, not kVA.** Output power = $x \times S \times \cos\phi$ (watts). Don't forget the power factor.
4. **At maximum efficiency, $x = \sqrt{P_{Fe}/P_{Cu,FL}}$.** If $P_{Fe} = 350$ W and $P_{Cu} = 400$ W, then $x = 0.935$. Max η is at 93.5% of full load.
5. **All-day efficiency is always less than full-load efficiency** because iron losses accumulate during idle periods.

## 🔗 Related Topics

- [T-06a: OC Test](T-06a_OC_Test.md) — Measures $P_{Fe}$
- [T-06b: SC Test](T-06b_SC_Test.md) — Measures $P_{Cu,FL}$
- [T-05: Voltage Regulation](T-05_Voltage_Regulation.md) — Often calculated alongside efficiency
- [T-11: Miscellaneous](T-11_Miscellaneous_Transformer.md) — Hysteresis and eddy current loss formulas

---

[← T-06b: SC Test](T-06b_SC_Test.md) | [🏠 Index](00_Index.md) | [T-07a: 3-Phase Connections →](T-07a_3Phase_Connections.md)
