# ECE 2207: Electrical Machine-I — YouTube Study Guide
## Ankit Goyal Playlist (Curated for ECE 2207)

> **Course**: ECE 2207 — Electrical Machine-I (3 Credits)  
> **Playlist**: Electrical Machines for GATE & ESE — Ankit Goyal Sir  
> **Lectures Kept**: 85 of 166 (81 out-of-scope lectures on DC Machines, Synchronous Machines, EM Energy Conversion, and Special Machines have been removed)

---

## How to Use This Guide

Each lecture's subtopics are tagged with a relevance indicator:

| Tag | Meaning | What to Do |
|:---:|---|---|
| 🟢 | **Core** — In syllabus AND covered in maam's slides | **Must watch**. This will be tested. |
| 🟡 | **Syllabus Extra** — In syllabus but not explicitly in slides, OR in slides but not in syllabus, OR goes deeper than slides | **Watch if topic feels weak**. Can skip if time is short and topic feels complex. |
| 🔵 | **Foundation** — Prerequisite knowledge for understanding core topics | **Watch if fundamentals feel shaky**. Not directly tested but needed for comprehension. |
| ⚪ | **Beyond Scope** — Not in ECE 2207 syllabus | **Skip unless curious**. Kept for reference only. |

> [!TIP]
> **Recommended study order**: Part 0 (skim) → Part 2 (Induction Motor) → Part 1 (Transformer) → Part 3 (Single-Phase IM).  
> Induction Motor was covered first in class, so starting there aligns with your class notes.

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
- 🔵 Ferromagnetic materials — hysteresis loop, residual magnetism, coercive force *(needed for transformer core losses)*
- 🔵 Eddy current losses — lamination rationale *(directly used in transformer/motor core design)*
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
- 🟢 Core materials — CRGO silicon steel, laminations *(Slides L-09 S03)*
- 🟡 Cooling mechanisms, application domains — *not explicitly in slides*
- 🟡 Stacking factor, eddy current mitigation

#### [Lecture 012: Transformer Construction Part 2](Lecture_012_Transformer_Construction_Part_2.md) `01:07:28`
- 🟡 Rectangular vs circular cross-section, stepped cores — *not in slides but deepens understanding*
- 🟡 Winding types: helical, crossover, disc, sandwich
- 🟡 Transformer oil functions, bushings, breathers, conservator tanks

#### [Lecture 013: Problems based on Transformer Construction and Working](Lecture_013_Problems_based_on_Transformer_Construction_and_Working.md) `01:20:05`
- 🟢 EMF equation practice — net core area, turns allocation
- 🟡 V/f control concept and frequency scaling — *builds intuition*
- ⚪ Three-winding transformer design — *not in syllabus*

---

### 1.2 Ideal Transformer (014–016)

#### [Lecture 014: Ideal Transformer Part 1](Lecture_014_Ideal_Transformer_Part_1.md) `01:04:38`
- 🟢 **Ideal transformer assumptions** *(Slides L-08 S04)*
- 🟢 **EMF equation derivation**: $E = 4.44 f N \Phi_m$ *(Slides L-08 S14)*
- 🟢 **Transformation ratio** $K = N_2/N_1$ *(Syllabus: transformation ratio)*
- 🟢 **No-load phasor diagram** *(Slides L-09 S05-S07)*

#### [Lecture 015: Ideal Transformer Part 2](Lecture_015_Ideal_Transformer_Part_2.md) `00:49:28`
- 🟢 **Load phasor diagrams** *(Slides L-09 S10-S12)*
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

#### [Lecture 017: Practical Transformer Part 1](Lecture_017_Practical_Transformer_Part_1.md) `01:04:23`
- 🟢 **No-load current components**: $I_\mu$ (magnetizing) and $I_w$ (core-loss) *(Slides L-09 S05-S08)*
- 🟢 **No-load equivalent circuit** *(Slides L-09 S05-S08)*
- 🟢 **On-load phasor diagram** — demagnetization, reflected current *(Slides L-09 S10-S12)*
- 🟢 $I_0 = \sqrt{I_\mu^2 + I_w^2}$ *(Slides L-09 S06)*

#### [Lecture 018: Practical Transformer Part 2](Lecture_018_Practical_Transformer_Part_2.md) `00:54:24`
- 🟢 **Winding resistance** — KVL formulation *(Slides L-10 S06-S07)*
- 🟢 **Leakage flux** → leakage reactance $X_1, X_2$ *(Slides L-10 S03-S05)*
- 🟢 **Phasor diagram with resistance and leakage** *(Slides L-10 S14-S15)*
- 🟢 Resistance referral: $R_{01} = R_1 + R_2/K^2$ *(Slides L-10 S09)*

