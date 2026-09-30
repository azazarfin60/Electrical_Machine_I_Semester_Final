---
class: "15"
date: "Undated"
instructor: "Fariya Tabassum (FT Mam)"
course: "ECE-2207: Electrical Machines-I"
student: "Raidah (Roll: 2310035)"
scan_pages: ["027"]
notebook_pages: ["27_L"]
topics:
  - Voltage Regulation Definition & Formula
  - Part A (Transformer) vs Part B (Induction Motor) Syllabus Structure
  - Comparison of Testing Methodologies: No-Load vs Open Circuit
  - Comparison of Testing Methodologies: Blocked Rotor vs Short Circuit
  - High Voltage Side Shorting Precautions (Variac Control)
  - Dominant Losses in Each Test
  - Exam and Lab Final Guidelines
---

# Class 15: Transformer Voltage Regulation & Systematic IM Comparison

> **Instructor**: Fariya Tabassum (FT Mam)  
> **Source Scan Pages**: P27_L  
> [← Previous Class: Class 14](Class_14_Equivalent_Circuit_and_Parameter_Shifting.md) | [📚 Index](00_Index_and_Topic_Map.md) | [Next Class: Class 16 →](Class_16_Three_Phase_Transformers_and_Harmonics.md)

---

## 1. Transformer Voltage Regulation (%VR)

<!-- Page 27_L -->

**Voltage Regulation (%VR)** is defined as the percentage change in secondary terminal voltage from no-load to full-load condition:

$$\boxed{\%VR = \frac{V_{s,nl} - V_{s,fl}}{V_{s,fl}} \times 100\%}$$

- $V_{s,nl}$: Secondary terminal voltage at no-load ($= E_2$)
- $V_{s,fl}$: Secondary terminal voltage at full load ($= V_2$)
- **Ideal Value**: For an ideal transformer, $\%VR = 0\%$ (i.e., secondary terminal voltage remains perfectly constant regardless of connected load).

---

## 2. Systematic Comparison: Induction Motor vs. Transformer

The ECE-2207 course syllabus is divided into two symmetrical halves:
- **PART A**: Transformer
- **PART B**: Induction Motor

```text
Course Architecture & Testing Parallels
├── No-Load Condition
│    ├── Induction Motor: No-Load Test   ──> Small current, Cu loss negligible, Core loss dominates
│    └── Transformer: Open Circuit (OC)  ──> Small current, Cu loss negligible, Core loss dominates
└── Full-Load / Locked Condition
     ├── Induction Motor: Blocked Rotor  ──> Low voltage applied, Core loss negligible, Cu loss dominates
     └── Transformer: Short Circuit (SC) ──> Low voltage applied, Core loss negligible, Cu loss dominates
```

$$\begin{array}{|l|l|l|}
\hline
\textbf{Feature} & \textbf{Induction Motor (Part B)} & \textbf{Transformer (Part A)} \\
\hline
\text{No-Load Test} & \text{No-Load Test} & \text{Open Circuit (OC) Test} \\
\text{Measurement Focus} & \text{Core loss } (P_i) + \text{Friction/Windage } (P_{w,f}) & \text{Core loss } (P_i = P_h + P_e) \\
\text{Current Level} & \approx 30 - 40\% \text{ of rated (large due to airgap)} & \approx 2 - 5\% \text{ of rated (very small)} \\
\text{Copper Loss} & \text{Negligible } (I_0^2 R \approx 0) & \text{Negligible } (I_0^2 R \approx 0) \\
\hline
\text{Full-Current Test} & \text{Blocked Rotor Test (BLR)} & \text{Short Circuit (SC) Test} \\
\text{Measurement Focus} & \text{Copper loss } (P_{cu}), R_1+R_2, X_1+X_2 & \text{Equivalent Copper loss } (P_{cu}), R_{01}, X_{01} \\
\text{Voltage Applied} & \text{Reduced voltage (10--15\% of rated)} & \text{Reduced voltage (5--10\% through Variac)} \\
\text{Core Loss} & \text{Negligible (due to very low voltage)} & \text{Negligible (due to very low voltage)} \\
\hline
\end{array}$$

> [!WARNING]
> **Short Circuit Test Safety Precaution**
> Short-circuiting the high-voltage winding could cause destructive current rushes and core saturation hazards.  
> Therefore, in the short-circuit test, **the low-voltage (LV) winding is always short-circuited, and a carefully controlled, small reduced voltage is applied to the high-voltage (HV) side via a Variac** (ensuring safe, easily measurable currents with standard laboratory meters).

---

## 3. Examination & Laboratory Hints

- **Lab Final**:
  - **Circuit Diagrams**: Clean, accurate schematic and wiring diagrams must be drawn independently in the lab final exam.
- **Lab Quiz**:
  - **Quiz Structure**: Short conceptual questions and technical fill-in-the-blanks will be assessed.

---

[← Previous Class: Class 14](Class_14_Equivalent_Circuit_and_Parameter_Shifting.md) | [📚 Back to Index](00_Index_and_Topic_Map.md) | [Next Class: Class 16 →](Class_16_Three_Phase_Transformers_and_Harmonics.md)
