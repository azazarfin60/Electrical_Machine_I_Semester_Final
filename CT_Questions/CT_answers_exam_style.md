# ECE 2207: Electrical Machines I
## CT Questions: All Answers: Exam Style
**Department:** ECE, RUET | **Session:** 2023-24

> **How to use this file:** Concise, exam-ready answers. Every key step is present without extra commentary. Focus on structure and critical equations.

---

## CT-01 (19/07/2026): Induction Motors

### Q1. Prove that 3-φ stator flux rotates at synchronous speed. [10 Marks]

**Setup:** Three windings 120° apart in space. Balanced 3-phase supply gives:

$$\Phi_R = \Phi_m \sin(\omega t), \quad \Phi_Y = \Phi_m \sin(\omega t - 120°), \quad \Phi_B = \Phi_m \sin(\omega t + 120°)$$

**At four key instants:**

| ωt | Φ_R | Φ_Y | Φ_B | Resultant |
|:---:|:---:|:---:|:---:|:---:|
| 0° | 0 | −(√3/2)Φ_m | +(√3/2)Φ_m | 1.5Φ_m ↑ |
| 60° | +(√3/2)Φ_m | −(√3/2)Φ_m | 0 | 1.5Φ_m (60° rotated) |
| 120° | +(√3/2)Φ_m | 0 | −(√3/2)Φ_m | 1.5Φ_m (120° rotated) |
| 180° | 0 | +(√3/2)Φ_m | −(√3/2)Φ_m | 1.5Φ_m (180° rotated) |

**General proof (component method):**

Resolve along X and Y axes:

$$\Phi_x = \frac{3}{2}\Phi_m \sin(\omega t), \qquad \Phi_y = -\frac{3}{2}\Phi_m \cos(\omega t)$$

Magnitude:
$$\Phi_r = \sqrt{\Phi_x^2 + \Phi_y^2} = \frac{3}{2}\Phi_m = 1.5\,\Phi_m \quad \textbf{(constant)}$$

Space angle: $\theta = \omega t - 90°$, so $\frac{d\theta}{dt} = \omega = 2\pi f$

$$\boxed{N_s = \frac{120f}{P} \text{ rpm}}$$

**Conclusion:** Resultant flux = $1.5\Phi_m$ (constant magnitude), rotates at synchronous speed $N_s$. *(Proved)*

---

### Q2. Explain the basic operating principle of an induction motor. [10 Marks]

1. **RMF is produced.** 3-phase supply creates a rotating magnetic field of constant magnitude $1.5\Phi_m$ at speed $N_s = \frac{120f}{P}$.

2. **Field cuts rotor bars.** At start $N = 0$, relative speed $= N_s$. The rotating field sweeps across stationary rotor conductors.

3. **EMF is induced.** By Faraday's Law, $e = Blv_{\text{rel}}$ is induced in each rotor bar.

4. **Rotor current flows.** End rings (squirrel cage) or external resistors (wound rotor) close the circuit. Induced EMF drives rotor current.

5. **Torque is developed.** By Lorentz force law, $F = BIl$ acts on current-carrying bars inside the stator field.

