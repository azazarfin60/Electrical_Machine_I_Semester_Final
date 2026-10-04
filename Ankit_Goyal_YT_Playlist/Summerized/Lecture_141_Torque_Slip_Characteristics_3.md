---
title: "Electrical Machines | Lec 102 | Torque Slip Characteristics -3 | GATE Electrical Engineering"
lecture: 141
topic: "Induction Machines"
duration: "00:49:44"
source: "https://www.youtube.com/watch?v=SPexadar380"
compiled: "2026-09-23"
tags:
  - electrical-machines
  - gate
---

[← Lec 140: Torque Slip Characteristics 2](Lecture_140_Torque_Slip_Characteristics_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 142: Torque Slip Characteristics 1 →](Lecture_142_Torque_Slip_Characteristics_1.md)

---

# Electrical Machines | Lec 102 | Torque Slip Characteristics -3 | GATE Electrical Engineering

- **Source**: https://www.youtube.com/watch?v=SPexadar380
- **Duration**: 00:49:44
- **Compiled**: 2026-09-23

---

## Overview

This lecture examines how induction motor torque-speed and power-speed curves shift under parameter variations. It analyzes changes in rotor resistance, leakage reactance, supply voltage, and supply frequency under constant $V/f$ and constant voltage regimes. The discussion isolates mechanical power in the equivalent circuit and derives the condition for maximum mechanical power transfer. Finally, the lecture details overall operating characteristics, proving how speed, power factor, stator current, and efficiency evolve from no-load to rated full-load.

## Contents

- [[#Effect of Parameter Variations on Torque|Effect of Parameter Variations on Torque]]
- [[#Frequency Variations and $V/f$ Control|Frequency Variations and $V/f$ Control]]
- [[#Maximum Mechanical Power vs. Maximum Torque|Maximum Mechanical Power vs. Maximum Torque]]
- [[#Evolution of Operating Characteristics|Evolution of Operating Characteristics]]

---

## Effect of Parameter Variations on Torque
_(00:13 - 16:58)_

We evaluate how altering physical parameters shifts the torque-speed curve:

1. **Increasing Rotor Resistance ($R_2$)**:
   - $T_{\text{max}}$ remains completely unchanged (peak height is invariant).
   - $s_{mT}$ increases proportionally. The peak shifts left toward lower speeds.
   - Starting torque $T_{\text{st}}$ increases.
   - Operating speed under a constant load drops (useful for speed control).
   - Starting current decreases, and operating power factor improves.

2. **Increasing Leakage Reactance ($X_2$)**:
   - Everything gets worse: $T_{\text{max}}$ decreases, $T_{\text{st}}$ decreases, and $s_{mT}$ decreases (peak shifts right).

3. **Decreasing Supply Voltage ($V_1$)**:
   - $T_{\text{max}} \propto V_1^2$ and $T_{\text{st}} \propto V_1^2$. The entire curve scales down vertically.
   - $s_{mT}$ and synchronous speed $N_s$ remain unaffected.

## Frequency Variations and $V/f$ Control
_(17:03 - 23:04)_

When supply frequency $f$ varies, synchronous speed $\omega_s \propto f$ and leakage reactance $X_2 \propto f$ also vary. 

**Case 1: Constant $V/f$ Control (Below Base Speed)**
- **$T_{\text{max}}$ is constant**: Because $T_{\text{max}} \propto (V_1/f)^2$, maintaining constant $V/f$ keeps peak torque strictly constant.
- **Starting Torque**: $T_{\text{st}} \propto 1/f$. Starting torque improves at lower frequencies.

**Case 2: Constant Voltage, Variable Frequency (Above Base Speed)**
- **$T_{\text{max}} \propto 1/f^2$**: Peak torque collapses rapidly as frequency increases in this field-weakening regime.
- **Starting Torque**: $T_{\text{st}} \propto 1/f^3$.

## Maximum Mechanical Power vs. Maximum Torque
_(23:07 - 39:12)_

A common trap is assuming maximum mechanical power ($P_{\text{mech}}$) occurs at the same slip as maximum torque ($T_{\text{dev}}$). This is false because $P_{\text{mech}} = T_{\text{dev}} \omega_s (1-s)$.

To maximize mechanical power, we apply the Maximum Power Transfer Theorem across the fictitious mechanical load resistor $R_2'(1/s - 1)$:
> [!success] Slip at Maximum Mechanical Power
> $$s_{mp} = \frac{R_2'}{R_2' + \sqrt{(R_{th} + R_2')^2 + (X_{th} + x_2')^2}}$$

Notice that **$s_{mp} < s_{mT}$**. Maximum mechanical power always occurs at a lower slip (higher speed) than maximum torque.

## Evolution of Operating Characteristics
_(39:13 - 49:37)_

As mechanical shaft load increases from no-load to full-load:

- **Speed**: Drops slightly (2-5% regulation), very similar to a DC shunt motor.
- **Current**: Rises monotonically from its magnetizing-dominated no-load value ($I_0 \approx 0.3 \text{ p.u.}$) to $1.0 \text{ p.u.}$ at full load.
- **Power Factor**: Starts extremely poor at no-load (0.1 to 0.2 lagging) due to the air gap requiring huge reactive magnetizing current. As active mechanical load increases, the active current component dominates, improving the power factor to 0.85 - 0.90 lagging at full load.
- **Efficiency**: Starts at zero (no output power). Rises rapidly to peak where variable copper losses equal constant rotational/core losses, then declines slightly toward full load.

---

## Summary and Key Takeaways

- Increasing rotor resistance preserves peak breakdown torque magnitude while shifting the peak toward lower speeds and increasing starting torque.
- Higher leakage reactance reduces starting torque, maximum breakdown torque, and intermediate torques across all slips.
- Supply voltage scaling shifts the entire torque-speed curve vertically by $V_1^2$ without changing the speed corresponding to maximum torque.
- In constant $V/f$ operation below base speed, maximum breakdown torque remains constant and starting torque varies inversely with frequency as $T_{\text{st}} \propto 1/f$.
- Above base speed with constant voltage, maximum torque scales as $T_{\text{max}} \propto 1/f^2$ and starting torque scales as $T_{\text{st}} \propto 1/f^3$.
- Mechanical power is modeled by fictitious resistance $R_2'(1/s - 1)$, and reaches its peak at slip $s_{mp} = \frac{R_2'}{R_2' + \sqrt{(R_{th} + R_2')^2 + (X_{th} + x_2')^2}}$, which is strictly less than breakdown slip $s_{mT}$.
- At no-load, an induction motor draws a high magnetizing current through the air gap, resulting in a low power factor between 0.1 and 0.2 lagging.
- Applying shaft load increases active stator current, which causes power factor to rise toward 0.85 to 0.90 lagging and causes efficiency to reach a peak where variable copper losses equal constant losses.

---

[← Lec 140: Torque Slip Characteristics 2](Lecture_140_Torque_Slip_Characteristics_2.md) | [🏠 Index](00_yt_study_guide.md) | [Lec 142: Torque Slip Characteristics 1 →](Lecture_142_Torque_Slip_Characteristics_1.md)
