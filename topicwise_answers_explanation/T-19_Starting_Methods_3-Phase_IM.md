[← T-18: Testing & Circle Diagram](T-18_IM_Testing_and_Circle_Diagram.md) | [🏠 Index](README.md) | [T-20: Speed Control & Braking →](T-20_Speed_Control_and_Braking.md)

---

# T-19: Starting Methods (3-Phase IM)

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Starting Methods (3-Phase IM)** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-19: Why Starting Methods Are Critical for Large Induction Motors (> 25 kW)

*Appears in: 2018 Q7(a), 2019 Q7(b), 2020 Q7(c)*

#### The physical origin of huge starting currents

At standstill ($N = 0$, $s = 1$), the rotor conductors are stationary relative to the rotating magnetic field. The rate of flux cutting is maximum, and the back-EMF that normally opposes current during running does not exist. 

The entire applied line voltage is opposed only by the small internal leakage impedance of the machine:
$$I_{start} = \frac{V_1}{\sqrt{(R_1 + R_2')^2 + (X_1 + X_2')^2}}$$

In standard industrial squirrel-cage induction motors, this standstill leakage impedance is extremely low. Consequently, when connected directly across the supply line (Direct-On-Line or DOL starting), the motor draws:
$$I_{start} = 5 \text{ to } 8 \times I_{\text{rated}}$$

#### Destructive effects of direct-on-line starting for motors > 25 kW:

1. **System voltage dip (sag):** The enormous starting current flowing through the supply transformer and distribution feeder cables causes a large internal impedance drop. This depresses the local busbar voltage by 10% to 25%, causing flickering lights, tripping computer systems, and disengaging under-voltage contactors of other running equipment.
2. **Thermal overloading:** Copper losses are proportional to current squared ($I^2 R$). A starting current of $6 I_{\text{rated}}$ produces $36 \times$ normal heat generation. Repeated DOL starts will char and degrade the stator winding insulation.
3. **Severe mechanical shock:** The sudden burst of starting torque produces severe mechanical stress on motor shafts, keyways, gearboxes, and belt drives.
4. **Utility regulations:** Supply utilities universally enforce regulations forbidding DOL starting for motors rated above 5 kW to 25 kW (depending on local distribution transformer capacity).

#### Solutions and starter technologies

To alleviate these issues, several starting methods are used:
- **Star-Delta Starter:** The motor starts in Star (reducing phase voltage to $V_L/\sqrt{3}$) and switches to Delta once near full speed.
- **Auto-transformer Starter:** Uses tapped auto-transformer windings (typically 50%, 65%, or 80% taps) to supply reduced voltage during start-up.
- **Rotor Resistance Starter:** For wound-rotor (slip-ring) motors only; inserts external rheostats to simultaneously limit current and boost starting torque.
- **Electronic Soft Starter:** Uses back-to-back thyristors with phase-angle firing control to ramp up voltage smoothly without electrical or mechanical transients.

![Star-delta starter connections](../Books/Theraja/Ch-35/diagrams/ch35_p23_fig35_21.jpg)

![Auto-transformer starter connections](../Books/Theraja/Ch-35/diagrams/ch35_p20_fig35_19.jpg)

---

### [2020 Q7(c)]: Proof: Star-Delta Starter is Equivalent to Auto-Transformer of Ratio $1/\sqrt{3}$ (57.7%)

> 📋 **Appeared in:** 2018 Q7(a), 2020 Q7(c)

#### Step 1: Direct-on-Line (DOL) starting with normal Delta connection

Let:
- $V_L$ = Supply line voltage.
- $Z_{sc}$ = Short-circuit (standstill) impedance per phase of the motor winding.

When started directly in Delta ($\Delta$):
- Voltage across each phase winding: $V_{ph,\Delta} = V_L$.
- Phase starting current:
  $$I_{ph,DOL} = \frac{V_L}{Z_{sc}}$$
- Supply line current in Delta:
  $$I_{L,DOL} = \sqrt{3} I_{ph,DOL} = \frac{\sqrt{3} V_L}{Z_{sc}}$$

#### Step 2: Star-Delta starter during starting (Star connection)

During start-up, the stator windings are reconnected in Star ($Y$):
- Voltage across each phase winding is reduced to line-to-neutral voltage:
  $$V_{ph,Y} = \frac{V_L}{\sqrt{3}}$$
- Phase starting current:
  $$I_{ph,Y} = \frac{V_{ph,Y}}{Z_{sc}} = \frac{V_L/\sqrt{3}}{Z_{sc}} = \frac{V_L}{\sqrt{3} Z_{sc}}$$
- In Star connection, line current equals phase current ($I_{L,Y} = I_{ph,Y}$):
  $$I_{L,Y} = \frac{V_L}{\sqrt{3} Z_{sc}}$$

#### Step 3: Ratio of line starting currents

Taking the ratio of line current drawn from the supply in Star to that in DOL Delta:
$$\frac{I_{L,Y}}{I_{L,DOL}} = \frac{\frac{V_L}{\sqrt{3} Z_{sc}}}{\frac{\sqrt{3} V_L}{Z_{sc}}} = \frac{1}{\sqrt{3} \times \sqrt{3}} = \frac{1}{3}$$

Thus, **a star-delta starter reduces the starting line current to exactly $\frac{1}{3}$ (33.3%) of the DOL value**.

#### Step 4: Line current with an Auto-Transformer starter

Let an auto-transformer have transformation tapping ratio $x = \frac{V_2}{V_1} < 1$:
- Voltage applied to motor terminals: $V_{motor} = x V_L$.
- Current drawn by motor from auto-transformer secondary:
  $$I_{motor} = x I_{DOL}$$
- Because the auto-transformer is an ideal power transformer (neglecting magnetizing current), input VA = output VA:
  $$V_L \times I_{line} = (x V_L) \times I_{motor} = (x V_L) \times (x I_{DOL})$$
  $$I_{line} = x^2 I_{DOL}$$

Notice that the supply line current is reduced by the factor **$x^2$** because of the dual reduction (reduced motor current plus step-down current transformation from supply to motor).

#### Step 5: Establishing equivalence

To make the auto-transformer draw the identical line current as the Star-Delta starter:
$$x^2 I_{DOL} = \frac{1}{3} I_{DOL}$$
$$x^2 = \frac{1}{3}$$
$$x = \frac{1}{\sqrt{3}} = 0.57735 \approx \boxed{57.7\%}$$

![Comparison of Direct-switching and Auto-transformer / Star-Delta starter](../Books/Theraja/Ch-35/diagrams/ch35_p20_fig35_20.jpg)

**Physical Conclusion:** A Star-Delta starter reduces voltage and line current by exactly the same amount as an auto-transformer starter set to a **57.7% voltage tapping ratio**.

---

[← T-18: Testing & Circle Diagram](T-18_IM_Testing_and_Circle_Diagram.md) | [🏠 Index](README.md) | [T-20: Speed Control & Braking →](T-20_Speed_Control_and_Braking.md)
