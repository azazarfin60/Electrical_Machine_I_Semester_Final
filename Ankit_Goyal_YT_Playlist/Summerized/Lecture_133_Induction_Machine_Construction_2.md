---
title: "Electrical Machines | Lec 96 | Induction Machine Construction - 2 | GATE Electrical Engineering"
lecture: 133
topic: "Induction Machines"
duration: "00:44:05"
source: "https://www.youtube.com/watch?v=J3BjnWsuUL8"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 132: Induction Machine Construction 1](Lecture_132_Induction_Machine_Construction_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 134: Inverted Induction Motor →](Lecture_134_Inverted_Induction_Motor.md)

---

# Electrical Machines | Lec 96 | Induction Machine Construction - 2 | GATE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=J3BjnWsuUL8
- **Duration**: 00:44:05
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines the construction, circuit arrangement, and relative kinematics of wound rotor induction machines. It establishes how rotor phase counts are determined from slot layouts and details the role of slip rings, carbon brushes, and external variable resistors. The discussion compares squirrel cage and slip ring machines across maintenance, starting torque, and industrial drive load categories. Finally, the lecture derives the slip frequency formula and proves that both stator and rotor magnetic fields rotate in synchronism at synchronous speed relative to the stationary stator.

## Contents

- [[#Wound Rotor Construction and External Resistance|Wound Rotor Construction and External Resistance]]
- [[#Comparison: SCIM vs SRIM|Comparison: SCIM vs SRIM]]
- [[#Industrial Mechanical Loads|Industrial Mechanical Loads]]
- [[#Rotor Frequency and Slip|Rotor Frequency and Slip]]
- [[#Relative Speeds and Magnetic Field Synchronization|Relative Speeds and Magnetic Field Synchronization]]

---

## Wound Rotor Construction and External Resistance
_(00:13 - 14:29)_

**Construction Principles**:
Unlike a squirrel cage, a wound rotor carries insulated copper coils.
1. The rotor carries a balanced 3-phase distributed winding.
2. The winding is always connected in star.
3. The winding must be designed for the exact same number of poles as the stator ($P_r = P_s$).
4. The three open star terminals connect to three phosphor-bronze slip rings mounted on the shaft.

**Function of External Resistance ($R_{\text{ext}}$)**:
Carbon brushes press against the slip rings, connecting the rotor circuit to a 3-phase external variable resistor bank. Adding $R_{\text{ext}}$ provides four benefits:
1. **Limits Starting Current**: Increases total impedance to limit inrush current.
2. **Increases Starting Torque**: Starting torque is proportional to $(R_2 + R_{\text{ext}})$.
3. **Improves Starting Power Factor**: Increases $\cos\theta_2$.
4. **Speed Control**: Allows varying the running speed by introducing slip loss.

## Comparison: SCIM vs SRIM
_(14:34 - 20:29)_

| Parameter | Squirrel Cage (SCIM) | Slip Ring (SRIM) |
| :--- | :--- | :--- |
| **Rotor Winding** | Solid uninsulated bars | Insulated phase-wound coils |
| **Mechanical Ruggedness** | Extremely rugged (no brushes) | Less rugged |
| **Maintenance** | Almost zero maintenance | Regular brush/ring replacement |
| **Air Gap** | Smaller | Larger (due to coil overhangs) |
| **Starting Current** | High | Low (limited by $R_{\text{ext}}$) |
| **Starting Torque** | Low | High (boosted by $R_{\text{ext}}$) |
| **Running Performance**| Superior efficiency & PF | Good |

## Industrial Mechanical Loads
_(20:29 - 24:48)_

Drives are selected based on the load torque ($T_L$) profile versus speed ($N$):
1. **Inverse Load ($T_L \propto 1/N$)**: High torque at low speed (Cranes, elevators, electric traction). Often require SRIMs.
2. **Constant Torque ($T_L = \text{constant}$)**: Paper mills, lathes.
3. **Parabolic Load ($T_L \propto N^2$)**: Fans, blowers, centrifugal pumps. Start easily since $T_L \approx 0$ at $N=0$. Ideal for SCIMs.

## Rotor Frequency and Slip
_(24:50 - 35:00)_

The rotor slips behind the synchronous speed ($N_s$).
- **Slip ($s$)**: $s = \frac{N_s - N_r}{N_s}$
- **Relative Speed**: The stator field sweeps past the rotor at a relative speed of $(N_s - N_r) = sN_s$.
- **Rotor Frequency ($f_r$)**: The electrical frequency of the induced rotor EMF is proportional to this relative speed:
  $f_r = \frac{P}{120}(N_s - N_r) = s f$
  Since operating slip is typically 2-5%, the running rotor frequency is very low (e.g., $1-2.5\text{ Hz}$ on a $50\text{ Hz}$ supply). Therefore, rotor core losses are negligible during running conditions.

## Relative Speeds and Magnetic Field Synchronization
_(35:01 - 43:57)_

For any machine to produce steady, unidirectional torque, its stator and rotor magnetic fields must be stationary relative to each other (i.e., locked in synchronism).
- **Stator RMF Speed w.r.t Stator**: $N_s$ (from the supply).
- **Rotor Speed w.r.t Stator**: $N_r$ (mechanical rotation).
- **Rotor RMF Speed w.r.t Rotor**: The rotor currents alternate at frequency $f_r$. This creates a rotating magnetic field moving at speed $\frac{120 f_r}{P} = \frac{120(sf)}{P} = sN_s$ relative to the rotor itself.
- **Rotor RMF Speed w.r.t Stator**: By relative motion (Runner on a Train): 
  $\text{Total Speed} = \text{Mechanical Speed} + \text{Field Speed w.r.t Structure}$
  $N_{\text{RMF,rotor w.r.t stator}} = N_r + sN_s = N_r + (N_s - N_r) = N_s$.

**Conclusion**: Both the stator magnetic field and the rotor magnetic field rotate at $N_s$ relative to the stationary ground. They are locked together at zero relative speed, ensuring steady electromagnetic torque.

---

## Summary and Key Takeaways

- A wound rotor carries an insulated distributed winding that must be wound for the exact number of stator poles and connected in star.
- Phosphor bronze slip rings and carbon brushes connect an external 3-phase rheostat in series with the rotor winding to limit starting current, improve starting torque, and provide speed control.
- Squirrel cage motors offer superior mechanical ruggedness and lower maintenance, whereas slip ring motors provide high starting torque under heavy mechanical loads.
- Mechanical loads categorize into inverse loads ($T_L \propto \frac{1}{N}$), constant torque loads ($T_L = \text{const}$), and parabolic loads ($T_L \propto N^2$).
- Slip $s = \frac{N_s - N_r}{N_s}$ measures the per-unit relative speed between the rotating magnetic field and the mechanical rotor.
- The frequency of EMF and current induced in the rotor winding equals slip frequency, derived as $f_r = \frac{P}{120}(N_s - N_r) = s f$.
- The rotor rotating magnetic field moves at speed $s N_s$ relative to the rotor core and at speed $N_s$ relative to the stationary stator.
- Steady electromagnetic torque requires both stator and rotor magnetic fields to be stationary relative to each other in space.

---

[← Lec 132: Induction Machine Construction 1](Lecture_132_Induction_Machine_Construction_1.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 134: Inverted Induction Motor →](Lecture_134_Inverted_Induction_Motor.md)
