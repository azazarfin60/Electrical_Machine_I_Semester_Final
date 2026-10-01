# Master Curriculum & Topic Map: ECE 2107 / ECE 2207 (Electrical Machines-I)

> **Purpose for AI & Researchers**: This master map indexes every topic, mathematical derivation, equivalent circuit model, experimental test, and textbook problem across Lectures **L-01 to L-11**. Consult this index to pinpoint the exact file, slide number, and line reference without loading all slide markdowns into the context window.

---

## 1. Executive Curriculum Directory

| Lecture Tag | Machine Domain | File Link | Primary Lecture Theme | Slides | Key Highlights |
| :--- | :--- | :--- | :--- | :---: | :--- |
| **L-01** | Foundations | [`L-01_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-01_ECE-2207.md) | Magnetic Fields & Machine Principles | 11 | Field generation, Biot-Savart, Transformer/Motor/Generator action, Fleming's rules |
| **L-02** | Induction Motor | [`L-02_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-02_ECE-2207.md) | Rotating Magnetic Field (RMF) | 14 | AC vs DC motors, 2-$\phi$ RMF ($F_m$), 3-$\phi$ RMF ($1.5 F_m$), flux revolving theory |
| **L-03** | Induction Motor | [`L-03_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-03_ECE-2107.md) | Slip, Vector Diagram & Equivalent Circuit | 20 | Synchronous speed $N_s$, slip $s$, rotor frequency $f_r$, transformer model, exact circuit |
| **L-04** | Induction Motor | [`L-04_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-04_ECE-2107.md) | Torque Equations & Characteristics | 17 | Starting torque, running torque, max torque condition ($s_{max} = R_2/X_2$), torque-speed curve |
| **L-05** | Induction Motor | [`L-05_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md) | Parameter Determination & Tests | 15 | No-load test, Blocked-rotor test, DC stator test, loss separation, worked 40-hp problem |
| **L-06** | Induction Motor | [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md) | Power Flow & Starting Methods | 20 | Power stages ($P_g : P_{cu} : P_{dev} = 1 : s : 1-s$), synchronous watt, DOL, Auto-transformer, Star-Delta, Rotor rheostat |
| **L-07** | Induction Motor | [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md) | Speed Control, Braking, 1-$\phi$ IM & Circle Diagram | 24 | Speed control methods, dynamic/DC/capacitor braking, plugging, induction generator, 1-$\phi$ split-phase/capacitor motors, circle diagram |
| **L-08** | Transformer | [`L-08_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-08_ECE-2107.md) | Fundamentals & Principle of Action | 14 | Transformer action, efficiency, DC transient behavior, AC sinusoidal derivation ($E = 4.44 f N \Phi_m$) |
| **L-09** | Transformer | [`L-09_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-09_ECE-2107.md) | Construction & Phasor Diagrams | 13 | Core vs Shell type, no-load phasor ($I_0, I_\mu, I_w$), loaded phasor (unity, lagging, leading pf) |
| **L-10** | Transformer | [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md) | Equivalent Circuit, Regulation & Tests | 19 | Leakage reactance, impedance referring ($K^2$), exact/approximate circuits, voltage regulation, OC test, SC test |
| **L-11** | Transformer | [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md) | 3-$\phi$ Transformers, Scott-T & Vector Groups | 29 | 3-$\phi$ connections (Y-Y, Y-$\Delta$, $\Delta$-Y, $\Delta$-$\Delta$), 3rd harmonic issues, Open-$\Delta$ (57.7%), Scott-T 3-$\phi$ to 2-$\phi$, Vector groups (Dyn11) |

---

## 2. Granular Slide-by-Slide Syllabus & Topic Mapping

### [L-01] Fundamentals of Electrical Machines & Magnetic Fields
* **Primary File**: [`L-01_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-01_ECE-2207.md)
* **Core Machine Family**: Electromechanical Foundations
* **Total Slides**: 11
* **Slide Breakdown**:
  * **Slide 01**: Course Title & Course Code (`ECE-2207`).
  * **Slide 02**: Quranic Inscription (*Surah Al-’Alaq 96:1*).
  * **Slide 03**: Prescribed Study Materials:
    * *Basic Knowledge*: B.L. Theraja (Vol-II), Stephen J. Chapman (*Electric Machinery Fundamentals*), A.E. Fitzgerald.
    * *Competitive / Govt Job Exams*: V.K. Mehta, J.B. Gupta.
  * **Slide 04**: Magnetic Field as the medium of electromechanical energy conversion.
  * **Slide 05**: Generation of Magnetic Field: Permanent magnets (magnetic dipole, magnetic lines of force).
  * **Slide 06**: Generation of Magnetic Field: Current-carrying straight conductor (Biot-Savart Law, Right-Hand Grip Rule).
  * **Slide 07**: Generation of Magnetic Field: Current-carrying coil / solenoid (Ampere's Circuital Law, polarity rule).
  * **Slide 08**: Fundamental Electromechanical Mechanisms: Overview of physical laws linking fields and mechanical systems.
  * **Slide 09**: **Basis of Transformer Action**: Faraday's Law of Electromagnetic Induction ($e = -N \frac{d\Phi}{dt}$); time-varying magnetic field inducing voltage in stationary coil.
  * **Slide 10**: **Basis of Motor Action**: Lorentz force on current-carrying conductor in a magnetic field ($F = B I l \sin \theta$); **Fleming's Left-Hand Rule** (Thumb: Force/Motion, Index: Field, Middle: Current).
  * **Slide 11**: **Basis of Generator Action**: Motional EMF induced in conductor moving through magnetic field ($e = B l v \sin \theta$); **Fleming's Right-Hand Rule** (Thumb: Motion, Index: Field, Middle: Induced Current).

---

### [L-02] Induction Motor Fundamentals & Rotating Magnetic Field (RMF)
* **Primary File**: [`L-02_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-02_ECE-2207.md)
* **Core Machine Family**: 3-Phase Induction Motors (Part 1)
* **Total Slides**: 14
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Induction Motor-SL1*).
  * **Slide 02**: Quranic Inscription (*Surah Ta-Ha 20:114*).
  * **Slide 03**: Terminology & Physical Construction: Stator (stationary outer frame) vs. Rotor (rotating inner cylinder); Field vs. Armature windings.
  * **Slide 04**: AC Motors Overview: Synchronous motors (runs at $N_s$) vs. Asynchronous / Induction motors (runs at $N < N_s$).
  * **Slide 05**: Induction Motor vs. DC Motor: Conduction via commutator/brushes (DC) vs. Inductive contactless energy transfer (AC).
  * **Slide 06**: Induction Motor Rotor Types: Squirrel-cage rotor vs. Wound/Slip-ring rotor (Ref: Video `V-01`).
  * **Slide 07**: Operational Pros & Cons:
    * *Advantages*: Simple and rugged construction, low cost, high reliability, self-starting, minimal maintenance.
    * *Disadvantages*: Essentially constant speed with speed drop on load, starting torque lower than DC motor, low lagging power factor at light loads.
  * **Slide 08**: **Flux Revolving Theory**: How multi-phase stator currents produce a revolving magnetic field of constant magnitude.
  * **Slide 09**: **Production of RMF by 2-$\phi$ Supply**: Two stator coils spaced $90^\circ$ electrically fed by currents in phase quadrature ($i_A = I_m \cos \omega t$, $i_B = I_m \sin \omega t$).
  * **Slide 10**: Mathematical Proof for 2-$\phi$ RMF across Angles:
    * $\theta = 0^\circ \implies \Phi_r = \Phi_m \angle 0^\circ$
    * $\theta = 45^\circ \implies \Phi_r = \Phi_m \angle 45^\circ$
    * $\theta = 90^\circ \implies \Phi_r = \Phi_m \angle 90^\circ$
    * $\theta = 135^\circ \implies \Phi_r = \Phi_m \angle 135^\circ$
  * **Slide 11**: Proof continued ($\theta = 180^\circ$); Conclusion: Constant resultant amplitude $F_R = F_m$ rotating at angular speed $\omega = 2\pi f$.
  * **Slide 12**: **Production of RMF by 3-$\phi$ Supply**: Three windings displaced $120^\circ$ in space carrying balanced currents displaced $120^\circ$ in time ($i_R, i_Y, i_B$).
  * **Slide 13**: Mathematical Proof for 3-$\phi$ RMF:
    * $\theta = 0^\circ \implies \Phi_R = \frac{3}{2} \Phi_m \angle 0^\circ$
    * $\theta = 60^\circ \implies \Phi_R = \frac{3}{2} \Phi_m \angle 60^\circ$
  * **Slide 14**: Proof continued for $\theta = 120^\circ, 180^\circ$; Core Conclusion: Resultant field has constant magnitude $\Phi_R = 1.5 \Phi_m = \frac{3}{2}\Phi_m$ and rotates synchronously at $N_s = 120f/P$.

---

### [L-03] Induction Motor Principles, Slip, Vector Diagram & Equivalent Circuit
* **Primary File**: [`L-03_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-03_ECE-2107.md)
* **Core Machine Family**: 3-Phase Induction Motors (Part 2)
* **Total Slides**: 20
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Induction Motor-SL2*).
  * **Slide 02**: Quranic Inscription (*Surah Ash-Sharh 94:5-6*).
  * **Slide 03**: **Synchronous Speed Equation**: $N_s = \frac{120 f}{P}$. Mechanical rotor speed $N_r \le N_s$.
  * **Slide 04**: **Why Does the Rotor Rotate?**: Relative velocity cuts rotor bars $\to$ Induced EMF $\to$ Rotor circulating current.
  * **Slide 05**: **Lenz's Law & Torque Production**: Mechanical force $F = B I l$ exerts torque in the direction of field rotation to reduce relative speed; why rotor can never reach $N_s$ (no relative speed $\implies$ no induced EMF $\implies$ zero torque).
  * **Slide 06**: Slip Definitions: Slip Speed $= N_s - N$.
  * **Slide 07**: Fractional & Percentage Slip: $s = \frac{N_s - N}{N_s}$, $N = N_s(1 - s)$.
  * **Slide 08**: **Frequency of Rotor Current**: $f_r = s \cdot f$. Standstill ($s=1 \implies f_r = f$); running ($s \approx 0.02-0.05 \implies f_r \approx 1-3\text{ Hz}$).
  * **Slide 09**: Textbook Practice Problems: B.L. Theraja Examples **34.3, 34.4, 34.5** (Poles, slip speed, rotor speed, rotor current frequency).
  * **Slide 10**: Induction Motor as a Generalized Transformer: Stator as primary, short-circuited rotating rotor as secondary.
  * **Slide 11**: Stator vs Rotor Quantities: Stator per-phase voltage $V_1 = -E_1 + I_1 Z_1$; Standstill rotor EMF $E_2$; Running rotor EMF $E_r = s E_2$; Running rotor reactance $X_r = s X_2$.
  * **Slide 12**: No-Load Stator Current $I_0$: Core-loss component $I_w$ and Magnetizing component $I_\mu$ ($I_0 = \sqrt{I_\mu^2 + I_w^2}$).
  * **Slide 13**: Induction Motor Equivalent Circuit: Ideal transformer model coupling stator and rotor.
  * **Slide 14**: Internal EMF & Flux Relationship: Core flux linked to internal voltage $E_1$.
  * **Slide 15**: Effective Turns Ratio $a_{\text{eff}}$ between stator and rotor windings.
  * **Slide 16**: **Rotor Circuit Model Transformation**: Rotor current $I_2 = \frac{s E_2}{\sqrt{R_2^2 + (s X_2)^2}} = \frac{E_2}{\sqrt{(R_2/s)^2 + X_2^2}}$.
  * **Slide 17**: Standstill Voltage Reference: $E_{R0}$ under locked-rotor conditions.
  * **Slide 18**: Variable Equivalent Resistance Decomposition:
    $$\frac{R_2}{s} = R_2 + R_2\left(\frac{1 - s}{s}\right)$$
    * $R_2$: Actual rotor winding ohmic copper loss.
    * $R_2\left(\frac{1 - s}{s}\right)$: Fictitious load resistance representing electromechanical power developed.
  * **Slide 19**: Transformation to Stator Reference: Referring rotor parameters using turns ratio ($R_2' = a_{\text{eff}}^2 R_2, X_2' = a_{\text{eff}}^2 X_2$).
  * **Slide 20**: **Complete Per-Phase Equivalent Circuit Diagram**: Features stator branch ($R_1, X_1$), shunt core branch ($R_c, X_M$), and referred rotor branch ($R_2'/s, X_2'$).

