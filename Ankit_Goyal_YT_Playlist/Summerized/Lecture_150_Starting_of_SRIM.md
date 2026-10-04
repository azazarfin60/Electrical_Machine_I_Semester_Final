---
title: "Starting of SRIM | L 43 | Electrical Machines | GATE 2022 | Ankit Goyal"
lecture: 150
topic: "Induction Machines"
duration: "00:36:40"
source: "https://www.youtube.com/watch?v=qr2pRtv3hSI"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 149: Starting of SRIM](Lecture_149_Starting_of_SRIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 151: Speed Control of Induction Motor 1 →](Lecture_151_Speed_Control_of_Induction_Motor_1.md)

---

# Starting of SRIM | L 43 | Electrical Machines | GATE 2022 | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=qr2pRtv3hSI
- **Duration**: 00:36:40
- **Compiled**: 2026-09-23

---

## Overview

This lecture provides systematic numerical problem solving on induction motor starting methods for squirrel-cage and slip-ring machines. It covers torque and current scaling under auto-transformer reduced-voltage starting, standstill voltage proportionality, and frequency-dependent reactance variations. The session also addresses induction motor phase sequence reversal and details multi-step rotor resistance starter designs for wound-rotor machines.

## Contents

- [[#Auto-Transformer Starting Calculations|Auto-Transformer Starting Calculations]]
- [[#Voltage and Frequency Scaling at Standstill|Voltage and Frequency Scaling at Standstill]]
- [[#Star-Delta Starting Characteristics|Star-Delta Starting Characteristics]]
- [[#Rotor Resistance Starter Design (Multi-Step)|Rotor Resistance Starter Design (Multi-Step)]]

---

## Auto-Transformer Starting Calculations
_(00:00 - 05:48)_

In auto-transformer starting, the starting torque relates to the direct-on-line torque via the tapping ratio $x$:
$$\frac{T_{\text{st}}}{T_{\text{fl}}} = x^2 \left(\frac{I_{\text{sc}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}}$$

**Example**:
Given $I_{\text{sc}} = 7 I_{\text{fl}}$ and $s_{\text{fl}} = 0.05$. If a starting torque of $1.5 T_{\text{fl}}$ is required, the tapping ratio $x$ is:
$$1.5 = x^2 (7)^2 (0.05) \implies x^2 = \frac{1.5}{2.45} \approx 0.6122 \implies x \approx 0.782 \text{ (or } 78.2\%)$$

Changing the tapping ratio from $x_1$ to $x_2$ scales torque quadratically:
$$\frac{T_2}{T_1} = \left(\frac{x_2}{x_1}\right)^2$$
For example, doubling the tapping from $30\%$ to $60\%$ quadruples the starting torque.

## Voltage and Frequency Scaling at Standstill
_(05:48 - 10:23)_

At standstill ($s = 1$), the machine is equivalent to a blocked-rotor condition.
- **Voltage Scaling**: Since impedance is constant at a fixed frequency, starting current is directly proportional to applied voltage ($I_{\text{st}} \propto V$). 
  Example: Reducing voltage from $415\text{ V}$ to $110\text{ V}$ scales current by $110/415$.
- **Frequency Scaling**: Leakage reactance $X$ is directly proportional to frequency ($X \propto f$). Resistance remains roughly constant. The new standstill impedance must be recalculated as $Z = \sqrt{R^2 + (X_{f_1} \cdot f_2/f_1)^2}$.

## Star-Delta Starting Characteristics
_(10:26 - 20:24)_

- **Phase Sequence Reversal**: Reversing the direction of rotation of a 3-phase induction motor is done by swapping any two supply lines, which changes the rotating magnetic field direction.
- **Current and Torque Reduction**: Starting in star reduces the applied phase voltage by $1/\sqrt{3}$. This causes both the supply line current and the starting torque to drop to exactly **one-third ($1/3$)** of their respective DOL delta values.
- **Function**: Star-delta starters protect the motor from thermal overheating ($I^2Rt$) and limit supply grid voltage sags. However, they do **not** provide smooth acceleration because the transition from star to delta creates an abrupt torque and current transient.

## Rotor Resistance Starter Design (Multi-Step)
_(20:46 - 30:44)_

To design an $n$-section rotor starter for a slip-ring induction motor:
1. Determine the minimum slip $s_m$. It is related to the current limits. Since $I \propto s$ at low slips, if $I_{\max} = 2 I_{\text{fl}}$, then $s_m = 2 s_{\text{fl}}$.
2. Calculate the common ratio $\alpha = s_m^{1/n}$.
3. Calculate the total initial resistance required: $R_1' = r_2/s_m$.
4. Calculate the first external section: $R_1 = R_1'(1 - \alpha)$.
5. Calculate subsequent sections using a geometric progression: $R_k = \alpha^{k-1} R_1$.

**Example Design (5-section starter)**:
Given $r_2 = 0.03\ \Omega$, $s_{\text{fl}} = 0.02$, $I_{\max} = 2 I_{\text{fl}}$, $n = 5$.
1. $s_m = 2(0.02) = 0.04$
2. $\alpha = (0.04)^{1/5} \approx 0.5253$
3. $R_1' = 0.03 / 0.04 = 0.75\ \Omega$
4. $R_1 = 0.75(1 - 0.5253) \approx 0.356\ \Omega$
5. $R_2 = 0.5253 \times 0.356 \approx 0.187\ \Omega$, etc.

---

## Summary and Key Takeaways

- Starting torque in auto-transformer starting scales with the square of the tapping ratio: $T_{\text{st}} = x^2 T_{\text{st, DOL}}$.
- At standstill, slip is unity and mechanical branch resistance is zero, so starting current scales directly with applied stator terminal voltage: $I_{\text{st}} \propto V$.
- Standstill leakage reactance varies directly with supply frequency ($X \propto f$), while winding resistance remains essentially constant.
- Star-delta starting reduces both starting line current drawn from supply and starting torque by a factor of 3 compared to direct switching: $I_{\text{st}} = \frac{1}{3} I_{\text{sc}}$ and $T_{\text{st}} = \frac{1}{3} T_{\text{st, DOL}}$.
- Reversing the direction of rotation of a three-phase induction motor is accomplished by interchanging any two supply line leads to reverse the stator phase sequence.
- In multi-step wound-rotor starters, consecutive switching slips follow a geometric progression with common ratio $\alpha = s_m^{1/n}$.
- Total initial rotor circuit resistance per phase is given by $R_1' = \frac{r_2}{s_m}$, and the individual resistance sections satisfy $R_k = \alpha^{k-1} R_1$.
- Star-delta starters protect against winding overheating and limit utility line disturbances, but they do not provide smooth acceleration due to the abrupt transition at star-to-delta changeover.

---

[← Lec 149: Starting of SRIM](Lecture_149_Starting_of_SRIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 151: Speed Control of Induction Motor 1 →](Lecture_151_Speed_Control_of_Induction_Motor_1.md)
