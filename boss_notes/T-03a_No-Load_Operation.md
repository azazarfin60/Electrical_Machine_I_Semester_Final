[← T-02: Construction](T-02_Construction.md) | [🏠 Index](00_Index.md) | [T-03b: Phasor Diagrams Under Load →](T-03b_Phasor_Diagrams_Under_Load.md)

---

# T-03a: No-Load Operation
> **Section:** A | **Priority:** 🟠 HIGH | **Exam Frequency:** 3/7 years
> **Sources:** Theraja Ch-32 (Art. 32.6–32.9), VK Mehta Ch-7 (Art. 7.4–7.6), Slides L-09 S04–S08

## Why This Topic Matters

No-load operation is tested in 4/7 papers (2019, 2020, 2023, 2024). It appears as "explain no-load operation with phasor diagram" (3-6 marks) or as a numerical where you decompose $I_0$ into its components. Understanding no-load current is also the foundation for the OC test (T-06a) and the shunt branch of the equivalent circuit (T-04). The 2024 paper used the 220V/110V, 0.5 A, 30 W data again in Q3(c), but this time it also gave $R_1 = 0.6\ \Omega$ and asked for four things, so the iron loss came out as 29.85 W rather than 30 W.

---

## 📝 Key Definitions

> **No-load current ($I_0$):** "When the primary of a transformer is connected to the supply and the secondary is open, the transformer is on no-load. The small current $I_0$ taken by the primary under no-load conditions is called no-load current." — VK Mehta, Art. 7.6. It is typically 2–10% of rated current.

> **Magnetizing current ($I_\mu$ or $I_m$):** "The component $I_\mu$ of $I_0$ which establishes the alternating flux $\Phi_m$ in the core is called the magnetizing current. It is in phase with the flux $\Phi_m$ and lags $V_1$ by 90°." — VK Mehta, Art. 7.6

> **Core-loss current ($I_w$ or $I_c$):** "The component $I_w$ of $I_0$ which supplies the iron losses (hysteresis + eddy current) is called the active or working or iron-loss component. It is in phase with $V_1$." — VK Mehta, Art. 7.6

---

## What Happens at No-Load

When you apply $V_1$ to the primary and leave the secondary open ($I_2 = 0$):

1. A small no-load current $I_0$ flows in the primary.
2. This current does two jobs:
   - **Magnetic job:** The magnetizing component $I_\mu$ sets up the alternating core flux $\Phi_m$.
   - **Thermal job:** The core-loss component $I_w$ supplies power for hysteresis and eddy current losses.
3. The flux $\Phi_m$ induces EMFs in both windings: $E_1 = 4.44 f N_1 \Phi_m$ and $E_2 = 4.44 f N_2 \Phi_m$.
4. Since the secondary is open, no current flows there. $V_2 = E_2$.

---

## No-Load Current Components

The no-load current $I_0$ splits into two perpendicular components:

$$I_0 = \sqrt{I_w^2 + I_\mu^2}$$

where:

- $I_w = I_0 \cos\phi_0$ (active component, in phase with $V_1$)
- $I_\mu = I_0 \sin\phi_0$ (reactive component, 90° lagging from $V_1$)

The no-load power factor is very low (0.1–0.3) because $I_\mu \gg I_w$. The magnetizing current dominates.

**No-load power input:**

$$W_0 = V_1 I_0 \cos\phi_0 = V_1 I_w$$

This power equals the iron loss (core loss) because copper loss at no-load is negligible ($I_0$ is tiny, so $I_0^2 R_1 \approx 0$).

$$\cos\phi_0 = \frac{W_0}{V_1 I_0}$$

---

## No-Load Phasor Diagram

![No-load phasor diagram showing flux, EMFs, and current components](diagrams/transformer_no_load_phasor.jpg)

**Step-by-step construction:**

1. Draw $\vec{\Phi}_m$ as the reference (horizontal, pointing right).
2. $\vec{E}_1$ and $\vec{E}_2$ lag $\Phi_m$ by 90° (pointing downward). The induced EMF is maximum when flux passes through zero.
3. $\vec{V}_1 = -\vec{E}_1$ (pointing upward). The applied voltage must balance the back-EMF.
4. $I_w$ is in phase with $V_1$ (pointing upward). It supplies real power for core losses.
5. $I_\mu$ lags $V_1$ by 90°. It points in the same direction as $\Phi_m$ (horizontal right). This makes sense: the magnetizing current creates the flux, so they are in phase.
6. $\vec{I}_0 = \vec{I}_w + \vec{I}_\mu$ (phasor sum). The angle between $V_1$ and $I_0$ is $\phi_0$.
7. Since secondary is open: $V_2 = E_2$ (no drops).

