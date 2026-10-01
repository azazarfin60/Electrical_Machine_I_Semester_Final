[← T-10: Auto-Transformer](T-10_Auto-Transformer.md) | [🏠 Index](README.md) | [T-12: Rotating Magnetic Field →](T-12_Rotating_Magnetic_Field.md)

---

# T-11: Miscellaneous Transformer Topics

**ECE 2207 — Explanation Answers (Sorted by Topic)**

> **Topic Overview:** This document compiles all semester final questions and explanation answers on **Miscellaneous Transformer Topics** from 7 years of exams (2017–2024).
> Repeated questions appear once with all exam appearances noted.

---

### Q1(b): Effect of frequency and flux on a transformer

> 📋 **Appeared in:** 2018 Q1(b)

#### Effect of frequency at constant voltage

From $E = 4.44 f N \Phi_m$. If $V_1$ is held constant (and $V_1 \approx E_1$):

$$\Phi_m \approx \frac{V_1}{4.44 f N_1}$$

As $f$ increases: $\Phi_m$ decreases (inversely proportional). Since hysteresis loss $\propto f B_m^{1.6}$ and eddy loss $\propto f^2 B_m^2$, if $B_m$ decreases faster than $f$ increases, iron losses may actually decrease. But leakage reactance $X = 2\pi fL$ increases with $f$, causing more reactive voltage drop across $X_1$ and $X_2'$.

As $f$ decreases (say from 50 Hz to 25 Hz): $\Phi_m$ must double. This pushes the core into saturation. Magnetizing current spikes. Core losses increase sharply. Voltage waveform becomes distorted. This is why transformers must be used at their design frequency.

#### Effect of flux (i.e., effect of supply voltage)

$B_m = \Phi_m / A$ where $A$ is core area. Since $\Phi_m \propto V/f$:
- Higher voltage → higher $B_m$
- Hysteresis loss $\propto B_m^{1.6}$: increases
- Eddy current loss $\propto B_m^2$: increases
- At saturation, the magnetizing current becomes very large and non-sinusoidal, causing third harmonic voltages

The transformer is designed to operate with $B_m$ just below saturation (~1.5 T for silicon steel). Operating it at overvoltage or underfrequency pushes it into saturation.

![Transformer core B-H hysteresis loop and saturation curve](../Books/diagrams/VK_Mehta_Fig_7_56.jpeg)

![Cutaway physical construction view of transformer](../Books/diagrams/Ch-32_p01_transformer.jpg)

---

[← T-10: Auto-Transformer](T-10_Auto-Transformer.md) | [🏠 Index](README.md) | [T-12: Rotating Magnetic Field →](T-12_Rotating_Magnetic_Field.md)
