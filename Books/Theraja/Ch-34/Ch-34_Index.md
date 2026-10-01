---
title: "Chapter 34: Induction Motor — Master Navigation & Comprehensive Study Guide"
author: "B.L. Theraja & A.K. Theraja"
book: "A Textbook of Electrical Technology — Volume II (AC & DC Machines)"
chapter: 34
total_pages: 70
source_file: "Ch-34.pdf"
subject: "ECE 2207: Electrical Machines"
tags:
  - electrical-engineering
  - induction-motor
  - syllabus-guide
  - obsidian-vault
  - master-index
---

# Chapter 34: Induction Motor
## Master Navigation & Comprehensive Study Guide
**Textbook:** *A Textbook of Electrical Technology (Vol. II — AC & DC Machines)* by B.L. Theraja & A.K. Theraja  
**Chapter Scope:** Pages 1243–1312 (70 PDF pages, complete 100% word-for-word digitization with vector-extracted diagrams)

---

## 📚 Vault Module Structure

To ensure lightning-fast rendering, seamless Obsidian mobile & desktop navigation, and focused topic study, this 70-page chapter has been organized into four modular study units:

```
Ch-34/
├── Ch-34_Index.md                              <-- Master Curriculum & Navigation Hub (You are here)
├── Ch-34_01_Construction_and_RMF.md             <-- Part 1: Construction & Rotating Magnetic Field
├── Ch-34_02_Torque_and_Characteristics.md      <-- Part 2: Torque Equations & Motor Characteristics
├── Ch-34_03_Power_Stages_and_Torque.md          <-- Part 3: Power Stages & Torque Relations
└── Ch-34_04_Linear_Motors_and_Equivalent_Circuit.md <-- Part 4: Linear Motors & Equivalent Circuit
```

---

## 📑 Detailed Table of Contents

