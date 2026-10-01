---
course: "ECE-2207: Electrical Machines-I"
institution: "Rajshahi University of Engineering & Technology (RUET)"
department: "Department of Electrical & Computer Engineering (ECE)"
instructor: "Fariya Tabassum (FT Mam), Assistant Professor"
student_author: "Raidah (Roll: 2310035)"
digitized_date: "30.09.2026"
total_classes: 18
total_scan_images: 32
total_notebook_pages: 61
total_extracted_diagrams: 35
---

# ECE-2207: Electrical Machines-I — Master Lecture Notes

> **Instructor**: Fariya Tabassum (*FT Mam*), Assistant Professor, Dept. of ECE, RUET  
> **Class Notes Author**: Raidah (Roll: 2310035)  
> **Semester**: 2-2 Semester Final Preparation  
> **Source Documents**: `Machine Classnote - 2310035.pdf` (32 scans / 61 notebook pages)  
> **Slide Repository**: [`../SlidesByMaam/`](../SlidesByMaam/map.md)

---

## 1. Syllabus & Section Architecture

The ECE-2207 curriculum is divided into two distinct examination sections:

```text
ECE-2207: Electrical Machines-I
├── SECTION B: Induction Motors (Classes 01 – 12)
│    ├── Module 1: Fundamentals & Rotating Magnetic Field (Classes 01 – 05)
│    ├── Module 2: Performance, Torque Equations & Testing (Classes 06 – 09)
│    └── Module 3: Power Stages, Starting, Speed Control & Braking (Classes 10 – 12)
└── SECTION A: Transformers (Classes 13 – 18)
     ├── Module 4: 1-Phase Transformers, Leakage Reactance & Regulation (Classes 13 – 15)
     └── Module 5: 3-Phase Transformers, Harmonics, V-V / Scott & Vector Groups (Classes 16 – 18)
```

---

## 2. Master Lecture Table of Contents

