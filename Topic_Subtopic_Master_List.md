# ECE 2207 — Master Topic & Subtopic List

> **Purpose:** Single reference for writing boss notes and sorting exam questions.
> **Sources cross-referenced:**
> - [Syllabus.md](Syllabus.md)
> - [SlidesByMaam/map.md](SlidesByMaam/map.md) (L-01 to L-11)
> - [ECE_2207_Question_Analysis.md](ECE_2207_Question_Analysis.md) (7 years: 2017–2024)

---

## How to Read This Document

- **Section** = Exam section (A or B)
- **Chapter** = Syllabus chapter
- **Topic** = Major topic heading (use for boss note file names / question folders)
- **Subtopic** = Leaf-level item (use for individual note sections / question tags)
- **Priority** = Exam frequency from 7-year analysis:
  - 🔴 **MUST** — Appeared 5+ times or every year
  - 🟠 **HIGH** — Appeared 3–4 times
  - 🟡 **MEDIUM** — Appeared 2 times
  - 🟢 **LOW** — Appeared 0–1 times
- **Slides** = Faculty lecture reference
- **Books** = Textbook chapter/section reference
- Topics are listed in **learning order** (prerequisites first), not alphabetical order.

---

## SECTION A — Transformer (Q1–Q4)

### Chapter 1: Transformer

