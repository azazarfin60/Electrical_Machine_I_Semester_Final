[← T-16: Torque Equations & Curves](T-16_Torque_Equations_and_Characteristics.md) | [🏠 Index](README.md) | [T-18: Testing & Circle Diagram →](T-18_IM_Testing_and_Circle_Diagram.md)

---

# T-17: Power Flow & Rotor Power

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Power Flow & Rotor Power** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### IM-01: Air-Gap Power Ratios: $P_g : P_{r,Cu} : P_m = 1 : s : (1-s)$

*Appears in: 2018 Q5b, 2020 Q6b, 2021 Q6c, 2023 Q6a, 2024 Q5b*

#### The power flow story

Electrical power enters the stator from the supply. Some is lost in stator resistance (stator Cu loss) and stator iron (core loss). The rest crosses the air gap as electromagnetic power: this is $P_g$, the air-gap power.

On the rotor side, $P_g$ must go somewhere. Part becomes heat in the rotor resistance (rotor Cu loss). The rest becomes mechanical work delivered to the shaft. The question is: what fraction goes where?

#### Derivation from the equivalent circuit

At slip $s$, the rotor circuit has:
- Rotor resistance: $R_2$
- Rotor reactance: $sX_2$
- Rotor current: $I_2 = sE_2/\sqrt{R_2^2 + s^2X_2^2}$

**Air-gap power per phase:**

In the equivalent circuit, the air-gap power appears as the power in the resistance $R_2/s$:
$$P_{g,\text{phase}} = I_2^2 \cdot \frac{R_2}{s}$$

**Rotor copper loss per phase:**

$$P_{Cu,\text{phase}} = I_2^2 \cdot R_2$$

**Mechanical power per phase:**

$$P_{m,\text{phase}} = P_{g,\text{phase}} - P_{Cu,\text{phase}} = I_2^2 \cdot \frac{R_2}{s} - I_2^2 R_2 = I_2^2 R_2\left(\frac{1}{s} - 1\right) = I_2^2 R_2 \cdot \frac{1-s}{s}$$

**Ratios:**

$$\frac{P_{Cu}}{P_g} = \frac{I_2^2 R_2}{I_2^2 R_2/s} = s$$

$$\frac{P_m}{P_g} = \frac{I_2^2 R_2(1-s)/s}{I_2^2 R_2/s} = (1-s)$$

Therefore:
$$\boxed{P_g : P_{Cu} : P_m = 1 : s : (1-s)}$$

![Induction motor power flow diagram showing air-gap, copper, and mechanical stages](../Books/diagrams/Ch-34_p39_fig38.jpg)

![Power stages block diagram of 3-phase induction motor](../Books/diagrams/Ch-34_p38_power_stages_block.jpg)

#### Physical intuition

At full load slip $s = 0.04$ (4%):
- 4% of air-gap power is wasted in rotor copper heat
- 96% becomes mechanical output

This is why induction motors are designed to run at small slip (2–5%). Small slip = small rotor copper loss = high rotor efficiency.

If you double the slip (say by adding rotor resistance), rotor copper loss doubles, and mechanical output drops. You're throwing away more power as heat in the rotor.

**For the whole rotor:** $\eta_{\text{rotor}} = (1-s)$. At $s = 0.04$: rotor efficiency = 96%. Very high: the rotor converts almost all received power to mechanical work.


---

---

### Q6(b): How supply voltage drop affects copper losses

> 📋 **Appeared in:** 2020 Q6(b)

#### The torque-voltage relationship

Torque at any slip:
$$T \propto \frac{sE_2^2 R_2}{R_2^2 + s^2 X_2^2}$$

Since $E_2 \propto V$ (rotor EMF is proportional to supply voltage).

For a constant-torque load (independent of speed), $T$ must remain the same after the voltage drops. So:

$$T = \frac{k s_1 (V_1)^2 R_2}{R_2^2 + s_1^2 X_2^2} = \frac{k s_2 (0.9V_1)^2 R_2}{R_2^2 + s_2^2 X_2^2}$$

**Simplified analysis (low slip approximation):**

At low slip, $s^2 X_2^2 \ll R_2^2$, so $T \approx k s E_2^2 R_2 / R_2^2 = k s E_2^2 / R_2 \propto s V^2$.

For constant torque: $s_1 V_1^2 = s_2 V_2^2$

$$s_2 = s_1 \left(\frac{V_1}{V_2}\right)^2 = s_1 \times \left(\frac{1}{0.9}\right)^2 = s_1 \times 1.2346$$

**Copper loss ratio:**

Rotor copper loss $P_{Cu} = s \times P_g$ and air-gap power $P_g = T \omega_s$ = constant (same torque, same synchronous speed).

$$\frac{P_{Cu,\text{new}}}{P_{Cu,\text{old}}} = \frac{s_2}{s_1} = 1.2346$$

**Increase in copper loss = 23.46%** for a 10% voltage drop.

**Why this matters:** A 10% voltage sag (common during grid disturbances) causes nearly 25% more copper losses. The motor overheats. Repeated voltage sags cause premature insulation failure. This is why voltage-sensitive motors (pumps, compressors) need to be protected with under-voltage relays.

---

[← T-16: Torque Equations & Curves](T-16_Torque_Equations_and_Characteristics.md) | [🏠 Index](README.md) | [T-18: Testing & Circle Diagram →](T-18_IM_Testing_and_Circle_Diagram.md)
