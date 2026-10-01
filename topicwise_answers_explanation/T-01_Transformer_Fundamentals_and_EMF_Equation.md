*(start)* | [🏠 Index](README.md) | [T-02: Construction & Core →](T-02_Transformer_Construction_and_Core.md)

---

# T-01: Transformer Fundamentals & EMF Equation

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Transformer Fundamentals & EMF Equation** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-01: EMF Equation: $E = 4.44 f N \Phi_m$: Full Derivation and Intuition

*Appears in: 2019 Q1b, 2021 Q1b, 2023 Q1b, 2024 Q4a, CT-03 Q2*

#### Why the EMF equation matters

This equation is the fundamental design equation of every transformer, every motor, every generator. If you know the supply voltage, frequency, and how many turns you want to use, this equation tells you how much core flux you need, or how big the core cross-section must be.

#### Physical picture before the math

Imagine threading a loop of wire through a magnetic core. If the flux through that core changes, an EMF appears in the wire (Faraday's Law). The faster the flux changes, the bigger the EMF.

For an AC supply at frequency $f$, the flux changes from peak to zero in quarter of a cycle: a time of $T/4 = 1/(4f)$ seconds. The faster the frequency, the less time to change, the bigger the average rate of change, the bigger the average EMF.

This is why $f$ appears in the formula.

#### The two-step derivation

**Step 1: Write the flux waveform.**

The core of an ideal transformer operating from a sinusoidal supply carries a sinusoidal flux:
$$\Phi(t) = \Phi_m\sin(\omega t) = \Phi_m\sin(2\pi ft)$$

Here $\Phi_m$ is the peak value in webers (Wb), $f$ is frequency in Hz.

**Step 2: Apply Faraday's Law.**

For a winding of $N_1$ turns linking the core flux, the induced EMF is:
$$e_1(t) = -N_1\frac{d\Phi}{dt}$$

Differentiate:
$$\frac{d\Phi}{dt} = \Phi_m \cdot \omega\cos(\omega t)$$

So:
$$e_1(t) = -N_1\omega\Phi_m\cos(\omega t)$$

Writing $-\cos\theta = \sin(\theta - 90°)$:
$$e_1(t) = N_1\omega\Phi_m\sin(\omega t - 90°)$$

This tells us two things:
1. The induced EMF is also sinusoidal.
2. It **lags** the core flux by exactly 90°. (The flux reaches its peak when the rate of change is zero, so EMF is zero at that instant, and the EMF is maximum when flux passes through zero: i.e., 90° behind.)

**Step 3: Find the RMS value.**

The peak value of the primary EMF:
$$E_{m1} = N_1\omega\Phi_m = N_1 \cdot 2\pi f \cdot \Phi_m$$

For a pure sine wave, RMS = peak / $\sqrt{2}$:
$$E_1 = \frac{E_{m1}}{\sqrt{2}} = \frac{2\pi f N_1\Phi_m}{\sqrt{2}} = \frac{2\pi}{\sqrt{2}} f N_1\Phi_m = \sqrt{2}\pi f N_1\Phi_m$$

**Step 4: Compute the numerical constant.**
$$\sqrt{2}\pi = 1.41421 \times 3.14159 = 4.44288 \approx 4.44$$

$$\boxed{E_1 = 4.44 f N_1\Phi_m}$$

![Sinusoidal flux waveform and induced EMF lagging by 90 degrees](../Books/Theraja/Ch-32/diagrams/Ch-32_p07_fig13.jpg)

**For the secondary:** The identical flux $\Phi(t)$ threads through all $N_2$ secondary turns (no leakage assumed). By the same derivation:
$$\boxed{E_2 = 4.44 f N_2\Phi_m}$$

![Transformer mutual induction principle](../Books/Theraja/Ch-32/diagrams/Ch-32_p02_principle.jpg)

#### Alternative derivation using average EMF

In the first quarter-cycle (time $= T/4 = 1/(4f)$), the flux rises from 0 to $\Phi_m$:

$$\text{Average rate of change of flux} = \frac{\Phi_m - 0}{1/(4f)} = 4f\Phi_m \text{ Wb/s}$$

By Faraday's Law, average EMF per turn $= 4f\Phi_m$ V.

For a sine wave, the form factor (ratio of RMS to average full-wave rectified value) is:
$$K_f = \frac{\text{RMS}}{\text{Average}} = \frac{\pi}{2\sqrt{2}} = 1.1107 \approx 1.11$$

RMS EMF per turn $= 1.11 \times 4f\Phi_m = 4.44f\Phi_m$

Multiply by turns:
$$E_1 = 4.44fN_1\Phi_m, \quad E_2 = 4.44fN_2\Phi_m \quad \checkmark$$

#### What the formula tells the transformer designer

From $E_1 = 4.44 f N_1\Phi_m$ and $V_1 \approx E_1$:
$$\Phi_m = \frac{V_1}{4.44 f N_1}$$

If core cross-section is $A$ m², then $B_m = \Phi_m/A$.

**Design implication:** For a given supply voltage and frequency, the peak flux density $B_m$ determines $N_1$, and then $N_2 = N_1 \times V_2/V_1$. The core area $A$ is chosen so that $B_m < B_{\text{saturation}}$ (~1.5–1.8 T for silicon steel).


---

---

### Question 5(b): Explain the operating principle of an ideal transformer

> 📋 **Appeared in:** 2017 Q5(b)

#### What "ideal" means

An ideal transformer is a theoretical construct where we remove all imperfections:
- No resistance in windings (no copper loss)
- No leakage flux (all flux links both windings perfectly)
- No core losses (no eddy current or hysteresis)
- No saturation (flux is exactly proportional to current)
- Infinite core permeability (no magnetizing current needed)

Real transformers are close to ideal for many practical calculations.

#### How it works: step by step

**1. Apply AC voltage to primary.**

You connect the primary ($N_1$ turns) to an AC source $v_1 = V_m\sin\omega t$. The source has an EMF. By Kirchhoff's Voltage Law, this EMF must be balanced by something on the primary side. With zero winding resistance, the only thing that can balance $v_1$ is the back-EMF induced by the core flux.

**2. Core flux is established.**

The primary current flowing through the $N_1$-turn winding creates a magnetic MMF ($= N_1 I_1$ ampere-turns). This MMF drives flux through the core. For an ideal core (infinite permeability), only an infinitesimally small MMF is needed to set up any amount of flux. So the magnetizing current is negligible.

The core flux is sinusoidal:
$$\Phi(t) = \Phi_m\sin(\omega t)$$

**3. EMF is induced in both windings.**

By Faraday's Law, the changing flux induces an EMF in every coil it threads:
$$e_1 = -N_1\frac{d\Phi}{dt}, \qquad e_2 = -N_2\frac{d\Phi}{dt}$$

Both EMFs are proportional to the number of turns. The ratio:
$$\frac{e_1}{e_2} = \frac{N_1}{N_2} = a$$

Since $e_1 = v_1$ (ideal, no resistance drop): $\frac{v_1}{v_2} = \frac{N_1}{N_2}$

**4. Output current and power.**

When a load $Z_L$ is connected to the secondary, current $I_2 = V_2/Z_L$ flows. This current tries to change the core flux (by Lenz's Law). But in an ideal transformer, the flux must stay exactly as required by $v_1$. So the primary draws an additional current $I_1'$ to cancel the secondary MMF:

$$N_1 I_1' = N_2 I_2 \implies I_1' = \frac{N_2}{N_1}I_2 = \frac{I_2}{a}$$

**5. Power conservation.**

For an ideal transformer: $V_1 I_1 = V_2 I_2$. Power in = Power out. The transformer simply changes the voltage/current ratio while conserving power.

![Basic working principle of ideal two-winding transformer](../Books/Theraja/Ch-32/diagrams/Ch-32_p02_fig01.jpg)

![Ideal transformer on load with primary and secondary currents and voltages](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_01.jpeg)

---

*(start)* | [🏠 Index](README.md) | [T-02: Construction & Core →](T-02_Transformer_Construction_and_Core.md)
