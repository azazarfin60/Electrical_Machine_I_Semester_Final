# T-02: Transformer Construction & Core

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Transformer Construction & Core** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-02: Leakage Flux: Physical Picture and All Effects

*Appears in: 2024 Q2b, CT-04 Q1*

#### The ideal vs. real transformer

In an ideal transformer, every magnetic flux line stays inside the iron core and links both primary and secondary windings. In reality, some flux takes a shortcut through the surrounding air or insulation without completing the path through the core.

This "straying" flux is called **leakage flux**. It is the single most important non-ideality of a transformer that affects its voltage regulation and equivalent circuit.

#### Three categories of flux

**Mutual flux $\Phi_m$:** Travels through the core and links both windings. This is the useful flux: the one that transfers power from primary to secondary. Without it, no transformation happens.

**Primary leakage flux $\Phi_{l1}$:** Created by primary current $I_1$. Instead of going through the secondary core window, it bulges out through the air surrounding the primary coil, then returns. It links primary turns only.

**Secondary leakage flux $\Phi_{l2}$:** Created by secondary current $I_2$. Similarly leaks through air around the secondary coil, linking only the secondary turns.

![Schematic of transformer showing mutual flux and primary/secondary leakage fluxes](../SlidesByMaam/diagrams/L-10_ECE-2107_p04_fig01.jpg)

#### Why does leakage flux travel through air?

The air path has constant (and low) magnetic permeability, unlike the iron core whose permeability is thousands of times higher. But even with low permeability, the air path near the windings is very short. The total reluctance of the leakage path can still be low enough to carry a small fraction of the total flux.

Since air doesn't saturate, leakage flux is directly proportional to current:
$$\Phi_{l1} = L_{l1} I_1 / N_1 \propto I_1$$

This is a linear relationship: leakage flux waveform is exactly in phase with the current causing it.

#### Effect 1: Leakage EMFs and Leakage Reactance

The alternating leakage flux $\Phi_{l1}$ induces an EMF in the primary by Faraday's Law:
$$e_{l1} = -N_1\frac{d\Phi_{l1}}{dt}$$

Since $\Phi_{l1} \propto I_1$ and the current is sinusoidal, the leakage flux is also sinusoidal and in phase with $I_1$. The derivative $d\Phi_{l1}/dt$ is 90° ahead of $\Phi_{l1}$. So the leakage EMF lags the current by 90°.

An EMF that lags the driving current by 90° behaves exactly like the voltage drop across an inductor. So we model the primary leakage as a **series inductive reactance**:
$$X_1 = \omega L_{l1} = 2\pi f L_{l1}$$

This reactance limits the primary current and causes a voltage drop. Similarly for the secondary:
$$X_2 = \omega L_{l2} = 2\pi f L_{l2}$$

#### Effect 2: Series voltage drops

The terminal voltage equations become:

**Primary (applying KVL):**
$$V_1 = E_1 + I_1 R_1 + jI_1 X_1$$

The applied voltage must overcome the back-EMF ($E_1$), the resistive drop ($I_1 R_1$), and the reactive drop ($jI_1 X_1$).

**Secondary (applying KVL):**
$$V_2 = E_2 - I_2 R_2 - jI_2 X_2$$

The secondary terminal voltage is less than $E_2$ because of drops across $R_2$ and $X_2$ inside the winding.

#### Effect 3: Worsened voltage regulation

Voltage regulation (VR) measures how much the secondary voltage drops from no-load to full-load.

At no-load: $I_2 = 0$, no drops, $V_2 = E_2$.

At full-load with lagging power factor: both the resistive drop $I_2R_2$ and the reactive drop $I_2X_2$ pull $V_2$ below $E_2$.

For lagging loads, the reactive drop subtracts from $E_2$:
$$|V_2| \approx E_2 - I_2(R_2\cos\phi + X_2\sin\phi)$$

The leakage reactance $X_2$ contributes significantly to poor regulation for inductive loads.

