[← T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) | [🏠 Index](00_Index.md) | [T-15b: Running & Max Torque →](T-15b_Torque_Running_and_Max.md)

---

# T-15a: Starting Torque & Maximum Starting Torque
> **Section:** B | **Priority:** 🟠 HIGH | **Exam Frequency:** 4/7 years
> **Sources:** Theraja Ch-34 (Art. 34.18-34.22), VK Mehta Ch-8 (Art. 8.11-8.12), Slides L-04

## Why This Topic Matters

Starting torque questions appeared in 4 out of 7 papers. The derivation of starting torque and the condition for maximum starting torque ($R_2 = X_2$) are standard 4-6 mark questions. Every wound-rotor motor problem uses this concept. The starting torque formula is also the entry point for all torque analysis.

---

## 📝 Key Definitions

> **Starting Torque ($T_{st}$):** "The torque developed by the motor at the instant of starting is called starting torque. At starting, the rotor is at standstill ($N = 0$, $s = 1$)." — VK Mehta, Art. 8.11

> **Condition for Maximum Starting Torque:** "The starting torque of an induction motor is maximum when rotor resistance per phase equals standstill rotor reactance per phase ($R_2 = X_2$)." — VK Mehta, Art. 8.12

---

## Starting Torque Derivation

At standstill, $s = 1$. All rotor quantities are at their standstill values:

$$E_{2s} = E_2, \quad X_{2s} = X_2, \quad I_2 = \frac{E_2}{\sqrt{R_2^2 + X_2^2}}, \quad \cos\phi_2 = \frac{R_2}{\sqrt{R_2^2 + X_2^2}}$$

Torque is proportional to $E_2 I_2 \cos\phi_2$:

$$T_{st} \propto E_2 \cdot \frac{E_2}{\sqrt{R_2^2 + X_2^2}} \cdot \frac{R_2}{\sqrt{R_2^2 + X_2^2}}$$

$$\boxed{T_{st} = \frac{kE_2^2 R_2}{R_2^2 + X_2^2}}$$

where $k = \frac{3}{2\pi N_s}$ (with $N_s$ in rps).

**For squirrel-cage motors:** $R_2$ is small and fixed. Starting torque is typically 1.5-2 times full-load torque. Starting current is 5-8 times rated.

**For slip-ring motors:** External resistance $R_{ext}$ can be added through slip rings to increase $R_2$ at starting. This increases starting torque and reduces starting current.

---

## Condition for Maximum Starting Torque

To find the $R_2$ that maximizes $T_{st}$, differentiate with respect to $R_2$ and set to zero:

$$\frac{dT_{st}}{dR_2} = kE_2^2 \cdot \frac{(R_2^2 + X_2^2)(1) - R_2(2R_2)}{(R_2^2 + X_2^2)^2} = 0$$

Numerator = 0:

$$R_2^2 + X_2^2 - 2R_2^2 = 0$$

$$X_2^2 = R_2^2$$

$$\boxed{R_2 = X_2}$$

**Maximum starting torque** (substituting $R_2 = X_2$):

$$T_{st,\max} = \frac{kE_2^2 \cdot X_2}{X_2^2 + X_2^2} = \boxed{\frac{kE_2^2}{2X_2}}$$

> [!IMPORTANT]
> Maximum starting torque equals the maximum running torque ($T_{\max}$). Both have the same formula $kE_2^2/(2X_2)$. But they occur at different slips: $T_{st,\max}$ occurs at $s = 1$ when $R_2 = X_2$, while $T_{\max}$ occurs at $s = R_2/X_2$ for any $R_2$.

---

## Effect of Rotor Resistance on Starting Torque

| Condition | Starting Torque | Starting Current | Rotor pf |
|:---|:---|:---|:---|
| $R_2 \ll X_2$ | Low | Very high | Low (mostly reactive) |
| $R_2 = X_2$ | Maximum | Moderate | $\cos 45° = 0.707$ |
| $R_2 \gg X_2$ | Decreasing | Low | High (mostly resistive) |

In wound-rotor motors, external resistance is gradually removed as the motor accelerates. At full speed, slip rings are short-circuited.

---

## 🏆 Golden Questions (Past Exam Archive)

### 🎯 Q1: What is pull-out torque? Derive the equation for maximum starting torque of a 3-phase IM.
> **Appeared:** 2019 Q8(a) — (5 marks)

**Full Answer:**