| Class # | Date | Scan Pages | Primary Topics | Lecture File Link |
|:---|:---|:---|:---|:---|
| **Class 01** | `23.06.2026` | P01 – P03 | Course outline; Motor working criteria; Faraday's law; Magnetic vs Electric fields; Generator vs Motor concept | [Class 01: Introduction & Working Principles](Class_01_Introduction_and_Working_Principles.md) |
| **Class 02** | *Undated* | P04 – P05 | Electromagnetic fields; Induced voltage $E \propto B l v \sin\theta$; Generator vs Alternator; Fleming's Left & Right hand rules; Transients | [Class 02: Electromagnetic Fields & Hand Rules](Class_02_Electromagnetic_Fields_and_Hand_Rules.md) |
| **Class 03** | `30.06.2026` | P06 – P08 (top) | Stator & Rotor; Induction Motor as a "Rotating Transformer"; Advantages & Disadvantages; Single-phase fan capacitor split; Core losses | [Class 03: IM Basics & Rotating Transformer](Class_03_Induction_Motor_Basics_and_Stator_Rotor.md) |
| **Class 04** | `01.07.2026` | P08 (bot) – P10 (left) | RMF Revolving field theory; Two-phase mathematical proof ($\Phi_r = \Phi_m$); Three-phase proof ($\Phi_r = 1.5\,\Phi_m$ at synchronous speed) | [Class 04: Production of RMF Mathematical Proof](Class_04_Rotating_Magnetic_Field_RMF_Proof.md) |
| **Class 05** | `07.07.2026` | P10 (right) – P12 | RMF conditions; Generator-Motor action sequence; Back EMF ($E_b$) and starter need; Slip definition; Equivalent circuit & Phasor diagram | [Class 05: RMF Conditions, Slip & IM Phasor](Class_05_RMF_Conditions_and_IM_Phasor_Diagram.md) |
| **Class 06** | *Undated* | P13 – P14 (left) | Rotor frequency $f_r = s f$; Speed math; Leakage flux & leakage reactance origin; Winding placement (HV outer, LV inner); Machine operating modes | [Class 06: Slip, Rotor Frequency & Reactance](Class_06_Slip_Rotor_Frequency_and_Transformer_Analogy.md) |
| **Class 07** | `14.07.2026` | P14 (right) – P15 (left) | Rotor torque proportionality ($T \propto E_2 I_2 \cos\phi_2$); Derivation of starting torque $T_{st}$; Condition for max starting torque ($R_2 = X_2$) | [Class 07: Rotor Torque Equation Derivation](Class_07_Rotor_Torque_Equation_Derivation.md) |
| **Class 08** | `20.07.2026` | P15 (right) – P17 (left) | Running torque $T_r$; Max running torque condition ($R_2 = s X_2$); Independence of $T_{max}$ on $R_2$; Torque-slip & Torque-speed curves | [Class 08: Maximum Torque & Torque-Slip Curve](Class_08_Maximum_Torque_and_Torque_Slip_Curve.md) |
| **Class 09** | `21.07.2026` | P17 (right) – P19 (left) | Induction Motor Testing: No-Load (Open-circuit) test; Blocked-rotor (Short-circuit) test; DC resistance test (Wye vs Delta conversion) | [Class 09: Induction Motor Testing](Class_09_Induction_Motor_Testing.md) |
| **Class 10** | `05.08.2026` | P19 (right) – P20 | Fixed vs variable losses; The 3 power flow stages ($P_1 \to P_2 \to P_m \to P_{sh}$); Proof of $P_2 : P_m : P_{rc} = 1 : (1-s) : s$; Synchronous Watt | [Class 10: Power Stages & Efficiency](Class_10_Power_Stages_and_Efficiency.md) |
| **Class 11** | `09.08.2026` | P21 | Inrush starting current hazards; Torque-current ratio proof: $\frac{T_{st}}{T_f} = (\frac{I_{st}}{I_f})^2 s_f$; Starting methods (DOL, Star-Delta, Auto-transf, Rotor resistance) | [Class 11: Induction Motor Starting Methods](Class_11_Induction_Motor_Starting_Methods.md) |
| **Class 12** | `16.08.2026` | P22 – P23 | Speed control methods; Electric braking (Plugging, DC dynamic, Capacitor braking); Induction Generator ($N_r > N_s$); 3-quadrant torque-speed curve | [Class 12: Speed Control & Electric Braking](Class_12_Speed_Control_and_Electric_Braking.md) |
| **Class 13** | `23.08.2026` | P24 – P25 | Transformer definition; Why DC cannot be applied (Core saturation); No-load current components ($I_w, I_\mu$); Leakage reactance origin; IM comparison | [Class 13: Transformer Principles & Construction](Class_13_Transformer_Principles_and_Construction.md) |
| **Class 14** | `06.09.2026` | P26 | Transformation ratio $K$; Parameter shifting principles ($R_2' = R_2/K^2$); Total equivalent impedance ($Z_{01}, Z_{02}$); Practical loaded phasor diagram | [Class 14: Equivalent Circuit & Parameter Shifting](Class_14_Equivalent_Circuit_and_Parameter_Shifting.md) |
| **Class 15** | *Undated* | P27 (left) | Percentage Voltage Regulation (%VR); Comprehensive comparison matrix between Induction Motor and Transformer tests; Lab exam tips | [Class 15: Voltage Regulation & IM Comparison](Class_15_Voltage_Regulation_and_IM_Comparison.md) |
| **Class 16** | `12.09.2026` | P27 (right) – P29 (left) | 3-phase transformers (Single unit vs 3-unit bank); Phase relations in Star & Delta; Unbalanced load reaction; Third harmonics & humming mitigation | [Class 16: 3-Phase Transformers & Harmonics](Class_16_Three_Phase_Transformers_and_Harmonics.md) |
| **Class 17** | `16.09.2026` | P29 (right) – P31 | $30^\circ$ phase shift in Y-$\Delta$; Open-Delta (V-V) connection & $57.7\%$ capacity proof; Scott-T connection & derivation of the $86.6\%$ teaser tap | [Class 17: Two-Transformer Connections (V-V & Scott-T)](Class_17_Two_Transformer_Connections_OpenDelta_ScottT.md) |
| **Class 18** | `20.09.2026` | P32 | Three-phase proofs review; Lab final and quiz guidelines; Transformer Vector Groups (Clock convention, Dyn1, Dyn11, Yyn6); Parallel criteria | [Class 18: Vector Groups & Review](Class_18_Transformer_Vector_Groups_and_Review.md) |

---

## 3. Core Mathematical Cheatsheet

### A. Induction Motor Essentials
- **Synchronous Speed**:
  $$N_s = \frac{120 f_s}{P}$$
- **Rotor Speed & Slip**:
  $$s = \frac{N_s - N_r}{N_s}, \quad N_r = N_s(1 - s), \quad f_r = s \cdot f_s$$
- **Torque Equation**:
  $$T_r = \frac{3}{2\pi N_s} \cdot \frac{s \cdot E_2^2 \cdot R_2}{R_2^2 + (s X_2)^2}$$
- **Condition for Maximum Starting Torque**:
  $$R_2 = X_2$$
- **Condition for Maximum Running Torque & Slip**:
  $$s_{max} = \frac{R_2}{X_2} \implies T_{max} = \frac{3}{2\pi N_s} \cdot \frac{E_2^2}{2 X_2} \quad (\text{independent of } R_2, \text{ proportional to } V^2)$$
- **Power Division Proportion**:
  $$\boxed{P_2 : P_m : P_{rc} = 1 : (1 - s) : s}$$
- **Starting to Full-Load Torque Ratio**:
  $$\frac{T_{st}}{T_f} = \left(\frac{I_{st}}{I_f}\right)^2 \cdot s_f$$

### B. Transformer Essentials
- **Transformation Ratio ($K$)**:
  $$K = \frac{N_2}{N_1} = \frac{E_2}{E_1} = \frac{I_1}{I_2}$$
- **Parameter Shifting**:
  $$R_2' = \frac{R_2}{K^2}, \quad X_2' = \frac{X_2}{K^2}, \quad R_1' = K^2 R_1, \quad X_1' = K^2 X_1$$
- **Voltage Regulation**:
  $$\%VR = \frac{V_{s,nl} - V_{s,fl}}{V_{s,fl}} \times 100\%$$
- **Open-Delta ($\text{V}-\text{V}$) Capacity**:
  $$\frac{\text{Rating}_{\text{V}-\text{V}}}{\text{Rating}_{\Delta-\Delta}} = \frac{1}{\sqrt{3}} \approx 57.7\% \quad (\text{utilizing } 86.6\% \text{ of the remaining two units})$$
- **Scott-T Teaser Transformer Turns**:
  $$V_{teaser} = \frac{\sqrt{3}}{2} V_L = 0.866 \cdot V_L \implies \text{Turns} = 86.6\% \text{ of Main Transformer}$$

---

## 4. Cross-Reference with Lecture Slides

The digitized handwritten notes align with the corresponding typed lecture slide modules in `../SlidesByMaam/`:

| Slide Deck | Slide File | Aligned Class Notes | Primary Shared Focus |
|:---|:---|:---|:---|
| **Lecture 01** | [`L-01_ECE-2207.md`](../SlidesByMaam/L-01_ECE-2207.md) | Class 01 | Course roadmap, magnetic principles, Faraday's law |
| **Lecture 02** | [`L-02_ECE-2207.md`](../SlidesByMaam/L-02_ECE-2207.md) | Class 02 | Electromagnetic fields, generation basics, hand rules |
| **Lecture 03** | [`L-03_ECE-2107.md`](../SlidesByMaam/L-03_ECE-2107.md) | Class 03, 04 | Induction motor construction, stator/rotor, RMF proofs |
| **Lecture 04** | [`L-04_ECE-2107.md`](../SlidesByMaam/L-04_ECE-2107.md) | Class 05, 06 | Slip, rotor frequency, equivalent circuit, phasor |
| **Lecture 05** | [`L-05_ECE-2107.md`](../SlidesByMaam/L-05_ECE-2107.md) | Class 07, 08 | Rotor torque equations, $T_{max}$, torque-slip characteristics |
| **Lecture 06** | [`L-06_ECE-2107.md`](../SlidesByMaam/L-06_ECE-2107.md) | Class 09 | Motor testing: No-load, blocked rotor & DC resistance |
| **Lecture 07** | [`L-07_ECE-2107.md`](../SlidesByMaam/L-07_ECE-2107.md) | Class 10, 11 | Power flow stages, efficiency, inrush current & starting |
| **Lecture 08** | [`L-08_ECE-2207.md`](../SlidesByMaam/L-08_ECE-2207.md) | Class 12 | Speed control, electric braking (plugging), induction generator |
| **Lecture 09** | [`L-09_ECE-2107.md`](../SlidesByMaam/L-09_ECE-2107.md) | Class 13, 14 | Transformer principles, leakage reactance, parameter shifting |
| **Lecture 10** | [`L-10_ECE-2107.md`](../SlidesByMaam/L-10_ECE-2107.md) | Class 15, 16 | Voltage regulation, 3-phase transformers, 3rd harmonics |
| **Lecture 11** | [`L-11_ECE-2107.md`](../SlidesByMaam/L-11_ECE-2107.md) | Class 17, 18 | V-V open delta, Scott-T connection, Vector groups |