For leading loads (capacitive), the reactive drop can add back (negative regulation: voltage actually rises with load), which is beneficial.

#### Effect 4: Fault current limiting: a benefit

During a secondary short circuit, the only impedance limiting the fault current is $Z_{01} = \sqrt{R_{01}^2 + X_{01}^2}$ (total leakage impedance referred to primary).

Without leakage reactance, short-circuit current would approach infinity. Leakage reactance physically limits the fault current to about 5–10 times rated current in well-designed power transformers. This prevents mechanical and thermal destruction during faults.


---

---

### Q3(b): Middle phase wound in reverse: shell-type transformer economy

> 📋 **Appeared in:** 2019 Q3(b)

#### Why three-phase shell type transformers can save core material

In a 3-phase shell-type transformer, three single-phase "frames" are placed side by side. Each phase has two yokes (top and bottom) connecting the outer limbs.

The fluxes are: $\Phi_A$, $\Phi_B$, $\Phi_C$ at 120° apart in time. At any instant:
$$\Phi_A + \Phi_B + \Phi_C = 0$$

**Without reverse winding (middle phase same direction):**

The middle yoke (between A and B frames, and between B and C frames) must carry flux that flows between adjacent phases. Since the outer limbs carry $\Phi_A$ and $\Phi_C$ outward, the middle phase must connect them. The yoke cross-sections must be designed for the full unidirectional flux.

**With reverse winding on middle phase B:**

The phase B flux direction is reversed in the core. This means $-\Phi_B$ flows in the B-limb. By symmetry, the yoke flux distribution becomes more balanced. The peak flux in each yoke section is reduced because the reversed middle-phase flux assists cancellation in the yokes.

The outer yokes (carrying only one phase each) need only $\Phi_m$ cross-section. The middle limb can also be reduced because its flux is balanced by the reversed winding MMF. Net result: less core material for the same power rating.

![Core-type and shell-type transformer magnetic circuits](../Books/diagrams/Ch-32_p02_fig02.jpg)

---

## Induction Motor Topics

---

### Q1(a): Why are cores laminated?

> 📋 **Appeared in:** 2020 Q1(a)

#### The physics of eddy current loss

The iron core sits in a time-varying magnetic field. By Faraday's Law, any closed conducting path threading this field has an EMF induced in it. If the resistance of the path is low, a current flows: an eddy current.

The iron core itself is a conductor. Without lamination, the whole solid iron block is one big conducting path. The induced EMF drives currents through the entire cross-section. These currents circulate in loops perpendicular to the flux, hence the name "eddy" currents.

Power dissipated by eddy currents: $P_e = k_e f^2 B_m^2 t^2 V_{\text{core}}$

where $t$ is the thickness of the conducting path. The critical point: power loss $\propto t^2$.

#### How lamination helps

Cut the core into thin sheets (laminations) insulated from each other by a thin oxide layer or varnish coating. Now each lamination is a separate conducting path with a much smaller cross-section.

![Stepped core cross section and laminations](../Books/diagrams/Ch-32_p05_fig10.jpg)

The eddy current in each lamination is confined to within one sheet of thickness $t_{\text{lam}}$. Since $P_e \propto t^2$, if you replace one thick sheet of thickness $T$ with $n$ laminations each of thickness $T/n$:

$$P_{e,\text{laminated}} = n \times k_e f^2 B_m^2 \left(\frac{T}{n}\right)^2 = \frac{k_e f^2 B_m^2 T^2}{n}$$

The eddy current loss drops by a factor of $n$ (number of laminations). Using 100 laminations instead of one solid piece: eddy current losses drop to 1/100.

**Typical lamination thickness:** 0.35 mm (power frequency), 0.1 mm (high frequency), 0.05 mm (very high frequency). At 50 Hz, 0.35 mm laminations reduce eddy current losses by a factor of $(0.35/1)^2 = 0.12$ compared to a 1 mm thick sheet: a large saving.

---