---

### [L-04] Induction Motor Torque Equations, Maximum Torque & Characteristics
* **Primary File**: [`L-04_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-04_ECE-2107.md)
* **Core Machine Family**: 3-Phase Induction Motors (Part 3)
* **Total Slides**: 17
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Induction Motor-SL3*).
  * **Slide 02**: Quranic Inscription (*Surah Al-Baqarah 2:286*).
  * **Slide 03**: Rotor Torque Principles: $T \propto \Phi I_2 \cos \varphi_2 \propto E_2 I_2 \cos \varphi_2$.
  * **Slide 04**: **Starting Torque Derivation**: Standstill condition ($s = 1$), rotor current $I_2 = \frac{E_2}{\sqrt{R_2^2 + X_2^2}}$, rotor power factor $\cos \varphi_2 = \frac{R_2}{\sqrt{R_2^2 + X_2^2}}$.
  * **Slide 05**: Starting Torque Formula:
    $$T_{st} = \frac{K_1 E_2^2 R_2}{R_2^2 + X_2^2} \quad \text{where } K_1 = \frac{3}{2\pi N_s}$$
  * **Slide 06**: **Condition for Maximum Starting Torque**:
    $$\frac{dT_{st}}{dR_2} = 0 \implies R_2 = X_2$$
    Starting torque is maximized when standstill rotor resistance per phase equals standstill rotor reactance per phase.
  * **Slide 07**: Textbook Practice Problems: B.L. Theraja Examples **34.6, 34.7, 34.8, 34.9, 34.11** (Calculating $T_{st}$, effect of extra rotor resistance, determining full-load torque).
  * **Slide 08**: Rotor Quantities Under Running Condition (at slip $s$): $E_{2r} = s E_2$, $X_{2r} = s X_2$, $Z_{2r} = \sqrt{R_2^2 + (s X_2)^2}$.
  * **Slide 09**: Running Torque Proportionality: $T_r \propto E_{2r} I_{2r} \cos \varphi_{2r}$.
  * **Slide 10**: **General Running Torque Equation**:
    $$T_r = \frac{K_1 s E_2^2 R_2}{R_2^2 + (s X_2)^2}$$
  * **Slide 11**: Torque Constant Evaluation: $K_1 = \frac{3}{2\pi N_s}$ (yielding torque in Newton-meters $\text{N}\cdot\text{m}$).
  * **Slide 12**: **Condition for Maximum Torque Under Running Conditions**: Differentiating $T_r$ with respect to slip $s$:
    $$\frac{dT_r}{ds} = 0 \implies s = s_{max} = s_b = \frac{R_2}{X_2}$$
  * **Slide 13**: Running Condition for Max Torque: Maximum torque occurs at the slip where rotor reactance equals rotor resistance ($s X_2 = R_2$).
  * **Slide 14**: **Breakdown / Pull-Out Torque Formula**:
    $$T_{max} = T_b = \frac{K_1 E_2^2}{2 X_2}$$
    *Crucial Conclusion*: Maximum torque is **independent of rotor resistance** $R_2$; however, the slip $s_b$ at which $T_{max}$ occurs is directly proportional to $R_2$.
  * **Slide 15**: **Torque-Slip Characteristics Analysis**:
    * *Low Slip Region* ($s \approx 0$): $s X_2 \ll R_2 \implies T \propto s$ (linear curve).
    * *High Slip Region* ($s$ near 1): $s X_2 \gg R_2 \implies T \propto \frac{1}{s}$ (hyperbolic curve).
  * **Slide 16**: Pull-Out Torque & Operating Stability: Stable motor operation occurs between $s = 0$ and $s = s_{max}$; operation beyond pull-out causes motor stalling.
  * **Slide 17**: **Torque-Speed Characteristics Curves**: Family of torque-speed curves for varying rotor resistance ($R, 4R, 6R$) demonstrating starting torque enhancement without altering peak pull-out torque.

---

### [L-05] Induction Motor Parameter Determination & Testing
* **Primary File**: [`L-05_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md)
* **Core Machine Family**: 3-Phase Induction Motors (Part 4)
* **Total Slides**: 15
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Induction Motor-SL4*).
  * **Slide 02**: Quranic Inscription.
  * **Slide 03**: Purpose of Parameter Determination: Finding $R_1, R_2, X_1, X_2, X_M$, and rotational/core losses.
  * **Slide 04**: **No-Load Test Concept**: Uncoupled motor running at rated voltage and rated frequency ($s \approx 0$).
  * **Slide 05**: No-Load Equivalent Circuit: Rotor branch acts as open circuit ($R_2/s \to \infty$); input impedance $Z_{NL} \approx R_1 + j(X_1 + X_M)$.
  * **Slide 06**: No-Load Test Equations:
    $$S_{NL} = \sqrt{3} V_{NL} I_{NL}, \quad Q_{NL} = \sqrt{S_{NL}^2 - P_{NL}^2}, \quad X_{NL} = \frac{Q_{NL}}{3 I_{NL,ph}^2} = X_1 + X_M$$
  * **Slide 07**: Separation of Losses from No-Load Test:
    $$P_{rot} = P_{core} + P_{f\&w} = P_{NL} - 3 I_{NL}^2 R_1$$
  * **Slide 08**: Separation of Core Loss from Friction & Windage: Plotting $P_{NL} - 3 I_1^2 R_1$ against $V^2$ and extrapolating to $V=0$ (intercept gives $P_{f\&w}$).
  * **Slide 09**: **Blocked-Rotor Test Concept**: Rotor clamped stationary ($N = 0, s = 1$); low voltage applied at reduced frequency (e.g., 15 Hz) to limit current to rated value.
  * **Slide 10**: Blocked-Rotor Equivalent Circuit: Magnetizing branch $X_M$ neglected ($X_M \gg X_2$); series impedance $Z_{BR} \approx R_{BR} + j X_{BR}'$.
  * **Slide 11**: Blocked-Rotor Equations & Reactance Splitting:
    $$Z_{BR} = \frac{V_{BR,ph}}{I_{BR,ph}}, \quad R_{BR} = \frac{P_{BR,ph}}{I_{BR,ph}^2} = R_1 + R_2, \quad X_{BR}' = \sqrt{Z_{BR}^2 - R_{BR}^2}$$
    Frequency correction: $X_{BR,60} = \frac{60}{f_{test}} X_{BR,test}$. Splitting per NEMA Design B: $X_1 = 0.4 X_{BR,60}$, $X_2 = 0.6 X_{BR,60}$.
  * **Slide 12**: **DC Test for Stator Resistance**: DC current injected into stator terminals to isolate pure ohmic resistance without inductive reactance.
  * **Slide 13**: DC Test Formulations:
    * *Wye (Y) Connected*: $R_1 = \frac{R_{DC}}{2}$
    * *Delta ($\Delta$) Connected*: $R_1 = \frac{3}{2} R_{DC}$
  * **Slide 14**: Skin Effect & Temperature AC Correction: $R_{1,AC} \approx 1.15-1.25 R_{1,DC}$.
  * **Slide 15**: **Comprehensive Worked-Out Numerical Problem**:
    * *Problem Statement*: 3-$\phi$, Y-connected, 40-hp, 60-Hz, 460-V, Design B motor ($I_{rated} = 57.8\text{ A}$, Blocked rotor at 15 Hz: $V_{line}=36.2\text{V}, I=58.0\text{A}, P=2573.4\text{W}$; No-load: $V_{line}=460\text{V}, I=32.7\text{A}, P=4664.4\text{W}$; DC test: $V_{DC}=12\text{V}, I_{DC}=59\text{A}$).
    * *Step-by-step Solution*:
      * $R_1 = \frac{12/59}{2} = 0.102\ \Omega/\text{phase}$
      * $R_2 = R_{BR} - R_1 = 0.2550 - 0.102 = 0.153\ \Omega/\text{phase}$
      * $X_1 = 0.4073\ \Omega, X_2 = 0.6109\ \Omega$
      * $X_M = X_{NL} - X_1 = 7.99 - 0.4073 = 7.58\ \Omega/\text{phase}$
      * Combined Core, Friction & Windage Loss $= 4337.3\text{ W}$
      * $I_{NL} \text{ as \% of rated} = \frac{32.7}{57.8} \times 100\% = 56.6\%$.

