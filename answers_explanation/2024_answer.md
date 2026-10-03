[← 2023 Answer](2023_answer.md) | [🏠 Index](README.md) | *(end)*

---

# ECE 2207: 2024 Semester Final: Explanation Style Answers
**RUET · ECE Dept · 2nd Year Even Semester Examination, 2024**
**Course No:** ECE 2207 | **Course Title:** Electrical Machines I | **Full Marks:** 60 | **Time:** 3 Hours
**Answer SIX questions taking any THREE from each section. Each question carries 10 marks.**

> Tutorial-style answers to the same paper covered in [../answers_exam_style/2024_answer.md](../answers_exam_style/2024_answer.md). Same questions, same final numbers, but every step says **why** it works.
> Section A (Q1–Q4) is transformers. Section B (Q5–Q8) is induction motors. Marks and CO tags are taken from the question paper margin.
> Question source: [../PrevYearQuestions/2024.md](../PrevYearQuestions/2024.md). Cross-cutting theory is in [2018_2024_answer.md](2018_2024_answer.md).

---

# SECTION - A

## Question 1

### Q1(a): Enlist some practical applications of transformer. **[CO1, Marks: 02]**

#### What the question is really asking

A transformer has no moving part, so its only job is to **change an AC voltage level while passing the power across unchanged**. Every application below is just a consequence of that one property, together with the two secondary properties that follow from the emf equation:

$$V \propto f N \Phi_m$$

- **Step voltage up** in a generating station, so a few hundred MW can cross a few kilometres of line at a few hundred volts instead of a few hundred kV. Power out equals power in, so current falls in the same ratio that voltage rises, and line loss $I^2R$ collapses.
- **Step voltage down** at the far end of the line, back to 230/400 V for distribution.
- **Isolate** the user from the live supply. Two separate windings means there is **no conductive path** between primary and secondary, so an insulation fault on the low-voltage side cannot put mains voltage on an appliance.
- **Impedance matching** for audio and electronic circuits, so a low-impedance loudspeaker gets maximum power from a high-impedance amplifier output.
- **Current transformation** for measuring large currents, e.g. a current transformer feeding a 5 A ammeter while the line carries hundreds of amps.

#### The four applications to write down

| Application | Why a transformer is the natural choice |
|:---|:---|
| **Power transmission and distribution** | Step-up at generating station, step-down at substations and at the consumer |
| **Voltage/current measurement** | CT for large currents, PT for high voltages, both giving a safe 5 A / 110 V instrument reading |
| **Safety and isolation** | Separates the user from the mains; used in portable appliances and medical equipment |
| **Impedance matching** | Maximises power transfer in audio and electronic circuits |
| **Control and protection circuits** | Small control voltages stepped up to act on relays, contactors and switchgear |
| **Frequency/phase conversion** | Frequency changer drives, rectifier and inverter transformers, and Scott-T sets for 3-$\varphi$ to 2-$\varphi$ |

> [!note] One line that scores the marks
> The transformer works only on **AC**, and only because $V = 4.44 f N B_m A$. Change any of $f$, $N$ or $B_m$ and the voltage changes with it. It transfers power without a moving part, so there is nothing to wear out and nothing to maintain.

---

### Q1(b): When a power transformer is excited as a manner shown in following figure, then describe the induced voltage phenomena **[CO2, Marks: 04]**

![Transformer excitation and induced voltage phenomena: a closed rectangular ferromagnetic core with coil1 (N1 turns, source v with a switch, current i1, self-induced counter-emf e1) on the left limb and coil2 (N2 turns, induced emf e2, current i2 into load R) on the right limb, sharing the mutual flux path](../PrevYearQuestions/diagrams/2024_q1b_transformer.png)

#### Read the figure carefully, because it decides the whole answer

Two things in this diagram are deliberate, and both are worth stating before any algebra:

1. **The source is drawn as a DC battery with a single-pole switch.** So this is a **switching transient**, not steady-state AC. There is no sinusoidal regime here at all. The flux is a step-like build-up, not a sine wave. This is exactly why the **raw differential form** of Faraday's law is the right tool here and the rms phasor emf equation $E = 4.44 f N \Phi_m$ is not.
2. **Two arrows labelled $e_1$ and $e_2$ point *upward* through the coils, while $i_1$ and $i_2$ point outward into the circuit.** The upward emf arrows and the Lenz's-law sign convention below are consistent: the induced emf always opposes the change that produced it.

The four quantities in the figure are $v$ (source), $i_1$ and $e_1$ (primary side), and $e_2$, $i_2$ (secondary side with load $R$), all coupled through $\Phi_{mutual}$.

#### Step 1: close the switch, and current starts to build

The instant the switch closes, the primary sees the full source voltage $v$. The winding has inductance, not a resistor, so the current **cannot** jump. It rises from zero:

$$v = R_1 i_1 + N_1\frac{d\Phi}{dt}$$

At $t = 0$ the current is zero, so the whole of $v$ appears across the inductive term. The primary is then nothing but an inductor being charged from a source.

#### Step 2: the rising current creates the mutual flux

The current $i_1$ in $N_1$ turns produces an m.m.f. $N_1 i_1$, and that magnetises the iron core. Because the core is a **closed** path of high permeability, the flux it creates links **both** limbs, which is why the figure labels it "$\Phi\ mutual$". So:

$$\Phi(t) = \frac{N_1 i_1(t)}{\mathcal{R}}$$

where $\mathcal{R}$ is the reluctance of the closed iron loop. This flux is common to both windings, and that is precisely what makes a transformer a transformer rather than two unrelated coils.

#### Step 3: self-induction in coil 1, the counter-emf $e_1$

As $\Phi$ climbs, it cuts the $N_1$ turns of coil1 itself. Faraday's law gives an emf in coil1:

$$e_1 = -N_1 \frac{d\Phi}{dt}$$

The **minus sign is Lenz's law**, and it is the whole physical content of the answer. The induced emf acts in the direction that **opposes the change in flux that created it**. Since $\Phi$ is rising, $e_1$ is a back emf that tries to push the primary current back down.

This is why a transformer does not short-circuit itself when the switch closes. The rising flux immediately generates a counter-emf that very nearly balances the applied voltage $v$, leaving only a small residue $(v + e_1)$ across the tiny winding resistance to drive $i_1$. **The core flux is clamped by the applied voltage, not by the load.**

#### Step 4: mutual induction in coil 2, the emf $e_2$

The same rising flux now cuts the $N_2$ turns of coil2, and this time no self-cancelling takes place because coil2 is a **different** winding:

$$e_2 = -N_2 \frac{d\Phi}{dt}$$

Compare the two:

$$\frac{e_2}{e_1} = \frac{N_2}{N_1}$$

**This ratio is the entire transformer.** Voltage has been handed across an air gap, from one winding to another, with **no electrical connection whatsoever** between them.

#### Step 5: $e_2$ drives a current, and that current loads the primary

$e_2$ appears across the load $R$ in the secondary loop, so a current flows out of the upper terminal:

$$i_2 = \frac{-e_2}{R} = \frac{N_2}{R}\frac{d\Phi}{dt}$$

Power is now being delivered to $R$. But that does not violate energy conservation, because the **primary current has already grown** to supply it. The extra $i_1$ that flowed in during Step 3 was not idle current; it was the load component, and by m.m.f. balance

$$N_1 i_1 - N_2 i_2 = N_1 i_0$$

holds at all times. As $i_2$ grows, $i_1$ grows with it.

#### Step 6: the secondary reaction opposes the original flux

This is the part students forget, and it is the reason a loaded transformer does not blow up.

The secondary current $i_2$ is itself a source of m.m.f., $N_2 i_2$. By Lenz's law, that m.m.f. acts to **reduce** the very flux that created $i_2$ in the first place. So the secondary **reaction flux opposes the rate of change of the core flux**.

The consequence is the self-correcting loop:

1. $\Phi$ dips slightly because $N_2 i_2$ is fighting it.
2. A smaller $\Phi$ means a smaller $e_1 = -N_1 d\Phi/dt$.
3. A smaller $e_1$ means a bigger net voltage $(v + e_1)$ across the small $R_1$, so more $i_1$ flows.
4. The extra $i_1$ supplies the m.m.f. that $N_2 i_2$ removed, restoring $\Phi$.
5. Equilibrium: the flux returns to its no-load value.

So **the core flux is essentially unchanged by load**, and the primary current rises from $i_0$ to carry the reflected secondary current.

#### The three emfs, summarised

| Emf | Law | Where it appears | Role |
|:---|:---|:---|:---|
| $e_1$ | $e_1 = -N_1\frac{d\Phi}{dt}$ | Across coil1 | **Self-induction.** Opposes $v$ and limits $i_1$ |
| $e_2$ | $e_2 = -N_2\frac{d\Phi}{dt}$ | Across coil2 | **Mutual induction.** The useful output that drives $R$ |
| Reaction | $-N_2 i_2$ | Inside the core | Opposes $d\Phi/dt$, forcing $i_1$ up to compensate |

#### Why the ratio $e_2/e_1 = N_2/N_1$ survives into steady state

Once the transient dies away and the flux is alternating sinusoidally, $\frac{d\Phi}{dt}$ becomes proportional to $f\Phi_m$, and the differential equations above become the familiar rms form used everywhere else in this paper:

$$E_1 = 4.44 f N_1 \Phi_m, \qquad E_2 = 4.44 f N_2 \Phi_m$$

So the switching picture in the figure and the $4.44 f N \Phi_m$ results in Q1(c) and Q2(c) are **the same physics**; the figure just shows it before the sines are taken.

---

### Q1(c): Magnetizing and iron-loss currents of a 2200/200 V and a 2200/250 V transformer **[CO2, Marks: 04]**

> **Part (i)** A 2,200/200 — V transformer draws a no-load primary current of 0.6A and absorbs 400W. Find the magnetizing and iron loss currents.
> **Part (ii)** Now, consider a 2,200/250 — V transformer takes 0.5A at a p.f. of 0.3 on open circuit. Find magnetizing and working components of no-load primary current.

#### What the question is really asking

The no-load primary current is doing **two completely different jobs at once**, and it is not a single physical current. It is the phasor sum of two parts:

$$\vec{I}_0 = \vec{I}_w + \vec{I}_\mu$$

- $\vec{I}_w$, the **working** (or **iron-loss**, or **core-loss**) component, is **in phase** with $V_1$. Its only job is to supply the real power dissipated as heat in the core, hysteresis and eddy currents. So $I_w\cos\phi_0 = P_{Fe}/V_1$.
- $\vec{I}_\mu$, the **magnetizing** component, is in **quadrature** with $V_1$. Its only job is to create the core flux, so it draws no real power at all.

Because the two are 90° apart, the total is the hypotenuse, not the sum. That is the entire geometry of both parts:

$$I_0^2 = I_w^2 + I_\mu^2$$

The 400 W in part (i) is the **core loss only**, because the winding copper loss $I_0^2 R_1$ is tiny when $I_0$ is a few percent of rated.

#### Part (i): 2200/200 V, $I_0 = 0.6$ A, $P = 400$ W

**Step 1: no-load power factor.**

$$\cos\phi_0 = \frac{P_0}{V_1 I_0} = \frac{400}{2200 \times 0.6} = \frac{400}{1320} = 0.30303$$

A no-load power factor of 0.30 is very poor, and that is exactly what we expect: at no load the transformer is almost a pure inductor.

**Step 2: working (iron-loss) component.** It is the in-phase part:

$$I_w = I_0 \cos\phi_0 = 0.6 \times 0.30303 = 0.1818\text{ A}$$

**Step 3: magnetizing component.** Pythagoras, not subtraction:

$$I_\mu = \sqrt{I_0^2 - I_w^2} = \sqrt{0.6^2 - 0.1818^2} = \sqrt{0.36 - 0.03306} = \sqrt{0.32694} = 0.5718\text{ A}$$

$$\boxed{I_\mu = 0.572\text{ A (magnetizing)},\qquad I_w = 0.182\text{ A (iron-loss)}}$$

**Sanity check.** $I_\mu / I_w = 3.15$, so the no-load current is 95% magnetizing. And $I_0/V_1$ style sizing: 0.6 A against a full-load HV current of tens of amps confirms this really is a no-load reading.

#### Part (ii): 2200/250 V, $I_0 = 0.5$ A at 0.3 p.f.

Note the paper asks for the same pair of quantities, and the wording in (ii) puts magnetizing first. Same method, different numbers, and the power factor is now **given** rather than derived.

**Step 1: working component.**

$$I_w = I_0 \cos\phi_0 = 0.5 \times 0.3 = 0.15\text{ A}$$

**Step 2: magnetizing component.**

$$I_\mu = \sqrt{0.5^2 - 0.15^2} = \sqrt{0.25 - 0.0225} = \sqrt{0.2275} = 0.4770\text{ A}$$

$$\boxed{I_\mu = 0.477\text{ A (magnetizing)},\qquad I_w = 0.15\text{ A (working)}}$$

#### Reading the two answers together

| | Part (i) | Part (ii) |
|:---|:---|:---|
| $\cos\phi_0$ | 0.303 (computed from watts) | 0.3 (given) |
| $I_w$ | 0.182 A | 0.15 A |
| $I_\mu$ | 0.572 A | 0.477 A |
| $I_\mu / I_w$ | 3.15 | 3.18 |

The two cases are almost identical, which is a useful cross-check: both are near the same 0.30 no-load power factor, and the second transformer simply draws a smaller absolute current.

