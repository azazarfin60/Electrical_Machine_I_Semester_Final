---
title: "Speed Control of IM - 1 | L 44 | Electrical Machines | GATE 2022 | Ankit Goyal"
lecture: 153
topic: "Induction Machines"
duration: "00:54:10"
source: "https://www.youtube.com/watch?v=hoKWN0Yx7H8"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 152: Speed Control of Induction Motor 2](Lecture_152_Speed_Control_of_Induction_Motor_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 154: Speed Control of IM 2 →](Lecture_154_Speed_Control_of_IM_2.md)

---

# Speed Control of IM - 1 | L 44 | Electrical Machines | GATE 2022 | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=hoKWN0Yx7H8
- **Duration**: 00:54:10
- **Compiled**: 2026-09-23

---

## Overview

This lecture solves advanced problem scenarios on induction motor speed control, rotor resistance modification, and stator coil reconnections. It examines power flow ratios across air gap, rotor copper loss, and shaft output under constant stator current and variable fan loads. The discussion details inverted induction motor operation where power feeds into the rotor while driving a coupled DC generator. It concludes by calculating minimum terminal voltage limits under supply fluctuations and determining consequent pole configurations when stator coil polarities reverse.

## Contents

- [[#Power Flow and Rotor Resistance Insertion|Power Flow and Rotor Resistance Insertion]]
- [[#Fan Load Analysis|Fan Load Analysis]]
- [[#Inverted Induction Motor Setup|Inverted Induction Motor Setup]]
- [[#Minimum Supply Voltage for Rated Torque|Minimum Supply Voltage for Rated Torque]]
- [[#Consequent Pole Modification|Consequent Pole Modification]]

---

## Power Flow and Rotor Resistance Insertion
_(00:02 - 16:19)_

**Power Flow Proportions**:
$$P_g : P_{cu} : P_{\text{mech}} = 1 : s : (1 - s)$$
Therefore, $P_g = P_{\text{mech}} / (1 - s)$.

**Constant Stator Current Condition**:
When external resistance is added to the rotor circuit but the stator still draws its rated full-load current (with terminal voltage constant), the total rotor impedance magnitude $|Z_2|$ remains unchanged. Since $X_2$ is constant:
$$\frac{R_2}{s_1} = \frac{R_2 + R_{\text{ext}}}{s_2}$$
Because $Z_2$ and $I_1$ are constant, air gap power $P_g$ is constant.
- The new developed mechanical power drops: $P_{m2} = (1 - s_2)P_g$.
- The rotor copper loss increases: $P_{cu} = s_2 P_g$.

## Fan Load Analysis
_(16:24 - 21:13)_

For a fan load ($T_L \propto N^2 \propto (1-s)^2$) and using the low-slip torque approximation ($T \approx \frac{3}{\omega_s} \frac{s V_1^2}{R_{2,\text{total}}}$):
$$\frac{T_2}{T_1} = \frac{s_2}{s_1} \frac{R_2}{R_2 + R_{\text{ext}}} = \left(\frac{1 - s_2}{1 - s_1}\right)^2$$
**Slip Ring Resistance Measurement**: Measuring resistance between any two slip rings at standstill yields $2 R_2$ (since two phases are in series).

## Inverted Induction Motor Setup
_(31:33 - 42:57)_

In an inverted induction motor, the 3-phase supply feeds the rotor instead of the stator.
- The rotor currents establish a rotating magnetic field in the air gap that rotates at synchronous speed $N_s = 120f/P$ **relative to the physical rotor structure**.
- If the rotor turns physically at speed $N$ in space, the absolute speed of the magnetic field in space is determined by whether the field rotates in the same or opposite direction to the rotor's physical motion.
- Power flows from the slip rings, across the air gap to the stator, while mechanical power $(1-s)P_g$ is developed at the shaft. This shaft power can act as the prime mover for a coupled generator (e.g., a DC generator supplying a load).

## Minimum Supply Voltage for Rated Torque
_(42:57 - 47:46)_

If supply voltage drops, the breakdown torque $T_{\text{max}}$ falls because $T_{\text{max}} \propto V^2$.
The minimum voltage at which the motor can still drive its rated full-load torque occurs when $T_{\text{max, new}} = T_{\text{fl}}$.
**Example**: If originally $T_{\text{max}} = 2 T_{\text{fl}}$, the voltage can drop until $T_{\text{max}}$ halves.
$$\left(\frac{V_{\text{min}}}{V_{\text{rated}}}\right)^2 = \frac{1}{2} \implies V_{\text{min}} = \frac{V_{\text{rated}}}{\sqrt{2}} \approx 0.707 V_{\text{rated}}$$
A drop below $70.7\%$ will stall the motor.

## Consequent Pole Modification
_(48:09 - 54:00)_

Magnetic poles form at the junctions between adjacent conductors carrying currents in opposite directions.
By reversing the connections to selected coil groups (changing the current direction through them), the number of such alternating junctions changes.
This consequent pole action alters the active pole count (e.g., from 8 poles down to 4 poles), effectively stepping up the synchronous speed in a 2:1 ratio.

---

## Summary and Key Takeaways

- In an induction motor, power partitions according to the strict ratio $P_g : P_{cu} : P_m = 1 : s : (1 - s)$, allowing developed mechanical power to define air gap power through $P_g = P_m / (1 - s)$.
- When external rotor resistance is inserted while maintaining rated stator current and constant terminal voltage, input impedance magnitude $|Z_2|$ remains constant, forcing $R_2 / s_1 = (R_2 + R_{\text{ext}}) / s_2$.
- Constant air gap power under increased slip diverts developed mechanical power into increased rotor copper loss in direct proportion to slip: $P_{cu} = s P_g$.
- For fan loads where load torque obeys $T_L \propto N^2$, torque equality in the low-slip region gives $s / (R_2 + R_{\text{ext}}) \propto (1 - s)^2$.
- In an inverted induction motor fed from slip rings, the magnetic field rotates at synchronous speed $N_s = 120f / P$ relative to the physical rotor structure.
- Mechanical power developed by an inverted induction motor acts as prime mover input to a coupled generator: $P_m = (1 - s)P_g$.
- The lowest supply voltage capable of delivering rated load without stalling occurs when reduced breakdown torque equals rated torque: $T_{\text{max, new}} = T_{\text{fl}}$.
- Because maximum torque scales as $V^2$, halving the breakdown torque requires terminal voltage to remain at least $V_{\text{min}} = V_{\text{rated}} / \sqrt{2} \approx 0.707 V_{\text{rated}}$.
- Magnetic poles form at junctions where adjacent conductors carry opposite currents, and reversing selected coil groups alters the active pole count through consequent pole action.

---

[← Lec 152: Speed Control of Induction Motor 2](Lecture_152_Speed_Control_of_Induction_Motor_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 154: Speed Control of IM 2 →](Lecture_154_Speed_Control_of_IM_2.md)
