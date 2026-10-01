[← T-22: DFRT & 1-Phase IM](T-22_DFRT_and_1Phase_IM.md) | [🏠 Index](00_Index.md) | [T-24: Miscellaneous IM Topics →](T-24_Miscellaneous_IM.md)

---

# T-23: Single-Phase IM Starting Methods
> **Section:** B | **Priority:** 🔴 MUST | **Exam Frequency:** 6/7 years
> **Sources:** VK Mehta Ch-9 (Art. 9.5-9.14), Theraja Ch-35, Slides L-08, L-09

## Why This Topic Matters

1-phase IM starting methods appeared in 6 out of 7 papers. Types include: capacitor-start (2017, 2020, 2023, 2024), capacitor-start-capacitor-run (2021, 2024), shaded pole (2023, 2024), split-phase (2017, 2018), and capacitor calculation numericals (2018, 2019, 2021). These questions range from 3-6 marks. This is the second most guaranteed topic after DFRT.

---

## 📝 Key Definitions

> **Capacitor-Start Motor:** "An auxiliary winding with a capacitor in series is placed 90° apart from the main winding. The capacitor advances the phase of auxiliary current. With proper capacitor value, the phase difference between main and auxiliary current approaches 90°, creating a rotating field for starting." — VK Mehta, Art. 9.8

> **Shaded-Pole Motor:** "A short-circuited copper band (shading band) is placed around a portion of each stator pole face. The flux in the shaded portion lags behind the flux in the unshaded portion, creating a sweeping effect from unshaded to shaded side." — VK Mehta, Art. 9.12

---

## Classification of 1-Phase IM Starting Methods

| Motor Type | Principle | Starting Torque | Running pf | Applications |
|:---|:---|:---|:---|:---|
| **Split-Phase** | High-$R_a$ auxiliary winding | 150-200% FL | Moderate | Fans, pumps, small tools |
| **Capacitor-Start** | Capacitor in series with auxiliary | 200-400% FL | Moderate | Compressors, conveyors |
| **Permanent-Split Cap** | Capacitor always in circuit | 50-100% FL | Good | Fans, blowers (quiet) |
| **Cap-Start, Cap-Run** | $C_{st}$ (start) + $C_{run}$ (run) | 200-350% FL | Good | Compressors, pumps |
| **Shaded-Pole** | Copper band on pole face | 40-60% FL | Poor | Small fans, timers |

---

## Capacitor-Start Motor

![Capacitor-start motor circuit and phasor diagram](diagrams/capacitor_start_circuit_phasor.jpeg)

**Construction:**
- Main winding (M) and auxiliary winding (A) placed 90° apart in space
- Capacitor in series with auxiliary winding
- Centrifugal switch disconnects auxiliary winding at ~75% of $N_s$

**Operation:**
1. The capacitor makes the auxiliary current $I_a$ LEAD the voltage
2. The main current $I_m$ LAGS the voltage
3. Total phase difference between $I_a$ and $I_m$ approaches 90°
4. 90° time displacement + 90° space displacement = rotating field
5. Starting torque is high (200-400% FL)
6. At ~75% speed, switch opens. Motor runs on main winding only.

---

## Capacitor-Start, Capacitor-Run Motor

![Two-value capacitor motor circuit](diagrams/cap_start_cap_run_circuit.jpeg)

**Two capacitors:**
- $C_{st}$ (large, starting): in circuit only during starting. Switched out by centrifugal switch.
- $C_{run}$ (small, running): permanently in circuit.

**Starting:** $C_{st} \| C_{run}$ gives large capacitance. Nearly 90° phase split. High starting torque.

**Running:** Only $C_{run}$ in circuit. Optimized for running efficiency and power factor. Smoother, quieter than capacitor-start-only motor.

---

## Shaded-Pole Motor

![Shaded-pole motor construction](diagrams/shaded_pole_motor.jpeg)

**Construction:** Salient stator poles. Short-circuited copper band (shading ring) around part of each pole.

