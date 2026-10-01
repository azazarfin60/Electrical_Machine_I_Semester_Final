[← T-15c: Torque-Speed Curves](T-15c_Torque_Speed_Curves.md) | [🏠 Index](00_Index.md) | [T-17a: No-Load Test →](T-17a_No_Load_Test.md)

---

# T-16: Power Flow & Rotor Power Division
> **Section:** B | **Priority:** 🟡 MEDIUM | **Exam Frequency:** 2/7 years
> **Sources:** Theraja Ch-34 (Art. 34.33-34.38), VK Mehta Ch-8, Slides L-06

## Why This Topic Matters

The power flow proof ($P_g : P_{Cu,r} : P_m = 1 : s : (1-s)$) appeared in 3 out of 7 papers (2018, 2023, 2024). The rotor efficiency proof ($\eta_r = 1-s$) appeared in 2021 and 2023. The synchronous watt definition appeared in 2021. These are short, high-scoring proofs (3-4 marks each). The power flow numerical appeared in 2020.

---

## 📝 Key Definitions

> **Air-Gap Power ($P_g$):** "The power transferred from the stator to the rotor across the air gap is called the air-gap power. It is given by $P_g = 3I_2^2 R_2/s$." — Theraja, Art. 34.34

> **Synchronous Watt:** "A synchronous watt is the torque which, at the synchronous speed of the machine under consideration, would give a power dissipation of 1 watt. Torque in synchronous watts equals the air-gap power in watts." — Theraja, Art. 34.35

> **Rotor Efficiency:** "The rotor efficiency is the ratio of the mechanical power developed to the air-gap power: $\eta_{\text{rotor}} = (1-s)$." — VK Mehta, Ch-8

---

## Power Flow Diagram

$$\text{Stator Input } P_1 \xrightarrow{-P_{s,Cu}-P_{Fe}} \text{Air-gap } P_g \xrightarrow{-P_{r,Cu}} \text{Mech Power } P_m \xrightarrow{-P_{f\&w}} \text{Output } P_{out}$$

![Power flow diagram of an induction motor](diagrams/power_flow_diagram.jpg)

**From the equivalent circuit:**

- Stator input: $P_1 = 3V_1I_1\cos\phi_1$
- Stator copper loss: $P_{s,Cu} = 3I_1^2R_1$
- Stator iron loss: $P_{Fe} \approx 3E_1^2/R_c$
- Air-gap power: $P_g = P_1 - P_{s,Cu} - P_{Fe} = 3I_2^2 \cdot R_2/s$
- Rotor copper loss: $P_{r,Cu} = 3I_2^2R_2$
- Mechanical power: $P_m = P_g - P_{r,Cu} = 3I_2^2R_2(1-s)/s$
- Output: $P_{out} = P_m - P_{f\&w} - P_{\text{stray}}$

---

## The Golden Power Ratio

This is the most important relationship in IM power analysis.

**Proof:** $P_{Cu,r} = sP_g$

From the equivalent circuit:

$$P_g = 3I_2^2 \cdot \frac{R_2}{s}$$

$$P_{Cu,r} = 3I_2^2 R_2 = s \cdot 3I_2^2 \cdot \frac{R_2}{s} = s \cdot P_g$$

$$\boxed{P_{Cu,r} = sP_g}$$

**Mechanical power:**

$$P_m = P_g - P_{Cu,r} = P_g - sP_g = (1-s)P_g$$

**The ratio:**

$$\boxed{P_g : P_{Cu,r} : P_m = 1 : s : (1-s)}$$

![Power stages block diagram](diagrams/power_stages_block.jpg)

**Physical meaning:** For every 1 watt crossing the air gap, $s$ watts become rotor heat and $(1-s)$ watts become mechanical power. At $s = 0.04$ (typical full load), 96% of air-gap power becomes mechanical, 4% becomes heat.

---

## Rotor Efficiency

$$\eta_{\text{rotor}} = \frac{P_m}{P_g} = \frac{(1-s)P_g}{P_g} = \boxed{(1-s)}$$