---

### [L-06] Power Stages, Torque & Starting Methods of Induction Motors
* **Primary File**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md)
* **Core Machine Family**: 3-Phase Induction Motors (Part 5)
* **Total Slides**: 20
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Induction Motor-SL5*).
  * **Slide 02**: Quranic Inscription.
  * **Slide 03**: Power Stages in an Induction Motor: Complete power flow chain overview.
  * **Slide 04**: **Power Flow Diagram**:
    * Stator Electrical Input: $P_{in} = \sqrt{3} V_L I_L \cos \theta$.
    * Stator Losses: Stator Copper Loss ($3 I_1^2 R_1$) + Stator Iron / Core Loss.
    * Air-gap Power (Rotor Input Power $P_g$ or $P_2$): $P_g = P_{in} - \text{Stator Losses}$.
  * **Slide 05**: **Fundamental Power Division**:
    * Rotor Copper Loss: $P_{cu,rotor} = 3 I_2^2 R_2 = s P_g$.
    * Gross Mechanical Power Developed ($P_{dev}$ or $P_{md}$): $P_{dev} = (1 - s) P_g$.
    * Golden Power Ratio:
      $$P_g : P_{cu,rotor} : P_{dev} = 1 : s : (1 - s)$$
  * **Slide 06**: Torque Developed by Motor: $T_d = \frac{P_g}{\omega_s} = \frac{P_{dev}}{\omega_m} = \frac{P_g}{2\pi N_s / 60}$.
  * **Slide 07**: Rotor Output Power (Shaft Power $P_{out}$): $P_{out} = P_{dev} - \text{Rotational Losses } (P_{f\&w} + P_{stray})$.
  * **Slide 08**: Machine Efficiency: $\eta = \frac{P_{out}}{P_{in}} \times 100\% = \frac{P_{out}}{P_{out} + \text{Total Losses}} \times 100\%$.
  * **Slide 09**: Summary of Energy Transformations across stator air gap and rotor shaft.
  * **Slide 10**: **Synchronous Watt Concept**:
    $$\text{Torque in Synchronous Watts} = \text{Rotor Input Power } P_g \text{ in Watts}$$
    Defined as the torque which, at synchronous speed, develops 1 Watt of mechanical power.
  * **Slide 11**: Starting Problem of Induction Motors: Severe starting current ($5-8 \times I_{FL}$) at low lagging power factor causes severe line voltage dips.
  * **Slide 12**: Direct Switching / Line Starting (DOL): $I_{st} \approx 7 I_{fl}$, but $T_{st}$ is only $\approx 1.96 T_{fl}$; limited to small motors ($< 5\text{ kW}$).
  * **Slide 13**: Classification of Starting Methods:
    * *Squirrel-cage*: Primary resistor/reactor, Auto-transformer, Star-Delta ($\text{Y}$-$\Delta$).
    * *Slip-ring*: Rotor rheostat starter.
  * **Slide 14**: Primary Resistor / Reactor Starting: Applied voltage reduced to $x V$; Starting current $I_{st} = x I_{sc}$; Starting torque $T_{st} = x^2 T_{sc}$.
  * **Slide 15**: **Auto-Transformer Starting**: Transformer tapping ratio $x$:
    * Voltage across motor $= x V_1$.
    * Motor starting current $= x I_{sc}$.
    * Line starting current drawn from supply $= x^2 I_{sc}$.
    * Starting torque $T_{st} = x^2 T_{sc}$.
  * **Slide 16**: Starting to Full-Load Torque Ratio for Auto-Transformer:
    $$\frac{T_{st}}{T_{fl}} = x^2 \left(\frac{I_{sc}}{I_{fl}}\right)^2 s_{fl}$$
  * **Slide 17**: Schematic Circuit Diagram of Auto-Transformer Starter (Start vs Run positions).
  * **Slide 18**: **Star-Delta ($\text{Y}$-$\Delta$) Starting**:
    * In Star (Start): $V_{ph} = \frac{V_L}{\sqrt{3}} \implies I_{st,\text{line}} = \frac{1}{3} I_{sc,\Delta}$.
    * Starting torque: $T_{st} = \frac{1}{3} T_{sc,\Delta}$.
    * Torque Ratio: $\frac{T_{st}}{T_{fl}} = \frac{1}{3} \left(\frac{I_{sc}}{I_{fl}}\right)^2 s_{fl}$.
  * **Slide 19**: **Slip-Ring Motor Starting via Rotor Rheostat**: External resistance $R_{ext}$ added to rotor via slip rings; reduces starting current while simultaneously increasing starting torque ($R_2 + R_{ext} \approx X_2$).
  * **Slide 20**: Rotor Rheostat Operation Sequence: Gradual cut-out of external resistance as motor reaches rated speed; textbook practice example B.L. Theraja **34.10**.

