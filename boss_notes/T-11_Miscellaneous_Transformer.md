[← T-10: Auto-Transformer](T-10_Auto_Transformer.md) | [🏠 Index](00_Index.md) | [T-12: Rotating Magnetic Field →](T-12_Rotating_Magnetic_Field.md)

---

# T-11: Miscellaneous Transformer Topics
> **Section:** A | **Priority:** 🟡 MEDIUM | **Exam Frequency:** Various (see individual topics)
> **Sources:** Theraja Ch-32 (various), VK Mehta Ch-7 (various), Slides L-08, L-11

## Why This Topic Matters

This file collects short-answer transformer topics that appear as 2-3 mark filler questions. Individually they are low-weight, but collectively they add up to 6-10 marks per paper. The most important ones: "Why rated in kVA?" (3/7 papers), "Hysteresis vs eddy current loss" (2/7), "Classify transformers" (1/7), "Instrument transformers" (1/7), "Inrush current" (1/7), "Effect of frequency" (1/7).

---

## 📝 Key Definitions

> **Hysteresis loss:** "When a magnetic material is subjected to a cycle of magnetization, the B-H curve traced out during demagnetization does not retrace the curve traced during magnetization. Energy is expended in overcoming this 'molecular friction,' appearing as heat. This energy loss per unit volume per cycle is proportional to the area of the hysteresis loop." — Theraja, Art. 32.3. Formula: $P_h = K_h f B_m^{1.6} V$ (Steinmetz formula).

> **Eddy current loss:** "Alternating flux through the conducting iron core induces EMFs which drive circulating currents (eddy currents) within the core. These cause $I^2R$ heating." — Theraja, Art. 32.3. Formula: $P_e = K_e f^2 B_m^2 t^2 V$ where $t$ = lamination thickness.

> **Instrument transformer:** "A transformer designed to scale high voltages or currents down to safe, measurable levels for instruments and relays. Two types: Potential Transformer (PT) for voltage measurement, and Current Transformer (CT) for current measurement." — VK Mehta, Art. 7.39

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Why are transformers rated in kVA (not kW)?
> **Appeared:** 2020 Q3(a) — 2 marks

**Full Answer:**

Transformer losses determine its heating and therefore its maximum safe operating capacity:

1. **Iron (core) loss:** Depends on supply voltage only (since $B \propto V/f$ and frequency is fixed). Independent of load current and independent of load power factor.
2. **Copper loss:** Depends on load current squared ($I^2R$). Independent of load power factor.

Since neither loss depends on the power factor of the connected load, the total loss (and hence the temperature rise) is determined by the voltage and current magnitudes alone. A transformer can handle a given product $V \times I$ regardless of whether the load power factor is 0.5, 0.8, or 1.0.

Since the manufacturer does not know what power factor the load will have, the rating is expressed in **volt-amperes (VA or kVA)**, not watts (kW). The actual power delivered (kW) depends on the load power factor: $P = S \cos\phi$. But the transformer's thermal capacity is determined by $S = VI$ (kVA).

---

### 🎯 Q2: Short notes on hysteresis loss and eddy current loss.
> **Appeared:** 2017 Q6(b) — 4 marks

**Full Answer:**

**Hysteresis Loss:**

When the transformer core is magnetized in alternating cycles, the magnetic domains reverse direction each half-cycle. Energy is spent overcoming molecular friction during this reversal. This energy appears as heat.

$$P_h = K_h \cdot f \cdot B_m^{1.6} \cdot V_{\text{core}} \quad \text{(Steinmetz formula)}$$

where $K_h$ depends on the core material, $f$ = frequency, $B_m$ = peak flux density, $V$ = core volume.

**How to reduce:** Use high-grade silicon steel (CRGO or HRGO) which has a narrow hysteresis loop (low $K_h$). Lamination does NOT reduce hysteresis loss.

**Eddy Current Loss:**

