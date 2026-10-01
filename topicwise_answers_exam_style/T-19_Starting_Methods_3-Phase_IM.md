[← T-18: Testing & Circle Diagram](T-18_IM_Testing_and_Circle_Diagram.md) | [🏠 Index](README.md) | [T-20: Speed Control & Braking →](T-20_Speed_Control_and_Braking.md)

---

# T-19: Starting Methods (3-Phase IM)

**ECE 2207 — Exam-Style Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and exam-style answers on **Starting Methods (3-Phase IM)** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2019 Q7(b)]
> 📋 **Appeared in:** 2019 Q7(b)

**(b) Effects of direct-line starting of IM > 25 kW. How to minimize? [04]**

**Effects of direct-on-line (DOL) starting:**
1. Starting current surge $= 5$–8 times rated current. This causes voltage dips in the supply that affect other loads.
2. High mechanical stress on motor shaft, couplings, and driven equipment due to high starting torque surges.
3. Thermal stress on windings: repeated DOL starting can overheat the motor.
4. For motors > 25 kW, the utility supply authority often prohibits DOL starting due to supply disturbances.

**How to minimize:**
1. **Star-delta starter:** Reduces starting voltage to $V_L/\sqrt{3}$. Starting current and torque reduce to 1/3 of DOL values.
2. **Auto-transformer starter:** Reduced voltage via tapped autotransformer. Provides better torque-current ratio than Y-Δ.
3. **Rotor resistance (slip-ring motor):** Insert external resistance in rotor circuit to improve starting torque with reduced current.
4. **Soft starter (electronic):** Thyristor-based gradual voltage ramp-up. Smooth starting, no current surge.
5. **Variable frequency drive (VFD):** Controls both voltage and frequency. Best control, most expensive.

![Star-delta starter connections](../Books/diagrams/ch35_p23_fig35_21.jpg)
![Auto-transformer starter connections](../Books/diagrams/ch35_p20_fig35_19.jpg)

---

### [2020 Q7(c)]
> 📋 **Appeared in:** 2018 Q7(a), 2020 Q7(c) (Years: 2018, 2020)

**(c) Prove that star-delta starter is equivalent to an auto-transformer of ratio $1/\sqrt{3}$ (58%). [05]**

**Direct-on-line (DOL) starting: delta connection:**

Each stator phase sees full line voltage $V_L$. Per-phase starting impedance $Z_s$. Starting current per phase:
$$I_{\phi,DOL} = \frac{V_L}{Z_s}$$

Line current (delta connection): $I_{L,DOL} = \sqrt{3} I_{\phi,DOL} = \frac{\sqrt{3} V_L}{Z_s}$

**Star-delta starting: star connection:**

Each phase sees $V_L/\sqrt{3}$. Starting current per phase:
$$I_{\phi,Y} = \frac{V_L/\sqrt{3}}{Z_s} = \frac{V_L}{\sqrt{3} Z_s}$$

Line current (star connection) = phase current:
$$I_{L,Y} = I_{\phi,Y} = \frac{V_L}{\sqrt{3} Z_s}$$

**Ratio of starting line currents:**
$$\frac{I_{L,Y}}{I_{L,DOL}} = \frac{V_L/(\sqrt{3} Z_s)}{\sqrt{3} V_L/Z_s} = \frac{1}{3}$$

Starting current is reduced to $1/3$ of DOL current.

**Auto-transformer equivalence:**

For an auto-transformer with ratio $x = V_2/V_1$, the supply current is $x^2$ times the DOL current.

Here: $x^2 = 1/3 \implies x = 1/\sqrt{3} = 0.577 \approx 58\%$

$$\boxed{\text{Star-delta starter} \equiv \text{Auto-transformer starter with ratio } \frac{1}{\sqrt{3}} = 57.7\%}$$

![Comparison of Direct-switching and Auto-transformer / Star-Delta starter](../Books/diagrams/ch35_p20_fig35_20.jpg)

*(Proved)*

---

[← T-18: Testing & Circle Diagram](T-18_IM_Testing_and_Circle_Diagram.md) | [🏠 Index](README.md) | [T-20: Speed Control & Braking →](T-20_Speed_Control_and_Braking.md)
