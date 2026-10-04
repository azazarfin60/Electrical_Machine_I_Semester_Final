---
title: "Starting of SCIM | L 42 | Electrical Machines | GATE 2022 | Ankit Goyal"
lecture: 148
topic: "Induction Machines"
duration: "01:02:50"
source: "https://www.youtube.com/watch?v=J_FVNSGokD4"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 147: Starting of SCIM](Lecture_147_Starting_of_SCIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 149: Starting of SRIM →](Lecture_149_Starting_of_SRIM.md)

---

# Starting of SCIM | L 42 | Electrical Machines | GATE 2022 | Ankit Goyal

- **Source**: https://www.youtube.com/watch?v=J_FVNSGokD4
- **Duration**: 01:02:50
- **Compiled**: 2026-09-23

---

## Overview

This lecture presents comprehensive numerical problem solving on starting squirrel-cage and wound-rotor induction motors. It analyzes conditions required to develop maximum torque right at standstill through rotor resistance and frequency adjustments. The session examines how feeder line impedance impacts star versus delta starting methods. It also evaluates performance scaling under varying supply frequencies and reduced voltage starters.

## Contents

- [[#Maximum Torque at Starting|Maximum Torque at Starting]]
- [[#Feeder Impedance in Star vs Delta Starting|Feeder Impedance in Star vs Delta Starting]]
- [[#Frequency Scaling of Starting Parameters|Frequency Scaling of Starting Parameters]]
- [[#Reduced Voltage Starting Analysis|Reduced Voltage Starting Analysis]]
- [[#Constant V/f Starting & Stability Limit|Constant V/f Starting & Stability Limit]]

---

## Maximum Torque at Starting
_(00:03 - 10:18)_

Maximum torque develops when the rotor resistance equals the rotor leakage reactance, occurring at slip $s_{mT} = R_2 / X_2$. 
To develop maximum torque exactly at starting, the slip at maximum torque must be unity ($s_{mT} = 1$). 

**Condition**:
$$R_2 + R_{\text{ext}} = X_2$$

Where $R_{\text{ext}}$ is the external rotor resistance that must be inserted (applicable to wound-rotor motors). The speed corresponding to maximum torque is known as the **stalling speed** or breakdown speed.

## Feeder Impedance in Star vs Delta Starting
_(10:31 - 25:26)_

When a feeder line with resistance $R_f$ connects to the motor, it reduces the terminal voltage and limits starting torque.
- **In Star Starting**: $R_f$ is in series with the motor phase impedance.
  $Z_{Y, \text{total}} = (R_f + R_{\text{br}}) + j X_{\text{br}}$
- **In Delta Starting**: The physical delta motor impedance must be converted to an equivalent star impedance ($Z_{\Delta \to Y} = Z_{\text{br}}/3$) to place it in series with the line feeder $R_f$.
  $Z_{\Delta, \text{eq}} = \left(R_f + \frac{R_{\text{br}}}{3}\right) + j \frac{X_{\text{br}}}{3}$

Decreasing feeder resistance (e.g., by paralleling identical feeders) increases starting torque. The percentage torque increase is far greater for delta starting than star starting, because the equivalent motor impedance in delta is smaller, making $R_f$ a more dominant portion of the total loop.

## Frequency Scaling of Starting Parameters
_(25:26 - 35:14)_

When supply frequency $f$ changes while holding voltage $V$ constant:
- **Starting Current**: $I_{\text{st}} \propto V/f$
- **Starting Torque**: $T_{\text{st}} \propto V^2/f^3$
- **Maximum Torque**: $T_{\max} \propto V^2/f^2$

To maintain identical starting current at a new frequency, keep $V/f$ constant. To maintain identical starting torque, $V^2/f^3$ must remain constant.

## Reduced Voltage Starting Analysis
_(35:18 - 40:22)_

When comparing starters against a Direct-On-Line (DOL) reference:
- **Auto-transformer**: With a tapping ratio $x$, the motor current reduces by $x$, the supply line current reduces by $x^2$, and the starting torque reduces by $x^2$. 
  For example, to limit motor current to $33\%$ ($x = 1/3$), the supply line current and starting torque drop to $(1/3)^2 = 1/9$ of the DOL values.
- **Star-Delta Starter**: Applies $1/\sqrt{3}$ phase voltage. Motor phase current drops by $1/\sqrt{3}$. Line current and starting torque both drop to $1/3$ of the delta DOL values.
- **Starter Selection**:
  - Up to 5 HP: DOL
  - 5 to 20 HP: Star-Delta
  - Above 20 HP: Auto-transformer (for squirrel-cage motors)

## Constant V/f Starting & Stability Limit
_(40:22 - 55:34)_

**Constant V/f Drive**:
Under constant $V/f$ control, $X_2$ scales with $f$. Since $s_{mT} = R_2/X_2$, the slip at maximum torque scales inversely with frequency ($s_{mT} \propto 1/f$). By lowering the frequency, $s_{mT}$ can be shifted to $1.0$, producing maximum torque right at standstill.

**Stability and Voltage Fluctuations**:
Electromagnetic torque scales with voltage squared ($T \propto V^2$). If voltage drops, the breakdown torque $T_{\max}$ drops. The motor will stall if $T_{\max}$ drops below the rated full-load load torque $T_{\text{fl}}$. The absolute minimum permissible voltage $V'$ occurs when $T_{\max}' = T_{\text{fl}}$.

---

## Summary and Key Takeaways

- Maximum torque develops at starting when rotor resistance equals standstill reactance: $s_{mT} = R_2/X_2 = 1$.
- To obtain peak torque at standstill in wound-rotor motors, the required series external resistance is $R_{\text{ext}} = X_2 - R_2$.
- When calculating feeder voltage drops with delta windings, transform the delta load to an equivalent star circuit with branch impedance $Z_{\text{br}}/3$.
- Paralleling an identical feeder halves the line resistance, yielding a significantly higher percentage torque increase in delta starting than in star starting.
- Neglecting stator impedance, starting current scales as $V/f$ and starting torque scales as $V^2/f^3$.
- Under constant $V/f$ speed control, slip at breakdown torque satisfies $s_{mT} \propto 1/f$, allowing peak torque at standstill by lowering supply frequency.
- In auto-transformer starting with tapping factor $x$, motor current scales as $x I_{\text{sc}}$, line current drawn from supply scales as $x^2 I_{\text{sc}}$, and torque scales as $x^2 T_{\text{st, DOL}}$.
- In star-delta starting, applied winding phase voltage drops by $1/\sqrt{3}$, while line current and starting torque drop by $1/3$.

---

[← Lec 147: Starting of SCIM](Lecture_147_Starting_of_SCIM.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 149: Starting of SRIM →](Lecture_149_Starting_of_SRIM.md)