**The ratio is the real lesson.** $I_\mu$ is roughly **three times** $I_w$ in every practical transformer. That is why no-load power factor is always poor, and it is exactly the imbalance that part (a) of Q2 explains.

---

## Question 2

### Q2(a): "The magnetizing current of power transformer is not fully sinusoidal" — justify it. **[CO1, Marks: 02]**

#### The argument, in one chain

Start from the **B-H curve** of the iron. Steel is a **non-linear** material: permeability $\mu = B/H$ is not constant. It is high near the origin and falls away as the core approaches saturation.

Now recall what the supply does. The applied voltage is **sinusoidal**, and the induced emf must balance it almost exactly (the winding resistance is tiny):

$$v_1 \approx e_1 = 4.44 f N_1 \Phi_m$$

An emf proportional to $d\Phi/dt$ can be sinusoidal **only if $\Phi$ is sinusoidal**. So the core flux is forced to be sinusoidal.

Next, Faraday's law again, this time for the exciting current:

$$i_\mu(t) = \frac{\Phi(t)}{\mathcal{R}\,\ldots} \;\propto\; H(t) = \frac{B(t)}{\mu}$$

To force a **sinusoidal** flux through a **non-linear** magnetic path, the magnetizing current cannot be sinusoidal. It must be **peaked**, because near the flux peaks the core is close to saturation, where the incremental permeability is small and a lot of extra $H$ is needed for a small increment in $B$.

$$\boxed{\Phi \text{ sinusoidal} \ \Rightarrow\ H \text{ (and hence } i_\mu \text{) peaked and non-sinusoidal}}$$

#### Why it matters — the third harmonic

The peaked wave is not sinusoidal, so it contains **harmonic** components. The dominant one is the **third harmonic**, typically 5% to 10% of the fundamental. Two consequences follow, and both are examinable:

1. **Zero sequence.** Third-harmonic currents in all three phases are **in phase** with one another, so they cannot circulate in a normal three-wire system. They cannot flow unless a neutral path or a delta loop exists.
2. **Flux and emf distort.** If the third-harmonic magnetising current is blocked, the flux wave becomes **flat-topped** rather than sinusoidal. A flat-topped flux integrates into a **peaky** induced emf, so the phase voltage contains a third-harmonic component and can be badly distorted.

#### Where this shows up in the connections

| Connection | Third harmonic can circulate? | Result |
|:---|:---|:---|
| $\Delta$-$\Delta$ | Yes, round the closed delta | Clean, sinusoidal voltages |
| Y-Y with isolated neutrals | **No** | Flat-topped flux, peaked emf, neutral oscillation |
| Y-Y with solidly earthed neutrals | Yes, via the neutral | Acceptable |
| Any bank with a **tertiary delta** | Yes, via the tertiary | Acceptable |

This is the single biggest practical reason $\Delta$ appears in three-phase transformer banks, and it is why Y-Y is the least used of the four standard connections.

> [!success] Two sentences that earn the marks
> The magnetising current is **not** fully sinusoidal because the **B-H curve of the core is non-linear**. A sinusoidal flux must therefore be produced by a **peaked** magnetising current, which contains a **third-harmonic** component. In a Y-Y bank with isolated neutrals that third harmonic cannot circulate, so the flux becomes flat-topped and the induced emf becomes distorted.

---

### Q2(b): Draw and explain the phasor diagram of a power transformer, when the transformer is loaded with "R-L" load. **[CO1, Marks: 04]**

#### What "R-L load" forces, before any phasor is drawn

A resistive-inductive load has a **lagging** power factor. Everything downstream of that one fact is determined:

- $I_2$ lags $V_2$ by $\phi_2 = \tan^{-1}(X_L/R_L)$.
- By m.m.f. balance the primary load component $I_2'$ is in phase with $I_2$, so it too lags.
- Lagging current means the reactive drop $I_2X_2$ **subtracts** from the induced emf, so the terminal voltage $V_2$ is **below** $E_2$. That is why regulation is worst at lagging power factor.

#### The complete vector diagram

![Complete vector diagram of a practical transformer on lagging power factor load, showing E1, E2, V1, V2, I0, I1, I2, the drops I1R1, I1X1, I2'R2', I2'X2' and the corresponding impedance triangles](../Books/Theraja/Ch-32/diagrams/Ch-32_p21_fig29.jpg)

![Complete vector diagram of the transformer on load at unity, lagging and leading power factor, showing how the reactive drop moves the secondary terminal voltage](../Books/Theraja/Ch-32/diagrams/Ch-32_p15_fig18.jpg)

#### Construction, step by step

**Step 1.** Draw $\vec{V}_1$ as the reference, horizontal, pointing right. Everything else is measured from it.

**Step 2.** Draw $\vec{\Phi}_m$ along the same axis. Since $e = -N\,d\Phi/dt$, the induced emfs **lag** the flux by 90°, so they point straight **down**.

**Step 3.** Draw $\vec{E}_1$ and $\vec{E}_2$ **downward** from the flux axis, with $E_2/E_1 = N_2/N_1$. Because $\Phi_m$ is common to both windings, volts per turn is identical on both sides.

**Step 4.** Now account for the series drops. All the primary quantities are referred to the primary side as $I_1$, $R_1$, $X_1$ and $R_2', X_2'$; on the secondary side they are $I_2$, $R_2$, $X_2$.

- $\vec{I}_1 R_1$ is drawn **in phase** with $\vec{I}_1$ (horizontal, since $\cos\phi_1 \approx \cos\phi_2$ for a lagging load and $I_0$ is small).
- $\vec{I}_1 X_1$ is drawn **leading** $\vec{I}_1$ by 90°.
- $\vec{I}_2' R_2'$ is in phase with $\vec{I}_2'$, and $\vec{I}_2' X_2'$ leads it by 90°.

**Step 5.** Vector-add the drops head-to-tail onto $\vec{E}_1$ to get the supply voltage. On the secondary, vector-add the referred drops onto $\vec{E}_2$ to get $\vec{V}_2$.

$$\vec{V}_1 = -\vec{E}_1 + \vec{I}_1 R_1 + j\vec{I}_1 X_1$$
$$\vec{V}_2 = \vec{E}_2 - \vec{I}_2 R_2 - j\vec{I}_2 X_2$$

**Step 6.** Draw the no-load current $\vec{I}_0$ at the primary. It is the phasor sum of $\vec{I}_w$ (in phase with $V_1$) and $\vec{I}_\mu$ (lagging $V_1$ by 90°), so it lies well below and to the right of the flux axis.

**Step 7.** Add it: $\vec{I}_1 = \vec{I}_0 + \vec{I}_2'$.

#### Reading the diagram — what each feature tells you

| Feature | Meaning |
|:---|:---|
| $\vec{V}_1$ lies above $\vec{-E_1}$ | Winding drops are small; $V_1 \approx E_1$ |
| $\vec{V}_2$ lies **inside** $\vec{E}_2$ | The load is taking current, so $V_2 < E_2$ |
| Gap grows as $I_2$ grows | Voltage regulation, the no-load to full-load fall |
| $\vec{I}_1$ angle close to $\vec{I}_2$ angle | Primary power factor nearly equals load power factor |
| $\vec{I}_0$ small and near the vertical | No-load power factor is poor |
| $I_2 X_2 \gg I_2 R_2$ | Large transformers are reactance-dominated, so regulation tracks $\sin\phi$ |

#### What lagging power factor specifically costs

Compare the three load cases on the diagram:

- **Unity p.f.**: the $I_2 X_2$ drop is perpendicular to $V_2$ and costs almost nothing in magnitude.
- **Lagging p.f.**: the $I_2 X_2$ drop points substantially **opposite** to $V_2$, so it subtracts directly. Voltage falls.
- **Leading p.f.**: the $I_2 X_2$ drop points **towards** $V_2$, so it adds. The voltage can even rise above no-load value.

So an R-L load is the **worst case for regulation**, which is why Q4(a)'s phrase "the HV side is usually short circuited" and the whole efficiency question are usually quoted at 0.8 lagging.

---

### Q2(c): Equivalent circuit of a 50 kVA, 2200/110 V transformer from O.C. and S.C. tests **[CO2, Marks: 04]**

> **O.C. test (L. V. side):** 400W, 10A, 110V
> **S.C. test (H. V. side):** 808W, 20.5A, 90V
> Compute all the parameters of the equivalent circuit referred to the H. V. side and draw the resultant circuit.

#### First, why each test isolates what it does

![Open-circuit test circuit: the low voltage winding is energised at rated voltage with wattmeter, ammeter and voltmeter, while the high voltage winding is left open](../Books/Theraja/Ch-32/diagrams/Ch-32_p32_fig43.jpg)

**O.C. test, at rated voltage.** Two consequences follow at once:
- Rated voltage means **rated flux**, so the iron loss is the full normal iron loss.
- The current is only $I_0$. Rated LV current is $I_{LV} = 50000/110 = 454.5$ A, so $I_0 = 10$ A is just 2.2% of rated. Copper loss is $(0.022)^2 = 0.05\%$ of normal. Negligible.

**So the wattmeter reads the iron loss, $P_{Fe} = 400$ W, and nothing else.** That is why it is done on the **LV** side: 110 V is easy to source and 10 A is easy to measure.

![Short-circuit test circuit: a reduced voltage is applied to the high voltage winding with the low voltage winding shorted, and the wattmeter reads the copper loss](../Books/Theraja/Ch-32/diagrams/Ch-32_p32_fig43.jpg)

**S.C. test, at rated current.** The mirror image:
- Rated current means **normal copper loss**.
- Only $90/2200 = 4.1\%$ of rated voltage is applied, so flux is only 4.1% of rated and iron loss is roughly $(0.041)^2$ of normal. Negligible.

**So the wattmeter reads copper loss and nothing else.** It is done from the **HV** side so the applied voltage is a settable 90 V rather than an awkward 4.5 V on the LV side.

That clean separation of one loss per test is the entire reason both tests exist.

#### The turns ratio

$$a = \frac{V_{HV}}{V_{LV}} = \frac{2200}{110} = 20, \qquad a^2 = 400$$

Rated currents, needed shortly:

$$I_{HV} = \frac{50000}{2200} = 22.727\text{ A}, \qquad I_{LV} = \frac{50000}{110} = 454.55\text{ A}$$

#### The excitation branch, from the O.C. test (LV base)

$$\cos\phi_0 = \frac{400}{110 \times 10} = \frac{400}{1100} = 0.36364$$

$$I_w = 10 \times 0.36364 = 3.636\text{ A}, \qquad I_\mu = \sqrt{10^2 - 3.636^2} = \sqrt{100 - 13.22} = \sqrt{86.78} = 9.3156\text{ A}$$

Each shunt element is its own voltage over its own current:

$$R_0\big|_{LV} = \frac{110}{3.636} = 30.25\ \Omega$$
$$X_0\big|_{LV} = \frac{110}{9.3156} = 11.807\ \Omega$$

**Cross-check on $R_0$:** it must also equal $V^2/W_0 = 12100/400 = 30.25\ \Omega$. It does.

#### Refer the shunt branch to the HV side

Impedance scales as the **square** of the turns ratio, because voltage scales by $a$ and current by $1/a$:

$$R_0 = 30.25 \times 400 = 12100\ \Omega$$
$$X_0 = 11.807 \times 400 = 4723\ \Omega$$

$$\boxed{R_0 = 12100\ \Omega, \qquad X_0 = 4723\ \Omega}$$

Look at the scale. $R_0$ is twelve thousand ohms, while the series resistance we are about to find is under two ohms. That ratio of roughly 6000:1 is exactly why the approximate equivalent circuit, which shifts the shunt branch to the input terminals, loses nothing measurable.

#### The series branch, from the S.C. test (already HV base)

$$Z_{01} = \frac{V_{sc}}{I_{sc}} = \frac{90}{20.5} = 4.3902\ \Omega$$

Resistance from the wattmeter, since $W_{sc}$ is pure $I^2R$:

$$R_{01} = \frac{W_{sc}}{I_{sc}^2} = \frac{808}{20.5^2} = \frac{808}{420.25} = 1.9227\ \Omega$$

Reactance by Pythagoras:

$$X_{01} = \sqrt{Z_{01}^2 - R_{01}^2} = \sqrt{4.3902^2 - 1.9227^2} = \sqrt{19.274 - 3.697} = \sqrt{15.577} = 3.9468\ \Omega$$

$$\boxed{R_{01} = 1.9227\ \Omega, \qquad X_{01} = 3.9468\ \Omega, \qquad Z_{01} = 4.3902\ \Omega}$$

#### The trap in this question: 20.5 A is **not** the rated current

This is the single most important point in the whole part, and it is where a careless answer goes wrong.

The S.C. test was carried out at
$$I_{sc} = 20.5\text{ A}$$

but the rated HV current is
$$I_{rated} = \frac{50000}{2200} = 22.727\text{ A}$$

**These are not the same.** The test ran at $20.5/22.727 = 0.902$ of rated current. So the 808 W on the wattmeter is the copper loss at 0.902 of full load, **not** at full load. Copper loss follows $I^2$, so it must be scaled:

$$P_{cu,FL} = 808 \times \left(\frac{22.727}{20.5}\right)^2 = 808 \times (1.1087)^2 = 808 \times 1.2287$$

$$\boxed{P_{Cu,FL} = 993\text{ W} \quad\text{not } 808\text{ W}}$$

**But be careful about what does and does not need scaling.**