#### [Lecture 019: Practical Transformer Part 3](Lecture_019_Practical_Transformer_Part_3.md) `01:10:45`
- 🟢 **Exact equivalent circuit** *(Slides L-10 S12)*
- 🟢 **Referred to primary / secondary** *(Slides L-10 S09-S11)*
- 🟢 **Approximate equivalent circuit** — shunt branch shifted *(Slides L-10 S13)*
- 🟡 Per-unit equivalent circuit — *deeper than slides*
- 🟡 Worked numerical problem

#### [Lecture 020: Problems based on Equivalent Circuit](Lecture_020_Problems_based_on_Equivalent_Circuit.md) `01:17:16`
- 🟢 Load impedance reflection and terminal voltage problems
- 🟢 Efficiency evaluation from equivalent circuit
- 🟢 Short-circuit test concepts and impedance referral
- 🟡 Maximum power transfer in transformer networks — *not in syllabus*

---

### 1.4 Testing: OC & SC Tests (021–023)

#### [Lecture 021: Testing of Transformer 1](Lecture_021_Testing_of_Transformer_1.md) `00:52:53`
- 🟢 **Open-circuit (OC) test** — LV side, HV open *(Syllabus: OC test; Slides L-10 S17)*
- 🟢 Extraction of $R_0, X_0$ from OC data
- 🟢 **Short-circuit (SC) test** — HV side, LV shorted *(Syllabus: SC test; Slides L-10 S18)*
- 🟢 Extraction of $R_{01}, X_{01}$ from SC data

#### [Lecture 022: Testing of Transformer Part 2](Lecture_022_Testing_of_Transformer_Part_2.md) `00:48:37`
- 🟡 Polarity test — *not in syllabus/slides but useful concept*
- ⚪ Sumpner's (back-to-back) test — *not in syllabus*
- ⚪ Phantom loading concept — *not in syllabus*

#### [Lecture 023: Problems Based on Testing of Transformer](Lecture_023_Problems_Based_on_Testing_of_Transformer.md) `01:14:06`
- 🟢 OC/SC test parameter extraction problems
- 🟢 Terminal voltage and regulation calculations from test data
- 🟢 Three-phase transformer testing problems
- ⚪ Sumpner's test problems — *not in syllabus, can skip*

---

### 1.5 Losses & Efficiency (024–026)

> [!NOTE]
> Losses and efficiency are not explicitly listed in the ECE 2207 syllabus as separate topics, but they're closely tied to OC/SC testing and actual transformer behavior. The OC test gives iron/core loss; the SC test gives copper loss. Understanding these makes testing problems much easier.

#### [Lecture 024: Losses and Efficiency Part 1](Lecture_024_Losses_and_Efficiency_Part_1.md) `01:02:06`
- 🟡 Hysteresis loss — Steinmetz formula, dipole reversal mechanism
- 🟡 Eddy current loss derivation — lamination thickness relationship
- 🟡 Separation of core losses experimentally

#### [Lecture 025: Losses and Efficiency Part 2](Lecture_025_Losses_and_Efficiency_Part_2.md) `00:59:19`
- 🟡 Copper loss and stray load loss
- 🟡 Transformer efficiency formula: $\eta = \frac{P_{out}}{P_{out} + P_i + P_{cu}}$
- 🟡 Maximum efficiency condition: $P_i = P_{cu}$
- 🟡 All-day efficiency concept

#### [Lecture 026: Problems Based on Losses and Efficiency in Transformers](Lecture_026_Problems_Based_on_Losses_and_Efficiency_in_Transformers.md) `01:14:58`
- 🟡 Practice problems on loss separation, efficiency, all-day efficiency

---

### 1.6 Voltage Regulation (027–028)

#### [Lecture 027: Voltage Regulation](Lecture_027_Voltage_Regulation.md) `01:16:37`
- 🟢 **Voltage regulation definition**: $VR = \frac{V_{NL} - V_{FL}}{V_{FL}} \times 100\%$ *(Syllabus: voltage regulation; Slides L-10 S16)*
- 🟢 **Approximate VR formula**: $VR \approx \frac{I_2(R_{02}\cos\varphi_2 \pm X_{02}\sin\varphi_2)}{V_{2,fl}}$ *(Slides L-10 S16)*
- 🟡 Maximum voltage regulation condition — *deeper than slides*
- 🟡 Zero regulation condition — *deeper than slides*
- 🟡 Phasor diagram derivation of VR for lagging/leading power factor

