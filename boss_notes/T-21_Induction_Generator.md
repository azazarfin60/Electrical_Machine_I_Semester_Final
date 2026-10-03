[← T-20: Speed Control & Braking](T-20_Speed_Control_and_Braking.md) | [🏠 Index](00_Index.md) | [T-22: DFRT & 1-Phase IM →](T-22_DFRT_and_1Phase_IM.md)

---

# T-21: Induction Generator
> **Section:** B | **Priority:** 🟡 MEDIUM | **Exam Frequency:** 3/7 years
> **Sources:** Theraja Ch-34 (Art. 34.47), Slides L-07

## Why This Topic Matters

Induction generator questions appeared in 3 out of 7 papers (2018, 2023, 2024). This is a rising trend: 2023 asked for the description with schematic arrangements (3 marks), and 2024 gave the descriptive process (4 marks) plus the capacitance and engine-speed numerical (4 marks) that repeats 2018 Q5(c) verbatim. The concept connects slip, power flow, and reactive power. It is worth 3-4 marks per appearance, and 8 of the 10 marks in 2024 Q8.

---

## 📝 Key Definitions

> **Induction Generator:** "When an induction motor is driven by an external prime mover at a speed above synchronous speed ($N > N_s$), slip becomes negative ($s < 0$). The machine reverses power flow and delivers active power to the supply while absorbing reactive power for its magnetization. This mode of operation is called induction generator or asynchronous generator mode." — Theraja, Art. 34.47

---

## How It Works

1. An external prime mover (engine, turbine) drives the IM rotor above synchronous speed ($N > N_s$).
2. Slip becomes negative: $s = (N_s - N)/N_s < 0$.
3. The air-gap power reverses direction: power flows from rotor to stator to supply.
4. The machine generates active (real) power.
5. It still draws reactive power (VARs) from the grid for excitation.

**Grid-connected IG:** The grid provides the reactive power and sets the frequency/voltage.

**Self-Excited IG (SEIG):** When not connected to the grid, shunt capacitors supply the reactive power. The capacitor bank must provide enough VARs to magnetize the machine.

![Self-excited induction generator with capacitor bank](diagrams/seig_capacitor_bank.jpg)

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: 440V, 4-pole, 1470 rpm, 30 kW IM used as generator. Rated current 40A, pf = 0.85. Find (i) capacitance per phase (delta-connected), (ii) engine speed for 50 Hz.
> **Appeared:** 2018 Q5(c) — 4 marks, **repeated verbatim as 2024 Q8(c) — 4 marks**

**Full Answer:**

$N_s = 120 \times 50/4 = 1500$ rpm

**(i) Capacitance per phase (delta):**

Reactive power needed: $Q = \sqrt{3} V_L I_L \sin\phi$

$\sin\phi = \sqrt{1 - 0.85^2} = 0.5268$

$Q = \sqrt{3} \times 440 \times 40 \times 0.5268 = 16065$ VAR

Per phase (delta): $Q_\phi = 16065/3 = 5355$ VAR

Phase voltage (delta) = line voltage = 440 V

$$X_C = V^2/Q_\phi = 440^2/5355 = 36.15\,\Omega$$

$$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 36.15} = \boxed{88.05\,\mu\text{F} \approx 88.2\,\mu\text{F per phase}}$$

**(ii) Engine speed for 50 Hz:**

Motor slip at full load: $s = (1500 - 1470)/1500 = 0.02$

As generator, slip magnitude is same but negative: $s_{\text{gen}} = -0.02$

$$N = N_s(1 - s_{\text{gen}}) = 1500(1 + 0.02) = \boxed{1530 \text{ rpm}}$$

> [!NOTE] Learn one solution for both years
> 2024 Q8(c) repeats 2018 Q5(c) word for word, data included. The answer is still 88.2 µF per phase in delta and 1530 rpm.

---

### 🎯 Q2: Describe the process following which an IM can be operated as IG.
> **Appeared:** 2024 Q8(b) — 4 marks

**Full Answer:**

**Step 1 — Reverse the sign of slip.** An induction motor becomes a generator only when the rotor turns **faster** than the rotating field. That is $N > N_s$, so
$$s = \frac{N_s - N}{N_s} < 0$$
The whole operating picture is set by this one sign change.

**Step 2 — What happens at negative slip.** The rotor emf $E_{2r} = sE_2$ and the active rotor current reverse phase, so power flow across the air gap reverses ($P_g < 0$) and mechanical torque opposes rotation (braking torque). Note that rotor copper loss ($3I_2^2 R_2$) remains strictly positive heat dissipation.

**Step 3 — Reverse the power flow.** Instead of taking power from the line through the shaft and giving it back through the rotor, the machine does the opposite:

| Port | Power direction in motoring | Power direction in generating |
|:---|:---|:---|
| Shaft | power **out** of the machine | power **in** to the machine |
| Stator terminals | power **in** from the line | power **out** to the line |