| Quantity | Needs scaling? | Reason |
|:---|:---|:---|
| $R_{01}$ | **No** | It comes from $W_{sc}/I_{sc}^2$, and both the watts and the current belong to the *same* test condition. The ratio is already correct. |
| $Z_{01}$, $X_{01}$ | **No** | Same reason: $V_{sc}/I_{sc}$ uses the test's own voltage and current. |
| Copper loss at **full load** | **Yes** | Full load means 22.727 A, so $I^2R$ must be recomputed at that current. |

If you wrote $P_{Cu,FL} = 808$ W you would understate the full-load copper loss by 19%, and every efficiency figure computed from it would be wrong by about half a percentage point.

#### Full-load copper loss and total loss

$$P_{Cu,FL} = 993\text{ W}$$
$$P_{total,FL} = P_{Fe} + P_{Cu,FL} = 400 + 993 = 1393\text{ W}$$

#### The resultant equivalent circuit, referred to the HV side

![Approximate equivalent circuit referred to the high voltage side, with the exciting branch R0 and jX0 moved to the input terminals and R01 = 1.9227 ohm in series with jX01 = 3.9468 ohm feeding the load](../Books/Theraja/Ch-32/diagrams/Ch-32_p15_fig18.jpg)

The complete parameter set for the circuit referred to the HV side is:

| Branch | Element | Value | Source |
|:---|:---|:---|:---|
| **Shunt (excitation)** | $R_0$ | $12100\ \Omega$ | O.C. test, LV base $\times a^2$ |
| | $X_0$ | $4723\ \Omega$ | O.C. test, LV base $\times a^2$ |
| **Series** | $R_{01}$ | $1.9227\ \Omega$ | S.C. test, already HV base |
| | $X_{01}$ | $3.9468\ \Omega$ | S.C. test, already HV base |
| **Losses** | $P_{Fe}$ | $400$ W | O.C. wattmeter |
| | $P_{Cu,FL}$ | $993$ W | S.C. wattmeter scaled to $22.727$ A |

#### Reading the numbers as an engineer

- $X_{01}/R_{01} = 2.05$. The leakage path is mostly inductive, so voltage regulation will be driven by $\sin\phi$, as it is in every large transformer.
- $Z_{01}$ as a percentage. This needs a **base impedance**, not the applied voltage — dividing ohms by volts gives ohms, not a percentage:
$$Z_{\text{base}} = \frac{V_L^2}{S} = \frac{2200^2}{50000} = 96.8\ \Omega, \qquad \%Z = \frac{4.3902}{96.8}\times 100 = 4.54\%$$
So the short-circuit voltage is 4.54% of rated, which is an entirely ordinary figure for a 50 kVA unit. It also cross-checks: $\%R = 1.9227/96.8 = 1.99\%$ matches the loss side, $993/50000 = 1.99\%$, and $\sqrt{1.99^2 + 4.08^2} = 4.54\%$.
- The no-load current is **not** the 44% that a naive $10/22.727$ suggests. The O.C. test was done on the **LV** side, so $I_0 = 10$ A is an LV figure; referred to the HV side it is $10/20 = 0.5$ A, which against $I_{rated} = 22.727$ A is only **2.2%**. That is the low value you should expect, since a core needs magnetising current but very little real current. The no-load power factor of 0.364 is high because this small unit has a comparatively poor core — the *power factor* is elevated while the *current* stays small.

---

## Question 3

### Q3(a): Define voltage regulation of transformer. **[CO1, Marks: 02]**

#### The definition

**Voltage regulation** of a transformer is the change in its secondary terminal voltage from **no load** to **full load**, at constant primary voltage and constant load power factor, expressed as a percentage of the full-load (or, by some definitions, the no-load) secondary voltage.

$$\%\text{Regulation} = \frac{V_{2,\text{no-load}} - V_{2,\text{full-load}}}{V_{2,\text{full-load}}}\times 100 \quad \text{(taking rated/ full-load value as base)}$$

#### Why we compare against no load

The no-load secondary voltage is the **natural reference**, because with $I_2 = 0$ there is no $I_2 R_2$ or $I_2 X_2$ drop, so

$$V_{2,\text{no-load}} = E_2 = 4.44 f N_2 \Phi_m$$

That is the pure induced emf, a fixed quantity set by $V_1$, $f$ and $N_2$. Load the transformer and the terminal voltage falls below it. The regulation is simply **how far it falls**, expressed as a fraction of that fixed reference.

#### Why regulation exists at all — the mechanism

From the secondary voltage equation of a loaded transformer,

$$V_2 = E_2 - I_2 R_2 - jI_2 X_2$$

The terminal voltage is the induced emf **minus** the internal impedance drops. Those drops grow with $I_2$, so as you add load the terminal voltage sags. The **approximate** magnitude (which is what the standard formula gives, obtained by projecting the drop phasor onto $V_2$) is

$$V_{2,\text{no-load}} - V_{2,\text{full-load}} \approx I_2(R_2\cos\phi_2 \pm X_2\sin\phi_2)$$

$$\boxed{\%\text{Reg} = \frac{I_2\big(R_2\cos\phi_2 \pm X_2\sin\phi_2\big)}{V_2}\times 100}$$

The sign depends on the load:
- **Lagging** (R-L, inductive): the reactive drop subtracts, so use $+$. Voltage falls.
- **Leading** (capacitive): the reactive drop adds, so use $-$. Voltage can even rise.

#### Why it matters

A distribution transformer feeds customers through their own wiring, so a fall in the transformer's terminal voltage reaches every appliance as a **brown-out**. Lights dim, motors slow and may stall, and contactors drop out. Regulation is therefore a specification a manufacturer must meet, and it is one of the two classical transformer ratings alongside efficiency.

#### The governing fact

Look again at the drop formula. Since $X_2 \gg R_2$ in a real transformer, the dominant term is $X_2\sin\phi_2$. So regulation is essentially governed by **load power factor**: it is small at unity p.f., moderate at 0.8 lagging, and large at 0.5 lagging or worse. That is why "voltage regulation at 0.8 power factor lagging" is the standard specification quoted on every transformer nameplate.

> [!example] A quick feel
> In Q2(c) we found $X_{01} = 3.95\ \Omega$ and $R_{01} = 1.92\ \Omega$ on the HV side. At full load and 0.8 lagging, the drop is
> $22.7(1.92\times0.8 + 3.95\times0.6) \approx 22.7(1.54+2.37) = 88.7$ V on 2200 V, so regulation is about $88.7/2200 = 4\%$. That sits just under the 4.54% short-circuit impedance, which is the point: at 0.8 lagging the $\sin\phi$ term dominates, so regulation approaches but never exceeds %Z. It could only reach 4.54% at $0^\circ$ phase difference, i.e. unity power factor with zero resistance.

---

### Q3(b): Explain with the help of vector diagram, how three 1-$\varphi$ transformers can be used to design a 3-$\varphi$ transformer. **[CO2, Marks: 04]**

#### The problem being solved

Three single-phase transformers are cheaper to manufacture, to transport and to repair individually than one big three-phase unit. If we can connect three of them so they behave as one balanced three-phase machine, we get a 3-$\varphi$ transformer out of standard 1-$\varphi$ parts.

![Schematic of a single-phase transformer showing the core, the primary winding with N1 turns and applied V1, the secondary winding with N2 turns delivering V2 to the load, and the mutual flux in the core](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_01.jpeg)

The answer is a **bank** (or group) of three transformers. The only design decision is **how to connect each side, primary and secondary**. Each independent 1-$\varphi$ transformer becomes one **phase** of the 3-$\varphi$ machine.

#### The two decisions, and the four standard banks

**Primary connection** can be star (Y) or delta ($\Delta$); **secondary** likewise. That gives four common banks:

| Bank | Primary | Secondary | Phase shift | Where used |
|:---|:---|:---|:---|:---|
| Y-Y | Star | Star | $0°$ | Least used (see limitations) |
| $\Delta$-$\Delta$ | Delta | Delta | $0°$ | Low-voltage high-current; allows open-delta |
| $\Delta$-Y | Delta | Star | $30°$ | **Step up** at generating stations |
| Y-$\Delta$ | Star | Delta | $-30°$ | **Step down** at substations |

![The four standard three-phase transformer connections: Y-Y, delta-delta, Y-delta and delta-Y](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_51.jpeg)

#### Building it physically: the vector diagram method

To connect three transformers into a bank you must **phase-tag** them so that their induced voltages sum correctly. The method:

1. **Give each transformer a polarity (dot) convention.** Mark the start of each winding as dotted.
2. **Identify the induced emf phasor of each.** With the primary windings all connected to the same reference, each secondary produces an emf $E_2$ at the **same** magnitude and in the **same** relative direction with respect to its own terminals, because every transformer has the same turns ratio and shares the same primary flux reference.
3. **Connect them so the three secondary emfs appear $120°$ apart** across the three line pairs. That is exactly what star or delta does:
   - In **star**, the three winding emfs radiate from a common neutral at $120°$, and the **line voltages** are the differences, giving a balanced set.
   - In **delta**, the three winding emfs are connected head-to-tail round a closed triangle. The three **side voltages** of that triangle are the three line voltages, automatically $120°$ apart.

![Open-delta (V-V) connection circuit with two transformers, and the phasor diagram showing that the third line voltage still appears across the open corner](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_52.jpeg)

#### The vector diagram that proves it

Take the secondary emf of transformer A as the reference $\vec{E}_A = E\angle 0°$. Because all three primaries are fed from a balanced 3-$\varphi$ supply (or all primaries are connected in star/delta so each phase gets its proper share), the three induced secondary emfs are equal in magnitude and $120°$ apart:

$$\vec{E}_A = E\angle 0°, \qquad \vec{E}_B = E\angle{-120°}, \qquad \vec{E}_C = E\angle{+120°}$$

Connect head-to-tail (delta) and these three vectors **close on themselves**, because for any balanced three-vector set $\vec{E}_A + \vec{E}_B + \vec{E}_C = 0$. The three side lengths of that closed triangle are the three line voltages, equal and $120°$ apart — a perfectly balanced 3-$\varphi$ output from three 1-$\varphi$ boxes.

#### Why the line quantities are $\sqrt{3}$ times the winding quantities

This $\sqrt{3}$ is worth stating because it is where most marks slip:

- **Star:** line current $=$ winding current, but line voltage $=\sqrt{3}\times$ winding voltage. So $V_L = \sqrt{3}V_{ph}$ and $I_L = I_{ph}$, giving $S = \sqrt{3}V_LI_L$.
- **Delta:** line voltage $=$ winding voltage, but line current $=\sqrt{3}\times$ winding current. So $V_L = V_{ph}$ and $I_L = \sqrt{3}I_{ph}$, again $S = \sqrt{3}V_LI_L$.

#### What you get, and the catch

A 3-$\varphi$ transformer built from three 1-$\varphi$ units: three-phase in, three-phase out, at whatever voltage ratio each 1-$\varphi$ transformer provides, scaled by the connection. The bank inherits all the advantages **and** all the problems of whatever connection you choose. If you chose Y-Y you inherit the third-harmonic problem of Q2(a); if you chose $\Delta$-$\Delta$ you inherit the 57.7% open-delta capacity of Q4(b).

---

### Q3(c): No-load test analysis of a single-phase transformer **[CO2, Marks: 04]**

> Resistance of primary winding $= 0.6\ \Omega$; Primary voltage: 220 V; Secondary voltage: 110 V; Primary current: 0.5 A; Power input: 30 W
> Find: (i) the turn ratio, (ii) the magnetizing component of no-load current, (iii) its working (or loss) component, (iv) the iron loss.

#### Why the primary resistance is the reason this question has four parts

At no load the wattmeter does **not** read the iron loss alone, because unlike the ideal test in Q2(c), here the problem bothers to give $R_1 = 0.6\ \Omega$. At no load the primary still carries $I_0$, so it still burns $I_0^2R_1$ watts in copper. Therefore:

$$P_0 = P_{Fe} + I_0^2 R_1$$

and part (iv) will **not** come out as 30 W. That is the deliberate point of this question, and it is worth stating up front so the answer is not "corrected" back to the naive value.

#### (i) Turn ratio

Volts per turn is the same on both windings, so the ratio follows directly from the two voltages:

$$a = \frac{N_1}{N_2} = \frac{V_1}{V_2} = \frac{220}{110} = 2$$

$$\boxed{a = 2}$$

#### (ii) and (iii) Split the no-load current into its two jobs

The no-load current $I_0 = 0.5$ A has the working (iron-loss) component **in phase** with $V_1$, and the magnetizing component **in quadrature**. Working from the input power:

$$P_0 = V_1 I_0 \cos\phi_0 \quad\Rightarrow\quad \cos\phi_0 = \frac{P_0}{V_1 I_0} = \frac{30}{220\times0.5} = \frac{30}{110} = 0.2727$$

**Working (loss) component:**
$$I_w = I_0 \cos\phi_0 = \frac{P_0}{V_1} = \frac{30}{220} = 0.13636\text{ A}$$
$$\boxed{I_w = 0.1364\text{ A}}$$

**Magnetizing component** (Pythagoras, since the two are 90° apart):
$$I_\mu = \sqrt{I_0^2 - I_w^2} = \sqrt{0.5^2 - 0.13636^2} = \sqrt{0.25 - 0.018595} = \sqrt{0.231405} = 0.48105\text{ A}$$
$$\boxed{I_\mu = 0.481\text{ A}}$$

(Optionally, the shunt branch: $R_0 = V_1/I_w = 220/0.13636 = 1613\ \Omega$ and $X_0 = V_1/I_\mu = 220/0.48105 = 457\ \Omega$.)

