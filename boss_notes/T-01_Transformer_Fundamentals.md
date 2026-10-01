[← T-00: Core Fundamentals](T-00_Core_Fundamentals.md) | [🏠 Index](00_Index.md) | [T-02: Construction →](T-02_Construction.md)

---

# T-01: Transformer Fundamentals & EMF Equation
> **Section:** A | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-32 (Art. 32.1–32.5), VK Mehta Ch-7 (Art. 7.1–7.3), Slides L-08

## Why This Topic Matters

The EMF equation $E = 4.44 f N \Phi_m$ appeared in 4 out of 7 papers (2019, 2021, 2023, 2024). It is the foundation for every transformer calculation. Questions range from "derive the EMF equation" (3–6 marks) to numericals asking you to find turns, flux, or voltages. If you know this derivation cold, you also understand the working principle of every AC machine.

---

## 📝 Key Definitions

> **Transformer:** "A transformer is a static (or stationary) piece of apparatus by means of which electric power in one circuit is transformed into electric power of the same frequency in another circuit. It can raise or lower the voltage in a circuit but with a corresponding decrease or increase in current. The physical basis of a transformer is mutual induction between two circuits linked by a common magnetic flux." — Theraja, Art. 32.1

> **Voltage Transformation Ratio ($K$):** "The constant $K = E_2/E_1 = N_2/N_1$ is known as voltage transformation ratio. If $N_2 > N_1$ i.e. $K > 1$, the transformer is called a step-up transformer. If $N_2 < N_1$ i.e. $K < 1$, it is called a step-down transformer." — Theraja, Art. 32.7

> **Ideal Transformer:** "An ideal transformer is one that has (1) no winding resistance, so there is no ohmic voltage drop and no copper loss; (2) no magnetic leakage flux, so all flux links both windings; (3) no core/iron loss, meaning the core has infinite permeability and zero hysteresis and eddy-current losses. Although an ideal transformer cannot be physically realized, its study provides a very powerful tool in the analysis of a practical transformer." — VK Mehta, Art. 7.2

---

## How a Transformer Works

A transformer has two windings (primary and secondary) wound on a common iron core. There is no electrical connection between them. Energy transfers through the magnetic field.

![Principle of transformer: step-up and step-down configurations](diagrams/transformer_principle_mutual_induction.jpg)

**Step 1: Apply AC voltage to the primary.** When you connect the primary ($N_1$ turns) to an AC supply $V_1$, a small current flows. This current creates an alternating magnetic flux $\Phi$ in the iron core.

**Step 2: Flux induces EMF in both windings.** By Faraday's law, the changing flux induces an EMF in every coil it passes through:

$$e_1 = -N_1 \frac{d\Phi}{dt}, \qquad e_2 = -N_2 \frac{d\Phi}{dt}$$

The ratio of EMFs equals the turns ratio:

$$\frac{E_1}{E_2} = \frac{N_1}{N_2}$$

