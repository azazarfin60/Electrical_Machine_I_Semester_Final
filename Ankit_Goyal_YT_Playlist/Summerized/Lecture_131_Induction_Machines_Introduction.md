---
title: "Induction Machines Introduction | Electrical Machines | Lec 94 | GATE & ESE | Ankit Goyal"
lecture: 131
topic: "Induction Machines"
duration: "00:49:07"
source: "https://www.youtube.com/watch?v=UqgqYfsL-fs"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 053: Problems based on Harmonics and Inrush Current](Lecture_053_Problems_based_on_Harmonics_and_Inrush_Current.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 132: Induction Machine Construction 1 →](Lecture_132_Induction_Machine_Construction_1.md)

---

# Induction Machines Introduction | Electrical Machines | Lec 94 | GATE & ESE | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=UqgqYfsL-fs
- **Duration**: 00:49:07
- **Compiled**: 2026-09-23

---

## Overview

This lecture introduces the fundamental principles, operational mechanisms, and physical laws governing three-phase induction machines. It establishes the singly excited nature of the induction motor by comparing its stator and rotor to the primary and secondary windings of a transformer. The discussion explains how a rotating stator magnetic field induces rotor currents to generate torque in accordance with Lenz's law. Detailed analyses highlight the role of the air gap in creating high magnetizing current and leakage reactance. Finally, the lecture contrasts squirrel cage and wound-rotor constructions to show how magnetic poles interact across the air gap.

## Contents

