---
title: "Starting of SCIM | Electrical Machines | Lec 105 | GATE/ESE (EE, ECE) | Ankit Goyal"
lecture: 147
topic: "Induction Machines"
duration: "00:50:16"
source: "https://www.youtube.com/watch?v=DlXAh9B10hI"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 146: Circle Diagram of Induction Motor](Lecture_146_Circle_Diagram_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 148: Starting of SCIM →](Lecture_148_Starting_of_SCIM.md)

---

# Starting of SCIM | Electrical Machines | Lec 105 | GATE/ESE (EE, ECE) | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=DlXAh9B10hI
- **Duration**: 00:50:16
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines starting methods for three-phase squirrel-cage induction motors. It explains why high standstill currents occur when the fictitious mechanical load resistance drops to zero at unity slip. The discussion evaluates Direct-On-Line starting alongside reduced-voltage techniques, including stator impedance, auto-transformer, and star-delta starters. Quantitative comparisons demonstrate the impact of voltage scaling on stator winding currents, line currents, and developed starting torque.

## Contents

- [[#The Starting Problem & DOL|The Starting Problem & DOL]]
- [[#Stator Impedance Starting|Stator Impedance Starting]]
- [[#Auto-Transformer Starting|Auto-Transformer Starting]]
- [[#Star-Delta Starting & Switching Transients|Star-Delta Starting & Switching Transients]]
- [[#Master Comparison of Starting Methods|Master Comparison of Starting Methods]]

---

## The Starting Problem & DOL
_(00:13 - 17:50)_

At standstill ($N_r = 0, s = 1$), the mechanical load resistance $R'_2(1/s - 1)$ becomes zero. The motor circuit is essentially a short circuit containing only the small winding impedances. 
This results in a very high starting current ($I_{\text{sc}} = 5 \text{ to } 8 \times I_{\text{fl}}$). Small motors can handle this due to rapid acceleration, but large motors require starting methods to limit thermal stress.

**Direct-On-Line (DOL) Starting**:
Rated voltage is applied directly. 
- Starting Current: $I_{\text{st}} = I_{\text{sc}}$
- The fundamental torque ratio is derived from $T \propto I_1^2 / s$:
  > [!success] DOL Torque Ratio
  > $$\left(\frac{T_{\text{st}}}{T_{\text{fl}}}\right)_{\text{DOL}} = \left(\frac{I_{\text{sc}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}}$$

## Stator Impedance Starting
_(17:53 - 22:50)_

A reactor (or resistor) in series with the stator reduces the terminal voltage by a fraction $x$ ($x < 1$).
- **Supply / Motor Current**: Reduces linearly. $I_{\text{st}} = x I_{\text{sc}}$
- **Starting Torque**: Reduces quadratically ($T \propto V_1^2$). 
  $$\frac{T_{\text{st}}}{T_{\text{fl}}} = x^2 \left(\frac{I_{\text{sc}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}} = x^2 \left(\frac{T_{\text{st}}}{T_{\text{fl}}}\right)_{\text{DOL}}$$
*Drawback*: Current drops by $x$, but torque drops much worse by $x^2$.

## Auto-Transformer Starting
_(22:53 - 32:39)_

An auto-transformer with a tapping ratio $x$ steps down the voltage to the motor.
- **Motor Current**: The current in the windings is $x I_{\text{sc}}$.
- **Supply Line Current**: Because of transformer action ($V_1 I_{\text{supply}} = V_2 I_{\text{motor}}$), the current drawn from the grid is further reduced by $x$.
  $$I_{\text{supply}} = x (x I_{\text{sc}}) = x^2 I_{\text{sc}}$$
- **Starting Torque**: Depends on the current in the motor winding ($x I_{\text{sc}}$), so it reduces by $x^2$.
  $$\frac{T_{\text{st}}}{T_{\text{fl}}} = x^2 \left(\frac{T_{\text{st}}}{T_{\text{fl}}}\right)_{\text{DOL}}$$
*Advantage*: Both supply current and starting torque decrease by the exact same proportion ($x^2$).

## Star-Delta Starting & Switching Transients
_(32:49 - 47:48)_

For motors designed to run in delta, starting them in star reduces the per-phase voltage by a factor of $1/\sqrt{3}$.
- **Phase Current**: $I_{\text{st, ph}} = I_{\text{sc}} / \sqrt{3}$.
- **Supply Line Current**: In star, line current equals phase current. Compared to DOL delta (where $I_{\text{line, delta}} = \sqrt{3} I_{\text{sc}}$):
  > [!success] Line Current Reduction
  > $$\frac{I_{\text{line, star}}}{I_{\text{line, delta}}} = \frac{1}{3}$$
- **Starting Torque**: Proportional to phase voltage squared, so it also reduces to $1/3$ of the DOL delta value.

**Closed-Transition Switching**:
Standard star-delta starters disconnect the motor during transition. The trapped rotor flux generates a back-EMF that causes severe inrush transients when reconnected in delta. *Closed-transition* starters use parallel resistors to maintain the supply connection during switching, preventing these surges.

## Master Comparison of Starting Methods
_(47:48 - 50:09)_

| Starting Method | Motor Winding Current ($I_{\text{st, motor}}$) | Supply Line Current ($I_{\text{supply}}$) | Starting Torque Ratio ($\frac{T_{\text{st}}}{T_{\text{fl}}}$) | Torque Scaling vs DOL |
| :--- | :--- | :--- | :--- | :--- |
| **Direct-On-Line (DOL)** | $I_{\text{sc}}$ | $I_{\text{sc}}$ | $\left(\frac{I_{\text{sc}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}}$ | $1$ |
| **Stator Reactor** | $x I_{\text{sc}}$ | $x I_{\text{sc}}$ | $x^2 \left(\frac{I_{\text{sc}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}}$ | $x^2$ |
| **Auto-transformer** | $x I_{\text{sc}}$ | $x^2 I_{\text{sc}}$ | $x^2 \left(\frac{I_{\text{sc}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}}$ | $x^2$ |
| **Star-Delta** | $\frac{I_{\text{sc}}}{\sqrt{3}}$ | $\frac{I_{\text{sc}}}{\sqrt{3}}$ | $\frac{1}{3} \left(\frac{I_{\text{sc}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}}$ | $\frac{1}{3}$ |

---

## Summary and Key Takeaways

- At standstill ($s = 1$), the mechanical load equivalent resistance $R'_2\left(\frac{1}{s}-1\right)$ is zero, leaving only winding impedance to limit the starting current.
- Small induction motors ($< 5\text{ HP}$) can start Direct-On-Line because low rotational inertia allows rapid acceleration before thermal damage occurs.
- The general torque ratio equation relates starting torque to full-load torque as $\frac{T_{\text{st}}}{T_{\text{fl}}} = \left(\frac{I_{\text{st}}}{I_{\text{fl}}}\right)^2 s_{\text{fl}}$.
- Under Direct-On-Line starting at rated line voltage, starting current equals short-circuit current: $I_{\text{st}} = I_{\text{sc}} = \frac{V_1}{Z_{\text{sc}}}$.
- In stator reactor starting with voltage scaling factor $x$, supply current drops by $x$ while starting torque drops by $x^2$.
- In auto-transformer starting with transformation ratio $x$, both supply line current and developed starting torque reduce by factor $x^2$.
- In star-delta starting, phase voltage drops by $\frac{1}{\sqrt{3}}$, reducing both supply line current and starting torque to $\frac{1}{3}$ of their delta DOL values.
- Closed-transition star-delta starters use parallel transition resistors to maintain uninterrupted supply connections, preventing trapped rotor flux from inducing severe switching transients.

---

[← Lec 146: Circle Diagram of Induction Motor](Lecture_146_Circle_Diagram_of_Induction_Motor.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 148: Starting of SCIM →](Lecture_148_Starting_of_SCIM.md)
