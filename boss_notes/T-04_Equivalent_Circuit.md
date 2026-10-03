[← T-03b: Phasor Under Load](T-03b_Phasor_Diagrams_Under_Load.md) | [🏠 Index](00_Index.md) | [T-05: Voltage Regulation →](T-05_Voltage_Regulation.md)

---

# T-04: Equivalent Circuit
> **Section:** A | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-32 (Art. 32.16–32.20), VK Mehta Ch-7 (Art. 7.12–7.15), Slides L-10

## Why This Topic Matters

The equivalent circuit derivation appeared in 4/7 papers (2017, 2018, 2020, 2024). It ranges from "derive the equivalent circuit step by step" (4–5 marks) to using the circuit for numerical calculations. The OC/SC test (T-06a, T-06b) exists to find the parameters of this circuit. Master this topic and you have a framework for half of Section A.

---

## 📝 Key Definitions

> **Equivalent circuit:** "Since the two windings of a transformer are coupled inductively, the transfer of energy from primary to secondary is by means of a mutual flux. To make analysis easier, we represent the transformer by an equivalent circuit in which all quantities are referred to one side, eliminating the magnetic coupling and replacing it with electrical quantities." — VK Mehta, Art. 7.12

> **Approximate equivalent circuit:** "In a power transformer, the no-load current $I_0$ is only about 2–5% of the full-load primary current. Therefore, the voltage drop across the primary impedance due to $I_0$ is negligible. We can move the shunt branch to the input terminals. This enables combining the series impedances into single lumped parameters: $R_{01} = R_1 + R_2'$ and $X_{01} = X_1 + X_2'$." — Derived from Theraja Art. 32.18

> **Referring impedances:** "To obtain a unified single electrical network and eliminate the ideal transformer block, all secondary impedances, voltages and currents are referred to the primary side. The transformation preserves power invariance: $I_2^2 R_2 = (I_2')^2 R_2'$, giving $R_2' = a^2 R_2$ where $a = N_1/N_2$." — From Theraja Art. 32.17

---

## Step-by-Step Circuit Development

### Step 1: Ideal Transformer Model

![Step 1: Ideal Transformer Model](diagrams/tx_step1_ideal_transformer.png)

$$\frac{E_1}{E_2} = \frac{N_1}{N_2} = a, \qquad \frac{I_1}{I_2} = \frac{1}{a}$$

### Step 2: Add Winding Resistances and Leakage Reactances

![Step 2: Winding resistance and leakage reactance](diagrams/tx_step2_winding_resistance_leakage.png)

$$\vec{V}_1 = \vec{E}_1 + \vec{I}_1(R_1 + jX_1), \qquad \vec{E}_2 = \vec{V}_2 + \vec{I}_2(R_2 + jX_2)$$

### Step 3: Add Excitation Shunt Branch

![Step 3: Shunt branch for core loss and magnetizing current](diagrams/tx_step3_excitation_shunt_branch.png)

$R_c = E_1/I_c = E_1^2/P_c$ (models iron losses). $X_m = E_1/I_\mu$ (models magnetizing current).

$$\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$$

### Step 4: Refer Secondary to Primary (Exact Equivalent Circuit)

![Step 4: Exact equivalent circuit referred to primary](diagrams/tx_step4_exact_referred_to_primary.png)

| Quantity | Transformation | Referred Value |
|:---|:---|:---|
| Voltage | Multiply by $a$ | $V_2' = aV_2$, $E_2' = aE_2 = E_1$ |
| Current | Divide by $a$ | $I_2' = I_2/a$ |
| Resistance | Multiply by $a^2$ | $R_2' = a^2 R_2$ |
| Reactance | Multiply by $a^2$ | $X_2' = a^2 X_2$ |
| Impedance | Multiply by $a^2$ | $Z_L' = a^2 Z_L$ |

### Step 5: Approximate Equivalent Circuit

![Step 5: Approximate circuit with shunt at input](diagrams/tx_step5_approximate_referred_to_primary.png)

Move shunt branch to input terminals. Combine series impedances:

$$R_{01} = R_1 + a^2 R_2, \qquad X_{01} = X_1 + a^2 X_2$$

### Step 6: Simplified Series Circuit (Neglecting $I_0$)

![Step 6: Simple series impedance model](diagrams/tx_step6_simplified_series_circuit.png)

$$\vec{V}_1 = \vec{V}_2' + \vec{I}_2'(R_{01} + jX_{01})$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Derive the equivalent circuit of a single-phase two-winding transformer referred to the primary side (step by step).
> **Appeared:** 2018 Q1(c) — 2 marks, 2020 Q1(b) — 4 marks, 2020 Q3(c) — 5 marks

**Full Answer:**

A practical two-winding transformer deviates from the ideal model due to four physical phenomena: (1) winding resistance ($R_1$, $R_2$) causing copper losses, (2) leakage flux causing leakage reactance ($X_1$, $X_2$), (3) finite core permeability requiring magnetizing current ($I_m$) and iron losses requiring active current ($I_c$), and (4) turns ratio providing galvanic isolation.

**Step 1 — Ideal Transformer Model:** Start with zero losses, zero leakage, infinite permeability. $E_1/E_2 = N_1/N_2 = a$. $V_1 = E_1$, $V_2 = E_2$.