- [[#Singly Excited & Asynchronous Nature|Singly Excited & Asynchronous Nature]]
- [[#The Air Gap & Magnetizing Current|The Air Gap & Magnetizing Current]]
- [[#Working Principle & Lenz's Law|Working Principle & Lenz's Law]]
- [[#Torque, Leakage Reactance, and Air Gap Optimization|Torque, Leakage Reactance, and Air Gap Optimization]]
- [[#Pole Adaptation: Squirrel Cage vs Wound Rotor|Pole Adaptation: Squirrel Cage vs Wound Rotor]]
- [[#Absence of Armature Reaction|Absence of Armature Reaction]]

---

## Singly Excited & Asynchronous Nature
_(00:13 - 08:57)_

- **Singly Excited**: Unlike Synchronous or DC machines that require two power sources (stator and rotor), an induction machine receives power ONLY on its stator. The rotor receives its energy purely via mutual induction across the air gap.
- **Asynchronous Operation**: The induction motor can **never** run at synchronous speed ($N_s = 120 f / P$). 
  - If $N_r = N_s$, the relative speed between the rotating magnetic field (RMF) and the rotor conductors becomes zero.
  - Zero relative speed $\implies$ no flux cutting $\implies$ no induced EMF $\implies$ zero rotor current $\implies$ zero torque.
  - Therefore, the rotor must always slip behind the RMF ($N_r < N_s$) to produce driving torque.

## The Air Gap & Magnetizing Current
_(08:57 - 19:09)_

An induction motor is essentially a rotating transformer with an **air gap**. 
- In a transformer, the core is a continuous iron path (high permeability, low reluctance). Thus, magnetizing current is tiny ($3-5\%$ of full load).
- In an induction motor, the flux must cross the air gap (low permeability $\mu_0$, high reluctance).
- **Consequence**: The induction motor draws a massive magnetizing current ($I_\mu \approx 30\% \text{ to } 35\%$ of full load) just to establish the working flux. This results in a very poor no-load power factor ($0.1 \text{ to } 0.2$ lagging).

## Working Principle & Lenz's Law
_(19:10 - 30:57)_

1. **RMF**: A balanced 3-phase supply on the stator produces a Rotating Magnetic Field revolving at $N_s$.
2. **Induction**: This RMF cuts the stationary rotor conductors, inducing an EMF ($e = B l v_{\text{rel}}$).
3. **Current**: Because the rotor circuit is closed (shorted end-rings or external resistance), rotor currents flow.
4. **Torque (Lenz's Law)**: By Lenz's law, the induced effect (torque) opposes the cause (relative speed $N_s - N_r$). To reduce this relative speed, the torque pushes the rotor in the *same direction* as the RMF. The rotor chases the stator field.

## Torque, Leakage Reactance, and Air Gap Optimization
_(30:58 - 36:00)_

The developed electromagnetic torque is given by:
$T = \frac{\pi}{8} P^2 \Phi F_2 \cos\theta_2$
- **Leakage Reactance ($X_2$)**: Flux that crosses the slot openings but doesn't link the other winding forms leakage reactance. This makes the rotor impedance complex ($Z_2 = R_2 + jX_2$), causing rotor current to lag the induced EMF by angle $\theta_2$.
- **Torque Reduction**: This lag $\theta_2$ reduces torque via the internal power factor term $\cos \theta_2$.
- **Air Gap Design Rule**: To maximize torque and minimize magnetizing current, the air gap in an induction motor must be as **small** as mechanically possible. (Contrast this with synchronous machines, where a large air gap is preferred to improve stability limits).

## Pole Adaptation: Squirrel Cage vs Wound Rotor
_(43:28 - 48:59)_

For steady torque, the stator and rotor must have the exact same number of magnetic poles ($P_s = P_r$).
- **Squirrel Cage Rotor**: Consists of uninsulated aluminum/copper bars shorted by end rings. It has no fixed winding layout. When placed in a stator with $P$ poles, the induced currents automatically distribute to form $P$ magnetic poles. **A squirrel cage automatically adapts to any stator pole number.**
- **Wound Rotor (Slip Ring)**: Consists of insulated, distributed 3-phase windings. Its poles are fixed by its physical winding design. **A wound rotor must be specifically manufactured to match the stator pole count.** If placed in a mismatched stator, net torque is zero.

## Absence of Armature Reaction
_(36:01 - 43:28)_

In DC and synchronous machines, armature reaction occurs when the load-carrying (armature) flux distorts the main (field) flux.
- **In an Induction Motor**: There is no "armature reaction". 
- The stator acts as both the primary (field provider) and the load carrier. Just like a transformer, any demagnetizing current drawn by the rotor ($I_2$) is immediately counterbalanced by the stator drawing an extra component of current ($I_1'$) from the supply. The main air gap flux remains strictly constant.

---

## Summary and Key Takeaways

- An induction machine is a singly excited AC machine where only the stator connects to a power source, while the rotor receives all its working energy through mutual induction across the air gap.
- An induction motor cannot operate at synchronous speed $N_s = 120 f / P$ because relative motion between the rotating stator field and the rotor conductors would vanish, reducing induced EMF, rotor current, and driving torque to zero.
- The composite magnetic circuit includes an air gap that sharply increases total reluctance, requiring a magnetizing current of $I_\mu \approx (0.30\text{ to }0.35) I_{\text{FL}}$, which cannot be neglected during equivalent circuit analysis.
- An induction machine operates as a variable frequency device where the rotor electrical frequency depends on slip according to $f_r = s f$.
- Rotor leakage reactance $X_2$ causes the rotor current to lag the induced EMF by an angle $\theta_2 = \arctan(X_2 / R_2)$, which reduces developed torque according to $T = \frac{\pi}{8} P^2 \Phi F_2 \cos\theta_2$.
- A small physical air gap is preferred in induction motors to minimize leakage reactance and magnetizing current, unlike synchronous machines where a large air gap improves steady-state power limits and stability.
- Armature reaction does not exist in an induction machine because the stator winding simultaneously produces the mutual flux and carries the load-balancing current.
- A squirrel cage rotor automatically induces the exact number of magnetic poles present on the stator ($P_r = P_s$), whereas a wound rotor must be manufactured with matching pole numbers by design.

---

[← Lec 053: Problems based on Harmonics and Inrush Current](Lecture_053_Problems_based_on_Harmonics_and_Inrush_Current.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 132: Induction Machine Construction 1 →](Lecture_132_Induction_Machine_Construction_1.md)
