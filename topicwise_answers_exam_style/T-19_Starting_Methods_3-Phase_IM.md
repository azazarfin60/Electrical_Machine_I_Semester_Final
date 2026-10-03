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

![Star-delta starter connections](../Books/Theraja/Ch-35/diagrams/ch35_p23_fig35_21.jpg)
![Auto-transformer starter connections](../Books/Theraja/Ch-35/diagrams/ch35_p20_fig35_19.jpg)

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

![Comparison of Direct-switching and Auto-transformer / Star-Delta starter](../Books/Theraja/Ch-35/diagrams/ch35_p20_fig35_20.jpg)

*(Proved)*

---


---

### [2023 Q7(a)]
> 📋 **Appeared in:** 2023 Q7(a)

**(a) Explain the $\text{Y}-\Delta$ starter to start $3-\varphi$ induction motor with the help of neat sketch. [CO3, Marks: 03]**

![Star-delta starter wiring diagram for a three-phase induction motor, with a changeover switch connecting the stator first in star and then in delta](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_8_33.jpeg)

**Where it is used.** Only on motors built to run with a **delta-connected stator**, and whose six winding ends are brought out to the terminal box.

**Operation.** A two-way changeover switch (or two contactors with a timer) does the work.

1. **START position.** The switch connects the three winding ends to a common point, so the stator is in **star**. Each phase then gets
   $$V_{ph} = \frac{V_L}{\sqrt{3}} = 0.577\, V_L$$
2. **RUN position.** After the motor reaches about 80% of full speed, the switch is thrown over. The windings are reconnected in **delta**, so each phase now gets the full line voltage $V_L$.

**Effect on current and torque.**

Let $I_{sc}$ be the per-phase short-circuit current the delta-connected motor would draw on direct switching.

$$I_{st}\ \text{per phase} = \frac{1}{\sqrt{3}}\, I_{sc}\ \text{per phase}$$

In star, line current equals phase current, so
$$\frac{\text{line } I_{st}}{\text{line } I_{sc}} = \frac{1}{3}$$

Since $T \propto V_{ph}^2$,
$$\frac{T_{st,Y}}{T_{st,\Delta}} = \left(\frac{1}{\sqrt{3}}\right)^2 = \frac{1}{3}$$

$$\boxed{\text{Starting current} = \tfrac{1}{3}\ \text{of DOL} \qquad \text{Starting torque} = \tfrac{1}{3}\ \text{of DOL}}$$

**Torque to full-load torque:**
$$\frac{T_{st}}{T_f} = \frac{1}{3}\left(\frac{I_{sc}}{I_f}\right)^2 s_f$$

**Merits and limits.** Cheap, simple and effective. It is equivalent to an auto-transformer starter with a 58% tap. But the starting torque is only one third of DOL, so it suits light-starting loads only, such as machine tools, pumps and motor-generator sets. There is also a current surge at changeover.

---

### [2023 Q7(b)]
> 📋 **Appeared in:** 2023 Q7(b)

**(b) A 15 Hp, $3-\varphi$, 6-pole, 50 Hz, 400 V, $\Delta-$connected induction motor runs at 960 rpm on full load. If it takes 84.6 A on direct starting, find the ratio of starting torque to full load torque with a star-delta starter. Full load efficiency and power factor are 88% and 0.85, respectively. [CO3, Marks: 04]**

![Star-delta starter wiring and circuit diagram](../Books/Theraja/Ch-35/diagrams/ch35_p23_fig35_21.jpg)

**Given:** $P_{out} = 15\text{ Hp}$, $P = 6$, $f = 50\text{ Hz}$, $V_L = 400\text{ V}$, $\Delta$-connected, $N = 960\text{ rpm}$, $I_{sc} = 84.6\text{ A}$ (line, on direct start), $\eta = 0.88$, $\cos\phi = 0.85$.

**Step 1. Synchronous speed and full-load slip.**
$$N_s = \frac{120 f}{P} = \frac{120 \times 50}{6} = 1000\text{ rpm}$$
$$s_f = \frac{N_s - N}{N_s} = \frac{1000 - 960}{1000} = 0.04$$

**Step 2. Full-load line current.**
$$P_{out} = 15 \times 746 = 11190\text{ W}$$
$$\text{Input} = \frac{11190}{0.88} = 12716\text{ W}$$
$$\sqrt{3}\, V_L I_f \cos\phi = 12716$$
$$I_f = \frac{12716}{\sqrt{3} \times 400 \times 0.85} = \frac{12716}{588.9} = 21.59\text{ A (line)}$$

**Step 3. Starting current with the star-delta starter.**

On direct (delta) start the line current would be 84.6 A. In star the line starting current is one third of that:
$$I_{st} = \frac{84.6}{3} = 28.2\text{ A (line)}$$

**Step 4. Torque ratio.** For a star-delta starter,
$$\frac{T_{st}}{T_f} = \frac{1}{3}\left(\frac{I_{sc}}{I_f}\right)^2 s_f$$
$$\frac{I_{sc}}{I_f} = \frac{84.6}{21.59} = 3.918$$
$$\frac{T_{st}}{T_f} = \frac{1}{3} \times (3.918)^2 \times 0.04 = \frac{1}{3} \times 15.35 \times 0.04 = 0.2047$$

$$\boxed{\frac{T_{st}}{T_f} = 0.205 \quad \text{i.e. } 20.5\% \text{ of full-load torque}}$$

> [!info] Cross-check with per-phase values
> $I_{sc}$ per phase $= 84.6/\sqrt{3} = 48.84\text{ A}$, so $I_{st}$ per phase $= 48.84/\sqrt{3} = 28.2\text{ A}$.
> Full-load phase current $= 21.59/\sqrt{3} = 12.47\text{ A}$.
> $T_{st}/T_f = (28.2/12.47)^2 \times 0.04 = 5.117 \times 0.04 = 0.205$. Same answer.

The starting torque is only about one fifth of full-load torque. This motor can only be star-delta started against a very light load.

---

[← T-18: Testing & Circle Diagram](T-18_IM_Testing_and_Circle_Diagram.md) | [🏠 Index](README.md) | [T-20: Speed Control & Braking →](T-20_Speed_Control_and_Braking.md)
