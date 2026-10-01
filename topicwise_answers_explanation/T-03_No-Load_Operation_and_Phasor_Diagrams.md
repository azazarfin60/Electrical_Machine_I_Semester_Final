[← T-02: Construction & Core](T-02_Transformer_Construction_and_Core.md) | [🏠 Index](README.md) | [T-04: Equivalent Circuit →](T-04_Equivalent_Circuit.md)

---

# T-03: No-Load Operation & Phasor Diagrams

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **No-Load Operation & Phasor Diagrams** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Q1(c): Why does primary current increase with secondary load?

> 📋 **Appeared in:** 2019 Q1(c)

#### The fundamental principle: MMF balance

An ideal transformer maintains the core flux $\Phi_m$ at a constant value (set by the supply voltage: $\Phi_m \approx V_1/(4.44 f N_1)$). This flux requires a certain amount of magnetomotive force (MMF):

$$\text{MMF required} = H \times l_c = \Phi_m \times \frac{l_c}{\mu A}$$

At no-load, the primary provides all the required MMF: $N_1 I_0 = $ const.

When a load draws secondary current $I_2$: The secondary current through $N_2$ turns creates a demagnetizing MMF = $N_2 I_2$. This tends to reduce the core flux.

But $V_1$ is fixed by the supply. Since $V_1 \approx E_1 = 4.44 f N_1 \Phi_m$, the flux cannot change (it's tied to the supply voltage). The primary current must increase to cancel the secondary demagnetization:

$$N_1 I_1 - N_2 I_2 = N_1 I_0 \approx \text{const}$$

$$N_1 I_1 = N_1 I_0 + N_2 I_2$$

$$I_1 = I_0 + \frac{N_2}{N_1} I_2 = I_0 + I_2'$$

As $I_2$ increases (more load), $I_1$ increases proportionally (larger primary current from the supply).

![Transformer under load condition with flux and currents](../Books/diagrams/Ch-32_p12_fig16.jpg)

**Energy flow:** The increased primary current brings in more energy from the supply to match the energy delivered to the load. The transformer doesn't generate energy: it regulates primary current to always match the secondary load.

---

---

### Q1(b): No-load operation of a 1-phase transformer

> 📋 **Appeared in:** 2024 Q1(b)

#### What happens physically before the load is connected

When you first switch on the transformer with the secondary open, the circuit looks like a simple RL series circuit (primary winding resistance $R_1$ and inductance $L_1$) connected to the supply.

But it is not quite simple, because the inductance $L_1$ is strongly coupled to the iron core, which is a non-linear magnetic material. The actual no-load current that flows is slightly non-sinusoidal (due to the non-linear B-H curve). However, for exam purposes, we treat it as sinusoidal.

**The no-load current has two physical roles:**

**Role 1: Magnetic:** A fraction of the current ($I_m$) is responsible for establishing the alternating core flux. This current is in quadrature with the applied voltage (90° lagging). It does no real work: it simply oscillates back and forth as the field grows and collapses. This is the magnetizing component.

**Role 2: Thermal:** The core heats up due to hysteresis and eddy current losses. These losses require real power input. A small active current component ($I_c$) in phase with the voltage supplies this power.

The total no-load current is the phasor sum: $I_0 = I_c - jI_m$ (taking $V_1$ as reference, $I_c$ is in phase, $I_m$ lags by 90°).

![No load transformer circuit with magnetizing and core loss components](../Books/diagrams/Ch-32_p21_fig29.jpg)

#### The phasor diagram at no-load: step by step

1. Draw $\vec{\Phi}_m$ as horizontal reference. (Flux is the physically fundamental quantity: everything else derives from it.)

2. Induced EMF lags flux by 90°: $\vec{E}_1$ is 90° clockwise from $\vec{\Phi}_m$.

3. Applied voltage must balance $E_1$: $\vec{V}_1 = -\vec{E}_1$ (upward, if $E_1$ is downward). Angle between $V_1$ and $\Phi_m$ = 90° (voltage leads flux by 90°).

4. $I_c$ is in phase with $-E_1$ (i.e., in phase with $V_1$). It is the "real" component.

5. $I_m$ lags $V_1$ by 90°. It points in the same direction as $\Phi_m$.

6. $I_0 = I_c + I_m$ (phasor sum: at angle $\phi_0$ from $V_1$).

7. Secondary: $\vec{E}_2 = \vec{E}_1 \times (N_2/N_1)$. Since secondary is open, $V_2 = E_2$.

![Transformer no load phasor diagram](../Books/diagrams/Ch-32_p29_fig39.jpg)

**Important observation:** The secondary open-circuit voltage $V_2 = E_2 = 4.44 f N_2 \Phi_m$ is in phase with $E_1$ and hence lags the primary applied voltage $V_1$ by 180°. This is expected: the secondary and primary EMFs are both induced by the same core flux and are in the same direction relative to their respective winding directions (but since the secondary winding direction is defined from the output terminal, conventionally $V_2$ is taken as positive when it drives current into a load, which gives it the right polarity).

---

### [2018 Q1(c)] Equivalent Circuit and Complete Vector Diagram for Lagging Power Factor

> 📋 **Appeared in:** 2018 Q1(c)

#### 1. Exact Equivalent Circuit of a Practical Transformer
A practical two-winding transformer deviates from the ideal model due to finite copper conductivity ($R_1, R_2$), leakage fluxes ($\Phi_{l1}, \Phi_{l2} \to X_1, X_2$), and finite core permeability with iron losses ($R_c \parallel jX_m$). The complete exact equivalent circuit is:

![Exact Equivalent Circuit of a Practical Transformer](diagrams/transformer_exact_equivalent_circuit.png)

* **Primary winding series impedance**: $\mathbf{Z}_1 = R_1 + jX_1$ accounts for primary winding resistance drop and leakage reactance drop.
* **Core excitation shunt branch**: Connected across primary induced back-EMF $\mathbf{E}_1$. Resistor $R_c$ carries active core-loss current $I_c$ (hysteresis + eddy current), while reactor $X_m$ carries reactive magnetizing current $I_m$ that sets up the mutual alternating flux $\Phi_m$.
* **Ideal transformer**: Scaled by turns ratio $a = N_1 / N_2$ providing galvanic isolation:
  $$\frac{E_1}{E_2} = \frac{N_1}{N_2} = a, \qquad \frac{I_2'}{I_2} = \frac{N_2}{N_1} = \frac{1}{a}$$
* **Secondary winding series impedance**: $\mathbf{Z}_2 = R_2 + jX_2$ accounts for secondary internal voltage drops before supplying terminal voltage $\mathbf{V}_2$ to load $Z_L$.

---

#### 2. Complete Vector (Phasor) Diagram on Load (Lagging Power Factor, $\cos\phi_2$)
For an inductive load with lagging power factor $\cos\phi_2$, the secondary current $\vec{I}_2$ lags the secondary terminal voltage $\vec{V}_2$ by phase angle $\phi_2$.

![Complete Transformer Vector Diagram for Lagging Power Factor](diagrams/transformer_phasor_lagging_pf.png)

##### Step-by-Step Construction Logic:
1. **Reference Mutual Flux ($\vec{\Phi}$)**:
   - Drawn horizontally along $+X$. Mutual flux is the common coupling medium linking both primary and secondary windings.
2. **Induced EMFs ($\vec{E}_1, \vec{E}_2$)**:
   - By Faraday's Law, induced EMF lags mutual flux by $90^\circ$:
     $$e = -N \frac{d\Phi}{dt} \implies \vec{E} \text{ lags } \vec{\Phi} \text{ by } 90^\circ$$
   - Both $\vec{E}_1$ and $\vec{E}_2$ are drawn vertically downward along $-Y$.
3. **Secondary Load Triangle**:
   - Secondary terminal voltage $\vec{V}_2$ leads secondary current $\vec{I}_2$ by load angle $\phi_2$ (i.e., $\vec{I}_2$ lags $\vec{V}_2$).
   - Applying secondary KVL:
     $$\vec{E}_2 = \vec{V}_2 + \vec{I}_2 R_2 + j\vec{I}_2 X_2$$
   - From the terminal of $\vec{V}_2$, draw resistive drop $\vec{I}_2 R_2$ **parallel** to $\vec{I}_2$.
   - From that tip, draw inductive leakage reactance drop $j\vec{I}_2 X_2$ **perpendicular (leading by $90^\circ$)** to $\vec{I}_2$.
   - The vector sum reaches the tip of induced EMF $\vec{E}_2$.
4. **Primary Counter-EMF ($-\vec{E}_1$)**:
   - To counteract the induced EMF, the primary applied voltage must establish $-\vec{E}_1$.
   - Draw $-\vec{E}_1$ vertically upward along $+Y$ ($180^\circ$ opposite to $\vec{E}_1$, leading $\vec{\Phi}$ by $90^\circ$).
5. **Primary Current Components**:
   - **Load reflected current ($\vec{I}_2'$)**: To neutralize secondary demagnetizing MMF ($N_2 \vec{I}_2$), primary draws load component $\vec{I}_2' = (N_2/N_1) \vec{I}_2$ oriented **$180^\circ$ opposite** to $\vec{I}_2$.
   - **Excitation current ($\vec{I}_0$)**: Composed of active loss component $\vec{I}_c$ (parallel to $-\vec{E}_1$) and reactive magnetizing component $\vec{I}_m$ (parallel to $\vec{\Phi}$):
     $$\vec{I}_0 = \vec{I}_c + \vec{I}_m, \qquad I_0 = \sqrt{I_c^2 + I_m^2}$$
   - **Total primary current ($\vec{I}_1$)**: Vector sum of no-load current and reflected load current:
     $$\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$$
6. **Primary Terminal Voltage ($\vec{V}_1$)**:
   - Applying primary KVL:
     $$\vec{V}_1 = -\vec{E}_1 + \vec{I}_1 R_1 + j\vec{I}_1 X_1$$
   - From the tip of $-\vec{E}_1$, add primary resistance drop $\vec{I}_1 R_1$ **parallel** to $\vec{I}_1$.
   - From that point, add primary leakage reactance drop $j\vec{I}_1 X_1$ **perpendicular (leading by $90^\circ$)** to $\vec{I}_1$.
   - The line joining the origin to the endpoint of $j\vec{I}_1 X_1$ represents the applied primary voltage $\vec{V}_1$.
   - The angle between $\vec{V}_1$ and $\vec{I}_1$ is the primary operating phase angle $\phi_1$, giving input power factor $\cos\phi_1$ (lagging).

> **Sources:** [Books/Ch-32_02_Phasor_and_Equivalent_Circuit.md](../Books/Theraja/Ch-32/Ch-32_02_Phasor_and_Equivalent_Circuit.md) · [ClassNoteByRaidah/Class_14.md](../ClassNoteByRaidah/Class_14_Transformer_Equivalent_Circuit_and_Phasor.md) · [SlidesByMaam/L-02_ECE-2207.md](../SlidesByMaam/L-02_ECE-2207.md)

---

[← T-02: Construction & Core](T-02_Transformer_Construction_and_Core.md) | [🏠 Index](README.md) | [T-04: Equivalent Circuit →](T-04_Equivalent_Circuit.md)
