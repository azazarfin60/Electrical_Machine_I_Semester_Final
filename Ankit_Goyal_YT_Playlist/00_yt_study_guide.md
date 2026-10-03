# ECE 2207: Electrical Machine-I — YouTube Study Guide
## Ankit Goyal Playlist (Curated for ECE 2207)

> **Course**: ECE 2207 — Electrical Machine-I (3 Credits)  
> **Playlist**: Electrical Machines for GATE & ESE — Ankit Goyal Sir  
> **Lectures Kept**: 85 of 166 (81 out-of-scope lectures on DC Machines, Synchronous Machines, EM Energy Conversion, and Special Machines have been removed)  
> **Priorities cross-checked against**: [ECE_2207_Question_Analysis.md](../ECE_2207_Question_Analysis.md) (7 papers: 2017–2021, 2023, 2024)

---

## How to Use This Guide

Every lecture is tagged two ways. The tag says how much the topic matters. The badge says how often it was actually asked.

| Tag | Meaning | What to Do |
|:---:|---|---|
| 🔴 | **Exam-proven** — asked in 4 or more of the 7 papers | **Watch first.** Work every problem. |
| 🟢 | **Core** — in syllabus AND in maam's slides | **Must watch.** This will be tested. |
| 🟡 | **Secondary** — asked 1 to 3 times, or goes deeper than slides | **Watch if the topic feels weak.** |
| 🔵 | **Foundation** — prerequisite for understanding core topics | **Watch if fundamentals feel shaky.** |
| ⚪ | **Not asked** — absent from all 7 papers and not in syllabus | **Skip.** Kept for reference only. |

A badge like `(5/7)` means the topic appeared in 5 of the 7 papers analyzed. No badge means it has never been asked directly.

> [!IMPORTANT]
> **The ⚪ tags in the old version of this guide were wrong in four places.** Auto-transformer, parallel operation, non-sinusoidal magnetizing current, and inrush current were all marked "skip entirely". All four have appeared in real papers. They are now tagged 🟡. See Sections 1.7 and 1.10.

> [!TIP]
> **Recommended study order**: Part 0 (skim) → Part 2 (Induction Motor) → Part 1 (Transformer) → Part 3 (Single-Phase IM).  
> Induction Motor was covered first in class, so starting there aligns with your class notes.  
> **If you have under a week**, ignore that order and work straight down the Exam-First Watch List below.

---

## Exam-First Watch List 🔴

These 11 lectures cover every question pattern that has appeared 4 or more times. Watching only these covers roughly 60% of the marks on a typical paper.

### Section A — Transformer

| Lecture | Covers | Frequency |
|:---|:---|:---:|
| [021](Lecture_021_Testing_of_Transformer_1.md) + [023](Lecture_023_Problems_Based_on_Testing_of_Transformer.md) | OC & SC test, parameter extraction | **7/7 🔥** |
| [043](Lecture_043_Three_Phase_Transformer_5.md) + [046](Lecture_046_Problems_Based_on_Three_Phase_Transformers_3.md) | Open-Δ (V-V), 57.7% proof | **7/7 🔥** |
| [027](Lecture_027_Voltage_Regulation.md) + [028](Lecture_028_Problems_based_on_Voltage_Regulation_of_Transformer.md) | Voltage regulation, all power factors | **5/7** |
| [014](Lecture_014_Ideal_Transformer_Part_1.md) | EMF equation derivation | **4/7** |
| [019](Lecture_019_Practical_Transformer_Part_3.md) | Equivalent circuit, step by step | **4/7** |
| [017](Lecture_017_Practical_Transformer_Part_1.md) | Loaded phasor diagram, no-load current | **4/7** |
| [025](Lecture_025_Losses_and_Efficiency_Part_2.md) | Efficiency, max efficiency, all-day efficiency | **4/7** |

### Section B — Induction Motor

| Lecture | Covers | Frequency |
|:---|:---|:---:|
| [161](Lecture_161_Single_Phase_Induction_Motor_2.md) | 1-φ IM starting methods | **6/7 🔥** |
| [135](Lecture_135_Rotating_Magnetic_Field.md) | RMF proof, $\Phi_R = 1.5\Phi_m$ | **5/7 🔥** |
| [160](Lecture_160_Single_Phase_Induction_Motor_1.md) | Double field revolving theory | **5/7 🔥** |
| [133](Lecture_133_Induction_Machine_Construction_2.md) | Slip, why IM cannot reach $N_s$ | **4/7** |
| [140](Lecture_140_Torque_Slip_Characteristics_2.md) | Max torque, breakdown slip | **4/7** |
| [139](Lecture_139_Torque_Slip_Characteristics_1.md) | Torque-speed curve, all regions | **4/7** |
| [146](Lecture_146_Circle_Diagram_of_Induction_Motor.md) | Circle diagram from NL and BR data | **4/7** |

---

## Part 0: Foundations 🔵
**Lectures 001–010 | ~10 hours**