#### 1.1 Transformer Fundamentals & Principle of Action
**Slides:** L-08 | **Books:** Theraja Ch-32, Chapman Ch-2

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.1.1 | What is a transformer — definition, static machine, mutual induction | 🟢 LOW | L-08 S04 | Basic definition, rarely asked standalone |
| 1.1.2 | Transformer action with DC (transient) — why transformers don't work on DC | 🟢 LOW | L-08 S09–S12 | Conceptual, asked in '19 |
| 1.1.3 | Transformer action with AC — sinusoidal flux, Faraday's law | 🟠 HIGH | L-08 S13 | Foundation for EMF equation |
| 1.1.4 | **EMF equation derivation** — $E = 4.44 f N \Phi_m$ | 🟠 HIGH | L-08 S14 | Asked in '19, '21, '23, '24 (4/7) |
| 1.1.5 | Transformation ratio $K = N_2/N_1 = E_2/E_1$ | 🟢 LOW | L-08 S14 | Always embedded in other questions |
| 1.1.6 | Ideal transformer properties | 🟡 MEDIUM | — | Asked in '21, '24 |
| 1.1.7 | Transformer classification (step-up, step-down, power, distribution, instrument) | 🟢 LOW | L-08 S05–S06 | Asked once ('18) |
| 1.1.8 | Transformer efficiency — why 95–99% (no moving parts) | 🟢 LOW | L-08 S08 | Conceptual filler |

#### 1.2 Transformer Construction
**Slides:** L-09 S03 | **Books:** Theraja Ch-32

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.2.1 | Core type vs shell type construction | 🟢 LOW | L-09 S03 | Asked once ('19, shell-type economy) |
| 1.2.2 | Laminated silicon steel core — purpose (reduce eddy currents) | 🟢 LOW | L-09 S03 | Asked once ('20) |
| 1.2.3 | Transformer breathing | 🟢 LOW | — | Asked once ('19) |

#### 1.3 No-Load Operation & Phasor Diagrams
**Slides:** L-09 S04–S13 | **Books:** Theraja Ch-32 (Art. 32.6–32.15)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.3.1 | No-load current $I_0$ — magnetizing component $I_\mu$ and core-loss component $I_w$ | 🟠 HIGH | L-09 S05–S06 | Asked in '19, '20, '24 (3/7) |
| 1.3.2 | No-load phasor diagram construction | 🟠 HIGH | L-09 S07–S08 | Part of phasor diagram questions |
| 1.3.3 | No-load power = iron loss: $W_0 = V_1 I_0 \cos\varphi_0$ | 🟠 HIGH | L-09 S08 | Tested via OC test numericals |
| 1.3.4 | Magnetizing current — why non-sinusoidal (peaked flux → flat-topped current) | 🟢 LOW | — | Asked once ('24) |
| 1.3.5 | **Phasor diagram under load** — unity, lagging, leading power factor | 🟠 HIGH | L-09 S10–S12 | Asked in '17, '18, '21, '24 (4/7) |
| 1.3.6 | Primary current decomposition: $\vec{I_1} = \vec{I_0} + \vec{I_2'}$ | 🟠 HIGH | L-09 S10 | Always part of loaded phasor |

#### 1.4 Equivalent Circuit
**Slides:** L-10 S03–S13 | **Books:** Theraja Ch-32 (Art. 32.16–32.20)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.4.1 | Leakage flux & leakage reactance concept ($X_1$, $X_2$) | 🟡 MEDIUM | L-10 S03–S05 | Conceptual prerequisite |
| 1.4.2 | Winding impedances: $Z_1 = R_1 + jX_1$, $Z_2 = R_2 + jX_2$ | 🟠 HIGH | L-10 S06 | Part of eq. circuit derivation |
| 1.4.3 | **Referring impedances** — $R_{01}, X_{01}$ (to primary), $R_{02}, X_{02}$ (to secondary) | 🟠 HIGH | L-10 S09–S10 | Core of eq. circuit, asked 4/7 |
| 1.4.4 | **Exact equivalent circuit** — complete diagram with $R_0$, $X_0$ shunt branch | 🟠 HIGH | L-10 S12 | Asked in '17, '18, '20, '24 |
| 1.4.5 | Approximate equivalent circuit — shunt branch moved to input | 🟠 HIGH | L-10 S13 | Simplified version for calculations |

#### 1.5 Voltage Regulation
**Slides:** L-10 S16 | **Books:** Theraja Ch-32 (Art. 32.22)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.5.1 | **Voltage regulation definition** — $VR = \frac{V_{2,nl} - V_{2,fl}}{V_{2,fl}} \times 100\%$ | 🔴 MUST | L-10 S16 | Asked in '18, '19, '21, '23, '24 (5/7) |
| 1.5.2 | **Approximate VR formula** — $VR \approx \frac{I_2(R_{02}\cos\varphi \pm X_{02}\sin\varphi)}{V_{2,fl}}$ | 🔴 MUST | L-10 S16 | + for lag, − for lead |
| 1.5.3 | VR at lagging, leading, unity pf — derive and compare | 🔴 MUST | L-10 S16 | Lagging → positive VR, leading → can be negative |

#### 1.6 Transformer Testing — OC & SC Tests
**Slides:** L-10 S17–S18 | **Books:** Theraja Ch-32 (Art. 32.23–32.28)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.6.1 | **Open-circuit (OC) test** — procedure, LV side, find $R_0$, $X_0$, iron loss | 🔴 MUST | L-10 S17 | **ALL 7 papers** 🔥 |
| 1.6.2 | **Short-circuit (SC) test** — procedure, HV side, find $R_{01}$, $X_{01}$, Cu loss | 🔴 MUST | L-10 S18 | **ALL 7 papers** 🔥 |
| 1.6.3 | Why OC test on LV side, SC test on HV side | 🟢 LOW | L-10 S17–S18 | Asked in '24 — new pattern |
| 1.6.4 | **OC/SC data → equivalent circuit parameters (numerical)** | 🔴 MUST | L-10 S19 | Ties with Open-Δ as the most certain question (both 7/7) |
| 1.6.5 | Hysteresis & eddy current losses | 🟢 LOW | — | Asked once ('17) |
| 1.6.6 | Inrush current when first connected | 🟢 LOW | — | Asked once ('17) |

#### 1.7 Transformer Efficiency
**Slides:** L-08 S08, L-10 S19 | **Books:** Theraja Ch-32 (Art. 32.29–32.34)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.7.1 | **Efficiency formula** — $\eta = \frac{x \cdot S \cdot \cos\varphi}{x \cdot S \cdot \cos\varphi + P_i + x^2 P_{cu}}$ | 🟠 HIGH | L-10 S19 | Asked in '17, '18, '19, '23 (4/7) |
| 1.7.2 | Efficiency at half load, full load, various pf (numerical) | 🟠 HIGH | L-10 S19 | Standard numerical pattern |
| 1.7.3 | **Condition for maximum efficiency** — Cu loss = Fe loss, derive | 🟡 MEDIUM | — | Asked in '19, '23 |
| 1.7.4 | **All-day efficiency** — energy efficiency with load schedule | 🟡 MEDIUM | — | Asked in '18, '19, '23 (3/7) |

#### 1.8 Three-Phase Transformer Connections
**Slides:** L-11 S03–S14 | **Books:** Theraja Ch-33

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.8.1 | Why 3-φ transformers — bank of three 1-φ vs single 3-φ unit | 🟢 LOW | L-11 S03–S05 | Conceptual intro |
| 1.8.2 | Y-Y connection — voltage/current relations | 🟡 MEDIUM | L-11 S07 | Asked in '19, '24 |
| 1.8.3 | **Y-Y limitations** — floating neutral, 3rd harmonic distortion, solutions | 🟡 MEDIUM | L-11 S08–S09 | Asked in '21, '23 |
| 1.8.4 | Y-Δ connection — relations, step-down use | 🟡 MEDIUM | L-11 S11–S12 | Part of 3-φ connection questions |
| 1.8.5 | Δ-Y connection — relations, step-up use, 30° phase shift | 🟡 MEDIUM | L-11 S13 | Part of 3-φ connection questions |
| 1.8.6 | Δ-Δ connection — no phase shift, handles unbalance | 🟡 MEDIUM | L-11 S14 | Gateway to Open-Δ |
| 1.8.7 | **Open-Δ (V-V) connection** — continuity of supply when one unit fails | 🔴 MUST | L-11 S16 | Asked 7/7 papers 🔥 |
| 1.8.8 | **Open-Δ capacity = 57.7% of closed-Δ — proof** | 🔴 MUST | L-11 S17–S18 | Ties with OC/SC as the most repeated question (7/7) |
| 1.8.9 | Open-Δ utilization factor = 86.6% | 🔴 MUST | L-11 S18 | Always paired with 57.7% proof |
| 1.8.10 | **Parallel operation conditions** for 3-φ transformers | 🟡 MEDIUM | — | Asked in '17, '21, '23 (3/7) |

#### 1.9 Phase Conversion — Scott (T-T) Connection
**Slides:** L-11 S21–S24 | **Books:** Theraja Ch-33

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.9.1 | **Scott connection** — 3-φ to 2-φ conversion principle | 🟡 MEDIUM | L-11 S21 | Asked in '18, '19, '24 (3/7) |
| 1.9.2 | Main transformer (50% center tap) + Teaser transformer (86.6% tap) | 🟡 MEDIUM | L-11 S22 | Hardware topology |
| 1.9.3 | Scott-T phasor proof — teaser voltage at 90° to main | 🟡 MEDIUM | L-11 S23 | Mathematical proof |
| 1.9.4 | Scott connection numerical — coil ratings, KVA calculation | 🟡 MEDIUM | L-11 S23 | Repeated numerical ('18, '24) |
| 1.9.5 | Three-phase T-connection (3-φ to 3-φ) | 🟢 LOW | L-11 S24 | Rarely asked |

#### 1.10 Vector Groups
**Slides:** L-11 S25–S29 | **Books:** Theraja Ch-33

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.10.1 | Vector group definition — phase displacement between HV & LV | 🟡 MEDIUM | L-11 S25 | Asked in '19, '21 |
| 1.10.2 | Clock representation — each hour = 30° | 🟡 MEDIUM | L-11 S26 | |
| 1.10.3 | Nomenclature — D/Y/d/y/z/n, four standard groups | 🟡 MEDIUM | L-11 S27 | |
| 1.10.4 | Dyn11 example — connection, clock diagram | 🟡 MEDIUM | L-11 S28–S29 | In syllabus, under-tested |

#### 1.11 Auto-Transformer
**Slides:** — | **Books:** Theraja Ch-32 (Art. 32.38)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 1.11.1 | Auto-transformer principle — single winding, conduction + induction | 🟡 MEDIUM | — | Asked in '20, '23 |
| 1.11.2 | **Copper saving proof** — saving = $(1-K)$ fraction | 🟡 MEDIUM | — | Derivation asked in '20, '23 |

---

## SECTION B — Induction Motors (Q5–Q8)

### Chapter 2: Three-Phase Induction Motor

#### 2.1 Rotating Magnetic Field (RMF)
**Slides:** L-01 (foundations), L-02 | **Books:** Theraja Ch-34 (Art. 34.1–34.5)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.1.1 | Magnetic field as medium of energy conversion (Faraday, Lorentz, Fleming) | 🟢 LOW | L-01 S04–S11 | Foundation concepts |
| 2.1.2 | AC motor types — synchronous vs asynchronous (induction) | 🟢 LOW | L-02 S04 | |
| 2.1.3 | IM construction — stator, rotor (squirrel-cage vs wound/slip-ring) | 🟢 LOW | L-02 S03, S06 | |
| 2.1.4 | IM advantages & disadvantages | 🟢 LOW | L-02 S07 | |
| 2.1.5 | Flux revolving theory — how multi-phase currents produce rotating field | 🔴 MUST | L-02 S08 | Conceptual foundation |
| 2.1.6 | 2-φ RMF — mathematical proof ($\Phi_R = \Phi_m$, constant magnitude) | 🟠 HIGH | L-02 S09–S11 | Part of RMF proof questions |
| 2.1.7 | **3-φ RMF — mathematical proof** ($\Phi_R = 1.5\Phi_m$, rotates at $N_s$) | 🔴 MUST | L-02 S12–S14 | Asked 5/7 papers 🔥 |
| 2.1.8 | Synchronous speed equation: $N_s = 120f/P$ | 🔴 MUST | L-03 S03 | Foundation for everything |

#### 2.2 Slip & Basic Principles
**Slides:** L-03 S04–S09 | **Books:** Theraja Ch-34 (Art. 34.6–34.10)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.2.1 | Why rotor rotates — relative velocity, induced EMF, Lenz's law | 🟠 HIGH | L-03 S04–S05 | Foundation for slip |
| 2.2.2 | **Slip definition** — $s = (N_s - N)/N_s$, $N = N_s(1-s)$ | 🟠 HIGH | L-03 S06–S07 | Asked 4/7 papers |
| 2.2.3 | **Why IM can't run at $N_s$** — proof (no relative speed → no EMF → no torque) | 🔴 MUST | L-03 S05 | Asked in '20, '21, '23, '24 |
| 2.2.4 | Rotor frequency: $f_r = sf$ | 🟠 HIGH | L-03 S08 | Tested in slip numericals |
| 2.2.5 | **Why IM = rotating transformer** | 🟡 MEDIUM | L-03 S10 | Asked in '17, '19, '20 (3/7) |

#### 2.3 Equivalent Circuit of IM
**Slides:** L-03 S11–S20 | **Books:** Theraja Ch-34, Chapman Ch-7

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.3.1 | Stator & rotor quantities — standstill vs running ($E_r = sE_2$, $X_r = sX_2$) | 🟠 HIGH | L-03 S11 | |
| 2.3.2 | No-load stator current $I_0$ — $I_w$ and $I_\mu$ components | 🟠 HIGH | L-03 S12 | Same concept as transformer |
| 2.3.3 | Rotor current: $I_2 = \frac{sE_2}{\sqrt{R_2^2 + (sX_2)^2}}$ | 🟠 HIGH | L-03 S16 | |
| 2.3.4 | $R_2/s$ decomposition: $R_2 + R_2(1-s)/s$ — copper loss + mechanical load | 🟠 HIGH | L-03 S18 | Key insight for circuit |
| 2.3.5 | Referring rotor parameters to stator ($R_2', X_2'$ using $a_{eff}$) | 🟠 HIGH | L-03 S19 | |
| 2.3.6 | **Complete per-phase equivalent circuit** — stator + shunt + referred rotor | 🟠 HIGH | L-03 S20 | Asked in '17, '20, '23 (3/7) |

#### 2.4 Torque Equations & Characteristics
**Slides:** L-04 | **Books:** Theraja Ch-34 (Art. 34.18–34.30)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.4.1 | Torque proportionality: $T \propto \Phi I_2 \cos\varphi_2 \propto E_2 I_2 \cos\varphi_2$ | 🟠 HIGH | L-04 S03 | |
| 2.4.2 | **Starting torque** derivation ($s=1$): $T_{st} = \frac{K_1 E_2^2 R_2}{R_2^2 + X_2^2}$ | 🟠 HIGH | L-04 S04–S05 | |
| 2.4.3 | **Condition for max starting torque**: $R_2 = X_2$ | 🟠 HIGH | L-04 S06 | |
| 2.4.4 | **Running torque** equation: $T_r = \frac{K_1 s E_2^2 R_2}{R_2^2 + (sX_2)^2}$ | 🟠 HIGH | L-04 S08–S10 | |
| 2.4.5 | **Maximum torque (breakdown)** derivation: $s_{max} = R_2/X_2$ | 🟠 HIGH | L-04 S12–S13 | Asked 4/7 papers |
| 2.4.6 | **Breakdown torque formula**: $T_{max} = \frac{K_1 E_2^2}{2X_2}$ — independent of $R_2$ | 🟠 HIGH | L-04 S14 | |
| 2.4.7 | **$T_{max}/T_f$ ratio** — numerical problem (nearly identical data repeated) | 🟠 HIGH | L-04 S14 | Asked in '17, '19, '24 |
| 2.4.8 | **Torque-slip characteristic** — low slip (linear) vs high slip (hyperbolic) | 🟠 HIGH | L-04 S15–S16 | Asked 4/7 papers |
| 2.4.9 | **Torque-speed curves** — family of curves for varying $R_2$ | 🟠 HIGH | L-04 S17 | Effect of $R_2$ on $T$-$s$ curve |
| 2.4.10 | Effect of changing $R_2$ and $X_2$ on torque-speed curves | 🟡 MEDIUM | L-04 S17 | In syllabus, under-tested ⚠️ |

#### 2.5 Power Flow & Rotor Power Division
**Slides:** L-06 S03–S10 | **Books:** Theraja Ch-34 (Art. 34.33–34.38)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.5.1 | Power flow diagram — input → stator losses → air-gap → rotor Cu loss → mechanical | 🟡 MEDIUM | L-06 S03–S04 | Asked in '18, '20 |
| 2.5.2 | **Golden power ratio**: $P_g : P_{cu,rotor} : P_{dev} = 1 : s : (1-s)$ | 🟡 MEDIUM | L-06 S05 | Key relationship |
| 2.5.3 | Developed torque: $T_d = P_g / \omega_s = P_{dev} / \omega_m$ | 🟡 MEDIUM | L-06 S06 | |
| 2.5.4 | Shaft power: $P_{out} = P_{dev} - P_{f\&w} - P_{stray}$ | 🟢 LOW | L-06 S07 | |
| 2.5.5 | **Synchronous watt** — definition and concept | 🟡 MEDIUM | L-06 S10 | Asked in '21, '23 |
| 2.5.6 | Rotor efficiency $\eta_{rotor} = (1-s)$ | 🟡 MEDIUM | L-06 S05 | Asked in '21, '23 |

#### 2.6 IM Testing & Parameter Determination
**Slides:** L-05 | **Books:** Theraja Ch-35, Chapman Ch-7

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.6.1 | No-load test — concept, equivalent circuit ($R_2/s \to \infty$), find $X_M$, $R_c$, losses | 🟠 HIGH | L-05 S04–S08 | Circle diagram input |
| 2.6.2 | Loss separation — $P_{rot} = P_{NL} - 3I_{NL}^2 R_1$ | 🟡 MEDIUM | L-05 S07–S08 | |
| 2.6.3 | Blocked-rotor test — $s=1$, find $R_{BR}$, $X_{BR}$, frequency correction | 🟠 HIGH | L-05 S09–S11 | Circle diagram input |
| 2.6.4 | DC stator resistance test — Y: $R_1 = R_{DC}/2$, Δ: $R_1 = 1.5R_{DC}$ | 🟡 MEDIUM | L-05 S12–S14 | |
| 2.6.5 | Complete parameter determination — worked numerical | 🟠 HIGH | L-05 S15 | 40-hp motor example |

#### 2.7 Starting Methods
**Slides:** L-06 S11–S20 | **Books:** Theraja Ch-34 (Art. 34.39–34.44)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.7.1 | Starting problem — why $I_{st} = 5$–$8 \times I_{FL}$ is dangerous | 🟢 LOW | L-06 S11 | Motivation |
| 2.7.2 | Direct-on-line (DOL) starting — limited to small motors (<5 kW) | 🟢 LOW | L-06 S12 | Asked once ('19) |
| 2.7.3 | Primary resistor / reactor starting | 🟢 LOW | L-06 S14 | |
| 2.7.4 | Auto-transformer starting — $I_{st} = x^2 I_{sc}$, $T_{st} = x^2 T_{sc}$ | 🟡 MEDIUM | L-06 S15–S17 | |
| 2.7.5 | **Star-delta (Y-Δ) starter** — $I_{st} = \frac{1}{3}I_{sc,\Delta}$, $T_{st} = \frac{1}{3}T_{sc,\Delta}$ | 🟡 MEDIUM | L-06 S18 | Asked in '18, '20, '23 (3/7) |
| 2.7.6 | Slip-ring motor — rotor rheostat starting ($R_2 + R_{ext} \approx X_2$) | 🟢 LOW | L-06 S19–S20 | |

#### 2.8 Speed Control
**Slides:** L-07 S03–S05 | **Books:** Theraja Ch-35 (Art. 35.18)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.8.1 | **Speed control methods** — stator side (voltage, V/f, pole changing, external impedance) | 🟠 HIGH | L-07 S03 | Asked in '17, '19, '23 (3/7) |
| 2.8.2 | Speed control — rotor side (external resistance, cascade, slip-frequency injection) | 🟡 MEDIUM | L-07 S03 | |
| 2.8.3 | Rotor resistance speed control — numerical (external $R$ for speed reduction) | 🟢 LOW | L-07 S05 | Asked once ('21) |

#### 2.9 Electric Braking
**Slides:** L-07 S06–S09 | **Books:** Theraja Ch-35

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.9.1 | Dynamic braking — motor runs as loaded generator | 🟡 MEDIUM | L-07 S06 | Part of braking definitions |
| 2.9.2 | DC injection braking — stator fed DC, stationary field | 🟡 MEDIUM | L-07 S07 | |
| 2.9.3 | Capacitor braking — self-excited generator mode | 🟢 LOW | L-07 S08 | |
| 2.9.4 | **Plugging** — reverse two stator leads, $s \approx 2$ | 🟠 HIGH | L-07 S09 | Asked 4/7 papers ('17–'20) |

#### 2.10 Induction Generator
**Slides:** L-07 S10–S12 | **Books:** Theraja Ch-34 (Art. 34.47)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.10.1 | **IM as induction generator** — driven above $N_s$, $s < 0$, delivers active power, absorbs VARs | 🟡 MEDIUM | L-07 S10–S11 | Rising trend 📈 ('18, '23, '24) |
| 2.10.2 | Grid-connected induction generator | 🟢 LOW | L-07 S11 | |
| 2.10.3 | Self-excited induction generator (SEIG) — shunt capacitor excitation | 🟡 MEDIUM | L-07 S12 | |
| 2.10.4 | Capacitance calculation for IG (numerical) | 🟡 MEDIUM | — | Repeated numerical ('18, '24) |

#### 2.11 Circle Diagram
**Slides:** L-07 S22–S24 | **Books:** Theraja Ch-35 (Art. 35.3–35.9)

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 2.11.1 | Circle diagram fundamentals — locus of IM current | 🟠 HIGH | L-07 S22 | |
| 2.11.2 | **Construction** — from NL test ($I_0, \cos\varphi_0$) and BR test ($I_{BR}, \cos\varphi_{BR}$) | 🟠 HIGH | L-07 S23 | Asked 4/7 papers ('17–'21) |
| 2.11.3 | Parameter extraction — max output, max torque, slip, η, pf | 🟠 HIGH | L-07 S24 | |
| 2.11.4 | Circle diagram numerical — complete problem | 🟠 HIGH | L-07 S24 | Declining trend — absent '23, '24 |

---

### Chapter 3: Single-Phase Induction Motor

#### 3.1 Theory of Operation
**Slides:** L-07 S15–S17 | **Books:** Theraja Ch-36

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 3.1.1 | Single-phase pulsating field — alternates along one axis, no rotation | 🔴 MUST | L-07 S15 | Prerequisite for DFRT |
| 3.1.2 | **1-φ IM is NOT self-starting** — $T_{st} = 0$, explain why | 🟡 MEDIUM | L-07 S15 | Asked in '17, '19 |
| 3.1.3 | **Double field revolving theory (DFRT)** — $\Phi_m\cos\omega t$ splits into two $\frac{\Phi_m}{2}$ rotating in opposite directions | 🔴 MUST | L-07 S16 | Asked 5/7 papers 🔥 |
| 3.1.4 | DFRT slip analysis — $s_f = s$, $s_b = 2-s$; at standstill $s_f = s_b = 1 \implies T_f = T_b \implies T_{net} = 0$ | 🔴 MUST | L-07 S16 | Core of the derivation |
| 3.1.5 | Making 1-φ IM self-starting — auxiliary winding at 90° for temporary 2-φ operation | 🔴 MUST | L-07 S17 | Bridge to starting methods |

#### 3.2 Starting Methods for 1-φ IM
**Slides:** L-07 S18–S21 | **Books:** Theraja Ch-36

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 3.2.1 | **Split-phase motor** — main (low R, high X) + auxiliary (high R, low X), ~30° phase split, centrifugal switch | 🔴 MUST | L-07 S18 | Asked 6/7 papers 🔥 |
| 3.2.2 | **Capacitor-start induction-run motor** — capacitor in series with auxiliary, ~80° split, high $T_{st}$ (3–4× $T_{fl}$), centrifugal switch | 🔴 MUST | L-07 S19 | Most commonly asked type |
| 3.2.3 | Phasor diagram comparison — split-phase vs capacitor-start | 🟡 MEDIUM | L-07 S20 | Visual comparison |
| 3.2.4 | **Capacitor-start capacitor-run** — two capacitors (large electrolytic for start + small oil/paper for run) | 🟠 HIGH | L-07 S21 | |
| 3.2.5 | **Permanent split capacitor (PSC) motor** — single run capacitor, no centrifugal switch | 🟠 HIGH | L-07 S21 | |
| 3.2.6 | Shaded-pole motor | 🟢 LOW | — | In textbook, not in slides |
| 3.2.7 | Capacitor value for maximum starting torque (numerical) | 🟡 MEDIUM | — | Asked in '18, '21 |

#### 3.3 1-φ IM Equivalent Circuit
**Slides:** — | **Books:** Theraja Ch-36

| # | Subtopic | Priority | Slides | Notes |
|:--|:---------|:--------:|:------:|:------|
| 3.3.1 | 1-φ IM equivalent circuit — forward and backward branch model | 🟢 LOW | — | **NEVER asked** but in syllabus 🔴 Gap |
| 3.3.2 | 1-φ IM phasor/vector diagram | 🟢 LOW | — | Asked once ('24) |

---

## Quick-Reference: Topic Count Summary

| Chapter | Topics | Subtopics | 🔴 MUST | 🟠 HIGH | 🟡 MED | 🟢 LOW |
|:--------|:------:|:---------:|:-------:|:-------:|:------:|:------:|
| **Ch-1: Transformer** | 11 | 47 | 7 | 14 | 16 | 10 |
| **Ch-2: 3-φ IM** | 11 | 47 | 6 | 17 | 16 | 8 |
| **Ch-3: 1-φ IM** | 3 | 9 | 5 | 2 | 2 | 2† |
| **Total** | **25** | **103** | **18** | **33** | **34** | **20†** |

> †Includes 1-φ IM equivalent circuit — never tested but in syllabus.

---

## Recommended Learning Order (Start-to-Finish)

The syllabus lists Transformer first, but the teacher taught IM first (L-01→L-07, then L-08→L-11). Either order works — what matters is internal sequencing within each chapter. Below is the recommended order if you follow the exam section structure:

### Pass 1 — Section A (Transformer)
1. **1.1** Fundamentals & EMF equation
2. **1.2** Construction (light read)
3. **1.3** No-load operation & phasor diagrams
4. **1.4** Equivalent circuit (needs 1.1 + 1.3)
5. **1.5** Voltage regulation (needs 1.4)
6. **1.6** OC & SC tests (needs 1.4) + **1.7** Efficiency (needs 1.6)
7. **1.8** Three-phase connections + Open-Δ
8. **1.9** Scott connection + **1.10** Vector groups
9. **1.11** Auto-transformer

### Pass 2 — Section B (Induction Motor)
1. **2.1** Rotating magnetic field (needs nothing)
2. **2.2** Slip & basic principles (needs 2.1)
3. **2.3** IM equivalent circuit (needs 2.2)
4. **2.4** Torque equations & characteristics (needs 2.2 + 2.3)
5. **2.5** Power flow & rotor power division (needs 2.4)
6. **2.6** IM testing (needs 2.3)
7. **2.7** Starting methods (needs 2.4 for torque context)
8. **2.8** Speed control + **2.9** Braking (needs 2.4)
9. **2.10** Induction generator (needs 2.2)
10. **2.11** Circle diagram (needs 2.6)
11. **3.1** 1-φ IM theory — DFRT (needs 2.1)
12. **3.2** 1-φ IM starting methods (needs 3.1)
13. **3.3** 1-φ IM equivalent circuit (if time permits)

---

## Tagging Scheme for Question Sorting

Use the subtopic IDs (e.g., `1.6.1`, `2.4.5`) as tags when sorting previous year questions. Example mapping:

| Question | Tag(s) |
|:---------|:-------|
| "Derive EMF equation of transformer" | `1.1.4` |
| "OC/SC test data → find parameters" | `1.6.1`, `1.6.2`, `1.6.4` |
| "Prove 57.7% capacity of Open-Δ" | `1.8.8` |
| "Explain DFRT for 1-φ IM" | `3.1.3`, `3.1.4` |
| "Draw torque-speed curve" | `2.4.8` |
| "Derive max torque formula" | `2.4.5`, `2.4.6` |
