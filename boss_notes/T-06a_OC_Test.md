[← T-05: Voltage Regulation](T-05_Voltage_Regulation.md) | [🏠 Index](00_Index.md) | [T-06b: SC Test →](T-06b_SC_Test.md)

---

# T-06a: Open-Circuit (OC) Test
> **Section:** A | **Priority:** 🔴 MUST | **Exam Frequency:** 7/7 years
> **Sources:** Theraja Ch-32 (Art. 32.23–32.25), VK Mehta Ch-7 (Art. 7.18–7.19), Slides L-10 S17

## Why This Topic Matters

The OC/SC test is the **single most certain question in the entire exam.** It appeared in ALL 7 papers (2017–2024). The format is always the same: given OC and SC test data, find the equivalent circuit parameters, then calculate efficiency and/or voltage regulation. This is your guaranteed 5–10 marks if you know the procedure. The OC test finds the shunt branch parameters ($R_c$, $X_m$) and the iron loss.

---

## 📝 Key Definitions

> **Open-Circuit (OC) Test (No-Load Test):** "The purpose of this test is to determine (i) the iron losses and (ii) no-load current $I_0$ which is helpful in finding the parameters of the equivalent circuit — $R_c$ and $X_m$. In this test, one winding of the transformer (usually the low-voltage winding) is connected to the supply at rated voltage. The other winding is left open. The input voltage, no-load current and input power are measured." — VK Mehta, Art. 7.18

> **Iron (core) loss ($P_{Fe}$):** "The iron loss consists of hysteresis loss and eddy current loss. Both depend on flux density in the core. Since $B \propto V/f$, and the supply voltage is nearly constant, iron loss is essentially constant at all loads." — From explanation notes

---

## Test Setup and Procedure

![Open-Circuit (OC) Test Circuit Diagram](diagrams/transformer_oc_test_circuit.png)

**Connections (VK Mehta, Art. 7.18):**
1. Connect the **LV winding** to the rated supply voltage through a variac.
2. Leave the **HV winding open-circuited** (no load connected).
3. Connect measuring instruments on the LV side:
   - Voltmeter ($V_0$) across the winding
   - Ammeter ($I_0$) in series
   - Low power factor (LPF) wattmeter ($W_0$)

**Why LV side?** Two reasons:
- Rated voltage on the LV side is lower (safer, easier to supply).
- Current measuring instruments can handle the no-load current more easily.

**Readings taken:** $V_0$, $I_0$, $W_0$ when voltage reaches rated value.

---

## Parameter Extraction

Since the secondary is open, the only current flowing is the no-load current $I_0$. This is small (2–10% of rated). The copper loss $I_0^2 R_1$ is negligible.

**All power input = iron loss:**

$$\boxed{P_{Fe} = W_0}$$

This iron loss is **constant at all loads.** It does not change whether the transformer is at no-load, half-load, or full-load.

**No-load power factor:**

$$\cos\phi_0 = \frac{W_0}{V_0 I_0}$$

**Current components:**

$$I_w = I_0 \cos\phi_0 \qquad \text{(core-loss component)}$$

$$I_\mu = I_0 \sin\phi_0 \qquad \text{(magnetizing component)}$$

**Shunt branch parameters (referred to the side where OC test is done):**

$$\boxed{R_c = \frac{V_0}{I_w} = \frac{V_0^2}{W_0}}$$

$$\boxed{X_m = \frac{V_0}{I_\mu}}$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Explain the procedure of the OC test and what parameters it determines.
> **Appeared:** 2021 Q2(b) — 4 marks

**Full Answer:**

**Setup:** Connect the LV winding to rated supply voltage through a variac. Leave HV winding open-circuited. Place ammeter ($I_0$), voltmeter ($V_0$), and LPF wattmeter ($W_0$) on the LV side.

**Procedure:** Gradually increase the supply voltage from zero to rated value using the variac. Record $V_0$, $I_0$, and $W_0$ at rated voltage.

**What it determines:**

