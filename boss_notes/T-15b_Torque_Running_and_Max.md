[← T-15a: Starting Torque](T-15a_Torque_Starting.md) | [🏠 Index](00_Index.md) | [T-15c: Torque-Speed Curves →](T-15c_Torque_Speed_Curves.md)

---

# T-15b: Running Torque & Breakdown Torque
> **Section:** B | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-34 (Art. 34.23-34.30), VK Mehta Ch-8 (Art. 8.16-8.18), Slides L-04

## Why This Topic Matters

The running torque derivation and the $T_f/T_{\max}$ ratio formula appeared in 4 out of 7 papers. The maximum torque derivation (proving independence from $R_2$) appeared in 2024 for 7 marks. The $T_f/T_{\max}$ numerical with given $R_2$, $X_2$, $s_f$ is a near-guaranteed question. Master this derivation cold.

---

## 📝 Key Definitions

> **Breakdown Torque (Maximum Torque):** "The maximum torque which an induction motor can develop without stalling is known as breakdown torque or pull-out torque." — Theraja, Art. 34.24

> **Slip at Maximum Torque:** "For maximum torque under running conditions, rotor resistance per phase must equal the standstill rotor reactance per phase multiplied by the slip: $R_2 = sX_2$, hence $s_{mT} = R_2/X_2$." — Theraja, Art. 34.25

---

## Running Torque Equation

At running slip $s$, the per-phase rotor quantities are:

$$I_2 = \frac{sE_2}{\sqrt{R_2^2 + (sX_2)^2}}, \qquad \cos\phi_2 = \frac{R_2}{\sqrt{R_2^2 + (sX_2)^2}}$$

Air-gap power: $P_g = 3I_2^2 \cdot R_2/s$. Torque $T = P_g/\omega_s$:

$$\boxed{T = \frac{ksE_2^2 R_2}{R_2^2 + s^2X_2^2}, \qquad k = \frac{3}{2\pi n_s}}$$

where $n_s = N_s/60$ is synchronous speed in rps.

---

## Derivation of Maximum Torque

**Step 1:** Differentiate $T$ with respect to $s$ and set to zero.

Maximize $f(s) = \frac{sR_2}{R_2^2 + s^2X_2^2}$:

$$\frac{df}{ds} = \frac{R_2(R_2^2 + s^2X_2^2) - sR_2 \cdot 2sX_2^2}{(R_2^2 + s^2X_2^2)^2} = 0$$

Numerator = 0:

$$R_2^2 + s^2X_2^2 - 2s^2X_2^2 = 0$$

$$R_2^2 = s^2X_2^2$$

$$\boxed{s_{mT} = \frac{R_2}{X_2}}$$

**Step 2:** Substitute $s = s_{mT} = R_2/X_2$ into the torque equation:

Numerator: $s_{mT} E_2^2 R_2 = \frac{R_2}{X_2} \cdot E_2^2 \cdot R_2 = \frac{R_2^2 E_2^2}{X_2}$

Denominator: $R_2^2 + s_{mT}^2 X_2^2 = R_2^2 + \frac{R_2^2}{X_2^2} \cdot X_2^2 = 2R_2^2$

$$T_{\max} = k \cdot \frac{R_2^2 E_2^2/X_2}{2R_2^2}$$

$$\boxed{T_{\max} = \frac{kE_2^2}{2X_2}}$$

**$R_2$ cancels completely!** Maximum torque depends only on $E_2$ (supply voltage) and $X_2$ (standstill reactance).

> [!IMPORTANT]
> Rotor resistance $R_2$ determines WHERE max torque occurs ($s_{mT} = R_2/X_2$) but NOT its VALUE ($T_{\max} = kE_2^2/2X_2$). Adding rotor resistance shifts the torque peak to higher slip without changing the peak height.

---

## $T_{\max}$ is Proportional to $V^2$

Since $E_2 \propto V$ (stator voltage):

$$T_{\max} \propto E_2^2 \propto V^2$$

A 10% voltage drop reduces $T_{\max}$ by about 19% (since $0.9^2 = 0.81$).

---

## $T_f/T_{\max}$ Ratio Formula

This is one of the most frequently tested formulas. Given $a = s_{mT} = R_2/X_2$ and $s_f$ = full-load slip:

$$\frac{T_f}{T_{\max}} = \frac{ksE_2^2R_2/(R_2^2 + s_f^2X_2^2)}{kE_2^2/(2X_2)}$$

$$= \frac{2s_f R_2 X_2}{R_2^2 + s_f^2 X_2^2} = \frac{2s_f(R_2/X_2)}{(R_2/X_2)^2 + s_f^2}$$