#### [Lecture 028: Problems based on Voltage Regulation of Transformer](Lecture_028_Problems_based_on_Voltage_Regulation_of_Transformer.md) `01:12:14`
- 🟢 Voltage regulation calculations from test data
- 🟡 Tap changer problems — *not explicitly in slides*
- 🟡 Three-phase transformer regulation

---

### 1.7 ⚪ Beyond Scope — Coupled Circuits, Auto-TF, Three-Winding (029–036)

> [!WARNING]
> These lectures cover topics **NOT in the ECE 2207 syllabus**: auto-transformers, magnetically coupled circuits, three-winding transformers, and scaling laws. **Skip entirely** unless you encounter these in previous year questions.

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
- ⚪ Auto-transformer construction and analysis

#### [Lecture 033: Auto Transformer in Hindi 2](Lecture_033_Auto_Transformer_in_Hindi_2.md) `01:06:30`
- ⚪ Two-winding to auto-transformer conversion

#### [Lecture 034: Auto Transformer in Hindi 3](Lecture_034_Auto_Transformer_in_Hindi_3.md) `00:33:38`
- ⚪ Auto-transformer comparison and applications

#### [Lecture 035: Problems based on Auto Transformer](Lecture_035_Problems_based_on_Auto_Transformer.md) `00:55:52`
- ⚪ Auto-transformer problems

#### [Lecture 036: Problems based on Three Winding Transformer](Lecture_036_Problems_based_on_Three_Winding_Transformer.md) `00:58:18`
- ⚪ Three-winding transformer problems

---

### 1.8 Three-Phase Transformer Connections (037–042)

#### [Lecture 037: Three Phase Transformer 1](Lecture_037_Three_Phase_Transformer_1.md) `01:08:18`
- 🟢 **Need for 3-phase transformers** *(Slides L-11 S03)*
- 🟢 **Bank of 3 single-phase vs integrated 3-phase unit** *(Slides L-11 S04-S05)*
- 🟢 Three-limbed core-type and shell-type 3-phase transformers
- 🟡 Five-limbed core construction — *mentioned in slides briefly*

#### [Lecture 038: Three Phase Transformer 2](Lecture_038_Three_Phase_Transformer_2.md) `00:53:20`
- 🟢 **Clock notation** for phase displacement *(Slides L-11 S26: clock representation)*
- 🟢 **Delta-Delta ($\Delta$-$\Delta$) connection** *(Slides L-11 S14)*
- 🟢 **Dd0 and Dd6** vector group phasor analysis *(Slides L-11 S27)*
- 🟡 Parallel operation constraints — *not in syllabus*

#### [Lecture 039: Three Phase Transformer 3](Lecture_039_Three_Phase_Transformer_3.md) `00:54:27`
- 🟢 **Star-Star (Y-Y) connection** — Yy0, Yy6 groups *(Slides L-11 S07-S10)*
- 🟢 **Y-Y problems**: floating neutral, 3rd harmonic voltage distortion *(Slides L-11 S08)*
- 🟢 **Delta-Star ($\Delta$-Y) connection** — Dy11, Dy1 groups *(Slides L-11 S13)*
- 🟢 $30°$ phase shift in Y-Δ and Δ-Y *(Slides L-11 S12-S13)*

#### [Lecture 040: Three Phase Transformer 4](Lecture_040_Three_Phase_Transformer_4.md) `00:47:12`
- 🟢 **Star-Delta (Y-$\Delta$) connection** — Yd1, Yd11 groups *(Slides L-11 S11-S12)*
- 🟢 **Vector group nomenclature**: Y/D/y/d/n + clock hour *(Slides L-11 S27)*
- 🟢 **Four standard groups**: Group 1 (0°), Group 2 (180°), Group 3 (−30°), Group 4 (+30°) *(Slides L-11 S27)*
- 🟡 Phase shift for positive/negative sequence — *deeper than slides*

#### [Lecture 041: Problems Based on Three Phase Transformers 1](Lecture_041_Problems_Based_on_Three_Phase_Transformers_1.md) `01:13:56`
- 🟢 Three-phase connection problems — current calculations, voltage ratios
- 🟢 Core area and winding turns design
- 🟡 Per-unit impedance on delta side

#### [Lecture 042: Problems Based on Three Phase Transformers 2](Lecture_042_Problems_Based_on_Three_Phase_Transformers_2.md) `01:10:48`
- 🟢 Clock group identification problems
- 🟢 Phase displacement derivation
- 🟡 Negative-sequence excitation — *deeper than slides*

---

### 1.9 Open-Delta, Scott-T & Phase Conversion (043–046)