**Pull-out torque:** The maximum torque a 3-phase IM can develop while running. Also called breakdown torque or $T_{\max}$. If the mechanical load exceeds pull-out torque, the motor stalls.

**Maximum starting torque derivation:**

Starting torque at $s = 1$:

$$T_{st} = \frac{kE_2^2 R_2}{R_2^2 + X_2^2}$$

To find $R_2$ for maximum starting torque, differentiate w.r.t. $R_2$ and set to zero:

$$\frac{dT_{st}}{dR_2} = kE_2^2 \cdot \frac{(R_2^2 + X_2^2) - 2R_2^2}{(R_2^2 + X_2^2)^2} = 0$$

$$R_2^2 + X_2^2 - 2R_2^2 = 0 \implies R_2 = X_2$$

Substituting $R_2 = X_2$:

$$T_{st,\max} = \frac{kE_2^2 X_2}{2X_2^2} = \boxed{\frac{kE_2^2}{2X_2}}$$

Note: $T_{st,\max} = T_{\max}$. When $R_2 = X_2$, the starting torque equals the maximum running torque.

---

### 🎯 Q2: Determine the starting torque of an IM.
> **Appeared:** 2021 Q5(b) — (4 marks)

**Full Answer:**

Starting torque is the torque developed at standstill ($s = 1$).

From the general torque equation at $s = 1$:

$$T_{st} = \frac{k \cdot 1 \cdot E_2^2 R_2}{R_2^2 + (1)^2 X_2^2} = \frac{kE_2^2 R_2}{R_2^2 + X_2^2}$$

where $k = 3/(2\pi N_s)$ and $E_2$ is standstill rotor EMF per phase.

**Effect of rotor resistance:** To maximize $T_{st}$, set $dT_{st}/dR_2 = 0$:

$$R_2^2 + X_2^2 - 2R_2^2 = 0 \implies R_2 = X_2$$

Maximum starting torque at $R_2 = X_2$:

$$T_{st,\max} = \frac{kE_2^2}{2X_2}$$

In wound-rotor motors, external resistance is added to achieve $R_{\text{total}} = X_2$ for maximum starting torque with reduced starting current.

### 🎯 Q3: Define starting and running torque of an induction motor (IM).
> **Appeared:** 2024 Q6(a) — 2 marks

**Full Answer:**

**Starting torque ($T_{st}$):** The torque developed at the instant of starting, when the rotor is stationary, so $s = 1$.
$$T_{st} = \frac{k E_2^2 R_2}{R_2^2 + X_2^2}$$
It depends on rotor resistance, so a wound-rotor motor can raise it by adding external resistance through the slip rings. Usually $1.5$ to $2.5$ times full-load torque.

**Running torque ($T_r$):** The torque developed at any speed after starting, that is at $0 < s < 1$. In the low-slip region
$$T_r \approx \frac{k E_2^2}{R_2}\, s$$
so running torque is very nearly proportional to slip. The motor settles where running torque equals load torque.

**Contrast to state:** starting torque is fixed by $s = 1$ and depends strongly on $R_2$, while running torque varies continuously with slip and, at small slip, is inversely proportional to $R_2$ ($T_r \propto s/R_2$), whereas the breakdown torque $T_{\max}$ is independent of $R_2$.

---

### 🎯 Q4: Determine the average torque of an induction motor if the rotor is assumed to be fully inductive.
> **Appeared:** 2023 Q6(c) — 3 marks

**Full Answer:**

$$T \propto \Phi\, I_2 \cos\phi_2, \qquad \phi_2 = \tan^{-1}\frac{X_2}{R_2}$$

**Fully inductive rotor means $R_2 = 0$, so $\phi_2 = 90^\circ$ and the active component of rotor current is zero.**

**Point-by-point proof.** Let the stator flux density wave be sinusoidal in space: $B(\theta) = B_m \sin\theta$. The rotor emf follows the flux density, and with a purely inductive rotor the current lags that emf by $90^\circ$:
$$i(\theta) = I_m \sin(\theta - 90^\circ) = -I_m \cos\theta$$

The force on a conductor is $F \propto B\, i\, l$, so
$$t(\theta) \propto B_m I_m \sin\theta \cdot (-\cos\theta) = -\frac{B_m I_m}{2} \sin 2\theta$$

