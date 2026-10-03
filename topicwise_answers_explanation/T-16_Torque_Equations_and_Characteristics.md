[← T-15: IM Equivalent Circuit](T-15_IM_Equivalent_Circuit.md) | [🏠 Index](README.md) | [T-17: Power Flow & Rotor Power →](T-17_Power_Flow_and_Rotor_Power.md)

---

# T-16: Torque Equations & Characteristics

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Torque Equations & Characteristics** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### [2024 Q6(a)]: Definitions of Starting and Running Torque of an Induction Motor

> 📋 **Appeared in:** 2024 Q6(a)

**(a) Define starting and running torque of an induction motor (IM). [Marks: 02, CO: 1]**

#### Definitions & Mathematical Expressions

1. **Starting Torque ($T_{st}$):**
   - The electromagnetic torque developed by an induction motor at the instant of starting when normal rated supply voltage is applied to the stator windings with the rotor at rest (standstill, $N = 0$, slip $s = 1$).
   - It represents the initial breakaway turning effort available to overcome static friction and accelerate the motor and connected mechanical load from zero speed.
   - **Formula:** Setting $s = 1$ in the fundamental torque equation:
     $$T_{st} = \frac{3}{2\pi N_s} \frac{E_2^2 R_2}{R_2^2 + X_2^2} = k \frac{E_2^2 R_2}{Z_2^2}\ \text{N}\cdot\text{m}$$
   - Starting torque is directly proportional to rotor resistance $R_2$ (up to $R_2 = X_2$) and to the square of applied stator voltage ($T_{st} \propto V^2$).

2. **Running Torque ($T$ or $T_{\text{run}}$):**
   - The steady-state electromagnetic torque developed by the motor while running at an operating speed $N$ under loaded conditions, corresponding to operating slip $s$ ($0 < s < 1$).
   - It balances the opposing mechanical load torque and rotational losses at that running speed.
   - **Formula:**
     $$T = \frac{3}{2\pi N_s} \frac{s E_2^2 R_2}{R_2^2 + (s X_2)^2}\ \text{N}\cdot\text{m}$$
   - Under normal running conditions near synchronous speed, $s$ is very small ($2\%\text{–}5\%$), making $(s X_2)^2 \ll R_2^2$. Hence, running torque is approximately linear with slip: $T \propto s$.

---

### [2024 Q7(b) / CT-02 Q1]: Proof of Maximum Torque Formula

> 📋 **Appeared in:** 2024 Q7(b), CT-02 Q1 (Years: 2024)

**(b) Prove that,**
$$T_{\max} = \frac{3}{2\pi N_s} \frac{E_2^2}{2X_2}\ \text{N-m}$$
**Variables having their usual meanings. [Marks: 04, CO: 1]**

#### Why this is surprising

Common intuition says: "More resistance = more voltage drop = less current = less torque." This is wrong in this context. Let's see why.

#### The full derivation and cancellation

Torque equation:
$$T = \frac{k s E_2^2 R_2}{R_2^2 + s^2 X_2^2}$$

Think of this as a function of two variables: $s$ and $R_2$. We want to find $T_{\max}$ by varying both.

**Finding the peak:** Differentiate with respect to $s$ (for fixed $R_2$):

$$\frac{dT}{ds} = kE_2^2 R_2 \cdot \frac{(R_2^2 + s^2X_2^2) - s(2sX_2^2)}{(R_2^2 + s^2X_2^2)^2} = 0$$

Numerator = 0:
$$R_2^2 + s^2X_2^2 - 2s^2X_2^2 = 0 \implies R_2^2 = s^2X_2^2 \implies s_{mT} = \frac{R_2}{X_2}$$

**Substituting $s_{mT} = R_2/X_2$ into the torque equation:**

At the peak, $s = R_2/X_2$. Denominator:
$$R_2^2 + s^2X_2^2 = R_2^2 + \frac{R_2^2}{X_2^2} \cdot X_2^2 = R_2^2 + R_2^2 = 2R_2^2$$

Numerator:
$$s_{mT} E_2^2 R_2 = \frac{R_2}{X_2} \cdot E_2^2 \cdot R_2 = \frac{R_2^2 E_2^2}{X_2}$$

Therefore:
$$T_{\max} = k \cdot \frac{R_2^2 E_2^2/X_2}{2R_2^2} = \frac{kE_2^2}{2X_2}$$

The $R_2^2$ terms in numerator and denominator cancel perfectly. $T_{\max}$ has no $R_2$ in it.