$$\boxed{\frac{T_f}{T_{\max}} = \frac{2as_f}{a^2 + s_f^2}}$$

---

## Worked Example (PYQ 2023)

**2023 Q5(b): 8-pole, 50 Hz IM. $s_f = 2.5\%$, $R_2 = 0.4\,\Omega$, $X_2 = 2.0\,\Omega$. Find $s_{mT}$, speed at $T_{\max}$, and $T_{\max}/T_f$.**

$$N_s = \frac{120 \times 50}{8} = 750 \text{ rpm}$$

**Slip at max torque:**

$$s_{mT} = \frac{R_2}{X_2} = \frac{0.4}{2.0} = \boxed{0.2}$$

**Speed at max torque:**

$$N_{mT} = N_s(1 - s_{mT}) = 750(1 - 0.2) = \boxed{600 \text{ rpm}}$$

**Torque ratio:** Using $a = 0.2$, $s_f = 0.025$:

$$\frac{T_f}{T_{\max}} = \frac{2 \times 0.2 \times 0.025}{0.04 + 0.000625} = \frac{0.010}{0.040625} = 0.246$$

$$\boxed{\frac{T_{\max}}{T_f} = \frac{1}{0.246} = 4.07}$$

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: Derive $T_f/T_{\max} = 2as_f/(a^2 + s_f^2)$.
> **Appeared:** 2017 Q2(b) — (3 marks)

**Full Answer:**

Torque at any slip: $T = ksE_2^2R_2/(R_2^2 + s^2X_2^2)$

Maximum torque (at $s_{mT} = R_2/X_2 = a$): $T_{\max} = kE_2^2/(2X_2)$

Full-load torque at $s_f$: $T_f = ks_fE_2^2R_2/(R_2^2 + s_f^2X_2^2)$

Taking ratio and substituting $a = R_2/X_2$:

$$\frac{T_f}{T_{\max}} = \frac{s_fR_2 \cdot 2X_2}{R_2^2 + s_f^2X_2^2} = \frac{2s_f(R_2/X_2)}{(R_2/X_2)^2 + s_f^2} = \boxed{\frac{2as_f}{a^2 + s_f^2}}$$

---

### 🎯 Q2: Derive the expression for maximum torque and show it is independent of rotor resistance.
> **Appeared:** 2024 Q6(a) — (7 marks)

**Full Answer:**

Torque: $T = ksE_2^2R_2/(R_2^2 + s^2X_2^2)$

Differentiate w.r.t. $s$, set $dT/ds = 0$:

$$R_2^2 + s^2X_2^2 - 2s^2X_2^2 = 0 \implies R_2^2 = s^2X_2^2 \implies s_{mT} = R_2/X_2$$

Substitute $s_{mT}$ back:

Numerator: $s_{mT}E_2^2R_2 = R_2^2E_2^2/X_2$

Denominator: $R_2^2 + s_{mT}^2X_2^2 = 2R_2^2$

$$T_{\max} = k \cdot \frac{R_2^2E_2^2/X_2}{2R_2^2} = \boxed{\frac{kE_2^2}{2X_2}}$$

$R_2$ cancels completely. $T_{\max}$ depends only on $E_2$ and $X_2$.

**Conclusion:** Rotor resistance determines where max torque occurs ($s_{mT} = R_2/X_2$). It has no effect on the value of max torque. Adding external resistance in a wound-rotor motor shifts the peak to higher slip without reducing it.

---

### 🎯 Q3: 8-pole, 50 Hz, $s_f = 2\%$, $R_2 = 0.001\,\Omega$, $X_2 = 0.005\,\Omega$. Find $T_{\max}/T_f$ and speed at $T_{\max}$.
> **Appeared:** 2017 Q2(d), 2019 Q8(c) — (3 marks)

**Full Answer:**

$N_s = 120 \times 50/8 = 750$ rpm

$s_{mT} = R_2/X_2 = 0.001/0.005 = 0.2$

$a = s_{mT} = 0.2$, $s_f = 0.02$

$$\frac{T_f}{T_{\max}} = \frac{2 \times 0.2 \times 0.02}{0.04 + 0.0004} = \frac{0.008}{0.0404} = 0.198$$

$$\boxed{\frac{T_{\max}}{T_f} = \frac{1}{0.198} \approx 5.05}$$

Speed at max torque: $N_{mT} = 750(1 - 0.2) = \boxed{600 \text{ rpm}}$

---