#### [Lecture 043: Three Phase Transformer 5](Lecture_043_Three_Phase_Transformer_5.md) `01:11:53`
- 🟢 **Open-Delta (V-V) connection** *(Slides L-11 S16-S18)*
- 🟢 **Capacity ratio**: $\frac{S_{V-V}}{S_\Delta} = \frac{1}{\sqrt{3}} \approx 57.7\%$ *(Slides L-11 S18)*
- 🟢 **Utilization factor**: $\frac{\sqrt{3}}{2} \approx 86.6\%$ *(Slides L-11 S18)*
- 🟡 V-V connection supplying star/delta loads — *deeper than slides*
- 🟡 Reactive power exchange in V-V — *not in slides*

#### [Lecture 044: Three Phase Transformer 6](Lecture_044_Three_Phase_Transformer_6.md) `01:00:31`
- 🟡 **Zigzag connection** — Dz0, Dz6, Yz1 groups — *connection type mentioned in vector group nomenclature (Slides L-11 S27: "z = zigzag") but not detailed in slides*
- 🟡 Harmonic cancellation via zigzag — *related to 3rd harmonic issues*

#### [Lecture 045: Three Phase Transformer 7](Lecture_045_Three_Phase_Transformer_7.md) `01:12:58`
- 🟢 **Scott-T connection** — 3-phase to 2-phase conversion *(Syllabus: phase conversion; Slides L-11 S21-S23)*
- 🟢 Main transformer (center-tapped at 50%) and Teaser transformer (tapped at 86.6%) *(Slides L-11 S22)*
- 🟢 Mathematical proof of 90° phase shift *(Slides L-11 S23)*
- 🟡 Primary current balancing under load — *deeper than slides*
- 🟡 VA ratings and utilization factor of Scott-T — *not in slides*

#### [Lecture 046: Problems Based on Three Phase Transformers 3](Lecture_046_Problems_Based_on_Three_Phase_Transformers_3.md) `01:06:24`
- 🟢 Open-Delta problems — rating, turns ratio, capacity derating
- 🟢 Scott-T connection problems — turns ratio, primary currents
- 🟡 Unbalanced load problems — *deeper than slides*

---

### 1.10 ⚪ Beyond Scope — Parallel Operation, Excitation, Transients (047–053)

> [!WARNING]
> These topics are **NOT in the ECE 2207 syllabus**. However, Lectures 049–051 on excitation phenomena cover **3rd harmonic behavior in Y-Y connections**, which overlaps with Slides L-11 S08-S09. If you find 3rd harmonic questions confusing, Lecture 049–050 can help.

#### [Lecture 047: Parallel Operation of Transformers](Lecture_047_Parallel_Operation_of_Transformers.md) `01:20:36`
- ⚪ Conditions for parallel operation, load sharing

#### [Lecture 048: Problems based on Parallel Operation of Transformer](Lecture_048_Problems_based_on_Parallel_Operation_of_Transformer.md) `01:04:18`
- ⚪ Parallel operation problems

#### [Lecture 049: Excitation Phenomenon 1](Lecture_049_Excitation_Phenomenon_1.md) `01:21:13`
- ⚪ Non-linear magnetization and harmonic generation
- 🟡 **3rd harmonic dominance** in magnetizing current — *useful for understanding Y-Y 3rd harmonic issues in Slides L-11 S08*

#### [Lecture 050: Excitation Phenomenon 2](Lecture_050_Excitation_Phenomenon_2.md) `00:57:03`
- ⚪ Triplen harmonic phase relationships
- 🟡 **Star connection triplen elimination** — *directly related to Y-Y grounding solutions in Slides L-11 S09*
- 🟡 **Delta circulating currents** for harmonic suppression

#### [Lecture 051: Excitation Phenomenon 3](Lecture_051_Excitation_Phenomenon_3.md) `01:10:18`
- ⚪ Oscillating neutral, tank stray losses
- 🟡 **Delta tertiary winding** for harmonic suppression — *mentioned in Slides L-11 S09*

#### [Lecture 052: Switching Transients](Lecture_052_Switching_Transients.md) `00:45:21`
- ⚪ Magnetizing inrush current, switching angle optimization

#### [Lecture 053: Problems based on Harmonics and Inrush Current](Lecture_053_Problems_based_on_Harmonics_and_Inrush_Current.md) `00:33:36`
- ⚪ Harmonic and inrush current problems

---

## Part 2: Three-Phase Induction Motor (Syllabus Chapter 2)
**Lectures 131–159 | Covers: RMF, Equiv Circuit, Torque-Speed, Testing, Starting, Speed Control, Braking, Induction Generator**