---

### [L-07] Speed Control, Electric Braking, Induction Generator, 1-$\phi$ Motors & Circle Diagram
* **Primary File**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md)
* **Core Machine Family**: 3-Phase & 1-Phase Induction Machines (Part 6)
* **Total Slides**: 24
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Induction Motor-SL6*).
  * **Slide 02**: Quranic Inscription (*Surah Al-Baqarah 2:269*).
  * **Slide 03**: **Speed Control Classifications**:
    * *Stator Side*: (1) Stator voltage control, (2) Supply frequency control ($V/f$ control), (3) Changing stator poles, (4) Adding external stator impedance.
    * *Rotor Side*: (1) Adding external rotor resistance (slip-ring only), (2) Cascade control, (3) Injecting slip-frequency EMF (Scherbius/Kramer drives).
  * **Slide 04**: Textbook Reference: B.L. Theraja Article **35.18**.
  * **Slide 05**: Practice Problems on Speed Control: B.L. Theraja Examples **35.29, 35.30**.
  * **Slide 06**: **Dynamic Electric Braking**: Converting stored mechanical kinetic energy into heat by running the motor as a loaded generator.
  * **Slide 07**: **DC Injection Braking**: Stator disconnected from AC line and energized with DC current; creates stationary magnetic field inducing eddy currents and copper losses in spinning rotor.
  * **Slide 08**: **Capacitor Braking**: Motor disconnected from line and connected to 3-$\phi$ capacitor bank; operates as self-excited generator dissipating energy in windings and discharge resistors.
  * **Slide 09**: **Plugging (Reverse Voltage Braking)**: Interchanging any two stator leads; reverses direction of RMF, producing massive counter-torque ($s \approx 2$ at initiation of braking); high rotor $I^2R$ dissipation.
  * **Slide 10**: **Induction Generator Operation**: Motor driven by prime mover above synchronous speed ($N > N_s \implies s < 0$); mechanical input converted to electrical active power delivered to AC system while absorbing reactive VARs from grid for excitation.
  * **Slide 11**: Grid-Connected Induction Generator schematic (driven by engine/turbine).
  * **Slide 12**: Self-Excited Induction Generator (SEIG): Standalone generator using shunt capacitors to provide excitation reactive power.
  * **Slide 13**: **Complete Torque-Speed Operating Curve of 3-Phase Induction Machine**:
    * *Motoring Region*: $0 < N < N_s$ ($0 < s < 1$).
    * *Generating Region*: $N > N_s$ ($s < 0$).
    * *Braking / Plugging Region*: Reverse rotation $N < 0$ ($s > 1$).
  * **Slide 14**: Textbook Practice Problem: B.L. Theraja Example **34.26**.
  * **Slide 15**: **Single-Phase Induction Motor (1-$\phi$ IM)**: Pulsating single-phase stator field alternates along one space axis; inherently **non-self-starting** ($T_{st} = 0$).
  * **Slide 16**: **Double Revolving Field Theory**: Alternating flux $\Phi = \Phi_m \cos \omega t$ resolved into two oppositely rotating fluxes of magnitude $\frac{\Phi_m}{2}$. Standstill slip $s_f = 1, s_b = 2 - 1 = 1 \implies T_f = T_b \implies T_{resultant} = 0$.
  * **Slide 17**: Making 1-$\phi$ IM Self-Starting: Conversion into temporary 2-phase machine during start via auxiliary/starting winding spaced $90^\circ$ electrically.
  * **Slide 18**: **Split-Phase Induction Motor**: Main winding has low $R$, high $X$; Auxiliary winding has high $R$, low $X$; Phase angle split $\alpha \approx 30^\circ$; Centrifugal switch disconnects auxiliary winding at $70-80\%$ speed.
  * **Slide 19**: **Capacitor-Start Induction-Run Motor**: Capacitor in series with auxiliary winding produces $\approx 80^\circ$ phase split between $I_m$ and $I_s$; develops very high starting torque ($3-4 \times T_{fl}$); Centrifugal switch cuts out capacitor.
  * **Slide 20**: Phasor diagram and torque comparison of Split-phase vs Capacitor-start motors.
  * **Slide 21**: **Capacitor-Start Capacitor-Run & Permanent Split Capacitor (PSC) Motors**: Uses two capacitors (large starting electrolytic capacitor + small continuous running paper/oil capacitor) for optimal start and high running efficiency/power factor.
  * **Slide 22**: **Circle Diagram Fundamentals**: Graphical locus of AC circuits; series $R$-$L$ circuit locus is a semicircle as reactance or resistance varies.
  * **Slide 23**: Construction of Induction Motor Circle Diagram: Using No-Load test ($V_{NL}, I_0, \cos \varphi_0$) and Blocked-Rotor test ($V_{BR}, I_{BR}, \cos \varphi_{BR}$) to construct the circle diameter, torque line, and output line.
  * **Slide 24**: Parameter Extraction from Circle Diagram: Finding max output power, max torque, slip, efficiency, and power factor graphically; Practice problems: B.L. Theraja Examples **35.3, 35.5, 35.6, 35.8, 35.9**.

---

