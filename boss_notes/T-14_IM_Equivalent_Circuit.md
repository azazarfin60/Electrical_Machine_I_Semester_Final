[← T-13: Slip & Basics](T-13_Slip_and_Basics.md) | [🏠 Index](00_Index.md) | [T-15a: Starting Torque →](T-15a_Torque_Starting.md)

---

# T-14: IM Equivalent Circuit
> **Section:** B | **Priority:** 🟠 HIGH | **Exam Frequency:** 3/7 years
> **Sources:** Theraja Ch-34 (Art. 34.47), VK Mehta Ch-8 (Art. 8.8-8.9), Chapman Ch-7, Slides L-03

## Why This Topic Matters

The equivalent circuit question appeared in 3 out of 7 papers (2017, 2020, 2023). It is worth 3-6 marks per appearance. More importantly, every torque and power calculation in Section B relies on this circuit. If you can draw the 6-step equivalent circuit development, you can answer any IM analysis question.

---

## 📝 Key Definitions

> **Equivalent Circuit of IM:** "An induction motor can be treated as a rotating transformer i.e. one in which primary winding is stationary but the secondary is free to rotate." — Theraja, Art. 34.2. The equivalent circuit represents the per-phase electrical model of this rotating transformer.

> **Load Resistance $R_L$:** "The resistance $R_2(1-s)/s$ represents the electrical equivalent of the gross mechanical power developed by the motor." — VK Mehta, Art. 8.9

---

## Step-by-Step Equivalent Circuit Development

### Step 1: Transformer Model at Standstill ($s = 1$)

At standstill, the IM acts exactly like a transformer. The stator is the primary. The rotor is the short-circuited secondary.

- Stator: resistance $R_1$, leakage reactance $X_1$
- Shunt branch: core loss resistance $R_c$, magnetizing reactance $X_m$
- Rotor: resistance $R_2$, standstill reactance $X_2$

![Step 1: Transformer model at standstill](diagrams/im_step1_transformer_model.png)

### Step 2: Rotor at Running Slip $s$

When running at slip $s$, the rotor frequency changes to $sf$. The rotor EMF and reactance scale with slip:

$$E_{2s} = sE_2, \qquad X_{2s} = sX_2$$

Rotor current:

$$I_2 = \frac{sE_2}{R_2 + jsX_2} = \frac{sE_2}{\sqrt{R_2^2 + (sX_2)^2}}$$

![Step 2: Rotor circuit at slip s](diagrams/im_step2_rotor_slip_frequency.png)

### Step 3: Frequency Transformation

Divide numerator and denominator of the rotor current equation by $s$:

$$I_2 = \frac{E_2}{R_2/s + jX_2}$$

This transforms the rotor to the stator frequency $f$. The rotor resistance appears as a variable resistance $R_2/s$ at the stator frequency.

![Step 3: Frequency transformation to stator frequency](diagrams/im_step3_rotor_mechanical_load.png)

### Step 4: Power Separation

Split $R_2/s$ into two parts:

$$\frac{R_2}{s} = R_2 + R_2\left(\frac{1-s}{s}\right)$$

- $R_2$ represents actual rotor copper loss (heat)
- $R_L = R_2(1-s)/s$ represents the mechanical load (gross mechanical power)

![Step 4: Power separation into copper loss and mechanical load](diagrams/im_step4_power_separation.png)

### Step 5: Exact Equivalent Circuit (Referred to Stator)

Refer all rotor quantities to the stator using the effective turns ratio $a = N_1/N_2$:

$$R_2' = a^2 R_2, \qquad X_2' = a^2 X_2, \qquad R_L' = R_2'\left(\frac{1-s}{s}\right)$$

![Step 5: Exact equivalent circuit referred to stator](diagrams/im_step5_exact_referred_to_stator.png)

### Step 6: Approximate Equivalent Circuit

Since the stator voltage drop is small (typically < 5%), the shunt branch ($R_c$, $X_m$) can be moved to the input terminals. This simplifies calculations without much loss of accuracy.

![Step 6: Approximate equivalent circuit](diagrams/im_step6_approximate_stator_terminals.png)

---

## Key Equations from the Equivalent Circuit

**Air-gap power (per phase):**

$$P_g = I_2^2 \cdot \frac{R_2}{s}$$

**Total air-gap power (3-phase):**

$$P_g = 3I_2^2 \cdot \frac{R_2}{s}$$

