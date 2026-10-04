---
title: "Braking of Induction Motor | Electrical Machines | Lec 109 | GATE & ESE (EE, ECE) | Ankit Goyal"
lecture: 155
topic: "Induction Machines"
duration: "00:27:37"
source: "https://www.youtube.com/watch?v=f-RBM0txOdc"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 154: Speed Control of IM 2](Lecture_154_Speed_Control_of_IM_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 156: Braking of Induction Motor →](Lecture_156_Braking_of_Induction_Motor.md)

---

# Braking of Induction Motor | Electrical Machines | Lec 109 | GATE & ESE (EE, ECE) | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=f-RBM0txOdc
- **Duration**: 00:27:37
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines electrical braking methods for three-phase induction motors. It focuses on the operating principles and mathematical relationships of regenerative braking, dynamic braking, and plugging. The discussion details how stationary DC excitation produces a stationary stator field to achieve smooth dynamic retardation. It then derives the reverse torque and altered slip relationships that govern rapid deceleration during plugging. Finally, the lecture analyzes how frequency-dependent rotor skin effect influences starting performance and introduces pull-up torque.

## Contents

- [[#Regenerative Braking|Regenerative Braking]]
- [[#Dynamic Braking (DC Injection)|Dynamic Braking (DC Injection)]]
- [[#Plugging (Reverse Current Braking)|Plugging (Reverse Current Braking)]]
- [[#Skin Effect and Pull-Up Torque|Skin Effect and Pull-Up Torque]]

---

## Regenerative Braking
_(00:13 - 07:11)_

Occurs when the motor transitions into generator action, meaning rotor speed $N_r$ becomes greater than synchronous speed $N_s$.
- **Mechanism**: Instead of speeding up the physical rotor, synchronous speed $N_s$ is abruptly reduced (e.g. by doubling stator poles or lowering VFD supply frequency). 
- **Slip**: Becomes negative ($s < 0$).
- **Action**: Kinetic energy from the rotating mass is converted into electrical energy and fed back to the supply mains, decelerating the shaft.
- **Constraint**: To prevent the motor from settling at the new lower synchronous speed, the supply must be disconnected just before $N_r$ drops to the new $N_s$.

## Dynamic Braking (DC Injection)
_(07:11 - 12:12)_

- **Mechanism**: The 3-phase AC supply is disconnected, and a DC source is injected across two or more stator terminals.
- **Stationary Field**: The DC current sets up a non-rotating, stationary magnetic field in space ($N_s = 0\text{ rpm}$). The net MMF magnitude is $1.5 NI$ fixed along a specific axis.
- **Slip**: $s_b = \frac{0 - N_r}{N_{s0}} = -\frac{N_r}{N_{s0}}$.
- **Action**: By Lenz's law, as the spinning rotor conductors cut the stationary field, induced currents produce a counter-torque to oppose relative motion. The motor decelerates smoothly to rest without risk of reversing rotation.

## Plugging (Reverse Current Braking)
_(12:22 - 22:50)_

Plugging is the fastest and most severe electrical braking method.
- **Mechanism**: Any two stator supply leads are interchanged. This reverses the phase sequence, causing the stator rotating magnetic field to abruptly reverse direction (from $+N_s$ to $-N_s$).
- **Slip**: The new relative slip is:
  $$s_p = \frac{(-N_s) - N_r}{-N_s} = \frac{N_s + N_r}{N_s} = 1 + \frac{N_r}{N_s}$$
  Since $N_r/N_s = 1 - s$ (from normal motoring), the plugging slip is $s_p = 2 - s$. For a motor running near synchronous speed ($s \approx 0$), the initial plugging slip is $s_p \approx 2$.
- **Braking Torque**: Electromagnetic torque reverses direction. The net decelerating torque is the sum of the plugging torque and the load torque:
  $$J \frac{d\omega}{dt} = - (T_{\text{plugging}} + T_L)$$
- **Constraint**: The supply MUST be disconnected exactly at zero speed; otherwise, the motor will accelerate in the reverse direction.

## Skin Effect and Pull-Up Torque
_(23:17 - 27:29)_

- **Skin Effect at Start**: At standstill ($s = 1$), rotor frequency equals supply frequency ($50\text{ Hz}$). The high frequency causes rotor currents to crowd near the conductor surface (skin effect), significantly increasing the effective AC rotor resistance ($R_2$) and thereby boosting starting torque.
- **Pull-Up Torque**: As the rotor accelerates, slip drops rapidly. The decreasing rotor frequency reduces the skin effect, lowering $R_2$ back toward its DC value. This temporary drop in resistance can cause a brief dip in developed torque before the standard low-slip characteristic takes over. The minimum torque reached during this dip is called the **pull-up torque**.

---

## Summary and Key Takeaways

- Electrical braking converts rotating mechanical kinetic energy into electrical energy without wearing mechanical brake shoes.
- Regenerative braking occurs when rotor speed exceeds synchronous speed ($N_r > N_s$), producing negative slip and returning electric power to the AC supply.
- In dynamic braking, the AC line is disconnected and DC current is injected across the stator terminals, setting up a stationary magnetic field of magnitude $1.5 N I$.
- The effective operating slip during dynamic braking is negative ($s_b = -N_r / N_{s0}$), producing a counter-torque that brings the rotor to rest without reversal.
- Plugging is initiated by swapping two stator supply lines, reversing the rotating field to synchronous speed $-N_s$.
- The operating slip at the start of plugging from near-synchronous forward speed is $s_p = 2 - s \approx 2$.
- The total decelerating torque during plugging equals the sum of the electromagnetic plugging torque and the mechanical load torque: $T_{\text{braking}} = T_{\text{plugging}} + T_L$.
- Skin effect at line frequency raises effective rotor resistance at stand-still, boosting starting torque.
- Diminishing skin effect as the rotor accelerates creates a temporary dip in torque known as pull-up torque before reaching breakdown torque.

---

[← Lec 154: Speed Control of IM 2](Lecture_154_Speed_Control_of_IM_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 156: Braking of Induction Motor →](Lecture_156_Braking_of_Induction_Motor.md)
