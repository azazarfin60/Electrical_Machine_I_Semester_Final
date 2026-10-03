[← T-20: Speed Control & Braking](T-20_Speed_Control_and_Braking.md) | [🏠 Index](README.md) | [T-22: 1-Phase IM Theory (DFRT) →](T-22_Single-Phase_IM_Theory_DFRT.md)

---

# T-21: Induction Generator

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Induction Generator** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-21: Induction Generator — Theory, Operation, and Sizing

*Appears in: 2018 Q5(c), 2023 Q8(b), 2024 Q8(b), 2024 Q8(c)*

#### Why an induction machine can generate

At slip $s < 0$ (rotor spinning faster than synchronous speed $N > N_s$), the direction of relative motion between the stator field and rotor conductors reverses. Consequently:
- Rotor induced EMF $sE_2$ reverses phase.
- Rotor current $I_2$ reverses phase.
- The developed electromagnetic torque reverses direction, acting as a counter-torque that opposes rotation.

Instead of the stator driving the rotor, an external prime mover (engine, turbine) drives the rotor above $N_s$. The machine now converts mechanical power from the shaft into electrical power delivered out through the stator.

#### Reactive power must be supplied externally

An induction generator cannot self-excite using real power alone; it requires leading reactive power (VARs) to establish and maintain its rotating magnetic field:
- **Grid-connected mode:** The AC mains supply sets the terminal voltage and frequency and automatically delivers the required magnetizing VARs.
- **Self-excited (islanded) mode:** A capacitor bank connected across the stator terminals supplies the necessary leading reactive current. Residual magnetism in the rotor initiates voltage build-up until the capacitor volt-ampere characteristic intersects the core saturation curve.

![Self-excited induction generator circuit with terminal capacitors](../Books/Theraja/Ch-34/diagrams/Ch-34_p34_fig31.jpg)
![Induction generator torque-slip curve in generating region (slip < 0)](../Books/Theraja/Ch-34/diagrams/Ch-34_p33_fig30.jpg)

---

### [2018 Q5(c) / 2024 Q8(c)]: Worked Numerical Problem — Capacitance and Engine Speed

> 📋 **Appeared in:** 2018 Q5(c), 2024 Q8(c) *(Verbatim repeat)*

**Problem:** A 440V, 4-pole, 1470 rpm, 30-kW, 3-$\varphi$ IM is to be used as IG. The rated current of the motor is 40A and full-load power factor is 85%. Calculate:
(i) Capacitance required per phase if capacitors are connected in delta.
(ii) Speed of the driving engine for generating a frequency of 50 Hz.

#### Step-by-Step Solution

**Given:**
- Line voltage $V_L = 440\text{ V}$
- Poles $P = 4$, frequency $f = 50\text{ Hz}$
- Rated motor speed $N = 1470\text{ rpm}$
- Rated current $I_L = 40\text{ A}$
- Power factor $\cos\phi = 0.85 \implies \sin\phi = \sqrt{1 - 0.85^2} = \sqrt{0.2775} = 0.5268$

**Step 0: Synchronous speed**
$$N_s = \frac{120 f}{P} = \frac{120 \times 50}{4} = \mathbf{1500\text{ rpm}}$$

#### (i) Capacitance required per phase ($\Delta$-connected)

1. **Total reactive power required by the machine:**
   $$Q = \sqrt{3}\,V_L I_L \sin\phi = \sqrt{3} \times 440 \times 40 \times 0.5268 \approx \mathbf{16,058.5\text{ VAR}} \quad (\approx 16.06\text{ kVAR})$$
   *(Using rounded $\sqrt{3} \approx 1.732$ and $\sin\phi \approx 0.527$ gives $16,082\text{ VAR}$).*

2. **Reactive power per phase:**
   $$Q_{\text{ph}} = \frac{Q}{3} = \frac{16058.5}{3} = \mathbf{5352.8\text{ VAR}}$$

3. **Capacitive reactance per phase in delta:**
   In delta connection, each capacitor experiences full line voltage: $V_{C,\text{ph}} = V_L = 440\text{ V}$.
   $$Q_{\text{ph}} = \frac{V_{C,\text{ph}}^2}{X_C} \implies X_C = \frac{440^2}{5352.8} = \frac{193600}{5352.8} = \mathbf{36.17\ \Omega}$$

4. **Capacitance per phase:**
   $$C = \frac{1}{2\pi f X_C} = \frac{1}{2\pi \times 50 \times 36.17} = \frac{1}{11362.4}\text{ F} = \mathbf{88.01\ \mu\text{F}}$$
   *(Using intermediate rounded values $X_C = 36.11\ \Omega$ yields $C = \mathbf{88.15\ \mu\text{F}} \approx \mathbf{88.2\ \mu\text{F}}$).*

$$\boxed{C \approx 88.0\text{ to } 88.2\ \mu\text{F per phase}\;(\Delta\text{-connected})}$$

#### (ii) Speed of the driving engine for generating 50 Hz

1. **Motoring slip at rated speed:**
   $$s_{\text{mot}} = \frac{N_s - N}{N_s} = \frac{1500 - 1470}{1500} = \frac{30}{1500} = \mathbf{0.02} \quad (2\%)$$

2. **Generator operating slip:**
   To generate rated electrical power at 50 Hz, the rotor must be driven above synchronous speed with equal slip magnitude:
   $$s_{\text{gen}} = -0.02$$

3. **Required engine speed:**
   $$N_{\text{engine}} = N_s(1 - s_{\text{gen}}) = 1500 \times [1 - (-0.02)] = 1500 \times 1.02 = \mathbf{1530\text{ rpm}}$$

$$\boxed{N_{\text{engine}} = 1530\text{ rpm}}$$

---

[← T-20: Speed Control & Braking](T-20_Speed_Control_and_Braking.md) | [🏠 Index](README.md) | [T-22: 1-Phase IM Theory (DFRT) →](T-22_Single-Phase_IM_Theory_DFRT.md)