The alternating flux induces EMFs in the conducting iron core itself (by Faraday's law). These drive circulating currents (eddy currents) within the core, which cause $I^2R$ heating.

$$P_e = K_e \cdot f^2 \cdot B_m^2 \cdot t^2 \cdot V_{\text{core}}$$

where $t$ = thickness of the conducting path (lamination thickness).

**How to reduce:** Laminate the core into thin insulated sheets. Since $P_e \propto t^2$, halving the lamination thickness reduces eddy loss by 75%.

**Comparison:**

| Feature | Hysteresis Loss | Eddy Current Loss |
|:---|:---|:---|
| Cause | Domain reversal | Circulating currents in core |
| Depends on | $f \cdot B_m^{1.6}$ | $f^2 \cdot B_m^2 \cdot t^2$ |
| Reduced by | Better core material (Si steel) | Lamination (thinner sheets) |
| Frequency dependence | Linear with $f$ | Quadratic with $f$ |

---

### 🎯 Q3: What happens when a transformer is first connected to the power line? Can it be mitigated?
> **Appeared:** 2017 Q8(b) — 4 marks

**Full Answer:**

When a transformer is first energized, a large transient current called **magnetizing inrush current** flows, which can be 8–15 times the rated full-load current.

**Why it happens:** At the instant of switching, the core may have residual (remnant) flux from previous energization. If switching occurs at the voltage zero-crossing, the instantaneous voltage is zero but the required flux to balance the rising voltage starts from a non-zero residual value. The flux must reach values far above the normal peak (up to $2\Phi_m + \Phi_{residual}$), driving the core deep into saturation. Saturated core has very low inductance, so current spikes to very large values. The inrush decays over several cycles as the transient flux component dies out due to winding resistance.

**Mitigation methods:**

**(1) Pre-insertion resistors:** Insert a resistance in series with the primary at the moment of switching. This limits the inrush current. The resistor is bypassed after a few cycles when the transient has died out.

**(2) Controlled (point-on-wave) switching:** Use circuit breakers that close at the voltage peak instead of zero-crossing. At voltage peak, the required flux starts from zero (not from maximum), minimizing the flux offset and hence the inrush.

**(3) Soft-start relays:** Monitor the current waveform asymmetry (inrush has a DC offset) to distinguish inrush from a genuine fault current, preventing false tripping of protection devices.

---

### 🎯 Q4: Classify transformers at a glance.
> **Appeared:** 2018 Q1(a) — 2 marks

**Full Answer:**

| Classification Basis | Types |
|:---|:---|
| **By voltage** | Step-up ($N_2 > N_1$, voltage increases) and Step-down ($N_2 < N_1$, voltage decreases) |
| **By construction** | Core-type (windings surround core) and Shell-type (core surrounds windings) |
| **By number of windings** | Two-winding, Auto-transformer (single winding with tap), Three-winding |
| **By cooling** | Oil-immersed (ONAN, ONAF, OFAF) and Dry-type (air-cooled) |
| **By application** | Power transformer (generation/transmission), Distribution transformer (consumer supply), Instrument transformer (CT, PT) |
| **By phases** | Single-phase and Three-phase |

---

### 🎯 Q5: What is an instrument transformer? Explain the Potential Transformer (PT).
> **Appeared:** 2017 Q8(a) — 3 marks

**Full Answer:**

**Instrument transformer:** A transformer designed specifically to scale high voltages or currents down to safe, measurable levels for instruments (voltmeters, ammeters, energy meters, relays). They provide electrical isolation between the high-power circuit and the measuring instruments.

Two types:
- **Potential Transformer (PT):** For voltage measurement
- **Current Transformer (CT):** For current measurement

**Potential Transformer (PT):**

A step-down transformer. The primary is connected across the high-voltage circuit to be measured. The secondary (usually rated 110V or 120V) is connected to a voltmeter or voltage relay.

The high-voltage side is insulated to withstand the full line voltage. The actual circuit voltage = voltmeter reading × PT ratio.

**Key rule:** The secondary of a PT must **never be short-circuited** (would cause excessive current and damage).

Compare with CT: The secondary of a CT must **never be open-circuited** (would cause dangerous voltage buildup across the secondary winding).

---

### 🎯 Q6: Describe the effect of frequency and flux on a transformer.
> **Appeared:** 2018 Q1(b) — 2 marks, 2017 Q7(c) — 4 marks

**Full Answer:**

From the EMF equation: $E = 4.44 f N \Phi_m$. Therefore $\Phi_m = V/(4.44 f N)$.

**Effect of frequency (voltage constant):**

If supply voltage $V_1$ is held constant and frequency $f$ increases:
- $\Phi_m$ decreases (inversely proportional to $f$)
- Lower flux means lower iron losses (both $P_h \propto f B_m^{1.6}$ and $P_e \propto f^2 B_m^2$ decrease because $B_m$ drops faster)
- Lower magnetizing current
- But leakage reactance $X = 2\pi f L$ increases, causing more reactive voltage drop

If frequency decreases (voltage constant):
- $\Phi_m$ increases. Core may saturate.
- Iron losses increase sharply
- Magnetizing current rises

**Numerical example (PYQ 2017 Q7(c)):** An 18 kVA, 20000/480V, 60 Hz transformer used at 50 Hz to supply a 15 kVA, 415 V load.

From the EMF equation, core flux is proportional to voltage over frequency:
$$\Phi_m \propto \frac{V}{f}$$

- **If operated at full rated voltage (20,000 V) at 50 Hz:**
  $$\frac{\Phi_{m,50}}{\Phi_{m,60}} = \frac{60}{50} = 1.20$$
  Core flux increases by 20%. This drives the core deep into magnetic saturation. Magnetizing current spikes dramatically, causing core overheating. It cannot operate safely at full rated voltage.

- **To prevent saturation, voltage must be derated ($V/f = \text{constant}$):**
  Scaling voltage by $50/60$ keeps core flux constant:
  $$V_{1,50} = 20000 \times \frac{50}{60} = 16667\text{ V}, \qquad V_{2,50} = 480 \times \frac{50}{60} = 400\text{ V}$$
  Rated current depends on conductor size, so it stays unchanged. The thermal kVA capacity drops with voltage:
  $$S_{50} = S_{60} \times \frac{50}{60} = 18 \times \frac{50}{60} = \boxed{15\text{ kVA}}$$

**Conclusion:** Yes, the transformer can safely supply 15 kVA, but only if the supply voltage is derated to 16.67 kV. This yields 400 V on the secondary (close to the 415 V load) at 100% of its derated thermal capacity.

### 🎯 Q7: Enlist some practical applications of transformer.
> **Appeared:** 2024 Q1(a) — 2 marks

**Full Answer:**

1. **Step-up in generating stations:** raise generator voltage to a high value for economical transmission (lower $I^2R$ loss).
2. **Step-down in receiving substations:** reduce the transmission voltage to distribution levels for consumer use.
3. **Interconnecting two systems of different voltages** (e.g. 400 kV with 345 kV) using auto-transformers.
4. **Voltage matching for instruments:** potential transformer for voltmeters, current transformer for ammeters and relays. They also give electrical isolation.
5. **Furnace and welding supplies:** arc-furnace and spot-welding transformers give the large low-voltage, high-current supply needed.
6. **Frequency/voltage control:** variacs in laboratories, and stabilizers for sensitive equipment.

Two marks means four or five clean one-liners. Do not write an essay.

---

---

## ⚡ Exam Tips & Common Mistakes

1. **kVA rating:** Many students write "because power factor varies." That is correct but incomplete. State explicitly: "Losses depend on V and I, not on cos φ."
2. **Hysteresis is reduced by material choice (Si steel), NOT by lamination.** Lamination reduces eddy current loss only.
3. **CT secondary must never be opened. PT secondary must never be shorted.** Don't confuse these.
4. **For inrush current, the worst case is switching at voltage zero-crossing** with maximum residual flux.

## 🔗 Related Topics

- [T-01: Fundamentals](T-01_Transformer_Fundamentals.md) — EMF equation and frequency dependence
- [T-02: Construction](T-02_Construction.md) — Lamination and core losses
- [T-06c: Efficiency](T-06c_Efficiency.md) — Loss calculations
- [T-10: Auto-Transformer](T-10_Auto_Transformer.md) — Special transformer type

---

[← T-10: Auto-Transformer](T-10_Auto_Transformer.md) | [🏠 Index](00_Index.md) | [T-12: Rotating Magnetic Field →](T-12_Rotating_Magnetic_Field.md)