#### The intuition behind the cancellation

When you increase $R_2$:
- The slip at peak torque increases ($s_{mT} = R_2/X_2$ grows).
- At the new peak slip, the rotor current is lower (higher impedance).
- But you're now evaluating at a higher slip, where more of the input power goes into the $R_2/s$ term: meaning the fraction going to resistance is higher.

These two effects exactly cancel: less current but higher per-unit power per unit current.

The result: **The height of the torque peak is set entirely by the supply voltage and the standstill leakage reactance**: two things that don't change when you add rotor resistance.

#### Practical application

Wound-rotor (slip-ring) induction motors can have external resistance added through the slip rings:

- **For starting heavy loads:** Add enough external resistance so $R_2 + R_{ext} = X_2$. This gives $s_{mT} = 1$, meaning maximum torque at standstill. The motor starts with maximum possible torque.
- **For speed control:** Different values of external resistance shift the operating slip and thus the speed, for a given load torque.
- **The max torque available** is always the same regardless of how much resistance is inserted.

![Torque-slip characteristics of 3-phase induction motor with varying rotor resistance](../Books/Theraja/Ch-34/diagrams/Ch-34_p29_fig22.jpg)

---

---

### Question 2(b): Prove: $T_f / T_{\max} = 2as_f / (a^2 + s_f^2)$

> 📋 **Appeared in:** 2017 Q2(b)

#### Why this ratio matters

This formula lets you compare the motor's actual operating torque at full load to the maximum torque it could ever develop. It tells you how close the motor is to its stability limit. A ratio of 0.4 means the motor operates at 40% of its maximum possible torque: comfortable safety margin. A ratio of 0.9 would mean dangerously close to stall.

#### Derivation

**General torque at any slip $s$:**

From the rotor circuit analysis, the air-gap power is:
$$P_g = 3I_2^2 \cdot \frac{R_2}{s} = \frac{3sE_2^2 R_2}{R_2^2 + s^2 X_2^2}$$

Torque:
$$T = \frac{P_g}{\omega_s} = \frac{k \cdot sE_2^2 R_2}{R_2^2 + s^2 X_2^2}, \qquad k = \frac{3}{2\pi n_s}$$

**Torque at maximum (from earlier derivation):**

At $s_{mT} = R_2/X_2$, $T_{\max} = kE_2^2/(2X_2)$.

**Torque at full load slip $s_f$:**
$$T_f = \frac{k s_f E_2^2 R_2}{R_2^2 + s_f^2 X_2^2}$$

**Taking the ratio:**
$$\frac{T_f}{T_{\max}} = \frac{k s_f E_2^2 R_2 / (R_2^2 + s_f^2 X_2^2)}{k E_2^2 / (2X_2)}$$

$$= \frac{s_f R_2 \times 2X_2}{R_2^2 + s_f^2 X_2^2}$$

Now substitute $a = s_{mT} = R_2/X_2$, which means $R_2 = aX_2$:

Numerator: $s_f \cdot aX_2 \cdot 2X_2 = 2as_f X_2^2$

Denominator: $(aX_2)^2 + s_f^2 X_2^2 = X_2^2(a^2 + s_f^2)$

$$\frac{T_f}{T_{\max}} = \frac{2as_f X_2^2}{X_2^2(a^2 + s_f^2)} = \boxed{\frac{2as_f}{a^2 + s_f^2}}$$

*(Proved)*

![Torque-slip curve showing stable and unstable operating regions](../Books/Theraja/Ch-34/diagrams/Ch-34_p22_fig21.jpg)

---

## SECTION - B (Transformers)

---

### Q6(a): Effect of supply frequency increase on torque and speed

> 📋 **Appeared in:** 2021 Q6(a)

#### Detailed analysis

When frequency jumps suddenly from $f_1$ to $f_2 > f_1$ with voltage $V$ unchanged:

**Immediately after frequency increase:**
- New synchronous speed: $N_{s2} = 120f_2/P > N_{s1}$
- Rotor is still spinning at old speed $N$
- New slip: $s' = (N_{s2} - N)/N_{s2}$: higher than before

**New maximum torque:**
$$T_{\max,2} = \frac{kE_2^2}{2X_{2,\text{new}}}$$

Since $X_2 = 2\pi f L_2$, and $f$ increased, $X_2$ increased. Flux falls as $\Phi_m \propto V/f$. But $E_2 = 4.44 f N_2 \Phi_m$, so $E_2 \propto V$ and $E_2^2 \propto V^2$. Also $k = 3/(2\pi n_s) \propto 1/f$.