**Step 3: Load draws current.** When a load connects to the secondary, current $I_2$ flows. This current tries to reduce the core flux (Lenz's law). But the supply voltage forces the flux to stay constant. So the primary draws more current $I_1$ to compensate.

**Step 4: Power is conserved.** For an ideal transformer: $V_1 I_1 = V_2 I_2$. The transformer changes the voltage-current ratio while keeping power constant.

The following points (from VK Mehta, Art. 7.1) should be noted:
1. Transformer action is based on mutual induction between two circuits linked by a common magnetic flux.
2. The frequency of induced EMF is the same as that of the applied voltage.
3. The two windings are not electrically connected; they are magnetically coupled.
4. Electrical power is transferred from primary to secondary with negligible loss.

---

## Ideal Transformer Properties

An ideal transformer assumes (Theraja, Art. 32.5):

1. **Zero winding resistance** ($R_1 = R_2 = 0$). No $I^2R$ losses and no ohmic voltage drop.
2. **Zero leakage flux.** All flux produced by primary links the secondary. No leakage reactance.
3. **Zero core losses.** Core has infinite permeability. No hysteresis or eddy current losses. Magnetizing current $I_\mu \approx 0$.

"It may be noted that it is impossible to realize such a transformer in practice, yet for convenience, we start with such a transformer and step by step approach an actual transformer." — Theraja

Key relationships for an ideal transformer:

$$\frac{V_1}{V_2} = \frac{N_1}{N_2} = \frac{I_2}{I_1} = a$$

where $a = N_1/N_2$ is the turns ratio.

---

## EMF Equation Derivation

This is the most important derivation in the transformer chapter. Two methods exist. Know both.

### Method 1: Calculus Method (Primary)

**Step 1:** Write the flux waveform. The core flux is sinusoidal:

$$\Phi(t) = \Phi_m \sin(2\pi f t)$$

where $\Phi_m$ is the peak flux in webers and $f$ is frequency in Hz.

**Step 2:** Apply Faraday's law for a winding of $N_1$ turns:

$$e_1(t) = -N_1 \frac{d\Phi}{dt} = -N_1 \cdot 2\pi f \Phi_m \cos(2\pi f t)$$

Since $-\cos\theta = \sin(\theta - 90°)$:

$$e_1(t) = N_1 \cdot 2\pi f \Phi_m \sin(2\pi f t - 90°)$$

This tells us the EMF **lags** the flux by 90°. When flux is at its peak, the rate of change is zero, so EMF is zero at that instant.

![Sinusoidal flux waveform and induced EMF lagging by 90°](diagrams/transformer_flux_emf_waveform.jpg)

**Step 3:** Find the peak EMF:

$$E_{m1} = 2\pi f N_1 \Phi_m$$

**Step 4:** Convert to RMS. For a sine wave, RMS = peak/$\sqrt{2}$:

$$E_1 = \frac{2\pi f N_1 \Phi_m}{\sqrt{2}} = \sqrt{2}\pi f N_1 \Phi_m$$

**Step 5:** Compute the constant:

$$\sqrt{2}\pi = 1.4142 \times 3.1416 = 4.443 \approx 4.44$$

$$\boxed{E_1 = 4.44 f N_1 \Phi_m}$$

The same flux links the secondary ($N_2$ turns):

$$\boxed{E_2 = 4.44 f N_2 \Phi_m}$$

### Method 2: Form Factor Method (Theraja, Art. 32.6)

"Flux increases from its zero value to maximum value $\Phi_m$ in one quarter of the cycle i.e. in $1/4f$ second." — Theraja

$$\text{Average rate of change of flux} = \frac{\Phi_m}{1/(4f)} = 4f\Phi_m \text{ Wb/s (= volt/turn)}$$

For a sine wave, the form factor (ratio of RMS to average of full-wave rectified value):

$$K_f = \frac{\text{RMS value}}{\text{Average value}} = 1.11$$

RMS EMF per turn $= 1.11 \times 4f\Phi_m = 4.44 f \Phi_m$

Multiply by turns: $E_1 = 4.44 f N_1 \Phi_m$ ✓

> [!TIP]
> The form factor method is faster to write in an exam. The calculus method is more rigorous. Use whichever the question asks for. If it says "derive," the calculus method is safer.

---

## Transformation Ratio

Dividing the two EMF equations (Theraja, Art. 32.7):

$$\frac{E_2}{E_1} = \frac{N_2}{N_1} = K$$

For an ideal transformer ($V_1 \approx E_1$, $V_2 \approx E_2$):

$$\frac{V_2}{V_1} = \frac{N_2}{N_1} = K$$

From power conservation ($V_1 I_1 = V_2 I_2$):

$$\frac{I_1}{I_2} = \frac{V_2}{V_1} = K$$

"Hence, currents are in the inverse ratio of the (voltage) transformation ratio." — Theraja

| Transformer Type | Condition | Effect |
|:---|:---|:---|
| Step-up | $K > 1$ ($N_2 > N_1$) | Voltage increases, current decreases |
| Step-down | $K < 1$ ($N_2 < N_1$) | Voltage decreases, current increases |

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Derive the transformer EMF equation under assumptions of constant permeability and no leakage flux.
> **Appeared:** 2019 Q1(b), 2021 Q1(b), 2023 Q1(b), 2024 Q4(a) — (3–6 marks)

**Full Answer:**

Let $N_1$ = primary turns, $N_2$ = secondary turns, $\Phi_m$ = peak flux (Wb), $f$ = frequency (Hz).

The core flux is sinusoidal: $\Phi(t) = \Phi_m \sin(\omega t)$ where $\omega = 2\pi f$.

By Faraday's law, instantaneous EMF induced in primary:

$$e_1 = -N_1 \frac{d\Phi}{dt} = -N_1 \omega \Phi_m \cos(\omega t) = N_1 \omega \Phi_m \sin(\omega t - 90°)$$

Peak EMF: $E_{m1} = 2\pi f N_1 \Phi_m$

RMS EMF: $E_1 = E_{m1}/\sqrt{2} = 2\pi f N_1 \Phi_m / \sqrt{2}$

$$\boxed{E_1 = 4.44 f N_1 \Phi_m}$$

Similarly: $\boxed{E_2 = 4.44 f N_2 \Phi_m}$

The EMF per turn is the same in both windings: $E_1/N_1 = E_2/N_2 = 4.44 f \Phi_m$

Also: $E_1/E_2 = N_1/N_2 = K$ (voltage transformation ratio).

---

### 🎯 Q2: What are the characteristics of an ideal transformer?
> **Appeared:** 2021 Q1(a), 2024 Q1(a) — (3–6 marks)

**Full Answer:**

An ideal transformer is one which has no losses (Theraja, Art. 32.5). It has:

1. **No winding resistance** ($R_1 = R_2 = 0$): No ohmic voltage drop ($IR = 0$) and no copper loss ($I^2R = 0$).
2. **No magnetic leakage flux**: All the flux produced by the primary links the secondary winding completely. There is no leakage flux. Hence leakage reactances are zero ($X_1 = X_2 = 0$).
3. **No core (iron) losses**: The core has infinite permeability, so the magnetizing current needed to establish flux is zero ($I_\mu = 0$). Hysteresis and eddy current losses are zero.

For such a transformer:
- Input VA = Output VA: $V_1 I_1 = V_2 I_2$
- Voltage ratio = Turns ratio: $V_1/V_2 = N_1/N_2 = a$
- Current ratio = Inverse turns ratio: $I_1/I_2 = N_2/N_1 = 1/a$
- Efficiency = 100%

"It is impossible to realize such a transformer in practice, yet for convenience we start with such a transformer and step by step approach an actual transformer." — Theraja

---

### 🎯 Q3: Show the schematic of a 1-φ transformer. Identify and label all variables on both sides.
> **Appeared:** 2023 Q1(a), 2024 Q1(a) — (6 marks)

**Full Answer:**

Draw a transformer with a laminated iron core and two windings:

**Primary side (left):**
- Applied voltage $V_1$ from AC supply
- Primary current $I_1$ entering the dot terminal
- $N_1$ turns on the primary winding
- Self-induced EMF $E_1$ (opposing $V_1$)

**Core (center):**
- Alternating mutual flux $\Phi(t) = \Phi_m \sin\omega t$ flowing through the laminated iron core

**Secondary side (right):**
- $N_2$ turns on the secondary winding
- Mutually induced EMF $E_2$
- Secondary current $I_2$ (flows when load $Z_L$ is connected)
- Terminal voltage $V_2$ across the load

**Key relationships to state:**
- $E_1/E_2 = N_1/N_2$ (EMF ratio = turns ratio)
- $V_1 I_1 = V_2 I_2$ (power conservation for ideal case)
- $K = N_2/N_1$ (transformation ratio)
- If $K > 1$: step-up; if $K < 1$: step-down

![Principle of transformer with labeled variables](diagrams/transformer_principle_mutual_induction.jpg)

---

### 🎯 Q4: 25 kVA transformer, 500/50 turns, 3000V/50Hz. Find full-load currents, secondary EMF, max flux.
> **Appeared:** 2021 Q1(c) — 4 marks

**Full Answer:**

Given: $S = 25$ kVA, $N_1 = 500$, $N_2 = 50$, $V_1 = 3000$ V, $f = 50$ Hz.

**Turns ratio:** $a = N_1/N_2 = 500/50 = 10$

**Secondary EMF:** $E_2 = V_1/a = 3000/10 = \boxed{300 \text{ V}}$

**Full-load currents:**

$$I_1 = \frac{S}{V_1} = \frac{25000}{3000} = \boxed{8.33 \text{ A}}$$

$$I_2 = \frac{S}{V_2} = \frac{25000}{300} = \boxed{83.3 \text{ A}}$$

**Maximum flux** (from EMF equation, $E_1 \approx V_1$):

$$\Phi_m = \frac{E_1}{4.44 f N_1} = \frac{3000}{4.44 \times 50 \times 500} = \frac{3000}{111000} = \boxed{27.03 \text{ mWb}}$$

Check: $E_2 = 4.44 \times 50 \times 50 \times 0.02703 = 300$ V ✓

---

### 🎯 Q5: 50 Hz, 6.6 kV/400V transformer. Core cross-section = 25 cm², max flux density = 1.2 T. Find number of turns on each side.
> **Appeared:** 2024 Q4(b) — 3 marks

**Full Answer:**

Given: $f = 50$ Hz, $V_1 = 6600$ V, $V_2 = 400$ V, $A = 25$ cm² $= 25 \times 10^{-4}$ m², $B_m = 1.2$ T.

**Maximum flux:**

$$\Phi_m = B_m \times A = 1.2 \times 25 \times 10^{-4} = 3 \times 10^{-3} \text{ Wb}$$

**Primary turns** (from EMF equation):

$$N_1 = \frac{E_1}{4.44 f \Phi_m} = \frac{6600}{4.44 \times 50 \times 3 \times 10^{-3}} = \frac{6600}{0.666} = \boxed{9910 \text{ turns}}$$

**Secondary turns:**

$$N_2 = \frac{E_2}{4.44 f \Phi_m} = \frac{400}{0.666} = \boxed{600 \text{ turns}}$$

Check: $N_1/N_2 = 9910/600 = 16.5 = V_1/V_2 = 6600/400 = 16.5$ ✓

---

## Exam Variants

| Year | Question | Data Given | Key Answer |
|:---|:---|:---|:---|
| 2021 Q1(c) | Find currents, EMF, flux | 25 kVA, 500/50 turns, 3000V/50Hz | $\Phi_m = 27.03$ mWb |
| 2024 Q4(b) | Find number of turns | 50Hz, 6.6kV/400V, $A = 25$ cm², $B_m = 1.2$ T | $N_1 = 9910$, $N_2 = 600$ |
| 2019 Q1(b) | Derive EMF equation | — | $E = 4.44 f N \Phi_m$ |
| 2023 Q1(b) | Derive EMF equation | — | Same derivation |

---

## ⚡ Exam Tips & Common Mistakes

1. **Don't confuse $K$ and $a$.** $K = N_2/N_1$ (transformation ratio, Theraja convention). $a = N_1/N_2$ (turns ratio). They are reciprocals. Use whichever the question defines. If not defined, state your convention.
2. **EMF equation uses peak flux $\Phi_m$, not RMS.** A common error is plugging in RMS flux values.
3. **Frequency must be in Hz, not rad/s.** The 4.44 constant already includes $2\pi/\sqrt{2}$.
4. **Show every step in the derivation.** Don't jump from Faraday's law to the final answer. The intermediate steps ($-\cos\theta$ to $\sin(\theta - 90°)$, peak to RMS conversion) carry marks.
5. **Cross-check with turns ratio.** After finding $N_1$ and $N_2$, verify $N_1/N_2 \approx V_1/V_2$.

## 🔗 Related Topics

- [T-02: Construction](T-02_Construction.md) — Core types and lamination
- [T-03a: No-Load Operation](T-03a_No-Load_Operation.md) — What happens when secondary is open
- [T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) — Building on the ideal model
- [T-06a: OC Test](T-06a_OC_Test.md) — Uses EMF equation to find core parameters

---

[← T-00: Core Fundamentals](T-00_Core_Fundamentals.md) | [🏠 Index](00_Index.md) | [T-02: Construction →](T-02_Construction.md)