### [Part 1: Construction & Rotating Magnetic Field](Ch-34_01_Construction_and_RMF.md)
* **Pages:** 1243–1256 (PDF pp. 1–14)
* **Core Articles:**
  * **34.1:** Classification of A.C. Motors (Induction, Synchronous, Commutator)
  * **34.2:** Induction Motor: General Principle
  * **34.3:** Construction (Stator core, windings, frame)
  * **34.4:** Squirrel-cage Rotor (End-rings, uninsulated copper/aluminum bars, skewing)
  * **34.5:** Phase-wound Rotor (Slip-ring rotor, 3-phase star-connected distributed winding)
  * **34.6:** Production of Rotating Field (Physical concepts of revolving stator flux)
  * **34.7:** Mathematical Proof for 2-Phase Supply ($\Phi_r = \Phi_m$ constant magnitude)
  * **34.8:** Mathematical Proof for 3-Phase Supply ($\Phi_r = 1.5 \Phi_m$ constant magnitude revolving at $\omega\text{ rad/s}$)
  * **34.9:** Why Does the Rotor Rotate? (Lenz's Law, force $F = BIl$)
  * **34.10:** Slip (Definition, fractional slip $s$, percentage slip, slip speed)
  * **34.11:** Frequency of Rotor Current ($f_r = s f$)
* **Worked Examples:** 34.1 to 34.5 (Speed, slip, rotor frequency, poles)
* **Diagrams:** Figures 34.1 to 34.16 + cutaway stator/rotor photographs.

---

### [Part 2: Torque Equations & Motor Characteristics](Ch-34_02_Torque_and_Characteristics.md)
* **Pages:** 1256–1280 (PDF pp. 14–38)
* **Core Articles:**
  * **34.12:** Relation between Torque and Rotor Power Factor ($T \propto \Phi I_2 \cos \phi_2$)
  * **34.13:** Starting Torque ($T_{st}$) derivation
  * **34.14:** Starting Torque of a Squirrel-cage Motor
  * **34.15:** Starting Torque of a Slip-ring Motor (Addition of external resistance)
  * **34.16:** Condition for Maximum Starting Torque ($R_2 = X_2$)
  * **34.17:** Effect of Change in Supply Voltage on Starting Torque ($T_{st} \propto V^2$)
  * **34.18:** Rotor E.M.F. and Reactance Under Running Conditions ($E_r = s E_2$, $X_r = s X_2$)
  * **34.19:** Torque Under Running Conditions ($T \propto \frac{s E_2^2 R_2}{R_2^2 + (s X_2)^2}$)
  * **34.20:** Condition for Maximum Torque Under Running Conditions ($R_2 = s X_2$ or $s_m = R_2/X_2$)
  * **34.21:** Maximum Torque ($T_{max} \propto \frac{E_2^2}{2 X_2}$, independent of $R_2$)
  * **34.22:** Full-load Torque and Maximum Torque Ratio ($\frac{T_f}{T_{max}} = \frac{2 a s_f}{a^2 + s_f^2}$)
  * **34.23:** Starting Torque and Maximum Torque Ratio ($\frac{T_{st}}{T_{max}} = \frac{2 a}{1 + a^2}$)
  * **34.24:** Effect of Change in Supply Voltage on Torque and Speed
  * **34.25:** Effect of Change in Supply Frequency on Torque and Speed
  * **34.26:** Full-load Torque and Starting Torque Ratio
  * **34.27:** Torque-Speed and Torque-Slip Curves (Stable and unstable operating regions)
  * **34.28:** Current-Torque Curve of an Induction Motor
  * **34.29:** Current-Speed Curve of an Induction Motor
  * **34.30:** Operating Modes (Motoring mode $0 < s < 1$, Generating mode $s < 0$, Braking/Plugging mode $s > 1$)
  * **34.31:** Complete Torque-Speed Characteristic ($-\infty < N < +\infty$)
  * **34.32:** Crawling (Harmonic torques, 7th harmonic forward crawl at $\approx N_s/7$)
  * **34.33:** Cogging or Magnetic Locking (Harmonic teeth alignment, remedies)
* **Worked Examples:** 34.6 to 34.26 (Extensive numerical analysis of torques, slips, and external resistors)
* **Practice Sets:**
  * **Tutorial Problem No. 34.1:** Starting & Maximum Torque Ratios (8 Problems)
  * **Tutorial Problem No. 34.2:** Slip, Running Torque & Resistance Variation (15 Problems)
* **Diagrams:** Figures 34.17 to 34.32.

---

### [Part 3: Power Stages & Torque Relations](Ch-34_03_Power_Stages_and_Torque.md)
* **Pages:** 1278–1296 & 1298–1300 (PDF pp. 36–54 & pp. 56–58)
* **Core Articles:**
  * **34.34:** Power Stages in an Induction Motor:
    $$\text{Stator Input } (P_1) \xrightarrow{-\text{Stator Losses}} \text{Rotor Input } (P_2) \xrightarrow{-\text{Rotor Cu Loss } (P_{cr})} \text{Gross Mechanical Power } (P_m) \xrightarrow{-\text{Friction \& Windage}} \text{Shaft Output } (P_{out})$$
  * **34.35:** Fundamental Power Ratio:
    $$P_2 : P_{cr} : P_m = 1 : s : (1 - s)$$
  * **34.36:** Torque Developed in Synchronous Watts ($T_g = P_2\text{ synchronous watts}$)
  * **34.37:** Induction Motor Efficiency and Slip Relations ($\text{Rotor efficiency} = 1 - s = N/N_s$)
  * **34.38:** Shaft Torque and Gross Mechanical Torque Relations
  * **34.39:** Condition for Maximum Mechanical Power Output
  * **34.40:** Calculation of Stator Current and Power Factor
  * **34.41:** Measurement of Slip (Stroboscopic method, Galvanometer method, Tachometer method)
  * **34.42:** Determination of Rotor Resistance and Reactance by Blocked-Rotor Test
* **Worked Examples:** 34.27 to 34.51 (Complete numerical problem coverage)
* **Practice Set:**
  * **Tutorial Problem No. 34.3:** Power Balance, Slip, Losses & Efficiency (19 Problems)
* **Diagrams:** Figures 34.33 to 34.40 + Power Stage block diagrams.

---

### [Part 4: Linear Induction Motors & Equivalent Circuit](Ch-34_04_Linear_Motors_and_Equivalent_Circuit.md)
* **Pages:** 1296–1311 (PDF pp. 54–69)
* **Core Articles:**
  * **34.43:** Sector Induction Motor (Construction, flux travel, power rating reduction)
  * **34.44:** Linear Induction Motor (LIM) ($v_s = 2 w f$, reaction plates)
  * **34.45:** Properties of Linear Induction Motor (Synchronous speed, slip, thrust $F = P_2/v_s$, power flow)
  * **34.46:** Magnetic Levitation (Physics of tractive vs levitation forces, high-speed space shift $\Delta t$, M-Bahn transit)
  * **34.47:** Induction Motor as a Generalized Transformer (Phasor diagram, why stator and rotor fields are stationary relative to each other in space)
  * **34.48:** Rotor Output Derivation via Transformer Model
  * **34.49:** Equivalent Circuit of the Rotor ($R_2/s = R_2 + R_L$, where $R_L = R_2(1/s - 1)$)
  * **34.50:** Complete & Approximate Equivalent Circuit of Induction Motor (Transformation to stator)
  * **34.51:** Power Balance Equations from Equivalent Circuit
  * **34.52:** Maximum Power Output Theorem ($R_L = Z_{01}$)
  * **34.53:** Corresponding Slip for Maximum Power Output ($s = \frac{R_2}{R_2 + Z_{01}}$) and $P_{g\text{ max}} = \frac{3 V_1^2}{2(R_{01} + Z_{01})}$
* **Worked Examples:** 34.52 to 34.60 (LIM calculations, equivalent circuit solving, exact & approximate methods)
* **Practice Sets:**
  * **Tutorial Problem No. 34.4:** Equivalent Circuit & Maximum Power Output (3 Problems)
  * **Objective Tests – 34:** Complete 28 Multiple-Choice & Fill-in-the-Blank examination questions with worked explanations and master answer key.
* **Diagrams:** Figures 34.41 to 34.59 + Maglev color photo.

---

## ⚡ Key Formula Cheatsheet

| Parameter / Relation | Formula | Unit / Notes |
|:---|:---|:---|
| **Synchronous Speed** | $N_s = \frac{120 f}{P}$ | $\text{rpm}$ |
| **Fractional Slip** | $s = \frac{N_s - N}{N_s}$ | Dimensionless ($0 \le s \le 1$) |
| **Rotor Speed** | $N = N_s (1 - s)$ | $\text{rpm}$ |
| **Rotor Frequency** | $f_r = s f$ | $\text{Hz}$ |
| **Rotor EMF per phase** | $E_r = s E_2$ | $\text{V}$ |
| **Rotor Standstill Impedance** | $Z_2 = \sqrt{R_2^2 + X_2^2}$ | $\Omega$ |
| **Rotor Running Impedance** | $Z_r = \sqrt{R_2^2 + (s X_2)^2}$ | $\Omega$ |
| **Starting Torque** | $T_{st} = \frac{k E_2^2 R_2}{R_2^2 + X_2^2}$ | $\text{N-m}$ |
| **Condition for Max Starting Torque** | $R_2 = X_2$ | Standstill condition |
| **Running Torque** | $T = \frac{k s E_2^2 R_2}{R_2^2 + (s X_2)^2}$ | $\text{N-m}$ |
| **Slip at Maximum Torque** | $s_m = \frac{R_2}{X_2}$ | Fractional slip |
| **Maximum Torque (Pull-out)** | $T_{max} = \frac{k E_2^2}{2 X_2}$ | Independent of $R_2$ |
| **Full Load to Max Torque Ratio** | $\frac{T_f}{T_{max}} = \frac{2 a s_f}{a^2 + s_f^2}$ | where $a = R_2 / X_2$ |
| **Starting to Max Torque Ratio** | $\frac{T_{st}}{T_{max}} = \frac{2 a}{1 + a^2}$ | where $a = R_2 / X_2$ |
| **Power Ratio Triangle** | $P_2 : P_{cr} : P_m = 1 : s : (1 - s)$ | Fundamental relation |
| **Rotor Copper Loss** | $P_{cr} = s P_2 = 3 I_2^2 R_2$ | $\text{Watts}$ |
| **Gross Mechanical Power** | $P_m = (1 - s) P_2 = 3 I_2^2 R_2 \left(\frac{1-s}{s}\right)$ | $\text{Watts}$ |
| **Gross Torque in Sync. Watts** | $T_g = P_2 = \frac{P_m}{1 - s}$ | $\text{synchronous watts}$ |
| **Gross Torque in N-m** | $T_g = \frac{9.55 P_2}{N_s} = \frac{9.55 P_m}{N}$ | $\text{N-m}$ |
| **Electrical Load Resistance** | $R_L = R_2 \left(\frac{1}{s} - 1\right)$ | $\Omega/\text{phase}$ |
| **Max Power Output Condition** | $R_L = Z_{01} = \sqrt{R_{01}^2 + X_{01}^2}$ | Equivalent circuit |
| **Slip at Max Power Output** | $s = \frac{R_2}{R_2 + Z_{01}}$ | Output power condition |
| **Maximum Gross Power Output** | $P_{g\text{ max}} = \frac{3 V_1^2}{2 (R_{01} + Z_{01})}$ | $\text{Watts}$ |
| **LIM Synchronous Speed** | $v_s = 2 w f$ | $\text{m/s}$ ($w = \text{pole pitch}$) |
| **LIM Thrust** | $F = \frac{P_2}{v_s}$ | $\text{Newtons (N)}$ |

---

## 🖼️ Diagram Directory Reference

All diagrams are cropped from vector elements at high resolution (150 DPI) and stored locally under `diagrams/`:

* **Part 1:** `Ch-34_p01_maglev.jpg`, `Ch-34_p02_motor.jpg`, `Ch-34_p02_fig01.jpg` to `Ch-34_p12_fig16.jpg` (20 images)
* **Part 2:** `Ch-34_p14_fig17.jpg` to `Ch-34_p34_fig32.jpg` (15 images)
* **Part 3:** `Ch-34_p36_slip_curve.jpg`, `Ch-34_p36_fig33_34.jpg` to `Ch-34_p47_fig40.jpg` (9 images)
* **Part 4:** `Ch-34_p54_fig41.jpg` to `Ch-34_p66_fig59.jpg` + `Ch-34_p55_maglev_photo.jpg` (20 images)

**Total Visual Artifacts Digitized:** 64 high-fidelity diagrams & figures.