> **Syllabus scope**: Rotating magnetic field · Equivalent circuit · Vector diagram · Torque-speed characteristics · Effect of changing R₂ and X₂ · Motor torque & developed rotor power · No-load test · Blocked rotor test · Starting methods · Electric braking · Speed control · Induction generator

---

### 2.1 Introduction & Construction (131–134)

#### [Lecture 131: Induction Machines Introduction](Lecture_131_Induction_Machines_Introduction.md) `00:49:07`
- 🟢 **Working principle** — inductive energy transfer, no brushes *(Slides L-02 S03-S07)*
- 🟢 **Torque production** — Lorentz force on rotor conductors *(Slides L-03 S04-S05)*
- 🟡 Air gap optimization and reluctance — *deeper than slides*

#### [Lecture 132: Induction Machine Construction 1](Lecture_132_Induction_Machine_Construction_1.md) `00:48:50`
- 🟢 **Stator construction** and winding layout *(Slides L-02 S03)*
- 🟢 **Squirrel cage rotor** — skewing, operational characteristics *(Slides L-02 S06)*
- 🟡 Slot types: open, semi-open, closed — *not in slides*

#### [Lecture 133: Induction Machine Construction 2](Lecture_133_Induction_Machine_Construction_2.md) `00:44:05`
- 🟢 **Wound/Slip-ring rotor** — slip rings, brushes, external resistance *(Slides L-02 S06)*
- 🟢 **SCIM vs SRIM** comparison *(Slides L-02 S07)*
- 🟢 **Slip**: $s = (N_s - N)/N_s$ *(Slides L-03 S06-S07)*
- 🟢 **Rotor frequency**: $f_r = sf$ *(Slides L-03 S08)*

#### [Lecture 134: Inverted Induction Motor](Lecture_134_Inverted_Induction_Motor.md) `00:44:05`
- 🟡 Inverted IM concept — rotor excited, stator rotates — *not in syllabus/slides but builds deeper understanding of IM physics*
- ⚪ Induction machine as frequency changer — *not in syllabus*

---

### 2.2 Rotating Magnetic Field (135)

#### [Lecture 135: Rotating Magnetic Field](Lecture_135_Rotating_Magnetic_Field.md) `00:55:58`
- 🟢 **RMF** from 3-phase supply: resultant $\Phi_R = 1.5\Phi_m$ *(Syllabus: RMF; Slides L-02 S08-S14)*
- 🟢 Synchronous speed: $N_s = 120f/P$
- 🟢 Slip problems and rotor frequency calculations
- 🟡 Dual-fed machine analysis — *not in slides*
- ⚪ Cogging and supersynchronous rotor field speeds — *not in syllabus*

---

### 2.3 Equivalent Circuit (136–137)

#### [Lecture 136: Equivalent Circuit 1](Lecture_136_Equivalent_Circuit_1.md) `00:44:11`
- 🟢 **Induction motor phasor diagram** *(Syllabus: vector diagram; Slides L-03 S10-S14)*
- 🟢 **Standstill rotor EMF** $E_2$ and running EMF $sE_2$ *(Slides L-03 S11)*
- 🟢 **Air-gap power** $P_g$ concept *(Slides L-06 S04)*
- 🟢 **Developed torque** formulation *(Slides L-06 S06)*

#### [Lecture 137: Equivalent Circuit 2](Lecture_137_Equivalent_Circuit_2.md) `00:40:59`
- 🟢 **Complete per-phase equivalent circuit** *(Syllabus: equivalent circuit; Slides L-03 S20)*
- 🟢 **$R_2/s$ decomposition**: $R_2/s = R_2 + R_2(1-s)/s$ *(Slides L-03 S16-S18)*
- 🟢 **Power flow diagram** — $P_g : P_{cu} : P_{dev} = 1 : s : (1-s)$ *(Slides L-06 S05)*
- 🟢 Loss classification and efficiency

---

### 2.4 Losses, Power Flow & Efficiency (138)

#### [Lecture 138: Losses and Efficiency of Induction Machines](Lecture_138_Losses_and_Efficiency_of_Induction_Machines.md) `01:16:06`
- 🟢 **Motor torque and developed rotor power** *(Syllabus: motor torque and developed rotor power; Slides L-06 S03-S09)*
- 🟢 **Power flow cascade**: $P_{in} \to P_g \to P_{dev} \to P_{out}$ *(Slides L-06 S03-S08)*
- 🟢 **Golden ratio**: $P_g : sP_g : (1-s)P_g$ *(Slides L-06 S05)*
- 🟢 Efficiency: $\eta = P_{out}/P_{in}$ *(Slides L-06 S08)*
- 🟢 Worked problems on power flow and efficiency