---

## Why Primary Current Increases with Load

When you connect a load and secondary current $I_2$ flows:

1. $I_2$ through $N_2$ turns creates a demagnetizing MMF = $N_2 I_2$.
2. This tends to reduce the core flux.
3. But $V_1$ is fixed by the supply. Since $V_1 \approx E_1 = 4.44 f N_1 \Phi_m$, the flux **must** stay constant.
4. The primary draws additional current $I_2'$ to cancel the secondary MMF:

$$N_1 I_1 = N_1 I_0 + N_2 I_2$$

$$I_1 = I_0 + \frac{N_2}{N_1} I_2 = I_0 + I_2'$$

"The increased primary current brings in more energy from the supply to match the energy delivered to the load. The transformer does not generate energy: it regulates primary current to always match the secondary load." — From explanation notes

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Explain the no-load operation of a 1-phase transformer with a neat phasor diagram.
> **Appeared:** 2020 Q1(c) — 3 marks

**Full Answer:**

When a transformer primary is connected to AC supply with secondary open-circuited, a small no-load current $I_0$ flows (2–10% of rated current). This current has two components:

**1. Magnetizing current ($I_\mu$):** This component establishes the alternating mutual flux $\Phi_m$ in the core. It is purely reactive and lags the applied voltage $V_1$ by 90°. It is in phase with the flux $\Phi_m$. It does no real work — it simply oscillates the magnetic field back and forth.

**2. Core-loss (active) current ($I_w$):** The core heats up due to hysteresis and eddy current losses. These losses require real power input. $I_w$ is in phase with $V_1$ and supplies this power.

The total no-load current is the phasor sum:

$$I_0 = \sqrt{I_w^2 + I_\mu^2}$$

The no-load power factor is very low ($\cos\phi_0 = 0.1$ to $0.3$) because $I_\mu \gg I_w$.

No-load power input: $W_0 = V_1 I_0 \cos\phi_0 = V_1 I_w = P_{\text{iron}}$ (copper loss is negligible)

**Phasor Diagram Construction:**

![No-load phasor diagram](diagrams/transformer_no_load_phasor.jpg)

1. Draw $\vec{\Phi}_m$ horizontal as reference.
2. $\vec{E}_1$, $\vec{E}_2$ lag $\Phi_m$ by 90° (downward). By Faraday's law: $e = -N\,d\Phi/dt$, so EMF is maximum when flux passes through zero.
3. $\vec{V}_1 = -\vec{E}_1$ (upward). Applied voltage balances the back-EMF.
4. $I_w$ is in phase with $V_1$ (upward).
5. $I_\mu$ is in phase with $\Phi_m$ (horizontal right). Lags $V_1$ by 90°.
6. $\vec{I}_0 = \vec{I}_w + \vec{I}_\mu$ at angle $\phi_0$ from $V_1$.
7. Since secondary is open: $V_2 = E_2$ (no load drops).

---

### 🎯 Q2: When a power transformer is excited as shown in the figure, describe the induced voltage phenomena.
> **Appeared:** 2024 Q1(b) — 4 marks

**Full Answer:**

![Transformer Excitation and Induced Voltage Phenomena](../PrevYearQuestions/diagrams/2024_q1b_transformer.png)

**Read the figure first.** A rectangular closed ferromagnetic core has two limbs. Coil1 ($N_1$ turns) sits on the left limb and is fed from a **DC source through a single-pole switch**. Coil2 ($N_2$ turns) sits on the right limb and drives a resistive load $R$. Both windings are linked by the mutual flux $\Phi_{mutual}$.

**Because the source is DC, this is a switching transient, not steady-state AC.** That is why Faraday's and Lenz's laws in their raw differential form are the right tool here rather than the phasor emf equation.

**The chain of events on closing the switch:**

1. **Closing the switch** applies $v$ to coil1 and starts the primary current $i_1$ flowing into the upper winding terminal.
2. **Flux builds up.** $i_1$ magnetises the core, so $\Phi_{mutual}$ rises from its residual value.
3. **Self-induction in coil1.** The primary itself develops a counter-EMF opposing the applied voltage:
   $$e_1 = -N_1 \frac{d\Phi}{dt}$$
4. **Mutual induction in coil2.** The same $\Phi_{mutual}$ links all $N_2$ turns of coil2, so it too develops an EMF:
   $$e_2 = -N_2 \frac{d\Phi}{dt}$$