Average over one pole pitch ($0$ to $\pi$):
$$T_{av} \propto -\frac{B_m I_m}{2\pi}\int_0^{\pi} \sin 2\theta \, d\theta = 0$$

**Same result from the torque formula:**
$$T = k \Phi I_2 \cos 90^\circ = 0$$

$$\boxed{T_{av} = 0 \ \text{when the rotor is fully inductive } (\phi_2 = 90^\circ)}$$

| Case | $\phi_2$ | Torque over a pole pitch | Average torque |
|:---|:---:|:---|:---|
| Non-inductive | $0^\circ$ | Always positive | Maximum |
| Partly inductive | $0 < \phi_2 < 90^\circ$ | Mostly positive, small reversed band | Reduced |
| Fully inductive | $90^\circ$ | Forward half exactly cancels reverse half | **Zero** |

So an induction motor must have resistance in the rotor circuit. A rotor with zero resistance would produce no net torque at all.

---

### 🎯 Q5: Slip-ring IM, star rotor, 120 V between slip-rings at standstill. $R_2 = 0.3\,\Omega/ph$, $X_2 = 1.5\,\Omega/ph$ at standstill. Find the rotor current/ph at 4% slip, and the slip and rotor current/ph at maximum torque.
> **Appeared:** 2024 Q6(c) — 4 marks

**Full Answer:**

**First convert the slip-ring voltage to a phase voltage.** 120 V is measured **between** the rings, so it is a line voltage. The rotor is star connected:
$$E_{2,\text{ph}} = \frac{120}{\sqrt{3}} = 69.28\text{ V}$$

At slip $s$ the rotor phase emf is $sE_2$ and the rotor phase reactance is $sX_2$.

**(i) Rotor current per phase at $s = 0.04$**
$$E_{2s} = 0.04 \times 69.28 = 2.771\text{ V}$$
$$|Z_r| = \sqrt{0.3^2 + (0.04 \times 1.5)^2} = \sqrt{0.09 + 0.0036} = 0.30594\ \Omega$$
$$I_{2r} = \frac{2.771}{0.30594} = \boxed{9.06\text{ A per phase}}$$

**(ii) Slip and rotor current per phase at maximum torque**
$$s_{mT} = \frac{R_2}{X_2} = \frac{0.3}{1.5} = \boxed{0.2 \ (20\%)}$$
$$|Z_r| = \sqrt{R_2^2 + (s_{mT} X_2)^2} = \sqrt{0.09 + 0.09} = 0.42426\ \Omega$$
$$E_{2s} = 0.2 \times 69.28 = 13.856\text{ V}, \qquad I_{2r} = \frac{13.856}{0.42426} = \boxed{32.7\text{ A per phase}}$$

> [!IMPORTANT] The trap in this question
> 120 V is the voltage **between slip rings**, that is a line voltage. Using 120 V directly as the phase voltage gives the wrong rotor current by a factor of $\sqrt{3}$.

---

---

## Exam Variants

| Year | Question | Type | Key Result |
|:---|:---|:---|:---|
| 2019 Q8(a) | Define pull-out torque + max $T_{st}$ derivation | Theory + derivation | $R_2 = X_2$ for max $T_{st}$ |
| 2021 Q5(b) | Determine starting torque of IM | Derivation | $T_{st} = kE_2^2R_2/(R_2^2 + X_2^2)$ |

---

## ⚡ Exam Tips & Common Mistakes

1. **Don't confuse $T_{st}$ and $T_{\max}$.** $T_{st}$ is torque at $s = 1$ for any $R_2$. $T_{\max}$ is the peak of the torque-slip curve.
2. **$R_2 = X_2$ is for maximum STARTING torque.** The condition for maximum RUNNING torque is $s = R_2/X_2$.
3. **Show the differentiation step.** Writing just "$R_2 = X_2$" without the calculus loses marks.
4. **State $k = 3/(2\pi N_s)$.** Don't leave $k$ undefined.

## 🔗 Related Topics

- [T-15b: Running & Max Torque](T-15b_Torque_Running_and_Max.md) — General torque and breakdown torque
- [T-19: Starting Methods](T-19_Starting_Methods_3Phase.md) — How to implement reduced starting current
- [T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) — Circuit basis for torque equation

---

[← T-14: IM Equivalent Circuit](T-14_IM_Equivalent_Circuit.md) | [🏠 Index](00_Index.md) | [T-15b: Running & Max Torque →](T-15b_Torque_Running_and_Max.md)
