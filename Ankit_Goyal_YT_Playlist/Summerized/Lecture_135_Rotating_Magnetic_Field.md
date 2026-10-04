---
title: "Rotating Magnetic Field | L 37 | Electrical Machines | GATE 2022 | Ankit Sir"
lecture: 135
topic: "Induction Machines"
duration: "00:55:58"
source: "https://www.youtube.com/watch?v=IwTwlQdb3ME"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 134: Inverted Induction Motor](Lecture_134_Inverted_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 136: Equivalent Circuit 1 →](Lecture_136_Equivalent_Circuit_1.md)

---

# Rotating Magnetic Field | L 37 | Electrical Machines | GATE 2022 | Ankit Sir

- **Source**: https://www.youtube.com/watch?v=IwTwlQdb3ME
- **Duration**: 00:55:58
- **Compiled**: 2026-09-23

---

## Overview

This lecture presents a problem-solving session focused on induction machine construction and rotating magnetic field kinematics. It covers operating slips across motoring, generating, and plugging regimes, along with forward and backward slip relationships in single-phase machines. The discussion works through conditions required to develop steady electromagnetic torque in doubly fed and mechanically coupled machine configurations. Finally, it analyzes resultant air-gap MMF magnitudes and the operation of rotor-fed inverted induction motors.

## Contents