(1) **Iron (core) loss:** $P_{Fe} = W_0$. The wattmeter reading directly gives the iron loss because: (a) secondary is open so $I_2 = 0$ (no copper loss in secondary), and (b) the no-load current $I_0$ is so small (2–5% of rated) that primary copper loss $I_0^2 R_1$ is negligible.

(2) **Shunt branch parameters:** $R_c = V_0^2/W_0$ (resistance representing core loss) and $X_m = V_0/I_\mu$ (magnetizing reactance).

(3) **No-load current and power factor:** $\cos\phi_0 = W_0/(V_0 I_0)$. This is typically very low (0.1–0.3).

(4) **Turns ratio verification:** By measuring both primary and open-circuit secondary voltages: $a = V_1/V_2$.

**Why LV side?** Lower voltage is safer. Current instruments can handle the small no-load current more easily.

---

### 🎯 Q2: Draw circuit diagrams for OC and SC tests.
> **Appeared:** 2020 Q2(c) — 2 marks

**Full Answer:**

**OC Test Circuit:** LV winding connected to rated AC supply through variac. Ammeter in series, voltmeter across, wattmeter measuring input. HV winding open-circuited.

![OC Test Circuit](diagrams/transformer_oc_test_circuit.png)

**SC Test Circuit:** HV winding connected to variable AC supply through variac. Ammeter in series, voltmeter across, wattmeter measuring input. LV winding solidly short-circuited with a thick copper conductor.

![SC Test Circuit](diagrams/transformer_sc_test_circuit.png)

---

### 🎯 Q3: Why are OC and SC tests preferred over direct load test?
> **Appeared:** 2024 Q3(a) — 4 marks

**Full Answer:**

Testing a 500 kVA transformer by direct load test would require:
- A load bank of 500 kVA (resistors, inductors, capacitors): expensive, large, and dangerous.
- Continuous power dissipation of ~15 kW in losses per hour.
- Only one load condition at a time. Different loads require reconfiguration.

**What OC and SC tests do instead:**

**OC test:** Apply rated voltage to LV winding (HV open). Only the no-load current flows (2–5% of rated). Power consumed = iron losses only (about 0.3–0.5% of rated kVA). For a 500 kVA transformer: test power is only 1.5–2.5 kW. Tiny.

**SC test:** Apply 5–10% of rated voltage to HV winding (LV short-circuited). Full-load current flows but at very low voltage. Power consumed = copper losses only (about 0.8–1.5% of rated kVA). Again tiny.

**From two simple, low-power tests, you get everything:**
- Core loss $P_{Fe}$ (from OC test)
- Full-load copper loss $P_{Cu,FL}$ (from SC test)
- All four equivalent circuit parameters ($R_c$, $X_m$, $R_{01}$, $X_{01}$)
- Efficiency at **any** load and **any** power factor (by formula)
- Voltage regulation at **any** load and **any** power factor (by formula)

**Key insight:** Efficiency and VR are calculated analytically using the measured parameters. You never need to actually apply real loads. This is why OC/SC tests are universally preferred.

---

## ⚡ Exam Tips & Common Mistakes

1. **OC test gives iron loss, not copper loss.** $W_0 = P_{Fe}$ because $I_0$ is too small for significant copper loss.
2. **OC test is done on LV side.** Not HV. The reason is safety and convenience.
3. **$R_c$ and $X_m$ are referred to the side where the test is done.** To refer to the other side, multiply by $a^2$ (or divide, depending on direction).
4. **Iron loss is CONSTANT.** It does not change with load.

## 🔗 Related Topics

- [T-06b: SC Test](T-06b_SC_Test.md) — The companion test for series parameters
- [T-06c: Efficiency](T-06c_Efficiency.md) — Uses $P_{Fe}$ from OC test
- [T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) — The circuit whose parameters we're finding
- [T-03a: No-Load Operation](T-03a_No-Load_Operation.md) — The physics of what happens during OC test

---

[← T-05: Voltage Regulation](T-05_Voltage_Regulation.md) | [🏠 Index](00_Index.md) | [T-06b: SC Test →](T-06b_SC_Test.md)
