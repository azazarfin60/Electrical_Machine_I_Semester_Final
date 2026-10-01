# T-12: Rotating Magnetic Field

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Rotating Magnetic Field** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Q5(c): 2-phase supply produces RMF: proof and comparison with 3-phase

> 📋 **Appeared in:** 2021 Q5(c)

#### The proof

Two windings placed at 90° in space, fed by two-phase supply (90° apart in time):

Flux along X-axis: $\Phi_a = \Phi_m\sin\omega t$
Flux along Y-axis: $\Phi_b = \Phi_m\sin(\omega t - 90°) = -\Phi_m\cos\omega t$

Resultant: $\Phi_r = \sqrt{\Phi_a^2 + \Phi_b^2} = \Phi_m = \text{constant}$

The field rotates at $\omega = 2\pi f$ rad/s, giving $N_s = 120f/P$ rpm.

**Comparison:**
- 3-phase produces $\Phi_r = 1.5\Phi_m$ (50% larger than single-phase peak)
- 2-phase produces $\Phi_r = \Phi_m$ (equal to single-phase peak)
- 3-phase is more efficient (higher flux per unit copper)
- 2-phase is only used in specialized applications (servo motors, certain instrumentation)

![Two phase rotating magnetic field phasor diagram and flux vector rotation](../ClassNoteByRaidah/diagrams/class04_fig02_twophase_rmf_phasors.jpg)

---

---

### Q5(a): The RMF proof: 2024 version with emphasis on what each step means

> 📋 **Appeared in:** 2017 Q1(b), 2018 Q6(b), 2021 Q5(c), 2024 Q5(a)

#### The complete physical story

Three stator windings, physically separated by 120° in the stator bore, each carrying a current that is 120° displaced in time from the other two.

The key insight: **each winding produces a field that pulsates along its own axis**. It does not rotate. It alternates.

When you add three pulsating fields from three different fixed directions (120° apart), and each alternates at the same frequency but with a 120° time delay, a remarkable cancellation and reinforcement pattern emerges.

The mathematics showed: at every instant, the vector sum has constant magnitude $1.5\Phi_m$ and rotates at angular frequency $\omega$.

**Why $1.5\Phi_m$ and not $3\Phi_m$?** Because all three phases never peak simultaneously. At any given moment, one phase might be at its peak while the other two are at intermediate values. The maximum achievable vector sum (given the 120° constraints) is $1.5\Phi_m$, not $3\Phi_m$.

Verify: At $\omega t = 90°$: $\Phi_R = \Phi_m$, $\Phi_Y = -\Phi_m/2$, $\Phi_B = -\Phi_m/2$. Vector sum: $\Phi_m + (-\Phi_m/2)e^{j120°} + (-\Phi_m/2)e^{-j120°} = \Phi_m + (-\Phi_m/2)(e^{j120°} + e^{-j120°}) = \Phi_m - \Phi_m \times 2 \times (-1/2)/2$... simplifying: $\Phi_m - (-\Phi_m/2) = 1.5\Phi_m$ (along the R-phase axis). ✓

![Three-phase stator current waveforms and rotating magnetic field flux vectors](../Books/diagrams/Ch-34_p09_fig11.jpg)

![Phasor vector addition of 3-phase fluxes at omega t = 0 and omega t = 60 degrees](../Books/diagrams/Ch-34_p09_fig12_13.jpg)

![Phasor vector addition of 3-phase fluxes at omega t = 120 and omega t = 180 degrees](../Books/diagrams/Ch-34_p10_fig14.jpg)

---