---

### 2.5 Torque-Slip Characteristics (139–143)

#### [Lecture 139: Torque Slip Characteristics 1](Lecture_139_Torque_Slip_Characteristics_1.md) `00:40:00`
- 🟢 **Torque-speed characteristic** — motoring, generating, braking regions *(Syllabus: torque-speed characteristics; Slides L-04 S15-S16)*
- 🟢 **Starting torque** formula *(Slides L-04 S04-S05)*
- 🟢 Low-slip linear region ($T \propto s$) and high-slip region ($T \propto 1/s$) *(Slides L-04 S15)*
- 🟡 Thévenin equivalent of stator network — *deeper than slides*
- 🟡 Voltage dependence of torque ($T \propto V^2$) — *useful but not in slides*

#### [Lecture 140: Torque Slip Characteristics 2](Lecture_140_Torque_Slip_Characteristics_2.md) `00:50:20`
- 🟢 **Maximum torque / breakdown torque**: $T_{max} = \frac{K_1 E_2^2}{2X_2}$ *(Slides L-04 S14)*
- 🟢 **Breakdown slip**: $s_b = R_2/X_2$ *(Slides L-04 S12-S13)*
- 🟢 **Effect of rotor resistance** on torque-speed curves *(Syllabus: effect of changing R₂ and X₂; Slides L-04 S17)*
- 🟢 **Maximum starting torque condition**: $R_2 = X_2$ *(Slides L-04 S06)*
- 🟢 $T_{max}$ is independent of $R_2$ — only $s_b$ changes *(Slides L-04 S14)*

#### [Lecture 141: Torque Slip Characteristics 3](Lecture_141_Torque_Slip_Characteristics_3.md) `00:49:44`
- 🟢 **Effect of rotor resistance** on current, power factor, speed *(Syllabus: effect of changing R₂ and X₂)*
- 🟡 **V/f control** fundamentals — *speed control method, in syllabus broadly but not detailed in slides*
- 🟡 Power-slip characteristics and maximum mechanical power — *deeper than slides*
- 🟡 Operating characteristics curves: torque, PF, efficiency vs speed

#### [Lecture 142: Torque Slip Characteristics 1 (Problems)](Lecture_142_Torque_Slip_Characteristics_1.md) `01:20:24`
- 🟢 Torque ratio problems — developed torque at given slip
- 🟢 External rotor resistance addition problems *(connects to effect of R₂)*
- 🟢 Full-load slip from breakdown ratios
- 🟡 Induction generator frequency dynamics — *not in slides*

#### [Lecture 143: Torque Slip Characteristics 2 (Problems)](Lecture_143_Torque_Slip_Characteristics_2.md) `00:49:06`
- 🟢 Practice problems: $T_{FL}/T_{max}$ ratios, starting current ratios
- 🟢 External resistance for full-load torque at specified slip
- 🟡 Frequency-voltage scaling problems — *deeper than slides*

---

### 2.6 Stability & Testing (144–145)

#### [Lecture 144: Stability and Testing of Induction Motor](Lecture_144_Stability_and_Testing_of_Induction_Motor.md) `00:55:29`
- 🟡 Operating point stability criteria — *not explicitly in syllabus but useful for understanding why motors stall*
- 🟢 **No-load test** — measurements, impedance calculations *(Syllabus: no-load test; Slides L-05 S04-S08)*
- 🟢 **Separation of no-load losses** *(Slides L-05 S06-S08)*
- 🟢 **Blocked rotor test** — equivalent circuit, parameter extraction *(Syllabus: blocked rotor test; Slides L-05 S09-S11)*
- 🟢 Direct-on-line starting relations from blocked rotor data

#### [Lecture 145: Stability and Testing of Induction Machines](Lecture_145_Stability_and_Testing_of_Induction_Machines.md) `00:49:20`
- 🟢 Testing practice problems — full-load efficiency, parameter extraction
- 🟢 Starting torque at rated voltage from test data
- 🟡 No-load loss separation and drive stability — *supplementary*
- 🟡 Speed control via external rotor resistance — *connects to speed control section*

---

### 2.7 Circle Diagram (146)

> [!NOTE]
> The circle diagram is **NOT in the ECE 2207 syllabus text** but IS **covered in maam's slides** (L-07, Slides 22–24). Watch if you expect it might appear in the exam. Can skip if time is very tight.