**Step 4 — Set up the excitation.** The machine still needs reactive power to magnetise itself. On a live grid the line supplies it. On an isolated load, connect a **capacitor bank** across the stator terminals so the capacitors provide the magnetising VARs; residual magnetism in the rotor starts the voltage build-up.

**Step 5 — Pick the speed and load.** The prime mover (engine, turbine) must run at a little above $N_s = 120f/P$. With the grid holding $f$, the speed is essentially fixed and the prime mover power sets the load. Beyond the breakdown point further prime-mover torque gives less output, so the machine cannot be overloaded.

---

### 🎯 Q3: With the help of schematic arrangements, describe how IM can be operated as IG.
> **Appeared:** 2023 Q8(b) — 3 marks

**Full Answer:**

**Principle.** Drive the rotor **above** synchronous speed with a prime mover. Then $N > N_s$, so
$$s = \frac{N_s - N}{N_s} < 0$$

With negative slip the rotor emf, rotor current and torque all reverse. The machine now opposes the prime mover, absorbs mechanical power at the shaft and feeds electrical power out through the stator. It has become an **induction generator**.

**Arrangement 1: Grid-connected induction generator**

![A squirrel-cage machine driven above synchronous speed by a prime mover while connected to a three-phase line, working as an induction generator, with its power-flow diagram](../Books/Theraja/Ch-34/diagrams/Ch-34_p33_fig28_29.jpg)

The stator stays connected to a live 3-phase line. The line fixes the voltage and the frequency, and supplies the magnetising (reactive) power.

- **Active power $P$** flows out of the stator into the line.
- **Reactive power $Q$** flows from the line into the machine, because the generator needs it to set up its own field.

So the machine delivers $P$ and absorbs $Q$ at the same time, and the two flow in opposite directions.

**Arrangement 2: Self-excited induction generator**

![Self-excited induction generator with a delta-connected capacitor bank supplying an isolated three-phase load](../Books/Theraja/Ch-34/diagrams/Ch-34_p33_fig30.jpg)

For an isolated load there is no line to draw $Q$ from. Connect a **capacitor bank** across the stator terminals instead. The capacitors supply the reactive power:
$$Q_C = \text{capacitor output} \ \geq \ Q \ \text{required by machine and load}$$

Residual magnetism in the rotor starts the build-up. Voltage grows until the capacitor line crosses the machine magnetising curve.

| Feature | Grid-connected | Self-excited |
|:---|:---|:---|
| Source of $Q$ | The line | Capacitor bank |
| Voltage and frequency set by | The line | Speed and capacitance |
| Voltage regulation | Good | Poor |

**Merits.** No d.c. field winding, no brushes, no synchronising needed, rugged and cheap, and it cannot be overloaded because torque falls off beyond the breakdown point.

**Limits.** Cannot supply reactive power. Cannot work alone without capacitors. Voltage and frequency are not independently controllable. Used for small hydro and wind plants.

---

### 🎯 Q4: What happens if the slip of a 3-phase IM becomes negative?
> **Appeared:** 2017 Q1(d) — 1 mark

**Full Answer:**

If $N > N_s$, slip is negative. The motor acts as an **induction generator**. It delivers active electrical power back to the supply. It still absorbs reactive power from the supply for magnetization.

---

### 🎯 Q5: How can the direction of rotation of a 3-phase IM be reversed?
> **Appeared:** 2020 Q6(a) — 2 marks

**Full Answer:**

Interchange any two of the three supply phase connections. This reverses the phase sequence (e.g., R-Y-B to R-B-Y), which reverses the direction of the rotating magnetic field. The rotor follows the RMF and reverses direction.

---

## Exam Variants

| Year | Question | Marks |
|:---|:---|:---|
| 2017 Q1(d) | Negative slip meaning | 1 |
| 2018 Q5(c) | IG capacitance + engine speed numerical | 4 |
| 2020 Q6(a) | Reverse rotation of IM | 2 |
| 2023 Q8(b) | How IM can be operated as IG (schematic arrangements) | 3 |
| 2024 Q8(b) | Process by which IM is operated as IG | 4 |
| 2024 Q8(c) | IG capacitance + engine speed (verbatim repeat of 2018 Q5(c)) | 4 |

---

## ⚡ Exam Tips & Common Mistakes

1. **Generator slip is negative.** $N > N_s$ means $s < 0$. The machine delivers power.
2. **Capacitors must supply ALL the VARs** for self-excited IG. No grid = no reactive power source.
3. **Engine speed = $N_s(1 + |s|)$.** Don't subtract; the generator runs ABOVE synchronous speed.

## 🔗 Related Topics

- [T-13: Slip & Basics](T-13_Slip_and_Basics.md) — Negative slip concept
- [T-20: Speed Control & Braking](T-20_Speed_Control_and_Braking.md) — Regenerative braking = generator mode
- [T-16: Power Flow](T-16_Power_Flow.md) — Reversed power flow at $s < 0$

---

[← T-20: Speed Control & Braking](T-20_Speed_Control_and_Braking.md) | [🏠 Index](00_Index.md) | [T-22: DFRT & 1-Phase IM →](T-22_DFRT_and_1Phase_IM.md)