> These lectures build prerequisite knowledge. Not directly in the ECE 2207 syllabus, but the concepts (Faraday's law, magnetic circuits, etc.) are assumed knowledge for transformers and motors. **Skim or skip if you're already comfortable with these fundamentals.**

### [Lecture 001: Introduction to Electrical Machines](Lecture_001_Introduction_to_Electrical_Machines.md) `00:47:15`
- 🔵 Course overview and syllabus architecture
- 🔵 Machine families: Transformers, DC, Synchronous, Induction
- 🔵 Exam strategy and textbook recommendations

### [Lecture 002: Electrical Materials](Lecture_002_Electrical_Materials.md) `01:13:04`
- 🔵 Conducting materials — copper vs aluminium properties
- 🔵 Carbon brushes and contact voltage drop
- 🔵 Diamagnetic and paramagnetic materials — susceptibility, permeability

### [Lecture 003: Electrical Materials 2](Lecture_003_Electrical_Materials_2.md) `01:07:36`
- 🟡 Ferromagnetic materials — hysteresis loop, residual magnetism, coercive force `(1/7)` *(hysteresis loss asked in '17)*
- 🟡 Eddy current losses — lamination rationale `(1/7)` *(laminating core purpose asked in '20)*
- 🔵 Silicon steel — CRGO properties *(core material for transformers, covered in Slides L-09)*
- 🔵 Insulating materials and dielectric breakdown

### [Lecture 004: Laws of Electromagnetism 1](Lecture_004_Laws_of_Electromagnetism_1.md) `01:08:29`
- 🔵 Biot-Savart's law — magnetic field from current elements
- 🔵 Ampere's circuital law — solenoid field derivation
- 🔵 **Faraday's law** ($e = -N \frac{d\Phi}{dt}$) *(foundation of transformer action — Slides L-01 S09, L-08 S14)*
- 🔵 **Lenz's law** *(used in transformer phasor diagrams and rotor torque explanation)*
- 🔵 Statically induced EMF *(basis of transformer EMF equation)*

### [Lecture 005: Laws of Electromagnetism 2](Lecture_005_Laws_of_Electromagnetism_2.md) `01:03:20`
- 🔵 **Lorentz force** ($F = BIl\sin\theta$) *(basis of motor action — Slides L-01 S10)*
- 🔵 **Motional EMF** ($e = Blv\sin\theta$) *(basis of generator action — Slides L-01 S11)*
- 🔵 **Dot convention** *(used in transformer polarity and 3-phase connections)*
- 🔵 Force between parallel conductors

### [Lecture 006: Problems Based on Electromagnetic Laws](Lecture_006_Problems_Based_on_Electromagnetic_Laws.md) `01:08:40`
- 🔵 Practice problems on Faraday's law, motional EMF, Lorentz force
- 🔵 Magnetic circuit analogies *(leads into magnetic circuits)*

### [Lecture 007: Magnetic Circuits](Lecture_007_Magnetic_Circuits.md) `01:04:40`
- 🔵 **Magnetic circuit concept** — reluctance, MMF, Ohm's law analogy *(essential for transformer and motor equivalent circuits)*
- 🔵 Series and parallel reluctance combinations
- 🔵 Air gap fringing and leakage flux *(directly relevant to transformer leakage reactance — Slides L-10)*

### [Lecture 008: Problems based on Magnetic Circuits](Lecture_008_Problems_based_on_Magnetic_Circuits.md) `01:03:26`
- 🔵 Practice on magnetic circuit analysis
- 🔵 Hysteresis loss, permanent magnet properties

### [Lecture 009: Per Unit System](Lecture_009_Per_Unit_System.md) `00:47:29`
- 🔵 Per-unit formulas for single-phase and three-phase systems *(used in transformer parameter normalization)*
- 🔵 Base quantities, impedance scaling

### [Lecture 010: Problems Based on Per Unit Systems](Lecture_010_Problems_Based_on_Per_Unit_Systems.md) `00:49:40`
- 🔵 Practice problems on per-unit conversions

---

## Part 1: Transformer (Syllabus Chapter 1)
**Lectures 011–053 | Covers: Ideal Transformer, Actual Transformer, Three-Phase Transformer**

> **Syllabus scope**: Transformation ratio · No-load & load vector diagrams · Equivalent circuit · Voltage regulation · OC test · SC test · 3-phase connections · Vector groups · Phase conversion

---

### 1.1 Construction & Basics (011–013)

#### [Lecture 011: Transformer Construction 1](Lecture_011_Transformer_Construction_1.md) `01:14:32`
- 🟢 **Core-type vs Shell-type** construction *(Slides L-09 S03)*
- 🟡 Core materials — CRGO silicon steel, laminations `(1/7)` *(laminating core purpose asked in '20)*
- 🟡 Transformer classification `(1/7)` *(asked in '18)*
- 🟡 Cooling mechanisms, application domains — *not explicitly in slides*
- 🟡 Stacking factor, eddy current mitigation

#### [Lecture 012: Transformer Construction Part 2](Lecture_012_Transformer_Construction_Part_2.md) `01:07:28`
- 🟡 **Breathers and conservator tanks** `(1/7)` *(transformer breathing asked in '19 Q3a)*
- 🟡 Rectangular vs circular cross-section, stepped cores — *not in slides but deepens understanding*
- 🟡 Winding types: helical, crossover, disc, sandwich
- 🟡 Transformer oil functions, bushings

#### [Lecture 013: Problems based on Transformer Construction and Working](Lecture_013_Problems_based_on_Transformer_Construction_and_Working.md) `01:20:05`
- 🔴 EMF equation practice — net core area, turns allocation `(4/7)`
- 🟢 V/f control concept and frequency scaling `(2/7)` *(frequency and flux effects asked in '18)*
- ⚪ Three-winding transformer design — *not in syllabus*

---

### 1.2 Ideal Transformer (014–016)

#### [Lecture 014: Ideal Transformer Part 1](Lecture_014_Ideal_Transformer_Part_1.md) `01:04:38` 🔴
- 🔴 **EMF equation derivation**: $E = 4.44 f N \Phi_m$ `(4/7)` *(Slides L-08 S14)*
- 🟡 **Ideal transformer assumptions / properties** `(2/7)` *(asked in '21, '24; Slides L-08 S04)*
- 🟢 **Transformation ratio** $K = N_2/N_1$ *(Syllabus: transformation ratio)*
- 🔴 **No-load phasor diagram** `(4/7)` *(phasor diagram asked in '17, '18, '21, '24; Slides L-09 S05-S07)*

#### [Lecture 015: Ideal Transformer Part 2](Lecture_015_Ideal_Transformer_Part_2.md) `00:49:28`
- 🔴 **Load phasor diagrams** `(4/7)` *(Slides L-09 S10-S12)*
- 🟢 **MMF balancing**: $N_1 I_1 = N_2 I_2$ *(Slides L-09 S10)*
- 🟢 **Impedance referral** across windings *(Slides L-10 S09-S11)*
- 🟡 Dot convention and polarity — *useful context, not explicitly tested*
- 🟡 Complex power conservation

#### [Lecture 016: Problems Based on Ideal Transformer](Lecture_016_Problems_Based_on_Ideal_Transformer.md) `01:06:42`
- 🟢 Phasor and current problems — practice on transformation ratio
- 🟡 Impedance matching for max power transfer — *not in syllabus*
- ⚪ Three-winding transformer problems — *not in syllabus*
- ⚪ DC transformer operation limitations — *not in syllabus*

---

### 1.3 Practical / Actual Transformer (017–020)

#### [Lecture 017: Practical Transformer Part 1](Lecture_017_Practical_Transformer_Part_1.md) `01:04:23` 🔴
- 🟢 **No-load current components**: $I_\mu$ (magnetizing) and $I_w$ (core-loss) `(3/7)` *(Slides L-09 S05-S08)*
- 🟢 **No-load equivalent circuit** *(Slides L-09 S05-S08)*
- 🔴 **On-load phasor diagram** — demagnetization, reflected current `(4/7)` *(Slides L-09 S10-S12)*
- 🟢 $I_0 = \sqrt{I_\mu^2 + I_w^2}$ `(3/7)` *(identical numerical in '20 Q2d and '24 Q3c)*

#### [Lecture 018: Practical Transformer Part 2](Lecture_018_Practical_Transformer_Part_2.md) `00:54:24`
- 🟢 **Winding resistance** — KVL formulation *(Slides L-10 S06-S07)*
- 🟢 **Leakage flux** → leakage reactance $X_1, X_2$ *(Slides L-10 S03-S05)*
- 🔴 **Phasor diagram with resistance and leakage** `(4/7)` *(Slides L-10 S14-S15)*
- 🟢 Resistance referral: $R_{01} = R_1 + R_2/K^2$ *(Slides L-10 S09)*

#### [Lecture 019: Practical Transformer Part 3](Lecture_019_Practical_Transformer_Part_3.md) `01:10:45` 🔴
- 🔴 **Exact equivalent circuit** `(4/7)` *(step-by-step derivation asked in '17, '18, '20, '24; Slides L-10 S12)*
- 🔴 **Referred to primary / secondary** `(4/7)` *(Slides L-10 S09-S11)*
- 🟢 **Approximate equivalent circuit** — shunt branch shifted *(Slides L-10 S13)*
- 🟡 Per-unit equivalent circuit — *deeper than slides*
- 🟡 Worked numerical problem

#### [Lecture 020: Problems based on Equivalent Circuit](Lecture_020_Problems_based_on_Equivalent_Circuit.md) `01:17:16`
- 🟢 Load impedance reflection and terminal voltage problems
- 🟢 Efficiency evaluation from equivalent circuit
- 🟢 Short-circuit test concepts and impedance referral
- 🟡 Maximum power transfer in transformer networks — *not in syllabus*

---

### 1.4 Testing: OC & SC Tests (021–023) 🔴 **THE most certain question**

> [!IMPORTANT]
> OC/SC test appeared in **all 7 papers**. It ties with Open-Δ (also 7/7) as the most certain question in the exam. Do not sit the exam without working every numerical variant in Lecture 023.

#### [Lecture 021: Testing of Transformer 1](Lecture_021_Testing_of_Transformer_1.md) `00:52:53` 🔴
- 🔴 **Open-circuit (OC) test** — LV side, HV open `(7/7 🔥)` *(Syllabus: OC test; Slides L-10 S17)*
- 🔴 Extraction of $R_0, X_0$ from OC data `(7/7 🔥)`
- 🔴 **Short-circuit (SC) test** — HV side, LV shorted `(7/7 🔥)` *(Syllabus: SC test; Slides L-10 S18)*
- 🔴 Extraction of $R_{01}, X_{01}$ from SC data `(7/7 🔥)`
- 🟡 **Why the SC test runs on the HV side** `(1/7)` *(asked in '24 as a short conceptual question)*

#### [Lecture 022: Testing of Transformer Part 2](Lecture_022_Testing_of_Transformer_Part_2.md) `00:48:37`
- 🟡 Polarity test — *not in syllabus/slides but useful concept*
- ⚪ Sumpner's (back-to-back) test — *not in syllabus, never asked*
- ⚪ Phantom loading concept — *not in syllabus, never asked*

#### [Lecture 023: Problems Based on Testing of Transformer](Lecture_023_Problems_Based_on_Testing_of_Transformer.md) `01:14:06` 🔴
- 🔴 OC/SC test parameter extraction problems `(7/7 🔥)`
- 🔴 Terminal voltage and regulation calculations from test data `(5/7)`
- 🟢 Three-phase transformer testing problems
- ⚪ Sumpner's test problems — *not in syllabus, can skip*

---

### 1.5 Losses & Efficiency (024–026) 🟢

> [!NOTE]
> The old version of this guide tagged this section 🟡 because losses are not a named syllabus heading. **The papers disagree.** Efficiency calculation appeared 4 times, all-day efficiency 3 times, and the "max efficiency when Cu loss = Fe loss" proof twice. Treat this section as core.

#### [Lecture 024: Losses and Efficiency Part 1](Lecture_024_Losses_and_Efficiency_Part_1.md) `01:02:06`
- 🟡 Hysteresis loss — Steinmetz formula, dipole reversal mechanism `(1/7)` *(asked in '17)*
- 🟡 Eddy current loss derivation — lamination thickness relationship `(1/7)` *(asked in '17)*
- 🟡 Separation of core losses experimentally

#### [Lecture 025: Losses and Efficiency Part 2](Lecture_025_Losses_and_Efficiency_Part_2.md) `00:59:19` 🔴
- 🔴 **Transformer efficiency formula**: $\eta = \frac{P_{out}}{P_{out} + P_i + P_{cu}}$ `(4/7)`
- 🟢 **Maximum efficiency condition**: $P_i = P_{cu}$ `(2/7)` *(proof asked in '19 Q3a and '23)*
- 🟢 **All-day efficiency** `(3/7)` *(asked in '18, '19, '23)*
- 🟢 Copper loss and stray load loss
- 🟢 Efficiency curves and the load fraction for peak efficiency

#### [Lecture 026: Problems Based on Losses and Efficiency in Transformers](Lecture_026_Problems_Based_on_Losses_and_Efficiency_in_Transformers.md) `01:14:58` 🔴
- 🟢 All-day efficiency by the tabular method `(3/7)` *(matches '23 Q3b and '19 Q4c)*
- 🔴 Efficiency at full load and half load, various power factors `(4/7)`
- 🟢 Loss separation from efficiency data
- 🟡 Constant voltage-frequency change problems `(1/7)` *(asked in '18)*

---

### 1.6 Voltage Regulation (027–028) 🔴

#### [Lecture 027: Voltage Regulation](Lecture_027_Voltage_Regulation.md) `01:16:37` 🔴
- 🔴 **Voltage regulation definition**: $VR = \frac{V_{NL} - V_{FL}}{V_{FL}} \times 100\%$ `(5/7)` *(Slides L-10 S16)*
- 🔴 **Approximate VR formula**: $VR \approx \frac{I_2(R_{02}\cos\varphi_2 \pm X_{02}\sin\varphi_2)}{V_{2,fl}}$ `(5/7)` *(Slides L-10 S16)*
- 🔴 **Phasor diagram derivation of VR for lagging, leading, unity pf** `(5/7)` *(the exact '18/'19/'21/'23/'24 pattern)*
- 🟡 Maximum voltage regulation condition — *deeper than slides*
- 🟡 Zero regulation condition — *deeper than slides*

#### [Lecture 028: Problems based on Voltage Regulation of Transformer](Lecture_028_Problems_based_on_Voltage_Regulation_of_Transformer.md) `01:12:14` 🔴
- 🔴 Voltage regulation calculations from test data `(5/7)`
- 🟡 Three-phase transformer regulation `(1/7)` *(matches '23 Q4c)*
- 🟡 Tap changer problems — *not explicitly in slides*

---

### 1.7 Auto-Transformer & Coupled Circuits (029–036)

> [!WARNING]
> **Correction from the previous version of this guide.** Lectures 032–035 were marked ⚪ "skip entirely". That was wrong. The **auto-transformer copper saving proof was asked in '20 and '23** and sits in Tier 3 of the exam prep guide. Watch **034** for the proof and **035** for the numericals.
> Lectures 029–031 and 036 stay ⚪. Coupled circuits, scaling laws, and three-winding transformers have never been asked.

#### [Lecture 029: Important Concepts in Electrical Machines 1](Lecture_029_Important_Concepts_in_Electrical_Machines_1.md) `00:57:11`
- ⚪ Magnetically coupled circuits, additive/subtractive polarity
- ⚪ Transformer scaling laws (dimensions, ratings)

#### [Lecture 030: Important Concepts in Electrical Machines 2](Lecture_030_Important_Concepts_in_Electrical_Machines_2.md) `01:03:42`
- ⚪ Power transformers vs distribution transformers
- ⚪ Three-winding transformer analysis
- ⚪ Tertiary winding applications

#### [Lecture 031: Transformer and Magnetically Coupled Circuits](Lecture_031_Transformer_and_Magnetically_Coupled_Circuits.md) `00:51:00`
- ⚪ T-equivalent and Pi-equivalent coupled circuits
- ⚪ Impedance matching at high frequency

#### [Lecture 032: Auto Transformer 1](Lecture_032_Auto_Transformer_1.md) `00:42:43`
- 🟡 Auto-transformer construction and circuit model `(2/7)`
- 🟡 Power split: inductively transferred vs conductively transferred
- 🟡 kVA rating advantage over an equivalent two-winding unit

#### [Lecture 033: Auto Transformer in Hindi 2](Lecture_033_Auto_Transformer_in_Hindi_2.md) `01:06:30`
- 🟡 Two-winding to auto-transformer conversion, additive and subtractive
- 🟡 Scaling of per-unit impedance, regulation, losses, and SC current

#### [Lecture 034: Auto Transformer in Hindi 3](Lecture_034_Auto_Transformer_in_Hindi_3.md) `00:33:38` 🟡 **← the proof you need**
- 🟡 **Conductor material saving derivation** `(2/7)` *(this is the '20 Q and '23 Q copper saving proof)*
- 🟡 Core savings, lower losses, higher efficiency
- 🟡 Limitations: no galvanic isolation, high fault current

#### [Lecture 035: Problems based on Auto Transformer](Lecture_035_Problems_based_on_Auto_Transformer.md) `00:55:52`
- 🟡 Auto-transformer numericals — upgraded kVA, winding currents, power split `(2/7)`

#### [Lecture 036: Problems based on Three Winding Transformer](Lecture_036_Problems_based_on_Three_Winding_Transformer.md) `00:58:18`
- ⚪ Three-winding transformer problems — *never asked*

---

### 1.8 Three-Phase Transformer Connections (037–042)

#### [Lecture 037: Three Phase Transformer 1](Lecture_037_Three_Phase_Transformer_1.md) `01:08:18`
- 🟢 **Need for 3-phase transformers** *(Slides L-11 S03)*
- 🟢 **Bank of 3 single-phase vs integrated 3-phase unit** *(Slides L-11 S04-S05)*
- 🟡 **Three-limbed shell-type core economy** `(1/7)` *(the '19 Q3b "reverse the middle phase winding" question)*
- 🟡 Five-limbed core construction — *mentioned in slides briefly*

#### [Lecture 038: Three Phase Transformer 2](Lecture_038_Three_Phase_Transformer_2.md) `00:53:20`
- 🟢 **Clock notation** for phase displacement `(2/7)` *(Slides L-11 S26)*
- 🟢 **Delta-Delta ($\Delta$-$\Delta$) connection** `(2/7)` *(Slides L-11 S14)*
- 🟢 **Dd0 and Dd6** vector group phasor analysis `(2/7)` *(Slides L-11 S27)*
- 🔴 Parallel operation constraints `(4/7)` *(see Lecture 047 for the full treatment)*

#### [Lecture 039: Three Phase Transformer 3](Lecture_039_Three_Phase_Transformer_3.md) `00:54:27`
- 🟢 **Star-Star (Y-Y) connection** — Yy0, Yy6 groups *(Slides L-11 S07-S10)*
- 🟡 **Y-Y limitations**: floating neutral, 3rd harmonic voltage distortion `(2/7)` *(asked in '21, '23; Slides L-11 S08)*
- 🟢 **Delta-Star ($\Delta$-Y) connection** — Dy11, Dy1 groups `(2/7)` *(Slides L-11 S13)*
- 🟢 $30°$ phase shift in Y-Δ and Δ-Y *(Slides L-11 S12-S13)*

#### [Lecture 040: Three Phase Transformer 4](Lecture_040_Three_Phase_Transformer_4.md) `00:47:12`
- 🟢 **Star-Delta (Y-$\Delta$) connection** — Yd1, Yd11 groups `(2/7)` *(Slides L-11 S11-S12)*
- 🟡 **Vector group nomenclature**: Y/D/y/d/n + clock hour `(2/7)` *(asked in '19, '21; Slides L-11 S27)*
- 🟡 **Four standard groups**: Group 1 (0°), Group 2 (180°), Group 3 (−30°), Group 4 (+30°) `(2/7)` *(the '19 Q3c Yd11-vs-Dy1 parallel question needs this)*
- 🟡 Phase shift for positive/negative sequence — *deeper than slides*

#### [Lecture 041: Problems Based on Three Phase Transformers 1](Lecture_041_Problems_Based_on_Three_Phase_Transformers_1.md) `01:13:56`
- 🟢 Three-phase connection problems — current calculations, voltage ratios `(2/7)` *(matches '18 Q3b and '24)*
- 🟢 Core area and winding turns design
- 🟡 Per-unit impedance on delta side

#### [Lecture 042: Problems Based on Three Phase Transformers 2](Lecture_042_Problems_Based_on_Three_Phase_Transformers_2.md) `01:10:48`
- 🟡 Clock group identification problems `(2/7)`
- 🟡 Phase displacement derivation `(2/7)`
- 🟡 Negative-sequence excitation — *deeper than slides*

---

### 1.9 Open-Delta, Scott-T & Phase Conversion (043–046) 🔴

#### [Lecture 043: Three Phase Transformer 5](Lecture_043_Three_Phase_Transformer_5.md) `01:11:53` 🔴
- 🔴 **Open-Delta (V-V) connection** `(7/7 🔥)` *(Slides L-11 S16-S18)*
- 🔴 **Capacity ratio**: $\frac{S_{V-V}}{S_\Delta} = \frac{1}{\sqrt{3}} \approx 57.7\%$ `(7/7 🔥)` *(ties with OC/SC as the most repeated proof)*
- 🔴 **Utilization factor**: $\frac{\sqrt{3}}{2} \approx 86.6\%$ `(7/7 🔥)` *(Slides L-11 S18)*
- 🟡 **Supply continuity when one phase burns out** `(1/7)` *(the '19 Q4a single-phasing-of-Δ-Δ question)*
- 🟡 V-V connection supplying star/delta loads — *deeper than slides*

#### [Lecture 044: Three Phase Transformer 6](Lecture_044_Three_Phase_Transformer_6.md) `01:00:31`
- 🟡 **Zigzag connection** — Dz0, Dz6, Yz1 groups — *named in vector group nomenclature (Slides L-11 S27: "z = zigzag") but not detailed in slides*
- 🟡 Harmonic cancellation via zigzag — *related to 3rd harmonic issues*

#### [Lecture 045: Three Phase Transformer 7](Lecture_045_Three_Phase_Transformer_7.md) `01:12:58`
- 🟢 **Scott-T connection** — 3-phase to 2-phase conversion `(3/7)` *(Syllabus: phase conversion; Slides L-11 S21-S23)*
- 🟢 Main transformer (center-tapped at 50%) and Teaser transformer (tapped at 86.6%) `(3/7)` *(Slides L-11 S22)*
- 🟢 Mathematical proof of 90° phase shift `(3/7)` *(Slides L-11 S23)*
- 🟡 Primary current balancing under load — *deeper than slides*
- 🟡 VA ratings and utilization factor of Scott-T — *not in slides*

#### [Lecture 046: Problems Based on Three Phase Transformers 3](Lecture_046_Problems_Based_on_Three_Phase_Transformers_3.md) `01:06:24`
- 🔴 Open-Delta problems — rating, turns ratio, capacity derating `(7/7 🔥)` *(matches '20 Q4c)*
- 🟢 Scott-T connection problems — turns ratio, primary currents `(3/7)` *(identical data in '18 Q4b and '24 Q4c)*
- 🟡 Unbalanced load problems — *deeper than slides*

---

### 1.10 Parallel Operation, Excitation & Transients (047–053)

> [!WARNING]
> **Correction from the previous version of this guide.** This whole block was marked ⚪ "NOT in the syllabus, skip". Three of these topics have been asked:
> - **Parallel operation conditions**: asked in '17, '21, '23 `(3/7)`. Watch **047**.
> - **Magnetizing current is not fully sinusoidal**: asked in '24 Q4a as a 2-mark justify. Watch **049**.
> - **Inrush current when first connected to the line**: asked in '17 `(1/7)`. Watch **052**.
>
> Lectures 048, 050, 051, and 053 are support material. Watch them only if the main lecture leaves you unsure.

#### [Lecture 047: Parallel Operation of Transformers](Lecture_047_Parallel_Operation_of_Transformers.md) `01:20:36` 🟡 **← conditions you need**
- 🔴 **Necessary conditions** to stop circulating current: equal voltage ratios, same polarity, same phase sequence, same phase displacement `(4/7)`
- 🔴 **Desirable conditions** for correct load sharing: equal per-unit impedance, matched X/R ratio `(4/7)`
- 🟡 Why transformers are paralleled: capacity, reliability, lower standby cost
- 🟡 Load sharing and maximum permissible load derivation

#### [Lecture 048: Problems based on Parallel Operation of Transformer](Lecture_048_Problems_based_on_Parallel_Operation_of_Transformer.md) `01:04:18`
- 🔴 Load sharing numericals, circulating current, max loading `(4/7)`
- 🟡 Conceptual questions on phasor groups in parallel *(helps with '19 Q3c)*

#### [Lecture 049: Excitation Phenomenon 1](Lecture_049_Excitation_Phenomenon_1.md) `01:21:13` 🟡 **← the '24 justify question**
- 🟡 **Why magnetizing current cannot be sinusoidal under saturation** `(1/7)` *(exactly the '24 Q4a 2-mark question)*
- 🟡 **Third harmonic dominance** in magnetizing current `(1/7)` *(also explains the Y-Y problems in Slides L-11 S08)*
- 🟡 Peaky current waveform, Fourier content, hysteresis angle $\beta$

#### [Lecture 050: Excitation Phenomenon 2](Lecture_050_Excitation_Phenomenon_2.md) `00:57:03`
- 🟡 **Star connection triplen elimination** — *directly related to Y-Y grounding solutions in Slides L-11 S09*
- 🟡 **Delta circulating currents** for harmonic suppression
- ⚪ Triplen harmonic phase relationships in depth

#### [Lecture 051: Excitation Phenomenon 3](Lecture_051_Excitation_Phenomenon_3.md) `01:10:18`
- 🟡 **Delta tertiary winding** for harmonic suppression — *mentioned in Slides L-11 S09*
- ⚪ Oscillating neutral, tank stray losses

#### [Lecture 052: Switching Transients](Lecture_052_Switching_Transients.md) `00:45:21`
- 🟡 **Magnetizing inrush current** when a transformer is first switched on `(1/7)` *(asked in '17)*
- 🟡 Switching angle and residual flux effect on inrush peak

#### [Lecture 053: Problems based on Harmonics and Inrush Current](Lecture_053_Problems_based_on_Harmonics_and_Inrush_Current.md) `00:33:36`
- 🟡 Harmonic and inrush current numericals `(1/7)`

---

## Part 2: Three-Phase Induction Motor (Syllabus Chapter 2)
**Lectures 131–159 | Covers: RMF, Equiv Circuit, Torque-Speed, Testing, Starting, Speed Control, Braking, Induction Generator**

> **Syllabus scope**: Rotating magnetic field · Equivalent circuit · Vector diagram · Torque-speed characteristics · Effect of changing R₂ and X₂ · Motor torque & developed rotor power · No-load test · Blocked rotor test · Starting methods · Electric braking · Speed control · Induction generator

---

### 2.1 Introduction & Construction (131–134)

#### [Lecture 131: Induction Machines Introduction](Lecture_131_Induction_Machines_Introduction.md) `00:49:07`
- 🔴 **Working principle** — inductive energy transfer, no brushes `(4/7)` *(feeds the "why IM is a rotating transformer" question; Slides L-02 S03-S07)*
- 🟢 **Torque production** — Lorentz force on rotor conductors *(Slides L-03 S04-S05)*
- 🟡 Air gap optimization and reluctance — *deeper than slides*

#### [Lecture 132: Induction Machine Construction 1](Lecture_132_Induction_Machine_Construction_1.md) `00:48:50`
- 🟢 **Stator construction** and winding layout *(Slides L-02 S03)*
- 🟢 **Squirrel cage rotor** — skewing, operational characteristics *(Slides L-02 S06)*
- 🟡 Slot types: open, semi-open, closed — *not in slides*

#### [Lecture 133: Induction Machine Construction 2](Lecture_133_Induction_Machine_Construction_2.md) `00:44:05` 🔴
- 🟢 **Wound/Slip-ring rotor** — slip rings, brushes, external resistance *(Slides L-02 S06)*
- 🟢 **SCIM vs SRIM** comparison *(Slides L-02 S07)*
- 🔴 **Slip**: $s = (N_s - N)/N_s$ and why the rotor can never reach $N_s$ `(5/7)` *(asked in '20, '21, '23, '24; Slides L-03 S06-S07)*
- 🔴 **Rotor frequency**: $f_r = sf$ `(5/7)` *(Slides L-03 S08)*

#### [Lecture 134: Inverted Induction Motor](Lecture_134_Inverted_Induction_Motor.md) `00:44:05`
- 🟡 Inverted IM concept — rotor excited, stator rotates — *builds the physical intuition behind "IM as rotating transformer"*
- ⚪ Induction machine as frequency changer — *not in syllabus*

---

### 2.2 Rotating Magnetic Field (135) 🔴

#### [Lecture 135: Rotating Magnetic Field](Lecture_135_Rotating_Magnetic_Field.md) `00:55:58` 🔴
- 🔴 **RMF proof** from 3-phase supply: resultant $\Phi_R = 1.5\Phi_m$, constant magnitude, rotates at $N_s$ `(5/7 🔥)` *(Syllabus: RMF; Slides L-02 S08-S14)*
- 🔴 Synchronous speed: $N_s = 120f/P$ `(5/7 🔥)`
- 🔴 Slip problems and rotor frequency calculations `(5/7)` *(matches '19 Q5c)*
- 🟡 Dual-fed machine analysis — *not in slides*
- 🟡 Cogging and supersynchronous rotor field speeds `(1/7)` *(cogging asked in '23)*

> [!TIP]
> The 2-φ version of the RMF proof also shows up. Class notes cover it (`class04_fig02_twophase_rmf_phasors.jpg`). This lecture only does the 3-φ case.

---

### 2.3 Equivalent Circuit (136–137)

#### [Lecture 136: Equivalent Circuit 1](Lecture_136_Equivalent_Circuit_1.md) `00:44:11`
- 🟡 **Induction motor phasor diagram** `(1/7)` *(Syllabus: vector diagram; asked in '24; Slides L-03 S10-S14)*
- 🟢 **Standstill rotor EMF** $E_2$ and running EMF $sE_2$ `(3/7)` *(the core of the "IM is a rotating transformer" answer; Slides L-03 S11)*
- 🟢 **Air-gap power** $P_g$ concept *(Slides L-06 S04)*
- 🔴 **Developed torque** formulation `(6/7)` *(Slides L-06 S06)*

#### [Lecture 137: Equivalent Circuit 2](Lecture_137_Equivalent_Circuit_2.md) `00:40:59`
- 🟢 **Complete per-phase equivalent circuit** `(3/7)` *(Syllabus: equivalent circuit; asked in '17, '20, '23; Slides L-03 S20)*
- 🟢 **$R_2/s$ decomposition**: $R_2/s = R_2 + R_2(1-s)/s$ `(3/7)` *(Slides L-03 S16-S18)*
- 🟢 **Power flow diagram** — $P_g : P_{cu} : P_{dev} = 1 : s : (1-s)$ `(2/7)` *(Slides L-06 S05)*
- 🟢 Loss classification and rotor efficiency `(2/7)` *(asked in '21, '23)*

---

### 2.4 Losses, Power Flow & Efficiency (138)

#### [Lecture 138: Losses and Efficiency of Induction Machines](Lecture_138_Losses_and_Efficiency_of_Induction_Machines.md) `01:16:06`
- 🟢 **Motor torque and developed rotor power** `(2/7)` *(Syllabus; Slides L-06 S03-S09)*
- 🟢 **Power flow cascade**: $P_{in} \to P_g \to P_{dev} \to P_{out}$ `(2/7)` *(Slides L-06 S03-S08)*
- 🟢 **Golden ratio**: $P_g : sP_g : (1-s)P_g$ `(2/7)` *(matches '20 Q6d)*
- 🟢 **Synchronous watt** `(2/7)` *(asked in '21, '23; Slides L-06 S08)*
- 🟢 **Rotor efficiency** `(2/7)` *(asked in '21, '23)*

---

### 2.5 Torque-Slip Characteristics (139–143) 🔴

#### [Lecture 139: Torque Slip Characteristics 1](Lecture_139_Torque_Slip_Characteristics_1.md) `00:40:00` 🔴
- 🔴 **Torque-speed characteristic** — motoring, generating, braking regions `(4/7)` *(asked in '20, '21, '23, '24; Slides L-04 S15-S16)*
- 🔴 **Starting torque** formula `(6/7)` *(Slides L-04 S04-S05)*
- 🔴 Low-slip linear region ($T \propto s$) and high-slip region ($T \propto 1/s$) `(4/7)` *(Slides L-04 S15)*
- 🟡 Thévenin equivalent of stator network — *deeper than slides*
- 🟡 Voltage dependence of torque ($T \propto V^2$) — *needed for star-delta starter proofs*

#### [Lecture 140: Torque Slip Characteristics 2](Lecture_140_Torque_Slip_Characteristics_2.md) `00:50:20` 🔴
- 🔴 **Maximum torque / breakdown torque**: $T_{max} = \frac{K_1 E_2^2}{2X_2}$ `(6/7)` *(asked in '17, '19, '21, '24; Slides L-04 S14)*
- 🔴 **Breakdown slip**: $s_b = R_2/X_2$ `(6/7)` *(Slides L-04 S12-S13)*
- 🟢 **Effect of rotor resistance** on torque-speed curves *(Syllabus: effect of changing R₂ and X₂; Slides L-04 S17)*
- 🟢 **Maximum starting torque condition**: $R_2 = X_2$ *(Slides L-04 S06)*
- 🟡 **$T_f/T_{max}$ ratio derivation** `(1/7)` *(asked in '17)*
- 🟢 $T_{max}$ is independent of $R_2$ — only $s_b$ changes *(Slides L-04 S14)*

#### [Lecture 141: Torque Slip Characteristics 3](Lecture_141_Torque_Slip_Characteristics_3.md) `00:49:44`
- 🟢 **Effect of rotor resistance** on current, power factor, speed *(Syllabus: effect of changing R₂ and X₂)*
- 🟡 **V/f control** fundamentals `(3/7)` *(speed control; see also 151, 152)*
- 🟡 Power-slip characteristics and maximum mechanical power — *deeper than slides*
- 🟡 Operating characteristics curves: torque, PF, efficiency vs speed

> [!NOTE]
> The syllabus names "effect of changing R₂ and X₂" but the papers rarely ask it head-on. The analysis flags it as under-tested. Lectures 140 and 141 cover it, so one pass is enough.

#### [Lecture 142: Torque Slip Characteristics 1 (Problems)](Lecture_142_Torque_Slip_Characteristics_1.md) `01:20:24` 🔴
- 🟢 **$T_{max}/T_f$ ratio problems** `(3/7)` *(near-identical data in '17 Q2d, '19 Q8c, '24 Q7c)*
- 🟡 External rotor resistance addition problems `(1/7)` *(matches '21 Q4c)*
- 🟢 Full-load slip from breakdown ratios
- 🟡 Induction generator frequency dynamics — *not in slides*

#### [Lecture 143: Torque Slip Characteristics 2 (Problems)](Lecture_143_Torque_Slip_Characteristics_2.md) `00:49:06`
- 🟢 Practice: $T_{FL}/T_{max}$ ratios, starting current ratios `(3/7)`
- 🟢 External resistance for full-load torque at specified slip
- 🟡 Frequency-voltage scaling problems — *deeper than slides*

---

### 2.6 Stability & Testing (144–145)

#### [Lecture 144: Stability and Testing of Induction Motor](Lecture_144_Stability_and_Testing_of_Induction_Motor.md) `00:55:29`
- 🟢 **No-load test** — measurements, impedance calculations `(2/7)` *(Syllabus: no-load test; asked directly in '24; Slides L-05 S04-S08)*
- 🟢 **Blocked rotor test** — equivalent circuit, parameter extraction `(2/7)` *(Syllabus: blocked rotor test; Slides L-05 S09-S11)*
- 🟢 **Separation of no-load losses** *(Slides L-05 S06-S08)*
- 🟡 Direct-on-line starting relations from blocked rotor data `(1/7)` *(asked in '19 for motors above 25 kW)*
- 🟡 Operating point stability criteria — *explains why motors stall*

> [!TIP]
> Both tests also feed the circle diagram in Lecture 146. Learn them once and you get two question types.

#### [Lecture 145: Stability and Testing of Induction Machines](Lecture_145_Stability_and_Testing_of_Induction_Machines.md) `00:49:20`
- 🟢 Testing practice problems — full-load efficiency, parameter extraction
- 🟢 Starting torque at rated voltage from test data
- 🟡 Speed control via external rotor resistance — *connects to speed control section*
- 🟡 No-load loss separation and drive stability — *supplementary*

---

### 2.7 Circle Diagram (146) 🔴

> [!IMPORTANT]
> **Upgraded from 🟡.** The old guide said "skip if time is very tight" because the circle diagram is not in the syllabus text. But it appeared in **4 of 7 papers** ('17, '18, '19, '21) and it is in maam's slides (L-07 S22-S24). It is a 🟠 HIGH priority golden question.
> The one caveat: it was **absent from '23 and '24**. It may be fading under the OBE syllabus. Learn the construction, but place it below the 🔴 items if you are short on time.

#### [Lecture 146: Circle Diagram of Induction Motor](Lecture_146_Circle_Diagram_of_Induction_Motor.md) `01:03:26` 🔴
- 🔴 **Construction from no-load and blocked-rotor test points** `(4/7)` *(Slides L-07 S23)*
- 🔴 **Graphical extraction of torque, power, efficiency, slip** `(4/7)` *(Slides L-07 S24)*
- 🔴 Torque line, output line, power line construction `(4/7)` *(matches '21 Q8c)*
- 🟢 Semicircular locus derivation for rotor current *(Slides L-07 S22)*

> [!EXAMPLE]
> The 415 V, 29.84 kW delta motor problem is identical in '17 Q3b and '19 Q6a. Same data: NL (415 V, 21 A, 1250 W), BR (100 V, 45 A, 2730 W). Solve it once.

---

### 2.8 Starting Methods (147–150)

#### [Lecture 147: Starting of SCIM](Lecture_147_Starting_of_SCIM.md) `00:50:16`
- 🟡 **Starting problem**: $I_{st} \approx 5\text{–}8 \times I_{FL}$ `(1/7)` *(Slides L-06 S11)*
- 🟡 **DOL starting** and why it is barred above 25 kW `(1/7)` *(asked in '19; Slides L-06 S12)*
- 🟢 **Stator resistance/reactance starting**: $I_{st} = xI_{sc}$, $T_{st} = x^2 T_{sc}$ *(Slides L-06 S13-S14)*
- 🟢 **Auto-transformer starting**: line current $= x^2 I_{sc}$ *(Slides L-06 S15-S17)*
- 🟡 **Star-Delta starting**: $I_{st} = \frac{1}{3}I_{sc,\Delta}$, $T_{st} = \frac{1}{3}T_{sc,\Delta}$ `(3/7)` *(asked in '18, '20, '23; Slides L-06 S18)*

#### [Lecture 148: Starting of SCIM (Problems)](Lecture_148_Starting_of_SCIM.md) `01:02:50`
- 🟡 Starting torque to full-load torque ratio problems `(3/7)` *(matches '23 Q7b)*
- 🟢 Starting problems — external resistance, feeder effects
- 🟡 Minimum voltage to avoid stalling

#### [Lecture 149: Starting of SRIM](Lecture_149_Starting_of_SRIM.md) `00:29:30`
- 🟢 **Rotor rheostat starting** — external $R_{ext}$ via slip rings *(Slides L-06 S19-S20)*
- 🟡 Geometric progression of switching slips — *deeper than slides*
- 🟡 Starter design worked example

#### [Lecture 150: Starting of SRIM (Problems)](Lecture_150_Starting_of_SRIM.md) `00:36:40`
- 🟢 SRIM starting practice problems
- 🟡 Five-section starter design — *deeper than slides*

---

### 2.9 Speed Control (151–154)

#### [Lecture 151: Speed Control of Induction Motor 1](Lecture_151_Speed_Control_of_Induction_Motor_1.md) `00:41:30`
- 🟢 **Stator voltage control** `(3/7)` *(Slides L-07 S03)*
- 🟢 **Rotor resistance control** `(3/7)` *(Slides L-07 S03)*
- 🟡 Rotor EMF injection (Scherbius/Kramer) — *named in Slides L-07 S03 but not detailed*
- 🟡 Sub-synchronous vs super-synchronous modes

#### [Lecture 152: Speed Control of Induction Motor 2](Lecture_152_Speed_Control_of_Induction_Motor_2.md) `00:43:42`
- 🟢 **Supply frequency control (V/f control)** `(3/7)` *(Slides L-07 S03)*
- 🟢 **Changing stator poles** — consequent poles `(3/7)` *(Slides L-07 S03)*
- 🟡 V/f profile, low-frequency voltage boost — *deeper than slides*
- 🟡 Cascading of induction motors — *named in Slides L-07 S03 but not detailed*

#### [Lecture 153: Speed Control of IM 1 (Problems)](Lecture_153_Speed_Control_of_IM_1.md) `00:54:10`
- 🟡 **External resistance for speed reduction at constant torque** `(1/7)` *(matches '21 Q4c)*
- 🟢 Speed control practice problems — rotor resistance insertion
- 🟢 Fan load analysis and minimum rotor resistance
- 🟡 Consequent pole modification problems

#### [Lecture 154: Speed Control of IM 2 (Problems)](Lecture_154_Speed_Control_of_IM_2.md) `00:45:46`
- 🟢 Practice: frequency scaling, rotor resistance control
- 🟡 V/f flux constraints, frequency variation effects

---

### 2.10 Electric Braking (155–156)

#### [Lecture 155: Braking of Induction Motor](Lecture_155_Braking_of_Induction_Motor.md) `00:27:37`
- 🔴 **Plugging** — reversing two stator leads, $s \approx 2$ `(4/7)` *(definition asked in '17, '18, '19, '20; Slides L-07 S09)*
- 🔴 **Regenerative braking** — motor driven above $N_s$ `(4/7)` *(Slides L-07 S06)*
- 🔴 **DC injection braking** — stationary field `(4/7)` *(Slides L-07 S07)*
- 🟡 Dynamic equations of plugging, skin effect — *deeper than slides*

> [!TIP]
> Braking shows up as a 2 to 3 mark "define" question, not a derivation. Learn the three definitions and one diagram each. Do not over-invest.

#### [Lecture 156: Braking of Induction Motor (Problems)](Lecture_156_Braking_of_Induction_Motor.md) `00:27:06`
- 🟢 Braking practice problems
- 🟢 Operating modes and braking torque comparison

---

### 2.11 Deep Bar, Double Cage & Induction Generator (157–159)

> [!NOTE]
> **Induction generator is a rising topic.** It appeared once in '18, then returned in both '23 and '24. The analysis calls it hot. Lectures 158 and 159 are worth real time.

#### [Lecture 157: High Torque Cage Rotor](Lecture_157_High_Torque_Cage_Rotor.md) `00:25:10`
- 🟡 **Deep bar rotor** — skin effect raises starting torque — *relates to the R₂ effect in the syllabus, not in slides*
- 🟡 **Double cage rotor** — outer cage high R (starting), inner cage low R (running) — *not in slides, never asked directly*
- 🟡 Equivalent circuit modeling of double cage

#### [Lecture 158: Miscellaneous Concepts](Lecture_158_Miscellaneous_Concepts.md) `00:46:21`
- 🟢 **Induction generator principles** — reactive power requirements `(3/7)` *(Syllabus: induction generator; Slides L-07 S10-S12)*
- 🟢 **Self-excited vs grid-connected induction generator** `(3/7)` *(Slides L-07 S11-S12)*
- 🟡 **Crawling and cogging** `(1/7)` *(new in '23, may return; not in slides)*

#### [Lecture 159: High Torque Cage Rotor and Induction Generator](Lecture_159_High_Torque_Cage_Rotor_and_Induction_Generator.md) `00:45:10`
- 🟢 **Induction generator problems** — operating speeds, power flow `(3/7)` *(Syllabus: induction generator)*
- 🟡 **Capacitance per phase for self-excitation** `(2/7)` *(identical data in '18 Q5c and '24 Q8c)*
- 🟡 Double cage standstill torque formulation — *relates to rotor resistance effects*
- 🟡 Parasitic phenomena: cogging vs crawling, deep bar current distribution

---

## Part 3: Single-Phase Induction Motor (Syllabus Chapter 3) 🔴
**Lectures 160–162 | Covers: Theory of operation, Equivalent circuit, Starting methods**

> **Syllabus scope**: Theory of operation · Equivalent circuit · Starting methods

> [!IMPORTANT]
> This is the densest 2 hours in the playlist. DFRT appeared in 5 of 7 papers. The 1-φ starting methods question appeared in 6 of 7. Two lectures, roughly 20% of Section B marks.

---

#### [Lecture 160: Single Phase Induction Motor 1](Lecture_160_Single_Phase_Induction_Motor_1.md) `00:36:02` 🔴
- 🔴 **Double revolving field theory** — alternating flux splits into two opposing rotating fields `(5/7 🔥)` *(Syllabus: theory of operation; Slides L-07 S15-S16)*
- 🟢 **Zero starting torque** at standstill ($T_f = T_b$) `(2/7)` *(the standalone "why is 1-φ IM not self-starting" question, asked in '17 and '19; it is also the punchline of every DFRT answer; Slides L-07 S16)*
- 🟢 **Equivalent circuit** for forward and backward fields *(Syllabus: equivalent circuit)*
- 🟡 **Torque-speed characteristics** of 1-φ IM `(1/7)` *(1-φ phasor diagram asked in '24)*

> [!WARNING]
> **Syllabus gap worth knowing.** The **1-φ IM equivalent circuit** is in the syllabus but has never been asked in any of the 7 papers. This lecture covers it. Give it one pass, not three.

#### [Lecture 161: Single Phase Induction Motor 2](Lecture_161_Single_Phase_Induction_Motor_2.md) `00:49:18` 🔴
- 🔴 **Split-phase motor** — high R auxiliary winding, ~30° phase split `(6/7 🔥)` *(Syllabus: starting methods; Slides L-07 S18)*
- 🔴 **Capacitor-start motor** — ~80° phase split, high starting torque `(6/7 🔥)` *(Slides L-07 S19)*
- 🔴 **Capacitor-start capacitor-run and PSC motors** `(6/7 🔥)` *(Slides L-07 S21)*
- 🟢 **Maximum starting torque derivation in capacitor motors** `(3/7)` *(capacitor value asked in '18, '21)*
- 🟡 Direction of rotation determination — *useful but not in slides*

#### [Lecture 162: Single Phase Induction Motor (Problems)](Lecture_162_Single_Phase_Induction_Motor.md) `00:49:06`
- 🟢 **Maximum starting torque capacitance calculation** `(3/7)` *(matches '21 Q7c)*
- 🟢 Practice problems on 1-φ IM equivalent circuit
- 🟢 Phase difference criterion and rotor direction
- 🟡 Full equivalent circuit input impedance and current — *deeper than slides*

---

## Gaps: Asked in Exams, Thin or Missing in This Playlist

These questions have appeared in real papers but the playlist does not cover them well. Use the other sources listed.

| Exam Topic | Years | Playlist Status | Go Here Instead |
|:---|:---|:---|:---|
| **Instrument transformer / PT operation** | '17 `(1/7)` | One passing mention in Lecture 015 | `Books/` (Theraja CT/PT articles), Slides L-09 |
| **Single phasing of a 3-φ IM** | '18 `(1/7)` | Not covered | `Books/` (VK Mehta IM chapter), `ClassNoteByRaidah/` |
| **Synchronous motor: not self-starting, V-curves** | '20 `(1/7)` | Removed with the 81 out-of-scope lectures | `Books/` (Chapman synchronous machines) |
| **2-φ RMF proof** | mixed with 3-φ `(5/7)` | Lecture 135 does the 3-φ case only | `ClassNoteByRaidah/` class04 figures |
| **Transformer breathing** | '19 `(1/7)` | Lecture 012 mentions breathers only | `Books/` (Theraja construction articles) |

> [!NOTE]
> **One inconsistency found in the analysis file.** [ECE_2207_Question_Analysis.md](../ECE_2207_Question_Analysis.md) lists "Single phasing effect" under Section B for both '18 and '19. But the '19 question (Q4a) is about a **delta-delta transformer**, which is Section A content, and it is really an open-delta continuity question. Only the '18 question (Q5a) is about an induction motor. Worth fixing in the analysis file.

---

## Quick Reference: Watch Priority Summary

### 🔴 Exam-Proven (asked 4+ times — watch these first)

| Exam Topic | Frequency | Lectures |
|---|:---:|---|
| OC test / SC test (TF) | **7/7** | 021, 023 |
| Open-Delta, 57.7% proof | **7/7** | 043, 046 |
| 1-φ IM starting methods | **6/7** | 161, 162 |
| Voltage regulation | **5/7** | 027, 028 |
| RMF proof | **5/7** | 135 |
| Double field revolving theory | **5/7** | 160 |
| EMF equation | **4/7** | 014, 013 |
| Equivalent circuit (TF) | **4/7** | 019, 018, 020 |
| Transformer phasor diagrams | **4/7** | 014, 015, 017, 018 |
| Efficiency calculation | **4/7** | 025, 026 |
| Slip, why $N \ne N_s$ | **4/7** | 133, 135 |
| Torque-speed curve | **4/7** | 139 |
| Max torque derivation | **4/7** | 140 |
| Circle diagram | **4/7** | 146 |
| Plugging / braking definitions | **4/7** | 155 |

### 🟢 Core (in syllabus and slides)

| Topic | Frequency | Lectures |
|---|:---:|---|
| Scott-T connection | 3/7 | 045, 046 |
| All-day efficiency | 3/7 | 025, 026 |
| $T_{max}/T_f$ ratio numericals | 3/7 | 142, 143 |
| Star-delta starter | 3/7 | 147, 148 |
| Induction generator | 3/7 | 158, 159 |
| Speed control | 3/7 | 151, 152, 153 |
| Equivalent circuit (IM) | 3/7 | 136, 137 |
| IM as rotating transformer | 3/7 | 131, 134, 136 |
| No-load / blocked rotor test (IM) | 1/7 | 144, 145 |
| Motor torque & developed power | 2/7 | 138 |
| Synchronous watt, rotor efficiency | 2/7 | 137, 138 |
| 3-phase connections, vector groups | 2/7 | 038, 039, 040, 042 |
| Effect of R₂, X₂ on torque | under-tested | 140, 141 |

### 🟡 Secondary (asked 1 to 3 times, or deeper than slides)

| Topic | Frequency | Lectures | Note |
|---|:---:|---|---|
| Parallel operation (TF) | 3/7 | **047**, 048 | Was wrongly marked skip |
| Auto-transformer copper saving | 2/7 | **034**, 035, 032, 033 | Was wrongly marked skip |
| Y-Y limitations, 3rd harmonic | 2/7 | 039, 049, 050 | |
| Capacitor for max starting torque | 2/7 | 161, 162 | |
| IG capacitance calculation | 2/7 | 159 | Identical data '18 and '24 |
| Max efficiency when $P_i = P_{cu}$ | 2/7 | 025, 026 | |
| Magnetizing current not sinusoidal | 1/7 | **049** | Was wrongly marked skip |
| Inrush current | 1/7 | **052**, 053 | Was wrongly marked skip |
| Crawling and cogging | 1/7 | 158 | New in '23 |
| Transformer breathing | 1/7 | 012 | Thin coverage |
| Shell-type core economy | 1/7 | 037, 011 | |
| Hysteresis and eddy current loss | 1/7 | 024, 003 | |
| Deep bar / double cage | never | 157 | Relates to R₂ effects |

### 🔵 Watch If Fundamentals Feel Shaky

| Topic | Lectures |
|---|---|
| EM fundamentals | 004, 005 |
| Magnetic circuits | 007 |
| Per-unit system | 009, 010 |
| All foundations | 001–010 |

### ⚪ Skip (never asked, not in syllabus)

| Topic | Lectures |
|---|---|
| Coupled circuits, scaling laws | 029, 031 |
| Three-winding transformer | 030, 036 |
| Sumpner's test, phantom loading | 022 (part) |
| Oscillating neutral, tank stray loss | 051 (part) |

---

## Related Files

- [ECE_2207_Question_Analysis.md](../ECE_2207_Question_Analysis.md) — frequency heatmaps and predictions that set the priorities above
- [Topic_Subtopic_Master_List.md](../Topic_Subtopic_Master_List.md) — all 103 subtopics with slide and book references
- [boss_notes/00_Index.md](../boss_notes/00_Index.md) — the distilled notes to read after watching
- [Syllabus.md](../Syllabus.md) — the official course scope