$$T_{\max,2} \propto \frac{(1/f_2) \cdot V^2}{2 \times 2\pi f_2 L_2} = \frac{V^2}{4\pi f_2^2 L_2} \propto \frac{V^2}{f^2}$$

**Maximum torque drops as $1/f^2$** when $V$ is constant. This is severe. A 20% frequency increase reduces max torque to $(1/1.2)^2 = 0.69$ of the original: nearly a third lost.

**This is why VFDs use V/f control:**

Variable frequency drives always change voltage proportionally with frequency ($V/f = $ constant). This keeps $E_2/f = $ constant, and therefore $E_2/X_2 = $ constant. Maximum torque remains constant at all speeds.

![Complete torque-speed and torque-slip curve across motoring, generating, and braking regions](../Books/Theraja/Ch-34/diagrams/Ch-34_p34_fig32.jpg)

---

### [2024 Q7(c)]: Worked Numerical Problem — Ratio of Maximum to Full-Load Torque & Breakdown Speed

> 📋 **Appeared in:** 2024 Q7(c)

**Problem:** A 50 Hz, 8 pole induction motor has F.L. slip of 4%. The rotor resistance/phase $= 0.01\ \Omega$ and standstill reactance/phase $= 0.1\ \Omega$. Find the ratio of maximum to full-load torque and the speed at which the maximum torque occurs.

#### Step-by-Step Solution

**Given:**
- Frequency $f = 50\text{ Hz}$, Poles $P = 8$
- Full-load slip $s_f = 4\% = 0.04$
- Rotor resistance per phase $R_2 = 0.01\ \Omega$
- Standstill rotor reactance per phase $X_2 = 0.1\ \Omega$

**Step 1: Synchronous speed**
$$N_s = \frac{120 f}{P} = \frac{120 \times 50}{8} = \mathbf{750\text{ rpm}}$$

**Step 2: Slip at maximum torque**
$$s_{mT} = \frac{R_2}{X_2} = \frac{0.01}{0.1} = \mathbf{0.10} \quad (\mathbf{10\%})$$

**Step 3: Speed at which maximum torque occurs**
$$N_{T\max} = N_s(1 - s_{mT}) = 750 \times (1 - 0.10) = 750 \times 0.90 = \mathbf{675\text{ rpm}}$$

**Step 4: Ratio of maximum to full-load torque**
Using Kloss's torque relation:
$$\frac{T_{FL}}{T_{\max}} = \frac{2}{\dfrac{s_f}{s_{mT}} + \dfrac{s_{mT}}{s_f}} = \frac{2}{\dfrac{0.04}{0.10} + \dfrac{0.10}{0.04}} = \frac{2}{0.4 + 2.5} = \frac{2}{2.9} = 0.6897$$

$$\frac{T_{\max}}{T_{FL}} = \frac{2.9}{2} = \mathbf{1.45}$$

$$\boxed{\frac{T_{\max}}{T_{FL}} = 1.45, \qquad N_{T\max} = 675\text{ rpm}}$$

---

### [2024 Q6(c)]: Worked Numerical Problem — Slip-Ring IM Rotor Currents & Maximum Torque Condition

> 📋 **Appeared in:** 2024 Q6(c)

**Problem:** A 3-$\varphi$, slip-ring IM with star-connected rotor has an induced emf of 120 volts between slip-rings at standstill with normal voltage applied to the stator. The rotor winding has a resistance per phase of $0.3\ \Omega$ and stand-still leakage reactance per phase of $1.5\ \Omega$. Determine:
(i) Rotor current/phase when running short-circuited with 4% slip.
(ii) The slip and rotor current per phase when the rotor is developing maximum torque.

#### Step-by-Step Solution

**Given:**
- Standstill line-to-line voltage between slip rings: $E_{2,\text{line}} = 120\text{ V}$
- Star-connected rotor $\implies$ Standstill rotor phase voltage:
  $$E_2 = \frac{E_{2,\text{line}}}{\sqrt{3}} = \frac{120}{\sqrt{3}} = \mathbf{69.282\text{ V}}$$
- Rotor resistance per phase: $R_2 = 0.3\ \Omega$
- Standstill rotor reactance per phase: $X_2 = 1.5\ \Omega$

#### (i) Rotor current per phase at 4% slip ($s = 0.04$)

- Induced rotor emf per phase:
  $$E_{2r} = s E_2 = 0.04 \times 69.282 = 2.7713\text{ V}$$