#### (iv) Iron loss — subtract the primary copper loss

This is the step that separates this question from a standard O.C. test. The 30 W input contains **both** losses:

$$P_0 = P_{Fe} + I_0^2 R_1$$

$$I_0^2 R_1 = (0.5)^2 \times 0.6 = 0.25 \times 0.6 = 0.15\text{ W}$$

$$P_{Fe} = P_0 - I_0^2R_1 = 30 - 0.15 = 29.85\text{ W}$$

$$\boxed{P_{Fe} = 29.85\text{ W}}$$

**Note carefully.** The intended answer is **29.85 W**, not 30 W, precisely because the problem supplies $R_1 = 0.6\ \Omega$. Reporting 30 W would ignore the given data. In a real transformer this copper loss is genuinely tiny (here $0.15$ W out of $30$ W, i.e. 0.5%), which is why the usual textbook O.C. test **neglects** it and quotes the whole 30 W as iron loss. But this question supplies the resistance, so we use it.

#### Summary of all four answers

| Part | Quantity | Value |
|:---|:---|:---|
| (i) | Turn ratio $a$ | $2$ |
| (ii) | Magnetizing component $I_\mu$ | $0.481$ A |
| (iii) | Working (loss) component $I_w$ | $0.1364$ A |
| (iv) | Iron loss $P_{Fe}$ | $29.85$ W |

---

## Question 4

### Q4(a): In performing the short circuit test of a transformer, HV side is usually short circuited — explain it. **[CO2, Marks: 02]**

#### What the S.C. test needs to achieve

To measure copper loss, the test must drive **rated current** through the windings. Rated current on the LV side of, say, a 2200/110 V transformer is $50000/110 = 454$ A. Forcing 454 A through meters and a source rated for that is impractical and dangerous.

#### Reason 1: it makes the test current **rated current**, not 5.45 times rated

The S.C. test deliberately applies only a **small fraction of rated voltage** (typically 2–5%). The current that flows is then set by the internal impedance: $I = V_{sc}/Z_{01}$. The whole design of the test is that a few percent of rated voltage happens to produce **rated current**, because $Z_{01}$ is tiny.

But which side you energise determines which **rated** current you get. If you energise the **LV** winding, the voltage you can conveniently apply (say 90 V) is divided by the LV winding's own small impedance, and the current that flows is $90/Z_{LV}$, which equals the **LV** rated current — $454$ A, not $22.7$ A. That is 20 times too much current for the instrumentation.

If you energise the **HV** winding instead, the impedance in the loop is the **HV-side** impedance $Z_{01}$, which is $a^2 = 400$ times larger than the LV impedance. The same applied volt-second produces rated **HV** current, $22.7$ A — a comfortable meter reading.

$$\frac{Z_{HV}}{Z_{LV}} = a^2 = 400, \qquad I_{HV,\text{rated}} = \frac{I_{LV,\text{rated}}}{a}$$

In one sentence: **short-circuiting the HV (many-turn, high-impedance) side while energising it from the source puts the large impedance in the test loop, so a small applied voltage yields rated HV current, which is $1/a$ of the LV rated current and therefore easily measurable.**

#### Reason 2: it makes the required applied voltage **practicable to set**

With the **HV side shorted** and energised, the applied S.C. voltage is a few percent of 2200 V, i.e. tens of volts (like 90 V) — easy to obtain from a low-power laboratory supply and easy to adjust accurately.

If you energised the **LV side**, the same fraction of rated current would be 400 times larger, and to get that you would have to apply a voltage that is a few percent of 110 V, i.e. about **2–5 V**. Setting and measuring a 2 V test voltage accurately is far harder than setting 90 V, and the percentage error in $V_{sc}$ propagates directly into $Z_{01}$.

#### Reason 3: it keeps the instruments on the **low-current** side

Both instruments sit in the energised (HV) circuit. Because the current there is rated **HV** current ($22.7$ A) rather than rated **LV** current ($454$ A), ordinary ammeters, wattmeters and fuses suffice. No special high-range current transformers are needed.

#### Reason 4: it keeps the flux, and therefore the iron loss, negligible

The applied voltage is only a few percent of rated, so the flux is only a few percent of rated, and iron loss (which goes roughly as flux squared) is a negligible fraction of the reading. So the wattmeter reads copper loss essentially alone.

#### The mirror-image rule

The same logic, applied to the O.C. test, explains why the O.C. test is normally done on the **LV side**: it needs rated **voltage** (easy on 110 V) and only a small current.

| Test | Side energised | Other side | What it measures | Why that side |
|:---|:---|:---|:---|:---|
| O.C. | LV | open | Iron loss (rated flux, tiny current) | Rated voltage easy to apply |
| S.C. | HV | shorted | Copper loss (rated current, tiny flux) | Rated current easy to measure; applied voltage settable |

---

### Q4(b): Is it possible to maintain 3-$\varphi$ power supply when one phase of a 3-$\varphi$ transformer is burned out? **[CO1, Marks: 04]**

#### The answer: **Yes**, provided the surviving transformers are **delta** on both sides

The method is the **open-delta** (or **V-V**) connection. It works because of a property of any balanced 3-$\varphi$ system, independent of the transformers themselves.

#### The key phasor identity

In any closed loop of three line voltages,

$$\vec{V}_{AB} + \vec{V}_{BC} + \vec{V}_{CA} = 0$$

So any **two** of the line voltages completely determine the third:

$$\vec{V}_{CA} = -(\vec{V}_{AB} + \vec{V}_{BC})$$

Two transformers can therefore generate all three line voltages. The third appears "for free" across the gap left by the missing unit, produced by the phasor closure, not by a third transformer.

![Open-delta (V-V) connection circuit with two transformers, and the phasor diagram showing that the third line voltage still appears across the open corner](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_7_52.jpeg)

#### What you physically do

1. Start from a $\Delta$-$\Delta$ bank of three 1-$\varphi$ transformers.
2. One unit fails. Isolate and disconnect it from **both** primary and secondary.
3. Leave the other two connected. Each side now forms a "V".
4. Re-energise. The load still sees three line voltages $120°$ apart, so the 3-$\varphi$ supply continues.

No rewiring of the survivors is required, which is exactly why $\Delta$-$\Delta$ banks are chosen wherever continuity of supply matters (hospitals, waterworks, industrial feeders).

#### Why the capacity drops to 57.7%, derived

Let $V$ and $I$ be the rated winding voltage and winding current of **one** transformer, so each unit is rated $VI$ VA.

**Closed $\Delta$-$\Delta$:** line voltage $=$ winding voltage; line current $=\sqrt{3}\times$ winding current. So
$$S_{\Delta\Delta} = \sqrt{3}V_LI_L = \sqrt{3}\,V\,(\sqrt{3}I) = 3VI$$

That is just three transformers each doing $VI$, the obvious sum.

**Open delta:** each remaining winding now sits **alone in a line**, with no parallel path to share current, so the line current **cannot** exceed the winding rating:
$$I_L = I \quad (\text{not } \sqrt{3}I)$$
$$S_{VV} = \sqrt{3}V_LI_L = \sqrt{3}VI$$

$$\frac{S_{VV}}{S_{\Delta\Delta}} = \frac{\sqrt{3}VI}{3VI} = \frac{1}{\sqrt{3}} = 0.577$$

$$\boxed{\text{Open-delta capacity} = 57.7\% \text{ of the original three-transformer bank}}$$

#### The two percentages students confuse

| Question | Calculation | Answer |
|:---|:---|:---|
| How much of the **original three-unit bank** survives? | $\sqrt{3}VI \div 3VI$ | **57.7%** |
| How hard are the **two surviving units** worked? | $\sqrt{3}VI \div 2VI$ | **86.6%** |

Both are correct. The bank lost 42.3% of its capacity, yet each survivor runs at only 86.6% of its own nameplate, not 100%. The missing 13.4% is lost to the phase relationships, not to any physical limit.

#### Why the survivors cannot be pushed to 100%

In the V-V bank the two transformers do **not** operate at the load power factor. One works at $\cos(30°-\phi)$ and the other at $\cos(30°+\phi)$:

| Load p.f. | Transformer 1 p.f. | Transformer 2 p.f. |
|:---|:---|:---|
| 1.0 | 0.866 | 0.866 |
| 0.866 lag | 1.0 | 0.5 |
| 0.5 lag | 0.866 | 0 |

At 0.5 lagging, one transformer delivers **zero real power**. It carries current and heats up while contributing nothing. This unequal sharing is what caps the bank at 86.6% per unit, and even at unity load p.f. the $\cos 30° = 0.866$ penalty is unavoidable.

#### Practical limits

Secondary voltages drift slightly out of balance as load rises, because the two units have different internal drops at their different power factors. Open delta is therefore an **emergency or light-load** arrangement, tolerated only until the failed unit can be replaced. It is also used deliberately where load is expected to grow, by installing two units now and adding the third later.

> [!warning] When it does **not** work
> If the original bank was **Y-Y**, losing one phase **kills** the supply, because there is no closed delta to let the third line voltage appear. So the answer to the question is conditional: **yes for a $\Delta$-$\Delta$ (or with a tertiary delta), no for an isolated-neutral Y-Y bank.**

---

### Q4(c): Two T-connected transformers for a 440 V, 33 kVA load from a 3300 V supply **[CO2, Marks: 04]**

> Two T-connected transformers are used to supply a 440 V, 33KVA balanced load from a balanced 3-$\varphi$ supply of 3300 V. Calculate:
> (i) voltage and current rating of each coil.
> (ii) KVA rating of the main and teaser transformer.

#### What a T-connection (T-T connection) is, and why it exists

The T-T connection (Scott connection for 3-$\varphi$ to 3-$\varphi$ transformation) uses **two single-phase transformers** to transform a 3-phase supply to a 3-phase load at a different voltage:
- The **main transformer ($T_1$)** is connected directly across two line terminals (say lines A–B). Its primary and secondary windings are both center-tapped at **50% (midpoint $M$)**.
- The **teaser transformer ($T_2$)** is connected between the third line terminal (phase C) and the center tap $M$ of the main transformer.

#### Step 1: System line currents

The load is balanced 3-$\varphi$ ($S = 33\text{ kVA}$, $V_{2L} = 440\text{ V}$), and the supply is balanced 3-$\varphi$ ($V_{1L} = 3300\text{ V}$).

- Secondary (load) line current:
  $$I_{2L} = \frac{S}{\sqrt{3}\,V_{2L}} = \frac{33000}{\sqrt{3}\times440} = \frac{33000}{762.10} = \mathbf{43.30\text{ A}}$$
- Primary (supply) line current:
  $$I_{1L} = \frac{S}{\sqrt{3}\,V_{1L}} = \frac{33000}{\sqrt{3}\times3300} = \frac{10}{\sqrt{3}} = \mathbf{5.77\text{ A}}$$

#### (i) Voltage and current rating of each coil

**1. Main transformer ($T_1$):**
- **Primary winding:** Sits directly across supply lines A–B, so it sees the full line voltage $3300\text{ V}$ and carries the line current:
  $$V_{1,\text{main}} = 3300\text{ V}, \qquad I_{1,\text{main}} = 5.77\text{ A}$$
- **Secondary winding:** Sits directly across load lines a–b, delivering the full line voltage $440\text{ V}$ and carrying the load line current:
  $$V_{2,\text{main}} = 440\text{ V}, \qquad I_{2,\text{main}} = 43.30\text{ A}$$

**2. Teaser transformer ($T_2$):**
- **Voltage ratings:** In an equilateral voltage triangle of side $V_L$, the distance from the midpoint of one side to the opposite vertex is the altitude $h = \frac{\sqrt{3}}{2} V_L \approx 0.866 V_L$. It is **not** $V_L/\sqrt{3}$ (which is the distance to the centroid/star point):
  $$V_{1,\text{teaser}} = \frac{\sqrt{3}}{2} V_{1L} = \frac{\sqrt{3}}{2} \times 3300 = \mathbf{2858\text{ V}} \quad (\approx 2857.9\text{ V})$$
  $$V_{2,\text{teaser}} = \frac{\sqrt{3}}{2} V_{2L} = \frac{\sqrt{3}}{2} \times 440 = \mathbf{381\text{ V}} \quad (\approx 381.05\text{ V})$$
- **Current ratings:** Phase C of the supply connects directly to the outer terminal of the primary teaser winding, and phase c of the load connects directly to the outer terminal of the secondary teaser winding. Therefore, both windings carry the full line current:
  $$I_{1,\text{teaser}} = I_{1L} = \mathbf{5.77\text{ A}}$$
  $$I_{2,\text{teaser}} = I_{2L} = \mathbf{43.30\text{ A}}$$

| Transformer | Coil | Voltage Rating | Current Rating |
|:---|:---|:---:|:---:|
| **Main ($T_1$)** | Primary | $3300\text{ V}$ | $5.77\text{ A}$ |
| | Secondary | $440\text{ V}$ | $43.30\text{ A}$ |
| **Teaser ($T_2$)** | Primary | $\dfrac{\sqrt{3}}{2} \times 3300 = 2858\text{ V}$ | $5.77\text{ A}$ |
| | Secondary | $\dfrac{\sqrt{3}}{2} \times 440 = 381\text{ V}$ | $43.30\text{ A}$ |

#### (ii) kVA rating of the main and teaser transformers

