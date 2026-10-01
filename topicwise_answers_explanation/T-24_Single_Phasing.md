# T-24: Single Phasing

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Single Phasing** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### T-24: Single Phasing of Three-Phase Induction Motors: Physical Analysis and Effects

*Appears in: 2018 Q6(a)*

#### What is single phasing?

**Single phasing** is the condition in which one of the three supply lines to a three-phase induction motor becomes open-circuited while the motor is either running or attempting to start. 

Common physical causes include:
- A blown fuse in one phase of the supply distribution board.
- A pitted, charred, or stuck contact on a three-phase electromagnetic contactor or starter.
- A broken overhead supply wire or loose screw terminal.
- An open circuit in one phase of the motor stator winding.

![3-Phase Supply Stator connection showing three phase winding supply](../Books/diagrams/Ch-34_p09_fig11.jpg)

#### Symmetrical component analysis: positive and negative sequence fields

When one line opens (say phase $C$), current in that phase drops to zero ($I_C = 0$). The remaining two lines ($A$ and $B$) carry identical and opposite currents ($I_A = -I_B$). 

Using the method of symmetrical components, this unbalanced two-wire current decomposes into equal positive-sequence and negative-sequence currents:
$$I_{positive} = I_{negative} = \frac{I_A}{\sqrt{3}}$$

This produces two counter-rotating magnetic fields in the machine:
1. **Positive-sequence rotating field:** Rotates in the normal forward direction at synchronous speed $+N_s$, producing forward driving torque.
2. **Negative-sequence rotating field:** Rotates in the opposite direction at $-N_s$. 
   - Because the rotor is spinning forward at speed $N$, the relative slip of the negative-sequence field is:
     $$s_{negative} = \frac{-N_s - N}{-N_s} = 2 - s_{positive} \approx 1.95$$
   - This backward field induces large, high-frequency currents ($\approx 2f = 100\text{ Hz}$) in the rotor bars, generating intense parasitic heat and a counter-braking torque.

---

### Case 1: Motor is already running when single phasing occurs

If the motor is running at rated load when one phase opens:
- **Momentum and continuation:** Due to the inertia of the rotor and load, and because the net torque ($T_f - T_b$) at normal operating slip is positive, the motor does not stop immediately. It continues spinning in the same direction.
- **Speed drop:** Because developed electromagnetic torque is reduced and counter-torque from the backward field opposes motion, the rotor slows down; slip increases from $\approx 3\%$ to $\approx 6–10\%$.
- **Massive current rise in remaining phases:** To maintain the required shaft power output ($P = T \omega \approx \text{const}$) with only two active line wires, the current in the surviving phases increases by:
  $$I_{\text{remaining}} \approx \sqrt{3} \times I_{\text{rated}} \approx 1.73 \text{ to } 2.0 \times I_{\text{rated}}$$
- **Severe thermal overheating:** Since copper loss scales with $I^2$, the two active stator windings experience:
  $$P_{loss} = (1.73)^2 \times P_{loss,\text{rated}} \approx 3 \times \text{Normal Heat Generation}$$
- **Vibration and acoustic noise:** Interaction between the positive- and negative-sequence fields generates a loud, distinct 100 Hz electromagnetic hum and heavy mechanical vibration.

Unless disconnected by a protection device, the stator insulation will burn out within a few minutes.

---

### Case 2: Motor attempts to start with an open phase

If one phase is already open before the motor is energized:
- **Zero starting torque:** At standstill ($N = 0$), both positive and negative sequence fields see slip $s = 1$. The forward starting torque is identical to the backward starting torque ($T_f = T_b$).
- **The motor will not rotate:** Net starting torque is zero. The motor stalls, emitting a loud buzzing or groaning sound.
- **Standstill short-circuit current:** The motor draws locked-rotor current ($5 \times \text{to } 8 \times I_{\text{rated}}$) through the two connected phases without producing back-EMF.
- **Imminent burnout:** Stator winding temperature rises at rates exceeding 10°C to 20°C per second. Winding insulation will be completely destroyed within 5 to 15 seconds unless fast-acting overload protection trips.

---

### Protection against single phasing

Because standard three-phase thermal bimetallic overload relays may respond too slowly to save the motor (especially if the motor was running at partial load where current does not exceed the total trip threshold), specialized protection schemes are required:

1. **Single-Phase Preventers:** Electronic or voltage-sensing relays that detect loss of voltage on any phase or severe voltage unbalance and trip the main contactor within 1 to 2 seconds.
2. **Negative-Sequence Overcurrent Relays:** Filter the line currents and trip instantaneously when negative-sequence current exceeds a safe preset threshold.
3. **Phase-failure monitoring in motor protection circuit breakers (MPCBs):** Modern MPCBs have differential trip mechanisms that accelerate tripping when phase currents are unbalanced.

---