**Operation:**
1. Alternating flux through the pole induces current in the shading ring (Lenz's law)
2. Ring current opposes flux change in shaded portion
3. Flux in shaded portion LAGS behind flux in unshaded portion
4. This time lag creates a sweeping effect: unshaded $\to$ shaded
5. Small starting torque in one direction

**Characteristics:** Very simple, no switches, no capacitors. Low starting torque (40-60% FL). Low efficiency. Fixed direction. Small sizes only (fans, display motors, hair dryers).

---

## Split-Phase (Resistance) Motor

![Split-phase motor circuit and phasor diagram](diagrams/split_phase_circuit_phasor.jpeg)

**Construction:** Auxiliary winding has higher resistance and lower reactance than main winding. Placed 90° apart in space.

**Operation:** Higher $R_a/X_a$ ratio makes $I_a$ lag less than $I_m$. Phase difference = 30°-40° (not 90°). Moderate starting torque.

---

## Capacitor Calculation for Maximum Starting Torque

For maximum starting torque, $I_m$ and $I_a$ must be 90° apart in time.

**Method:**
1. Find main winding angle: $\phi_m = \tan^{-1}(X_m/R_m)$
2. For 90° total: $I_a$ must lead $V$ by $(90° - \phi_m)$
3. Auxiliary circuit must be capacitive: net angle = $-(90° - \phi_m)$ leading
4. $X_C = X_a + R_a\tan(90° - \phi_m)$
5. $C = 1/(2\pi f X_C)$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Describe any two methods of making a 1-phase IM self-starting.
> **Appeared:** 2023 Q8(b), 2024 Q8(b) — (6 marks)

**Full Answer:**

**Method 1: Capacitor-Start Motor**

Auxiliary winding placed 90° from main winding. Capacitor in series with auxiliary. Capacitor makes $I_a$ lead $V$. Phase difference between $I_a$ and $I_m$ approaches 90°. 90° time split + 90° space split = RMF. Starting torque = 200-400% of FL. Centrifugal switch disconnects auxiliary at ~75% speed.

**Method 2: Shaded-Pole Motor**

Short-circuited copper band on part of each pole face. Alternating flux induces current in shading ring (Lenz's law). Flux in shaded portion lags behind unshaded. Creates sweeping effect from unshaded to shaded side. Small starting torque. Very simple, no switches. Low efficiency. For small motors only.

---

### 🎯 Q2: 230V, 50 Hz capacitor-start motor. Main: 100V, 2A, 40W. Auxiliary: 80V, 1A, 50W. Find capacitance for max starting torque.
> **Appeared:** 2018 Q8(c) — (4 marks)

**Full Answer:**

**Main winding:** $Z_m = 100/2 = 50\,\Omega$, $R_m = 40/4 = 10\,\Omega$, $X_m = \sqrt{50^2 - 10^2} = 49\,\Omega$

$\phi_m = \cos^{-1}(10/50) = 78.46°$ lagging

**Auxiliary winding:** $Z_a = 80/1 = 80\,\Omega$, $R_a = 50/1 = 50\,\Omega$, $X_a = \sqrt{80^2 - 50^2} = 62.45\,\Omega$

**For $I_a$ to lead $V$ by $(90° - 78.46°) = 11.54°$:**

$\tan(11.54°) = (X_C - X_a)/R_a$

$X_C = X_a + R_a\tan(11.54°) = 62.45 + 50 \times 0.204 = 72.65\,\Omega$

$$C = \frac{1}{2\pi \times 50 \times 72.65} = \boxed{43.8\,\mu\text{F}}$$

---

### 🎯 Q3: 250W, 230V, 50 Hz motor. $Z_m = (4.5 + j3.7)\,\Omega$, $Z_a = (9.5 + j3.5)\,\Omega$. Find starting capacitor for quadrature currents.
> **Appeared:** 2021 Q7(c) — (4 marks)

**Full Answer:**

$\phi_m = \tan^{-1}(3.7/4.5) = 39.43°$ lagging

For $I_a$ 90° ahead of $I_m$: $I_a$ must lead $V$ by $(90° - 39.43°) = 50.57°$

$\tan(50.57°) = (X_C - X_a)/R_a = (X_C - 3.5)/9.5$

$X_C - 3.5 = 9.5 \times 1.213 = 11.52$

$X_C = 15.02\,\Omega$

$$C = \frac{1}{2\pi \times 50 \times 15.02} = \boxed{211.8\,\mu\text{F}}$$

---

### 🎯 Q4: How does a capacitor-start-and-run motor operate?
> **Appeared:** 2021 Q7(b) — (4 marks)

**Full Answer:**

Two capacitors: $C_{st}$ (large) for starting, $C_{run}$ (small) for running.

**Starting:** $C_{st}$ and $C_{run}$ in parallel. Large capacitance gives nearly 90° phase split. High starting torque (200-350% FL).

**Running:** Centrifugal switch disconnects $C_{st}$ at ~75% speed. Motor runs with $C_{run}$ only. Optimized for efficiency, power factor, and quiet operation. Better than capacitor-start (auxiliary stays on) or permanent-split (higher starting torque).

---

### 🎯 Q5: Why does a permanent-split capacitor motor run more quietly than a capacitor-start motor?
> **Appeared:** 2017 Q4(b) — (4 marks)

**Full Answer:**

In a **capacitor-start motor**, the auxiliary winding is disconnected by a centrifugal switch at ~75% speed. After disconnection, the motor runs on the main winding only. This produces a pulsating field (not rotating). Pulsating torque causes vibration and noise. The switch click itself adds noise.

In a **permanent-split capacitor motor**, the auxiliary winding and capacitor remain connected at all times. The motor operates as a two-phase machine (approximate 90° phase shift) during both starting and running. The field is more nearly rotating at all speeds. No switch click. No current surge. Smoother, quieter operation.

---

### 🎯 Q6: Prove $X_c = X_a + r_a r_m/(Z_m + X_m)$ for max starting torque of capacitor split-phase motor.
> **Appeared:** 2019 Q6(b) — (4 marks)

**Full Answer:**

For maximum starting torque, $I_m$ and $I_a$ must be 90° apart.

Main winding: $Z_m = r_m + jX_m$. Main current $I_m$ lags $V$ by $\phi_m$.

For 90° between $I_m$ and $I_a$, the auxiliary impedance angle must satisfy:

From phasor geometry and the condition that real and imaginary parts of $I_m \cdot I_a^*$ give zero real product:

$$X_c = X_a + \frac{r_a r_m}{X_m + Z_m}$$

This ensures the auxiliary current leads the main current by exactly 90°, producing maximum starting torque.

---

## Exam Variants

| Year | Question | Marks | Type |
|:---|:---|:---|:---|
| 2017 Q4(b) | Permanent-split vs cap-start noise | 4 | Conceptual |
| 2017 Q4(c) | How auxiliary winding gives starting torque | 4 | Theory |
| 2018 Q8(b) | Split-phase phasor diagram | 4 | Theory |
| 2018 Q8(c) | Capacitor calculation numerical | 4 | Numerical |
| 2019 Q6(b) | Prove $X_c$ formula | 4 | Derivation |
| 2020 Q7(a) | Describe one starting method | 3 | Theory |
| 2021 Q7(b) | Cap-start cap-run operation | 4 | Theory |
| 2021 Q7(c) | Capacitor calculation | 4 | Numerical |
| 2023 Q8(b) | Two starting methods | 6 | Theory |
| 2024 Q8(b) | Two types of 1-phase IM | 6 | Theory |

---

## ⚡ Exam Tips & Common Mistakes

1. **Capacitor-start is the most commonly tested.** Know the circuit, phasor diagram, and principle.
2. **For capacitor numericals:** The key equation is $\tan(90° - \phi_m) = (X_C - X_a)/R_a$.
3. **Don't confuse the three capacitor motor types.** Start-only, run-only (permanent-split), and start+run (two-value).
4. **Shaded-pole direction is fixed:** unshaded to shaded. Cannot be reversed without physical modification.
5. **The centrifugal switch operates at ~75% of $N_s$.** Not at full speed.

## 🔗 Related Topics

- [T-22: DFRT & 1-Phase IM](T-22_DFRT_and_1Phase_IM.md) — Why starting methods are needed
- [T-24: Miscellaneous IM Topics](T-24_Miscellaneous_IM.md) — Single phasing, AC motor classification

---

[← T-22: DFRT & 1-Phase IM](T-22_DFRT_and_1Phase_IM.md) | [🏠 Index](00_Index.md) | [T-24: Miscellaneous IM Topics →](T-24_Miscellaneous_IM.md)