At $s = 0.04$: $\eta_{\text{rotor}} = 96\%$. This is why induction motors run at low slip.

---

## Synchronous Watt

One synchronous watt is the torque that develops one watt of power at synchronous speed.

$$T \text{ (synchronous watts)} = P_g \text{ (watts)}$$

To convert to N-m:

$$T = \frac{P_g}{\omega_s} = \frac{P_g}{2\pi N_s/60} \text{ N-m}$$

**Example:** $P_g = 5000$ W, $N_s = 1000$ rpm:

$$T = \frac{5000}{2\pi \times 1000/60} = \frac{5000}{104.7} = 47.75 \text{ N-m}$$

---

## Worked Example (PYQ 2020)

**2020 Q6(d): 400V, 50 Hz, 6-pole IM. $P_g = 75$ kW. Rotor EMF makes 100 alternations per minute. Find slip, rotor speed, Cu losses per phase, mechanical power.**

Rotor frequency: $f_r = 100/60 = 5/3$ Hz

**(i) Slip:** $s = f_r/f = (5/3)/50 = 1/30 = \boxed{0.0333 = 3.33\%}$

**(ii) Rotor speed:** $N_s = 120 \times 50/6 = 1000$ rpm

$$N = N_s(1-s) = 1000(1-0.0333) = \boxed{966.7 \text{ rpm}}$$

**(iii) Rotor Cu losses (total):** $P_{Cu,r} = sP_g = 0.0333 \times 75000 = 2500$ W

Per phase: $P_{Cu,r}/3 = \boxed{833.3 \text{ W}}$

**(iv) Mechanical power:** $P_m = (1-s)P_g = 0.9667 \times 75000 = \boxed{72500 \text{ W} = 72.5 \text{ kW}}$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Show that rotor copper loss = $s \times$ air-gap power. Also show $P_m : P_{Cu,r} : P_g = (1-s) : s : 1$.
> **Appeared:** 2018 Q5(b), 2023 Q6(a), 2024 Q5(b) — (4 marks)

**Full Answer:**

From the equivalent circuit, air-gap power: $P_g = 3I_2^2 \cdot R_2/s$

Rotor copper loss: $P_{Cu,r} = 3I_2^2R_2 = s \cdot 3I_2^2 \cdot R_2/s = sP_g$

$$\boxed{P_{Cu,r} = sP_g}$$

Mechanical power: $P_m = P_g - P_{Cu,r} = P_g - sP_g = (1-s)P_g$

$$P_m : P_{Cu,r} : P_g = (1-s)P_g : sP_g : P_g = \boxed{(1-s) : s : 1}$$

---

### 🎯 Q2: What is rotor efficiency? Show that $\eta_{\text{rotor}} = (1-s)$.
> **Appeared:** 2021 Q6(c), 2023 Q6(c) — (3-4 marks)

**Full Answer:**

Rotor efficiency is the ratio of mechanical power developed to electrical power input to the rotor (air-gap power).

$$\eta_{\text{rotor}} = \frac{P_m}{P_g} = \frac{(1-s)P_g}{P_g} = \boxed{(1-s)}$$

At $s = 0.04$ (typical full load): $\eta_{\text{rotor}} = 96\%$.

For every unit of power crossing the air gap, fraction $s$ is wasted as rotor copper heat and fraction $(1-s)$ becomes mechanical work. Low slip means high rotor efficiency. This is why induction motors are designed to operate at small slip.

---

### 🎯 Q3: Define synchronous watt with an example.
> **Appeared:** 2021 Q8(a) — (3 marks)

**Full Answer:**

**Synchronous watt:** A unit of torque used in induction motor analysis. One synchronous watt is the torque that develops one watt of power at synchronous speed.

$$T \text{ (synchronous watts)} = P_g \text{ (watts)}$$

Conversion: $T (\text{N-m}) = P_g/\omega_s = P_g/(2\pi N_s/60)$

**Example:** Motor has $P_g = 5000$ W, $N_s = 1000$ rpm ($\omega_s = 104.7$ rad/s):