- Rotor reactance per phase:
  $$X_{2r} = s X_2 = 0.04 \times 1.5 = 0.06\ \Omega$$
- Rotor impedance per phase:
  $$Z_{2r} = \sqrt{R_2^2 + X_{2r}^2} = \sqrt{0.3^2 + 0.06^2} = \sqrt{0.09 + 0.0036} = \sqrt{0.0936} = 0.30594\ \Omega$$
- Rotor current per phase:
  $$I_{2r} = \frac{E_{2r}}{Z_{2r}} = \frac{2.7713}{0.30594} = \mathbf{9.06\text{ A}}$$

$$\boxed{I_{2r} = 9.06\text{ A per phase at } s = 4\%}$$

#### (ii) Slip and rotor current per phase at maximum torque

- Slip at maximum torque:
  $$s_m = \frac{R_2}{X_2} = \frac{0.3}{1.5} = \mathbf{0.20} \quad (\mathbf{20\%})$$
- At $s_m = 0.20$, $X_{2r} = s_m X_2 = 0.20 \times 1.5 = 0.30\ \Omega = R_2$:
  $$E_{2r} = s_m E_2 = 0.20 \times 69.282 = 13.8564\text{ V}$$
  $$Z_{2r} = \sqrt{R_2^2 + R_2^2} = 0.3\sqrt{2} = 0.42426\ \Omega$$
- Rotor current per phase:
  $$I_{2r,\max} = \frac{E_{2r}}{Z_{2r}} = \frac{13.8564}{0.42426} = \mathbf{32.66\text{ A}} \approx \mathbf{32.7\text{ A}}$$

$$\boxed{s_m = 0.20\;(20\%), \qquad I_{2r,\max} = 32.7\text{ A per phase}}$$

---

### [2024 Q8(a)]: Complete Torque-Slip Characteristic of a Three-Phase Induction Machine

> 📋 **Appeared in:** 2024 Q8(a)

**(a) Draw the torque ~ slip of 3-$\varphi$ induction machine. [Marks: 02, CO: 1]**

![Complete torque-speed and torque-slip curve across motoring, generating, and braking regions](../Books/Theraja/Ch-34/diagrams/Ch-34_p34_fig32.jpg)

#### The Three Operating Regions of an Induction Machine

An induction machine can operate in three distinct quadrants depending on rotor slip:

1. **Motoring Region ($0 < s < 1$, $0 < N < N_s$):**
   - The rotor rotates in the same direction as the stator RMF, but at a speed below synchronous speed ($N < N_s$).
   - Electrical energy is drawn from the AC supply and converted into mechanical torque to drive a load.
   - Key operating points:
     - **Standstill ($s = 1$, $N = 0$):** Motor develops starting torque $T_{st}$.
     - **Breakdown / Maximum Torque ($s = s_m = R_2/X_2$):** Peak pull-out torque $T_{\max} = \frac{3}{2\pi N_s} \frac{E_2^2}{2X_2}$.
     - **Normal Operating Range ($s = 0.02\text{–}0.05$):** Stable, linear torque-slip region ($T \propto s$).
     - **Synchronous Speed ($s = 0$, $N = N_s$):** Zero torque ($T = 0$).

2. **Generating Region ($s < 0$, $N > N_s$):**
   - An external prime mover (such as a wind turbine or diesel engine) drives the rotor above synchronous speed ($N > N_s$) in the direction of the rotating field.
   - Slip becomes negative ($s < 0$).
   - Induced rotor EMF and currents reverse phase relative to the air-gap flux, producing negative (counter) torque that opposes rotation.
   - The machine converts mechanical input into electrical power fed back into the AC supply grid. Requires reactive magnetizing power from grid or shunt capacitors.

3. **Braking / Plugging Region ($s > 1$, $N < 0$):**
   - The rotor rotates in the direction opposite to the stator RMF (achieved by reversing any two stator supply phases while running, or driven backwards by an overhauling load).
   - Relative speed between RMF and rotor exceeds synchronous speed: $N_s - (-N) = N_s + N > N_s \implies s > 1$.
   - Developed electromagnetic torque opposes mechanical rotation, bringing the rotor to a rapid stop (plugging).
   - All electrical power drawn from the line and mechanical kinetic energy from the shaft are dissipated as intense heat inside the rotor circuit.

---

[← T-15: IM Equivalent Circuit](T-15_IM_Equivalent_Circuit.md) | [🏠 Index](README.md) | [T-17: Power Flow & Rotor Power →](T-17_Power_Flow_and_Rotor_Power.md)