### 🎯 Q4: Show that maximum torque varies proportionally with $V^2$.
> **Appeared:** 2020 Q7(b) — (4 marks)

**Full Answer:**

$E_2 \propto V$ (by transformer action). Maximum torque: $T_{\max} = kE_2^2/(2X_2)$.

Since $E_2 \propto V$: $T_{\max} \propto E_2^2 \propto V^2$.

A 10% voltage drop reduces $T_{\max}$ to $(0.9)^2 = 0.81$ times the original, a 19% reduction. Voltage sags are very damaging to motor performance.

---

### 🎯 Q5: 6-pole, 240V star, 50 Hz IM. $R_2 = 0.12\,\Omega$, $X_2 = 0.85\,\Omega$, $N_1/N_2 = 1.8$, $s_f = 4\%$. Find developed torque, max torque, speed at max torque.
> **Appeared:** 2018 Q6(c) — (5 marks)

**Full Answer:**

$N_s = 120 \times 50/6 = 1000$ rpm $= 16.67$ rps

$k = 3/(2\pi \times 16.67) = 0.02865$

Phase voltage: $V_{ph} = 240/\sqrt{3} = 138.56$ V

Rotor EMF: $E_2 = V_{ph}/(N_1/N_2) = 138.56/1.8 = 76.98$ V

**Full-load torque ($s = 0.04$):**

$$T_f = \frac{0.02865 \times 0.04 \times 76.98^2 \times 0.12}{0.12^2 + 0.04^2 \times 0.85^2} = \frac{0.02865 \times 0.04 \times 5926 \times 0.12}{0.0144 + 0.001156} = \frac{0.815}{0.01556} = \boxed{52.4 \text{ N-m}}$$

**Maximum torque:**

$$T_{\max} = \frac{kE_2^2}{2X_2} = \frac{0.02865 \times 5926}{1.7} = \boxed{99.9 \text{ N-m}}$$

**Speed at max torque:** $s_{mT} = 0.12/0.85 = 0.1412$

$$N_{mT} = 1000(1 - 0.1412) = \boxed{858.8 \text{ rpm}}$$

---

## Exam Variants

| Year | Question | Data | Key Answer |
|:---|:---|:---|:---|
| 2017 Q2(b) | Derive $T_f/T_{\max}$ formula | Theory | $2as_f/(a^2 + s_f^2)$ |
| 2017 Q2(d) | 8-pole numerical | $R_2=0.001$, $X_2=0.005$ | $T_{\max}/T_f = 5.05$ |
| 2018 Q6(c) | 6-pole numerical | 240V, $R_2=0.12$, $X_2=0.85$ | $T_f=52.4$, $T_{\max}=99.9$ |
| 2019 Q8(c) | Same as 2017 Q2(d) | Nearly identical | Same method |
| 2020 Q7(b) | $T_{\max} \propto V^2$ | Theory | Proof |
| 2023 Q5(b) | 8-pole numerical | $R_2=0.4$, $X_2=2.0$ | $T_{\max}/T_f = 4.07$ |
| 2024 Q6(a) | Derive $T_{\max}$, show independent of $R_2$ | 7-mark derivation | $kE_2^2/(2X_2)$ |

---

## ⚡ Exam Tips & Common Mistakes

1. **Don't confuse $s_{mT}$ with $s_f$.** $s_{mT} = R_2/X_2$ is the slip at max torque. $s_f$ is the full-load slip.
2. **$T_{\max}$ formula has $2X_2$ in the denominator.** A common error is writing $X_2$ instead of $2X_2$.
3. **In the $T_f/T_{\max}$ formula, $a = R_2/X_2$ = $s_{mT}$.** Don't confuse with the turns ratio.
4. **Units of $k$:** If $N_s$ is in rps, $k = 3/(2\pi N_s)$. If $N_s$ is in rpm, $k = 3/(2\pi N_s/60)$.
5. **Always check if rotor values are referred to stator.** The question may give $R_2'$ and $X_2'$ (primed = referred).

## 🔗 Related Topics

- [T-15a: Starting Torque](T-15a_Torque_Starting.md) — Special case at $s = 1$
- [T-15c: Torque-Speed Curves](T-15c_Torque_Speed_Curves.md) — Graphical representation
- [T-20: Speed Control](T-20_Speed_Control_and_Braking.md) — Uses $R_2$ variation for speed control

---

[← T-15a: Starting Torque](T-15a_Torque_Starting.md) | [🏠 Index](00_Index.md) | [T-15c: Torque-Speed Curves →](T-15c_Torque_Speed_Curves.md)