### [L-08] Transformer Fundamentals, Energy Transfer & Principles of Action
* **Primary File**: [`L-08_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-08_ECE-2107.md)
* **Core Machine Family**: Transformers (Part 1)
* **Total Slides**: 14
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Transformer-SL1*).
  * **Slide 02**: Quranic Inscription (*Surah Ibrahim*).
  * **Slide 03**: Prescribed Study Materials: Rosenblatt (Ch 14), B.L. Theraja (Ch 32).
  * **Slide 04**: **Transformer Definition & Nature**: Static electromagnetic machine; transfers AC power between circuits at constant frequency via mutual magnetic induction.
  * **Slide 05**: Industrial Uses of Transformers: Voltage stepping for bulk transmission, distribution stepping for consumer utilization, galvanic DC isolation, impedance matching, instrument measurement (CT/PT).
  * **Slide 06**: Power Transformers: High-voltage transmission and substation step-up/step-down ratings.
  * **Slide 07**: Physical Construction & Visuals: Silicon steel core, laminated limbs, high/low voltage bushings, oil conservator tank, cooling radiators.
  * **Slide 08**: **Transformer Efficiency**: Why efficiency is exceptionally high ($95-99\%$): absence of moving parts eliminates friction, windage, and mechanical wear losses.
  * **Slide 09**: **Principle of Transformer Action with Transient DC Input**:
    * Switch closing: DC current rises $\to \frac{d\Phi}{dt} > 0 \to$ Induced secondary EMF opposing flux build-up (Lenz's law).
    * Steady DC state: $\frac{d\Phi}{dt} = 0 \to$ Induced EMF drops to zero (transformers do not operate on steady DC).
  * **Slide 10**: Direction Finding: Right-hand grip rule for flux direction, Lenz's law for secondary induced polarity, dot convention.
  * **Slide 11**: Transient DC Input - Switch Opening: Magnetic flux collapses rapidly ($\frac{d\Phi}{dt} < 0$) inducing reverse EMF pulse.
  * **Slide 12**: Core Insight of DC Transient Operation: Inductive energy transfer requires changing flux linkage.
  * **Slide 13**: **Principle of Transformer Action with Sinusoidal AC Input**: Sinusoidal supply voltage produces alternating flux $\Phi = \Phi_m \sin \omega t$.
  * **Slide 14**: **Derivation of Fundamental EMF Equation**:
    $$e_1 = -N_1 \frac{d\Phi}{dt} = -N_1 \frac{d}{dt}(\Phi_m \sin \omega t) = -N_1 \omega \Phi_m \cos \omega t = 2\pi f N_1 \Phi_m \sin(\omega t - 90^\circ)$$
    $$\text{RMS Primary EMF: } E_1 = \frac{2\pi}{\sqrt{2}} f N_1 \Phi_m = 4.44 f N_1 \Phi_m$$
    $$\text{RMS Secondary EMF: } E_2 = 4.44 f N_2 \Phi_m$$
    Transformation Ratio $K = \frac{E_2}{E_1} = \frac{N_2}{N_1}$.

---

### [L-09] Transformer Construction & Phasor Diagrams
* **Primary File**: [`L-09_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-09_ECE-2107.md)
* **Core Machine Family**: Transformers (Part 2)
* **Total Slides**: 13
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Transformer-SL2*).
  * **Slide 02**: Quranic Inscription (*Surah An-Nahl*).
  * **Slide 03**: **Transformer Construction Types**:
    * *Core Type*: Windings encircle the two vertical magnetic limbs; simple insulation, suited for high-voltage applications.
    * *Shell Type*: Magnetic core surrounds and encloses the windings; three limbs (central limb has twice the cross-sectional area of outer limbs); high mechanical bracing, suited for low-voltage, high-current applications.
    * Laminated silicon steel sheets ($0.35-0.5\text{ mm}$) insulated by varnish to minimize eddy current loss.
  * **Slide 04**: Transformer Phasor Diagram Overview: Modeling ideal vs real transformer under varying loads.
  * **Slide 05**: **Phasor Diagram Under No-Load Condition**: Secondary open ($I_2 = 0$); primary draws small no-load current $I_0$ ($3-5\%$ of full-load current).
  * **Slide 06**: Components of No-Load Current $I_0$:
    * *Magnetizing Component* ($I_\mu$ or $I_m$): $I_\mu = I_0 \sin \varphi_0$ (in phase with mutual flux $\Phi_m$, wattless/reactive, sets up core flux).
    * *Working / Core-Loss Component* ($I_w$ or $I_c$): $I_w = I_0 \cos \varphi_0$ (in phase with applied voltage $V_1$, active/wattful, supplies hysteresis and eddy current losses).
    * Magnitude: $I_0 = \sqrt{I_\mu^2 + I_w^2}$.
  * **Slide 07**: No-Load Phasor Diagram Construction: Mutual flux $\vec{\Phi}$ on horizontal reference; induced EMFs $E_1$ and $E_2$ lag $\Phi$ by $90^\circ$; applied voltage $\vec{V_1} = -\vec{E_1}$ leads $\Phi$ by $90^\circ$; $\vec{I_0}$ lags $\vec{V_1}$ by no-load angle $\varphi_0$.
  * **Slide 08**: No-Load Power Factor & Iron Loss: No-load power factor $\cos \varphi_0 \approx 0.1-0.2$ lagging; No-load power $W_0 = V_1 I_0 \cos \varphi_0 = \text{Iron Loss } P_i$.
  * **Slide 09**: Textbook Practice Problems: Rosenblatt Example **14.4**, B.L. Theraja Example **32.9** (Calculating $I_0, I_\mu, I_w, \cos \varphi_0$).
  * **Slide 10**: **Phasor Diagram Under Loaded Condition**:
    * Secondary supplies load current $I_2$ at power factor $\cos \varphi_2$.
    * Secondary MMF $N_2 I_2$ demagnetizes the core.
    * Primary draws reflected load current $I_2'$ to neutralize secondary MMF ($N_1 I_2' = N_2 I_2 \implies I_2' = K I_2$).
    * Total Primary Current: $\vec{I_1} = \vec{I_0} + \vec{I_2'}$.
  * **Slide 11**: Phasor Diagram for Non-Inductive Load (Unity Power Factor, $\cos \varphi_2 = 1$): Secondary current $I_2$ in phase with $V_2$.
  * **Slide 12**: Phasor Diagram for Reactive Loads:
    * *Inductive Load* (Lagging pf): $I_2$ lags $V_2$ by angle $\varphi_2$.
    * *Capacitive Load* (Leading pf): $I_2$ leads $V_2$ by angle $\varphi_2$.
  * **Slide 13**: Textbook Practice Problems: B.L. Theraja Examples **32.12, 32.13, 32.14** (Determining primary current $I_1$ and primary power factor $\cos \varphi_1$).

---

### [L-10] Transformer Leakage Reactance, Equivalent Circuit, Voltage Regulation & Testing
* **Primary File**: [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md)
* **Core Machine Family**: Transformers (Part 3)
* **Total Slides**: 19
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Transformer-SL3*).
  * **Slide 02**: Quranic Inscription (*Surah Al-Hadid 57:25*).
  * **Slide 03**: **Leakage Reactance Concept**: Primary leakage flux $\Phi_{L1}$ and secondary leakage flux $\Phi_{L2}$ completing paths through air rather than linking both windings.
  * **Slide 04**: Effect of Leakage Flux: Induces self-reactance EMFs that cause internal inductive voltage drops.
  * **Slide 05**: Fictitious Reactance Representation: $X_1 = 2\pi f L_1$, $X_2 = 2\pi f L_2$.
  * **Slide 06**: Total Winding Impedances: Primary $\vec{Z_1} = R_1 + j X_1$; Secondary $\vec{Z_2} = R_2 + j X_2$.
  * **Slide 07**: Transformer Terminal Voltage Equations:
    $$\vec{V_1} = -\vec{E_1} + \vec{I_1} R_1 + j \vec{I_1} X_1, \quad \vec{E_2} = \vec{V_2} + \vec{I_2} R_2 + j \vec{I_2} X_2$$
  * **Slide 08**: Transformation Ratio $K$: $K = \frac{E_2}{E_1} = \frac{N_2}{N_1} \approx \frac{V_2}{V_1} = \frac{I_1}{I_2}$.
  * **Slide 09**: **Equivalent Resistance Referring**:
    * Secondary referred to Primary: $R_2' = \frac{R_2}{K^2} \implies R_{01} = R_1 + \frac{R_2}{K^2}$.
    * Primary referred to Secondary: $R_1' = K^2 R_1 \implies R_{02} = R_2 + K^2 R_1$.
  * **Slide 10**: **Equivalent Reactance Referring**:
    * Secondary referred to Primary: $X_2' = \frac{X_2}{K^2} \implies X_{01} = X_1 + \frac{X_2}{K^2}$.
    * Primary referred to Secondary: $X_1' = K^2 X_1 \implies X_{02} = X_2 + K^2 X_1$.
    * Equivalent Impedances: $Z_{01} = \sqrt{R_{01}^2 + X_{01}^2}$, $Z_{02} = \sqrt{R_{02}^2 + X_{02}^2}$.
  * **Slide 11**: Transformed Voltage & Current References: $E_2' = E_2/K = E_1$, $V_2' = V_2/K$, $I_2' = K I_2$.
  * **Slide 12**: **Complete Exact Equivalent Circuit Diagram**: Complete circuit schematic showing $R_1, X_1, R_0, X_0, R_2', X_2'$ and ideal transformer block.
  * **Slide 13**: **Approximate Equivalent Circuits**: Shunt magnetizing branch ($R_0, X_0$) shifted to input terminals; combines series parameters into $R_{01}$ and $X_{01}$.
  * **Slide 14**: Complete Phasor Diagram with Winding Resistances and Leakage Reactances (Lagging Power Factor Load).
  * **Slide 15**: Complete Phasor Diagram for Leading & Unity Power Factor Loads.
  * **Slide 16**: **Voltage Regulation (VR)**:
    $$VR = \frac{V_{S,nl} - V_{S,fl}}{V_{S,fl}} \times 100\%$$
    $$\text{Approximate Expression: } VR \approx \frac{I_2(R_{02} \cos \varphi_2 \pm X_{02} \sin \varphi_2)}{V_{2,fl}} \times 100\%$$
    *(+ for lagging power factor, - for leading power factor)*.
  * **Slide 17**: **Open-Circuit (No-Load) Test**:
    * Performed on Low-Voltage (LV) side with High-Voltage (HV) open.
    * Rated voltage applied; instruments measure $V_1, I_0, W_0$.
    * Wattmeter measures Core/Iron Loss $P_i = W_0$.
    * Parameter extractions:
      $$\cos \varphi_0 = \frac{W_0}{V_1 I_0}, \quad I_w = I_0 \cos \varphi_0, \quad I_\mu = I_0 \sin \varphi_0, \quad R_0 = \frac{V_1}{I_w}, \quad X_0 = \frac{V_1}{I_\mu}$$
  * **Slide 18**: **Short-Circuit (Impedance) Test**:
    * Performed on High-Voltage (HV) side with Low-Voltage (LV) dead short-circuited.
    * Reduced voltage ($5-10\%$ of rated) applied to circulate full-load rated current $I_{sc}$.
    * Wattmeter measures Full-Load Copper Loss $W_{sc} = P_{cu}$.
    * Parameter extractions:
      $$R_{01} = \frac{W_{sc}}{I_{sc}^2}, \quad Z_{01} = \frac{V_{sc}}{I_{sc}}, \quad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$
  * **Slide 19**: Textbook Practice Problems: Rosenblatt Examples **14.7, 14.8, 14.9, 14.10**, B.L. Theraja Examples **32.27, 32.35, 32.36, 32.40** (Equivalent circuit parameters, OC/SC tests, voltage regulation, efficiency).