5. **Load current.** $e_2$ drives $i_2$ out of the upper terminal into the load $R$.
6. **Secondary reaction flux opposes $d\Phi/dt$.** By Lenz's law the secondary current creates a flux that opposes the build-up of core flux. This is the same m.m.f. balance that later keeps the core flux constant in a working transformer.

**Ratio to state at the end:** $E_2/E_1 = N_2/N_1$, and both induced EMFs lag the flux by $90°$.

---

### 🎯 Q3: No-load test data: 220V/110V, $I_0$ = 0.5 A, 30 W, primary resistance $R_1 = 0.6\ \Omega$. Find the turn ratio, magnetizing and working components, and the iron loss.
> **Appeared:** 2020 Q2(d) — 3 marks; 2024 Q3(c) — 4 marks

**Full Answer:**

Given: $R_1 = 0.6\ \Omega$; $V_1 = 220$ V; $V_2 = 110$ V; $I_0 = 0.5$ A; $W_0 = 30$ W.

**(i) Turn ratio**
$$a = \frac{V_1}{V_2} = \frac{220}{110} = \boxed{2}$$

**No-load power factor:**
$$\cos\phi_0 = \frac{W_0}{V_1 I_0} = \frac{30}{220 \times 0.5} = \frac{30}{110} = 0.2727$$
$$\phi_0 = \cos^{-1}(0.2727) = 74.17°$$

**(ii) Magnetizing (reactive) component:**
$$I_\mu = I_0 \sin\phi_0 = 0.5 \times \sin(74.17°) = 0.5 \times 0.9621 = \boxed{0.481\text{ A}}$$

**(iii) Working (core-loss) component:**
$$I_w = I_0 \cos\phi_0 = 0.5 \times 0.2727 = \boxed{0.1364\text{ A}}$$

**(iv) Iron loss.** The wattmeter reads power **input**, which is the iron loss plus the small primary copper loss. This is why the 2024 paper supplies $R_1$:
$$P_{core} = W_0 - I_0^2 R_1 = 30 - (0.5^2 \times 0.6) = 30 - 0.15 = \boxed{29.85\text{ W}}$$

> [!NOTE] 30 W vs 29.85 W
> If the question does not give $R_1$ (as in 2020 Q2(d)), the answer is simply 30 W. When $R_1$ is given, the intended answer is 29.85 W. State the correction and mention that 30 W is the usual approximation.

**Check:** $I_0 = \sqrt{0.1364^2 + 0.481^2} = \sqrt{0.0186 + 0.2314} = 0.5$ A ✓

Note that $I_\mu \gg I_w$. The no-load current is mostly magnetizing.

---

### 🎯 Q4: Magnetizing and iron-loss components of no-load current: (i) 2200/200 V, $I_0 = 0.6$ A, 400 W; (ii) 2200/250 V, 0.5 A at 0.3 pf on open circuit.
> **Appeared:** 2024 Q1(c) — 4 marks

**Full Answer:**

$I_0 = \sqrt{I_w^2 + I_\mu^2}$, with $I_w = I_0\cos\phi_0$ and $I_\mu = I_0\sin\phi_0$.

**(i) 2200/200 V, $I_0 = 0.6$ A, 400 W absorbed**
$$\cos\phi_0 = \frac{400}{2200 \times 0.6} = 0.30303$$
$$I_w = 0.6 \times 0.30303 = \boxed{0.182\text{ A}}, \qquad I_\mu = \sqrt{0.6^2 - 0.1818^2} = \boxed{0.572\text{ A}}$$

**(ii) 2200/250 V, 0.5 A at 0.3 pf**
$$I_w = 0.5 \times 0.3 = \boxed{0.15\text{ A}}, \qquad I_\mu = \sqrt{0.5^2 - 0.15^2} = \boxed{0.477\text{ A}}$$

> [!NOTE] Label clearly which is which
> The paper asks for magnetizing first in part (i) and "magnetizing and working" in part (ii). Both parts need the same pair, so state which value is $I_\mu$ and which is $I_w$ every time.

---

### 🎯 Q5: Justify: "The magnetizing current of power transformer is not fully sinusoidal."
> **Appeared:** 2024 Q2(a) — 2 marks

**Full Answer:**

The core flux $\Phi_m$ is forced to be nearly sinusoidal because it is linked to a sinusoidal applied voltage through the emf equation $V_1 \approx 4.44 f N_1 \Phi_m$. But the magnetizing current $I_m$ is whatever current the core needs to sustain that flux.

**A saturating core is a non-linear element.** Its flux-current relation $\Phi = f(I_m)$ is not linear, so the current that produces a sinusoidal flux must itself be **peaked and distorted**, with a third-harmonic component. The sharper the saturation knee, the more pronounced the peak.