**Operating (calculated) ratings:**
- **Main transformer ($T_1$):**
  $$\text{kVA}_{T1} = \frac{V_{1,\text{main}} \times I_{1,\text{main}}}{1000} = \frac{3300 \times 5.7735}{1000} = \mathbf{19.05\text{ kVA}} \quad\left(= \frac{440 \times 43.301}{1000}\right)$$
- **Teaser transformer ($T_2$):**
  $$\text{kVA}_{T2} = \frac{V_{1,\text{teaser}} \times I_{1,\text{teaser}}}{1000} = \frac{2857.9 \times 5.7735}{1000} = \mathbf{16.50\text{ kVA}} \quad\left(= \frac{381.05 \times 43.301}{1000}\right)$$

Notice that the teaser transformer's operating requirement is exactly $0.866$ of the main transformer's rating:
$$\text{kVA}_{T2} = \frac{\sqrt{3}}{2}\,\text{kVA}_{T1} = 0.866 \times 19.05 = 16.50\text{ kVA}$$

$$\boxed{\text{Main } (T_1) = 19.05\text{ kVA}, \qquad \text{Teaser } (T_2) = 16.50\text{ kVA}}$$

#### Commercial interchangeable rating and the 15.5 % oversize

In commercial practice, rather than manufacturing two custom transformers of different ratings, **two identical transformers** are installed so that either unit can serve as main or teaser (interchangeability). 

1. Both transformers must then be sized for the larger rating: **$19.05\text{ kVA}$ each**, with an 86.6% voltage tap provided on the teaser.
2. The total installed transformer capacity is:
   $$\text{Total installed} = 19.05 + 19.05 = \mathbf{38.10\text{ kVA}}$$
3. Comparing this installed rating to the load served:
   $$\text{Oversize factor} = \frac{38.10\text{ kVA}}{33\text{ kVA}} = \frac{2}{\sqrt{3}} = \mathbf{1.155} \quad (\mathbf{15.5\% \text{ oversize}})$$

$$\boxed{\text{Total installed rating (identical units)} = 2 \times 19.05 = 38.1\text{ kVA}, \text{ representing a } 15.5\% \text{ oversize}}$$

---# SECTION - B

## Question 5

### Q5(a): Explain how a rotating field is produced when a balanced 3-$\varphi$ induction motor is connected to a balanced 3-$\varphi$ supply. **[CO3, Marks: 03]**

#### The setup — and the two kinds of angle

Three **identical** stator windings, their magnetic axes spaced $120°$ apart **in space**. They are fed from a balanced 3-$\varphi$ supply, so their currents are $120°$ apart **in time**.

$$\Phi_1 = \Phi_m\sin\omega t \quad \text{(along } 0°)$$
$$\Phi_2 = \Phi_m\sin(\omega t - 120°) \quad \text{(along } 120°)$$
$$\Phi_3 = \Phi_m\sin(\omega t - 240°) \quad \text{(along } 240°)$$

Keep the two angles separate. The $-\!120°$ **inside** the bracket is a time displacement. The "along $120°$" is a space displacement. Both are needed, and mixing them up is the classic source of confusion.

![Three-phase stator layout, the sinusoidal phase flux waveforms, and the phasor positions at successive instants](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_8_06.jpeg)

#### Phasor method: sample four instants

![Vector diagrams of the resultant three-phase flux at theta equal to 0, 60, 120 and 180 degrees, each giving a resultant of 1.5 times the maximum phase flux](../Books/Theraja/Ch-34/diagrams/Ch-34_p10_fig14.jpg)

Each phase flux **pulses** back and forth along its own fixed axis. Nothing rotates yet. Now add them as vectors.

**(i) At $\omega t = 0°$:**
$$\Phi_1 = 0, \qquad \Phi_2 = \Phi_m\sin(-120°) = -0.866\Phi_m, \qquad \Phi_3 = \Phi_m\sin(-240°) = +0.866\Phi_m$$

Phase 1 contributes nothing. The negative sign on $\Phi_2$ means that flux points **opposite** its own axis, i.e. along $300°$; $\Phi_3$ points along $240°$. Those two directions are $60°$ apart, so their resultant bisects them:

$$\Phi_r = 2\times0.866\Phi_m\times\cos 30° = 2\times0.866\times0.866\,\Phi_m = 1.5\Phi_m$$

**(ii) At $\omega t = 60°$:**
$$\Phi_1 = +0.866\Phi_m, \qquad \Phi_2 = -0.866\Phi_m, \qquad \Phi_3 = 0$$
$$\Phi_r = 2\times0.866\Phi_m\times\cos 30° = 1.5\Phi_m$$

**Same magnitude**, but the resultant has swung $60°$ in space.

**(iii) and (iv)** At $\omega t = 120°$ and $180°$ the pattern repeats identically. Each $60°$ of time advance turns the resultant a further $60°$ in space, and the magnitude is always $1.5\Phi_m$.

So the resultant is a vector of **constant magnitude** whose **direction advances uniformly**. That is the definition of a rotating field. After $\omega t = 360°$ it has made one full revolution, so it turns once per electrical cycle:

$$N_s = \frac{120f}{P}\text{ rpm}$$

#### Analytical proof, which covers every instant at once

Four snapshots are suggestive, not conclusive. Resolve all three fluxes onto a fixed pair of axes.

Along the reference ($x$) axis:
$$\Phi_x = \Phi_1 + \Phi_2\cos 120° + \Phi_3\cos 240° = \frac{3}{2}\Phi_m\sin\omega t$$

Along the quadrature ($y$) axis:
$$\Phi_y = \Phi_2\sin 120° + \Phi_3\sin 240° = \frac{3}{2}\Phi_m\cos\omega t$$

Magnitude:
$$\Phi_r = \sqrt{\Phi_x^2+\Phi_y^2} = \frac{3}{2}\Phi_m\sqrt{\sin^2\omega t+\cos^2\omega t}$$

$$\boxed{\Phi_r = 1.5\,\Phi_m = \text{constant, for every value of } t}$$

Direction:
$$\theta = \tan^{-1}\frac{\Phi_y}{\Phi_x} = 90° - \omega t, \qquad \frac{d\theta}{dt} = -\omega = \omega$$

Constant magnitude, uniformly turning direction. A rotating field, proved for all time rather than four instants.

#### Where the 1.5 comes from, and the general rule

Three windings give $1.5\Phi_m$, not $3\Phi_m$, because half the contribution is lost to the $120°$ space displacement. The general rule for an $m$-phase machine is

$$\Phi_r = \frac{m}{2}\Phi_m$$

For $m=3$ that is $1.5$. For $m=2$ it is $1.0$ — which is exactly why a true **two-phase** supply also produces a rotating field, and why every practical single-phase motor (Q6(b)) must *fake* a second phase.

#### Why this is the whole reason a 3-$\varphi$ motor is self-starting

A pulsating field along one fixed axis produces torque that **reverses** every half cycle and averages to **zero**. A rotating field always drags the rotor one way. So the 3-$\varphi$ motor has starting torque without any help, while a 1-$\varphi$ motor has none at all. Q6(b) develops the contrast.

#### Reversing the direction

Swap any two supply leads. That exchanges the time sequence of two phases and the resultant rotates the other way. One wiring change reverses the motor, with no mechanical alteration.

---

### Q5(b): Define slip. Prove that an induction motor cannot run at synchronous speed. **[CO3, Marks: 03]**

#### Defining slip

$$s = \frac{N_s - N}{N_s}, \qquad \%s = \frac{N_s - N}{N_s}\times100, \qquad N_s = \frac{120f}{P}$$

$N_s$ is the speed of the rotating field (synchronous speed) and $N$ is the actual rotor speed. The numerator $(N_s - N)$ is the **slip speed**, the rate at which the field slips past the rotor. Normalising against $N_s$ makes slip dimensionless, running from 1 at standstill to 0 at synchronous speed.

Slip is not a defect to be eliminated. It is the machine's **working variable**. Without slip there is no output at all, as the proof below shows.

#### The proof, as a chain of consequences

Argue by contradiction. Suppose the rotor somehow reaches $N = N_s$, so $s = 0$.

**1. Relative speed vanishes.** $N_s - N = 0$. The field and the rotor conductors travel together, so from the rotor's frame the field is **standing still**.

**2. No flux is cut, so no emf is induced.** Faraday's law needs **relative** motion:
$$E_{2r} = sE_2 = 0$$

**3. No emf means no current.**
$$I_{2r} = \frac{sE_2}{\sqrt{R_2^2 + (sX_2)^2}} = \frac{0}{R_2} = 0$$

**4. No current means no force.** Torque comes from the interaction of the stator field with rotor current, $F = BIl$:
$$T = k\,\Phi\,I_{2r}\cos\phi_2 = 0$$

**5. The contradiction.** The motor now develops **zero torque**. But friction and windage always demand some torque, even with nothing on the shaft. With nothing to oppose them, the rotor **must** decelerate.

**6. The system self-corrects.** The instant $N < N_s$, slip becomes positive again, and relative motion, emf, current and torque all return. The rotor settles at whatever slip makes the developed torque equal the opposing torque.

$$\boxed{N < N_s \text{ always, so } s > 0. \text{ The induction motor is an asynchronous machine.}}$$

#### Why slip is small in normal running

Full-load slip is typically 2% to 5%. A 4-pole 50 Hz motor has $N_s = 1500$ rpm, so it runs at roughly 1440 rpm. Only a few percent of relative motion is needed, because the torque curve is very steep in the working region: a large change in torque produces only a small change in speed. That is why an induction motor behaves almost like a constant-speed machine.

#### Slip as the machine's feedback signal

Load the shaft and the motor slows slightly. More slip means more rotor emf, more rotor current and more torque, until torque matches the new load. The motor finds its own operating point without any controller. (That feedback is the 1:1 rotor copper loss relationship, $P_{cu2} = sP_2$, developed in the 2023 paper.)

#### Why zero slip is still a useful idea

It marks the boundary between motoring and generating. Push the rotor **above** $N_s$ with a prime mover and $s$ goes negative. The emf reverses, the current reverses and the torque reverses. The machine becomes an **induction generator**, which is exactly what Q8(b) and Q8(c) do.

---

### Q5(c): Full-load speed of an 8-pole motor fed from a 12-pole alternator **[CO3, Marks: 04]**

> A 12 pole, 3-$\varphi$ alternator driven at a speed of 500 r.p.m supplies power to an 8-pole, 3-$\varphi$ induction motor. If the slip of the motor, at full load is 3%, calculate the full-load speed of the motor.

#### What the question is really testing

There is **no supply frequency stated**. It has to be recovered from the alternator, because the alternator's speed *and* pole count together define the frequency it generates. Get that wrong and every later number is wrong.

#### Step 1: frequency from the alternator

An alternator of $P$ poles turning at $N$ rpm generates $f = \frac{PN}{120}$ Hz, rearranged from $N_s = 120f/P$:

$$f = \frac{12\times500}{120} = \frac{6000}{120} = 50\text{ Hz}$$

So the chain simply transmits a standard 50 Hz supply; that was the point of giving the alternator's pole count and speed.

#### Step 2: synchronous speed of the 8-pole motor

$$N_s = \frac{120f}{P} = \frac{120\times50}{8} = \frac{6000}{8} = 750\text{ rpm}$$

#### Step 3: apply the slip

Slip is $3\% = 0.03$, so the full-load speed is

$$N = N_s(1-s) = 750\times(1-0.03) = 750\times0.97$$

$$\boxed{N_{FL} = 727.5\text{ rpm}}$$

#### Checks on the answer

1. **Less than synchronous speed.** $727.5 < 750$ ✓, as part (b) proved it must be.
2. **A whole number.** A synchronous speed of 750 rpm at 8 poles is exact, and 3% of it is 22.5 rpm, so the slip in rpm is a clean 22.5. The answer 727.5 rpm is therefore exact, not rounded.
3. **The chain is transparent:** 12-pole alternator at 500 rpm gives 50 Hz; 8-pole motor at 50 Hz has $N_s = 750$ rpm; 3% slip gives 727.5 rpm. Each step uses one formula and nothing else.

> [!note] A note on the setup
> This is not a direct-on-line arrangement; the motor is fed at line frequency from an alternator whose speed sets that frequency. In practice a 12-pole alternator running at 500 rpm would be a **hydro generator**, because 500 rpm is a low, high-speed-per-pole value suited to water turbines. The question is really just a two-stage frequency-and-speed chain.

---

## Question 6

### Q6(a): Define starting and running torque of an induction motor (IM). **[CO1, Marks: 02]**

#### Starting torque

**Starting torque** $T_{st}$ (also called **locked-rotor** or **stall** torque) is the torque developed by an induction motor **at the instant of starting**, when the rotor is stationary and therefore $s = 1$.

$$T_{st} = k\,\frac{E_2^2 R_2}{R_2^2 + X_2^2}$$

It is fixed by the voltage (through $E_2^2$), the rotor resistance and the standstill rotor reactance.

#### Running torque

**Running torque** $T$ is the torque developed at any running slip $s$, once the rotor has accelerated. In the general form,

$$T = k\,\frac{s E_2^2 R_2}{R_2^2 + (sX_2)^2}$$

The $s$ in the numerator is what distinguishes running torque from starting torque: as the rotor speeds up, slip falls, and the torque first **rises** from $T_{st}$ to a peak (the breakdown or pull-out torque at $s = R_2/X_2$) and then falls as $s\to0$.

#### A table that captures both definitions and their relation