$$T = 5000/104.7 = 47.75 \text{ N-m}$$

The torque is 5000 synchronous watts, which equals 47.75 N-m at this synchronous speed.

---

### 🎯 Q4: Derive power equations of an induction motor from equivalent circuit.
> **Appeared:** 2020 Q6(b) — (4 marks)

**Full Answer:**

From the per-phase equivalent circuit:

**Stator input:** $P_1 = 3V_1I_1\cos\phi_1$

**Stator copper loss:** $P_{s,Cu} = 3I_1^2R_1$

**Stator iron loss:** $P_{Fe} \approx 3V_1^2/R_c$

**Air-gap power:** $P_g = P_1 - P_{s,Cu} - P_{Fe} = 3I_2^2 \cdot R_2/s$

**Rotor copper loss:** $P_{Cu,r} = 3I_2^2R_2 = sP_g$

**Mechanical power:** $P_m = P_g - P_{Cu,r} = (1-s)P_g = 3I_2^2R_2(1-s)/s$

**Output:** $P_{out} = P_m - P_{f\&w}$

**Summary:** $P_g : P_{Cu,r} : P_m = 1 : s : (1-s)$

---

### 🎯 Q5: Motor driving constant-torque load. Voltage drops to 90%. Find increase in Cu losses.
> **Appeared:** 2021 Q6(b) — (4 marks)

**Full Answer:**

For small slip (low-slip approximation): $T \approx kE_2^2s/R_2 \propto sV^2/R_2$

At constant torque: $s_1V_1^2 = s_2V_2^2$

$$s_2 = s_1(V_1/V_2)^2 = s_1 \times (1/0.9)^2 = s_1 \times 1.2346$$

Rotor Cu loss: $P_{Cu} = sP_g$, and $P_g = T\omega_s$ (constant).

$$P_{Cu,\text{new}}/P_{Cu,\text{old}} = s_2/s_1 = 1.2346$$

**Increase:** $(1.2346 - 1) \times 100\% = \boxed{23.46\%}$

Cu losses increase by about 23.5% when voltage drops to 90%.

---

## Exam Variants

| Year | Question | Key Result |
|:---|:---|:---|
| 2018 Q5(b) | Show $P_{Cu,r} = sP_g$ | Proof |
| 2020 Q6(b) | Derive power equations | Full chain |
| 2020 Q6(d) | Power flow numerical | $s = 3.33\%$, $P_m = 72.5$ kW |
| 2021 Q6(b) | 90% voltage, Cu loss increase | 23.46% increase |
| 2021 Q6(c) | Rotor efficiency | $\eta_r = 1-s$ |
| 2021 Q8(a) | Synchronous watt | Definition + example |
| 2023 Q6(a) | Show power ratio | $1 : s : (1-s)$ |
| 2023 Q6(c) | Rotor efficiency proof | $\eta_r = 1-s$ |
| 2024 Q5(b) | Show $P_{Cu,r} = sP_g$ + ratio | Same proof |

---

## ⚡ Exam Tips & Common Mistakes

1. **The ratio is $1 : s : (1-s)$, not $1 : (1-s) : s$.** Air gap : Cu loss : Mechanical. Don't swap the last two.
2. **Rotor efficiency is $(1-s)$, not $(1-s)\%$.** Express as per-unit or convert explicitly.
3. **Synchronous watt is numerically equal to $P_g$ in watts.** The conversion to N-m requires dividing by $\omega_s$.
4. **For power flow numericals:** Always start by finding slip from rotor frequency ($s = f_r/f$).

## 🔗 Related Topics

- [T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) — Source of power equations
- [T-15b: Running & Max Torque](T-15b_Torque_Running_and_Max.md) — Torque from air-gap power
- [T-17a: No-Load Test](T-17a_No_Load_Test.md) — Measures fixed losses

---

[← T-15c: Torque-Speed Curves](T-15c_Torque_Speed_Curves.md) | [🏠 Index](00_Index.md) | [T-17a: No-Load Test →](T-17a_No_Load_Test.md)