**Step 2 — Add winding impedances:** Model primary resistance $R_1$ and leakage reactance $X_1$ as series impedance on primary side. Similarly $R_2$ and $X_2$ on secondary. KVL: $V_1 = E_1 + I_1(R_1 + jX_1)$ and $E_2 = V_2 + I_2(R_2 + jX_2)$.

**Step 3 — Add shunt excitation branch:** Connect $R_c \parallel jX_m$ across the primary induced EMF $E_1$. $R_c = E_1^2/P_c$ carries core-loss current $I_c$. $X_m = E_1/I_m$ carries magnetizing current $I_m$. By KCL: $I_1 = I_0 + I_2'$.

**Step 4 — Refer secondary to primary:** To eliminate the ideal transformer block, convert all secondary quantities using the turns ratio $a = N_1/N_2$: $V_2' = aV_2$, $I_2' = I_2/a$, $R_2' = a^2 R_2$, $X_2' = a^2 X_2$, $Z_L' = a^2 Z_L$. The $a^2$ rule for impedance comes from power invariance: $I_2^2 R_2 = (I_2')^2 R_2'$.

This gives the **Exact Equivalent Circuit** referred to primary.

**Step 5 — Approximate circuit:** Since $I_0$ is small (2–5% of rated), the drop $I_0(R_1 + jX_1)$ is negligible. Move shunt branch to input terminals. Combine series: $R_{01} = R_1 + a^2 R_2$, $X_{01} = X_1 + a^2 X_2$.

**Step 6 — Simplified series circuit:** For full-load calculations, neglect $I_0$ entirely. The transformer becomes: $V_1 = V_2' + I_2'(R_{01} + jX_{01})$.

---

### 🎯 Q2: Numerical — 200/400V step-up transformer. Given equivalent circuit parameters, find primary current and secondary voltage.
> **Appeared:** 2017 Q8(c) — 5 marks

**Full Answer:**

Given: 200/400V step-up, $R_{eq} = 0.15\,\Omega$, $X_{eq} = 0.37\,\Omega$, $R_c = 600\,\Omega$, $X_m = 300\,\Omega$ (all referred to LV/primary). Load: 10A at 0.8 pf lag on secondary.

**Turns ratio:** $a = 200/400 = 0.5$

**Refer load to primary:** $I_2' = I_2/a = 10/0.5 = 20$ A

$$\vec{I}_2' = 20(0.8 - j0.6) = 16 - j12 \text{ A}$$

**No-load current.** Here 200 V is the given rated primary voltage, so take $\vec{V}_1 = 200\angle 0°$ V as the reference:

$$I_c = \frac{V_1}{R_c} = \frac{200}{600} = 0.333 \text{ A}, \qquad I_\mu = \frac{V_1}{X_m} = \frac{200}{300} = 0.667 \text{ A}$$

$$\vec{I}_0 = 0.333 - j0.667 \text{ A}$$

**Total primary current:**

$$\vec{I}_1 = \vec{I}_0 + \vec{I}_2' = (0.333 - j0.667) + (16 - j12) = 16.333 - j12.667 \text{ A}$$

$$|I_1| = \sqrt{16.333^2 + 12.667^2} = \boxed{20.67 \text{ A}}$$

Primary power factor: $\cos\phi_1 = 16.333/20.67 = 0.79$ lagging.

**Secondary terminal voltage.** Approximate voltage drop referred to the primary:

$$\Delta V = I_2'(R_{01}\cos\phi_2 + X_{01}\sin\phi_2) = 20(0.15 \times 0.8 + 0.37 \times 0.6) = 6.84 \text{ V}$$

$$V_2' = V_1 - \Delta V = 200 - 6.84 = 193.16 \text{ V}$$

$$V_2 = \frac{V_2'}{a} = \frac{193.16}{0.5} = \boxed{386.3 \text{ V}}$$

(Theraja Example 32.40 gives 386.32 V.)

---

## ⚡ Exam Tips & Common Mistakes

1. **Remember the $a^2$ rule for impedances.** Voltage scales by $a$, current by $1/a$, impedance by $a^2$.
2. **Draw all 5 (or 6) steps when asked for "step-by-step."** Each step carries marks.
3. **The shunt branch goes across $E_1$ in the exact circuit, across $V_1$ in the approximate circuit.**
4. **OC test → shunt branch ($R_c$, $X_m$). SC test → series branch ($R_{01}$, $X_{01}$).**

## 🔗 Related Topics

- [T-03b: Phasor Under Load](T-03b_Phasor_Diagrams_Under_Load.md) — Phasor analysis of this circuit
- [T-05: Voltage Regulation](T-05_Voltage_Regulation.md) — Uses Step 6 circuit
- [T-06a: OC Test](T-06a_OC_Test.md) — Finds $R_c$, $X_m$
- [T-06b: SC Test](T-06b_SC_Test.md) — Finds $R_{01}$, $X_{01}$

---

[← T-03b: Phasor Under Load](T-03b_Phasor_Diagrams_Under_Load.md) | [🏠 Index](00_Index.md) | [T-05: Voltage Regulation →](T-05_Voltage_Regulation.md)