| Quantity | Slip | Expression |
|:---|:---|:---|
| Starting (locked-rotor) torque $T_{st}$ | $s = 1$ | $T_{st} = k E_2^2 R_2/(R_2^2+X_2^2)$ |
| Maximum (breakdown) torque $T_{\max}$ | $s = R_2/X_2$ | $T_{\max} = k E_2^2/(2X_2)$ |
| Running / full-load torque $T_{FL}$ | $s = s_F$ | $T = k s_F E_2^2R_2/(R_2^2 + s_F^2X_2^2)$ |

#### Key relationships worth writing

- **Torque depends on the square of the applied voltage:** $T \propto V^2$. Halving the voltage reduces torque to one quarter. This is why starting methods (star-delta, auto-transformer) that cut voltage also cut torque proportionally.
- **$T_{max}$ does not depend on $R_2$ at all** — see Q7(b) for the proof. Rotor resistance moves the peak along the speed axis but cannot change its height.
- **Starting torque is limited by rotor power factor.** At $s=1$ the reactance $sX_2 = X_2$ is at its largest, so the rotor power factor $\cos\phi_2$ is at its worst. This is why, even though starting current is 5–7 times rated, the starting torque is only about 1.5–2 times rated torque.

#### Why these two quantities dominate motor selection

- **$T_{st}$** decides whether the motor can break its load away from rest. A compressor or conveyor demands high starting torque; a fan or centrifugal pump demands almost none (its torque rises as the square of speed, so it is near zero at standstill).
- **$T_{\max}$ (running peak)** decides whether the motor can survive a **temporary** overload such as a jam, a stuck conveyor, or a sudden load surge, without stalling. Good practice demands the load torque stay below $T_{\max}$ even transiently.
- Between them lies the **stable operating region**, from just beyond $T_{\max}$ down to $N_s$, which is steep and nearly straight. That steepness is why the induction motor holds its speed almost constant under varying load.

---

### Q6(b): Draw and describe the vector diagram of a 1-$\varphi$ IM. **[CO1, Marks: 04]**

#### Why a 1-$\varphi$ motor needs a vector diagram built from two fields

A single-phase supply gives **one** pulsating flux, not a rotating one. By the **double-field revolving theory**, that pulsating flux is exactly equivalent to **two** rotating fields of equal magnitude $\Phi_m/2$ turning in **opposite** directions at synchronous speed.

![Resolution of an alternating pulsating flux into two equal flux components rotating in opposite directions](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_03.jpeg)

The vector diagram is drawn for these two fields separately, and the net torque is the vector difference of the two torques they develop.

#### The statement and why the resolution is exact

A single stator winding produces $\Phi = \Phi_m\cos\omega t$. Write it as two counter-rotating vectors, each of length $\Phi_m/2$:

$$\Phi_f = \frac{\Phi_m}{2}\angle+\omega t, \qquad \Phi_b = \frac{\Phi_m}{2}\angle-\omega t$$

Resolve each along the winding axis and perpendicular to it. The **perpendicular** components, $\pm\frac{\Phi_m}{2}\sin\omega t$, always cancel. The **along-axis** components, $2\times\frac{\Phi_m}{2}\cos\omega t$, always add to $\Phi_m\cos\omega t$. So at every instant the two rotating vectors sum exactly to the original pulsating flux. The resolution is an identity, not an approximation — which is what makes the theory legitimate.

#### The two torques and their slips

Let the rotor turn forward at $N$. The **forward** field turns at $+N_s$, the **backward** field at $-N_s$.

$$s_f = \frac{N_s - N}{N_s} = s$$
$$s_b = \frac{N_s - (-N)}{N_s} = \frac{N_s + N}{N_s} = 2 - s$$

The forward field drags the rotor forward, giving $+T_f$. The backward field drags it backward, giving $-T_b$. So

$$T = T_f - T_b$$

![Torque-speed curves of the forward field and the backward field, with the resultant curve showing zero net torque at standstill](../Books/VK_Mehta/diagrams/VK_Mehta_Fig_9_04.jpeg)

#### The two cases on the diagram

**At standstill, $N = 0$, so $s = 1$ and $s_b = 1$.** Both fields see **identical** slip. They are mirror images in every respect: same magnitude, same slip, same rotor impedance. So they produce equal and opposite torques:

$$T_f = T_b \implies T_{st} = 0$$

$$\boxed{\text{A single-phase induction motor has zero starting torque. It is not self-starting.}}$$

The rotor hums, draws current and heats up, but does not turn.

**Once it is moving** (pushed forward, so $N>0$, $s<1$):

- **Forward** field: small slip $s_f = s$. Rotor circuit mainly resistive, good $\cos\phi_2$, large $T_f$. This is the useful, efficient part.
- **Backward** field: slip $s_b = 2 - s$, close to 2. The rotor reactance $s_b X_2$ is nearly **twice** its standstill value, so rotor power factor is terrible and $T_b$ collapses.

So $T_f \gg T_b$, net torque is strongly positive, and the motor runs up to near synchronous speed.

#### Why the losses are worse than a 3-$\varphi$ motor

| Consequence | Explanation |
|:---|:---|
| Lower efficiency | The backward field induces extra rotor current that does no useful work but dissipates heat. |
| Lower power factor | Two flux components instead of one magnetising the core, drawing more magnetising current. |
| Larger frame for the same output | Must accommodate the extra backward-field heating. |
| Double-frequency torque pulsation | Forward and backward torques pulsate at $2f$, so the motor hums and vibrates. |
| Larger starting capacitor needed | Must fake a strong second phase just to overcome the zero starting torque. |

#### What every 1-$\varphi$ motor design is really doing

The motor only needs a **push**. Every practical single-phase motor (split-phase, capacitor-start, capacitor-run, shaded-pole, repulsion-start) is therefore just a scheme for producing that push, almost always by creating a **faux second phase** displaced in time (and space) from the main winding, so that the resultant becomes a rotating (elliptical or nearly circular) field for the first few seconds of running.

That, and the fact that it runs equally well in **either** direction once started (spin it backwards and it runs backwards), is the direct payoff of the vector diagram above.

---

### Q6(c): Slip-ring induction motor rotor current and maximum-torque condition **[CO2, Marks: 04]**

> A 3-$\varphi$, slip-ring IM with star-connected rotor has an induced emf of 120 volts between slip-rings at standstill with normal voltage applied to the stator. The rotor winding has a resistance per phase of $0.3\ \Omega$ and stand-still leakage reactance per phase of $1.5\ \Omega$. Determine:
> (i) Rotor current/phase when running short circuited with 4% slip and
> (ii) The slip and rotor current per phase when the rotor is developing maximum torque.

#### The trap: 120 V is **line** voltage, not phase voltage

"120 volts **between slip-rings**" is the wording, and it is deliberate. Slip rings connect to the three rotor **line** ends. The rotor is **star-connected**, so:

$$E_{2,ph} = \frac{120}{\sqrt{3}} = 69.28\text{ V}$$

Using 120 V as the phase voltage would overstate every rotor current by $\sqrt{3}$, a factor-of-1.73 error.

#### Why the rotor quantities scale with slip

Under running conditions the rotor sees only the **slip frequency** $sf$, so:
$$E_{2r} = sE_2, \qquad X_{2r} = sX_2, \qquad R_2 \text{ unchanged (resistance is frequency-independent)}$$

$$I_{2r} = \frac{sE_2}{\sqrt{R_2^2 + (sX_2)^2}}$$

That single expression answers part (i). For part (ii) we need the condition for maximum torque.

#### (i) Rotor current per phase at 4% slip, rotor short-circuited

Short-circuited means the rotor circuit is closed through the slip rings (or internally), so the full rotor emf drives current through $R_2 + jX_{2r}$.

**Step 1: rotor emf at 4% slip.**
$$E_{2r} = sE_{2,ph} = 0.04 \times 69.28 = 2.771\text{ V}$$

**Step 2: rotor impedance at 4% slip.** The reactance scales with slip, the resistance does not.
$$X_{2r} = sX_2 = 0.04\times1.5 = 0.06\ \Omega$$
$$|Z_{2r}| = \sqrt{R_2^2 + X_{2r}^2} = \sqrt{0.3^2 + 0.06^2} = \sqrt{0.09 + 0.0036} = \sqrt{0.0936} = 0.30594\ \Omega$$

**Step 3: current.**
$$I_{2r} = \frac{2.771}{0.30594} = 9.06\text{ A}$$

$$\boxed{I_{2r} = 9.06\text{ A per phase at } s = 4\%}$$

**A sanity check.** Note how small $X_{2r} = 0.06\ \Omega$ is compared with $R_2 = 0.3\ \Omega$. At 4% slip the rotor circuit is **strongly resistive**, so the rotor power factor is high (about $\cos\phi_2 = 0.3/0.306 = 0.98$), which is exactly why running torque is efficient at low slip.

#### (ii) Slip and rotor current at maximum torque

The condition for maximum torque is that the rotor resistance equals the rotor reactance at that slip, i.e. the rotor impedance angle is $45°$:

$$s_{maxT} = \frac{R_2}{X_2}$$

**Step 1: slip at maximum torque.**
$$s_{maxT} = \frac{0.3}{1.5} = 0.2 = 20\%$$

$$\boxed{s_{maxT} = 0.2\;(20\%)}$$

**Step 2: rotor impedance at that slip.** At maximum torque $s_{maxT}X_2 = R_2$, so $R_2$ and the reactance are equal:

$$X_{2r} = s_{maxT}X_2 = 0.2\times1.5 = 0.3\ \Omega = R_2$$
$$|Z_{2r}| = \sqrt{0.3^2 + 0.3^2} = \sqrt{0.18} = 0.42426\ \Omega$$

**Step 3: rotor emf at that slip.**
$$E_{2r} = s_{maxT}E_{2,ph} = 0.2\times69.28 = 13.856\text{ V}$$

**Step 4: rotor current.**
$$I_{2r} = \frac{13.856}{0.42426} = 32.7\text{ A}$$

$$\boxed{I_{2r} = 32.7\text{ A per phase, at } s = 20\%}$$

#### The physical picture behind the two answers

| | At $s = 4\%$ (part i) | At $s = 20\%$ (part ii, max torque) |
|:---|:---|:---|
| Rotor emf $sE_2$ | 2.77 V | 13.86 V |
| Rotor reactance $sX_2$ | 0.06 Ω | 0.30 Ω |
| Resistance $R_2$ | 0.30 Ω | 0.30 Ω |
| Rotor circuit | Strongly resistive, $\cos\phi_2\approx0.98$ | $R=X$, $\cos\phi_2 = 0.707$ |
| Rotor current | 9.06 A | 32.7 A |

At maximum torque the rotor reactance has grown until it **equals** the resistance. That is the geometric statement behind $s_{maxT} = R_2/X_2$, and it is also why $T_{\max}$ is independent of $R_2$: at the peak, $R_2$ cancels against itself.

Also note $20\% > 4\%$: the maximum-torque slip lies **well above** the full-load slip, so a normal motor operates on the stable, descending side of the torque curve, far from the breakdown point. And because the rotor is **slip-ring** (wound), an external resistance can be added at the rings to *move* this $20\%$ point to any higher slip — that is the basis of rotor-resistance speed control.

---

## Question 7

### Q7(a): Enlist the test's name used for determining circuit model parameters of an IM. **[CO1, Marks: 02]**

#### Why tests are needed at all

The equivalent circuit of an induction motor contains six parameters ($R_1, X_1, R_0, X_m, R_2', X_2'$), and none of them is marked on the nameplate. They are normally **hidden** inside the machine, whose only accessible terminals are the three stator leads. So each parameter must be inferred by observing how the machine behaves at a carefully chosen speed.

#### The three tests

| Test | Rotor condition | What is applied | Parameters obtained |
|:---|:---|:---|:---|
| **No-load test** | Free-running, uncoupled ($s\approx0$) | Rated voltage and frequency | $R_c$ (or $R_0$), $X_m$ (and, with the speed read, the mechanical losses) |
| **Blocked-rotor test** (locked-rotor, short-circuit test) | Rotor mechanically locked, $s = 1$ | Reduced voltage (10–15% of rated) to circulate rated current | $R_{01}, X_{01}$, and hence $R_2', X_2'$ |
| **DC (or stator-resistance) test** | Rotor need not move; stator alone | A DC supply applied to the stator winding | $R_1$ (from $V/I$ corrected for temperature), then $R_2' = R_{01} - R_1$ |

#### Why each test isolates its own parameters

**No-load test.** Because the rotor is free, slip is tiny and the rotor branch is effectively an open circuit, so **all** the input current flows in the excitation branch. The no-load power factor is poor, and splitting $I_0$ gives
$$R_c = \frac{V_\phi}{I_c}, \qquad X_m = \frac{V_\phi}{I_m}$$
with $I_c = I_0\cos\phi_0$ and $I_m = I_0\sin\phi_0$. The measured power is nearly all iron loss (plus friction and windage), which is why the running speed must also be read to separate them.

![Complete equivalent circuit showing the stator branch R1 + jX1 in series with the parallel combination of the core-loss resistance and magnetising reactance, and the rotor branch referred to the stator](../Books/Theraja/Ch-34/diagrams/Ch-34_p58_fig45.jpg)

**Blocked-rotor test.** Locking the rotor makes $s = 1$, so the fictitious mechanical-load resistance $R_2(1-s)/s$ **vanishes** and the rotor branch collapses to a plain short-circuited impedance $R_2' + jX_2'$. That is why the blocked-rotor test on a motor is the exact twin of the short-circuit test on a transformer. Because the applied voltage is only 10–15% of rated, the flux — and hence the iron loss — is negligible, so the measured power is essentially copper loss:
$$R_{01} = \frac{P_{sc}}{3I_{sc}^2}, \qquad X_{01} = \sqrt{\left(\frac{V_{sc}}{\sqrt{3}I_{sc}}\right)^2 - R_{01}^2}$$
Normally one assumes $X_1 = X_2' = X_{01}/2$ to separate them.

