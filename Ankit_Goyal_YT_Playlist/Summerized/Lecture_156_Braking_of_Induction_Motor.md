---
title: "Braking of Induction Motor | L 46 | Electrical Machines | GATE 2022 | Ankit Goyal"
lecture: 156
topic: "Induction Machines"
duration: "00:27:06"
source: "https://www.youtube.com/watch?v=0m4pbxc7uwE"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 155: Braking of Induction Motor](Lecture_155_Braking_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 157: High Torque Cage Rotor →](Lecture_157_High_Torque_Cage_Rotor.md)

---

# Braking of Induction Motor | L 46 | Electrical Machines | GATE 2022 | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=0m4pbxc7uwE
- **Duration**: 00:27:06
- **Compiled**: 2026-09-23

---

## Overview

This practice session reviews electrical braking methods for three-phase induction motors through conceptual questions and numerical calculations. It examines industrial selection criteria, comparing regenerative braking, DC dynamic braking, and plugging across hoists, rolling mills, and machine tools. The lecture details the terminal connections and operating slip regions that define each braking mode. It then presents a complete numerical evaluation of load torque, plugging torque, and total retarding torque using induction motor equivalent circuit parameters.

## Contents

- [[#Industrial Braking Applications and Selection|Industrial Braking Applications and Selection]]
- [[#Efficiency and Torque Characteristics|Efficiency and Torque Characteristics]]
- [[#Numerical Analysis of Plugging|Numerical Analysis of Plugging]]

---

## Industrial Braking Applications and Selection
_(00:02 - 09:29)_

Electrical braking techniques are selected based on the specific mechanical demands of the load.

| Braking Method | Triggering Mechanism | Operating Slip | Energy Exchange | Primary Application |
| :--- | :--- | :--- | :--- | :--- |
| **Regenerative Braking** | $N_r > N_s$ | $s = \frac{N_s - N_r}{N_s} < 0$ | Kinetic energy returned to AC supply line | Electric traction, cranes, hoists |
| **Dynamic Braking** | Stator switched from AC to DC | $s_b = -\frac{N_r}{N_{s0}}$ | Kinetic energy dissipated in rotor resistance | Machine tools, printing presses, elevators |
| **Plugging** | Two stator supply lines interchanged | $s_p = 2 - s$ | Kinetic energy + supply energy dissipated as heat | Emergency stops, rapid reversal |

- **Electric Traction & Hoists**: Rely heavily on **regenerative braking**. When lowering a heavy load, gravity drives the motor above synchronous speed. The machine regenerates, acting as a brake while sending energy back to the grid.
- **Machine Tools & Printing Presses**: Favor **dynamic braking** (DC injection). This provides a smooth, controlled deceleration to a precise stop without the risk of reversing rotation (unlike plugging) and without wearing out friction pads.

## Efficiency and Torque Characteristics
_(09:34 - 14:28)_

- **Efficiency**: **Regenerative braking** is the most efficient because it recovers energy. Plugging is the least efficient as it draws massive power from the line only to waste it entirely as $I^2 R$ heat, alongside the dissipated kinetic energy.
- **Braking Torque Magnitude**: **Plugging** develops the highest maximum braking torque. The relative speed between the backwards-rotating field and the forward-spinning rotor is maximized ($N_{\text{rel}} = N_s + N_r$).
- **DC Machine Counterpart**: In DC motors, dynamic braking requires disconnecting the armature from the supply and shorting it through an external resistor. A **separately excited** field is mandatory to ensure flux remains present when the armature is disconnected from the line.

## Numerical Analysis of Plugging
_(15:00 - 27:05)_

When evaluating a plugging scenario mathematically, Newton's second law dictates the deceleration:
$$J \frac{d\omega}{dt} = - (T_{\text{plugging}} + T_L)$$
Since both the load torque and the reversed electromagnetic torque now act in the same direction to retard the motor, they add together.

**Calculation Sequence**:
1. Calculate the initial motoring slip: $s = (N_s - N_r)/N_s$.
2. Calculate the steady-state load torque $T_L$ matching the initial motor torque:
   $$T_L = \frac{3}{\omega_s} \frac{V_1^2 (R_2'/s)}{(R_1 + R_2'/s)^2 + (X_1 + X_2')^2}$$
3. Find the plugging slip: $s_p = 2 - s$.
4. Calculate the plugging torque $T_{\text{plugging}}$ by substituting $s_p$ in place of $s$ in the exact equivalent circuit torque equation.
5. The total instantaneous braking torque acting on the shaft is $T_{\text{braking}} = T_L + T_{\text{plugging}}$.

---

## Summary and Key Takeaways

- Regenerative braking is the most energy-efficient method because it recovers kinetic energy and feeds power back to the AC grid.
- Dynamic braking is preferred in machine tools and printing presses because it decelerates the drive smoothly without reversing shaft rotation.
- Plugging provides the highest instantaneous braking torque by rotating the stator field in reverse at $-N_s$.
- Under DC dynamic braking, the stator magnetic field is stationary ($N_s = 0$), operating the induction motor in the generating quadrant with slip $s_b = -N_r / N_s < 0$.
- In plugging, the operating slip immediately after interchanging two stator supply terminals is $s_p = 2 - s$.
- The total decelerating torque acting on the shaft during plugging is the sum of load torque and electromagnetic plugging torque: $T_{\text{braking}} = T_L + T_{\text{plugging}}$.
- In permanent magnet DC machines, dynamic braking requires an external series resistor to prevent damaging current spikes across the armature.
- Dynamic braking in conventional DC machines is most effective with separately excited field connections to avoid flux collapse upon line disconnection.

---

[← Lec 155: Braking of Induction Motor](Lecture_155_Braking_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 157: High Torque Cage Rotor →](Lecture_157_High_Torque_Cage_Rotor.md)