**Where the harmonic goes.** Three-phase core-type transformers are built so the third-harmonic magnetizing currents circulate in the delta of the three limbs, which suppresses third-harmonic voltages in the phase windings. Star-connected windings without a delta path cannot carry them, and the third-harmonic flux then appears as a third-harmonic voltage. That is the standard reason a power transformer uses a delta tertiary.

---

### 🎯 Q3: Why does primary current increase as secondary load increases?
> **Appeared:** 2019 Q1(c) — 4 marks

**Full Answer:**

An ideal transformer maintains the core flux $\Phi_m$ at a constant value set by the supply voltage: $\Phi_m \approx V_1/(4.44 f N_1)$. This flux requires a certain MMF to sustain it.

At no-load, the primary alone provides all the required MMF: $N_1 I_0 = \text{const}$.

When a load draws secondary current $I_2$, the secondary winding (with $N_2$ turns) creates a demagnetizing MMF $= N_2 I_2$. This tends to reduce the core flux.

But $V_1$ is fixed by the supply. Since $V_1 \approx E_1 = 4.44 f N_1 \Phi_m$, the flux **cannot** change (it is locked to the supply voltage). Therefore, the primary current must increase to cancel the secondary demagnetization:

$$N_1 I_1 - N_2 I_2 = N_1 I_0 \approx \text{const}$$

$$N_1 I_1 = N_1 I_0 + N_2 I_2$$

$$I_1 = I_0 + \frac{N_2}{N_1} I_2 = I_0 + I_2'$$

As $I_2$ increases (more load), $I_1$ increases proportionally. The increased primary current brings in more energy from the supply to match the energy delivered to the load. The transformer does not generate energy; it acts as an automatic current regulator that adjusts $I_1$ to always balance the secondary MMF.

---

## Exam Variants

| Year | Question | Data Given | Key Answer |
|:---|:---|:---|:---|
| 2020 Q1(c) | Explain no-load with sketch | Conceptual | Phasor diagram + components |
| 2020 Q2(d) | Find $I_\mu$, $I_w$ | 220V/110V, $I_0 = 0.5$ A, $W_0 = 30$ W | $I_w = 0.136$ A, $I_\mu = 0.481$ A |
| 2024 Q1(b) | Induced voltage on switching the DC-excited figure | Conceptual, 4 marks | Faraday/Lenz transient chain |
| 2024 Q1(c) | $I_m$, $I_w$ from watt data | 2200/200 V, 0.6 A, 400 W; and 2200/250 V, 0.5 A, 0.3 pf | 0.572/0.182 A and 0.477/0.15 A |
| 2024 Q2(a) | Magnetizing current non-sinusoidal | Conceptual, 2 marks | Core saturation is non-linear |
| 2024 Q3(c) | OC test, 4 quantities | 220V/110V, 0.5 A, 30 W, $R_1 = 0.6\,\Omega$ | $a = 2$, $I_m = 0.481$ A, $I_w = 0.1364$ A, $P_{core} = 29.85$ W |
| 2019 Q1(c) | Why does $I_1$ increase with load? | Conceptual | MMF balance argument |

---

## ⚡ Exam Tips & Common Mistakes

1. **$I_\mu$ is the bigger component.** Students often swap $I_w$ and $I_\mu$. Remember: most of the no-load current goes into creating flux ($I_\mu$), not into losses ($I_w$). The no-load pf is low (0.1–0.3).
2. **No-load power = iron loss only.** Copper loss at no-load is negligible because $I_0$ is tiny. So $W_0 = P_{\text{iron}}$.
3. **The phasor diagram uses $\Phi_m$ as reference, not $V_1$.** Start with flux horizontal. Everything else follows from there.
4. **The 220V/110V, 0.5A, 30W numerical is a guaranteed repeat.** Memorize the answers.

## 🔗 Related Topics

- [T-01: Fundamentals](T-01_Transformer_Fundamentals.md) — EMF equation that determines the flux
- [T-03b: Phasor Under Load](T-03b_Phasor_Diagrams_Under_Load.md) — Adding load to the no-load diagram
- [T-04: Equivalent Circuit](T-04_Equivalent_Circuit.md) — $R_0$ and $X_0$ come from no-load data
- [T-06a: OC Test](T-06a_OC_Test.md) — The OC test IS the no-load test

---

[← T-02: Construction](T-02_Construction.md) | [🏠 Index](00_Index.md) | [T-03b: Phasor Diagrams Under Load →](T-03b_Phasor_Diagrams_Under_Load.md)