6. **Rotor spins (Lenz's Law).** Rotor turns in the same direction as the RMF to reduce relative motion.

7. **Cannot reach $N_s$.** If $N = N_s$: relative speed = 0 → EMF = 0 → current = 0 → torque = 0. Friction slows the rotor. Always $N < N_s$.

$$s = \frac{N_s - N}{N_s}, \qquad f_r = sf$$

---

## CT-02 (03/08/2026): Induction Motors

### Q1. Justify: Maximum torque is independent of R₂. [10 Marks]

![Torque-Speed characteristics](../Books/diagrams/Chapman_Ch07_p202_torque_speed_r2_comp.jpg)

**Torque equation:**
$$T = \frac{k \cdot s E_2^2 R_2}{R_2^2 + s^2 X_2^2}, \qquad k = \frac{3}{2\pi N_s}$$

**Slip at max torque:** Differentiate w.r.t. $s$, set to zero:

$$\frac{dT}{ds} = 0 \implies R_2^2 - s^2 X_2^2 = 0 \implies \boxed{s_{mT} = \frac{R_2}{X_2}}$$

Peak slip depends on $R_2$. Increasing $R_2$ shifts the torque peak to higher slip.

**Value of $T_{\max}$:** Substitute $s = R_2/X_2$:

$$T_{\max} = \frac{k \cdot \frac{R_2}{X_2} \cdot E_2^2 \cdot R_2}{R_2^2 + \frac{R_2^2}{X_2^2} \cdot X_2^2} = \frac{k \cdot \frac{R_2^2}{X_2} \cdot E_2^2}{2R_2^2} = \boxed{\frac{kE_2^2}{2X_2}}$$

$R_2$ cancels completely. $T_{\max}$ depends only on $E_2$ (supply voltage) and $X_2$ (standstill reactance).

**Conclusion:**
- Changing $R_2$ shifts peak position ($s_{mT} = R_2/X_2$) but not peak value.
- At $R_2 = X_2$: $s_{mT} = 1$, so maximum torque coincides with starting torque. *(Justified)*

---

### Q2. Explain the blocked rotor test of an induction motor. [10 Marks]

![3-Phase Induction Motor Blocked-Rotor Test Circuit Connection (Two-Wattmeter Method)](diagrams/im_blocked_rotor_test_circuit.png)

![Per-Phase Equivalent Circuit During Blocked-Rotor Test (Simplified Series Circuit)](diagrams/im_blocked_rotor_equivalent_circuit.png)

**Setup:** Rotor is locked ($N = 0$, $s = 1$). Analogous to the short-circuit test of a transformer.

**Circuit:**
```
3-φ Supply → Variac → [V, A, W1+W2] → Stator terminals
                                        [Rotor: LOCKED]
```

**Procedure:**
1. Lock the rotor mechanically.
2. Short-circuit slip rings (wound rotor).
3. Start with zero voltage. Raise via variac until rated stator current flows.
4. Record: $V_{br}$, $I_{br}$, $P_{br} = W_1 + W_2$.

**Why low voltage?** Core loss ∝ $V^2$. At 10–15% rated voltage, iron loss ≈ 0. So $P_{br}$ = copper losses only.

**Parameters (star-connected):**
$$Z_{01} = \frac{V_{br}/\sqrt{3}}{I_{br}}, \qquad R_{01} = \frac{P_{br}}{3I_{br}^2}, \qquad X_{01} = \sqrt{Z_{01}^2 - R_{01}^2}$$
$$R_2' = R_{01} - R_1, \qquad X_1 \approx X_2' = \frac{X_{01}}{2}$$

**Necessities:**
1. Gives full-load copper loss → efficiency calculation.
2. Gives $R_{01}$, $X_{01}$ → series branch of equivalent circuit.
3. Starting current at rated voltage: $I_{sc} = I_{br} \times (V_{\text{rated}}/V_{br})$.
4. Estimates starting torque: $T_{st} \propto I_{sc}^2 R_2$.
5. Needed for circle diagram construction (gives $\cos\phi_{sc}$ and $I_{sc}$).

---

## CT-03 (26/08/2026): Transformers

### Q1. Schematic of a 1-φ transformer with variables labeled. [10 Marks]

![Schematic representation of a 1-phase transformer connected to a sinusoidal source on primary and load on secondary with all labeled variables](../Books/diagrams/VK_Mehta_Fig_7_01.jpeg)

**Primary variables:**
| Symbol | Meaning |
|:---:|:---|
| $v_1(t)$, $V_1$ | Applied terminal voltage (instantaneous / RMS) |
| $i_1(t)$, $I_1$ | Primary current from AC source |
| $N_1$ | Number of primary turns |
| $e_1(t)$, $E_1$ | Self-induced counter-EMF (lags $\Phi$ by 90°) |

**Secondary variables:**
| Symbol | Meaning |
|:---:|:---|
| $N_2$ | Number of secondary turns |
| $e_2(t)$, $E_2$ | Mutually induced EMF |
| $v_2(t)$, $V_2$ | Secondary terminal voltage |
| $i_2(t)$, $I_2$ | Load current |
| $Z_L = R_L + jX_L$ | Load impedance |

**Core variables:**
| Symbol | Meaning |
|:---:|:---|
| $\Phi(t)$ | Instantaneous mutual flux (Wb) |
| $\Phi_m$ | Peak mutual flux (Wb) |
| $A$ | Core cross-sectional area (m²) |
| $K = N_2/N_1$ | Voltage transformation ratio |

---

### Q2. Prove $E_1 = 4.44 f N_1 \Phi_m$ and $E_2 = 4.44 f N_2 \Phi_m$. [10 Marks]

**Given:** $\Phi(t) = \Phi_m \sin(\omega t)$. Same flux links both windings (no leakage).

**Derivation for $E_1$:**

By Faraday's Law:
$$e_1(t) = -N_1\frac{d\Phi}{dt} = -N_1 \omega \Phi_m \cos(\omega t) = N_1 \omega \Phi_m \sin(\omega t - 90°)$$

Peak value:
$$E_{m1} = N_1 \omega \Phi_m = 2\pi f N_1 \Phi_m$$

RMS value:
$$E_1 = \frac{E_{m1}}{\sqrt{2}} = \frac{2\pi f N_1 \Phi_m}{\sqrt{2}} = \sqrt{2}\pi f N_1 \Phi_m$$

Since $\sqrt{2}\pi = 4.44$:

$$\boxed{E_1 = 4.44\, f N_1 \Phi_m}$$

**For $E_2$:** Same flux, same derivation with $N_2$:

$$\boxed{E_2 = 4.44\, f N_2 \Phi_m} \qquad \textit{(Proved)}$$

**Alternative (average EMF method):** In quarter-cycle $T/4 = 1/(4f)$, flux changes by $\Phi_m$:
$$\text{Average EMF/turn} = 4f\Phi_m$$
$$E_{\text{rms}} = K_f \times 4f\Phi_m = 1.11 \times 4f\Phi_m = 4.44 f\Phi_m$$
Multiply by turns: $E_1 = 4.44fN_1\Phi_m$, $E_2 = 4.44fN_2\Phi_m$ *(Same result)*

---

## CT-04 (09/09/2026): Transformers

### Q1. Effect of leakage flux on transformer operation (with schematic). [10 Marks]

**Three types of flux:**
- $\Phi_m$: mutual flux, links both windings through core, transfers power.
- $\Phi_{l1}$: primary leakage flux, links only $N_1$ turns, path through air.
- $\Phi_{l2}$: secondary leakage flux, links only $N_2$ turns, path through air.

**Schematic:**
![Schematic of transformer showing mutual flux and primary/secondary leakage fluxes](../SlidesByMaam/diagrams/L-10_ECE-2107_p04_fig01.jpg)

**Effects:**

1. **Leakage reactances:** Each leakage flux induces a self-EMF lagging by 90°. This behaves like a series reactance:
   $$X_1 = 2\pi f L_{l1}, \qquad X_2 = 2\pi f L_{l2}$$

2. **Voltage drop inside windings:**
   $$V_1 = -E_1 + I_1 R_1 + jI_1 X_1$$
   $$V_2 = E_2 - I_2 R_2 - jI_2 X_2$$

3. **Worse voltage regulation:** Under lagging pf loads, $jI_2X_2$ reduces $V_2$.

4. **Fault current limiting (beneficial):** During a short circuit, $X_1 + X_2$ limits the fault current and protects the transformer.

---

### Q2. Phasor diagram of an R-L loaded ideal transformer: step by step. [10 Marks]

![Core and windings of an ideal transformer](../Books/diagrams/Ch-32_p07_fig13.jpg)

**Ideal transformer assumptions:** $R_1 = R_2 = X_1 = X_2 = 0$, $I_0 = 0$, so $V_2 = E_2$ and $V_1 = -E_1$.

**Step 1: Reference phasor:**
Draw $\vec{\Phi}_m$ along the +X axis (horizontal reference).

**Step 2: Induced EMFs:**
By Faraday's Law, induced EMF lags flux by 90°. Draw $\vec{E}_1$ and $\vec{E}_2$ vertically downward (−Y axis).

**Step 3: Secondary terminal voltage:**
No internal drops in ideal transformer. $\vec{V}_2 = \vec{E}_2$ (downward).

**Step 4: Secondary load current:**
R-L load, so $\vec{I}_2$ lags $\vec{V}_2$ by $\theta_2 = \tan^{-1}(X_L/R_L)$. Draw $\vec{I}_2$ clockwise from $\vec{V}_2$.

**Step 5: Primary current:**
Ampere-turn balance: $N_1 I_1 = N_2 I_2$. Primary current is opposite to $I_2$:
$$\vec{I}_1 = -\frac{N_2}{N_1}\vec{I}_2 \qquad \text{(180° reversed)}$$

**Step 6: Primary voltage:**
No drops. $\vec{V}_1 = -\vec{E}_1$ (vertically upward, +Y axis).

**Step 7: Power factor angle:**
Angle between $\vec{V}_1$ and $\vec{I}_1$ equals $\theta_1 = \theta_2$. Same pf on both sides.

**Phasor summary:**
![Transformer on-load phasor diagram](../Books/diagrams/Ch-32_p26_fig35.jpg)

| Phasor | Angle |
|:---:|:---:|
| $\vec{\Phi}_m$ | 0° |
| $\vec{E}_1 = \vec{E}_2 = \vec{V}_2$ | −90° |
| $\vec{V}_1$ | +90° |
| $\vec{I}_2$ | $−90° − \theta_2$ |
| $\vec{I}_1$ | $90° − \theta_1$ (= $90° − \theta_2$) |

---

*Source questions:* [CT_01.md](CT_01.md) · [CT_02.md](CT_02.md) · [CT_03.md](CT_03.md) · [CT_04.md](CT_04.md)