---

### [L-11] 3-Phase Transformers, Connections, Two-Transformer Schemes, Scott-T & Vector Groups
* **Primary File**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md)
* **Core Machine Family**: 3-Phase Transformers (Part 4)
* **Total Slides**: 29
* **Slide Breakdown**:
  * **Slide 01**: Title slide (*Transformer-SL4*).
  * **Slide 02**: Quranic Inscription (*Surah Al-Mulk 67:30*).
  * **Slide 03**: Necessity of 3-Phase Transformers: Generation, transmission, and heavy industrial distribution.
  * **Slide 04**: Construction Options: Bank of three separate single-phase transformers vs Single 3-phase unit (3-legged / 5-legged core).
  * **Slide 05**: Comparison: 3-$\phi$ single unit is lighter, smaller, cheaper, and $\approx 15\%$ more efficient; Bank offers replacement of single faulted phase.
  * **Slide 06**: Standard 3-Phase Connections: Four standard topologies ($\text{Y}$-$\text{Y}$, $\text{Y}$-$\Delta$, $\Delta$-$\text{Y}$, $\Delta$-$\Delta$).
  * **Slide 07**: **Wye-Wye ($\text{Y}$-$\text{Y}$) Connection**:
    $$V_{\varphi P} = \frac{V_{LP}}{\sqrt{3}}, \quad V_{LS} = \sqrt{3} V_{\varphi S}, \quad \text{Line Voltage Ratio } \frac{V_{LP}}{V_{LS}} = a$$
  * **Slide 08**: **Severe Problems with $\text{Y}$-$\text{Y}$ Connection**:
    1. *Unbalanced Load Problem*: In ungrounded Y-Y, unbalanced loads shift the neutral voltage (floating neutral), causing severe line-to-neutral overvoltages.
    2. *Third-Harmonic Voltage Distortion*: Magnetizing current contains prominent 3rd harmonics; in ungrounded wye, 3rd harmonic currents cannot flow, distorting phase voltage into peaked waves with $3rd$ harmonic voltages up to $50\%$ of fundamental.
  * **Slide 09**: Solutions to $\text{Y}$-$\text{Y}$ Defects: Solidly ground neutrals, or include a closed tertiary delta ($\Delta$) winding to circulate 3rd harmonic currents.
  * **Slide 10**: Summary of $\text{Y}$-$\text{Y}$ connection.
  * **Slide 11**: **Wye-Delta ($\text{Y}$-$\Delta$) Connection**:
    $$V_{LP} = \sqrt{3} V_{\varphi P}, \quad V_{LS} = V_{\varphi S}, \quad \text{Line Voltage Ratio } \frac{V_{LP}}{V_{LS}} = \sqrt{3} a$$
    Commonly used for step-down transmission substations.
  * **Slide 12**: $\text{Y}$-$\Delta$ Characteristics: Third-harmonic currents freely circulate in closed delta (no voltage distortion); introduces a **$30^\circ$ phase shift** between primary and secondary line voltages.
  * **Slide 13**: **Delta-Wye ($\Delta$-$\text{Y}$) Connection**:
    $$V_{LP} = V_{\varphi P}, \quad V_{LS} = \sqrt{3} V_{\varphi S}, \quad \text{Line Voltage Ratio } \frac{V_{LP}}{V_{LS}} = \frac{a}{\sqrt{3}}$$
    Commonly used for generator step-up stations (low voltage to transmission EHV); provides neutral on secondary for 4-wire commercial distribution; introduces a **$30^\circ$ phase shift**.
  * **Slide 14**: **Delta-Delta ($\Delta$-$\Delta$) Connection**:
    $$V_{LP} = V_{\varphi P}, \quad V_{LS} = V_{\varphi S}, \quad \text{Line Voltage Ratio } \frac{V_{LP}}{V_{LS}} = a$$
    No phase shift; handles unbalanced loads cleanly; third harmonics circulate in delta; permits Open-$\Delta$ operation if one unit fails.
  * **Slide 15**: 3-Phase Transformation Using Only Two Transformers: Emergency and economic schemes.
  * **Slide 16**: **Open-$\Delta$ (or V-V) Connection**: Formed when one transformer of a $\Delta$-$\Delta$ bank is removed for maintenance. Balanced 3-phase voltages maintained:
    $$V_C = -V_A - V_B = -V\angle 0^\circ - V\angle -120^\circ = V\angle 120^\circ$$
  * **Slide 17**: Power Handling Capability of Open-$\Delta$:
    $$\text{Closed-}\Delta\text{ Rating} = 3 V_{ph} I_{ph} = \sqrt{3} V_L (\sqrt{3} I_S) = 3 V_L I_S$$
    $$\text{Open-}\Delta\text{ Rating} = \sqrt{3} V_L I_S$$
  * **Slide 18**: **Open-$\Delta$ Capacity Ratios Derivation**:
    $$\frac{\text{Open-}\Delta\text{ kVA}}{\text{Closed-}\Delta\text{ kVA}} = \frac{\sqrt{3} V_L I_S}{3 V_L I_S} = \frac{1}{\sqrt{3}} \approx 0.577 \implies 57.7\%$$
    $$\text{Utilization of 2 Installed Units} = \frac{\sqrt{3} V_L I_S}{2 V_L I_S} = \frac{\sqrt{3}}{2} \approx 0.866 \implies 86.6\%$$
  * **Slide 19**: Practice Problems on Open-$\Delta$: Rosenblatt Examples **14.4, 14.5**.
  * **Slide 20**: **Open-Wye Open-Delta Connection**: Derived from two phases and neutral of 4-wire wye system for rural 3-phase loads; disadvantage: large neutral return current.
  * **Slide 21**: **Scott-T Connection**: Converts 3-phase power to 2-phase power (at $90^\circ$) or vice versa.
  * **Slide 22**: Scott-T Hardware Topology:
    * *Main Transformer* ($T_1$): Connected between lines B and C; center-tapped at $50\%$ point $D$.
    * *Teaser Transformer* ($T_2$): Connected between line A and center tap $D$; tapped at $86.6\%$ ($\frac{\sqrt{3}}{2}$) of full primary winding.
  * **Slide 23**: Scott-T Mathematical & Phasor Proof:
    $$V_{ad} = V_{ab} + V_{bd} = V_L \angle -120^\circ + 0.5 V_L \angle 0^\circ = \frac{\sqrt{3}}{2} V_L \angle -90^\circ$$
    Proves teaser voltage is strictly in quadrature ($90^\circ$) with main transformer voltage.
  * **Slide 24**: **Three-Phase T-Connection**: Two transformers connected in T configuration on both primary and secondary to convert 3-$\phi$ to 3-$\phi$ power.
  * **Slide 25**: **Vector Groups of Transformers**: Defines the phase angle displacement between primary (HV) and secondary (LV) voltage vectors introduced by winding configurations.
  * **Slide 26**: **Clock Representation System**:
    * HV reference phasor set at **12 o'clock** ($0^\circ$).
    * Anti-clockwise phasor rotation: each clock hour corresponds to $30^\circ$ phase displacement.
    * $1\text{ o'clock} = -30^\circ$ (LV lags HV by $30^\circ$).
    * $6\text{ o'clock} = 180^\circ$ phase inversion.
    * $11\text{ o'clock} = +30^\circ$ (LV leads HV by $30^\circ$).
  * **Slide 27**: **Vector Group Nomenclature**:
    * *Capital Letter*: HV winding connection ($\text{Y}$ = Star, $\text{D}$ = Delta).
    * *Small Letter*: LV winding connection ($\text{y}$ = star, $\text{d}$ = delta, $\text{z}$ = zigzag).
    * *Letter 'n' or 'N'*: Neutral brought out.
    * *Four Standard Groups*: Group 1 ($0^\circ$: Yy0, Dd0, Dz0), Group 2 ($180^\circ$: Yy6, Dd6, Dz6), Group 3 ($-30^\circ$: Yd1, Dy1, Yz1), Group 4 ($+30^\circ$: Yd11, Dy11, Yz11).
  * **Slide 28**: Dyn1 Vector Group Detailed Connection & Clock Diagram.
  * **Slide 29**: **Dyn11 Vector Group Detailed Example**: Delta HV, Wye LV with neutral brought out; secondary line voltage leads primary line voltage by $30^\circ$ (11 o'clock).

---

## 3. Essential Equations & Mathematical Cheat-Sheet

### 3.1 Foundations & Magnetic Circuits (L-01)
* **Faraday's Law of Induction**: $e = -N \frac{d\Phi}{dt}$
* **Lorentz Force on Conductor**: $F = B I l \sin \theta$
* **Motional Induced EMF**: $e = B l v \sin \theta$

### 3.2 Induction Motor Kinematics & Rotor Quantities (L-02, L-03)
* **Resultant RMF (2-Phase)**: $F_R = F_m$
* **Resultant RMF (3-Phase)**: $F_R = 1.5 F_m = \frac{3}{2} F_m$
* **Synchronous Speed**: $N_s = \frac{120 f}{P}$
* **Slip**: $s = \frac{N_s - N}{N_s}$
* **Rotor Frequency**: $f_r = s \cdot f$
* **Rotor Running Voltage**: $E_{2r} = s E_2$
* **Rotor Running Reactance**: $X_{2r} = s X_2$
* **Rotor Current**: $I_{2r} = \frac{s E_2}{\sqrt{R_2^2 + (s X_2)^2}} = \frac{E_2}{\sqrt{(R_2/s)^2 + X_2^2}}$

### 3.3 Induction Motor Torque & Power Flow (L-04, L-06)
* **Starting Torque**: $T_{st} = \frac{3}{2\pi N_s} \frac{E_2^2 R_2}{R_2^2 + X_2^2}$
* **Max Starting Torque Condition**: $R_2 = X_2$
* **Running Torque**: $T_r = \frac{3}{2\pi N_s} \frac{s E_2^2 R_2}{R_2^2 + (s X_2)^2}$
* **Max Running Torque Slip**: $s_{max} = s_b = \frac{R_2}{X_2}$
* **Breakdown / Pull-Out Torque**: $T_{max} = \frac{3}{2\pi N_s} \frac{E_2^2}{2 X_2}$ *(independent of $R_2$)*
* **Power Ratio**: $P_g : P_{cu,rotor} : P_{dev} = 1 : s : (1 - s)$
* **Developed Torque**: $T_d = \frac{P_g}{\omega_s} = \frac{P_{dev}}{\omega_m}$

### 3.4 Induction Motor Starting & Starters (L-06)
* **Auto-Transformer Starter**: $I_{st} = x^2 I_{sc}, \quad \frac{T_{st}}{T_{fl}} = x^2 \left(\frac{I_{sc}}{I_{fl}}\right)^2 s_{fl}$
* **Star-Delta Starter**: $I_{st} = \frac{1}{3} I_{sc,\Delta}, \quad \frac{T_{st}}{T_{fl}} = \frac{1}{3} \left(\frac{I_{sc}}{I_{fl}}\right)^2 s_{fl}$

### 3.5 Single-Phase Induction Motors (L-07)
* **Double Revolving Slips**: $s_f = s, \quad s_b = 2 - s$
* **Standstill Condition**: $s_f = 1, s_b = 1 \implies T_f = T_b \implies T_{st} = 0$

### 3.6 Transformers: EMF, Impedance & Regulation (L-08, L-10)
* **EMF Equation**: $E = 4.44 f N \Phi_m$
* **Transformation Ratio**: $K = \frac{E_2}{E_1} = \frac{N_2}{N_1} \approx \frac{V_2}{V_1} = \frac{I_1}{I_2}$
* **Referred Resistance to Primary**: $R_{01} = R_1 + \frac{R_2}{K^2}$
* **Referred Reactance to Primary**: $X_{01} = X_1 + \frac{X_2}{K^2}$
* **Referred Resistance to Secondary**: $R_{02} = R_2 + K^2 R_1$
* **Referred Reactance to Secondary**: $X_{02} = X_2 + K^2 X_1$
* **Voltage Regulation**: $VR \approx \frac{I_2 (R_{02} \cos \varphi_2 \pm X_{02} \sin \varphi_2)}{V_{2,fl}} \times 100\%$

### 3.7 3-Phase Transformers & Scott-T (L-11)
* **Open-$\Delta$ vs Closed-$\Delta$ Capacity**: $\frac{S_{V-V}}{S_\Delta} = \frac{1}{\sqrt{3}} \approx 0.577\ (57.7\%)$
* **Open-$\Delta$ Utilization Factor**: $\frac{\sqrt{3} V_L I_S}{2 V_L I_S} = \frac{\sqrt{3}}{2} \approx 0.866\ (86.6\%)$
* **Scott-T Teaser Winding Tap**: $86.6\% = \frac{\sqrt{3}}{2} \approx 0.866$
* **Scott-T Main Winding Tap**: $50\%$ center tap
* **Vector Group Clock Angle**: Each hour $= 30^\circ$ phase lag (anti-clockwise phasor rotation)

---

## 4. Experimental Tests & Laboratory Procedures

| Machine | Test Name | Purpose / Parameters Determined | Slides |
| :--- | :--- | :--- | :--- |
| **Induction Motor** | **No-Load Test** | Determines magnetizing reactance $X_M$, core loss resistance $R_c$, and separates friction & windage losses $P_{f\&w}$. | [L-05: S04–S08](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md#L45-L105) |
| **Induction Motor** | **Blocked-Rotor Test** | Determines total equivalent resistance $R_{BR} = R_1 + R_2$ and equivalent leakage reactance $X_{BR}' = X_1 + X_2$. | [L-05: S09–S11](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md#L107-L148) |
| **Induction Motor** | **DC Stator Resistance Test** | Measures ohmic stator resistance $R_1$ for Wye ($R_{DC}/2$) and Delta ($1.5 R_{DC}$) connections. | [L-05: S12–S14](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md#L150-L178) |
| **Induction Motor** | **Circle Diagram Test** | Uses No-load and Blocked-rotor test points to plot circle diagram for graphical determination of slip, torque, power, and losses. | [L-07: S22–S24](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L205-L232) |
| **Transformer** | **Open-Circuit (OC) Test** | Conducted on LV side with HV open. Determines core/iron loss $P_i$, magnetizing reactance $X_0$, and core-loss resistance $R_0$. | [L-10: S17](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L201-L215) |
| **Transformer** | **Short-Circuit (SC) Test** | Conducted on HV side with LV shorted. Determines full-load copper loss $P_{cu}$, equivalent resistance $R_{01}$, and leakage reactance $X_{01}$. | [L-10: S18](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L217-L232) |

---

## 5. Textbook Numerical Problems Index

| Lecture | Prescribed Textbook | Example / Problem Reference | Core Problem Topic |
| :--- | :--- | :--- | :--- |
| **L-03** | B.L. Theraja (Vol-II) | Example **34.3, 34.4, 34.5** | Synchronous speed, slip speed, percentage slip, rotor frequency |
| **L-04** | B.L. Theraja (Vol-II) | Example **34.6, 34.7, 34.8, 34.9, 34.11** | Starting torque, max starting torque condition, full-load torque |
| **L-05** | Stephen J. Chapman / Sen | **Worked-Out 40-hp Problem** (Slide 15) | Complete equivalent circuit parameter calculation from No-load, Blocked rotor, and DC tests |
| **L-06** | B.L. Theraja (Vol-II) | Example **34.10** | Power stages, air-gap power, rotor copper loss, mechanical power, starter ratios |
| **L-07** | B.L. Theraja (Vol-II) | Example **35.29, 35.30** | Induction motor speed control via rotor resistance |
| **L-07** | B.L. Theraja (Vol-II) | Example **34.26** | Induction generator operation |
| **L-07** | B.L. Theraja (Vol-II) | Example **35.3, 35.5, 35.6, 35.8, 35.9** | Circle diagram construction, graphical performance evaluation |
| **L-09** | Rosenblatt / Theraja | Rosenblatt Ex **14.4**; Theraja Ex **32.9** | Transformer no-load parameters ($I_0, I_\mu, I_w, \cos \varphi_0$) |
| **L-09** | B.L. Theraja (Vol-II) | Example **32.12, 32.13, 32.14** | Loaded transformer primary current, power factor under reactive loads |
| **L-10** | Rosenblatt / Theraja | Rosenblatt Ex **14.7–14.10**; Theraja Ex **32.27, 32.35, 32.36, 32.40** | Transformer equivalent circuits, OC/SC tests, voltage regulation, efficiency |
| **L-11** | Rosenblatt | Example **14.4, 14.5** | Three-phase transformer connections and Open-$\Delta$ (V-V) capacity |

---

## 6. Master Alphabetical Cross-Reference Index (A–Z)

* **Air-gap Power ($P_g$)**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md#L40-L65) (Slides 4–5)
* **Auto-Transformer Starter**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md#L160-L195) (Slides 15–17)
* **Blocked-Rotor Test**: [`L-05_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md#L107-L148) (Slides 9–11, 15)
* **Braking (Dynamic, DC Injection, Capacitor, Plugging)**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L50-L88) (Slides 6–9)
* **Capacitor-Start / Capacitor-Run Motors**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L170-L203) (Slides 19–21)
* **Circle Diagram**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L205-L232) (Slides 22–24)
* **Clock Representation of Vector Groups**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L265-L310) (Slides 26–29)
* **Core Type vs Shell Type Transformer**: [`L-09_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-09_ECE-2107.md#L30-L45) (Slide 3)
* **DC Injection Braking**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L60-L70) (Slide 7)
* **DC Test for Stator Resistance**: [`L-05_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md#L150-L178) (Slides 12–14, 15)
* **Delta-Delta ($\Delta$-$\Delta$) Connection**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L150-L165) (Slide 14)
* **Delta-Wye ($\Delta$-Y) Connection**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L135-L148) (Slide 13)
* **Direct-On-Line (DOL) Starting**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md#L125-L140) (Slide 12)
* **Double Revolving Field Theory**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L140-L160) (Slide 16)
* **Dyn11 Vector Group**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L295-L315) (Slide 29)
* **Efficiency of Transformer**: [`L-08_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-08_ECE-2107.md#L75-L88) (Slide 8)
* **EMF Equation of Transformer**: [`L-08_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-08_ECE-2107.md#L135-L160) (Slide 14)
* **Equivalent Circuit (Induction Motor)**: [`L-03_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-03_ECE-2107.md#L135-L210) (Slides 13–20)
* **Equivalent Circuit (Transformer)**: [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L100-L160) (Slides 9–13)
* **Faraday's Law of Induction**: [`L-01_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-01_ECE-2207.md#L80-L95) (Slide 9), [`L-08_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-08_ECE-2107.md)
* **Fleming's Left-Hand & Right-Hand Rules**: [`L-01_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-01_ECE-2207.md#L97-L125) (Slides 10–11)
* **Floating Neutral / Third Harmonics in Y-Y**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L80-L105) (Slides 8–9)
* **Flux Revolving Theory**: [`L-02_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-02_ECE-2207.md#L80-L95) (Slide 8)
* **Induction Generator (Grid & Self-Excited)**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L90-L125) (Slides 10–12)
* **Leakage Reactance & Leakage Flux**: [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L30-L85) (Slides 3–7)
* **Maximum Starting Torque Condition ($R_2 = X_2$)**: [`L-04_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-04_ECE-2107.md#L70-L95) (Slide 6)
* **Maximum Running Torque Condition ($s = R_2/X_2$)**: [`L-04_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-04_ECE-2107.md#L140-L175) (Slides 12–14)
* **No-Load Phasor Diagram (Transformer)**: [`L-09_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-09_ECE-2107.md#L50-L95) (Slides 5–8)
* **No-Load Test (Induction Motor)**: [`L-05_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-05_ECE-2107.md#L45-L105) (Slides 4–8)
* **Open-Circuit (OC) Test (Transformer)**: [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L201-L215) (Slide 17)
* **Open-$\Delta$ (or V-V) Connection (57.7%)**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L170-L210) (Slides 16–19)
* **Open-Wye Open-Delta Connection**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L215-L225) (Slide 20)
* **Phasor Diagram with Winding Leakage**: [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L165-L185) (Slides 14–15)
* **Plugging of Induction Motor**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L80-L90) (Slide 9)
* **Power Flow & Division ($P_g : P_{cu} : P_{dev}$)**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md#L40-L75) (Slides 4–5)
* **Pull-Out / Breakdown Torque**: [`L-04_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-04_ECE-2107.md#L160-L190) (Slides 14–16)
* **Rotor Rheostat Starter**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md#L215-L235) (Slides 19–20)
* **Rotating Magnetic Field (2-Phase & 3-Phase)**: [`L-02_ECE-2207.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-02_ECE-2207.md#L90-L155) (Slides 9–14)
* **Scott-T Connection (3-$\phi$ to 2-$\phi$)**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L230-L260) (Slides 21–23)
* **Short-Circuit (SC) Test (Transformer)**: [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L217-L232) (Slide 18)
* **Single-Phase Induction Motor**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L135-L203) (Slides 15–21)
* **Slip & Slip Speed**: [`L-03_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-03_ECE-2107.md#L60-L85) (Slides 6–7)
* **Speed Control Methods (Induction Motor)**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L30-L48) (Slides 3–5)
* **Split-Phase Machine**: [`L-07_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-07_ECE-2107.md#L165-L185) (Slide 18)
* **Star-Delta Starter**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md#L198-L214) (Slide 18)
* **Synchronous Speed ($N_s = 120f/P$)**: [`L-03_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-03_ECE-2107.md#L30-L45) (Slide 3)
* **Synchronous Watt**: [`L-06_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-06_ECE-2107.md#L105-L120) (Slide 10)
* **Three-Phase T-Connection**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L260-L268) (Slide 24)
* **Torque-Slip & Torque-Speed Curves**: [`L-04_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-04_ECE-2107.md#L170-L205) (Slides 15–17)
* **Transient DC Input on Transformer**: [`L-08_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-08_ECE-2107.md#L90-L130) (Slides 9–12)
* **Vector Groups (Clock Method)**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L265-L315) (Slides 25–29)
* **Voltage Regulation of Transformer**: [`L-10_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-10_ECE-2107.md#L185-L200) (Slide 16)
* **Wye-Delta (Y-$\Delta$) Connection**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L110-L132) (Slides 11–12)
* **Wye-Wye (Y-Y) Connection**: [`L-11_ECE-2107.md`](file:///home/azaz/AntigravityxStudy/SemesterFinal_2_2/ECE_2207/SlidesByMaam/L-11_ECE-2107.md#L70-L108) (Slides 7–10)