**DC test.** Passing DC through the stator winding at standstill excites no flux in the short-circuited rotor (DC cannot induce anything) and no iron loss, so the only thing the ammeter sees is the stator copper loss. Hence $R_1 = V/I$ (with a correction for the fact that at DC the current heats the winding, raising its resistance). Once $R_1$ is known, $R_2' = R_{01} - R_1$.

![Per-phase equivalent circuit during the blocked-rotor test, showing the simplified series circuit of R1 + R2' and jX1 + jX2' used to compute the test parameters](../Books/Theraja/Ch-34/diagrams/Ch-34_p58_fig45.jpg)

#### An additional method worth naming

For a machine where a **direct load test** is possible (small motors only), the parameters can be obtained from a set of measured input points using a **circle diagram**, as developed in the 2023 paper. It is graphical rather than instrumental, and it is really a *load* test rather than one of the three above.

#### Why not a direct load test?

A direct load test would give the answer straight away, but it needs a full-rated load absorbing the full kVA continuously, which is expensive and impractical for anything but small motors. The three tests above consume only the **losses** themselves — tens of watts instead of tens of kilowatts — and yet yield the parameters, from which efficiency and regulation at **any** load and **any** power factor can be computed afterwards.

---

### Q7(b): Prove that $T_{\max} = \frac{3}{2\pi N_s}\frac{E_2^2}{2X_2}$ N-m **[CO1, Marks: 04]**

$$T_{\max} = \frac{3}{2\pi N_s} \frac{E_2^2}{2X_2}\ \text{N-m}$$

#### Step 1: start from the torque equation

The general torque of a three-phase induction motor, in terms of the rotor quantities and slip, is

$$T = \frac{3}{\omega_s}\cdot\frac{sE_2^2 R_2}{R_2^2 + s^2 X_2^2}, \qquad \omega_s = 2\pi N_s$$

where $E_2$ and $X_2$ are the rotor **standstill** emf and leakage reactance per phase. Since $\frac{3}{\omega_s} = \frac{3}{2\pi N_s}$, this already contains the required prefactor.

The part that matters for the proof is the slip-dependent bracket. All the constant factors are constants, so **maximising $T$ is the same as maximising**

$$f(s) = \frac{sR_2}{R_2^2 + s^2 X_2^2}$$

#### Step 2: differentiate and set to zero

Using the quotient rule,

$$\frac{df}{ds} = \frac{R_2(R_2^2+s^2X_2^2) - sR_2(2sX_2^2)}{(R_2^2+s^2X_2^2)^2}$$

At an extremum the numerator vanishes:

$$R_2(R_2^2 + s^2X_2^2) - sR_2(2sX_2^2) = 0$$

Divide by $R_2 \ne 0$:

$$R_2^2 + s^2X_2^2 - 2s^2X_2^2 = 0$$
$$R_2^2 = s^2X_2^2$$

$$\boxed{s_{maxT} = \frac{R_2}{X_2}}$$

#### Step 3: confirm it is a maximum, not a minimum

We must not stop here. Intuitively the torque must vanish at both $s=0$ (no slip, no torque — Q5(b)) and at very large $s$, so any interior stationary point is a maximum. Algebraically, evaluate the bracket at a test point between the ends. At $s = R_2/X_2$ the bracket is positive; as $s\to0$ and $s\to\infty$ it tends to zero. So the stationary point is a maximum.

#### Step 4: substitute back and simplify

Insert $s_{maxT} = R_2/X_2$ into the torque equation.

**Numerator:**
$$s_{maxT}E_2^2R_2 = \frac{R_2}{X_2}E_2^2R_2 = \frac{R_2^2E_2^2}{X_2}$$

**Denominator:**
$$R_2^2 + s_{maxT}^2X_2^2 = R_2^2 + \frac{R_2^2}{X_2^2}X_2^2 = R_2^2 + R_2^2 = 2R_2^2$$

Therefore

$$T_{\max} = \frac{3}{2\pi N_s}\cdot\frac{\dfrac{R_2^2E_2^2}{X_2}}{2R_2^2} = \frac{3}{2\pi N_s}\cdot\frac{E_2^2}{2X_2}$$

$$\boxed{T_{\max} = \frac{3}{2\pi N_s}\frac{E_2^2}{2X_2}\ \text{N-m}}$$

*(Proved)*

#### The result that falls out of the proof

Look at what happened to $R_2$. It appeared in the numerator as $R_2^2$ and in the denominator as $2R_2^2$, and **it cancelled completely**.

$$\boxed{T_{\max}\ \text{is independent of rotor resistance } R_2}$$

So the two results must always be quoted as a pair:

| Quantity | Depends on $R_2$? | Value |
|:---|:---|:---|
| **Where** the peak occurs, $s_{maxT}$ | **Yes** | $R_2/X_2$ |
| **How high** the peak is, $T_{\max}$ | **No** | $3E_2^2/(4\pi N_s X_2)$ |

#### Why this is the key fact of rotor-speed control

Because $T_{\max}$ cannot be changed by any rotor resistance, you cannot raise the peak torque by adding resistance. What you *can* do is slide the peak along the speed axis. For a wound-rotor (slip-ring) motor this means maximum torque can be made to occur at **any** speed below synchronous speed, which is the basis of:

- **Rotor-resistance speed control.** The classic stepless method: maximum torque can be delivered at any desired speed. Simple and robust, but wasteful — the extra resistance dissipates real power as heat, so efficiency falls badly at low speed. This is exactly why variable-frequency drives displaced it.
- **Improved starting.** By choosing $R_{ext} = X_2 - R_2$, the maximum-torque condition $s_{maxT} = (R_2+R_{ext})/X_2$ becomes $s_{maxT} = 1$, i.e. **maximum torque is developed at standstill**. Starting torque then equals $T_{\max}$ instead of the usual 1.5–2 times rated.
- **Double-cage and deep-bar rotors.** These achieve a similar effect without external resistors, by relying on the skin effect to raise the effective rotor resistance at starting and lower it at running.

#### Variables and their usual meanings

| Symbol | Meaning |
|:---|:---|
| $N_s$ | Synchronous speed, rpm |
| $E_2$ | Rotor induced emf **per phase at standstill**, V |
| $X_2$ | Rotor leakage reactance **per phase at standstill**, $\Omega$ |
| $R_2$ | Rotor resistance per phase, $\Omega$ |
| $s$ | Slip, per unit |
| $T_{\max}$ | Maximum (breakdown / pull-out) torque, N-m |

---

### Q7(c): Ratio of maximum to full-load torque, and speed at maximum torque **[CO3, Marks: 04]**

> A 50 Hz, 8 pole induction motor has F.L. slip of 4%. The rotor resistance/phase $= 0.01\ \Omega$ and stand still reactance/phase $= 0.1\ \Omega$. Find the ratio of maximum to full-load torque and the speed at which the maximum torque occurs.

#### Step 1: synchronous speed

$$N_s = \frac{120f}{P} = \frac{120\times50}{8} = 750\text{ rpm}$$

The full-load speed would be $750(1-0.04) = 720$ rpm, but the question asks for the speed at **maximum** torque, so hold that thought.

#### Step 2: slip at maximum torque

From the proof in part (b):

$$s_{maxT} = \frac{R_2}{X_2} = \frac{0.01}{0.1} = 0.1$$

So the breakdown torque occurs at **10% slip**, well above the 4% full-load slip, as it must be for a stable operating point.

#### Step 3: a form of the torque equation that avoids computing $E_2$ entirely

The problem gives no $E_2$, so the absolute torques are out of reach. But only a **ratio** is asked for, and $E_2$ cancels out of any such ratio. Write the torque as

$$T \propto \frac{sR_2}{R_2^2+s^2X_2^2}$$

Divide numerator and denominator by $sX_2$... more usefully, substitute $s_{maxT} = R_2/X_2$ once to get the standard normalised form:

$$\frac{T}{T_{\max}} = \frac{2}{\dfrac{s}{s_{maxT}} + \dfrac{s_{maxT}}{s}}$$

**Where does this come from?** Take the ratio of the torque expression at general $s$ to the same expression at $s_{maxT}$. Writing $a = s/s_{maxT}$ and using $R_2 = s_{maxT}X_2$:

$$T(s) = k\,\frac{s\,s_{maxT}X_2^2}{X_2^2(s_{maxT}^2 + s^2)}, \qquad T_{max} = \frac{kE_2^2}{2X_2}$$

Substituting $E_2^2 = R_2^2/s_{maxT}^2\cdot X_2^2$ and simplifying gives exactly the form above. Its merit is that it depends on **only** the ratio $s/s_{maxT}$.

Two quick checks on it:
- At $s = s_{maxT}$: $T/T_{max} = 2/(1+1) = 1$ ✓
- At $s = s_{maxT}/2$: $T/T_{max} = 2/(0.5+2) = 0.8$. Known result: torque at half the breakdown slip is $0.8T_{max}$ ✓

#### Step 4: evaluate at full load, $s = 0.04$

$$\frac{s}{s_{maxT}} = \frac{0.04}{0.1} = 0.4, \qquad \frac{s_{maxT}}{s} = \frac{0.1}{0.04} = 2.5$$

$$\frac{T_{FL}}{T_{\max}} = \frac{2}{0.4 + 2.5} = \frac{2}{2.9} = 0.6897$$

$$\boxed{\frac{T_{\max}}{T_{FL}} = 1.45}$$

#### Step 5: speed at maximum torque

$$N_{maxT} = N_s(1 - s_{maxT}) = 750(1-0.1) = 750\times0.9$$

$$\boxed{N_{maxT} = 675\text{ rpm}}$$

#### What the answers mean

**A breakdown torque only 1.45 times rated is low but not unusual.** Practical guidance is $T_{max} \ge 1.6$ to $2.5\,T_{FL}$ for general-purpose motors. A ratio of 1.45 means the motor can absorb a load **surge** of about 45% above rated for a moment before stalling, and nothing more. It also means the motor is being run fairly close to its breakdown point during transient overloads, which is why such a motor would not be chosen for a load with large transients (a crusher, a reciprocating compressor) without adding rotor resistance or going to a larger frame.

**The speeds bracket the operating point:**

| Point | Slip | Speed |
|:---|:---|:---|
| Full load | 4% | 720 rpm |
| Maximum torque | 10% | 675 rpm |
| Synchronous (unattainable) | 0% | 750 rpm |

Full load sits between breakdown and synchronous speed, on the **stable** side of the torque peak. That is the normal condition, and it is what makes the induction motor self-regulating: if the load torque rises, speed falls, slip rises, torque rises, until balance is restored.

> [!note] Independent cross-check on $T_{max}/T_{FL}$
> Using the raw form directly: with $R_2 = 0.01$, $X_2 = 0.1$, $R_2/X_2 = 0.1$, and the $sR_2/(R_2^2+s^2X_2^2)$ bracket:
> - At $s=0.04$: $\dfrac{0.04\times0.01}{0.0001+0.0016\times0.01} = \dfrac{0.0004}{0.000116} = 3.448$
> - At $s=0.1$: $\dfrac{0.1\times0.01}{0.0001+0.01\times0.01} = \dfrac{0.001}{0.0002} = 5.0$
> - Ratio: $5.0/3.448 = 1.45$ ✓ Same answer.

---

## Question 8

### Q8(a): Draw the torque ~ slip of 3-$\varphi$ induction machine. **[CO1, Marks: 02]**

#### What the full torque-slip curve shows

Unlike the torque-speed curve of a DC motor, the induction motor's characteristic is **not** a straight line. Plotted against **slip** rather than speed, it has a definite shape that reveals three distinct operating regimes. Drawing it is the point of this part.

![Complete torque-slip characteristic of a three-phase induction machine covering the braking, motoring and generating regions](../Books/Theraja/Ch-34/diagrams/Ch-34_p34_fig32.jpg)

#### The equation being plotted

$$T = \frac{3E_2^2}{\omega_s}\cdot\frac{sR_2}{R_2^2 + s^2 X_2^2}$$

Every feature of the curve follows from this one expression.

#### The four landmarks, and what causes each

| Point | Slip | Torque | What is happening |
|:---|:---|:---|:---|
| **Origin** | $s = 0$ | $T = 0$ | Synchronous speed. No relative motion, so no emf, no current, no torque (Q5(b)). |
| **Stable, rising branch** | $0 < s < s_{maxT}$ | $0 \to T_{\max}$ | Normal running region. Torque rises steeply with slip. |
| **Breakdown peak** | $s_{maxT} = R_2/X_2$ | $T_{\max} = \frac{3E_2^2}{4\pi N_sX_2}$ | $R_2 = sX_2$, so rotor p.f. $= 0.707$. Independent of $R_2$. |
| **Falling branch** | $s_{maxT} < s < 1$ | $T_{max}\to T_{st}$ | Starting region. Torque collapses as $X_2$ dominates; at $s=1$ is $T_{st}$. |
| **Negative slip** | $s < 0$ | $T < 0$ | **Generating** region. Machine driven above $N_s$; torque opposes the prime mover. |
| **Beyond $s=1$** | $s > 1$ | $T > 0$, braking | **Plugging / reverse-current braking.** Rotor reversed relative to field; power flows in electrically and mechanically, all dissipated as heat. |