- [[#Slip Value Interpretations|Slip Value Interpretations]]
- [[#Single-Phase Motor Slips|Single-Phase Motor Slips]]
- [[#Steady Torque Conditions (Doubly Fed Motor)|Steady Torque Conditions (Doubly Fed Motor)]]
- [[#Resultant Air-Gap MMF|Resultant Air-Gap MMF]]
- [[#Speed Units (Mechanical vs. Electrical Radians)|Speed Units (Mechanical vs. Electrical Radians)]]
- [[#Mechanically Coupled Machines Power Flow|Mechanically Coupled Machines Power Flow]]

---

## Slip Value Interpretations
_(00:02 - 09:51)_

The operating slip is defined as $s = \frac{N_s - N_r}{N_s}$, which dictates the physical operating region:
- **$0 < s < 1$ (Motoring)**: Rotor rotates in the same direction as the stator field, but slower ($0 < N_r < N_s$).
- **$s < 0$ (Generating)**: Rotor is driven faster than synchronous speed in the same direction ($N_r > N_s$).
- **$s > 1$ (Plugging / Reverse Rotation)**: Rotor rotates in the opposite direction to the stator field ($N_r < 0$).

> [!example] Problem
> The slip of an induction motor is 1.5. Describe the state of the rotor.
> **Solution**: $N_r = N_s(1 - s) = N_s(1 - 1.5) = -0.5 N_s$. 
> The rotor rotates in the opposite direction at half the synchronous speed.

## Single-Phase Motor Slips
_(09:52 - 14:33, 49:19 - 55:56)_

By double revolving field theory, a single-phase stator produces two counter-rotating magnetic fields.
- **Forward Slip ($s_f$)**: Slip relative to the field rotating in the same direction as the rotor ($s_f = s$).
- **Backward Slip ($s_b$)**: Slip relative to the field rotating in the opposite direction.
- **Core Formula**: $s_b = 2 - s_f$

> [!example] Problem
> A 4-pole, 60 Hz induction motor operates at a forward slip of 5%. What is the backward slip?
> **Solution**: $s_b = 2 - 0.05 = 1.95$. (195%).

## Steady Torque Conditions (Doubly Fed Motor)
_(14:44 - 19:48)_

For any AC machine to produce steady, unidirectional torque, its stator and rotor magnetic fields must rotate at the exact same speed in space.

> [!example] Problem
> A 3-phase, 4-pole slip ring induction motor receives a 50 Hz supply on its stator. A 10 Hz voltage (same phase sequence) is fed to its rotor. At what rotor speed will it produce steady torque?
> **Solution**: 
> 1. Stator field speed in space: $N_s = 120(50)/4 = 1500 \text{ rpm}$.
> 2. Rotor field speed w.r.t rotor: $N_{\text{field w.r.t rotor}} = 120(10)/4 = 300 \text{ rpm}$.
> 3. Rotor field speed in space: $N_r + 300$.
> 4. For steady torque, equate the space speeds: $N_r + 300 = 1500 \implies N_r = 1200 \text{ rpm}$.

## Resultant Air-Gap MMF
_(19:49 - 24:38)_

In a balanced 3-phase winding, three pulsating MMFs combine to produce a single revolving field of constant magnitude.
- The peak amplitude of the resultant air-gap rotating MMF wave is: **$F_{\text{net}} = \frac{3}{2} F_m = \frac{3}{2} N_{\text{ph}} I_m$**
  (where $I_m = \sqrt{2} I_{\text{rms}}$ is the peak phase current).

## Speed Units (Mechanical vs. Electrical Radians)
_(24:41 - 29:32)_

Be extremely careful with speed units in examinations:
- **Synchronous RPM**: $N_s = \frac{120 f}{P}$
- **Mechanical Angular Speed ($\text{rad/s}$)**: $\omega_m = \frac{2\pi N_s}{60}$ (Depends on pole count).
- **Electrical Angular Speed ($\text{rad/s}$)**: $\omega_e = 2\pi f$ (Independent of pole count).

## Mechanically Coupled Machines Power Flow
_(44:21 - 49:19)_

When two machines are mechanically coupled on the same shaft, they are locked to the same mechanical speed ($N_r$). Power flow depends on which machine operates above its synchronous speed.

> [!example] Problem
> A 4-pole, 40 Hz induction machine is coupled to a 4-pole, 50 Hz synchronous machine. Determine the operating mode.
> **Solution**:
> 1. The synchronous machine dictates the shaft speed: $N_r = N_{\text{sync}} = \frac{120 \times 50}{4} = 1500 \text{ rpm}$.
> 2. The synchronous machine draws power from the 50 Hz grid and acts as a **Motor**.
> 3. The natural synchronous speed of the induction machine is: $N_{s,\text{IM}} = \frac{120 \times 40}{4} = 1200 \text{ rpm}$.
> 4. Since the shaft drives the induction machine at 1500 rpm ($N_r > N_{s,\text{IM}}$), it operates as an **Induction Generator** (negative slip).
> 5. **Power Flow**: 50 Hz grid $\to$ Sync Motor $\to$ Mechanical Shaft $\to$ Induction Generator $\to$ 40 Hz grid.

---

## Summary and Key Takeaways

- Operating slip $s = \frac{N_s - N_r}{N_s}$ classifies machine operation: $0 < s < 1$ for motoring, $s < 0$ for generating, and $s > 1$ for plugging with counter-rotation.
- In single-phase induction machines, the forward slip is $s_f = s$ and the backward slip relative to the reverse revolving field is $s_b = 2 - s_f$.
- Developing steady electromagnetic torque requires that the machine stator and rotor have identical pole counts and that both air-gap magnetic fields rotate at identical speeds in space.
- An induction machine operating as an electromechanical frequency changer delivers slip-ring frequency $f_r = |s| f$ with terminal voltage proportional to $|s|$.
- A balanced three-phase winding excited by peak phase current $I_m$ produces a resultant rotating air-gap MMF wave of constant peak amplitude $F_{\text{net}} = \frac{3}{2} N_{\text{ph}} I_m$.
- Synchronous speed in mechanical radians per second is $\omega_m = \frac{2\pi N_s}{60}$, whereas in electrical radians per second it is $\omega_e = 2\pi f$.
- In a rotor-fed inverted induction motor, the rotor field rotates at $N_s$ relative to the rotor core, the stator induced frequency is $f_s = s f$, and the rotor physically counter-rotates.
- Cogging or magnetic locking occurs when stator slots equal an integral multiple of rotor slots ($S_s = k S_r$), causing teeth alignment into a minimum reluctance path.
- In mechanically coupled machine sets operating at different frequencies, the machine running above its synchronous speed operates as a generator delivering power to its local grid.

---

[← Lec 134: Inverted Induction Motor](Lecture_134_Inverted_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 136: Equivalent Circuit 1 →](Lecture_136_Equivalent_Circuit_1.md)