#### [Lecture 146: Circle Diagram of Induction Motor](Lecture_146_Circle_Diagram_of_Induction_Motor.md) `01:03:26`
- 🟡 Semicircular locus derivation for rotor current *(Slides L-07 S22)*
- 🟡 Construction from no-load and blocked-rotor test points *(Slides L-07 S23)*
- 🟡 Graphical extraction of torque, power, efficiency, slip *(Slides L-07 S24)*
- 🟡 Torque line, output line, power line construction

---

### 2.8 Starting Methods (147–150)

#### [Lecture 147: Starting of SCIM](Lecture_147_Starting_of_SCIM.md) `00:50:16`
- 🟢 **Starting problem**: $I_{st} \approx 5\text{–}8 \times I_{FL}$ *(Slides L-06 S11)*
- 🟢 **DOL starting** *(Slides L-06 S12)*
- 🟢 **Stator resistance/reactance starting**: $I_{st} = xI_{sc}$, $T_{st} = x^2 T_{sc}$ *(Slides L-06 S13-S14)*
- 🟢 **Auto-transformer starting**: line current $= x^2 I_{sc}$ *(Slides L-06 S15-S17)*
- 🟢 **Star-Delta starting**: $I_{st} = \frac{1}{3}I_{sc,\Delta}$, $T_{st} = \frac{1}{3}T_{sc,\Delta}$ *(Slides L-06 S18)*

#### [Lecture 148: Starting of SCIM (Problems)](Lecture_148_Starting_of_SCIM.md) `01:02:50`
- 🟢 Starting problems — external resistance, feeder effects
- 🟡 Constant V/f starting — *mentioned in speed control context*
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
- 🟢 **Stator voltage control** *(Slides L-07 S03)*
- 🟢 **Rotor resistance control** *(Slides L-07 S03)*
- 🟡 Rotor EMF injection (Scherbius/Kramer) — *mentioned in Slides L-07 S03 but not detailed*
- 🟡 Sub-synchronous vs super-synchronous modes

#### [Lecture 152: Speed Control of Induction Motor 2](Lecture_152_Speed_Control_of_Induction_Motor_2.md) `00:43:42`
- 🟢 **Supply frequency control (V/f control)** *(Slides L-07 S03)*
- 🟢 **Changing stator poles** — consequent poles *(Slides L-07 S03)*
- 🟡 V/f profile, low-frequency voltage boost — *deeper than slides*
- 🟡 Cascading of induction motors — *mentioned in Slides L-07 S03 but not detailed*

#### [Lecture 153: Speed Control of IM 1 (Problems)](Lecture_153_Speed_Control_of_IM_1.md) `00:54:10`
- 🟢 Speed control practice problems — rotor resistance insertion
- 🟢 Fan load analysis and minimum rotor resistance
- 🟡 Consequent pole modification problems

#### [Lecture 154: Speed Control of IM 2 (Problems)](Lecture_154_Speed_Control_of_IM_2.md) `00:45:46`
- 🟢 Practice: frequency scaling, rotor resistance control
- 🟡 V/f flux constraints, frequency variation effects

---

### 2.10 Electric Braking (155–156)

#### [Lecture 155: Braking of Induction Motor](Lecture_155_Braking_of_Induction_Motor.md) `00:27:37`
- 🟢 **Regenerative braking** — motor driven above $N_s$ *(Slides L-07 S06)*
- 🟢 **DC injection braking** — stationary field *(Slides L-07 S07)*
- 🟢 **Plugging** — reversing two stator leads, $s \approx 2$ *(Slides L-07 S09)*
- 🟡 Dynamic equations of plugging, skin effect — *deeper than slides*

#### [Lecture 156: Braking of Induction Motor (Problems)](Lecture_156_Braking_of_Induction_Motor.md) `00:27:06`
- 🟢 Braking practice problems
- 🟢 Operating modes and braking torque comparison

---

### 2.11 Deep Bar, Double Cage & Induction Generator (157–159)

#### [Lecture 157: High Torque Cage Rotor](Lecture_157_High_Torque_Cage_Rotor.md) `00:25:10`
- 🟡 **Deep bar rotor** — skin effect enhances starting torque — *relates to effect of rotor resistance (syllabus) but not in slides*
- 🟡 **Double cage rotor** — outer cage high R (starting), inner cage low R (running) — *not in slides*
- 🟡 Equivalent circuit modeling of double cage

#### [Lecture 158: Miscellaneous Concepts](Lecture_158_Miscellaneous_Concepts.md) `00:46:21`
- 🟡 Crawling and cogging phenomena — *not in syllabus/slides but commonly asked*
- 🟢 **Induction generator principles** — reactive power requirements *(Syllabus: induction generator; Slides L-07 S10-S12)*
- 🟢 Self-excited vs grid-connected induction generator *(Slides L-07 S11-S12)*

