# T-16: Torque Equations & Characteristics

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Torque Equations & Characteristics** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### IM-02: Maximum Torque is Independent of Rotor Resistance

*Appears in: CT-02 Q1, 2017 Q2b related, 2023 Q5, 2024 Q6a*

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

![Torque-slip characteristics of 3-phase induction motor with varying rotor resistance](../Books/diagrams/Ch-34_p29_fig22.jpg)

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

![Torque-slip curve showing stable and unstable operating regions](../Books/diagrams/Ch-34_p22_fig21.jpg)

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

Since $X_2 = 2\pi f L_2$, and $f$ increased, $X_2$ increased. But $E_2 \propto V/f$, so $E_2^2 \propto V^2/f^2$.

$$T_{\max,2} \propto \frac{V^2/f_2^2}{2 \times 2\pi f_2 L_2} = \frac{V^2}{4\pi f_2^3 L_2} \propto \frac{1}{f^3}$$

**Maximum torque drops as $f^3$** when $V$ is constant. This is severe. A 20% frequency increase reduces max torque to $(1/1.2)^3 = 0.58$ of the original: nearly halved.

**This is why VFDs use V/f control:**

Variable frequency drives always change voltage proportionally with frequency ($V/f = $ constant). This keeps $E_2/f = $ constant, and therefore $E_2/X_2 = $ constant. Maximum torque remains constant at all speeds.

![Complete torque-speed and torque-slip curve across motoring, generating, and braking regions](../Books/diagrams/Ch-34_p34_fig32.jpg)

---

