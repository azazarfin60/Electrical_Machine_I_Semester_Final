---
title: "Electrical Machines | Lec 97 | Inverted Induction Motor | GATE Electrical Engineering"
lecture: 134
topic: "Induction Machines"
duration: "00:44:05"
source: "https://www.youtube.com/watch?v=C8qkMm6eEaI"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 133: Induction Machine Construction 2](Lecture_133_Induction_Machine_Construction_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 135: Rotating Magnetic Field →](Lecture_135_Rotating_Magnetic_Field.md)

---

# Electrical Machines | Lec 97 | Inverted Induction Motor | GATE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=C8qkMm6eEaI
- **Duration**: 00:44:05
- **Compiled**: 2026-09-23

---

## Overview

This lecture explores the inverted induction motor where three-phase excitation is supplied to the rotor and the stator is short-circuited. It analyzes the relative speeds of the physical structures and magnetic fields using Lenz's law and relative kinematics. The discussion explains why the rotor rotates in reverse relative to its magnetic field. Finally, the lecture derives the operation of a wound-rotor induction machine as an electromechanical frequency changer and solves a dual-speed design problem.

## Contents

- [[#Concept of the Inverted Induction Motor|Concept of the Inverted Induction Motor]]
- [[#Torque and Direction of Rotation|Torque and Direction of Rotation]]
- [[#Relative Speeds and Frequencies|Relative Speeds and Frequencies]]
- [[#The Frequency Changer|The Frequency Changer]]

---

## Concept of the Inverted Induction Motor
_(00:13 - 12:43)_

**Definition**: An **inverted induction motor** (or rotor-fed induction motor) is one where the 3-phase AC supply is fed to the **rotor** winding, while the **stator** winding is short-circuited.
- Because it requires electrical access to the rotor winding, it can **only** be built using a **Slip Ring (Wound Rotor) Induction Motor**. A squirrel cage machine cannot be operated as an inverted induction motor.
- When power is applied to the rotor, the rotor currents produce a Rotating Magnetic Field (RMF) that rotates at synchronous speed ($N_s$) relative to the physical rotor structure.

## Torque and Direction of Rotation
_(12:43 - 17:31)_

**Lenz's Law Application**:
- The rotor RMF sweeps across the stationary stator conductors, inducing EMF and stator currents.
- The interaction tries to drag the stator in the direction of the rotating field. But the stator is bolted to the ground and cannot move.
- By Newton's Third Law (Action-Reaction), the stator exerts an equal and opposite backward torque on the rotor. 
- **Core Rule**: In an inverted induction motor, the rotor rotates in a direction **opposite** to the rotating magnetic field created by its own winding.

**Physical Analogy (The Treadmill)**:
- Imagine sprinting forward on a treadmill at $v = N_s$.
- If the treadmill belt (the rotor core) moves backward at $u = N_r$, your net speed in the room is $N_s - N_r$.
- By rotating backward, the rotor slows down its magnetic field in stationary space, reducing the cutting velocity across the stator conductors to satisfy Lenz's law.

## Relative Speeds and Frequencies
_(17:31 - 35:23)_

**Frequencies**:
- In a normal motor: Stator supplied at $f$, Rotor induced at $f_r = sf$.
- In an inverted motor: Rotor supplied at $f$, Stator induced at $f_s = sf$.

**Relative Speeds in Inverted Motor**:
Let the rotor field rotate forward at $N_s$ relative to the rotor. The rotor mechanically rotates backward at $-N_r$.
1. **Stator Core Speed (w.r.t Ground)**: $0$
2. **Rotor Core Speed (w.r.t Ground)**: $-N_r$
3. **Rotor RMF Speed (w.r.t Ground)**: $N_s + (-N_r) = N_s - N_r = sN_s$
4. **Stator RMF Speed (w.r.t Ground)**: The stator currents alternate at $sf$. They create a stator RMF that rotates at speed $sN_s$ relative to the stator. So, $sN_s$.
5. **Relative Speed between Fields**: $sN_s - sN_s = 0$. Both fields are locked in synchronism, producing steady torque.

## The Frequency Changer
_(35:23 - 43:59)_

A wound-rotor induction motor can act as an electromechanical frequency changer. By mechanically driving the rotor with an external prime mover, we control the slip ($s$) and thus the output frequency at the slip rings ($f_r = |s| f$).

Because frequency cannot be negative physically, an absolute slip magnitude $|s| = f_r/f$ yields two mathematical solutions: $s = +|s|$ and $s = -|s|$.

> [!example] Problem
> A 3-phase, 4-pole, 50 Hz SRIM is used as a frequency changer to supply a 20 Hz load from its rotor. Find the two prime mover speeds.
> **Solution**:
> $N_s = \frac{120 \times 50}{4} = 1500 \text{ rpm}$.
> Required slip magnitude: $|s| = 20/50 = 0.4$.
> Two valid slips: $s_1 = +0.4$ and $s_2 = -0.4$.
> **Speed 1 (Subsynchronous)**: $N_{r1} = N_s(1 - s_1) = 1500(1 - 0.4) = 900 \text{ rpm}$.
> **Speed 2 (Supersynchronous)**: $N_{r2} = N_s(1 - s_2) = 1500(1 + 0.4) = 2100 \text{ rpm}$.
> *Note: The magnitude of the induced rotor voltage ($E_2$) is identical at both speeds since $f_r$ and $\Phi$ are identical.*

---

## Summary and Key Takeaways

- An inverted induction motor supplies three-phase AC power to the rotor through slip rings while the stator winding terminals are closed.
- The configuration requires external rotor connections, so it is physically possible only with a slip-ring (wound-rotor) induction motor.
- In an inverted induction motor, the rotor rotates in a direction opposite to the rotating magnetic field created by the rotor winding.
- The relative speed of the rotor magnetic field relative to the stationary stator is $N_s - N_r = s N_s$.
- The frequency induced in the stationary stator winding is $f_s = s f$, which is the dual of a conventional induction motor.
- Both the stator and rotor magnetic fields rotate synchronously at $s N_s$ relative to the stationary stator, maintaining zero relative speed between them.
- An induction machine operates as an electromechanical frequency changer where slip-ring frequency is continuously regulated by prime mover speed via $f_r = |s| f$.
- For any desired output frequency, two prime mover operating speeds exist: subsynchronous speed $N_{r1} = N_s(1 - |s|)$ and supersynchronous speed $N_{r2} = N_s(1 + |s|)$.

---

[← Lec 133: Induction Machine Construction 2](Lecture_133_Induction_Machine_Construction_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 135: Rotating Magnetic Field →](Lecture_135_Rotating_Magnetic_Field.md)