#### [Lecture 159: High Torque Cage Rotor and Induction Generator](Lecture_159_High_Torque_Cage_Rotor_and_Induction_Generator.md) `00:45:10`
- 🟡 Double cage standstill torque formulation — *relates to rotor resistance effects*
- 🟢 **Induction generator** problems — operating speeds, power flow *(Syllabus: induction generator)*
- 🟡 Parasitic phenomena: cogging vs crawling, deep bar current distribution

---

## Part 3: Single-Phase Induction Motor (Syllabus Chapter 3)
**Lectures 160–162 | Covers: Theory of operation, Equivalent circuit, Starting methods**

> **Syllabus scope**: Theory of operation · Equivalent circuit · Starting methods

---

#### [Lecture 160: Single Phase Induction Motor 1](Lecture_160_Single_Phase_Induction_Motor_1.md) `00:36:02`
- 🟢 **Double revolving field theory** — alternating flux → two opposing rotating fields *(Syllabus: theory of operation; Slides L-07 S15-S16)*
- 🟢 **Zero starting torque** at standstill ($T_f = T_b$) *(Slides L-07 S16)*
- 🟢 **Equivalent circuit** for forward and backward fields *(Syllabus: equivalent circuit)*
- 🟢 **Torque-speed characteristics** of 1-φ IM

#### [Lecture 161: Single Phase Induction Motor 2](Lecture_161_Single_Phase_Induction_Motor_2.md) `00:49:18`
- 🟢 **Split-phase motor** — high R auxiliary winding, ~30° phase split *(Syllabus: starting methods; Slides L-07 S18)*
- 🟢 **Capacitor-start motor** — ~80° phase split, high starting torque *(Slides L-07 S19)*
- 🟢 **Capacitor-start capacitor-run** and PSC motors *(Slides L-07 S21)*
- 🟡 Maximum starting torque derivation in capacitor motors — *deeper than slides*
- 🟡 Direction of rotation determination — *useful but not in slides*

#### [Lecture 162: Single Phase Induction Motor (Problems)](Lecture_162_Single_Phase_Induction_Motor.md) `00:49:06`
- 🟢 Practice problems on 1-φ IM equivalent circuit
- 🟢 Phase difference criterion and rotor direction
- 🟡 Full equivalent circuit input impedance and current — *deeper than slides*
- 🟡 Maximum starting torque capacitance calculation

---

## Quick Reference: Watch Priority Summary

### 🔴 Highest Priority (Must Watch)
These directly map to syllabus topics that appeared in maam's slides:

| Syllabus Topic | Lectures |
|---|---|
| Transformation ratio, EMF equation | 014, 015 |
| No-load & load vector diagrams | 014, 015, 017 |
| Equivalent circuit (TF) | 018, 019, 020 |
| OC test / SC test (TF) | 021 |
| Voltage regulation | 027 |
| 3-phase connections (Y-Y, Y-Δ, Δ-Y, Δ-Δ) | 038, 039, 040 |
| Vector groups | 038, 039, 040 |
| Open-Delta, Scott-T | 043, 045 |
| RMF | 135 |
| Equivalent circuit (IM) | 136, 137 |
| Torque-speed characteristics | 139, 140 |
| Effect of R₂, X₂ on torque | 140, 141 |
| Motor torque & developed power | 138 |
| No-load test / Blocked rotor test (IM) | 144 |
| Starting methods | 147, 149 |
| Speed control | 151, 152 |
| Electric braking | 155 |
| Induction generator | 158, 159 |
| 1-φ IM theory & starting | 160, 161 |

### 🟡 Secondary Priority
| Topic | Lectures | Why |
|---|---|---|
| Losses & efficiency (TF) | 024–026 | Closely tied to OC/SC testing |
| Circle diagram | 146 | In slides but not syllabus |
| Deep bar / double cage | 157 | Relates to R₂ effects |
| 3rd harmonics in Y-Y | 049–050 | Helps with 3-phase TF questions |

### 🔵 Watch If Needed
| Topic | Lectures |
|---|---|
| EM fundamentals | 004, 005 |
| Magnetic circuits | 007 |
| All foundations | 001–010 |

### ⚪ Skip
| Topic | Lectures |
|---|---|
| Auto-transformer | 032–035 |
| Parallel operation (TF) | 047–048 |
| Excitation transients | 051–053 |
| Coupled circuits, scaling | 029–031, 036 |