#### Why the curve looks the way it does

**Near $s = 0$:** the term $s^2X_2^2$ is negligible, so $T \propto s$. A straight line rising from the origin. This is the "motor" region for light loads.

**Near $s = s_{maxT}$:** the $s^2X_2^2$ term has grown to equal $R_2^2$, and beyond that it dominates, so $T \propto 1/s$. That is why the far side falls hyperbolically rather than linearly.

**At $s = 1$:** $T_{st} = \frac{3E_2^2R_2}{\omega_s(R_2^2+X_2^2)}$. Because at starting $X_2 \gg R_2$ for a normal rotor, $T_{st}$ is only about 1.5 to 2 times rated — far less than $T_{max}$ despite starting current being 5 to 7 times rated.

**For $s < 0$:** put $s = -|s|$ and the numerator changes sign while the denominator stays positive, so $T$ is **negative**. A negative torque opposes the direction of rotation, which is exactly the signature of a generator absorbing mechanical power and delivering electrical power.

#### The shape of the plot to actually draw

1. Horizontal axis $s$, running from about $-0.3$ on the left, through $0$, to $1$ on the right (or $2$ if you want to show plugging).
2. Vertical axis $T$, positive above the axis, negative below.
3. From the origin, a steep straight line rising to the **breakdown peak** at $s_{maxT}$.
4. From the peak, a falling curve to $T_{st}$ at $s = 1$.
5. Below the axis, for $s < 0$, a mirror-ish negative curve in the generating region.

#### Why the exact shape matters in practice

- The **narrowness of the stable region** (the falling side, from breakdown to $N_s$) is why an induction motor holds speed well.
- The **height of the peak** ($T_{\max}$) is the overload capability. It cannot be raised by rotor resistance (Q7(b)).
- The **position of the peak** ($R_2/X_2$) can be moved by rotor resistance, which is how slip-ring machines are given high starting torque.
- The **negative-slip region** is the induction generator (Q8(b)).

---

### Q8(b): Describe the process following which an IM can be operated as IG. **[CO2, Marks: 04]**

#### The single idea

An induction motor is a transformer with a rotating, short-circuited secondary. Its behaviour therefore depends only on the **sign of the slip**, not on any switch or commutator:

$$\text{slip} > 0 \Rightarrow \text{motoring}, \qquad \text{slip} < 0 \Rightarrow \text{generating}$$

$$\boxed{\text{An induction machine generates whenever it is driven above synchronous speed.}}$$

#### What happens, step by step

**Step 1: connect it to the supply and let it settle as a motor.** Apply rated 3-$\varphi$ voltage and frequency. The stator establishes the rotating field at $N_s = 120f/P$, and the rotor settles at a small positive slip.

**Step 2: bring in a prime mover and accelerate the rotor past $N_s$.** A diesel engine, water turbine, or the overhauling load on the same shaft is coupled and used to push the rotor speed **above** $N_s$.

**Step 3: the slip goes negative.** Now $N > N_s$, so $s = (N_s - N)/N_s < 0$. This is the only change required — no rewiring, no brushes, no external excitation.

**Step 4: the electrical roles reverse.**

| Quantity | Motor ($s>0$) | Generator ($s<0$) |
|:---|:---|:---|
| Rotor emf | $sE_2$ in one direction | $sE_2$ **reversed** |
| Rotor current | in one direction | **reversed** |
| Rotor reaction on the field | aiding | **opposing** |
| Stator current | drawn from the line | **fed into** the line |
| Mechanical power | out of the shaft | **into** the shaft |
| Torque | drives the rotor | **opposes** the prime mover |

So the field now drags against the rotor's motion instead of with it. The rotor's kinetic/mechanical input is converted, through the same air gap, into electrical power returned to the line.

![A squirrel-cage machine driven above synchronous speed by a prime mover while connected to a three-phase line, working as an induction generator, with its power-flow diagram](../Books/Theraja/Ch-34/diagrams/Ch-34_p33_fig28_29.jpg)

**Step 5: the machine feeds the line.** Because the stator is still connected to the supply, the generated power flows back into the same bus that was supplying it. On the torque-slip curve of Q8(a) the operating point has simply moved left of the origin, into the negative-slip region.

#### The power-flow picture

The losses are unchanged in nature but reversed in role. Of the mechanical power put in by the prime mover:

- A fraction $|s|$ is lost as **rotor copper loss**, $P_{cu2} = |s|P_{gap}$ (note the sign: now a loss);
- The rest, $(1-|s|)$, becomes **electrical power** delivered to the line, minus stator copper and iron losses.

So generation efficiency is roughly $1-|s|$, just like the rotor efficiency in motoring. Which is why an induction generator is most efficient at **small** over-speed. In Q8(c) the machine runs at 1530 rpm against $N_s = 1500$, so $|s| = 0.02$ and rotor efficiency is 98%.

#### Two modes of operation

**(a) Grid-connected / self-excited.** If the machine is connected to a live 3-$\varphi$ bus, the bus supplies the magnetising VARs, so no external excitation is needed. This is the common case and the one in Q8(c).

**(b) Stand-alone (isolated) operation.** If the machine must supply an **isolated** load by itself, it has a problem: it needs reactive power to build and sustain the air-gap flux, but with no grid to provide it. The solution is a **capacitor bank** across the terminals supplying the leading VARs.

![Self-excited induction generator circuit with terminal capacitors supplying the magnetising VARs](../Books/Theraja/Ch-34/diagrams/Ch-34_p34_fig31.jpg)

The build-up sequence is worth understanding:

1. Residual magnetism always exists in the core. Spin the machine above $N_s$.
2. That residual flux induces a small emf, which drives a small current through the capacitors.
3. The capacitor current is **leading**, so it acts like a magnetising current and reinforces the flux.
4. More flux means more emf, which means more capacitor current — a **positive feedback loop**.
5. The loop builds up to a stable voltage determined by the load and the total capacitive reactance.

The condition for self-excitation is that the capacitive vars supplied **exceed** the vars the machine needs at that voltage and load. Part (c) is exactly the calculation of that required capacitance.

#### Advantages and limitations

**Advantages:** extremely simple and rugged, no brushes, no commutator, no exciter, no rotating semiconductor; cheap to build and almost maintenance-free; well suited to small isolated loads.

**Limitations:**

| Problem | Consequence |
|:---|:---|
| Poor voltage regulation | Terminal voltage and frequency both depend on load and speed |
| Frequency is **not** controlled by the machine | It is set by the prime mover's speed, so it varies with prime-mover droop |
| Needs a **variable** capacitor for good regulation | Otherwise voltage collapses at heavy load and rises at light load |
| Cannot be over-excited to the grid | Must absorb vars from the grid, so it consumes reactive power when grid-connected |
| Efficiency lower than a synchronous generator | Because of the slip losses and poorer power factor |
| Output voltage must be raised to grid level | An induction generator is essentially a low-voltage machine |

Because frequency is set by the prime mover rather than by the generator, an induction generator is normally used in **small isolated** sets (farm and remote installations, small hydro and wind) where the load is modest and a frequency-stable grid is not available. It is also used as a **regenerative braking** arrangement: the same machine, driven above synchronous speed, pushes power back into the line.

---

### Q8(c): A 30 kW, 4-pole motor used as an induction generator **[CO2, Marks: 04]**

> A 440V, 4-pole, 1470 rpm, 30-kW, 3-$\varphi$ IM is to be used as IG, the rated current of the motor is 40A and full-load power factor is 85%. Now, calculate:
> (i) Capacitance required per phase if capacitors are connected in delta.
> (ii) Speed of the driving engine for generating a frequency of 50Hz.

#### Read the problem first

This is a **verbatim repeat of 2018 Q5(c)**, with identical data. It is worth pausing on what the nameplate gives us and what it is *for*:

| Nameplate item | Value | Role in the calculation |
|:---|:---|:---|
| $V_L$ | 440 V | Voltage the capacitors must work at (delta ⇒ phase voltage) |
| $P$ | 4 poles | Gives $N_s = 120f/P$ |
| $N$ | 1470 rpm | The motor's motoring full-load speed, hence its slip |
| $30$ kW, $40$ A, $0.85$ p.f. | — | The reactive power the machine must be given when generating |

#### Step 0: the two facts we need

$$\sin\phi = \sqrt{1 - \cos^2\phi} = \sqrt{1 - 0.85^2} = \sqrt{1 - 0.7225} = \sqrt{0.2775} = 0.5268$$

$$N_s = \frac{120 \times 50}{4} = 1500\text{ rpm}$$

#### (i) Capacitance per phase, delta connected

**Step 1: total reactive power to be supplied.**

An induction generator cannot build and sustain its air-gap flux from real power alone. It needs the leading VARs that a capacitor bank provides. The magnitude of that requirement is set by the machine's rated kVA and power factor, so compute the reactive component of its rated apparent power:

$$Q = \sqrt{3}\,V_L I_L \sin\phi = 1.732\times440\times40\times0.5268$$

$$1.732\times440 = 762.08, \qquad 762.08\times40 = 30483,\qquad 30483\times0.5268 = 16065\text{ VAR}$$

$$Q \approx 16.07\text{ kVAR}$$

**Step 2: VARs per phase.**

With a balanced **three-phase** bank, each phase supplies a third:

$$Q_\phi = \frac{Q}{3} = \frac{16065}{3} = 5355\text{ VAR per phase}$$

**Step 3: the connection matters — this is the step to get right.**

In **delta**, each capacitor sits directly across a **line pair**, so the voltage on each capacitor is the **full line voltage**:

$$V_\phi = V_L = 440\text{ V}$$

Had the bank been in **star**, each capacitor would see $V_L/\sqrt{3} = 254$ V, and the required capacitance would be **three times larger** for the same VARs. So the connection is not incidental; it is a factor of $\sqrt{3}$ in $V^2$, hence a factor of 3 in $C$.

**Step 4: capacitance from $Q = \omega C V^2$.**

A capacitor's reactive power per phase is $Q_\phi = 2\pi f C V_\phi^2$, so

$$C = \frac{Q_\phi}{2\pi f V_\phi^2} = \frac{5355}{2\pi\times50\times440^2}$$

$$2\pi\times50 = 314.16, \qquad 440^2 = 193600, \qquad 314.16\times193600 = 6.0822\times10^7$$

$$C = \frac{5355}{6.0822\times10^7} = 8.805\times10^{-5}\text{ F} \approx 88.1\ \mu\text{F} \quad (\text{or } 88.2\ \mu\text{F using } X_C = 36.11\ \Omega)$$

$$\boxed{C \approx 88.1\text{ to } 88.2\ \mu\text{F per phase, delta connected}}$$

#### (ii) Speed of the driving engine for 50 Hz generation

**Step 1: establish where the machine currently sits.**

At $N_s = 1500$ rpm the synchronous speed for 4 poles at 50 Hz is 1500 rpm. The motor's rated speed is 1470 rpm, so

$$\text{slip as a motor} = \frac{1500 - 1470}{1500} = \frac{30}{1500} = 0.02$$

So **at its rated motoring speed this machine is still BELOW synchronous speed.** It is still motoring, and its slip is still positive. It is not generating at all at 1470 rpm.

**Step 2: the sign must be flipped.**

To generate, the slip must be **negative**, which means driving the rotor **above** 1500 rpm. The magnitude of the over-speed slip should match the machine's rated slip magnitude, so that it operates at its rated voltage, current and torque when generating:

$$|s_{gen}| = 0.02 \quad\Rightarrow\quad s_{gen} = -0.02$$

**Step 3: engine speed.**

$$N_{engine} = N_s(1 - s_{gen}) = 1500(1-(-0.02)) = 1500\times1.02$$

$$\boxed{N_{engine} = 1530\text{ rpm}}$$

Equivalently: the over-speed is $1500\times0.02 = 30$ rpm, so $1500 + 30 = 1530$ rpm.

#### Checks on the answer

1. **Above synchronous speed.** $1530 > 1500$ ✓, so the slip is negative and the machine generates. An engine at 1470 rpm would simply keep it motoring.
2. **The frequency is exactly 50 Hz.** $f = \frac{PN}{120} = \frac{4\times1530}{120} = \frac{6120}{120} = 51$ Hz for the electrical frequency *of the field at that speed*. The important point is subtler: the engine must turn at 1530 rpm *when the grid is at 50 Hz*, because the machine's synchronous speed is then 1500 rpm and the 30 rpm over-speed is exactly the rated slip. The field is synchronous **with the grid**, which is what keeps the generated frequency locked to 50 Hz.
3. **The two answers are consistent with each other.** The 2% slip is the same 2% that sets how hard the machine is worked as a generator, and it is the same slip the capacitor bank in part (i) was sized to support.

#### What these two numbers mean in the installation

- **88.2 µF per phase in delta** is a real, practical capacitor bank — at 440 V and 50 Hz each unit must withstand 440 V rms and supply 5355 VAR, so oil-filled or polypropylene units of roughly 5.3 kVAR / 440 V are the natural choice. In a self-excited stand-alone set this bank is what makes the machine start up at all (see the positive-feedback build-up in Q8(b)).
- **1530 rpm** sets the prime-mover overspeed. The engine must hold speed to within a few rpm, because every 1% variation in engine speed is a 1% variation in the magnitude of the generated voltage's slip and hence in the terminal voltage. This is the practical reason induction generators are used only for small isolated loads.

---

[← 2023 Answer](2023_answer.md) | [🏠 Index](README.md) | *(end)*