**Rotor copper loss:**

$$P_{Cu,r} = 3I_2^2 R_2 = sP_g$$

**Mechanical power:**

$$P_m = P_g - P_{Cu,r} = (1-s)P_g = 3I_2^2 R_2\frac{(1-s)}{s}$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Draw the step-by-step equivalent circuit of a 3-phase induction motor.
> **Appeared:** 2017 Q3(a), 2020 Q5(c) — (3-6 marks)

**Full Answer:**

See [Step-by-Step Equivalent Circuit Development](#step-by-step-equivalent-circuit-development) above for the complete 6-step development:

1. **Standstill transformer model:** Stator ($R_1, X_1$) + shunt ($R_c, X_m$) + rotor ($R_2, X_2$)
2. **Running rotor:** EMF becomes $sE_2$, reactance becomes $sX_2$
3. **Frequency transformation:** Divide by $s$ to get $R_2/s$ at stator frequency
4. **Power separation:** $R_2/s = R_2 + R_2(1-s)/s$, where $R_2(1-s)/s$ is mechanical load
5. **Refer to stator:** $R_2' = a^2R_2$, $X_2' = a^2X_2$
6. **Approximate circuit:** Move shunt branch to input terminals

---

### 🎯 Q2: How can the equivalent circuit model of an induction motor be obtained?
> **Appeared:** 2020 Q5(c) — (6 marks)

**Full Answer:**

The equivalent circuit of an IM is obtained by treating it as a rotating transformer.

**Starting point:** At standstill ($s = 1$), the IM is identical to a transformer. The stator is the primary with impedance $Z_1 = R_1 + jX_1$. The shunt branch models core losses ($R_c$) and magnetizing current ($X_m$). The rotor is the short-circuited secondary with impedance $Z_2 = R_2 + jX_2$.

**Running modification:** When the rotor spins at slip $s$, two things change: (a) rotor EMF reduces to $sE_2$, (b) rotor reactance reduces to $sX_2$.

**Key trick:** The rotor current equation $I_2 = sE_2/\sqrt{R_2^2 + (sX_2)^2}$ can be rewritten as $I_2 = E_2/\sqrt{(R_2/s)^2 + X_2^2}$ by dividing top and bottom by $s$. This transforms the rotor circuit to stator frequency. The resistance $R_2/s$ splits as $R_2 + R_2(1-s)/s$, where $R_2$ accounts for copper loss and $R_2(1-s)/s$ represents mechanical power.

**Final step:** Refer all rotor quantities to the stator using $a^2$ scaling. Move shunt branch to input for the approximate circuit.

---

## Exam Variants

| Year | Question | Marks | Focus |
|:---|:---|:---|:---|
| 2017 Q3(a) | Draw step-by-step equivalent circuit | 3 | All 6 steps |
| 2020 Q5(c) | How to obtain eq. circuit model? | 6 | Derivation + explanation |
| 2023 Q7(a) | Explain NL and BR tests, find parameters | 9 | Testing + circuit |

---

## ⚡ Exam Tips & Common Mistakes

1. **Draw ALL six steps.** Don't jump to the final circuit. Each step carries marks.
2. **Label $R_2(1-s)/s$ clearly.** This is the mechanical load, not just a resistor.
3. **$R_2/s$ is NOT the rotor resistance.** It is the total impedance that accounts for both copper loss and mechanical power.
4. **The shunt branch is NOT negligible.** In the exact circuit, it sits between $Z_1$ and $Z_2'$. Only move it for the approximate circuit.
5. **Know both exact and approximate circuits.** Some questions ask specifically for one or the other.

## 🔗 Related Topics

- [T-13: Slip & Basics](T-13_Slip_and_Basics.md) — Slip determines all rotor quantities
- [T-15a: Starting Torque](T-15a_Torque_Starting.md) — Torque from the equivalent circuit
- [T-16: Power Flow](T-16_Power_Flow.md) — Power stages from the circuit
- [T-17a: No-Load Test](T-17a_No_Load_Test.md) — Finding shunt branch parameters
- [T-17b: Blocked Rotor Test](T-17b_Blocked_Rotor_Test.md) — Finding series branch parameters

---

[← T-13: Slip & Basics](T-13_Slip_and_Basics.md) | [🏠 Index](00_Index.md) | [T-15a: Starting Torque →](T-15a_Torque_Starting.md)
